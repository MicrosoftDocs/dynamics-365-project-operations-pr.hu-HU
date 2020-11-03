---
title: Használja az Ütemezési táblát a projekt erőforrásainak lefoglalásához
description: Ez a témakör információkat nyújt az erőforrások lefoglalásáról.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
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
ms.openlocfilehash: fa7e34b12f3767e89cc13ddde930e5c9f8ebc565
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078314"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="f73ac-103">Használja az Ütemezési táblát a projekt erőforrásainak lefoglalásához</span><span class="sxs-lookup"><span data-stu-id="f73ac-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="f73ac-104">Amellett, hogy egy projekten belül erőforrásokat foglal le egy projekten belül, az Ütemezési táblán is foglalhat keményen vagy puhán.</span><span class="sxs-lookup"><span data-stu-id="f73ac-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="f73ac-105">Mielőtt lefoglalhat az Ütemezési tábláról, létre kell hoznia vagy generálnia kell az erőforrás-követelményeket.</span><span class="sxs-lookup"><span data-stu-id="f73ac-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="f73ac-106">Kövesse ezeket a lépéseket az Ütemezési táblából az erőforrás-követelmények létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f73ac-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="f73ac-107">Ha az oldal alján található **Foglalási követelmények** ablaktábla összecsukódik, válassza ki a kibontásvezérlőt annak kibontásához.</span><span class="sxs-lookup"><span data-stu-id="f73ac-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="f73ac-108">A **Foglalási követelmények** panelen, a **Projekt** lapon válassza ki a foglalási követelményt.</span><span class="sxs-lookup"><span data-stu-id="f73ac-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![A Projekt lapon kiválasztott követelmény](media/Resource-Management-image73.png)

3. <span data-ttu-id="f73ac-110">Válassza a **Rendelkezésre állás** lehetőséget a foglalható források szűréséhez és a rendelkezésre álló források megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="f73ac-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="f73ac-111">Válasszon egy vagy több erőforrást az Ütemezési táblából.</span><span class="sxs-lookup"><span data-stu-id="f73ac-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="f73ac-112">Az **Erőforrás létrehozása foglalás** panel jobb oldalán, adja meg a foglalás adatait, majd válassza **Foglalás és kilépés** pontot.</span><span class="sxs-lookup"><span data-stu-id="f73ac-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Hozzon létre erőforrás-foglalási ablakot a kiválasztott foglalható erőforráshoz](media/Resource-Management-image74.png)

6. <span data-ttu-id="f73ac-114">Amíg a követelményt az **Erőforrás-foglalás létrehozása** panelen választja ki, válassza ki az erőforrás egy vagy több celláját a foglalás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f73ac-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Több cellát választott ki egy erőforráshoz](media/Resource-Management-image75.png)

7. <span data-ttu-id="f73ac-116">Válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f73ac-116">Select **Book**.</span></span>

<span data-ttu-id="f73ac-117">A követelmény a kiválasztott erőforrás felhasználásával teljesül.</span><span class="sxs-lookup"><span data-stu-id="f73ac-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="f73ac-118">A **Foglalási követelmények** panelen vegye figyelembe, hogy a követelményt frissítették, és az erőforrás a projektnél lefoglaltként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="f73ac-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Erőforrás lefoglalva a projektre](media/Resource-Management-image76.png)
