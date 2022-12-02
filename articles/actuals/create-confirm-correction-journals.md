---
title: Helyesbítő naplók létrehozása és megerősítése
description: Ez a cikk a helyesbítő napló létrehozásáról és megerősítéséről tartalmaz további információt.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928067"
---
# <a name="create-and-confirm-correction-journals"></a>Helyesbítő naplók létrehozása és megerősítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Időnként előfordulhat, hogy egy idő-vagy költségbejegyzés helytelenül van megadva. Előfordulhat például, hogy egy tanácsadó helytelen időpontot választ ki időbejegyzés létrehozásakor, vagy egy költség bevitelekor rossz projektet választ ki. Ha egy tanácsadó nem tudja frissíteni a beküldött bejegyzéseket, a háttéradminisztrátor közvetlenül kijavíthatja a projekthez tartozó tényadatokat.

## <a name="correct-approved-time-entries"></a>Jóváhagyott időbejegyzések kijavítása     

A következő lépések végrehajtásával helyesbítheti a projekt egy vagy több időbejegyzését.

1. Az **Értékesítés** területen jelölje ki a **Tranzakciók** elemet, majd válassza a **Jóváhagyott idő** lehetőséget. 

2. A **Jóváhagyott idő** listájában keressen meg és jelöljön ki egy vagy több jóváhagyott időbejegyzést a helyesbítéshez. A szűrő segítségével megkeresheti a kapcsolódó bejegyzéseket. Szűrheti például a projekt azonosítójára, és kijelölheti a projekt az adott Projektazonosítóval rendelkező összes jóváhagyott időbejegyzést.

3. Válassza a **Bejegyzések helyesbítése** lehetőséget. A rendszer automatikusan létrehoz egy új helyesbítő naplót az **Idő helyesbítése** hozzárendelt típussal. A kijelölt bejegyzéseket a rendszer hozzáadja a naplóhoz. 

4. Az **Új napló** lapon adja meg a helyesbítő napló **Leírását**, majd válassza ki az **Időbejegyzések helyesbítései** lapot.  

5. Az **Időbejegyzések új értékei** részben igény szerint frissítse a mezőket a megfelelő adatokkal. Megváltoztathatja például a hozzárendelt projektet vagy a lefoglalható erőforrást.

6. Válassza a **Előnézet** elemet. A párbeszédpanelen válassza az **OK** lehetőséget. A **Naplósorok** lapon megtekintheti a sztornírozott kijelölt időpontokhoz kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva. Ha további helyesbítésekre van szükség, ismételje meg az 5. és a 6. lépéseket. 

    > [!NOTE]
    > Minden helyesbített tényadatnak ugyanazok az értékei lesznek, mint amelyeket kiválasztott **Időbejegyzések új értékei** szakaszban.

7. Ha a javítások a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget. A párbeszédpanelen válassza az **OK** lehetőséget.

8. Térjen vissza az **Értékesítés** területre, válassza a **Projektek** lehetőséget, majd nyissa meg azt a projektet, amelyhez az imént az időbejegyzéseket frissítette. 

9. A **Projektek** oldalon, a **Tényadatok** lapon tekintse meg a végrehajtott módosításokat. 

    > [!NOTE]
    > Ha a **Tényadatok** lap nem látható, válassza a **Kapcsolódó** > **Tényadatok** lehetőséget.  

10. A **Tényleges adatok társított nézete** listában látható, hogy a sztornírozott eredeti időbejegyzések továbbra is ott vannak, ahogy a hozzájuk tartozó helyesbített időpontok is. 

 
## <a name="correct-approved-expense-entries"></a>Jóváhagyott költségbejegyzések kijavítása

Hajtsa végre az alábbi lépéseket egy vagy több költségbejegyzés kijavításához. 

1. Az **Értékesítés** terület bal oldali navigációs ablaktáblájának **Tranzakciók** területén a **Jóváhagyott kiadások** lehetőséget.

2. A **Jóváhagyott kiadások** listájában jelölje ki a helyesbíteni kívánt projektet, majd válassza a **Bejegyzések helyesbítése** lehetőséget. A rendszer automatikusan létrehoz majd egy új helyesbítő naplót a **Költség helyesbítése** hozzárendelt típussal. 

3. Az **Új napló** lapon adja meg a helyesbítés **Leírását**, és a **Költség javítása** lapon, a **Költségek új értékei** szakaszban jelölje ki a kiválasztott költségsorhoz helyesbíteni kívánt adatmezőket. Például hozzárendelheti a költséget egy másik **Projekthez**, vagy helyesbítheti a **Költségkategóriát**, a **Költség dátumát** vagy a **Lefoglalható erőforrást**.

4. Válassza a **Előnézet** elemet. A párbeszédpanelen válassza az **OK** lehetőséget. 

5. A **Naplósorok** lapon ellenőrizze a javításokat. Megtekintheti a kijelölt költségbejegyzésekhez kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva.

6. Ha a javított értékek a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget. A párbeszédpanelen válassza az **OK** lehetőséget. Ha az értékek nem a várt módon jelennek meg , válassza a **Mégse** lehetőséget a **Jóváhagyott kiadások** listájához való visszatéréshez. Ismételje meg a 2 – 5. lépéseket. 

7. A helyesbítő napló megerősítése után lépjen vissza a frissített projekthez vagy projektekhez, és tekintse meg a változtatásokat.

8. A projekt oldalán a **Tényadatok** lapon tekintse át a **Tényleges adatok társított nézete** listát. Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva.


## <a name="correct-approved-material-usage-logs"></a>Jóváhagyott anyaghasználati naplók javítása

Hajtsa végre az alábbi lépéseket egy vagy több anyaghasználati napló kijavításához.

1. Az **Értékesítés** terület bal oldali navigációs ablaktáblájának **Tranzakciók** területén válassza a **Tényadatok** lehetőséget.

2. A **Tényadatok** listában oszlopszűrők használatával válassza ki az **Anyag** tranzakciós osztályt, hogy csak az anyagok tényadatai legyenek láthatók. Más oszlopszűrőkkel tovább korlátozhatja a látható tényadatokat. Miután megkeresi a kívánt tényadat-készletet, jelölje ki a tényadatokat, majd válassza a **Bejegyzések javítása** lehetőséget. A rendszer automatikusan létrehoz egy új helyesbítő naplót az **Anyag helyesbítése** hozzárendelt típussal.

3. Az **Új napló** oldal **Leírás** mezőjében adja meg a javítás leírását. Ezt követően az **Anyaghelyesbítések** lap **Anyagok új értékei** szakaszában válassza ki az adatmezőket a kijelölt anyagsorok helyesbítéséhez. Az anyagot hozzárendelheti például egy másik projekthez, vagy javíthatja a terméket, az anyagdátumát vagy az alvállalkozói szerződést.

4. Válassza a **Előnézet** elemet. Majd a párbeszédpanelen válassza az **OK** lehetőséget.

5. Ellenőrizze a javításokat a **Naplósorok** lapon. Megtekintheti a sztornírozott kijelölt anyagbejegyzésekhez kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva.

6. Ha a javított értékek a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget. Majd a párbeszédpanelen válassza az **OK** lehetőséget. Ha az értékek nem a várt módon jelennek meg , válassza a **Mégse** lehetőséget a **Tényadatok** listájához való visszatéréshez. Majd ismételje meg a 2 – 5. lépéseket.

7. A helyesbítő napló megerősítése után lépjen vissza a frissített projekthez vagy projektekhez, és tekintse meg a változtatásokat.

8. A projekt oldalán a **Tényadatok** lapon tekintse át a **Tényleges adatok társított nézete** listát. Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
