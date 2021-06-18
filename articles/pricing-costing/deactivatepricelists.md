---
title: Árlisták inaktiválása
description: Ez témakör ismerteti a fel nem használt vagy régi árlisták inaktiválását vagy eltávolítását.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001339"
---
# <a name="deactivate-price-lists"></a>Árlisták inaktiválása 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A régi vagy nem használt árlisták Dynamics 365 Project Operations-ből törénő eltávolításához két lépést kell tennie. 

1. Az árlista eltávolítása vagy törlése az adott oldalakról.
2. Inaktiválja vagy törölje az árlistát az **Árlisták** lap Aktív árlistáiból.

>[!IMPORTANT]
> Az árlista teljes eltávolításához mindkét lépést végre kell hajtania. Csak a 2. lépés végrehajtása – azaz az árlista Akítv árlisták nézetéből való közvetlen törlése vagy inaktiválása – nem elegendő. Az árlista hozzárendelését is törölnie kell az 1. lépésben említett összes helyről.

## <a name="delete-the-price-list-from-specific-pages"></a>Az árlista törlése az adott oldalakról
1. Ha árlistát szeretne törölni a Project Operations alkalmazásból, akkor nyissa meg az alábbi oldalakat:  

      - **Projektparaméterek** oldal > **Árlisták** fül
      - **Szervezeti egység** lap > **Árlisták** rács
      - **Partner** oldal > **Projektárlisták** rács
      - **Projektárajánlatok** lap > **Projektárlisták** rács: Ez az összes aktív projektárajánlatra vonatkozik.
      - **Projektszerződések** lap > **Projektárlisták** rács: Ez az összes aktív projektszerződésre vonatkozik.

 2. Minden oldalhoz ki kell választania a törölni kívánt árlistát, majd a **Törlés** lehetőséget. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Törölje vagy inaktiváljs az árlistát az Árlisták oldalról
 
1. Ha törölni szeretne egy árlistát az aktív árlistákból, menjen az **Értékesítés** > **Ügyfelek** > **Árlisták** lapra. 
2. Válassza ki a törölni kívánt árlistákat, majd kattintson a **Törlés** lehetőségre. Ha az árlista bármely meglévő tranzakcióra hivatkozik, akkor nem fogja tudni törölni. Ha ez történik, inaktiválhatja az árlistát, hogy az ne jelenjen meg egyetlen nézetben sem. 
3. Az árlista inaktiválásához jelölje ki újra az árlistát, majd válassza az **Inaktiválás** lehetőséget.   
