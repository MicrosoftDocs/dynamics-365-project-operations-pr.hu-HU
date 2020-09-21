---
title: A projekt haladása és költségfogyasztása
description: Ez a témakör a projekt előrehaladásának és a költségfelhasználásnak a nyomon követéséről nyújt információkat.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752284"
---
# <a name="project-progress-and-cost-consumption"></a>A projekt haladása és költségfogyasztása

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Az előrehaladás ütemtervéhez viszonyított nyomon követésének szükségessége iparáganként eltérő. Egyes iparágak granulált szinten követik el, mások viszont magasabb szinten követnek nyomot. Ez a témakör bemutatja, hogyan kell ütemezni a szervezet követelményeit.

## <a name="effort-tracking-view"></a>Erőfeszítések nyomon követésének megtekintése

Az **Erőfeszítés követése** nézet követi a feladatok előrehaladását az ütemtervben. Összehasonlítja a tényleges erőfeszítési órákat, amelyeket egy feladatra költöttek, az adott feladatra tervezett erőfeszítési órákkal. A PSA a következő képleteket használja a követési mutatók kiszámításához:

- Haladás százaléka = az eddig elköltött tényleges erőfeszítés ÷ a feladathoz tervezett erőfeszítés 
- Teljes becslés (ETC) = Tervezett erőfeszítés - A ténylegesen elvégzett erőfeszítés eddig 
- Teljes becslés (EAC) = fennmaradó erőfeszítés + az eddig elköltött tényleges erőfeszítés 
- Tervezett erőfeszítés szórása = Tervezett erőfeszítés - EAC

A PSA a feladat erőfeszítés-varianciájának előrejelzését mutatja. Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték. Ezért elmarad az ütemtervtől. Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték. Ezért még hamarabb van.

## <a name="re-projecting-effort"></a>Az erőfeszítés újratervezése

Általában a projektmenedzser felülvizsgálja a feladat eredeti becsléseit. A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel. Nem javasoljuk azonban, hogy a projektvezetők megváltoztassák az alapszintet, mivel a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.

Kétféle módon lehet egy projektmenedzser újraprogramozni a feladatokat:

- Helyezze felül az alapértelmezett ETC-t egy új becsléssel a feladat tényleges hátralévő erőfeszítéseiről. 
- A feladat valódi előrehaladásának új becslésével felülbírálja az alapértelmezett haladási százalékot.

Ezeknek a megközelítéseknek a segítségével át kell számítani a feladat ETC-jét, EAC-ját és az előrehaladási százalékot, valamint a feladatra várható erőfeszítési varianciát. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Az erőfeszítések újratervezése az összefoglaló feladatok során

Az összefoglaló vagy a tároló feladatokra tett erőfeszítések újratervezhetők. Függetlenül attól, hogy a felhasználó újraprogramozza-e a fennmaradó erőfeszítést vagy az összefoglaló feladatok előrehaladási százalékát, a következő számítási sorozat kezdődik:

- Kiszámítják az EAC, ETC és a feladat előrehaladási százalékát.
- Az új EAC eloszlik a gyermek feladataival azonos arányban, mint az eredeti EAC volt a feladatnál.
- Kiszámítjuk az új EAC-t az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig. 
- Az érintett gyermek feladatait a levélcsomópontokig az ETC-vel és az előrehaladási százalékkal újraszámolják az EAC-érték alapján. Ez új előrejelzést eredményez a feladat erőfeszítési variációja szempontjából. 
- Az összesítő feladatok EAC-ját egészen a gyökércsomópontig újraszámolják.

### <a name="cost-tracking-view"></a>Költségkövetési nézet 

A **Költségkövetés** nézet összehasonlítja a feladat tényleges költségeit a feladat tervezett költségével. 

> [!NOTE]
> Ez a nézet csak a munkaköltségeket mutatja, és nem tartalmazza a költségbecslésekből származó költségeket. 

A PSA a következő képleteket használja a követési mutatók kiszámításához:

- A felhasznált költség százalékos aránya = a mai napig ténylegesen elköltött költség ÷ A feladat tervezett költsége
- Teljes költség (CTC) = Tervezett költség - a mai napig ténylegesen elköltött költség
- EAC = CTC + a mai napig töltött tényleges költség
- Tervezett költség szórás = Tervezett költség - EAC

A feladaton látható a költségváltozás vetülete. Ha az EAC meghaladja a tervezett költségeket, akkor a feladat várhatóan többet fog fizetni, mint az eredetileg tervezték. Ezért a költségvetés fölé emelkedik. Ha az EAC kevesebb, mint a tervezett költség, akkor a feladat várhatóan kevesebbre kerül, mint az eredetileg tervezték. Ezért a költségvetés keretein belül növekszik.

## <a name="project-managers-re-projection-of-cost"></a>A projektvezető költségeinek újratervezése

Az erőfeszítés újratervezésekor a CTC, az EAC, a felhasznált költségek százalékos arányát és a várható költségváltozást mind a **Költségkövetés** nézetben újraszámolják.

## <a name="project-status-summary"></a>A projekt állapotának összefoglalása

A követési adatok az **Erőfeszítés követése** és **Költség nyomon követése** nézetekben a projekt gyökércsomópontjában, az összefoglaló feladatokban és a levélcsomópontok feladatainak szintjén mutatják az előrehaladást és a költségfelhasználást. Az **Állapot** szakasz a **Projekt entitás** oldalon a projekt szintű állapotának összefoglalását mutatja.

## <a name="status-summary-fields"></a>Állapot-összefoglaló mezők

Az **Általános projekt állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja. Színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot. A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz. A **Állapot frissítése** mező nem szerkeszthető, és ez az érték időbélyeg, amely jelzi, ha az állapot utolsó frissítése.

Az **Ütemezés teljesítménye** és **Költség teljesítése** mezőket a követési dátumtól kezdve állítják be. Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezeket a mezőket **Ahead** értékre állíthatja. Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket állíthatja **Mögött** értékre.
