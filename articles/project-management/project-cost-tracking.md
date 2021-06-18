---
title: Projektköltség nyomon követése
description: Ez témakör arról nyújt tájékoztatást, hogy a Project Operations hogyan követi nyomon a projektből származó munkaköltséget és -kiadást.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cb76987cf15a14639f34cd3b67c1296a020b2e3e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996524"
---
# <a name="labor-cost-tracking-on-projects"></a>Projektekre vonatkozó munkaköltség nyomon követése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations a legalacsonyabb szükséges részletességű granularitással követi nyomon a projekttervbeli munkabecsléseket és -kiadásokat. A munkaköltségek pénzügyi becsült száma a tervezett ráfordításon és a projektterv egyes levélcsomópont-feladathoz rendelt általános vagy nevesített erőforrásokon alapul. Amikor a projekt elkezdődik, és az emberek elkezdik jelenteni a különböző projektfeladatokra fordított időket, a tényleges munkaköltséget összegzi a program, amely megkezdi a leképezések kiszámítását.

## <a name="labor-cost-tracking-view"></a>Munkaköltség követési nézet

A **Projektek** lap **Követés** fülén, a **Követés** > **Költség** gombra kattintva megnyithatja a **Költségkövetés** nézetet, és megtekintheti a projektterv egyes feladatainak munkakiadási folyamatát. Ez a nézet összehasonlítja a feladatra költött tényleges munkaköltséget a feladat tervezett munkaköltséggel is. A Project Operations a következő képleteket használja a munkaköltség-metrikák kiszámításához:

- **Tervezett költség**: Minden levélcsomópont-feladat összes erőforrás-hozzárendelésének becsült költsége
- **Tényleges költség**: A feladaton rögzített idő összes költség tényadatának összege
- **Költségfelhasználás százalékos aránya**: Tényleges költség ÷ Befejezéskori költség becslése
- **Fennmaradó költség**: Befejezéskori költség becslése – Tényleges költség
- **Befejezéskori költség**: Fennmaradó költség + Tényleges költség
- **Költségeltérés**: Tervezett költség – Befejezéskori költség becslése

Minden feladat megjeleníti a feladat költségeltérési leképezését. Ha a befejezéskori költség becslése több, mint a tervezett költség, a feladat várhatóan túl fog lépni a költségvetésen. Ha a befejezéskori költség becslése alacsonyabb, mint a tervezett költség, a feladat várhatóan a költségvetésen belül kész lesz.

>[!NOTE]
> A Project Operations csak a **Követés** fül **Projekt** lapján mutatja a munkaköltségeket. Azonban az anyagokat és kiadásokat felbecsülheti és nyomon követheti felhasználásra, ezek a költségek nem szerepelnek a **Követés** fülön feltüntetett költségekben. Ez a fül csak a munkaköltségek újratervezése érdekében működnek az erőfeszítések újratervezése révén.
A megjelenített költségösszegek a projekt költségpénzneme szerint vannak átváltva a projekt önköltségi árának pénzneméből, amelyet a költségárfolyam meghatározásához használnak. A projekt költségpénzneme a projektben szereplő szerződő egység pénzneme. Előfordulhat, hogy a **Projekt** lap **Becslések** fülén látható becsült költségértékek nem érik el a **Követés** lapon lévő tervezett költséget. Ennek az eltérésnek az az oka, hogy a költség **Becslés** rácson lévő összegzést és a tervezett költségeket másképp számítják ki a **Követés** rácson. 
>
> - A **Becslések fül** a becsült költséget az árlistában szereplő költségárfolyam azonos pénznemében számítja ki. Ezután az árlista pénznemében szereplő becsült költség a projekt költségpénznemének becsült költségéhez lesz átszámolva. A projekt pénznemében becsült költség 2 tizedesjegyre van kerekítve. Az átalakítás során egyetlen ponton sem alkalmazzák a pénznempontosságot. 
> - A **Követés** fülön a tervezett költségszámítás egy kissé eltérő számítási sorrendet követ, amely két szakaszban alkalmazza a pénznempontosságot: 
   ><ol>
   ><li>Az árlista pénznemben a becsült költségösszeget az alap pénznemére váltja át (1. átalakítás).</li>
   ><li>Az alap pénznemben a becsült költségösszeget a projekt költségpénznemére váltja át (2. átalakítás). </li>
   ></ol>
   >A pénznempontosságot mindkét lépésben alkalmazni kell egy tervezett költségen (a **Követés** fülön), amely kissé eltér a becsült költségtől (a **Becslések** fül **Idő - szakaszos** nézetben). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>A levélcsomópont-feladatok költségeinek újratervezése

