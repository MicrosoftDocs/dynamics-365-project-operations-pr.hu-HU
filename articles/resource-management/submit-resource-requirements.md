---
title: Erőforrás-kérelem elküldése
description: A létrehozott erőforrás-igényt erőforrás-kérésként is beadhatja. Ezután a kérést teljesítés céljából elküldik egy erőforrás-kezelőnek.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077986"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="9a74c-104">Erőforrás-kérelem elküldése</span><span class="sxs-lookup"><span data-stu-id="9a74c-104">Submit a resource request</span></span>

<span data-ttu-id="9a74c-105">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="9a74c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a74c-106">A létrehozott erőforrás-igényt erőforrás-kérésként is beadhatja.</span><span class="sxs-lookup"><span data-stu-id="9a74c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="9a74c-107">Ezután a kérést teljesítés céljából elküldik egy erőforrás-kezelőnek.</span><span class="sxs-lookup"><span data-stu-id="9a74c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="9a74c-108">A Dynamics 365 Project Operations rendszerben a **Projektek** oldalon válassza a **Csapat** lapot, hogy megtekintse a foglalható erőforrások listáját.</span><span class="sxs-lookup"><span data-stu-id="9a74c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="9a74c-109">Válassza ki a listából az általános erőforrást, amely rendelkezik erőforrás-követelménnyel, majd kattintson a **Kérés benyújtása** elemre.</span><span class="sxs-lookup"><span data-stu-id="9a74c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="9a74c-110">Az általános csapattag kérésének státusza **Benyújtott** lesz.</span><span class="sxs-lookup"><span data-stu-id="9a74c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="9a74c-111">Miután a kérést teljesítették az általános erőforrást egy megnevezett erőforrás váltja fel, ha az erőforrás-kezelő egy megnevezett erőforrás lefoglalásával teljesíti a kérést.</span><span class="sxs-lookup"><span data-stu-id="9a74c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="9a74c-112">Ellenkező esetben az általános erőforrás a csoporton marad, és a kérés állapota **Áttekintés szükséges** értékre változik , ha az erőforrás-kezelő egy megnevezett erőforrást javasolt.</span><span class="sxs-lookup"><span data-stu-id="9a74c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
