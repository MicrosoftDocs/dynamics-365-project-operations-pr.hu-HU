---
title: Projekterőforrás-ajánlat elfogadása vagy elutasítása
description: Ez a témakör projekterőforrás-ajánlatok jóváhagyásával vagy elutasításával kapcsolatban tartalmaz tájékoztatást.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e244ad48b4d6b50aea528d4ea378c28b8e42f2b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129861"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a><span data-ttu-id="5a148-103">Projekterőforrás-ajánlat elfogadása vagy elutasítása</span><span class="sxs-lookup"><span data-stu-id="5a148-103">Accept or reject a proposed project resource</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5a148-104">Ez a témakör projekterőforrás-ajánlatok jóváhagyásával vagy elutasításával kapcsolatban tartalmaz tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="5a148-104">This topic provides information about how to approve or reject a proposed project resource.</span></span>

<span data-ttu-id="5a148-105">Amikor egy erőforrás-kezelő egy elnevezett erőforrást ajánl egy projekt általános erőforrás-kérelmének kitöltéséhez, a rendszer frissíti az általános csoporttag **Kérelem állapota** mezőjét a következőre: **Ellenőrzés szükséges**.</span><span class="sxs-lookup"><span data-stu-id="5a148-105">When a resource manager proposes a named resource to fill the generic resource request for a project, the **Request Status** field for the generic team member will be updated to **Needs Review**.</span></span> <span data-ttu-id="5a148-106">A kérelmet a program elküldi jóváhagyásra vagy elutasításra a projektmenedzsernek.</span><span class="sxs-lookup"><span data-stu-id="5a148-106">The request will be sent to the project manager for approval or rejection.</span></span>

![Általános csoporttag ajánlattal](media/RM-how-to-19.png)

<span data-ttu-id="5a148-108">Az **Ajánlott erőforrások** fül **Projektcsoporttag** lapja mutatja az erőforrás-ajánlat aktuális foglalásait.</span><span class="sxs-lookup"><span data-stu-id="5a148-108">The grid on the **Proposed Resources** tab on the **Project Team Member** page shows the proposed resource’s current bookings.</span></span> <span data-ttu-id="5a148-109">Az ajánlat elfogadása után a rendszer frissíti a rácsot foglalás megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5a148-109">After the proposal is accepted, the grid is updated to reflect that booking.</span></span> 

<span data-ttu-id="5a148-110">Az erőforrás-ajánlat elfogadásához és az erőforrás csoportba foglalásához kattintson **Ajánlatok elfogadásak** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="5a148-110">To accept the proposed resource and book that resource on your team, click **Accept Proposals**.</span></span>  
<span data-ttu-id="5a148-111">Az ajánlat elutasításához kattintson az **Erőforrás visszautasítása** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="5a148-111">To reject the proposal, click **Reject Resource**.</span></span>

![Erőforrás-ajánlat elfogadása](media/RM-how-to-20.png) 

<span data-ttu-id="5a148-113">Egy általános erőforrás-kérés közvetlen teljesítése egy megnevezett erőforrással esetéhez hasonlóan az általános erőforrás lecserélésre kerül, és a hozzárendelt feladatokat frissíti a megnevezett csapattaggal.</span><span class="sxs-lookup"><span data-stu-id="5a148-113">Similar to directly fulfilling a generic resource request with a named resource, the generic resource will be replaced and the assigned tasks will be updated with the named team member.</span></span>
