---
title: Projekt értékesítés nyomon követése
description: Ez a cikk arról nyújt tájékoztatást, hogy a Project Operations hogyan követi nyomon a projekt munkabevételeinek előrehaladását.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911277"
---
# <a name="project-sales-tracking"></a>Projekt értékesítés nyomon követése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations a legalacsonyabb szükséges részletességű granularitással követi nyomon a projekttervbeli munkabecsléseket és -bevételeket. A munkabevételek becsült száma a tervezett ráfordításon és a projektterv egyes levélcsomópont-feladathoz rendelt általános vagy nevesített erőforrásokon alapul. Amikor a projekt elkezdődik, és az emberek elkezdik jelenteni a különböző projektfeladatokra fordított időket, a tényleges munkabevételt összegzi a program, amely megkezdi a leképezések kiszámítását.

## <a name="labor-revenue-tracking-view"></a>Munkabevételek nyomon követése nézet

A **Projektek** lap **Követés** fülön a **Követés** > **Költség** gombra kattintva megnyithatja a **Költségkövetés** nézetet. Vagy válassza a **Használat** > **Számlázási díj** lehetőséget a **Bevétel nyomon követése** nézet megnyitásához, amely a projektterv minden feladatának munkabevétel-előrehaladását mutatja. Ez a nézet összehasonlítja a feladatre költött tényleges munkabevételt a feladat tervezett munkabevétellel is. A Project Operations a következő képleteket használja a munkabevétel-metrikák kiszámításához:

- **Tervezett bevétel**: Minden levélcsomópont-feladat összes erőforrás-hozzárendelésének becsült értékesítési értéke
- **Tényleges bevétel**: A feladaton rögzített idő összes számlázatlan értékesítési tényadatának összege
- **Számlázható bevétel%**: Tényleges bevétel ÷ Befejezéskori becsült bevétel
- **Fennmaradó bevétel**: Befejezéskori becsült bevétel – Tényleges bevétel
- **Befejezéskori becsült bevétel**: Fennmaradó bevétel + Tényleges bevétel
- **Bevétel eltérése**: Tervezett bevétel – Befejezéskori becsült bevétel


> [!NOTE]
> A Project Operations csak a **Követés** fül **Projekt** lapján mutatja a munkabevételeket. Azonban az anyagokat és kiadásokat felbecsülheti és nyomon követheti felhasználásra, ezek a bevételek nem szerepelnek a **Követés** fülön feltüntetett bevételekben. Ez a fül csak a munkaerőbevételek újratervezése érdekében működnek az erőfeszítések újratervezése révén.  
> Az összes megjelenített bevételösszeget a projekt költségpénznemébe konvertálja. A projekt költségpénzneme a projektben szereplő szerződő egység pénzneme. Rögzített árú projektek esetében a **Munkabevétel nyomon követése** nézet bevételi számai nem relevánsak, mert a számlázatlan értékesítési tényadatok nincsenek rögzítve az időjóváhagyáson.
> Előfordulhat, hogy a projekt **Becslés** fülén látható idő becsült értékesítési értékei nincsenek hozzáadva a **Követés** fül tervezett bevételi értékét. Ennek az eltérésnek két oka lehet:
><ol>
   ><li> A <b>Becslések</b> fül a becsült bevétel értékesítési pénznemét mutatja, míg a <b>Követés</b> fül a költségpénznemre átváltott tervezett bevételeket. </li>
   ><li> Ha a becsült értékesítések a szerződés pénznemére lesznek átváltva a projekt pénznemére a <b>Becslések</b> fülön látható módon, az átváltás olyan lépéseket tartalmaz, amelyek pontatlansághoz vezethetnek: </li>
><ol>
><li> A szerződés pénznemében a becsült értékesítési összeget először az alap pénznemre váltja át (1. átalakítás).</li>
><li> Az alap pénznemben a becsült értékesítési összeget a projekt költségpénznemére váltja át (2. átalakítás). </li>
></ol>
></ol>
> A pénznem-pontosság mindkét lépésben alkalmazva van, ez a projekt pénznemében tervezett bevételnek a szerződés pénznemében tervezett értékesítéstől való eltérését eredményezi.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>A levélcsomópont-feladatok bevételeinek újratervezése

