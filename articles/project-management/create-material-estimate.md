---
title: Anyagokra vonatkozó pénzügyi becslések projekteknél
description: Ez témakör a projektalapú anyagokra meghatározásáról vagy becsléséről nyújt tájékoztatást.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 089158666dc8fd09cd5d2b615715ed8aaff5575a
ms.sourcegitcommit: e6090e1fef5f475a3cd56b78b6abca29f90da8f5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2022
ms.locfileid: "8737305"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Anyagokra vonatkozó pénzügyi becslések projekteknél

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations lehetővé teszi a projektmenedzserek számára, hogy minden projekthez vagy feladathoz projektalapú anyagköltségeket határozzanak meg. Minden anyagbecslés társítható egy adott projektfeladathoz. A projektekben használt anyagok lehetnek beírt termékek vagy termékek a termékkatalógusból. Egy termék és egy egység minden egyes kombinációjához meg lehet határozni egy árat az értékesítések projektárlistáiban és a projekt költséglistáiban.  

Projektanyag-becslés megtekintéséhez, hozzáadásához vagy törléséhez végezze el a következő lépéseket.

1. Válassza a **Projektek** lehetőséget, és válassza ki a frissíteni kívánt projektet.
2. Az **Anyagbecslések** fülön tekintse meg a projektanyag-becslések listáját.
3. Az új anyagbecslés létrehozásához válassza az **Új anyagbecslés** lehetőséget. Vagy jelöljön ki egy törölni kívánt anyagbecslést, majd válassza az **Anyagbecslés törlése** lehetőséget.

Az alábbi tábla a project **Anyagbecslési sor** mezőiről nyújt tájékoztatást. 

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Feladatok | A feladatok listája a projektben. Ez magában foglalja az összegző és levélcsomópont-feladatokat. | Amikor kiválaszt egy feladatot egy anyagbecslési sorhoz, az hatással lesz a feladat becsült anyagköltségáre és becsült anyagértékesítésére. Ha ez a mező üres, az anyagbecslés csak projektszinten lesz nyomon követve és összegezve. |
| Termék kiválasztása |  Meghatározhatja, hogy a becsléssor a meglévő (katalogizált) vagy a nem katalogizált termékhez készült-e. | Ez a mező határozza meg, hogy kiválaszt-e egy terméket a katalogizált vagy nem katalogizált termékből. |
| Termék | A termékkatalógus termékazonosítója. Termékazonosító kiválasztásakor a **Termék kiválasztása** mezőben lévő érték automatikusan **Meglévő termék** mezővé frissül. Az azonosítót a költség- és értékesítési árak árlistából való beolvasására használják. | Ennek a mezőnek nincs későbbi hatása. |
| Nem katalogizált termék leírása | A termék nevének beírásához használt szövegmező. Ez a mező akkor használandó, ha a **Termék kiválasztása** mezőben a **Nem katalogizált** lehetőséget választja.| Ennek a mezőnek nincs későbbi hatása. |
| Kezdési dátum | Az az előre jelzett dátum, amikor az anyagot várhatóan fel kell használni. | Ennek a mezőnek nincs későbbi hatása. |
| Egységcsoport | Ebben a mezőben az alapértelmezett érték a katalógusterméken lévő alapértelmezett kiszereléscsoportból származik. A mező frissítésével másik kiszereléscsoportot jelölhet ki. | Ennek a mezőnek nincs későbbi hatása. |
| Kiszerelés | Ebben a mezőben lévő érték a kijelölt termék alapértelmezett kiszereléséből származik. A mező frissítésével másik kiszerelést jelölhet ki. | A kiszerelés módosítása eltérő alapértelmezett kiszerelésárat és -költséget eredményez. |
| Mennyiség | A projektben használni kívánt termék becsült mennyisége. | Ennek a mezőnek nincs későbbi hatása. |
| Egységköltség | A kiválasztott termék és kiszereléskombináció kiszerelésköltsége a vonatkozó önköltségiár-listában beállítottak szerinti. | A kiszerelésköltség mindig a projekt költségpénzében jelenik meg. Ha az árlistában nincs beállítva kiszerelésköltség a kombinált termékhez és kiszerelésbeállításhoz, a kiszerelésköltség alapértelmezés szerint 0,00 lesz. |
| Egységár | A kiválasztott termék és kiszereléskombináció ára a vonatkozó értékesítési árlistában beállítottak szerinti. | A kiszerelésár mindig a projekt értékesítési pénznemében jelenik meg. Ha az árlistában nincs beállítva kiszerelésár a kombinált termékhez és kiszerelésbeállításhoz, akkor a kiszerelésár alapértelmezés szerint 0,00 lesz.|
| Teljes összeg | A mennyiségi \* kiszerelésköltségként kiszámított költségösszeg.| A költségösszeg mindig a projekt költségpénznemében jelenik meg. |
| Értékesítés összesen | A mennyiségi \* kiszerelésár kiszámított értékesítési összeg. | Az értékesítési összeg mindig a projekt értékesítési pénznemében jelenik meg. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
