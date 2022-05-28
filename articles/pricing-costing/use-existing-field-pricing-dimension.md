---
title: Project Operations-mezők mint árképzési dimenziók
description: Ez a témakör a Dynamics 365 Project Operations rendszerben mezők árazási dimenzióként való használatáról nyújt információkat.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a68bfe5a61f032f28f69c1aaed29f12cbea285d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594121"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Project Operations-mezők mint árképzési dimenziók

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A **Tények** entitás számos olyan mezőt tartalmaz, amelyek használható árképzési dimenzióként erőforrásalapú árképzéshez. Például egy közös mező a **Foglalható erőforrás**. Kisebb, 20-30-nél kevesebb számlázható erőforrással rendelkező cégeknél egyszerűbb megközelítés lehet az egyes erőforrásokra jellemző számla- és költségráták meghatározása. Ahogy azonban a számlázható munkaerő nő, az erőforrás-specifikus arányok irreálisá válhatnak. Az erőforrások kinevezésével, tapasztaltabbá válásával párhuzamosan, illetve ahogy az erőforrások új készségeket szereznek, az erőforrások költsége és a számlázási díjak módosulnak. 

Egy másik példa a tranzakciós kategória. Az ügyfelek és az implementálók a tranzakciós kategóriát használják a munka osztályozására, és a mező használatára az ár és a költség alapján a munka kategóriája alapján.


[!INCLUDE[footer-include](../includes/footer-banner.md)]