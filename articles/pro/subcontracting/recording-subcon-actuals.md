---
title: Az alvállalkozói szerződésben rögzített összetevők felvételi ideje, költségei és anyagfelhasználása
description: Ez a témakör azt mutatja be, hogy az alvállalkozói összetevőkből származó projekteken rögzített időt, költséget és anyagfelhasználást a Microsoft hogyan követi nyomon Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599227"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Az alvállalkozói összetevők projektjeinek idő-, költség- és anyagfelhasználásának rögzítése

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör azt mutatja be, hogy az alvállalkozói összetevőkből származó projekteken rögzített időt, költséget és anyagfelhasználást a Microsoft hogyan követi nyomon Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Az alvállalkozói idő költsége a projekteken
A Projektműveletek mezőben a szerződéses dolgozók az alkalmazottakhoz hasonló módon rögzíthetik a projekteken eltöltött időt. Amikor időt ad meg a projekteken és/vagy projekttevékenységeken, a szerződéses dolgozó kiválaszthat egy adott alvállalkozói és alvállalkozói sort.

A szerződéses dolgozók által benyújtott idő jóváhagyásakor a projektköltséget az alvállalkozó beszerzési árlistájának Szerepkör árak **szakaszában az** adott szerződéses dolgozói erőforráshoz beállított egységköltség-ráta alapján rögzíti a program.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>A projektek alvállalkozói költségeinek költsége
A projekteken felmerült költségek megadásakor a költségtételen kiválaszthat egy alvállalkozói és alvállalkozói sort. 

A költségtétel benyújtásakor és jóváhagyásakor a program a költségköltséget az adott tranzakciókategóriához beállított egységköltség alapján rögzíti a program az **alvállalkozó beszerzési árlistájának Kategória árak** szakaszában.

## <a name="costing-for-subcontracted-materials-on-projects"></a>A projektek alvállalkozói anyagainak költségszámítása
Amikor anyagfelhasználást ad meg a projektekben, kiválaszthat egy alvállalkozói és alvállalkozói sort az anyaghasználati naplóban. Az anyaghasználati napló elküldésekor és jóváhagyásakor a program az alvállalkozói árlista árlistájának Árlistatétel szakaszában **az adott termékhez beállított egységköltség alapján rögzíti az anyagköltséget a** projekten.

Az anyagfelhasználás a projektekben szereplő termékekbe való íráshoz is rögzíthető. Az ilyen típusú anyaghasználat alvállalkozói és alvállalkozói sorhoz is csatolható. A beírt termékek anyaghasználatának rögzítésekor meg kell adnia a beírt termék egységköltségét. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
