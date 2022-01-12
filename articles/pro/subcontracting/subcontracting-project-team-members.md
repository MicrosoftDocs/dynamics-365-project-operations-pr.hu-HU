---
title: Alvállalkozói projektcsapat tagjai
description: Ez a témakör elmagyarázza, hogyan alvállalkozásba adaktatja a projektcsapat tagjait a Microsoft programban Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903676"
---
# <a name="subcontracting-project-team-members"></a>Alvállalkozói projektcsapat tagjai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations programban dönthet úgy, hogy nem személyzettel vagy személyzettel nem dolgozó projektcsapat-tagokat ad át.

- A nem személyzettel rendelkező projektcsapat tagjai általános erőforrással rendelkeznek.
- A személyzet tagjai egy elnevezett erőforrással rendelkeznek.

Amikor egy projektcsapattagot egy alvállalkozói sorhoz kapcsol, a csapattag által végzett tevékenységekhez való hozzárendelések az alvállalkozóhoz csatolt beszerzési árlista alapján újracosodnak.  A **Projekt** részletei lap Becsültek lapján **válassza az Árak frissítése** gombot az **alvállalkozásról** szóló döntésből eredő frissített díjszabás és/vagy költségszámítás megtekintéséhez. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>A projektcsapat egy tagjának alvállalkozásba adása
A **csapattag adatai** oldalon alvállalkozási és alvállalkozói sormezők találhatók, amelyek lehetővé teszik a projektmenedzser számára, hogy kifejezze, hogyan szeretné felhívni az alvállalkozótól igényelt kapacitást. Ha általános erőforrásként szeretne alvállalkozásba adni egy projektcsapattagot, kövesse az alábbi lépéseket:

1.  Válasszon alvállalkozót a **Csapattag részletei** oldalon.

2.  Csak **Piszkozat vagy Megerősített állapotú alvállalkozókat választhat** **ki**. **A lezárt** vagy **a törölt** alvállalkozók nem választhatók ki. 

3.  **Az Alvállalkozó sor mező az alvállalkozó kiválasztása után** válik láthatóvá.

4.  Az **Alvállalkozó sor** mezőben csak az időre szóló alvállalkozói sorokat választhatja ki. A költségekhez vagy az anyaghoz nem választhat alvállalkozói sorokat.

5.  A projektcsapat-rekord szerepkörének meg kell egyeznie az alvállalkozói vonalon betöltött szereppel. Ez biztosítja, hogy a projekten becsült szerepkör ideje ugyanaz a szerepkör, amelyet az alvállalkozói sorban vásárolnak. 

Ha egy általános csapattag alvállalkozói és alvállalkozói sorhoz van társítva, az **általános csapattagsor Dolgozó típusa** mezője Szerződés-feldolgozóra frissül, és **az** **alvállalkozói érvényesség** érvényes **lesz**.

## <a name="subcontracting-a-staffed-project-team-member"></a>A projektcsapat munkatársának alvállalkozásba adása
Az általános vagy személyzet nélküli csapattagokhoz hasonlóan a projekthez szükséges személyzettel rendelkező csapattag kapacitása is összekapcsolható egy alvállalkozóval. Egy megnevezett projektcsapat-tag alvállalkozásba adása az alábbi lépéseket:

1.  Győződjön meg arról, hogy a megnevezett erőforrás a foglalható erőforrás szerződéses feldolgozó típusaként van beállítva. Győződjön meg arról is, hogy **a foglalható erőforrás Szállító** mezője megegyezik a kiválasztott alvállalkozó szállítójával. 

2.  Alvállalkozókat csak **Piszkozat vagy Megerősített állapotban választhat** **ki**. **A lezárt** vagy **a törölt** alvállalkozók nem választhatók ki. 

3.  **Az Alvállalkozó sor mező az alvállalkozó kiválasztása után** válik láthatóvá.

4.  Az **Alvállalkozó sor** mezőben csak az időre szóló alvállalkozói sorokat választhatja ki. A költségekhez vagy az anyaghoz nem választhat alvállalkozói sorokat.

5.  A projektcsapat-rekord szerepkörének meg kell egyeznie az alvállalkozói vonalon betöltött szereppel. Ez biztosítja, hogy a projekten becsült szerepkör ideje ugyanaz a szerepkör, amelyet az alvállalkozói sorban vásárolnak. 

A lefoglalható erőforrás szerződéses dolgozói típusként beállított megnevezett projektcsapat-tagok **nem** érvényes alvállalkozói érvényességi állapotúak **lesznek**, ha nem kapcsolódnak alvállalkozóhoz. Ha egy megnevezett projektcsapattag alvállalkozói és alvállalkozói sorhoz van társítva, a **csapattag sor Dolgozó típusa** mezője **szerződés-feldolgozóra frissül, az** **alvállalkozói érvényesség** pedig Érvényes **lesz**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
