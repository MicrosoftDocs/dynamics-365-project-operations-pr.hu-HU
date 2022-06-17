---
title: Szállítói számla integrációja
description: Ez a cikk a szállítói számlák Project Operationsben való integrációjával kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912059"
---
# <a name="vendor-invoice-integration"></a>Szállítói számla integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projekthez kapcsolódó beszerzés a(z) Dynamics 365 Project Operations felületen a **Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák** pontban egy függőben lévő szállítói számla bizonylat használatával rögzíthető. További információkért lásd: [Nem raktározott anyagok beszerzése függőben lévő szállítói számlával](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> A cikkben ismertetett funkciók használata előtt tekintse át és alkalmazza a szükséges konfigurációkat. További információkért lásd: [Nem raktározott anyagok és függőben lévő szállítói számlák engedélyezése](../procurement/configure-materials-nonstocked.md).

A Project Operations felületen a projekttel kapcsolatos szállítói számlák feladása speciális könyvelési szabályok alkalmazásával történik:

- A projekttel kapcsolatos költségek (beleértve a vissza nem térítendő adót is) nem kerülnek azonnal kifüggesztették a projekt költségszámlájára a főkönyvben. Ehelyett a költség a **Beszerzési integrációs számlára** kerül. Ez a fiók a **Projektkezelés és könyvelés** > **Beállítás** > **Projektkezelés és könyvelés paraméterei**, **Project Operations a Dynamics 365 Customer engagement felületen** lapon van beállítva.
- A Dual-Write szinkronizálja a szállítói számla adatait a(z) Microsoft Dataverse felületre a következő táblatérképekkel:

     - **Project Operations integrációja projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices)**: Ez a táblatérkép szinkronizálja a szállítói számla fejlécének adatait. Csak a projektazonosítót tartalmazó, legalább egy sort tartalmazó szállítói számlák szinkronizálódnak a(z) Dataverse felületre.
     - **Project Operations integrációja projekt szállítói számlasort exportáló entitása** (msdyn_projectvendorinvoicelines): Ez a táblatérkép szinkronizálja a szállítói számlasor fejlécének adatait. Csak a projektazonosítót tartalmazó sorok szinkronizálódnak a(z) Dataverse felületre.

     > [!NOTE]
     > A szállítói számla részletei a(z) Dataverse felületen nem szerkeszthetők.

Az adó-alrendszeri adatszolgáltatási kötelezettség, a szállítói analitikus és egyéb pénzügyi feladások a szállítói számla feladásakor Dynamics 365 Finance adott esetben kerülnek rögzítésre.

![Szállítói számla integrációja.](media/DW7VendorInvoice.png)

Amikor egy **Szállítói számla** entitásához írnak bejegyzéseket, megkezdődik a(z) Dataverse felületen a bejegyzések automatikus jóváhagyási folyamata. Szükség esetén az automatizált jóváhagyási folyamat állapota a(z) Dataverse felületen a **Kifejlett beállítások** > **Rendszer** > **Rendszeres munkák** pontban ellenőrizhető. A jóváhagyás befejezése után az anyag tranzakció osztályrekordjai létrejönnek a **Tényleges adatok** entitásban.

Az anyagokkal kapcsolatos tényleges adatokat ezután a **Project Operations integration actuals (msdyn_actuals)** kettős írású táblatérkép segítségével dolgozzák fel. További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md).

Az **Importálás az előkészítésből** időszakos folyamat szállítói számlával kapcsolatos Project Operations integrációs naplósorokat hoz létre. Az ellentételezési számla nem teljesít a beszerzésintegrációs számlán. Az integrációs napló kiállításakor a szállítói számla tranzakció számlaegyenlege kiegyenlítődik, és a sor összege átkerül a projekt költségszámlájára. A projekt alkönyvi tranzakciókat is létrehoznak a későbbi számlázási és bevételi elszámolási célokra.