A levélcsomópont-feladatból származó munkaköltségek nem újratervezhetők közvetlenül a **Projekt** lap **Követés** fülén. A **Ráfordítás követése** nézetben azonban újratervezheti a feladat fennmaradó ráfordítását. Ez a feladat fennmaradó költségének újraszámítását eredményezni. Az alábbi leírás ismerteti ennek a működését.

1. A projektmenedzser a feladatokra vonatkozó **Fennmaradó ráfordítás** mező alapértelmezett értékének frissítésével, a feladat fennmaradó ráfordításának új becslésével tudja újratervezni. Az újratervezés a feladat befejezéskori munkamennyiség becslésének (EAC), a folyamat százalékos arányának és a feladat tervezett ráfordítási varianciájának újraszámítását eredményezi. Az EAC, a teljes becslés (ETC) és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.
2. A feladat fennmaradó költségeinek új értéke alapján a rendszer kiszámítja a **Költségkövetés** nézet fennmaradó bevételét. A fennmaradó költségnek fennmaradó ráfordítás alapján való kiszámításához a rendszer először a feladat egy órás erőfeszítésének átlagos költségét számítja ki tervezett költségként vagy tervezett ráfordításként. A tervezett költség a feladat összes erőforrás-hozzárendelésének költségének összege. Az óránkénti átlagos költség a feladat újonnan előrejelzett fennmaradó erőfeszítéseinek fennmaradó költségének kiszámítására használható.
3. A rendszer újra kiszámítja a levélcsomópont-feladat befejezéskori becsült költségét és a költségfelhasználási százalékát.
4. Az összesítő feladatok befejezéskori becsült költségét egészen a gyökércsomópontig újraszámolják.

## <a name="reprojecting-costs-on-summary-tasks"></a>Az összesítő feladatok költségeinek újratervezése

A munkaköltségeket összefoglaló feladatokat vagy tárolófeladatokat is újratervezheti. Azonban nem tudja közvetlenül újratervezni a munkaköltségeket a **Projekt** lap **Követés** fülén található összesítő feladatokban. A levélcsomópont-feladatokhoz hasonlóan az összegző és tárolófeladatok újratervezési összegzését elvégezheti a **Ráfordításkövetés** nézetben is. Ebben a nézetben újratervezheti az összegzőfeladat fennmaradó ráfordításait, ami az összegző feladat fennmaradó költségének újraszámítását eredményezi. Az alábbi leírás ismerteti ennek a működését.

1. A projektmenedzser az összegző feladatokra vonatkozó fennmaradó ráfordítás alapértelmezett értékének frissítésével, a feladat új becslésével tudja újratervezni. Ez a frissítés az összegző feladat befejezéskori munkamennyiség becslésének (EAC), a folyamat százalékos arányának és a feladat tervezett ráfordítási varianciájának újraszámítását eredményezi. Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát szintén újraszámolják, és új előrejelzést adnak az erőkifejtés szórására.
2. Az összegző feladat fennmaradó költségeinek új értéke alapján a rendszer kiszámítja a **Költségkövetés** nézet fennmaradó bevételét. A fennmaradó költségnek fennmaradó ráfordítás alapján való kiszámításához a rendszer először az összegző feladat egy órás erőfeszítésének átlagos költségét számítja ki tervezett költségként vagy tervezett ráfordításként. Az óránkénti átlagos költség az összegző feladat újonnan előrejelzett fennmaradó erőfeszítéseinek költségének kiszámítására használható.
3. A rendszer újra kiszámítja az összegző feladat befejezéskori becsült költségét és a költségfelhasználási százalékát.
4. Az új költség a feladat eredeti tervezett költségével azonos arányban osztják el a gyermekfeladatok között.
5. Kiszámítjuk az új befejezéskori költség értékét az egyes feladatok mindegyikétől egészen a levélcsomóponti feladatokig. Ezen érték alapján az érintett gyermekfeladatok a levélcsomópontokig újraszámolják a fennmaradó költség százalékát és a költségfelhasználási százalékot a befejezéskori költség értéke alapján. Ez az érték új előrejelzést eredményez a feladat költségvariációja szempontjából. 


A **Költségteljesítmény** mező beállítható a követési adatokból. Ha a **Költségkövetés** nézet gyökércsomópontjának költségeltérése negatív, ezt a mezőt a **Költségvetésen belül** lehetőségre állíthatja. Ha a gyökércsomópont költségeltérése pozitív, a **Költségvetésen túl** értékre állíthatja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
