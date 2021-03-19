---
title: Projekt becslésének eltávolítása
description: Ez a témakör a projektbecslés eltávolításával kapcsolatosan tartalmaz információkat, miután az elkészült.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270681"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="0081d-103">Projekt becslésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0081d-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0081d-104">A projektbecslések biztosítják a becsült és a projekthez ütemezett munka pénzügyi áttekintését.</span><span class="sxs-lookup"><span data-stu-id="0081d-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="0081d-105">A projektek becsült értékének megadásához a projektet egy becsült projekthez kell csatolnia.</span><span class="sxs-lookup"><span data-stu-id="0081d-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="0081d-106">A becsült projektek mindig egy meglévő projekten alapulnak, de több projekt is hivatkozhat egyetlen becsült projektre.</span><span class="sxs-lookup"><span data-stu-id="0081d-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="0081d-107">Csak a rögzített árú és a beruházási projektek csatolhatók a becsült projektekhez, és a projekteknek ugyanahhoz a csoporthoz kell tartozniuk, mint a becsült projektnek.</span><span class="sxs-lookup"><span data-stu-id="0081d-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="0081d-108">A becsült projekt megszüntetéséhez annak teljesnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0081d-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="0081d-109">A következő lépésekből megtudhatja, hogyan lehet megszüntetni a becsléseket.</span><span class="sxs-lookup"><span data-stu-id="0081d-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="0081d-110">Lépjen a **Projektvezetés és könyvelés** > **Minden projekt** elemre, és nyissa meg a projektet.</span><span class="sxs-lookup"><span data-stu-id="0081d-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="0081d-111">A **Kezelés** lapon jelölje ki a **Becslések** elemet, majd a **Becslés** lapon válassza az **Eltávolítás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0081d-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="0081d-112">A **Becslés eltávolítása** lap **Általános** fülén adja meg a következő beállításokat:</span><span class="sxs-lookup"><span data-stu-id="0081d-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="0081d-113">**Időszak kódja** : Válassza ki az időszak kódját a megfelelő becsült projektek kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="0081d-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="0081d-114">**Becslés dátuma**: Válassza ki a megfelelő becslési dátumot az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="0081d-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="0081d-115">**Eltávolítás folyamatban lévő munka figyelmeztetésekkel**: Engedélyezze ezt a beállítást, ha értesítést szeretne kapni, amikor egy folyamatban lévő munkához kapcsolódó becslés el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="0081d-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="0081d-116">Ha a beállítás nincs engedélyezve, akkor az eltávolítás nem folytatható, ha nem becsült tranzakciók léteznek.</span><span class="sxs-lookup"><span data-stu-id="0081d-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="0081d-117">Ez a beállítás csak akkor érhető el, ha az eltávolítást egy becsült projektre alkalmazza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0081d-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="0081d-118">Periodikus feladás használata esetén nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="0081d-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="0081d-119">Ez a beállítás a **Projekt paraméterei** lap **Becslés** lapjának beállításaival működik az **Eltávolítás engedélyezése, ha nem becsült tranzakciók léteznek** mezőcsoportban.</span><span class="sxs-lookup"><span data-stu-id="0081d-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="0081d-120">**Fázis beállítása befejezettre**: Engedélyezze ezt a beállítást, ha az eltávolítás futtatása után a becsült projekt fázisát **Befejezett** értékre szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="0081d-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="0081d-121">**Becslési listák nyomtatása**: Válassza ki, hogy milyen adatok szerepeljenek a becslési listák kinyomtatásakor.</span><span class="sxs-lookup"><span data-stu-id="0081d-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="0081d-122">**Információs napló megjelenítése**: Engedélyezze ezt a beállítást az információs napló megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0081d-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="0081d-123">**Könyvelési dátum**: Válassza ki a becslés főkönyvi feladási dátumát.</span><span class="sxs-lookup"><span data-stu-id="0081d-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="0081d-124">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="0081d-124">Select **OK**.</span></span>
5. <span data-ttu-id="0081d-125">Az eltávolítási folyamat befejeződése után a megszüntetett becsült projekt negatív értékkel jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0081d-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="0081d-126">Ha nem kívánja eltávolítani a becslést, akkor kiválaszthatja az eltávolított becslést, és kiválaszthatja az **Eltávolítás visszaállítása** elemet.</span><span class="sxs-lookup"><span data-stu-id="0081d-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]