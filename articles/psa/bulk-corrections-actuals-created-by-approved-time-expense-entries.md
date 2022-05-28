---
title: A jóváhagyott idő-és költség tételek által létrehozott tényadatok tömeges javítása
description: Ez a témakör ismerteti, hogy egy adminisztrátor számára hogyan lehetséges a korábban jóváhagyott idő vagy kiadási tételekre egyszeri vagy tömeges helyesbítéseket végezni, ha a számlázás nem fejeződött be.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 107ba01f2fd5717e1717824631aeee099d8a8205
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683365"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>A jóváhagyott idő-és költség tételek által létrehozott tényadatok tömeges javítása

[!include [banner](../includes/psa-now-project-operations.md)]

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
