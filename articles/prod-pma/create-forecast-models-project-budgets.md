---
title: Előrejelzési modellek létrehozása a projektköltségvetésekhez
description: Ez a témakör ismerteti, hogyan lehet előrejelzési modellt létrehozni a fennmaradó költségvetésekhez.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078228"
---
# <a name="create-forecast-models-for-project-budgets"></a>Előrejelzési modellek létrehozása a projektköltségvetésekhez 

[!include [banner](../includes/banner.md)]

Ez a témakör ismerteti, hogyan lehet előrejelzési modellt létrehozni a fennmaradó költségvetésekhez. Egy költségvetés-ellenőrzés alá tartozó projekt a következő két típusú költségvetést használja: eredeti és fennmaradó. A projektek költségvetésének létrehozásakor meg kell adnia az **Előrejelzési modellek** lapon létrehozott eredeti és fennmaradó költségvetési előrejelzési modelleket. A projektek költségvetések a megadott modellek alapján jönnek létre, amikor véglegesíti a projekt költségvetését.

> [!NOTE]
> A költségvetés-ellenőrzéshez használt előrejelzési modell nem lehet almodell vagy nem használható almodellként.

1. Válassza a **Projektmenedzsment és könyvelés** > **Beállítások** > **Előrejelzések**  > **Előrejelzési modellek** lehetőséget.
2. Új előrejelzési modell létrehozásához válassza az **Új** lehetőséget, majd adja meg az új modellhez tartozó modellszámot és nevet. 
3. Állítsa be a **Leállítva** beállítást **Igen** értékre az előrejelzési modellre vonatkozó előrejelzési sorok módosulásának elkerülése érdekében. 
4. Ha a modellhez társított előrejelzési sorokban pénzforgalmi előrejelzéseket kell létrehoznia a főkönyvben, akkor állítsa be a **Pénzforgalmi előrejelzések befoglalása** beállítást **Igen** értékre. 
5. Ha a projekt dátumát szeretné számlázási dátumként használni, akkor állítsa az **Előrejelzési számla dátuma** beállítást **Igen** értékre. 
6. A **Költségvetés típusa** mezőben válassza ki a következő modelltípusok egyikét:

   - **Eredeti költségvetés** : A kezdeti költségvetés létrehozásakor és jóváhagyásakor meghatározott eredeti költségvetési összegek használata.
   - **Fennmaradó költségvetés** : A projekt élettartama során a fennmaradó költségvetési összegeket használja. Az ebben az előrejelzési modellben szereplő egyenlegeket a rendszer a tényleges tranzakciókkal csökkenti, és a költségvetési módosítások szerint növeli vagy csökkenti.
   - **Átvitel** : A projekthez tartozó átviteli költségvetés összegeit használja. Az átvitel egy opcionálisfolyamat, amely a fel nem használt költségvetési összegek átvitelére szolgál az egyik pénzügyi évből a másikba.

7. Végezze el a következő beállításokat igény szerint:

   - Ha a projekt dátumát szeretné számlázási dátumként használni, akkor használja az **Előrejelzési számla dátuma** beállítást.
   - Engedélyezze az **Előrejelzés folyamatban lévő munkával** lehetőséget, hogy előrejelzést készítsen folyamatban lévő munka alapján, majd válassza ki a folyamatban lévő munka típusát. 
   - Az alapértelmezett **Költségvetési** típust **Nincs** értékként hagyhatja, vagy új típust adhat meg. A költségvetés típusa a rekord módosítása után nem módosítható.     
    > [!NOTE]
    > Ha módosítja az alapértelmezett költségvetési típust, akkor az összes többi lehetőség nem lesz elérhető a frissítésekhez, és ez az előrejelzési modell nem használható fel újra. 
   


 

