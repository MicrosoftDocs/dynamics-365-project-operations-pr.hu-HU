---
title: Projekthez tartozó becsült költség és bevétel meghatározása
description: Projektköltség meghatározása és a bevétel megbecslése a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148826"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Projekthez tartozó becsült költség és bevétel meghatározása 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

A projekt becslések a megbecsült és ütemezett munka pénzügyi nézetét adják a projekt munkalebontási struktúrában. A becslések nézet tájékoztatja a tervezett munka bevétel hatásáról és a költségekről. A becslések nézet eszközt nyújt az információk megtekintéséhez az előre meghatározott dimenziók számáról, hogy a lehető legjobban értesüljön a projekt pénzügyi hatásairól.  
  
## <a name="cost-and-sales-value-of-the-project"></a>A projekt költségi és értékesítési értéke  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] árlisták meghatározzák a projekt által használt szerepkörök költség- és számlázási mértékét. A projekt munkalebontási struktúrában a feladatokkal társított szerepkörökön alapján meghatározhatja a munka költség és jövedelem hatását.  
  
## <a name="cost-price-defaulting"></a>Önköltségi ár alapértelmezése  
Minden egyes projekthez tartozik egy szervezet (a projektben feltüntetett **Tulajdonos Egység** ). A tulajdonos szervezeti egységével társított árlista a kiszerelés önköltségi árát határozza meg. A(z) [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] meghatározza az önköltségi ár szerepköreit a szerepkörök kombinációjának és az önköltségi listában szereplő szervezeti egységek megkeresésével annak érdekében, hogy a becslési sorokban az adat érvényességéhez a megfelelő önköltségi árat megkapja.  
  
Ha a szerepkör kombinációja, kiszerelés és a szervezeti egység nem határozza meg a tulajdonos származó önköltségi ár, az egységet a szerepkör és a szervezeti egység kombinációjában nem részesítik előnyben. Önköltségi ár esetén, ezt az árat arra a kiszerelésre alakítják át, amelyet a becslési sorban kiválasztott.  
  
A szerepkör és a szervezeti kiszerelés kombinációja nem határozhatja meg az önköltségi árat, a szervezeti egységet nem részesítik előnyben a szerepkör és a kiszerelés kombinációjában, az ár alapértelmezett a bármilyen beszélgetés lefolytatását követően, ha szükséges.  
  
 Ha nincs ár a szerepkörhöz, az önköltségi ár 0.00 az alapértelmezési érték a becslési sorban.  
  
 A projekt költség becslési sorában összes költség összege a tulajdonos szervezeti kiszerelés pénznemében szerepel.  
  
## <a name="sales-price-defaulting"></a>Sales-ár alapértelmezése  
Az értékesítési ár lista azon az értesítési entitáson alapul, amelyet csatoltak a projekthez. Az árajánlattal vagy szerződéssel társított értékesítési árlista meghatározza a kiszerelés értékesítési árát. Ha az árajánlat vagy szerződés egy egyéni árlistával rendelkezik, ez lesz a projekt becslések alapértelmezett értékesítési árlistája. Ha nincs kapcsolat az értékesítési entitásokkal, akkor a paraméterek beállításaiban konfigurált alapértelmezett értékesítési árlista a projekt alapértelmezett értékesítési árlistája. Minden egyes becslési sor erőforrás szervezeti kiszereléssel rendelkezik, amely társítva van azért, hogy megmutassa hogy a a szervezeti egység melyikből könyveli el az erőforrásokat a feladat befejezéséhez. A társított szerepkörök értékesítési árát a szerepkörök, kiszerelés, és a kiszerelés és az értékesítési árlistában szereplő erőforrás szervezeti kiszerelés kombinációinak keresésével határozzák meg, annak érdekében, hogy megkapják a kiszerelés érvényességéhez a megfelelő értékesítési árat a becslési sorokban.  
  
Ha a szerepkör, a kiszerelés és az erőforrás szervezeti kiszerelés kombinációja nem határozza meg az értékesítési árat az érékesítési árlistából, a rendszer figyelmen kívül hagyja a kiszerelést és a szerepkör és az erőforrás szervezeti kiszerelés kombinációját keresi. Sales-ár találata esetén, ahhoz a kiszereléshez alakítják majd át, amelyet az értékesítési becslési sorban kiválasztott.  
  
Ha nem talál a rendszer árat a szerepkörhöz, akkor 0.00-nak kell lennie az alapértelmezett értékesítési árnak a becslési sorban.  
  
