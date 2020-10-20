---
title: Ütemezési segéd áttekintése
description: Ez a témakör az erőforrások Ütemezési segéddel végzett foglalásához nyújt tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908222"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="651db-103">Ütemezési segéd áttekintése</span><span class="sxs-lookup"><span data-stu-id="651db-103">Schedule assistant overview</span></span>

<span data-ttu-id="651db-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="651db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="651db-105">Az Ütemezési segéd erőforrások foglalására szolgál a projektmenedzser által meghatározott követelmények alapján.</span><span class="sxs-lookup"><span data-stu-id="651db-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="651db-106">Az ütemezési segéd az erőforrás-követelményben megadott paraméterekre támaszkodik az erőforrás megkereséséhez.</span><span class="sxs-lookup"><span data-stu-id="651db-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="651db-107">Az Ütemezési segéd olyan erőforrásokat javasol, amelyek megfelelnek a vonatkozó követelményeknek, például az időablakoknak vagy a szükséges szakértelmeknek.</span><span class="sxs-lookup"><span data-stu-id="651db-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="651db-108">A megfelelő erőforrások azonosítását követően az erőforráskezelő vagy a projektmenedzser lefoglalhatja az erőforrást a munkához.</span><span class="sxs-lookup"><span data-stu-id="651db-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="651db-109">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="651db-109">Prerequisites</span></span>

<span data-ttu-id="651db-110">Az Ütemezési segéd a Universal Resource Scheduling megoldás része.</span><span class="sxs-lookup"><span data-stu-id="651db-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="651db-111">Ez a megoldás megtalálható a Dynamics 365 Project Operations, a Dynamics 365 Field Service és a Dynamics 365 Customer Service termékekben, és azokkal együtt kerül telepítésre.</span><span class="sxs-lookup"><span data-stu-id="651db-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="651db-112">Erőforrások és követelmények párosítása</span><span class="sxs-lookup"><span data-stu-id="651db-112">Matching requirements and resources</span></span>

<span data-ttu-id="651db-113">A létrehozott erőforrás-követelmény olyan részleteken alapul, mint például:</span><span class="sxs-lookup"><span data-stu-id="651db-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="651db-114">Jellemzők</span><span class="sxs-lookup"><span data-stu-id="651db-114">Characteristics</span></span>
-   <span data-ttu-id="651db-115">Szerepkörök</span><span class="sxs-lookup"><span data-stu-id="651db-115">Roles</span></span>
-   <span data-ttu-id="651db-116">Részlegek</span><span class="sxs-lookup"><span data-stu-id="651db-116">Business units</span></span>
-   <span data-ttu-id="651db-117">Erőforrás-preferenciák</span><span class="sxs-lookup"><span data-stu-id="651db-117">Resource preferences</span></span>
-   <span data-ttu-id="651db-118">Munkaigénykontúrok</span><span class="sxs-lookup"><span data-stu-id="651db-118">Effort contours</span></span>
-   <span data-ttu-id="651db-119">Időzóna</span><span class="sxs-lookup"><span data-stu-id="651db-119">Time zone</span></span>

<span data-ttu-id="651db-120">Az Ütemezési segéd ezeket az adatokat használja az erőforrások szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="651db-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="651db-121">Az Ütemezési segéd indítása</span><span class="sxs-lookup"><span data-stu-id="651db-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="651db-122">Az ütemezési segéd kétféleképpen indítható el.</span><span class="sxs-lookup"><span data-stu-id="651db-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="651db-123">Ha hibrid módot használ, a csapattagrácsában bármelyik csapattagot kijelölheti, akinek nem teljesült erőforrás-követelménye van, majd kiválaszthatja a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="651db-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="651db-124">Ha a központi módot használja, az erőforrás-kezelő megkeresi és kiválasztja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="651db-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="651db-125">Ütemezési segéd szűrői</span><span class="sxs-lookup"><span data-stu-id="651db-125">Schedule assistant filters</span></span>

<span data-ttu-id="651db-126">Az Ütemezési segéd futását követően az erőforrás-követelmény részletei szűrt értékként jelennek meg a bal oldali ablaktáblában.</span><span class="sxs-lookup"><span data-stu-id="651db-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="651db-127">Az erőforrás-kezelő vagy a projektmenedzser az ütemezési igényeknek megfelelően, a szűrők módosításával finomíthatja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="651db-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="651db-128">A szűrőablakon a munkával kapcsolatos beállítások láthatók, például:</span><span class="sxs-lookup"><span data-stu-id="651db-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="651db-129">Munka kezdete és befejezése</span><span class="sxs-lookup"><span data-stu-id="651db-129">Work start and end</span></span>
-   <span data-ttu-id="651db-130">Jellemzők</span><span class="sxs-lookup"><span data-stu-id="651db-130">Characteristics</span></span>
-   <span data-ttu-id="651db-131">Szerepkörök</span><span class="sxs-lookup"><span data-stu-id="651db-131">Roles</span></span>
-   <span data-ttu-id="651db-132">Szervezeti egységek</span><span class="sxs-lookup"><span data-stu-id="651db-132">Organizational units</span></span>
-   <span data-ttu-id="651db-133">Erőforrás-kezelő vállalat</span><span class="sxs-lookup"><span data-stu-id="651db-133">Resourcing company</span></span>
-   <span data-ttu-id="651db-134">Erőforrástípusok</span><span class="sxs-lookup"><span data-stu-id="651db-134">Resource types</span></span>
-   <span data-ttu-id="651db-135">Előnyben részesített erőforrások</span><span class="sxs-lookup"><span data-stu-id="651db-135">Preferred resources</span></span>
