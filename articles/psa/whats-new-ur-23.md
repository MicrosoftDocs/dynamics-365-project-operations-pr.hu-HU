---
title: Újdonságok vagy változások a Project Service Automation 23-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 23-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131121"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="43e95-103">Project Service Automation 23-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="43e95-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="43e95-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="43e95-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="43e95-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="43e95-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="43e95-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="43e95-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="43e95-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="43e95-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="43e95-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="43e95-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="43e95-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 23-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="43e95-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="43e95-110">Ennek a verziónak a buildszáma V3.10.34.30, és általánosan elérhető egy önálló frissítésben 2020 augusztusában.</span><span class="sxs-lookup"><span data-stu-id="43e95-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="43e95-111">23-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="43e95-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="43e95-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="43e95-112">Bug fixes</span></span>

<span data-ttu-id="43e95-113">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="43e95-113">**Time and Expense**</span></span>

<span data-ttu-id="43e95-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="43e95-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="43e95-115">Az Edge-eset kezelése a **Projektcsoporttag törlése** opcióban, hogy értelmes kivételt adjon.</span><span class="sxs-lookup"><span data-stu-id="43e95-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="43e95-116">A hozzárendelés importálásának eredményei üres eltávolítási képernyőn.</span><span class="sxs-lookup"><span data-stu-id="43e95-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="43e95-117">**Erőforráskezelés**</span><span class="sxs-lookup"><span data-stu-id="43e95-117">**Resource Management**</span></span>

<span data-ttu-id="43e95-118">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="43e95-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="43e95-119">Az **Erőforrás-kihasználtsági rács erőforráskártya** nem megfelelő adatot jelenít meg, ha az időintervallum öt napnál nagyobb.</span><span class="sxs-lookup"><span data-stu-id="43e95-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="43e95-120">Ha az ügyfelek lefoglalható erőforrást hoznak létre, a beépülő modul időnként nem adja hozzá automatikusan az erőforrást egy Microsoft Office 365 csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="43e95-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="43e95-121">Az **Egyeztetés** nézet a **Heti** vagy a **Havi** nézetben hibásan jeleníti meg a manuális körvonalakat.</span><span class="sxs-lookup"><span data-stu-id="43e95-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="43e95-122">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="43e95-122">**Project Management**</span></span>

<span data-ttu-id="43e95-123">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="43e95-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="43e95-124">A **RetrieveMultiple for usersettings** entitások túlságosan nagy száma leromlott teljesítményt okoz a projektek jóváhagyása és az egyéb műveletek esetében.</span><span class="sxs-lookup"><span data-stu-id="43e95-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="43e95-125">A **Projekttervezés** rács erőforrás-keresése a projektcsapat csak öt tagjának megjelenítésére korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="43e95-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="43e95-126">A **Projekttervezés** rács erőforrás-keresés funkciója nem szűri az inaktív erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="43e95-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="43e95-127">A manuális mód nem a várt módon működik a projekttervezési munkalebontási struktúrában.</span><span class="sxs-lookup"><span data-stu-id="43e95-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="43e95-128">A **Projekttervezés** rács **Inaktív tranzakciós kategóriák** mezőt is megjelenít.</span><span class="sxs-lookup"><span data-stu-id="43e95-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="43e95-129">Az **Erőforrás-hozzárendelés** rács hibásan kerekíti az értékeket, ha egy feladathoz több hozzárendelés tartozik.</span><span class="sxs-lookup"><span data-stu-id="43e95-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="43e95-130">A kerekítési értékek eltérést mutatnak a tervezett költség és a tényleges költség között egy adott feladat esetében.</span><span class="sxs-lookup"><span data-stu-id="43e95-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="43e95-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="43e95-131">**Sales**</span></span>

<span data-ttu-id="43e95-132">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="43e95-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="43e95-133">Az **Összes tranzakciós kategória beolvasása** opcióra való dupla kattintás több sort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="43e95-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
