---
title: Erőforrás-kérelem benyújtása
description: Ez a témakör információkat nyújt a projekt erőforrás iránti kérelem benyújtásáról.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752271"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="37355-103">Erőforrás-kérelem benyújtása</span><span class="sxs-lookup"><span data-stu-id="37355-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="37355-104">A létrehozott erőforrás-igényt erőforrás-kérésként is beadhatja.</span><span class="sxs-lookup"><span data-stu-id="37355-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="37355-105">Ezután a kérést teljesítés céljából elküldik egy erőforrás-kezelőnek.</span><span class="sxs-lookup"><span data-stu-id="37355-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="37355-106">A Project Service Automation (PSA) rendszerben a **Projektek** oldalon kattintson a **Csapat** fülre, hogy megtekintse a foglalható erőforrások listáját.</span><span class="sxs-lookup"><span data-stu-id="37355-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="37355-107">Válassza ki a listából az általános erőforrást, amely rendelkezik erőforrás-követelménnyel, majd kattintson a **Kérés benyújtása** elemre.</span><span class="sxs-lookup"><span data-stu-id="37355-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Erőforrás-kérés benyújtása](media/RM-how-to-18.png)

<span data-ttu-id="37355-109">Az általános csapattag kérésének státusza **Benyújtott** lesz.</span><span class="sxs-lookup"><span data-stu-id="37355-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="37355-110">Miután a kérést az erőforrás-kezelő teljesítette, az általános erőforrást egy megnevezett erőforrás váltja fel, ha az erőforrás-kezelő egy megnevezett erőforrás lefoglalásával teljesíti a kérést.</span><span class="sxs-lookup"><span data-stu-id="37355-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="37355-111">Ellenkező esetben az általános erőforrás a csapaton marad, és a kérés állapota **Áttekintés szükséges** értékre változik , ha az erőforrás-kezelő egy megnevezett erőforrást javasolt.</span><span class="sxs-lookup"><span data-stu-id="37355-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