A becslések nézet egy hálózat nézettel rendelkezik, ami a kiszereléssel, az összes költséggel, és az értékesítési árral ellátott becslési sorok lapos hálózatát jeleníti meg.  
  
## <a name="time-phased-view-of-project-estimates"></a>A projekt becslések időzített nézete  
A projekt becslések időzített nézetében a hálózat nézetből származó becslési adatot a szerepkör által mutatják ki, és megmutatja a becslési adat idővonalon keresztül történő terjedését az kiválasztott időskálán.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>A feladat módján alapuló erőfeszítés becslési elosztás  
Az időzített nézetben a feladat szerint megbecsült összes erősfeszítést a kiszerelésenkénti erőfeszített órák bizonyos számának elhelyezésével a kiválasztott időskála időtartamában osztódik. A project service szolgáltatásban a feladat módja határozza meg, hogy milyen erőfeszítés helyeztek ki a feladat időtartama alatt. A kétféle elosztás: az egyenletes elosztás és az elosztáson alapuló munkaórák. 
  
## <a name="work-hours-based-allocation"></a>A munkaidő alapú elosztás  
Egy feladathoz az automatikus ütemezésű feladat mód a feladat szerint megbecsült erőforrások számát irányítja, amelyek a napi teljes munkaórák felhasználásához vannak megbecsülve. Ez a feladat időtartama alatti eloszlatással történő erőforrás lefoglalást követően válik érvényessé az időzített nézetben is. Például egy "Nappali" időskálán, egy erőforrás által elvégzendő becsült feladathoz, a napra felosztott ráfordítás nem lépi túl a napi munkaórákat, amelyek a projekt naptárában meg vannak határozva. Ezért az erőkifejtés felosztás mindig biztosítja, hogy az erőforrások az egész napi használatra legyenek megbecsülve.  
  
## <a name="even-distribution"></a>Egyenletes forgalmazás  
Manuálisan ütemezett feladat mód nem tolerálja a munkaórákat, a projekt naptárat, vagy a feladatban meghatározott erőforrások számát. A vevő adatbevitelén alapul a feladat ütemezés. Az ilyen feladatokhoz, a kiszerelésenkénti erőforrás elosztás a kiválasztott időskála időtartama alatt nem rendelkezik semmilyen korlátozó tényezővel. A feladatban a teljes erőforrás egyaránt osztott és a kiválasztott időskála minden egyes kiszerelés időtartamához kapcsolódik.  
  
Ily módon a feladat szerint meghatározott feladat mód határozza meg az erőforrás forgalmazását vagy a kiszerelési időtartamonkénti erőforrás elosztást az időzített becsléseknél.  
  
## <a name="grouping-and-time-phasing-options"></a>Csoportosítás és időzítési beállítások  
Ez a nézet segít megérteni Önnek az erőforrás, a költség és az értékesítési becslések napi, heti, havi, vagy évi lebontás alapján történő forgalmazást. A Csoportosítás opció lehetővé teszi a becsült adat kimutatását a két másik dimenzióban: a kategória és az erőforrás. Mind a hálózatos nézetben és mind az időzített nézetben kiválaszthatja a megjelenítendő mezőket. Mindegyik időmezőhöz az összeg megjelenik felül az összes becsült erőforrás, költség megjelenítésével, és a napi, heti, havi, vagy évi értékesítésekkel.  
  
Az alapértelmezett költség és eladási ár dátum szerint érvényes. Ha a szerepkörök érték változik, átláthatóbbá válik az időzített nézetben, amikor a becsült adat megtekintésekor az 'Erőforrás' és a heti időzítés ki van mutatva.  
  
## <a name="expense-estimates"></a>Költség becslések  
Bármely költség, amely felmerül a projektben, nem közvetlenül kapcsolódik a felhasználandó laborhoz rögzíteni lehet a projekt becslésekben a hálózati nézetben. A **Költség becslés hozzáadása** lehetőség használatával a hálózati nézetben teheti meg. Egy adott feladat vagy a teljes projekt költségbecslései rögzíthetők. Ezekben a sorokban kiválaszthat költségkategóriákat, és megadhat egy feltételes dátumot, amikor a költség várhatóan beérkezik. Ha a társított költség és értékesítési árlista alapértelmezett árral vagy a költség kategóriákhoz meghatározott árrész százalékokkal rendelkezik , a társítás becslési listáján lesz alapértelmezve.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Projektmenedzseri útmutató](../psa/project-manager-guide.md)
