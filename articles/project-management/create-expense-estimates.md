---
title: Költség becslések
description: Ez a témakör a projektalapú kiadások definiálásával vagy becslésével kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287061"
---
# <a name="expense-estimates"></a><span data-ttu-id="d6cf8-103">Költség becslések</span><span class="sxs-lookup"><span data-stu-id="d6cf8-103">Expense estimates</span></span>
<span data-ttu-id="d6cf8-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d6cf8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6cf8-105">Az erőforrás-alapú becslésekkel együtt a projektmenedzserek a Dynamics 365 Project Operations alkalmazásnak köszönhetően meghatároznak projektalapú költségeket mindegyik projekthez.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="d6cf8-106">Minden egyes költségtétel hozzárendelhető egy adott projektfeladathoz vagy költségkategóriához.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="d6cf8-107">A költségkategóriák általában szervezeti szinten vannak meghatározva.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="d6cf8-108">Az egyes kiadások kategóriáinak árazását általában a következő hierarchia határozza meg:</span><span class="sxs-lookup"><span data-stu-id="d6cf8-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="d6cf8-109">Cég</span><span class="sxs-lookup"><span data-stu-id="d6cf8-109">Organization</span></span>
- <span data-ttu-id="d6cf8-110">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="d6cf8-110">Customer</span></span>
- <span data-ttu-id="d6cf8-111">Árajánlat/szerződés</span><span class="sxs-lookup"><span data-stu-id="d6cf8-111">Quote/contract</span></span>

<span data-ttu-id="d6cf8-112">Hajtsa végre a következő lépéseket a projektkiadások megtekintéséhez, hozzáadásához és törléséhez.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="d6cf8-113">Nyissa meg a **Projektek** elemet, és jelölje ki a kezelni kívánt projektet.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="d6cf8-114">Válassza ki a **Projektbecslések** lapot, és tekintse meg a projektek kiadásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="d6cf8-115">Kiadás hozzáadásához válassza az **Új kiadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="d6cf8-116">Másik lehetőségként jelölje ki a törlendő kiadást, majd válassza a **Kiadás törlése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="d6cf8-117">Minden egyes költségsori tételhez a következő attribútumok vannak definiálva:</span><span class="sxs-lookup"><span data-stu-id="d6cf8-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="d6cf8-118">**Kategória**: A projekttel kapcsolatban felmerült összes kiadás leírására szolgáló közös csoportosítások.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="d6cf8-119">**Kezdő dátum**: A kiadás várható felmerülésének dátuma.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="d6cf8-120">**Mennyiség**: Egy adott kategóriához tartozó kiadási tételek becsült száma.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="d6cf8-121">**Egység önköltségi ára**: A kiadás költségének kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="d6cf8-122">**Egység értékesítési ára**: A kiadás értékesítési árának kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="d6cf8-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]