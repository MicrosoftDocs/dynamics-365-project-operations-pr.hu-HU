---
title: A projekt költségei és bevételei
description: Ez a témakör információkat nyújt a projekt költségeinek és bevételeinek megbecsléséről.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fe51af8adb7c3831a57494b8359def2a0176b552efe16feb53a2a265f5ffcb0c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002559"
---
# <a name="project-costs-and-revenue"></a>A projekt költségei és bevételei

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projektbecslések biztosítják a becsült és a projekt ütemezésében ütemezett munka pénzügyi áttekintését. A **Projektek** oldal **Becslések** füle megmutatja a költségek és bevételek hatását a tervezés alatt álló munkára. Információt nyújt számos előre definiált dimenzióról is. 

> ![Becslések fül.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>A projekt költségei és értékesítési értékei

Az árlisták meghatározzák a projektben található szerepkörök költségét és a számlamértékét. A munka költség- és bevételi hatásait meghatározhatja a pozíciónévhez és a feladathoz hozzárendelt elnevezett erőforráshoz társított szerepkörök alapján. Ha vannak olyan feladatok, amelyeknek nincs hozzárendelése (általános vagy megnevezett), akkor nem kaphat költség- vagy eladási becslést. A költségek és az értékesítési értékek figyelembe veszik az árlistákban meghatározott dátumot.

### <a name="default-cost-price"></a>Alapértelmezett beszerzési ár  

Minden projekt szervezethez tartozik. A szervezet neve a **Szerződő részleg** mezőben van feltüntetve. A bekerülési egységár meghatározásához a szerződő részleggel társított árlistát kell használni. A becsléssorokban megadott dátumon meghatározott szerepekhez tartozó helyes költségek meghatározásához keresse meg a szerepkör, az egység és szervezeti egység kombinációját a bekerülésiár-listán. 

A bekerülési ár kiszámításához az összes feladatot hozzá kell rendelni egy erőforráshoz. Bármely nem hozzárendelt feladat bekerülési ára: 0,00.

Ha a szerepkör, az egység és a szervezeti egység kombinációja nem adja meg a bekerülési árat a szerződő részleg árlistájából, a rendszer figyelmen kívül hagyja az egységet. Ehelyett csak a szerep és a szervezeti egység kombinációját keresi. Ha bekerülési ár kerül megállapításra, akkor az átváltási tényezőket kell felhasználni arra, hogy átalakítsák azt a becsléssorban kiválasztott egységre.

Ha a szerepkör és a szervezeti egység kombinációja nem eredményez bekerülési árat, a rendszer figyelmen kívül hagyja a szervezeti egységet. Ehelyett a szerepkör és az egység kombinációját keresi az alapértelmezett ár beállításához (bármilyen konverzió alkalmazása után).

Ha a rendszer nem talál árat a szerepkörre, akkor a becsléssor bekerülési árát az alapértelmezett **0,00** értékre állítja. A projekt költségbecslési soraiban szereplő összes költségösszeget a szerződő részleg pénznemében kell rögzíteni.

> [!NOTE]
> Alapértelmezés szerint a Microsoft Dynamics 365 az alappénznemben tárolja a költségeket. A **Becslések** lapon feltüntetett költségösszegek azonban a szerződő részleg pénznemében vannak megadva.  

### <a name="default-sales-price"></a>Alapértelmezett eladási ár 

Az eladásiár-listát az a értékesítési entitás határozza meg, amelyhez a projektet csatolták, vagy a projekt ügyfele. Ha egy értékesítési entitás, például lehetőség, árajánlat vagy szerződés van társítva a projekthez, akkor az eladási entitás eladási árát az az árlista határozza meg, amely az árajánlathoz vagy a szerződéshez kapcsolódik. Ha az árajánlat vagy a szerződés egyedi árlistával rendelkezik, akkor ezt az árlistát kell használni alapértelmezett eladási árlistaként a projektbecslésekhez. Ha nincs kapcsolat értékesítési entitásokkal, akkor a paraméterekből származó alapértelmezett eladási árlistát kell használni a projekt alapértelmezett eladási árlistájához, amely megegyezik a projektben definiált ügyfélpénznemmel.

Minden becsléssorhoz hozzá van rendelve egy erőforrásbiztosító egység. Az erőforrásbiztosító egység azt a szervezeti egységet jelöli, amelyből az erőforrásokat lefoglalják a feladat elvégzéséhez. A társított szerepek eladási árának meghatározásához keresse meg a szerepkör, az egység és az erőforrásbiztosító egység kombinációját az eladásiár-listán. Ha a feladathoz nincs hozzárendelés, akkor a feladat eladási ára 0,00.

Ha a szerepkör, az egység és az erőforrásbiztosító kombinációja nem ad vissza eladási árat az eladási árlistáról, a rendszer figyelmen kívül hagyja az egységet. Ehelyett csak a szerepkör és az erőforrásbiztosító egység kombinációját keresi. Ha talál eladási árat, akkor a konverziós tényezőket kell felhasználni arra, hogy átszámítsák arra az egységre, amelyet az eladás becsléssorában választott ki. 

Ha a szerepkör és az erőforrásbiztosító kombinációja nem ad vissza eladási árat az eladásiár-listáról, akkor a rendszer figyelmen kívül hagyja az erőforrásbiztosító egységet. Ehelyett a szerepkör és az egység kombinációját keresi az alapértelmezett ár beállításához (bármilyen konverzió alkalmazása után).

Ha a rendszer nem talál árat a szerepkörre, akkor a becsléssor eladási árát alapértelmezett **0,00** értékre állítja.

A **Becslések** lapon van egy rács nézet, amely becsléssorokat mutat. A rács az egység oszlopait, a teljes bekerülési árat és a teljes eladási árat tartalmazza, ahogy az a következő ábrán látható. 

> ![Rács nézet a Becslések lapon.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>A projekt becslések időzített nézete

A projektbecslések időszakos nézete a rács nézetének becsült adatait mutatja az idővonalon a kiválasztott idősávban. Alapértelmezés szerint a becsült adatok a **Szerepkör** dimenzióban vannak elforgatva.

> ![Időszakos nézet a projektbecslésekhez.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>A becsült erőfeszítés elosztása a feladatmód alapján

Az időszakos nézetben a teljes feladatra becsült teljes erőfeszítést elosztja azáltal, hogy az erőfeszítési órákat egységnyi időszakra osztja a kiválasztott idősávban. A feladatmód meghatározza, hogy az erőfeszítéseket hogyan osztják el a feladat időtartama alatt. A kétféle felosztás az **Egyenletes** és a **Munkaidő-alapú**.

### <a name="work-hours-based-allocation"></a>A munkaidő alapú elosztás
 
AZ automatikus ütemezés feladatmódban a feladat erőforrásainak napi alapértelmezett óráit a teljes munkaidő arányában kell beállítani. Ez a viselkedés akkor alkalmazható, amikor az erőfeszítést úgy osztják el, hogy azt az egyes szakaszokban a feladat teljes időtartamára osztják el. Például, ha úgy becsüli, hogy a feladatot egy erőforrás a **Nap** időskálán hajtja végre, a napi kiosztott erőfeszítés nem haladja meg a projektnaptárban meghatározott napi munkaórák számát. Ezért az erőfeszítés-elosztás mindig biztosítja, hogy az erőforrásokat a teljes napra becsüljék meg.

### <a name="even-allocation"></a>Egyenletes elosztás

A kézi ütemezésű feladatmódban a projektnaptárból származó munkaórákat nem veszik figyelembe. Ehelyett a feladat ütemezése a felhasználói bevitelen alapul. Ezeknek a feladatoknak az időegységenkénti erőfeszítés-elosztása a kiválasztott időszakban nem rendelkezik korlátozó tényezővel. A feladat teljes erőfeszítése egyenlően van felosztva és elosztva minden egyes időtartamra a kiválasztott időszakban. Ezért a feladaton definiált feladatmód határozza meg az erőfeszítés-eloszlást, vagy az erőfeszítés elosztását egységidőszakonként az időszakos becslésekben.

## <a name="grouping-and-time-phasing-options"></a>Csoportosítás és időzítési beállítások

Az időszakos nézet az erőfeszítések, költségek és eladások becslésének napi, heti, havi vagy éves eloszlását mutatja. Alapértelmezés szerint a becsült adatok a **Szerepkör** dimenzióban vannak elforgatva. A **Csoportosítás** opcióval azonban két másik dimenzión is elforgatható: ez a **Kategória** és az **Erőforrás**.

Mind a rács nézetben, mind az időszakos nézetben kiválaszthatja, hogy mely mezők jelenjenek meg. Az egyes időblokkok összege a projekt alján látható. Megmutatják a napra, hétre, hónapra vagy évre a teljes becsült erőfeszítést, költséget és értékesítést. Az alapértelmezett bekerülési ár és az eladási ár dátum szerint érvényes. Más szavakkal, minden erőforrás esetén változnak a kiválasztott időszakos nézet alapján.

## <a name="expense-estimates"></a>Költség becslések

Az **Új költségbecslés hozzáadása** gomb segítségével a rács nézetben feljegyezhetők a projekt során felmerülő költségek, amelyek nem közvetlenül kapcsolódnak a munkaerőhöz. Rögzítheti egy adott feladat vagy a teljes projekt költségbecsléseit. Válassza ki a költségkategóriákat és a kezdeti dátumot, amikor várhatóan felmerül a költség. Ha a kapcsolódó bekerülési és az eladási árlista alapértelmezett árakat tartalmaz (vagy ha a költségkategóriákhoz meghatározták a jelölési százalékokat), akkor azok automatikusan bekerülnek a becsléssorba, amikor a társítás megtörténik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]