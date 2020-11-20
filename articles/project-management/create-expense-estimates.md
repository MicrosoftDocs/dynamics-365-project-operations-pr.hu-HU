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
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131706"
---
# <a name="expense-estimates"></a><span data-ttu-id="c2fd9-103">Költség becslések</span><span class="sxs-lookup"><span data-stu-id="c2fd9-103">Expense estimates</span></span>
<span data-ttu-id="c2fd9-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c2fd9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2fd9-105">Az erőforrásalapú becslések meghatározásával együtt a Dynamics 365 Project Operations lehetővé teszi, hogy a projektmenedzserek az egyes projektek projektalapú kiadásait definiálják.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="c2fd9-106">Minden egyes költségtétel hozzárendelhető egy adott projektfeladathoz vagy költségkategóriához.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="c2fd9-107">A költségkategóriák általában szervezeti szinten vannak meghatározva.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="c2fd9-108">Az egyes kiadások kategóriáinak árazását általában a következő hierarchia határozza meg:</span><span class="sxs-lookup"><span data-stu-id="c2fd9-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="c2fd9-109">Cég</span><span class="sxs-lookup"><span data-stu-id="c2fd9-109">Organization</span></span>
- <span data-ttu-id="c2fd9-110">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="c2fd9-110">Customer</span></span>
- <span data-ttu-id="c2fd9-111">Árajánlat/szerződés</span><span class="sxs-lookup"><span data-stu-id="c2fd9-111">Quote/contract</span></span>

<span data-ttu-id="c2fd9-112">Hajtsa végre a következő lépéseket a projektkiadások megtekintéséhez, hozzáadásához és törléséhez.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="c2fd9-113">Nyissa meg a **Projektek** elemet, és jelölje ki a kezelni kívánt projektet.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="c2fd9-114">Válassza ki a **Projektbecslések** lapot, és tekintse meg a projektek kiadásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="c2fd9-115">Kiadás hozzáadásához válassza az **Új kiadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="c2fd9-116">Másik lehetőségként jelölje ki a törlendő kiadást, majd válassza a **Kiadás törlése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="c2fd9-117">Minden egyes költségsori tételhez a következő attribútumok vannak definiálva:</span><span class="sxs-lookup"><span data-stu-id="c2fd9-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="c2fd9-118">**Kategória**: A projekttel kapcsolatban felmerült összes kiadás leírására szolgáló közös csoportosítások.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="c2fd9-119">**Kezdő dátum**: A kiadás várható felmerülésének dátuma.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="c2fd9-120">**Mennyiség**: Egy adott kategóriához tartozó kiadási tételek becsült száma.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="c2fd9-121">**Egység önköltségi ára**: A kiadás költségének kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="c2fd9-122">**Egység értékesítési ára**: A kiadás értékesítési árának kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

