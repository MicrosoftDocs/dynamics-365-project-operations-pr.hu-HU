---
title: Projekt nyomon követésének áttekintése
description: Ez a témakör a projekt előrehaladásának és a költségfelhasználásnak a nyomon követéséről nyújt információkat.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127355"
---
# <a name="project-tracking-overview"></a>Projekt nyomon követésének áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az előrehaladás ütemtervéhez viszonyított nyomon követésének szükségessége iparáganként eltérő. Egyes iparágak részletes szinten követnek nyomon, mások viszont magasabb szinten követnek nyomot. Ez a témakör bemutatja, hogyan kell ütemezni a szervezet követelményeit.

## <a name="effort-tracking-view"></a>Erőfeszítések nyomon követésének megtekintése

A tevékenység **Nyomon követése** nézet nyomon követi a feladatok előrehaladását az ütemezésben, és összehasonlítja a feladat tervezett munkaidejét a feladatra fordított tényleges munkaórákkal. A Dynamics 365 Project Operations a következő képleteket használja a követési metrikák kiszámításához:

- **Haladás százaléka**: Az eddig elvégzett tényleges erőfeszítés + teljes becslés (EAC) 
- **Teljes becslés (ETC)** Tervezett erőfeszítés – A ténylegesen elvégzett erőfeszítés eddig 
- **Teljes becslés (EAC)**: Fennmaradó erőfeszítés + Eddig elvégzett tényleges erőfeszítés 
- **Tervezett erőfeszítés szórása**: Tervezett erőfeszítés – EAC

A Project Operations a feladat erőfeszítés-varianciájának előrejelzését mutatja. Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték, és elmarad az ütemtervtől. Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték, és előrehaladottabb állapotban van az ütemtervhez képest.

## <a name="reprojecting-effort"></a>Az erőfeszítés újratervezése

A projektmenedzserek gyakran felülvizsgálják a feladat eredeti becsléseit. A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel. Nem javasolt azonban, hogy a projektmenedzserek módosítsák az alaptervi számokat. Ez azért van, mert a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.

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

A **Költségkövetés** nézet összehasonlítja a feladat tényleges költségeit a feladat tervezett költségével. 

> [!NOTE]
> Ez a nézet csak a munkaköltségeket mutatja, és nem tartalmazza a költségbecslésekből származó költségeket. A Project Operations a következő képleteket használja a követési metrikák kiszámításához:

- **Felhasznált költség százalékos aránya** A mai napig ténylegesen elköltött költség ÷ A becsült költség befejezéskor
- **Teljes költség (CTC)** Tervezett költség – A mai napig ténylegesen elköltött költség
- **EAC**: Fennmaradó költség + Eddig elköltött aktuális költség
- **Tervezett költség szórás**: Tervezett költség – EAC

A feladaton látható a költségváltozás vetülete. Ha az EAC meghaladja a tervezett költségeket, akkor a feladat várhatóan többet fog fizetni, mint az eredetileg tervezték. Ezért a költségvetés fölé emelkedik. Ha az EAC kevesebb, mint a tervezett költség, akkor a feladat várhatóan kevesebbre kerül, mint az eredetileg tervezték. Ezért a költségvetés keretein belül növekszik.

## <a name="project-managers-reprojection-of-cost"></a>A projektvezető költségeinek újratervezése

Az erőfeszítés újratervezésekor a CTC, az EAC, a felhasznált költségek százalékos arányát és a várható költségváltozást mind a **Költségkövetés** nézetben újraszámolják.

## <a name="project-status-summary"></a>A projekt állapotának összefoglalása

A követési adatok az **Erőfeszítés követése** és **Költség nyomon követése** nézetekben a projekt gyökércsomópontjában, az összefoglaló feladatokban és a levélcsomópontok feladatainak szintjén mutatják az előrehaladást és a költségfelhasználást. Az **Állapot** szakasz a **Projekt entitás** oldalon a projekt szintű állapotának összefoglalását mutatja.

## <a name="status-summary-fields"></a>Állapot-összefoglaló mezők

Az **Általános projekt állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja. Színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot. A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz. A **Állapot frissítése** mező nem szerkeszthető, és ez az érték időbélyeg, amely jelzi, ha az állapot utolsó frissítése.

Az **Ütemezés teljesítménye** és **Költség teljesítése** mezőket a követési dátumtól kezdve állítják be. Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezeket a mezőket **Ahead** értékre állíthatja. Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket állíthatja **Mögött** értékre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]