---
title: Anyaghasználat rögzítése projekteknél és projektfeladatoknál
description: Ez a cikk információt nyújt arról, hogyan naplózhat anyaghasználatot projekteknél és projektfeladatoknál.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920063"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Anyaghasználat rögzítése projekteknél és projektfeladatoknál

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Miközben a projektcsoport a projekt feladatain dolgozik, anyagokat fogyasztanak el vagy használnak fel. Az anyaghasználati napló lehetővé teszi ennek a használatnak a nyilvántartását annak érdekében, hogy azt a projektmenedzser jóváhagyja, és végül kiszámlázza az ügyfélnek. 

A katalogizált vagy nem kategorizált anyagok használatának rögzítéséhez és a jóváhagyónak való elküldéséhez kövesse az alábbi lépéseket: 

1. A navigációs ablakban válassza az **Anyaghasználat**, majd az **Új** lehetőséget.
2. Az **Új anyaghasználat** lapon adja meg a szükséges anyaghasználati adatokat, majd kattintson a **Mentés** gombra.

Az alábbi tábla az **Anyaghasználati napló** lap mezőiről nyújt tájékoztatást. 

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Ismertetés | Az adott anyaghasználat leírása. | Ennek a mezőnek nincs későbbi hatása. |
| Dátum | Az a dátum, amikor az anyagot várhatóan fel kell használni. | Ennek a mezőnek nincs későbbi hatása. |
| Project | Aktív projektek listája. | Ha projektet választ ki egy anyaghasználati naplóhoz, az hatással van a **Feladat** mezőre, és csak azokat a feladatokat mutatja, amelyek a projektben vannak. |
| Feladatok | A projekttel kapcsolatos feladatok listája, beleértve az összegző és levélcsomópont-feladatokat. | Ha feladatot választ ki egy anyaghasználati naplóhoz, az hatással van a feladat tényleges anyagköltségére és a tényleges anyagértékesítésre. Ha ez a mező üres, a megfelelő anyaghasználati költség és értékesítés csak projektszinten lesz nyomon követve és összegezve. |
| Termék kiválasztása | Adja meg, hogy ez az anyaghasználat **Meglévő** (katalógus) termékhez vagy **Nem katalogizált** termékhez készült-e. | Ez a mező határozza meg a termék típusát. |
| Termék | A termékkatalógus termékazonosítója. Termékazonosító kiválasztásakor a **Termék kiválasztása** mező automatikusan **Meglévő termék** mezővé frissül. Az azonosítót a költség- és értékesítési árak árlistából való beolvasására használják. | Ennek a mezőnek nincs későbbi hatása. |
| Nem katalogizált termék leírása | A termék nevének beírásához használt szövegmező. Ez a mező akkor érhető el, ha a **Termék kiválasztása** mezőben a **Nem katalogizált** termék lehetőséget választja.| Ennek a mezőnek nincs későbbi hatása. |
| Lefoglalható erőforrás| Az az erőforrás, amely ezt az anyagot használta a projektben. Ennek a mezőnek az alapértelmezett beállítása a bejelentkezett felhasználó foglalható erőforrása, de módosítható úgy, hogy a projektcsoport többi tagja nevében rögzítse a használatot. | Ennek a mezőnek nincs későbbi hatása. |
| Egységcsoport | Ebben a mezőben az alapértelmezett érték abból az egységcsoportból származik, amely alapértelmezettként van beállítva a katalógusterméken. A mező frissítésével másik kiszereléscsoportot jelölhet ki. | Ennek a mezőnek nincs későbbi hatása. |
| Kiszerelés | Ebben a mezőben az alapértelmezett érték a kijelölt termék alapértelmezett egysége. A mező frissítésével másik kiszerelést jelölhet ki. | A kiszerelés módosítása eltérő alapértelmezett kiszerelésárat és -költséget eredményez. |
| Mennyiség | A projekten vagy a projektfeladatban használt termék mennyisége. | Ennek a mezőnek nincs későbbi hatása. |
| Egységköltség | A kiválasztott termék és kiszereléskombináció kiszerelésköltsége a vonatkozó önköltségiár-listában beállítottak szerinti. | A kiszerelésköltség mindig a projekt költségpénzében jelenik meg. Ha az árlistában nincs egységköltség a kombinált termékhez és egységhez, az egységköltség alapértelmezés szerint 0,00 lesz. |
| Teljes összeg | A mennyiségi \* kiszerelésköltségként kiszámított költségösszeg.| A költségösszeg mindig a projekt költségpénznemében jelenik meg. |


## <a name="submit-material-usage-for-review-and-approval"></a>Anyaghasználat elküldése ellenőrzésre és jóváhagyásra 
Miután rögzítette az összes anyaghasználatot, és készen áll a jóváhagyásra, el kell küldenie a használati adatokat ellenőrzésre.

1. Menjen az **Anyaghasználati napló** lehetőségre, és jelöljön ki egy vagy több bejegyzést. Vagy jelölje be az összes anyaghasználati rekordot a fejlécen található jelölőnégyzet segítségével.
2. Válassza a **Küldés** lehetőséget. A rendszer feldolgozza a kijelölt bejegyzéseket, majd létrehozza az anyaghasználat-jóváhagyási kérelmeket.

## <a name="recall-a-material-usage-log"></a>Egy anyaghasználati napló visszavonása

Szükség esetén visszahívhat egy beküldött anyaghasználatot. Az anyaghasználati bejegyzés visszahívásához szükséges idő a jóváhagyási szakasztól függ.  Ha a jóváhagyó még nem hagyta jóvá a bejegyzést, akkor a visszahívás azonnal megtörténhet. Ha azonban a bejegyzést már jóváhagyták, a jóváhagyónak jóvá kell hagynia a visszahívást, és vissza kell fordítania a tranzakciókat.

1. Menjen az **Anyaghasználat** lehetőségre, és az anyaghasználati naplók listájában válassza ki a visszahívni kívánt anyaghasználatot.
2. Válassza az **Előhívás** lehetőséget. Ha az anyaghasználati bejegyzést még nem hagyták jóvá, a rendszer azonnal visszahívja azt. Ha az anyagbejegyzést már jóváhagyták, visszahívási kérelem jön létre, amely értesíti a jóváhagyót, hogy vissza szeretné hívni az anyaghasználatot. A jóváhagyó ezután megerősíti, hogy a sztornírozás megtehető, és a tétel visszakerül a rendszerbe.

## <a name="delete-a-material-usage-log"></a>Egy anyaghasználati napló törlése

Törölheti a még el nem küldött anyaghasználati naplókat. A már elküldött anyaghasználati napló törléséhez először vissza kell hívnia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
