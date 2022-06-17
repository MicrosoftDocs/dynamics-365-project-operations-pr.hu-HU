---
title: Költségekre vonatkozó pénzügyi becslések projekteknél
description: Ez a cikk a projektalapú költségek meghatározásáról vagy becsléséről nyújt tájékoztatást.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a29244a65dd88d3ba0f8333a63627bb0c068273
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925691"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Költségekre vonatkozó pénzügyi becslések projekteknél
_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations lehetővé teszi a projektmenedzserek számára, hogy minden projekthez vagy feladathoz projektalapú költségeket határozzanak meg. Minden költségelem társítható egy adott projektfeladathoz. A költségek különböző költségkategóriákba vannak kategorizálva, amelyek szervezeti szinten vannak definiálva. Az egyes költségkategóriák árképzése és költségszámítása az árlistában van meghatározva. 

Hajtsa végre a következő lépéseket a projektkiadások megtekintéséhez, hozzáadásához és törléséhez.

1. Nyissa meg a **Projektek** elemet, és jelölje ki a kezelni kívánt projektet.
2. Válassza ki a **Projektbecslések** lapot, és tekintse meg a projektek kiadásainak listáját.
3. Kiadás hozzáadásához válassza az **Új kiadás** lehetőséget. Másik lehetőségként jelölje ki a törlendő kiadást, majd válassza a **Kiadás törlése** lehetőséget.

Az alábbi tábla a projekt **Költségbecslési sor** mezőiről nyújt tájékoztatást. 

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Feladatok | A feladatok listája a projektben. Ez magában foglalja az összegző és levélcsomópont-feladatokat. | A költségbecslési sor feladatának kiválasztása hatással lesz a feladat becsült önköltségére és becsült költségértékesítésére. Ha ez a mező üresen lett hagyva, akkor a költségbecslés csak projektszinten lesz nyomon követve és összegezve. |
| Kategória | Azon tranzakciókategóriák listája, amelyek költségkategóriákat kapcsoltak az alkalmazásban. | A költségbecslési sorban a kategória kiválasztása hajtja az árképzést és a költségszámítást. |
| Kezdési dátum | Az előre jelzett dátum, amelyen a költség jelentkezni fog. | Ennek a mezőnek nincs későbbi hatása. |
| Egységcsoport | Ebben a mezőben az alapértelmezett érték abból az egységcsoportból származik, amely alapértelmezettként van beállítva a kiválasztott kategóriában. A mező frissítésével másik kiszereléscsoportot jelölhet ki. | Ennek a mezőnek nincs későbbi hatása. |
| Kiszerelés | Ebben a mezőben az érték alapértelmezetten a kijelölt kategória alapértelmezett kiszerelésére áll át. A mező frissítésével másik kiszerelést jelölhet ki. | A kiszerelés módosítása eltérő alapértelmezett kiszerelésárat és -költséget eredményez. |
| Mennyiség | Az Ön által benyújtandó becsült költség mennyisége. | Ennek a mezőnek nincs későbbi hatása. |
| Egységköltség | A kiválasztott kategória és kiszereléskombináció költsége a vonatkozó önköltségiár-listában beállítottak szerinti | A kiszerelésköltség mindig a projekt költségpénzében jelenik meg. |
| Egységár | A kiválasztott kategória és kiszereléskombináció ára a vonatkozó értékesítési árlistában beállítottak szerinti. | A kiszerelésár mindig a projekt értékesítési pénznemében jelenik meg. |
| Teljes összeg | A mennyiségi \* kiszerelésköltségként kiszámított költségösszeg.| A költségösszeg mindig a projekt költségpénznemében jelenik meg. |
| Értékesítés összesen | A mennyiségi \* kiszerelésár kiszámított értékesítési összeg. | Az értékesítési összeg mindig a projekt értékesítési pénznemében jelenik meg. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
