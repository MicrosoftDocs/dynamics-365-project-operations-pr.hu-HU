---
title: Projektekhez kapcsolódó erőfeszítés nyomon követése
description: Ez a témakör a projekt ráfordításának és a munkafolyamat nyomon követéséről nyújt információkat.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010879"
---
# <a name="project-effort-tracking"></a>Projektekhez kapcsolódó erőfeszítés nyomon követése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az előrehaladás ütemtervéhez viszonyított nyomon követésének szükségessége iparáganként eltérő. Egyes iparágak részletes szinten követnek nyomon, mások viszont magasabb szinten követnek nyomot. Ez a témakör bemutatja, hogyan kell ütemezni a szervezet követelményeit.

## <a name="effort-tracking-view"></a>Erőfeszítések nyomon követésének megtekintése

A tevékenység **Nyomon követése** nézet nyomon követi a feladatok előrehaladását az ütemezésben, és összehasonlítja a feladat tervezett munkaidejét a feladatra fordított tényleges munkaórákkal. A Dynamics 365 Project Operations a következő képleteket használja a követési mutatók kiszámításához:

- **Haladás százaléka**: Az eddig elvégzett tényleges erőfeszítés + teljes becslés (EAC) 
- **Fennmaradó ráfordítás**: Befejezéskori becsült ráfordítás – Az eddigi tényleges ráfordítás 
- **Teljes becslés (EAC)**: Fennmaradó erőfeszítés + Eddig elvégzett tényleges erőfeszítés 
- **Tervezett erőfeszítés szórása**: Tervezett erőfeszítés – EAC

A Project Operations a feladat erőfeszítés-varianciájának előrejelzését mutatja. Ha az EAC meghaladja a tervezett erőfeszítéseket, akkor a feladat várhatóan több időt vesz igénybe, mint az eredetileg tervezték, és elmarad az ütemtervtől. Ha az EAC kevesebb, mint a tervezett erőfeszítés, akkor a feladat várhatóan kevesebb időt vesz igénybe, mint az eredetileg tervezték, és előrehaladottabb állapotban van az ütemtervhez képest.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>A levélcsomópont-feladatok ráfordításának újratervezése

A projektmenedzserek gyakran felülvizsgálják a feladat eredeti becsléseit. A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel. Nem javasoljuk azonban, hogy a projektmenedzserek megváltoztassák a tervezett ráfordítások számát. Ennek az az oka, hogy a projekt tervezett ráfordítása a projekt ütemtervének és költségbecslésének megállapított igazságforrást jelenti, és a projekt valamennyi érdekeltje egyetértett vele.

A projektmenedzser a feladatokra vonatkozó alapértelmezett **Fennmaradó ráfordítás** frissítésével, a feladat új becslésével tudja újratervezni. Ez a frissítés a feladat befejezéskori munkamennyiség becslésének (EAC), a folyamat százalékos arányának és a tevékenység tervezett ráfordítási varianciájának újraszámítását eredményezi. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Az erőfeszítések újratervezése az összefoglaló feladatok során

Az összefoglaló vagy a tároló feladatokra tett erőfeszítések újratervezhetők. A projektmenedzserek frissíthetik az összegző feladatok fennmaradó ráfordítását. A fennmaradó ráfordítás frissítése az alkalmazás következő számítási készletét indítja el:

- Kiszámítják az EAC és a feladat előrehaladási százalékát.
- Az új EAC eloszlik a gyermek feladataival azonos arányban, mint az eredeti EAC volt a feladatnál.
- Kiszámítjuk az új EAC-t az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig. 
- Az érintett gyermek feladatait a levélcsomópontokig a fennmaradó ráfordítással és az előrehaladási százalékkal újraszámolják az EAC-érték alapján. Ez új előrejelzést eredményez a feladat erőfeszítési variációja szempontjából. 
- Az összesítő feladatok EAC-ját egészen a gyökércsomópontig újraszámolják.


## <a name="project-status-summary"></a>A projekt állapotának összefoglalása

A követési adatok az **Erőfeszítés követése** és **Költség nyomon követése** nézetekben a projekt gyökércsomópontjában, az összefoglaló feladatokban és a levélcsomópontok feladatainak szintjén mutatják az előrehaladást és a költségfelhasználást. Az **Állapot** szakasz a **Projekt entitás** oldalon a projekt szintű állapotának összefoglalását mutatja.

## <a name="status-summary-fields"></a>Állapot-összefoglaló mezők

Az **Általános projekt állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja. Színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot. A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz. A **Állapot frissítése** mező nem szerkeszthető, és ez az érték időbélyeg, amely jelzi, ha az állapot utolsó frissítése.

Az **Ütemezés teljesítménye** és **Költség teljesítése** mezőket a követési dátumtól kezdve állítják be. Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezeket a mezőket **Ahead** értékre állíthatja. Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket állíthatja **Mögött** értékre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
