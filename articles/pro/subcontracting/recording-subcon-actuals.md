---
title: Az alvállalkozói szerződésben rögzített összetevők felvételi ideje, költségei és anyagfelhasználása
description: Ez a cikk azt ismerteti, hogy a Microsoft hogyan követi nyomon az alvállalkozói összetevőkből származó projekteken rögzített időt, költségeket és anyaghasználatot Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522516"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Idő, költségek és anyagfelhasználás rögzítése az alvállalkozói összetevők projektjein

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a cikk azt ismerteti, hogy a Microsoft hogyan követi nyomon az alvállalkozói összetevőkből származó projekteken rögzített időt, költségeket és anyaghasználatot Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Az alvállalkozói idő költsége a projekteken
A Project Operationsben a szerződéses dolgozók az alkalmazottakhoz hasonló módon rögzíthetik a projekteken töltött időt. Amikor időt ad meg a projektekhez és/vagy a projekttevékenységekhez, a szerződéses dolgozó kiválaszthat egy adott alvállalkozói és alvállalkozói sort.

A szerződéses dolgozók által beküldött idő jóváhagyásakor a projektköltséget a rendszer az alvállalkozói beszerzési árlista Szerepkörárak **szakaszában az adott szerződéses dolgozói erőforráshoz** beállított egységköltségi ráta alapján rögzíti.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>A projektek alvállalkozásba adott költségeinek költsége
A projekteken felmerült költségek megadásakor kiválaszthat egy alvállalkozói és alvállalkozói sort a költségbevitelben. 

Amikor ezt a költségbejegyzést elküldik és jóváhagyják, a költségköltséget a rendszer az alvállalkozói szerződés beszerzésiár-listájának Kategóriaárak **szakaszában az adott tranzakciós kategóriához** beállított egységköltség alapján rögzíti a projekten.

## <a name="costing-for-subcontracted-materials-on-projects"></a>A projektek alvállalkozásba adott anyagok költségszámítása
Amikor anyaghasználatot ad meg a projektekhez, kiválaszthat egy alvállalkozói és alvállalkozói sort az anyaghasználati naplóban. Az anyaghasználati napló elküldésekor és jóváhagyásakor az anyagköltséget a rendszer az alvállalkozói árlista Árlista cikkeinek **szakaszában az adott termékhez** beállított egységköltség alapján rögzíti a projekten.

Az anyagfelhasználás a projektek beírt termékeihez is rögzíthető. Ez a fajta anyagfelhasználás alvállalkozói és alvállalkozói vonalhoz is kapcsolható. A beírt termékek anyaghasználatának rögzítésekor meg kell adnia a beírt termék egységköltségét. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
