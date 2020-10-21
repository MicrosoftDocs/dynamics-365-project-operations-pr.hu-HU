---
title: Termékalapú árajánlatsorok költségszámítása
description: Ez a témakör az önköltség termékalapú árajánlatsorokra való alkalmazásával kapcsolatban tartalmaz információkat.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906198"
---
# <a name="costing-product-based-quote-lines"></a>Termékalapú árajánlatsorok költségszámítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A Dynamics 365 Project Operations alkalmazásban a termékalapú árajánlatsorokhoz tartozik egy **Önköltségi ár** mező is. A mező segítségével nyomon követheti a termék önköltségi árát az árajánlatsorban és a későbbi jövedelmezőségi számításokhoz.

Ha egy termékalapú árajánlatsor jön létre egy termékkatalógushoz, akkor a termékalapú árajánlatsor költségét a rendszer alapértelmezés szerint a termékkatalógus **Általános költség** mezőjéből számítja ki. A termékkatalógus általános költség mezőjének beállítása a szervezet alappénznemében történik. A termékalapú árajánlatsor alapértelmezett egységköltségét az árajánlatban szereplő értékesítési pénznemre váltja át a rendszer.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Termékalapú árajánlatsor egységára

A termékalapú árajánlatsor egységköltségének a célja, hogy lehetővé tegye a különböző költségeket egy termék egyes értékesítéseinél. Ez nem tipikus eset, de néha a termék költségét a szállító a végső értékesítés ügyfelétől függően diszkontálhatja.

Például:

A Fabrikam Robotics a robotkarok telepítését végzi el az A Datum Corporation gyártósorain. A fabrikam üzembe helyezési szolgáltatásokat biztosít, de a robotkarokat a Trey Roboticstól szerzi be. Ha a robotkarok telepítése az A Datum Corporation helyszínén új ipari vertikumot nyit a Trey robotkarjai számára, akkor a Trey speciális engedményt adhat ehhez az üzlethez a Fabrikam számára.

Ebben az esetben a Fabrikam létrehoz egy termékalapú árajánlatsort a robotkarok számára, és az árajánlathoz külön egységköltséget ad meg. Ez a költség eltér a Trey robotkarok általános költségétől.
