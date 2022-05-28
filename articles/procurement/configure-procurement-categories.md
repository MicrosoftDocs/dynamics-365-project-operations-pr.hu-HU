---
title: Beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal
description: Ez a témakör a projekt beszerzési rendeléseivel és a függőben lévő szállítói számlákkal használható beszerzési kategóriák konfigurálását ismerteti.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613334"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A beszerzési szakemberek katalógusokat hozhatnak létre és tarthatnak fenn a projekt beszerzési rendelésekben és a függőben lévő szállítói számlákban használható cikkekről és szolgáltatásokról. [A beszerzési katalógusok](/dynamics365/supply-chain/procurement/procurement-catalogs) egyszerű módot kínálnak a vásárlások kategorizálására anélkül, hogy konfigurálnia és használnia kellene egy kiadott termékkatalógust. Minden beszerzési kategória hozzárendelhető egy projektkategóriához az idő-, költség- vagy cikktranzakciókhoz. A beszerzési kategóriát használó függőben lévő szállítói számla feladása után a rendszer idő-, költség- vagy anyagprojekt-tényleges adatokat, projekttranzakciókat és analitikus tételeket hoz létre.

## <a name="minimum-version-requirements"></a>Minimális verziókövetelmények

A következő verziók szükségesek ahhoz, hogy beszerzési kategóriákat használjon a Microsoft Dynamics 365 Project Operations nem raktározott/erőforrás-alapú forgatókönyvek projekt beszerzési rendeléseivel:

- A Project Operations Dataverse megoldás 4.41.0.45 vagy újabb verziója
- Pénzügyi és üzemeltetési környezet 10.0.26-os vagy újabb verziója

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kettős írású térképek futtatása a beszerzési kategória támogatásához

Győződjön meg arról, hogy a Project Operations integrációs projekt szállítói számlasor-exportálási entitásának msdyn **projectvendorinvoicelines\_ hozzárendelése** 1.0.0.4 vagy újabb verziót használ.

## <a name="enable-the-feature-key-for-procurement-categories"></a>A szolgáltatáskulcs engedélyezése beszerzési kategóriákhoz

Az alábbi lépéseket követve engedélyezheti a beszerzési kategóriák projekt beszerzési rendelésekkel való használatának funkcióit.

1. A Dynamics 365 Finance nyissa meg a **Szolgáltatáskezelés** munkaterületet.
1. A szolgáltatáslistában keresse meg a Beszerzési kategóriák használata a **Projektműveletek erőforrásalapú/nem raktározott forgatókönyvekhez** szolgáltatásban, majd válassza az Engedélyezés **lehetőséget**.

> [!IMPORTANT]
> Előfeltételként engedélyeznie kell a Függőben lévő szállítói számlák engedélyezése a **Projektműveletek szolgáltatásban erőforrásalapú/nem raktározott forgatókönyvekhez** funkciót is.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektkategóriák leképezése a Beszerzési kategória hierarchiájában

Az alábbi lépéseket követve a projektkategóriákat a Beszerzési kategória **hierarchiájában szereplő** beszerzési kategóriákhoz rendelheti:

1. Ugrás a **Beszerzési és beszerzési \> beszerzési kategóriákra**.
1. Válassza **a Kategóriahierarchia szerkesztése lehetőséget**.
1. Válassza ki a kívánt kategóriahierarchia-csomópontot, majd a Projektkategóriák **hozzárendelése lapon társítsa a csomópontot az Idő**, Költség**vagy **,Cikkprojekt** kategória (azaz az Alapértelmezett idő vagy **az** Alapértelmezett költség **kategória**) projektkategóriájához **.**
1. Válassza a **Mentés** parancsot.
1. Zárja be a lapot.

> [!NOTE]
> Beszerzési kategória hozzárendelése projektkategóriához nem kötelező. Ha egy beszerzési kategória nincs leképezve, a rendszer a Projektmenedzsment és könyvelési paraméterek **lap Projektműveletek a Dynamics 365 ügyfélkapcsolati lapján a Projektműveletek** **a** Dynamics 365-ön ügyfélkapcsolati **lapon** a Cikk **mezőben** beállított értéket fogja használni.
