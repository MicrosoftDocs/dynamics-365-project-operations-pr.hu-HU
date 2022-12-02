---
title: Az alvállalkozói szerződésben rögzített összetevők felvételi ideje, költségei és anyagfelhasználása
description: Ez a cikk ismerteti, hogy az alvállalkozói összetevőiből származó projekteknél rögzített időt, költséget és anyagokat hogyan követi nyomon a Microsoft Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Az alvállalkozói szerződéshez tartozó projektekben rögzített összetevők felvételi ideje, költségei és anyagfelhasználása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a cikk ismerteti, hogy az alvállalkozói összetevőiből származó projekteknél rögzített időt, költséget és anyagokat hogyan követi nyomon a Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projektekre vonatkozó alvállalkozói idő költségszámítása
A Project Operations alkalmazásban a szerződéses dolgozók az alkalmazottakhoz hasonlóan rögzíthetik a projektekhez szükséges időt. Az idő megadásakor a projektekhez és/ vagy projektfeladatokhoz a szerződéses munkavállaló kiválaszthat egy adott alvállalkozót és alvállalkozói sort.

A szerződéses dolgozók által beküldött idő jóváhagyásakor a projektköltség az adott szerződés feldolgozói erőforráshoz beállított egységköltségrátájával lesz rögzítve az alvállalkozón található beszerzési árlista **Szerepkörárak** szakaszában.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Alvállalkozói költésségek költségszámítása a projektekben
A projektekhez kapcsolódó költségek megadásakor a költségbevitelhez kijelölhet egy alvállalkozói szerződést és egy alvállalkozói sort. 

Amikor ezt a költségbejegyzést beküldik és jóváhagyják, a költéségár a projekthez az egységköltség alapján lesz rögzítve, ami ahhoz a tranzakciókategóriához van beállítva az alvállalkozói szerződés beszerzési árlistájának **Kategóriaárak** szakaszában.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Alvállalkozói anyagok költségszámítása a projektekben
A projektekhez kapcsolódó anyaghasználat megadásakor kijelölhet egy alvállalkozói szerződést és egy alvállalkozói sort az anyaghasználati naplóban. Amikor ezt az anyaghasználati naplót beküldik és jóváhagyják, az anyagár a projekthez az egységköltség alapján lesz rögzítve, ami ahhoz a termékhez van beállítva az alvállalkozói szerződés beszerzési árlistájának **Árlistaelemek** szakaszában.

A projektekbe nem katalogizált termékeihez is rögzíthet anyaghasználatot. Az ilyen típusú anyaghasználat alvállalkozói szerződéshez és alvállalkozói sorokhoz is kapcsolódhat. Nem katalogizált termékekhez használt anyagok rögzítésekor meg kell adnia a nem katalogizált termék egységárát. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
