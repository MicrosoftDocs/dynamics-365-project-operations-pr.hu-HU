---
title: Erőforráskezelői útmutató
description: Útmutató az erőforrás-kezeléshez a Project Service szolgáltatásban
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752301"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="f44cb-103">Erőforrás-kezelői útmutató (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f44cb-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f44cb-104">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lehetőségek a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]-ben segítenek megtalálni a megfelelő erőforrást a megfelelő időben a megfelelő projekthez, és biztosítják, hogy az erőforrások kihasználása hatékony legyen.</span><span class="sxs-lookup"><span data-stu-id="f44cb-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="f44cb-105">Telepítse a vállalati tanácsadókat hatékonyan és eredményesen a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segítségével.</span><span class="sxs-lookup"><span data-stu-id="f44cb-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="f44cb-106">Ezek olyan eszközöket biztosítanak, amelyekre szüksége van az erőforrások ütemezéséhez a tanácsadási projektek ütemterve és követelményei, valamint a tanácsadók képzettségei és elérhetősége alapján.</span><span class="sxs-lookup"><span data-stu-id="f44cb-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="f44cb-107">Gyorsan megtalálhatja a legalkalmasabb tanácsadókat, akik elérhetők a projekthez, és könnyen átláthatja, hogyan lehet jobban ütemezni őket az egyes projektek lefutása során.</span><span class="sxs-lookup"><span data-stu-id="f44cb-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="f44cb-108">Az erőforrás-ütemezés segítségével a következőket teheti meg:</span><span class="sxs-lookup"><span data-stu-id="f44cb-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="f44cb-109">Összevetheti az erőforrásokat és a projekteket az alapján, hogy képzettségeik és jártassági szintjeik, mennyire megfelelők a projekt erőforrás-követelményei szempontjából.</span><span class="sxs-lookup"><span data-stu-id="f44cb-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="f44cb-110">Egyeztetheti egy erőforrás ütemezését egy projektnaptárral az erőforrás elérhetősége és beütemezett szabadideje alapján.</span><span class="sxs-lookup"><span data-stu-id="f44cb-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="f44cb-111">A színkódolást alkalmazó naptár vizuális segítséget nyújt az erőforrások elérhetőségéről.</span><span class="sxs-lookup"><span data-stu-id="f44cb-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="f44cb-112">Megvizsgálhatja az egyes tanácsadók kapacitását, és megállapíthatja, az adott kapacitás aktuális felhasználási módját.</span><span class="sxs-lookup"><span data-stu-id="f44cb-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="f44cb-113">Ez segít kideríteni, ha egy tanácsadó kihasználtsága túl magas vagy túl alacsony mértékű, illetve hogy a kapacitásuknak megfelelően dolgoznak-e.</span><span class="sxs-lookup"><span data-stu-id="f44cb-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="f44cb-114">Egy adott százalék, vagy egy konkrét óraszámot hozzárendelése egy dolgozó kapacitásához egy projektben.</span><span class="sxs-lookup"><span data-stu-id="f44cb-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="f44cb-115">Erőforrások csoportos lefoglalása.</span><span class="sxs-lookup"><span data-stu-id="f44cb-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="f44cb-116">Erőforrások ideiglenes vagy végleges lefoglalása, illetve az ideiglenes foglalások egy lépésben történő átalakítása végleges foglalássá.</span><span class="sxs-lookup"><span data-stu-id="f44cb-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="f44cb-117">Projektcsoport automatikus kialakítása a projekt munkalebontási struktúrájában meghatározott erőforrások alapján.</span><span class="sxs-lookup"><span data-stu-id="f44cb-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="f44cb-118">Erőforrás-kérelmek teljesítése (helyettesítő erőforrások lefoglalása, javaslása és keresése).</span><span class="sxs-lookup"><span data-stu-id="f44cb-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="f44cb-119">Az erőforrások hozzárendelése történhet egy központi (az erőforrás-kezelő végzi a hozzárendelést) vagy egy hibrid (az erőforrás-kezelőn kívül más vezetők is elvégezhetik a hozzárendelést) modell alapján.</span><span class="sxs-lookup"><span data-stu-id="f44cb-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="f44cb-120">Egy központi vagy hibrid erőforrás-kezelési modell és annak beállításával kapcsolatos további információkért lásd: [További paraméterek beállításainak konfigurálása (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="f44cb-121">Több projektre kiterjedően is hatékonyan kezelheti az erőforrásokat, és biztosíthatja, hogy a projektek megfelelő személyzettel ellátottak legyenek.</span><span class="sxs-lookup"><span data-stu-id="f44cb-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="f44cb-122">A következő feladatokat kell végrehajtania:</span><span class="sxs-lookup"><span data-stu-id="f44cb-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="f44cb-123">[Erőforrás-kérelmek kezelése](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="f44cb-124">Párosítsa tanácsadói képzettségeit és jártasságait a megfelelő projektekhez.</span><span class="sxs-lookup"><span data-stu-id="f44cb-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="f44cb-125">[Erőforrás elérhetőségének megtekintése](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="f44cb-126">Ellenőrizze a tanácsadók elérhetőségét egy naptárnézetben.</span><span class="sxs-lookup"><span data-stu-id="f44cb-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="f44cb-127">[Erőforrás kihasználtság megtekintése](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="f44cb-128">Tekintse meg, hogy tanácsadói az idő hány százalékában vannak lefoglalva.</span><span class="sxs-lookup"><span data-stu-id="f44cb-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="f44cb-129">[Erőforrások ütemezése egy projekthez](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="f44cb-130">Tanácsadók időbeosztása egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="f44cb-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="f44cb-131">További információkért az egyes projektek erőforrás-kérelmeinek benyújtásával kapcsolatban lásd: [Erőforrás-kérelmek elküldése](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="f44cb-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f44cb-132">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="f44cb-132">See Also</span></span>  
 <span data-ttu-id="f44cb-133">[Project Service áttekintése](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f44cb-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="f44cb-134">[Rendszergazdai útmutató](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f44cb-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="f44cb-135">[Partnerkezelői útmutató](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f44cb-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f44cb-136">[Projektmenedzseri útmutató](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f44cb-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="f44cb-137">Idő, Költségek és Együttműködési útmutató</span><span class="sxs-lookup"><span data-stu-id="f44cb-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)