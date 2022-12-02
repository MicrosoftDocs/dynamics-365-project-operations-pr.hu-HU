---
title: Használjon beszerzési kategóriákat a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz
description: Ez a cikk ismerteti, hogyan konfigurálhatók a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz használható beszerzési kategóriák.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028613"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Használjon beszerzési kategóriákat a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A beszerzési szakemberek a beszerezhető cikkekre és szolgáltatásokra vonatkozó katalógusokat hozhatnak létre, és ezek használhatók a projekt beszerzési rendeléseiben és a függőben lévő szállítói számlákon. A [Beszerzési katalógusokkal](/dynamics365/supply-chain/procurement/procurement-catalogs) egyszerűen kategorizálhatja a beszerzéseket, anélkül hogy konfigurálnia és használnia kellene egy kiadott termékkatalógust. Minden egyes beszerzési kategória leképezható egy projektkategóriára idő-, költség- vagy cikk-tranzakciókhoz. Miután beszerzési kategóriát használó, függőben lévő szállítói számlát feladnak, a rendszer létrehozza az időt, a költség vagy az anyag projekt-tényszámokat, projekttranzakciókat és az alszámla bejegyzéseket.

## <a name="minimum-version-requirements"></a>A minimális verziókövetelmények

A következő verziók szükségesek ahhoz, hogy a beszerzési kategóriákat használjon a beszerzési rendelésekkel a Microsoft Dynamics 365 Project Operations nem készletezett vagy erőforrásalapú forgatókönyvekhez:

- A Project Operations Dataverse megoldás 4.41.0.45 vagy újabb verzióra
- 10.0.26-os vagy újabb pénzügy és műveletek környezetverzió

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kettős írási leképezések futtatása a kategóriatámogatáshoz

Ügyeljen arra, hogy a **Project Operations integrációja projekt szállítói számlasort exportáló entitása\_msdyn_projectvendorinvoicelines** 1.0.0.4 vagy újabb verziót használjon.

## <a name="enable-the-feature-key-for-procurement-categories"></a>A szolgáltatáskulcs engedélyezése a beszerzési kategóriákhoz

A következő lépések alkalmazásával engedélyezheti a beszerzési kategóriák projekt beszerzési rendelésekkel való használatát.

1. A Dynamics 365 Finance-ben lépjen a **Szolgáltatáskezelés** munkaterületre.
1. A szolgáltatáslistában keresse meg a **Beszerzési kategóriák használata a Project Operations alkalmazásban erőforrás-alapú/nem raktározott forgatókönyvekhez** funkciót, és válassza az **Engedélyezés** lehetőséget.

> [!IMPORTANT]
> Előfeltételként engedélyezze a **Project Operations alkalmazásban függőben lévő szállítói számlák engedélyezése az erőforrás-alapú/nem raktározott forgatókönyvekhez** funkciót.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektkategóriák leképezés a Beszerzési kategóriahierarchiában

A következő lépések segítségével leképezi a projektkategóriákat a **Beszerzési kategória** hierarchiára:

1. Ugorjon a **Beszerzés és forrás \> Beszerzési kategóriák pontra**.
1. Válassza ki a **Kategóriahierarchia szerkesztése** lehetőséget.
1. Válassza ki a kívánt kategóriahierarchia csomópontot, majd a **Projektkategóriák hozzárendelése** lapon társítsa a csomópontot a projektkategóriához az **Idő**, **Költség** vagy **Cikk projektje** kategóriához ( vagyis az **Alapértelmezett idő** vagy **Alapértelmezett költség** kategória).
1. Válassza a **Mentés** parancsot.
1. Zárja be a lapot.

> [!NOTE]
> Az beszerzési kategória projektkategóriára való leképezése nem kötelező. Ha a beszerzési kategória nincs leképezve, a rendszer a **Projektkategória alapértelmezései** szakasz **Cikk** mezőjében szereplő értéket használja a **Project Operations a Dynamics 365 Customer engagement alkalmazásban** lapon a **Projektvezetés és könyvelési paraméterek** oldalon.
