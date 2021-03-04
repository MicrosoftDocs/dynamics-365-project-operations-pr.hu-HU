---
title: Projekt előrehaladása és költségfogyasztása
description: Ez a témakör a projekt előrehaladásának és a költségfelhasználásnak a nyomon követéséről nyújt információkat.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148016"
---
# <a name="project-progress-and-cost-consumption"></a>Projekt előrehaladása és költségfogyasztása

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Az előrehaladás ütemtervéhez viszonyított nyomon követésének szükségessége iparáganként eltérő. Egyes iparágak granulált szinten követik el, mások viszont magasabb szinten követnek nyomot. Ez a témakör bemutatja, hogyan kell ütemezni a szervezet követelményeit.

## <a name="effort-tracking-view"></a>Erőfeszítések nyomon követésének megtekintése

Az **Erőfeszítés követése** nézet követi a feladatok előrehaladását az ütemtervben. Az egy feladatra ténylegesen ráfordított órákat veti össze a feladatra tervezett órák mennyiségével. A Project Service Automation a következő képleteket használja a követési metrikák kiszámításához:

Kezdetben a feladat létrehozásakor: a tervezett költség a teljes becslés értékre lesz beállítva a befejezéskor. Ha a tényleges adatokat rögzítik a feladatban, akkor a következő az erőfeszítés nyomon követésének nézetének kiszámítása lesz

- Haladás százaléka = az eddig elvégzett tényleges erőfeszítés + teljes becslés (EAC) 
- Becslés a végrehajtásra (ETC) = teljes becslés (EAC) – eddig elvégzett tényleges erőfeszítés 
- Teljes becslés (EAC) = fennmaradó erőfeszítés + eddig elvégzett tényleges erőfeszítés 
- Tervezett erőfeszítés szórása = Tervezett erőfeszítés - EAC

A Project Service Automation a feladat erőfeszítés-varianciájának leképezését jeleníti meg. Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték. Ezért elmarad az ütemtervtől. Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték. Ezért még hamarabb van.

## <a name="reprojecting-effort"></a>Az erőfeszítés újratervezése

Általában a projektmenedzser felülvizsgálja a feladat eredeti becsléseit. A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel. Nem javasoljuk azonban, hogy a projektvezetők megváltoztassák az alapszintet, mivel a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.

Kétféle módon tudja egy projektmenedzser újraprogramozni a feladatokat:

- Helyezze felül az alapértelmezett ETC-t egy új becsléssel a feladat tényleges hátralévő erőfeszítéseiről. 
- A feladat valódi előrehaladásának új becslésével felülbírálja az alapértelmezett haladási százalékot.

Ezeknek a megközelítéseknek a segítségével át kell számítani a feladat ETC-jét, EAC-ját és az előrehaladási százalékot, valamint a feladatra várható erőfeszítési varianciát. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Az erőfeszítések újratervezése az összefoglaló feladatok során

Az összefoglaló vagy a tároló feladatokra tett erőfeszítések újratervezhetők. Függetlenül attól, hogy a felhasználó újratervezi-e a fennmaradó erőfeszítést vagy az összefoglaló feladatok előrehaladási százalékát, a következő számítási sorozat kezdődik:

- Kiszámítják az EAC, ETC és a feladat előrehaladási százalékát.
- Az új EAC eloszlik a gyermek feladataival azonos arányban, mint az eredeti EAC volt a feladatnál.
- Kiszámítjuk az új EAC-t az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig. 
- Az érintett gyermek feladatait a levélcsomópontokig az ETC-vel és az előrehaladási százalékkal újraszámolják az EAC-érték alapján. Ez új előrejelzést eredményez a feladat erőfeszítési variációja szempontjából. 
- Az összesítő feladatok EAC-ját egészen a gyökércsomópontig újraszámolják.

### <a name="cost-tracking-view"></a>Költségkövetési nézet 

A **Költségkövetés** nézet összehasonlítja a feladat tényleges költségeit a tervezett költséggel. 

> [!NOTE]
> Ez a nézet csak a munkaköltségeket mutatja, és nem tartalmazza a költségbecslésekből származó költségeket. 

A Project Service Automation a következő képleteket használja a követési metrikák kiszámításához:

A feladatok létrehozásakor a tervezett költség megegyezik a teljes becsült költséggel. Miután a tényleges adatokat rögzítették a feladatban, a **Követés** nézetben a költségek számítása a következőképpen történik:

 - A felhasznált költség százalékos aránya = a mai napig ténylegesen elköltött költség ÷ A feladat becsült költsége befejezéskor
 - Teljesítési költség (CTC) = a feladat becsült költsége – a mai napig ténylegesen elköltött költség
 - A feladat becsült költsége = CTC + a mai napig ténylegesen elköltött költség
 - Előrejelzett költségeltérés = tervezett költség – a feladat becsült költsége

A feladaton látható a költségváltozás vetülete. Ha a feladat becsült költsége meghaladja a tervezett költségeket, akkor a feladat várhatóan többe fog kerülni, mint azt eredetileg tervezték. Ezért a költségvetés fölé emelkedik. Ha a feladat becsült költsége kisebb a tervezett költségnél, akkor a feladat várhatóan kevesebbe fog kerülni, mint azt eredetileg tervezték és a trendje a költségvetés alatt marad.

## <a name="project-managers-reprojection-of-cost"></a>A projektvezető költségeinek újratervezése

Az erőfeszítés újbóli leképezésekor a CTC-t, a teljes befejezéskori becslést, a felhasznált költségek százalékos arányát és a várható költségváltozást mind újraszámolják a **Költségkövetés** nézetben.

## <a name="project-status-summary"></a>A projekt állapotának összefoglalása

A követési adatok az **Erőfeszítés követése** és **Költség nyomon követése** nézetekben a projekt gyökércsomópontjában, az összefoglaló feladatokban és a levélcsomópontok feladatainak szintjén mutatják az előrehaladást és a költségfelhasználást. Az **Állapot** szakasz a **Projekt entitás** oldalon a projekt szintű állapotának összefoglalását mutatja.

## <a name="status-summary-fields"></a>Állapot-összefoglaló mezők

Az **Általános projekt állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja. Színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot. A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz. A **Állapot frissítése** mező nem szerkeszthető, és ez az érték időbélyeg, amely jelzi, ha az állapot utolsó frissítése.

Az **Ütemezés teljesítménye** és **Költség teljesítése** mezőket a követési dátumtól kezdve állítják be. Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezeket a mezőket **Ahead** értékre állíthatja. Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket állíthatja **Mögött** értékre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]