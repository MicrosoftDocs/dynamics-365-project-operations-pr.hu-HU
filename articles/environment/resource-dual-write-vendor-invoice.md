---
title: Szállítói számla integrációja
description: Ez témakör a Project Operations szolgáltatásban lévő szállítói számlák integrációjáról nyújt információt.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955770"
---
# <a name="vendor-invoice-integration"></a>Szállítói számla integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projekthez kapcsolódó beszerzés a(z) Dynamics 365 Project Operations felületen a **Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák** pontban egy függőben lévő szállítói számla bizonylat használatával rögzíthető. További információkért lásd: [Nem raktározott anyagok beszerzése függőben lévő szállítói számlával](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Mielőtt a jelen témakör leírt funkciókat használod, tekintsd át és alkalmazd a szükséges konfigurációkat. További információkért lásd: [Nem raktározott anyagok és függőben lévő szállítói számlák engedélyezése](../procurement/configure-materials-nonstocked.md).

A Project Operations felületen a projekttel kapcsolatos szállítói számlák feladása speciális könyvelési szabályok alkalmazásával történik:

- A projekttel kapcsolatos költségek (beleértve a vissza nem térítendő adót is) nem kerülnek azonnal kifüggesztették a projekt költségszámlájára a főkönyvben. Ehelyett a költség a **Beszerzési integrációs számlára** kerül. Ez a fiók a **Projektkezelés és könyvelés** > **Beállítás** > **Projektkezelés és könyvelés paraméterei**, **Project Operations a Dynamics 365 Customer engagement felületen** lapon van beállítva.
- A Dual-Write szinkronizálja a szállítói számla adatait a(z) Microsoft Dataverse felületre a következő táblatérképekkel:

     - **Project Operations integrációja projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices)**: Ez a táblatérkép szinkronizálja a szállítói számla fejlécének adatait. Csak a projektazonosítót tartalmazó, legalább egy sort tartalmazó szállítói számlák szinkronizálódnak a(z) Dataverse felületre.
     - **Project Operations integrációja projekt szállítói számlasort exportáló entitása** (msdyn_projectvendorinvoicelines): Ez a táblatérkép szinkronizálja a szállítói számlasor fejlécének adatait. Csak a projektazonosítót tartalmazó sorok szinkronizálódnak a(z) Dataverse felületre.

     > [!NOTE]
     > A szállítói számla részletei a(z) Dataverse felületen nem szerkeszthetők.

Az adózói alkönyv, a szállítói alkönyv és egyéb pénzügyi könyvelések a szállítói számla Dynamics 365 Finance felületen való könyvelésekor kerülnek rögzítésre.

![Szállítói számla integrációja](media/DW7VendorInvoice.png)

Amikor egy **Szállítói számla** entitásához írnak bejegyzéseket, megkezdődik a(z) Dataverse felületen a bejegyzések automatikus jóváhagyási folyamata. Szükség esetén az automatizált jóváhagyási folyamat állapota a(z) Dataverse felületen a **Kifejlett beállítások** > **Rendszer** > **Rendszeres munkák** pontban ellenőrizhető. A jóváhagyás befejezése után az anyag tranzakció osztályrekordjai létrejönnek a **Tényleges adatok** entitásban.

Az anyagokkal kapcsolatos tényleges adatokat ezután a **Project Operations integration actuals (msdyn_actuals)** kettős írású táblatérkép segítségével dolgozzák fel. További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md).

Az **Importálás az előkészítésből** időszakos folyamat szállítói számlával kapcsolatos Project Operations integrációs naplósorokat hoz létre. Az ellentételezési számla nem teljesít a beszerzésintegrációs számlán. Az integrációs napló kiállításakor a szállítói számla tranzakció számlaegyenlege kiegyenlítődik, és a sor összege átkerül a projekt költségszámlájára. A projekt alkönyvi tranzakciókat is létrehoznak a későbbi számlázási és bevételi elszámolási célokra.
