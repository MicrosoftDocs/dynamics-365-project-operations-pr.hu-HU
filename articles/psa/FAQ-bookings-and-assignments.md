---
title: Erőforrások lefoglalása és a feladat-hozzárendelésekhez való kapcsolódásuk
description: Ez a témakör ismerteti az elnevezett erőforrások kezelését, az erőforrás-foglalásokat és a feladat-hozzárendeléseket, és azt, hogy ezek hogyan kapcsolódnak egymáshoz.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 83b1bf39c71275f2e8e4ec20082f711154696586
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286206"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Erőforrások lefoglalása és a feladat-hozzárendelésekhez való kapcsolódásuk

[!include [banner](../includes/psa-now-project-operations.md)]

Kétféle módon lehet elnevezett erőforrásokat lefoglalni egy projektcsapathoz és hozzárendelni projektfeladatokhoz:

- Az erőforrás közvetlenül lefoglalható egy projektre, majd hozzárendelhető a projekt feladataihoz.
- A feladatok hozzárendelhetők egy általános erőforráshoz, amely azután az általános megkeresésére és lecserélésére használható egy megnevezett erőforrással. 

Mindkét esetben az erőforrás lefoglalása fenntartja az erőforrás kapacitását.

A projektet megtervező projektmenedzser birtokában van a projektterv és az ütemezés. Ha általános erőforrást használ a hozzárendeléshez, majd erőforrás-követelményt generál belőle, a projektmenedzser lefoglalhatja az erőforrásokat a projekthez a projekttervben meghatározott kontúrokkal. Képes erőforrásokat lefoglalni egy projekthez, majd feladatokhoz hozzárendelni azokat, azonban nem lehetséges a foglalás kontúrjainak hozzáigazítása a feladatok körvonalaihoz. A foglalások nem befolyásolják a projekt ütemtervét.

Gondoljon egy összetett projektre több egymást átfedő feladattal, ahol több ugyanolyan típusú erőforrások kell egyidejűleg működnie. Ha egy erőforrás olyan eloszlást kapott, amely eltér a hozzárendelések összesítettjétől, nehezen módosíthatók a feladatok, hogy a lefoglalások eloszlása megfeleljen a különálló feladatoknak és az eredeti eloszlásaiknak.

Az alábbi példában négy feladat esetében ugyanazon erőforrás teljes követelménye 62 óra egy két hetes időszakban, és van egy specifikus eloszlás. Ha Róbert erőforrás ugyanabban a két hétben 62 órára van lefoglalva, de eltérő eloszlással, a követelmény és a foglalások igazítva vannak.

| **Feladateloszlások**    | **Teljes óraszám** | Hé 6/4 | Ke 6/5 | Sze 6/6 | Csü 6/7 | Pé 6/8 | Szo 6/9 | Va 6/10 | Hé 6/11 | Ke 6/12 | Sze 6/13 | Csü 6/14 | Pé 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| 1. feladat               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| 2. feladat               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| 3. feladat               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| 4. feladat               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Végösszegek**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Róbert elérhetősége
| **Erőforrás   lefoglalás** | **Teljes óraszám** | Hé 6/4 | Ke 6/5 | Sze 6/6 | Csü 6/7 | Pé 6/8 | Szo 6/9 | Va 6/10 | Hé 6/11 | Ke 6/12 | Sze 6/13 | Csü 6/14 | Pé 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Róbert                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Azonban nincs rendszerezett módját a lefoglat órák eloszlásának hozzárendeléséhez a feladatokhoz napi szinten. Ha a projektmenedzser kész arra, hogy az erőforrások rendelkezésre állásának megfelelően módosítsa a projekt ütemezését, el kell eltávolítania a hozzárendelést, és át kell dolgoznia a feladatokat, hogy megfeleljenek a lefoglalási eloszlásoknak.

Abban az esetben, ha egy szervezet kiadta a projekttervezés feladatát egy projektmenedzsernek és egy erőforrás-menedzsernek egy időben, a projektmenedzser határozza meg az ütemezést, amely tartalmazza a szükséges ráfordítás eloszlását. Az erőforrás-menedzser nem módosíthatja az ütemezést a projektmenedzser tudta nélkül a ráfordítási eloszlások módosításával a valós erőforrások foglalásakor. Ha az erőforrás-menedzser a projektmenedzser által kérttől eltérő dolgot teljesíti, meg kell állapodniuk arról, hogy milyen módosítások szükségesek a projektütemezésben.

Mivel a foglalások és a hozzárendelések nincsenek szorosan összekapcsolva, lehetséges a feladat kontúrjaitól eltérő kontúrok lefoglalása, vagy a hozzárendelések megváltoztatása, hogy olyan helyzeteket eredményezzen, ahol a foglalások és a hozzárendelések nem igazodnak egymáshoz.

Az **Egyeztetés nézet** segítségével a projektmenedzser láthatja a projektcsoport tagjainak foglalásait és feladatait. A nézet színek és mintázatok segítségével jeleníti meg, hol nem áll fenn egyezőség a csoport tagjainak foglalásai és hozzárendelései között. Ezen információk alapján a projektmenedzser javító intézkedéseket tehet vagy kiterjesztve az erőforrások foglalásait azokra az esetekre, ahol vannak hozzárendelések és nincsenek foglalások, vagy törölheti a foglalásokat, ahol az erőforrások le vannak foglalva, de nincsenek hozzárendelések.

> [!NOTE]
> Ha áthelyez egy olyan feladatot, amelyet saját maga kontúrozott, akkor ezek a kontúrok nem lesznek fenntartva. Az eloszlások újragenerálása a projektnaptár szerint történik meg, hogy tükrözze a változásokat a munkaórák és munkaszüneti napok szerint. Ez a rendszer kialakításából fakad, mivel a rendszer nem ismeri az eredeti kontúr szándékát, és nem tudja meghatározni, hogy van-e értelme megőrizni ezt a kontúrt egy új időszakban. Mivel a foglalások és a hozzárendelések le vannak választva, a foglalások megtartják az eredeti foglalási kontúrokat. Ebben az esetben törölni kell és újra le kell foglalni az új hozzárendelés eloszlásához.



[!INCLUDE[footer-include](../includes/footer-banner.md)]