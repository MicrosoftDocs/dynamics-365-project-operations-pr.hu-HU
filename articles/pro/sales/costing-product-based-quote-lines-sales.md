---
title: Termékalapú árajánlatsorok költségszámítása
description: Ez a cikk az önköltség termékalapú árajánlatsorokra való alkalmazásával kapcsolatban tartalmaz információkat.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825614"
---
# <a name="costing-product-based-quote-lines"></a>Termékalapú árajánlatsorok költségszámítása

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A Dynamics 365 Project Operations termékalapú ajánlatsorai **Önköltségi ár** mezőt is tartalmaznak. A mező segítségével nyomon követheti a termék önköltségi árát az árajánlatsorban és a későbbi jövedelmezőségi számításokhoz.

Ha egy termékalapú árajánlatsor jön létre egy termékkatalógushoz, akkor a termékalapú árajánlatsor költségét a rendszer alapértelmezés szerint a termékkatalógus **Általános költség** mezőjéből számítja ki. A termékkatalógus általános költség mezőjének beállítása a szervezet alappénznemében történik. A termékalapú árajánlatsor alapértelmezett egységköltségét az árajánlatban szereplő értékesítési pénznemre váltja át a rendszer.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Termékalapú árajánlatsor egységára

A termékalapú árajánlatsor egységköltségének a célja, hogy lehetővé tegye a különböző költségeket egy termék egyes értékesítéseinél. Ez nem tipikus eset, de néha a termék költségét a szállító a végső értékesítés ügyfelétől függően diszkontálhatja.

Például:

A Fabrikam Robotics a robotkarok telepítését végzi el az A Datum Corporation gyártósorain. A fabrikam üzembe helyezési szolgáltatásokat biztosít, de a robotkarokat a Trey Roboticstól szerzi be. Ha a robotkarok telepítése az A Datum Corporation helyszínén új ipari vertikumot nyit a Trey robotkarjai számára, akkor a Trey speciális engedményt adhat ehhez az üzlethez a Fabrikam számára.

Ebben az esetben a Fabrikam létrehoz egy termékalapú árajánlatsort a robotkarok számára, és az árajánlathoz külön egységköltséget ad meg. Ez a költség eltér a Trey robotkarok általános költségétől.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
