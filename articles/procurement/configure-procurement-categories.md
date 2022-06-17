---
title: Beszerzési kategóriák használata projektbeszerzési rendelésekkel és függőben lévő szállítói számlákkal
description: Ez a cikk azt ismerteti, hogyan konfigurálhatja a projektbeszerzési rendelésekkel és a függőben lévő szállítói számlákkal használható beszerzési kategóriákat.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927423"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Beszerzési kategóriák használata projektbeszerzési rendelésekkel és függőben lévő szállítói számlákkal

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A beszerzési szakemberek katalógusokat hozhatnak létre és tarthatnak karban a projekt beszerzési rendeléseiben és a függőben lévő szállítói számlákban használható cikkekről és szolgáltatásokról. [A beszerzési katalógusok](/dynamics365/supply-chain/procurement/procurement-catalogs) egyszerű módot kínálnak a vásárlások kategorizálására anélkül, hogy konfigurálnia és használnia kellene egy kiadott termékkatalógust. Minden beszerzési kategória leképezhető egy projektkategóriára az idő,a költség vagy a cikktranzakciók tekintetében. A beszerzési kategóriát használó, függőben lévő szállítói számla feladása után a rendszer idő-, költség- vagy anyagprojekt-tényeket, projekttranzakciókat és a továbbadó bejegyzéseket hoz létre.

## <a name="minimum-version-requirements"></a>Minimális verziókövetelmények

A következő verziók szükségesek ahhoz, hogy a beszerzési kategóriákat projektvásárlási rendelésekkel együtt használhassa a Microsoft Dynamics 365 Project Operations nem készletezett/erőforrás-alapú forgatókönyveihez:

- Project Operations-megoldás Dataverse 4.41.0.45-es vagy újabb verziója
- Finance and Operations környezet 10.0.26-os vagy újabb verzió

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kétírásos térképek futtatása beszerzési kategória támogatásához

Győződjön meg arról, hogy a Project Operations integrációs projekt szállítói számlaexportálási entitás msdyn **projectvendorinvoicelines leképezése \_** 1.0.0.4 vagy újabb verziót használ.

## <a name="enable-the-feature-key-for-procurement-categories"></a>A funkciókulcs engedélyezése beszerzési kategóriákhoz

Kövesse az alábbi lépéseket a beszerzési kategóriák projektbeszerzési rendelésekkel való használatának engedélyezéséhez.

1. A Dynamics 365 Finance nyissa meg a **Funkciókezelés** munkaterületet.
1. A szolgáltatáslistában keresse meg a Beszerzési kategóriák használata a **Project Operations erőforrás-alapú/nem készletezett forgatókönyvekhez** funkciót, majd válassza az Engedélyezés **lehetőséget**.

> [!IMPORTANT]
> Előfeltételként engedélyeznie kell a Függőben lévő szállítói számlák engedélyezése a **Project Operationsben erőforrás-alapú/nem készletezett forgatókönyvekhez** funkciót is.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektkategóriák leképezése a Beszerzési kategóriahierarchiában

Kövesse az alábbi lépéseket a projektkategóriák beszerzési kategóriákra való leképezéséhez a **Beszerzési kategóriahierarchiában**:

1. Lépjen a Beszerzési és forrásbeszerzési **kategóriákhoz.\>**
1. Válassza a Kategóriahierarchia **szerkesztése lehetőséget**.
1. Válassza ki a kívánt kategóriahierarchia-csomópontot, majd a **Projektkategóriák** hozzárendelése lapon társítsa a csomópontot a projektkategóriához az **Idő**, **Költség** vagy **Cikkprojekt** kategóriából (azaz az Alapértelmezett idő **vagy** az **Alapértelmezett költség** kategóriából).
1. Válassza a **Mentés** parancsot.
1. Zárja be a lapot.

> [!NOTE]
> A beszerzési kategória projektkategóriához való hozzárendelése nem kötelező. Ha egy beszerzési kategória nincs leképezve, a rendszer azt az értéket fogja használni, amely a **Projektkategória alapértelmezései** szakasz Cikk **mezőjében van beállítva a** **Project Operations on Dynamics 365 Customer engagement** lap **Projektmenedzsment és könyvelési** paraméterek lapján.
