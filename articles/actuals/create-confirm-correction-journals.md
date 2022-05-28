---
title: Helyesbítő naplók létrehozása és megerősítése
description: Ez a témakör a helyesbítő napló létrehozásáról és megerősítéséről tartalmaz további információt.
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
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582806"
---
# <a name="create-and-confirm-correction-journals"></a>Helyesbítő naplók létrehozása és megerősítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Előfordulhat, hogy egy idő- vagy költségbejegyzés helytelenül van megadva. Előfordulhat például, hogy egy tanácsadó rossz dátumot választ ki időbejegyzés létrehozásakor, vagy rossz projektet választ ki költség megadásakor. Ha egy tanácsadó nem tudja frissíteni a beküldött bejegyzéseket, a háttéradminisztrátor közvetlenül kijavíthatja a projekt tényleges adatait.

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

7. Miután megerősítette a javítási naplót, térjen vissza a frissített projekthez vagy projektekhez a módosítások megtekintéséhez.

8. A projektlap **Tényleges adatok** lapján tekintse át a **Tényleges társított nézet** listát. Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva.


## <a name="correct-approved-material-usage-logs"></a>Jóváhagyott anyaghasználati naplók javítása

Egy vagy több anyaghasználati naplóbejegyzés kijavításához hajtsa végre az alábbi lépéseket.

1. **Az Értékesítés** területen, a bal oldali navigációs ablakban, a Tranzakciók **csoportban** válassza a Ténylegesek **lehetőséget**.

2. **A Ténylegesek** listában oszlopszűrőkkel válassza ki az **Anyagtranzakció** osztályt, hogy csak az anyagok tényleges adatai jelenjenek meg. Más oszlopszűrők használatával tovább korlátozhatja a megjelenített tényleges adatokat. Miután megtalálta a kívánt tényleges adatokat, válassza ki a tényleges adatokat, majd válassza a Tételek javítása **lehetőséget**. A rendszer automatikusan létrehoz egy új korrekciós naplót, és hozzárendeli az **Anyagkorrekció** típusát.

3. **Az Új napló** lap Megnevezés **mezőjében** adja meg a javítás leírását. Ezután az **Anyagkorrekció lap Anyagkorrekció** **lapján** válassza ki a kijelölt anyagsorokhoz helyesbíteni kívánt adatmezőket. Hozzárendelheti például az anyagot egy másik projekthez, vagy kijavíthatja a terméket, az anyagdátumot vagy az alvállalkozói szerződést.

4. Válassza a **Előnézet** elemet. Ezután a párbeszédpanelen válassza az OK **lehetőséget**.

5. **A Naplósorok** lapon ellenőrizze a javításokat. Megtekintheti a sztornírozott kijelölt anyagtételekhez és a létrehozott helyesbített megfelelő sorokhoz kapcsolódó eredeti tényleges értékek listáját.

6. Ha a javított értékek a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget. Ezután a párbeszédpanelen válassza az OK **lehetőséget**. Ha az értékek nem a várt módon jelennek meg, válassza a Mégse gombra **a** **Ténylegesek** listához való visszatéréshez. Ezután ismételje meg a 2-től 5.-ig terjedő lépéseket.

7. Miután megerősítette a javítási naplót, térjen vissza a frissített projekthez vagy projektekhez a módosítások megtekintéséhez.

8. A projektlap **Tényleges adatok** lapján tekintse át a **Tényleges társított nézet** listát. Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
