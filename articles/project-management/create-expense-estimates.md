---
title: Költség becslések
description: Ez a témakör a projektalapú kiadások definiálásával vagy becslésével kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078014"
---
# <a name="expense-estimates"></a><span data-ttu-id="cfd74-103">Költség becslések</span><span class="sxs-lookup"><span data-stu-id="cfd74-103">Expense estimates</span></span>
<span data-ttu-id="cfd74-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="cfd74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cfd74-105">Az erőforrásalapú becslések meghatározásával együtt a Dynamics 365 Project Operations lehetővé teszi, hogy a projektmenedzserek az egyes projektek projektalapú kiadásait definiálják.</span><span class="sxs-lookup"><span data-stu-id="cfd74-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="cfd74-106">Minden egyes költségtétel hozzárendelhető egy adott projektfeladathoz vagy költségkategóriához.</span><span class="sxs-lookup"><span data-stu-id="cfd74-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="cfd74-107">A költségkategóriák általában szervezeti szinten vannak meghatározva.</span><span class="sxs-lookup"><span data-stu-id="cfd74-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="cfd74-108">Az egyes kiadások kategóriáinak árazását általában a következő hierarchia határozza meg:</span><span class="sxs-lookup"><span data-stu-id="cfd74-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="cfd74-109">Cég</span><span class="sxs-lookup"><span data-stu-id="cfd74-109">Organization</span></span>
- <span data-ttu-id="cfd74-110">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="cfd74-110">Customer</span></span>
- <span data-ttu-id="cfd74-111">Árajánlat/szerződés</span><span class="sxs-lookup"><span data-stu-id="cfd74-111">Quote/contract</span></span>

<span data-ttu-id="cfd74-112">Hajtsa végre a következő lépéseket a projektkiadások megtekintéséhez, hozzáadásához és törléséhez.</span><span class="sxs-lookup"><span data-stu-id="cfd74-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="cfd74-113">Nyissa meg a **Projektek** elemet, és jelölje ki a kezelni kívánt projektet.</span><span class="sxs-lookup"><span data-stu-id="cfd74-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="cfd74-114">Válassza ki a **Projektbecslések** lapot, és tekintse meg a projektek kiadásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="cfd74-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="cfd74-115">Kiadás hozzáadásához válassza az **Új kiadás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="cfd74-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="cfd74-116">Másik lehetőségként jelölje ki a törlendő kiadást, majd válassza a **Kiadás törlése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="cfd74-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="cfd74-117">Minden egyes költségsori tételhez a következő attribútumok vannak definiálva:</span><span class="sxs-lookup"><span data-stu-id="cfd74-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="cfd74-118">**Kategória** : A projekttel kapcsolatban felmerült összes kiadás leírására szolgáló közös csoportosítások.</span><span class="sxs-lookup"><span data-stu-id="cfd74-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="cfd74-119">**Kezdő dátum** : A kiadás várható felmerülésének dátuma.</span><span class="sxs-lookup"><span data-stu-id="cfd74-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="cfd74-120">**Mennyiség** : Egy adott kategóriához tartozó kiadási tételek becsült száma.</span><span class="sxs-lookup"><span data-stu-id="cfd74-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="cfd74-121">**Egység önköltségi ára** : A kiadás költségének kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="cfd74-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="cfd74-122">**Egység értékesítési ára** : A kiadás értékesítési árának kiszámításához használt egységár.</span><span class="sxs-lookup"><span data-stu-id="cfd74-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

