---
title: Beszerzési rendelések projekthez
description: A cikk ismerteti a projekthez tartozó beszerzési rendelések létrehozásához használható különböző módszereket. A használt metódus függ a beszerzési rendelés céljétól, hogy mikor használják fel a beszerzett cikkeket, és attól is, hogy mikor számítják fel a cikkeket a projekthez.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752213"
---
# <a name="purchase-orders-for-a-project"></a>Beszerzési rendelések projekthez

[!include [banner](../includes/banner.md)]

A cikk ismerteti a projekthez tartozó beszerzési rendelések létrehozásához használható különböző módszereket. A használt metódus függ a beszerzési rendelés céljétól, hogy mikor használják fel a beszerzett cikkeket, és attól is, hogy mikor számítják fel a cikkeket a projekthez.

### <a name="methods-for-creating-a-purchase-order"></a>Beszerzési rendelés létrehozásának módszerei

A következő módszerekkel hozhat létre beszerzési rendelést a Projektmenedzsment és könyvelés részben. A beszerzési rendelés célja meghatározza, hogy mikor használják fel a beszerzési rendelést, és ebből következően pedig azt is, hogy mikor számítják fel a cikkeket a projekthez.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Módszer</th>
<th>Cél</th>
<th>Cikkek felhasználása</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hozzon létre egy beszerzési megrendelést közvetlenül egy projektből.</td>
<td>Ezzel a módszerrel cikkeket vásárolhat egy külső szállítótól a projektben való felhasználás céljából. A beszerzési rendelést az alábbi két módszerrel hozhatja létre:
<ul>
<li>Magából a projektből. Ebben az esetben a projekt már meg van adva a beszerzési rendeléshez.</li>
<li>A projekt beszerzési rendeléséhez navigálva. A beszerzési rendelés létrehozásához a szállítót és a projektet is ki kell választania.</li>
</ul></td>
<td>A cikkek a szállítói számla frissítésekor kerülnek felhasználásra.</td>
</tr>
<tr class="even">
<td>Hozzon létre egy beszerzési rendelést közvetlenül egy értékesítési rendelésből.</td>
<td>Ennek a módszernek a használatával akkor vásároljon cikkeket, amikor értékesítési rendelést hoz létre egy projektből.</td>
<td>A cikkek akkor kerülnek felhasználásra, amikor az értékesítési rendelés ki van számlázva az ügyfélnek.</td>
</tr>
<tr class="odd">
<td>Hozzon létre egy beszerzési rendelést egy cikkszükségletből.</td>
<td>Ennek a módszernek a használatával akkor vásároljon cikkeket, amikor cikkszükségletet hoz létre egy projektből.</td>
<td>A felhasznált cikkeket a cikkszükséglet frissítésekor használják fel.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> A szállítói számla vagy a csomagjegyzék frissítésekor a rendszer felszólítja, hogy frissítse a szállítólevelet a cikkszükségleten.

További tudnivalókért lásd: [Cikkek bevételezése a beszerzési rendelésen cikkszükségletből](tasks/receive-items-purchase-order-item-requirement.md).

