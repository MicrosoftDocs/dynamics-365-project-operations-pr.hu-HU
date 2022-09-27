---
title: Alvállalkozóiprojektcsoporttag-regisztráció
description: Ez a cikk azt ismerteti, hogyan alvállalkozásba adhatja a projektcsapat tagjait a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522798"
---
# <a name="subcontracting-project-team-members"></a>Alvállalkozóiprojektcsoporttag-regisztráció

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoftban Dynamics 365 Project Operations választhatja a személyzet nélküli vagy személyzettel rendelkező projektcsapat tagjainak alvállalkozásba adását.

- A projektcsapat személyzet nélküli tagjaihoz általános erőforrás van hozzárendelve.
- A személyzettel rendelkező csapattagok egy elnevezett erőforrást rendelnek hozzá.

Amikor egy projektcsapat-tagot egy alvállalkozói sorhoz kapcsol, a csapattag által a feladatokhoz rendelt összes hozzárendelés az alvállalkozói szerződéshez csatolt beszerzési árlista alapján kerül sor.  **A Projekt részletei** lap Becslések **lapján** válassza az Árak **frissítése gombot az** alvállalkozói szerződésről szóló döntésből eredő frissített árképzés és/vagy költségszámítás megtekintéséhez. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>A projektcsapat személyzettel nem rendelkező tagjának alvállalkozásba adása
A **Csapattagok adatai** oldalon alvállalkozói és alvállalkozói sormezők találhatók, amelyek lehetővé teszik a projektmenedzser számára, hogy kifejezze, hogyan szeretné lehívni a szükséges kapacitást egy alvállalkozói szerződésből. Ha egy projektcsapat-tagot általános erőforrásként szeretne alvállalkozásba adni, kövesse az alábbi lépéseket:

1.  Válasszon ki egy alvállalkozói szerződést a **Csapattagok részletei** oldalon.

2.  Csak Vázlat **vagy** Megerősített **állapotú alvállalkozói szerződéseket** választhat. **A lezárt** vagy **törölt** alvállalkozói szerződések nem választhatók ki. 

3.  Az **Alvállalkozói sor** mező az alvállalkozói szerződés kiválasztása után válik láthatóvá.

4.  **Az Alvállalkozói sor** mezőben csak olyan alvállalkozói sorokat választhat ki, amelyek az időre vonatkoznak. Nem választhat alvállalkozói sorokat költség- vagy anyaghoz.

5.  A projektcsapat tagjainak rekordja szerepkörének meg kell egyeznie az alvállalkozói vonalon betöltött szereppel. Ez biztosítja, hogy a projekten becsült szerep ideje ugyanaz a szerepkör legyen, mint az alvállalkozói sorban. 

Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az általános csapattag sorban a **Dolgozó típusa** mező Szerződés-feldolgozóra **frissül,** az Alvállalkozói érvényesség **mezőben pedig** Érvényes **lesz**.

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat személyzettel rendelkező tagjának alvállalkozásba adása
Az általános vagy személyzet nélküli csapattagokhoz hasonlóan a projekthez szükséges személyzettag-kapacitás is összekapcsolható az alvállalkozói szerződésekkel. Egy megnevezett projektcsapattag alvállalkozásba adásához kövesse az alábbi lépéseket:

1.  Győződjön meg arról, hogy a megnevezett erőforrás szerződéses feldolgozó típusú foglalható erőforrásként van beállítva. Győződjön meg arról is, hogy a **foglalható erőforrás Szállító mezője** megegyezik a kiválasztott alvállalkozói szerződés szállítójával. 

2.  Az alvállalkozói szerződéseket **csak Vázlat** vagy **Megerősített** állapotban választhatja ki. **A lezárt** vagy **törölt** alvállalkozói szerződések nem választhatók ki. 

3.  Az **Alvállalkozói sor** mező az alvállalkozói szerződés kiválasztása után válik láthatóvá.

4.  **Az Alvállalkozói sor** mezőben csak olyan alvállalkozói sorokat választhat ki, amelyek az időre vonatkoznak. Nem választhat alvállalkozói sorokat költség- vagy anyaghoz.

5.  A projektcsapat tagjainak rekordja szerepkörének meg kell egyeznie az alvállalkozói vonalon betöltött szereppel. Ez biztosítja, hogy a projekten becsült szerep ideje ugyanaz a szerepkör legyen, mint az alvállalkozói sorban. 

Azok a megnevezett projektcsapat-tagok, akik szerződéses dolgozóként vannak beállítva a Foglalható erőforrás szerződéses dolgozói **típusként, alvállalkozói érvényességi állapottal** jelennek meg Nem érvényes **, ha nincsenek alvállalkozói szerződéshez kapcsolva.** Ha egy megnevezett projektcsapat-tag alvállalkozói és alvállalkozói sorhoz van társítva, a **csapattag sor Dolgozó típusa** mezője Szerződés-feldolgozóra **frissül**, és **az Alvállalkozói érvényesség** értéke Érvényes **lesz**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
