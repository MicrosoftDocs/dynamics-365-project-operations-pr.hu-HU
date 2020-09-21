---
title: Erőforrások ütemezése egy projekthez
description: Erőforrások ütemezése projekthez a Project Service szolgáltatásban
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752299"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="c64a2-103">Erőforrások ütemezése projekthez (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c64a2-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c64a2-104">Ellenőrizheti az erőforrás-elérhetőséget, hogy átfogó képet kapjon az erőforrások foglaltságáról, vagy szűrheti a megjelenített elemeket képzettségek, csapat, hely és egyéb beállítások szerint.</span><span class="sxs-lookup"><span data-stu-id="c64a2-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="c64a2-105">Az ütemezési táblán az erőforrások és az elérhetőségük látható.</span><span class="sxs-lookup"><span data-stu-id="c64a2-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="c64a2-106">Rendelkezésre állás megjelenítése módjának kiválasztása: **óra**, **nap**, **hét**, vagy **hónap**.</span><span class="sxs-lookup"><span data-stu-id="c64a2-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="c64a2-107">Az ütemezés beállítása előtt fontos beállítani.</span><span class="sxs-lookup"><span data-stu-id="c64a2-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="c64a2-108">További információ: [Ütemezési tábla konfigurálása (Field Service vagy Project Service Automation)](../field-service/configure-schedule-board.md).</span><span class="sxs-lookup"><span data-stu-id="c64a2-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](../field-service/configure-schedule-board.md).</span></span>
  
<span data-ttu-id="c64a2-109">Régebbi verziójú rendszer használata esetén az erőforrások rendelkezésre állásához lásd: [Az erőforrás rendelkezésre állásának megtekintése](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="c64a2-109">If you are using an older version, for resource availability, see [View resource availability](../project-service/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="c64a2-110">Az ütemezésitábla-foglalás funkcióhoz, a geokódoláshoz és a helyszolgáltatásokhoz be kell kapcsolni a Térképet.</span><span class="sxs-lookup"><span data-stu-id="c64a2-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="c64a2-111">Válassza a főmenüben az **Erőforrás-ütemezés** > **Adminisztráció** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="c64a2-112">Kattintson az **Ütemezési paraméterekre**.</span><span class="sxs-lookup"><span data-stu-id="c64a2-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="c64a2-113">Nyissa meg a rekordot, és görgessen le a **Resource Scheduling Optimization** szakaszhoz.</span><span class="sxs-lookup"><span data-stu-id="c64a2-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="c64a2-114">A **Csatlakozás a Térképhez** mezőben válassza az **Igen** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="c64a2-115">Hagyja jóvá a feltételeket és mentse el a rekordot.</span><span class="sxs-lookup"><span data-stu-id="c64a2-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="c64a2-116">A főmenüben válassza a **Project Service** > **Ütemezési táblázat** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="c64a2-117">Innen többféle módon lehetséges egy foglalási követelményt manuálisan ütemezni.</span><span class="sxs-lookup"><span data-stu-id="c64a2-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="c64a2-118">Válassza ki az Ön számára megfelelő módot.</span><span class="sxs-lookup"><span data-stu-id="c64a2-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="c64a2-119">Elérhető erőforrások keresése</span><span class="sxs-lookup"><span data-stu-id="c64a2-119">Find available resources</span></span>

1.  <span data-ttu-id="c64a2-120">A **Foglalási követelmény**-listán kattintson jobb gombbal egy nem ütemezett foglalásra és válasszon az alábbiak közül:</span><span class="sxs-lookup"><span data-stu-id="c64a2-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="c64a2-121">Válassza a **Rendelkezésre állás keresése – Aktuális erőforrások** lehetőséget rendelkezésre álló erőforrások kereséséhez a listáról az ütemezési táblán.</span><span class="sxs-lookup"><span data-stu-id="c64a2-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="c64a2-122">Válassza a **Rendelkezésre állás keresése – Minden erőforrás** lehetőséget rendelkezésre álló erőforrás kereséséhez a rendszerben</span><span class="sxs-lookup"><span data-stu-id="c64a2-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="c64a2-123">Ha ezt elvégzi, akkor a szűrők a kijelölt foglalási szükséglethez tartozó beállításokat fogják megjeleníteni.</span><span class="sxs-lookup"><span data-stu-id="c64a2-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="c64a2-124">Amikor egy elérhető sávot lát, kattinson jobb gombbal az idősávra az ütemezési táblán, és válassza a **Foglalás itt** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="c64a2-125">Vagy húzza és dobja a foglalási követelést az elérhető időszeletbe.</span><span class="sxs-lookup"><span data-stu-id="c64a2-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="c64a2-126">Foglaljon le erőforrást a napi nézet segítségével, és keresse meg a kevésbé lefoglalt felhasználókat</span><span class="sxs-lookup"><span data-stu-id="c64a2-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="c64a2-127">Az ütemezési táblán válassza a **Nézet mód** lehetőséget, majd a **Napok** menüpontot.</span><span class="sxs-lookup"><span data-stu-id="c64a2-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="c64a2-128">Ez annak a rácsnézetét mutatja, hogy hány órát foglalt naponta az erőforrás, és mely napokon szabad.</span><span class="sxs-lookup"><span data-stu-id="c64a2-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="c64a2-129">Kattintson az erőforrás nevére, amelyet le szeretne foglalni, majd válassza a **Lefoglalás** elemet.</span><span class="sxs-lookup"><span data-stu-id="c64a2-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="c64a2-130">Az **Erőforrás-lefoglalás (létrehozás)** párbeszédpanelen válassza ki azt a projektet, amelyhez az erőforrást le akarja foglalni, valamint a foglalás módját, és a kezdő és befejező időpontokat.</span><span class="sxs-lookup"><span data-stu-id="c64a2-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="c64a2-131">Ha kész, válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="c64a2-132">Ütemezési tábla megtekintése</span><span class="sxs-lookup"><span data-stu-id="c64a2-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="c64a2-133">Válasszon egy nem ütemezett foglalási követelményt a listából alul.</span><span class="sxs-lookup"><span data-stu-id="c64a2-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="c64a2-134">Húzza a foglalási követelést egy rendelkezésre álló erőforrásba/időszeletbe az ütemezési táblázatban.</span><span class="sxs-lookup"><span data-stu-id="c64a2-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="c64a2-135">Ha kész, válassza a **Foglalás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c64a2-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="c64a2-136">További információforrások</span><span class="sxs-lookup"><span data-stu-id="c64a2-136">Additional resources</span></span>  
 [<span data-ttu-id="c64a2-137">Erőforráskezelői útmutató</span><span class="sxs-lookup"><span data-stu-id="c64a2-137">Resource manager guide</span></span>](../project-service/resource-manager-guide.md)