A levélcsomópont-feladatból származó munkabevételek nem újratervezhetők közvetlenül a **Projekt** lap **Követés** fülén. A **Ráfordítás követése** nézetben azonban újratervezheti a feladat fennmaradó ráfordítását. Ez a feladat fennmaradó bevételének újraszámítását eredményezni. Az alábbi leírás ismerteti ennek a működését.

1. A projektmenedzser a feladatokra vonatkozó **Fennmaradó ráfordítás** mező alapértelmezett értékének frissítésével, a feladat fennmaradó ráfordításának új becslésével tudja újratervezni. Az újratervezés a feladat befejezéskori munkamennyiség becslésének (EAC), a folyamat százalékos arányának és a feladat tervezett ráfordítási varianciájának újraszámítását eredményezi. Az EAC, a teljes becslés (ETC) és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.
2. A feladat fennmaradó ráfordításainak új értéke alapján a rendszer kiszámítja a **Bevételkövetés** nézet fennmaradó bevételét. A fennmaradó bevételnek a fennmaradó ráfordítás alapján való kiszámításához a rendszer először a feladat egy órás erőfeszítésének átlagos bevételét számítja ki tervezett bevételként vagy tervezett ráfordításként. A tervezett bevétel a feladat összes erőforrás-hozzárendelésének bevételének összege. Az óránkénti átlagos bevétel a feladat újonnan előrejelzett fennmaradó erőfeszítéseinek fennmaradó bevételének kiszámítására használható.
3. A rendszer újra kiszámítja a levélcsomópont-feladat befejezéskori becsült bevételét és a bevételfelhasználási százalékát.
4. Az összesítő feladatok befejezéskori becsült bevételét egészen a gyökércsomópontig újraszámolják.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Az összesítő feladatok bevételeinek újratervezése

A munkabevételeket összefoglaló feladatokat vagy tárolófeladatokat is újratervezheti. Azonban nem tudja közvetlenül újratervezni a munkabevételeket a **Projekt** lap **Követés** fülén található összesítő feladatokban. A levélcsomópont-feladatokhoz hasonlóan az összegző és tárolófeladatok újratervezési összegzését elvégezheti a **Ráfordításkövetés** nézetben is. Ebben a nézetben újratervezheti az összegzőfeladat fennmaradó ráfordításait, ami az összegző feladat fennmaradó bevételének újraszámítását eredményezi. Az alábbi leírás ismerteti ennek a működését.

1. A projektmenedzser a feladatokra vonatkozó **Fennmaradó ráfordítás** mező alapértelmezett értékének frissítésével, a feladat **Fennmaradó ráfordításának** új becslésével tudja újratervezni. Az újratervezés a feladat befejezéskori munkamennyiség becslésének (EAC), a folyamat százalékos arányának és a feladat tervezett ráfordítási varianciájának újraszámítását eredményezi. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.
2. A feladat **Fennmaradó ráfordítás** mezőjének új értéke alapján a rendszer kiszámítja a **Bevételkövetés** nézet fennmaradó bevételét. A fennmaradó bevételnek fennmaradó ráfordítás alapján való kiszámításához a rendszer először a feladat egy órás erőfeszítésének átlagos bevételét számítja ki tervezett bevételként vagy tervezett ráfordításként. A tervezett bevétel a feladat összes erőforrás-hozzárendelésének bevételének összege. Ezután ezt az óránkénti átlagos bevételt a feladat újonnan előrejelzett fennmaradó ráfordításának bevételének kiszámítására használják.
3. A rendszer újra kiszámítja az összegző feladat befejezéskori becsült bevételét és a bevételfelhasználási százalékait.
4. A befejezéskori becsült bevétel új értékét a feladat eredeti tervezett bevételével azonos arányban osztják el a gyermekfeladatok között.
5. Kiszámítjuk az új befejezéskori becsült bevételt az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig. Ezen érték alapján az érintett gyermekfeladatok a levélcsomópontokig újraszámolják a fennmaradó bevétel százalékát és a bevételfelhasználási százalékot a befejezéskori bevétel értéke alapján. Ez új előrejelzést eredményez a feladat bevétel variációja szempontjából. 
6. Az összesítő feladatok befejezéskori becsült bevételét egészen a gyökércsomópontig újraszámolják.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

