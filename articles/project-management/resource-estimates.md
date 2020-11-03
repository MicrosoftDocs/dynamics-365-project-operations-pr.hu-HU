---
title: Erőforrásbecslések
description: Ez a témakör az erőforrásbecslések Project Operations rendszerben történő számításának módjáról tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078012"
---
# <a name="resource-estimates"></a>Erőforrásbecslések

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az erőforrás-becslések a megfelelő árképzési dimenziókkal rendelkező munkalebontási struktúrában meghatározott időfázisos erőfeszítésből származnak. A számítások általában: **arány/hr érték az egyes szerepkörökhöz x órák száma**. Az egyes erőforrások időfázisos erőfeszítéseit az erőforrás-hozzárendelési rekord tárolja. Az árazás egy előre megadott árlistában van tárolva. Az egységek átváltása a megfelelő árlista alapján kerül alkalmazásra.

![Erőforrásbecslések](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Alapértelmezett önköltségi ár és költségpénznem

Az önköltségi árak alapértelmezés szerint a szervezeti egységből származnak.

## <a name="default-bill-rate-and-sales-currency"></a>Alapértelmezett számlázási gyakoriság és értékesítési pénznem

Az értékesítési árak egy alkalommal kerülnek alkalmazásra. Az értékesítési árlista alapértelmezett hierarchiája a következő:

1. Cég
2. Ügyfél
3. Árajánlat/szerződés
