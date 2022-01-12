---
title: Az alvállalkozói alkatrészek töltött idejének, költségeinek és anyaghasználatának rögzítése
description: Ez a témakör azt ismerteti, hogy az alvállalkozói összetevőkből származó projekteken rögzített időt, költségeket és anyaghasználatot a Microsoft hogyan követi nyomon Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903678"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Az alvállalkozói alkatrészek projektjeinek ideje, költségei és anyaghasználata

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör azt ismerteti, hogy az alvállalkozói összetevőkből származó projekteken rögzített időt, költségeket és anyaghasználatot a Microsoft hogyan követi nyomon Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Az alvállalkozói idő költsége a projekteken
A Projektműveletekben a szerződéses alkalmazottak az alkalmazottakhoz hasonló módon rögzíthetik a projektek idejét. A projektek és/vagy projektfeladatok időbe adásakor a szerződéses munkavállaló kiválaszthat egy adott alvállalkozói és alvállalkozói sort.

A szerződéses alkalmazottak által benyújtott idő jóváhagyásakor a projektköltséget az adott szerződéses feldolgozói erőforráshoz az alvállalkozó beszerzési árlistájának Szerepkör árak szakaszában beállított egységköltség-arány alapján kell **elszámolni**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>A projektek alvállalkozásba adásának költségei
A projektek költségeinek megadásakor a költségtételen kiválaszthat egy alvállalkozói és alvállalkozói sort. 

Amikor ezt a költségtételt benyújtják és jóváhagyják, a költségköltséget az adott tranzakciókategóriához az **alvállalkozó beszerzési árlistájának Kategória árak szakaszában beállított egységköltség alapján kell** elszámolni.

## <a name="costing-for-subcontracted-materials-on-projects"></a>A projektek alvállalkozói anyagának költsége
A projektek anyagfelhasználásának megadásakor az anyaghasználati naplóban kiválaszthat egy alvállalkozói és alvállalkozói sort. Az anyaghasználati napló benyújtásakor és jóváhagyásakor az anyagköltséget a projekten az adott termékhez az **alvállalkozói árlista Árlista-cikkek szakaszában beállított egységköltség alapján** rögzítik.

Az anyaghasználat a projekteken lévő termékek írására is rögzíthető. Az ilyen típusú anyagfelhasználás alvállalkozói és alvállalkozói vonalhoz is kapcsolható. A beírt termékek anyaghasználatának rögzítésekor meg kell adnia a beírt termék egységenkénti költségét. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
