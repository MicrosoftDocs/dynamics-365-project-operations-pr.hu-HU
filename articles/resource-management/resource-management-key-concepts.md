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
ms.openlocfilehash: bcdfc7296ec09421668673d8502e7103c887d667
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279501"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="caed5-103">Erőforrás-kezelési alapfogalmak</span><span class="sxs-lookup"><span data-stu-id="caed5-103">Resource management key concepts</span></span>

<span data-ttu-id="caed5-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="caed5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="caed5-105">Az erőforrások a szolgáltatás-alapú szervezetek legfontosabb eszközei.</span><span class="sxs-lookup"><span data-stu-id="caed5-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="caed5-106">Az a képesség, hogy megfelelő időben megtalálja a megfelelő erőforrásokat, lefoglalja ezeket az erőforrásokat a projektekre és felhasználhatóvá tegye őket, elősegíti a szervezet számára a bevételi célok és az ügyfelek elégedettségének elérését.</span><span class="sxs-lookup"><span data-stu-id="caed5-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="caed5-107">A projekt-erőforrás-szolgáltatási funkciót a Dynamics 365 Project Operations a következő feladatokhoz használhatja:</span><span class="sxs-lookup"><span data-stu-id="caed5-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="caed5-108">A projektcsoportokat formálhatja a rendelkezésre álló és képzett erőforrások lefoglalásával.</span><span class="sxs-lookup"><span data-stu-id="caed5-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="caed5-109">Készítsen általános csapattag-nyilvántartásokat, és határozza meg szerepüket és az erőforrás-szervezeti egységet.</span><span class="sxs-lookup"><span data-stu-id="caed5-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="caed5-110">Generáljon erőforrás-követelményeket az általános csapattagok számára a feladatukból.</span><span class="sxs-lookup"><span data-stu-id="caed5-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="caed5-111">Összehangolja a készségeket az erőforrás-igény alapján meghatározott készségek azonosításával a rendelkezésre álló erőforrás-készségekkel.</span><span class="sxs-lookup"><span data-stu-id="caed5-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="caed5-112">Helyettesítő források.</span><span class="sxs-lookup"><span data-stu-id="caed5-112">Substitute resources.</span></span>
- <span data-ttu-id="caed5-113">Igazítsa a projektütemezési feladatokat és az erőforrás-könyveket.</span><span class="sxs-lookup"><span data-stu-id="caed5-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="caed5-114">Összehangolja a különbségeket a foglalások és a megbízások között.</span><span class="sxs-lookup"><span data-stu-id="caed5-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="caed5-115">Az erőforrás-foglalás megváltoztatása az irodán kívüli állapotra reagálva.</span><span class="sxs-lookup"><span data-stu-id="caed5-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="caed5-116">Együttműködés a projektvezetők és az erőforrás-kezelők között.</span><span class="sxs-lookup"><span data-stu-id="caed5-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="caed5-117">Tekintse meg az erőforrás-felhasználás előzményeit a célhoz viszonyítva, beleértve az erőforrások idejének felhasználásának bontását.</span><span class="sxs-lookup"><span data-stu-id="caed5-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="caed5-118">Fenntartja a készségek és jártassági adattárat.</span><span class="sxs-lookup"><span data-stu-id="caed5-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="caed5-119">A Project Operationsben általános vagy megnevezett erőforrásokkal láthatja el munkaerővel a projektet.</span><span class="sxs-lookup"><span data-stu-id="caed5-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="caed5-120">Különböző módszerekkel felveheti és kijelölheti a csapattagokat, valamint kezelheti a foglalásaikat és feladataikat.</span><span class="sxs-lookup"><span data-stu-id="caed5-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]