---
title: Projektek erőforrás-kezelése kezdőlap
description: Ez a témakör információkat nyújt a projekterőforrások biztosításáról.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 579a07e117cf00727813385da28d47f7e42f0127
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369469"
---
# <a name="project-resourcing-home-page"></a><span data-ttu-id="7545e-103">Projektek erőforrás-kezelése kezdőlap</span><span class="sxs-lookup"><span data-stu-id="7545e-103">Project resourcing home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7545e-104">Ez a témakör információkat nyújt a projekterőforrások biztosításáról.</span><span class="sxs-lookup"><span data-stu-id="7545e-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="7545e-105">Az egyik kihívás a projektmenedzserek és az erőforrás-menedzserek számára a projekt tervezési fázisában az erőforrás-elosztás, ahol meg kell határozniuk és le kell foglalniuk a megfelelő erőforrást a projekten végzett munkához.</span><span class="sxs-lookup"><span data-stu-id="7545e-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="7545e-106">A Dynamics 365 Finance alkalmazásban a projektek erőforrás-biztosítási képességei lehetővé teszik ideiglenes erőforrásokként kezelt szerepek megadását, amelyek lefoglalhatók egy adott aktivitáshoz vagy egy aktivitás részéhez.</span><span class="sxs-lookup"><span data-stu-id="7545e-106">In Dynamics 365 Finance, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="7545e-107">Az ilyen típusú erőforrás-biztosítás segítségével a projektmenedzserek és az erőforrás-menedzserek a következő feladatokat hajthatják végre:</span><span class="sxs-lookup"><span data-stu-id="7545e-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="7545e-108">Olyan szerepkört adhatnak meg, amely rendelkezik a szükséges kompetenciákkal, hogy könnyen megfeleltethető legyen az erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="7545e-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="7545e-109">Szerepkörök használatával megadhatják a fenntartott erőforrásokon alapuló kezdeti aktivitási ütemezést.</span><span class="sxs-lookup"><span data-stu-id="7545e-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="7545e-110">Megbecsülhetik a költségeket, és egy kezdeti költségvetést határozhatnak meg a projektek hozzárendelt szerepkörei és erőforrásai alapján.</span><span class="sxs-lookup"><span data-stu-id="7545e-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="7545e-111">A szerepkörök használatával megbecsülhetik az egyes aktivitásokhoz szükséges erőforrás-foglalások számát.</span><span class="sxs-lookup"><span data-stu-id="7545e-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="7545e-112">Megbecsülhetik az erőforrások számát, amelyek a projekt teljes életciklusához szükségesek.</span><span class="sxs-lookup"><span data-stu-id="7545e-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="7545e-113">Kidolgozhatnak egy munkalebontási struktúrát (WBS) a kezdeti erőforrás-hozzárendelések segítségével.</span><span class="sxs-lookup"><span data-stu-id="7545e-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="7545e-114">[![Projekt életciklusa](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="7545e-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="7545e-115">A projektek tervezése során a tervezett erőforrások lecserélhetők a munkatársakkal ellátott erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="7545e-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="7545e-116">A projektmenedzser ugyancsak visszatérhet, és frissítheti az erőforrás-biztosítási foglalásokat a projekt bármely fázisában.</span><span class="sxs-lookup"><span data-stu-id="7545e-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

<span data-ttu-id="7545e-117">A következő témakörök azokról a feladatokról tartalmaznak tájékoztatást, amelyeket a projektek erőforrás-kezelési projektjeinek végrehajtásakor végre kell hajtani.</span><span class="sxs-lookup"><span data-stu-id="7545e-117">The following topics provide information about the tasks that need to be completed when you are working on resourcing projects.</span></span>

- [<span data-ttu-id="7545e-118">Projekt-erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="7545e-118">Set up project resources</span></span>](set-up-project-resources.md)
- [<span data-ttu-id="7545e-119">Erőforrás-kompetenciák kezelése</span><span class="sxs-lookup"><span data-stu-id="7545e-119">Manage resource competencies</span></span>](manage-resource-competencies.md)
- [<span data-ttu-id="7545e-120">Új projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7545e-120">Create a new project</span></span>](create-new-project.md)
- [<span data-ttu-id="7545e-121">A szerepköralapú árképzés beállítása</span><span class="sxs-lookup"><span data-stu-id="7545e-121">Set up role-based pricing</span></span>](set-up-role-based-pricing.md)
- [<span data-ttu-id="7545e-122">Projektcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="7545e-122">Create a project team</span></span>](create-project-team.md)
- [<span data-ttu-id="7545e-123">Erőforráskapacitás szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="7545e-123">Synchronize resource capacity</span></span>](synchronize-resource-capacity.md)
- [<span data-ttu-id="7545e-124">Projekterőforrás ütemezési teljesítménye</span><span class="sxs-lookup"><span data-stu-id="7545e-124">Project resource scheduling performance</span></span>](project-scheduling-performance.md)
- [<span data-ttu-id="7545e-125">Szerepkörök beállítása a munkalebontási struktúra sablonjaihoz</span><span class="sxs-lookup"><span data-stu-id="7545e-125">Set up roles on Work breakdown structure templates</span></span>](set-up-roles-wbs-template.md)
- [<span data-ttu-id="7545e-126">Tervezett erőforrások erőforrás-teljesítése</span><span class="sxs-lookup"><span data-stu-id="7545e-126">Resource fulfillment for planned resources</span></span>](resource-fulfillment-planned-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]