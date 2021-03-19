---
title: Helyesbítő naplók létrehozása és megerősítése
description: Ez a témakör a helyesbítő napló létrehozásáról és megerősítéséről tartalmaz további információt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276936"
---
# <a name="create-and-confirm-correction-journals"></a>Helyesbítő naplók létrehozása és megerősítése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Időnként előfordulhat, hogy egy idő-vagy költségbejegyzés helytelenül van megadva. Előfordulhat például, hogy egy tanácsadó helytelen időpontot választki időbejegyzés létrehozásakor, vagy egy költség bevitelekor felcserél számokat. Ha egy tanácsadó nem tudja frissíteni a beküldött bejegyzéseket, az adminisztrátor közvetlenül kijavíthatja a projekthez tartozó bejegyzést.

A jelen témakör eljárásainak végrehajtásához rendszergazdai jogosultságokra van szükség.

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

A következő ábrán például két olyan sor tétel szerepel, amelyek mennyisége 8,00 és terhelések tartoznak hozzájuk a Mennyiség oszlopban. Emellett két olyan sor tétel szerepel, amelynek mennyisége -8,00, és ezekhez az Összeg oszlopban jóváírás látható. Ezek a javítások nullára módosítják a mennyiséget.

 
## <a name="correct-approved-expense-entries"></a>Jóváhagyott költségbejegyzések kijavítása

Hajtsa végre az alábbi lépéseket egy vagy több költségbejegyzés kijavításához. 

1. Az **Értékesítés** terület bal oldali navigációs ablaktáblájának **Tranzakciók** területén a **Jóváhagyott kiadások** lehetőséget.

2. A **Jóváhagyott kiadások** listájában jelölje ki a helyesbíteni kívánt projektet, majd válassza a **Bejegyzések helyesbítése** lehetőséget. A rendszer automatikusan létrehoz majd egy új helyesbítő naplót a **Költség helyesbítése** hozzárendelt típussal. 

3. Az **Új napló** lapon adja meg a helyesbítés **Leírását**, és a **Költség javítása** lapon, a **Költségek új értékei** szakaszban jelölje ki a kiválasztott költségsorhoz helyesbíteni kívánt adatmezőket. Például hozzárendelheti a költséget egy másik **Projekthez**, vagy helyesbítheti a **Költségkategóriát**, a **Költség dátumát** vagy a **Lefoglalható erőforrást**.

4. Válassza a **Előnézet** elemet. A párbeszédpanelen válassza az **OK** lehetőséget. 

5. A **Naplósorok** lapon ellenőrizze a javításokat. Megtekintheti a kijelölt költségbejegyzésekhez kapcsolódó eredeti tényadatok listáját, valamint a hozzájuk tartozó helyesbített sorokat, amelyek létre lettek hozva.

6. Ha a javított értékek a várt módon jelennek meg ,válassza a **Jóváhagyás** lehetőséget. A párbeszédpanelen válassza az **OK** lehetőséget. Ha az értékek nem a várt módon jelennek meg , válassza a **Mégse** lehetőséget a **Jóváhagyott kiadások** listájához való visszatéréshez. Ismételje meg a 2 – 5. lépéseket. 

> [!NOTE]
> Minden helyesbített tényadatnak ugyanazok az értékei lesznek, mint amelyeket kiválasztott **Költségek új értékei** szakaszban.

7. A helyesbítő napló megerősítése után lépjen vissza a frissített projekthez vagy projektekhez, és tekintse meg a változtatásokat.  

8. A projekt oldalán a **Tényadatok** lapon tekintse át a **Tényleges adatok társított nézete** elemet. Az eredeti bejegyzések és a helyesbített bejegyzések vannak felsorolva. A következő ábra az eredeti költségbejegyzés összegeket, illetve az azokhoz tartozó helyesbített költségbejegyzés-mennyiségeket. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]