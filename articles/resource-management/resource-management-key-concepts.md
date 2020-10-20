---
title: Erőforrás-kezelési alapfogalmak
description: Ez a témakör a Microsoft Dynamics Project Operations erőforrás-kezelés képességével kapcsolatos információkat tartalmaz.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897544"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="cc61b-103">Erőforrás-kezelési alapfogalmak</span><span class="sxs-lookup"><span data-stu-id="cc61b-103">Resource management key concepts</span></span>

<span data-ttu-id="cc61b-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="cc61b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc61b-105">Az erőforrások a szolgáltatás-alapú szervezetek legfontosabb eszközei.</span><span class="sxs-lookup"><span data-stu-id="cc61b-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="cc61b-106">Az a képesség, hogy megfelelő időben megtalálja a megfelelő erőforrásokat, lefoglalja ezeket az erőforrásokat a projektekre és felhasználhatóvá tegye őket, elősegíti a szervezet számára a bevételi célok és az ügyfelek elégedettségének elérését.</span><span class="sxs-lookup"><span data-stu-id="cc61b-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="cc61b-107">A projekt-erőforrás-szolgáltatási funkciót a Dynamics 365 Project Operations szolgáltatásban a következő feladatok végrehajtásához használhatja:</span><span class="sxs-lookup"><span data-stu-id="cc61b-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="cc61b-108">A projektcsoportokat formálhatja a rendelkezésre álló és képzett erőforrások lefoglalásával.</span><span class="sxs-lookup"><span data-stu-id="cc61b-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="cc61b-109">Készítsen általános csapattag-nyilvántartásokat, és határozza meg szerepüket és az erőforrás-szervezeti egységet.</span><span class="sxs-lookup"><span data-stu-id="cc61b-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="cc61b-110">Generáljon erőforrás-követelményeket az általános csapattagok számára a feladatukból.</span><span class="sxs-lookup"><span data-stu-id="cc61b-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="cc61b-111">Összehangolja a készségeket az erőforrás-igény alapján meghatározott készségek azonosításával a rendelkezésre álló erőforrás-készségekkel.</span><span class="sxs-lookup"><span data-stu-id="cc61b-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="cc61b-112">Helyettesítő források.</span><span class="sxs-lookup"><span data-stu-id="cc61b-112">Substitute resources.</span></span>
- <span data-ttu-id="cc61b-113">Igazítsa a projektütemezési feladatokat és az erőforrás-könyveket.</span><span class="sxs-lookup"><span data-stu-id="cc61b-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="cc61b-114">Összehangolja a különbségeket a foglalások és a megbízások között.</span><span class="sxs-lookup"><span data-stu-id="cc61b-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="cc61b-115">Az erőforrás-foglalás megváltoztatása az irodán kívüli állapotra reagálva.</span><span class="sxs-lookup"><span data-stu-id="cc61b-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="cc61b-116">Együttműködés a projektvezetők és az erőforrás-kezelők között.</span><span class="sxs-lookup"><span data-stu-id="cc61b-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="cc61b-117">Tekintse meg az erőforrás-felhasználás előzményeit a célhoz viszonyítva, beleértve az erőforrások idejének felhasználásának bontását.</span><span class="sxs-lookup"><span data-stu-id="cc61b-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="cc61b-118">Fenntartja a készségek és jártassági adattárat.</span><span class="sxs-lookup"><span data-stu-id="cc61b-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="cc61b-119">A Project Operationsben általános vagy megnevezett erőforrásokkal láthatja el munkaerővel a projektet.</span><span class="sxs-lookup"><span data-stu-id="cc61b-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="cc61b-120">Különböző módszerekkel felveheti és kijelölheti a csapattagokat, valamint kezelheti a foglalásaikat és feladataikat.</span><span class="sxs-lookup"><span data-stu-id="cc61b-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
