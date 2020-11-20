---
title: Erőforrás-kezelési alapfogalmak
description: Ez a témakör a Microsoft Dynamics Project Operations erőforrás-kezelés képességével kapcsolatos információkat tartalmaz.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a14f0ec328049d1b199201955c384df9fac61e39
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123876"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="99564-103">Erőforrás-kezelési alapfogalmak</span><span class="sxs-lookup"><span data-stu-id="99564-103">Resource management key concepts</span></span>

<span data-ttu-id="99564-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="99564-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99564-105">Az erőforrások a szolgáltatás-alapú szervezetek legfontosabb eszközei.</span><span class="sxs-lookup"><span data-stu-id="99564-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="99564-106">Az a képesség, hogy megfelelő időben megtalálja a megfelelő erőforrásokat, lefoglalja ezeket az erőforrásokat a projektekre és felhasználhatóvá tegye őket, elősegíti a szervezet számára a bevételi célok és az ügyfelek elégedettségének elérését.</span><span class="sxs-lookup"><span data-stu-id="99564-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="99564-107">A projekt-erőforrás-szolgáltatási funkciót a Dynamics 365 Project Operations szolgáltatásban a következő feladatok végrehajtásához használhatja:</span><span class="sxs-lookup"><span data-stu-id="99564-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="99564-108">A projektcsoportokat formálhatja a rendelkezésre álló és képzett erőforrások lefoglalásával.</span><span class="sxs-lookup"><span data-stu-id="99564-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="99564-109">Készítsen általános csapattag-nyilvántartásokat, és határozza meg szerepüket és az erőforrás-szervezeti egységet.</span><span class="sxs-lookup"><span data-stu-id="99564-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="99564-110">Generáljon erőforrás-követelményeket az általános csapattagok számára a feladatukból.</span><span class="sxs-lookup"><span data-stu-id="99564-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="99564-111">Összehangolja a készségeket az erőforrás-igény alapján meghatározott készségek azonosításával a rendelkezésre álló erőforrás-készségekkel.</span><span class="sxs-lookup"><span data-stu-id="99564-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="99564-112">Helyettesítő források.</span><span class="sxs-lookup"><span data-stu-id="99564-112">Substitute resources.</span></span>
- <span data-ttu-id="99564-113">Igazítsa a projektütemezési feladatokat és az erőforrás-könyveket.</span><span class="sxs-lookup"><span data-stu-id="99564-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="99564-114">Összehangolja a különbségeket a foglalások és a megbízások között.</span><span class="sxs-lookup"><span data-stu-id="99564-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="99564-115">Az erőforrás-foglalás megváltoztatása az irodán kívüli állapotra reagálva.</span><span class="sxs-lookup"><span data-stu-id="99564-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="99564-116">Együttműködés a projektvezetők és az erőforrás-kezelők között.</span><span class="sxs-lookup"><span data-stu-id="99564-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="99564-117">Tekintse meg az erőforrás-felhasználás előzményeit a célhoz viszonyítva, beleértve az erőforrások idejének felhasználásának bontását.</span><span class="sxs-lookup"><span data-stu-id="99564-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="99564-118">Fenntartja a készségek és jártassági adattárat.</span><span class="sxs-lookup"><span data-stu-id="99564-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="99564-119">A Project Operationsben általános vagy megnevezett erőforrásokkal láthatja el munkaerővel a projektet.</span><span class="sxs-lookup"><span data-stu-id="99564-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="99564-120">Különböző módszerekkel felveheti és kijelölheti a csapattagokat, valamint kezelheti a foglalásaikat és feladataikat.</span><span class="sxs-lookup"><span data-stu-id="99564-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
