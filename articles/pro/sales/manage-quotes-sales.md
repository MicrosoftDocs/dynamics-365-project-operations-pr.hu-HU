---
title: Projektárajánlatok kezelése
description: Ez a témakör információkat nyújt a projektárajánlatokról.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272931"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="47959-103">Projektárajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="47959-103">Manage project quotes</span></span>

<span data-ttu-id="47959-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="47959-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47959-105">A Dynamics 365 Project Operations a projektárajánlatok segítséget nyújtanak a projekt munkára vonatkozó ajánlatok kialakításában.</span><span class="sxs-lookup"><span data-stu-id="47959-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="47959-106">A projektárajánlat szerkezete a Project Operationsban a következő összetevőkkel épül fel a projektjavaslatokhoz:</span><span class="sxs-lookup"><span data-stu-id="47959-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="47959-107">Árajánlatsorok, amelyek beazonosítják a magas szintű összetevőként megjelenített különálló munkaösszetevőket.</span><span class="sxs-lookup"><span data-stu-id="47959-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="47959-108">Árajánlatsor-adatok, amelyek meghatározzák és megbecsülik az egyes magas szintű összetevőkhöz vagy árajánlatsorhoz szükséges munkát.</span><span class="sxs-lookup"><span data-stu-id="47959-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="47959-109">Az ütemezés vagy a dátumbecslések, valamint a munka pénzügyi aspektusai az adott árajánlatsorhoz köthetők.</span><span class="sxs-lookup"><span data-stu-id="47959-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="47959-110">Az egyes árajánlatosorokhoz szerződésközési modellek és számlázható összetevők vannak beállítva.</span><span class="sxs-lookup"><span data-stu-id="47959-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="47959-111">Ez a beállítás segít a bevétel, a kiadások és a jövedelmezőség elterjedésének becslésében az egyes árajánlati sorokhoz és az általános árajánlathoz.</span><span class="sxs-lookup"><span data-stu-id="47959-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="47959-112">Összes projektalapú árajánlat megtekintése</span><span class="sxs-lookup"><span data-stu-id="47959-112">View all project-based quotes</span></span>

<span data-ttu-id="47959-113">A projektárajánlatok listája az **Árajánlatok** listaoldalon látható.</span><span class="sxs-lookup"><span data-stu-id="47959-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="47959-114">Válassza az **Értékesítés** > **Ajánlatok** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="47959-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="47959-115">Itt a rendszerben található összes projektárajánlat listája megjelenik.</span><span class="sxs-lookup"><span data-stu-id="47959-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="47959-116">A **Nézetváltó** segítségével már szűrt nézeteket is kiválaszthat az árajánlatokhoz.</span><span class="sxs-lookup"><span data-stu-id="47959-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="47959-117">Az egyéni szűrőfeltételek használatával saját nézeteket és navigációs beállításokat állíthat be.</span><span class="sxs-lookup"><span data-stu-id="47959-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="47959-118">Árajánlatokat lehet létrehozni vagy törölni ebből a listából vagy részletes oldalakról.</span><span class="sxs-lookup"><span data-stu-id="47959-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]