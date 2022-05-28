---
title: Alvállalkozóiprojektcsoporttag-regisztráció
description: Ez a témakör bemutatja, hogyan lehet alvállalkozásba adni a projektcsapat tagjait a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587849"
---
# <a name="subcontracting-project-team-members"></a>Alvállalkozóiprojektcsoporttag-regisztráció

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations programban választhat, hogy alvállalkozásba adja a személyzettel nem rendelkező vagy személyzettel rendelkező projektcsapat tagjait.

- A projektcsapat személyzettel nem rendelkező tagjaihoz általános erőforrás van hozzárendelve.
- A személyzet tagjai egy elnevezett erőforrással rendelkeznek.

Amikor egy projektcsapat-tagot alvállalkozói sorhoz kapcsol, a csapattag tevékenységeihez rendelt hozzárendelések az alvállalkozóhoz csatolt beszerzési árlista alapján újraküldetjük.  **A Projekt részletei** lap Becslések **lapján** válassza az Árak frissítése gombot **az** alvállalkozói szerződéskötésről szóló döntésből eredő frissített árképzés és/vagy költségszámítás megtekintéséhez. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Nem álló projektcsapat-tag alvállalkozásba adása
A **Csapattag adatai** lap alvállalkozói és alvállalkozói sormezőkkel rendelkezik, amelyek lehetővé teszik a projektmenedzser számára, hogy kifejezze, hogyan szeretné lehívni az alvállalkozói szerződésből szükséges kapacitást. Ha egy projektcsapat-tagot általános erőforrásként szeretne alvállalkozásba adni, hajtsa végre az alábbi lépéseket:

1.  Válasszon egy alvállalkozót a **Csapattag részletes** oldalán.

2.  Csak Piszkozat **vagy** Megerősített **állapotú alvállalkozókat** választhat. **A lezárt** vagy **visszavont** alvállalkozók nem választhatók ki. 

3.  Az **Alvállalkozói sor mező az alvállalkozói szerződés** kiválasztása után válik láthatóvá.

4.  Az Alvállalkozói **sor** mezőben csak az időre vonatkozó alvállalkozói sorokat választhatja ki. Költséghez vagy anyaghoz nem választhat alvállalkozói sorokat.

5.  A projektcsapat-bejegyzés szerepkörének meg kell egyeznie az alvállalkozói sorban szereplő szerepkörrel. Ez biztosítja, hogy a projekten becsült szerepkör ideje ugyanaz a szerepkör legyen, mint az alvállalkozói sorban. 

Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az **általános csapattagsor Dolgozótípus** mezője Szerződés dolgozómunkásra **frissül**, az alvállalkozói szerződés érvényessége **pedig** Érvényes **értékre** lesz állítva.

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat személyzetének tagja alvállalkozói szerződése
Az általános vagy személyzet nélküli csapattagokhoz hasonlóan a projekthez szükséges személyzettel rendelkező csapattag-kapacitás is összekapcsolható egy alvállalkozói szerződéssel. A projektcsapat megnevezett tagjának alvállalkozásba adásához hajtsa végre az alábbi lépéseket:

1.  Győződjön meg arról, hogy a megnevezett erőforrás szerződési dolgozó típusú könyvelhető erőforrásként van beállítva. Győződjön meg arról is, hogy a **könyvelhető erőforrás Szállító** mezője megegyezik a kiválasztott alvállalkozó szállítójával. 

2.  Az alvállalkozókat csak Piszkozat **vagy** **Megerősített** állapotban választhatja ki. **A lezárt** vagy **visszavont** alvállalkozók nem választhatók ki. 

3.  Az **Alvállalkozói sor mező az alvállalkozói szerződés** kiválasztása után válik láthatóvá.

4.  Az Alvállalkozói **sor** mezőben csak az időre vonatkozó alvállalkozói sorokat választhatja ki. Költséghez vagy anyaghoz nem választhat alvállalkozói sorokat.

5.  A projektcsapat-bejegyzés szerepkörének meg kell egyeznie az alvállalkozói sorban szereplő szerepkörrel. Ez biztosítja, hogy a projekten becsült szerepkör ideje ugyanaz a szerepkör legyen, mint az alvállalkozói sorban. 

A Könyvelhető erőforrás **szerződéses dolgozótípusaként** beállított megnevezett projektcsapat-tagok nem érvényes **alvállalkozói** érvényességi állapotúak lesznek, ha nem alvállalkozáshoz kapcsolódnak alvállalkozói szerződés szerinti jogcímen. Ha egy megnevezett projektcsapat-tag alvállalkozói és alvállalkozói sorhoz van társítva, a **csapattag sor Dolgozó típusa** mezője Szerződés dolgozói **és** alvállalkozói **érvényesség** **értékre** frissül.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
