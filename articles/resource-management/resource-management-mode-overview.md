---
title: Erőforrás-kezelési módok áttekintése
description: Ez a témakör a Dynamics 365 Project Operations Erőforráskezelés funkciójáról nyújt információkat.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367894"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="25fa9-103">Erőforrás-kezelési módok áttekintése</span><span class="sxs-lookup"><span data-stu-id="25fa9-103">Resource management modes overview</span></span>

<span data-ttu-id="25fa9-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="25fa9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="25fa9-105">A Dynamics 365 Project Operations két módot támogat a teljes foglalási folyamat végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="25fa9-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="25fa9-106">A kezelési mód projektparaméterként van definiálva, és módosítható az üzleti igények változása esetén.</span><span class="sxs-lookup"><span data-stu-id="25fa9-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="25fa9-107">Központi mód</span><span class="sxs-lookup"><span data-stu-id="25fa9-107">Central mode</span></span>
<span data-ttu-id="25fa9-108">Azoknál a szervezeteknél, akik központosítják az erőforrások elosztását a projektek számára, a központi mód biztosítja, hogy a projektmenedzserek a projekt szintjén meghatározhatják az erőforrás-követelményeket.</span><span class="sxs-lookup"><span data-stu-id="25fa9-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="25fa9-109">Az erőforrás-követelmények teljesítését egy erőforrás-kezelőre delegálja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="25fa9-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="25fa9-110">A projektmenedzserek elfogadhatják vagy visszautasíthatják azokat az erőforrásokat, amelyeket az erőforrás-kezelő javasolt.</span><span class="sxs-lookup"><span data-stu-id="25fa9-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Központi mód](./media/resource-management-central.png)

<span data-ttu-id="25fa9-112">Az erőforrások központi móddal való kezeléséhez lásd:</span><span class="sxs-lookup"><span data-stu-id="25fa9-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="25fa9-113">Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása</span><span class="sxs-lookup"><span data-stu-id="25fa9-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="25fa9-114">Nevesített erőforrások foglalása erőforrás-követelményekből</span><span class="sxs-lookup"><span data-stu-id="25fa9-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="25fa9-115">Erőforrás-kérelem elküldése</span><span class="sxs-lookup"><span data-stu-id="25fa9-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="25fa9-116">Erőforrás-követelmény teljesítése</span><span class="sxs-lookup"><span data-stu-id="25fa9-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="25fa9-117">Fogadja el vagy utasítsa el a javasolt projekt erőforrást egy erőforrás-kérésből</span><span class="sxs-lookup"><span data-stu-id="25fa9-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="25fa9-118">Hibrid mód</span><span class="sxs-lookup"><span data-stu-id="25fa9-118">Hybrid mode</span></span>
<span data-ttu-id="25fa9-119">Azoknál a szervezeteknél, akik rugalmasságot igényelnek az erőforrások elosztásában, a hibrid mód lehetővé teszi, hogy a projektmenedzserek és az erőforrás-menedzserek is tudják az erőforrásokat foglalni.</span><span class="sxs-lookup"><span data-stu-id="25fa9-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibrid mód](./media/resource-management-hybrid.png)

<span data-ttu-id="25fa9-121">A támogatott központi mód folyamata mellett a következő témakörök nyújtanak információkat a hibrid módban használható további támogatott foglalási folyamatokkal kapcsolatban:</span><span class="sxs-lookup"><span data-stu-id="25fa9-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="25fa9-122">Erőforrás közvetlen foglalása egy projekthez:</span><span class="sxs-lookup"><span data-stu-id="25fa9-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="25fa9-123">Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="25fa9-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="25fa9-124">Erőforrás foglalása az erőforrás-követelményekből:</span><span class="sxs-lookup"><span data-stu-id="25fa9-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="25fa9-125">Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása</span><span class="sxs-lookup"><span data-stu-id="25fa9-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="25fa9-126">Nevesített erőforrások foglalása erőforrás-követelményekből</span><span class="sxs-lookup"><span data-stu-id="25fa9-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]