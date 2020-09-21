---
title: Szoftverkövetelmények
description: Ez a témakör információkat nyújt arról, hogyan kell foglalni a követelményeket.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752303"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="7b9a7-103">Szoftverkövetelmények</span><span class="sxs-lookup"><span data-stu-id="7b9a7-103">Soft-book requirements</span></span>

<span data-ttu-id="7b9a7-104">Az erőforrás-igény keményen foglalható.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="7b9a7-105">A kemény foglalás olyan javaslatot hoz létre, amely felhasználja az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="7b9a7-106">A javaslatot ezután visszatérés céljából megküldik a kérelmezőnek jóváhagyás céljából.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="7b9a7-107">A puha foglalás egy ideiglenesen hozzáad egy erőforrást a projektcsoporthoz, és más státusszal rendelkezik az Ütemezési táblán, de nem használja fel az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="7b9a7-108">Az erőforrás ütemezéséhez az Ütemezési táblán állítsa be a **Foglalási állapot** mezőt **Lágy** értékre.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![A foglalás státusa lágyra van állítva](media/Resource-Management-image77.png)

<span data-ttu-id="7b9a7-110">Amikor a **Csapat** fül a **Megnevezett csapattagok** nézetben található, ott jelenik meg az erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="7b9a7-111">A puhán foglalt órákat a **Puhán foglalt órák** oszlopban kell feltüntetni.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Kedvezményesen lefoglalva tartott órák a Megnevezett csapattagok nézetében](media/Resource-Management-image78.png)

<span data-ttu-id="7b9a7-113">A puha foglalású csapattagokat feladatokhoz lehet rendelni.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-113">Soft-booked team members can be assigned to tasks.</span></span>

![A feladathoz kiosztott, puha foglalású csapattag](media/Resource-Management-image79.png)

<span data-ttu-id="7b9a7-115">Az **Összehangolás** lapon nem jelennek meg a puhán foglalt erőforrások foglalása, mivel az **Összehangolás** lapon csak a nehéz foglalásokat veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Szoftverkönyvvel ellátott erőforrás foglalások nélkül az Egyeztetés lapon](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="7b9a7-117">Az erőforrást nem lehet könyvelni egy általános csapattag által generált követelmény alapján.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="7b9a7-118">Az Ütemezési táblán az erőforrás puha foglalásainak eltérő színezése történik.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Puha foglalás a menetrend táblán](media/Resource-Management-image81.png)

<span data-ttu-id="7b9a7-120">A puha foglalás átalakításához egy kemény foglalássá az Ütemező táblán kattintson a jobb gombbal a puha foglalásra, majd válassza az **Állapot megváltoztatása** \> **Kemény foglalás** \> **Nehéz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![A foglalás státuszának keményre változtatása](media/Resource-Management-image82.png)

<span data-ttu-id="7b9a7-122">A foglalás megváltozik, és az állapot megváltozik az Ütemezési táblán.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="7b9a7-123">Mivel a foglalási státus most **Kemény**, az erőforrás foglaltként jelenik meg, kapacitása és rendelkezésre állása módosítva.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="7b9a7-124">Ugyanezt a módszert használhatja a kemény foglalás vagy az engedményes foglalás törlésére az Ütemezési táblán.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="7b9a7-125">A projekt **Csapat** lapján a foglalt erőforrás nehezen foglalttá történő konvertálásához válassza ki az erőforrást, majd válassza a **Megerősítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="7b9a7-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Megerősítés parancs](media/Resource-Management-image83.png)