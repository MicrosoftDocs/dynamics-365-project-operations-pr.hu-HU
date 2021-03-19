---
title: Projektszerződések kezelése
description: Ez a témakör információkat nyújt a projektalapú szerződéssorok megtekintéséről.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273202"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="c52a6-103">Projektszerződések kezelése</span><span class="sxs-lookup"><span data-stu-id="c52a6-103">Manage project contracts</span></span>

<span data-ttu-id="c52a6-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c52a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c52a6-105">Project szerződések a Dynamics 365 Project Operations alkalmazásban rögzítik és kezelik a projektek szerződéses megállapodásait és számlázási adatait.</span><span class="sxs-lookup"><span data-stu-id="c52a6-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="c52a6-106">A projektszerződés szerkezete a Project Operations alkalmazásban a következő összetevőkkel épül fel a projektalapú munkához:</span><span class="sxs-lookup"><span data-stu-id="c52a6-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="c52a6-107">Szerződéssorok, amelyek beazonosítják a projektszámlán magas szintű összetevőként megjelenített különálló munkaösszetevőket.</span><span class="sxs-lookup"><span data-stu-id="c52a6-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="c52a6-108">Szerződéssoradatok, amelyek meghatározzák és megbecsülik az egyes magas szintű összetevőkhöz vagy szerződéssorhoz szükséges munkát.</span><span class="sxs-lookup"><span data-stu-id="c52a6-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="c52a6-109">A becslés tartalmazza az ütemezést, valamint, a szerződéssorhoz kapcsolt munka pénzügyi aspektusait.</span><span class="sxs-lookup"><span data-stu-id="c52a6-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="c52a6-110">Minden egyes szerződéssor esetében, amely számlázási megállapodást tartalmaz az egyes szerződéssorokhoz és a teljes szerződéshez meg kell adni a szerződési modelleket és számlázható komponenseket.</span><span class="sxs-lookup"><span data-stu-id="c52a6-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="c52a6-111">Az összes projektalapú szerződés megtekintése</span><span class="sxs-lookup"><span data-stu-id="c52a6-111">View all project-based contracts</span></span>

<span data-ttu-id="c52a6-112">A projektszerződések listája a **Szerződések** listaoldalon látható.</span><span class="sxs-lookup"><span data-stu-id="c52a6-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="c52a6-113">Válassza a **Értékesítés** > **Szerződések** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c52a6-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="c52a6-114">Itt a rendszerben található összes projektszerződés listája megjelenik.</span><span class="sxs-lookup"><span data-stu-id="c52a6-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="c52a6-115">A többi szűrt nézet kiválasztásához válassza a **Nézetváltót** (a nézet neve melletti legördülő nyilat).</span><span class="sxs-lookup"><span data-stu-id="c52a6-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="c52a6-116">Saját nézetet hozhat létre egyéni szűrési feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="c52a6-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="c52a6-117">Szerződéseket lehet létrehozni vagy törölni ebből a listából vagy részletes oldalakról.</span><span class="sxs-lookup"><span data-stu-id="c52a6-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]