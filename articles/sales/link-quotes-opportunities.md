---
title: Projektárajánlatok létrehozása lehetőségekből
description: Ez a témakör a projektárajánlatok lehetőségekből történő létrehozását ismerteti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898535"
---
# <a name="create-project-quotes-from-opportunities"></a>Projektárajánlatok létrehozása lehetőségekből

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az árajánlatokat a következő módszerekkel lehet létrehozni a projektlehetőségekből:

- Az **Árajánlatok** lapról a **Projektlehetőség** oldalon
- A lehetőség értékesítési folyamatából
- A lehetőség hivatkozásának egy meglévő árajánlaton történő frissítésével

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Az Árajánlatok lapról a Projektlehetőség oldalon

Ha projektárajánlatot szeretne létrehozni egy lehetőségből, hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Projektlehetőség** oldalt, és válassza az **Árajánlatok** lapot. 
2. Az **Árajánlatok** alrácson válassza a **+** lehetőséget, ha a lehetőség alapján új árajánlatot szeretne létrehozni. A rendszer az összes lehetőségsort és a kapcsolódó projektárlistákat átmásolja az új árajánlatba a lehetőségből.

## <a name="from-the-opportunity-sales-process-flow"></a>A lehetőség értékesítési folyamatából

Ha egy árajánlatot szeretne létrehozni a lehetőség értékesítési folyamatából, hajtsa végre az alábbi lépéseket.

1. A lehetőség értékesítési folyamatából nyissa meg a lehetőséget.
2. Válassza a **Minősítés** fázist. 
3. Válassza **Tovább** lehetőséget, majd a **+ Létrehozás** lehetőséget úr árajánlat létrehozásához. Az új ajánlat **Összegzés** lapján található információk nagy része alapértelmezés szerint a lehetőségből fog megjelenni. 
4. Írja be a hiányzó szükséges adatokat, vagy szükség szerint frissítse az alapértelmezett értékeket az **Összesítés** lapon,
5. Válassza a **Mentés** parancsot. Létrejön az új árajánlat, és a lehetőséghez lesz társítva. Ezután megtekintheti az árajánlat adatait az **Árajánlatok** lapon a **Lehetőség** oldalon. 

   A lehetőség értékesítési folyamata a következő fázisba lép át: **Ajánlat**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>A lehetőség hivatkozásának egy meglévő árajánlaton történő frissítésével

A meglévő árajánlatok a lehetőséghez csatolhatók. Hajtsa végre az alábbi lépéseket a meglévő árajánlaton szereplő lehetőségadatok frissítéséhez.

1. Nyissa meg az **Árajánlat** oldalt, és válassza az **Összegzés** lapot.
2. A **Lehetőség** mezőben jelölje ki azt a lehetőséget, amelyet az árajánlathoz szeretne csatolni. Az árajánlatot a lehetőség **Árajánlatok** rácsában tekintheti meg. 
3. A lehetőség értékesítési folyamata segítségével a lehetőség áthelyezhető a következő fázisba: **Ajánlat**. 

   Ha a lehetőséget ebbe a fázisba helyezi, akkor ezt az árajánlatot a lehetőséghez társított árajánlatok listájából választhatja ki. Az árajánlat kiválasztása azt jelzi, hogy továbbhalad vele.

   A lehetőséghez kapcsolódó összes egyéb árajánlat továbbra is elérhető lesz, és mindaddig aktív marad, amíg az egyiket el nem nyerik. Az értékesítési folyamatot visszahelyezheti az előző (**Minősítés**) fázisba, és másik ajánlatot választhat ki, amellyel továbbléphet.
