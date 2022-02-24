---
title: Költségekre vonatkozó pénzügyi becslések projekteknél
description: Ez a témakör a projektalapú kiadások definiálásával vagy becslésével kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701785"
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
