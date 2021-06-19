---
title: Projekterőforrás ütemezési teljesítménye
description: Ez a témakör a nagy számú projektre vonatkozó erőforrás-ütemezési teljesítmény javításával kapcsolatban tartalmaz tájékoztatást.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010024"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="19499-103">Projekterőforrás ütemezési teljesítménye</span><span class="sxs-lookup"><span data-stu-id="19499-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="19499-104">Az erőforrás-ütemezéssel kapcsolatos teljesítményproblémák akkor fordulnak elő, ha a projektek száma eléri a több ezres értéket.</span><span class="sxs-lookup"><span data-stu-id="19499-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="19499-105">Az erőforrás-ütemezési teljesítmény javításához egy funkció érhető el, amely lehetővé teszi, hogy a felhasználók csökkentsék az erőforrás elérhetőségi űrlapjának indításához szükséges időt.</span><span class="sxs-lookup"><span data-stu-id="19499-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="19499-106">Ezzel eltávolítja az erőforrás-kapacitás összesítés-szinkronizálási folyamatát, és a **ResProjectResource** tábla használatával felgyorsítja az erőforrások keresését.</span><span class="sxs-lookup"><span data-stu-id="19499-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="19499-107">Ne feledje, hogy a **ResRollup** táblát a továbbiakban nem használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="19499-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19499-108">Ha az erőforrás-kapacitás összesítés-szinkronizálási folyamata vagy a **ResProjectResource** tábla függősége fennáll, ne használja ezt a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="19499-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="19499-109">Erőforrás-ütemezési teljesítmény fokozásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="19499-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="19499-110">Az erőforrás-ütemezés teljesítménynövelésének engedélyezéséhez hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="19499-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="19499-111">Lépjen a **Funkciókezelés** > **Összes** pontra, és a funkciók listájában keresse meg a **Projekterőforrás ütemezésiteljesítmény-növelési funkciójának engedélyezése** elemet.</span><span class="sxs-lookup"><span data-stu-id="19499-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="19499-112">Válassza ki az **Engedélyezés most** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="19499-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="19499-113">Ha nem találja a funkciót a listájában, akkor a lista frissítéséhez jelölje be a **Frissítések keresése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="19499-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="19499-114">Frissítse a böngészőt, majd nyissa meg a **projektmenedzsment és a könyvelés** > **időszakos** > **Projekterőforrások** > **Erőforrásnaptárak kapacitásának szinkronizálása az összes vállalatban**.</span><span class="sxs-lookup"><span data-stu-id="19499-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="19499-115">Állítsa a **Meglévő kapacitásrekordok eltávolítása** beállítást **Igen** értékre a korábbi adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="19499-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="19499-116">Ha növekményes adatokat szeretne létrehozni, akkor állítsa **Nem** értékre.</span><span class="sxs-lookup"><span data-stu-id="19499-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="19499-117">Az **Időszak kódja** mezőben válassza ki, hogy milyen időszakra kell létrehozni az adatot.</span><span class="sxs-lookup"><span data-stu-id="19499-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="19499-118">Ha kiválaszt egy időszakkódot, a kezdő és befejező dátumot nem kell meghatározni.</span><span class="sxs-lookup"><span data-stu-id="19499-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="19499-119">Ha üresen hagyja az **Időszak kódja** mezőt, akkor az adatok generálásához válassza ki a kezdési és a befejezési dátumot.</span><span class="sxs-lookup"><span data-stu-id="19499-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="19499-120">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="19499-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="19499-121">Ezzel az általános adatokat szétotsztja a **ResCalendarCapacity** táblába a környezet minden vállalatában, így a kötegelt feldolgozást csak egy jogi személyben kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="19499-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="19499-122">Az ebben a kötegelt feldolgozásban szereplő adatok szükségesek az erőforrás-kapacitásnak a hozzárendelt naptáron keresztüli kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="19499-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="19499-123">Nyissa meg a **projektmenedzsment és a könyvelés** > **időszakos** > **Projekterőforrások** > **Projekterőforrások kitöltése az összes vállalatban**, majd válassza az **OK** elemet.</span><span class="sxs-lookup"><span data-stu-id="19499-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="19499-124">Ez az adatfrissítési parancsfájl a **ResProjectResource** , a **ResCalendarDateTimeRange** és a **ResEffectiveDateTimeRange** tábláiban lévő általános adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="19499-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="19499-125">A **PSAPRojSchedRole.RootActivity** mező értékeit is frissíti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="19499-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="19499-126">Ha ez nem történik meg, akkor figyelmeztetés jelenik meg, amikor megpróbálja végrehajtani az erőforrás-ütemezési műveleteket.</span><span class="sxs-lookup"><span data-stu-id="19499-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="19499-127">Erőforrás-ütemezési teljesítmény fokozásának kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="19499-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="19499-128">Lépjen a **Funkciókezelés** > **Összes** pontra, és keresse meg a **Projekterőforrás ütemezésiteljesítmény-növelési funkciójának engedélyezése** elemet.</span><span class="sxs-lookup"><span data-stu-id="19499-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="19499-129">Jelölje ki a funkciót, majd válassza a **Letiltás** gombot.</span><span class="sxs-lookup"><span data-stu-id="19499-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="19499-130">Frissítse a böngészőjét.</span><span class="sxs-lookup"><span data-stu-id="19499-130">Refresh your browser.</span></span>
4. <span data-ttu-id="19499-131">Nyissa meg a **Projektmenedzsment és könyvelés** > **Időszakos** > **Kapacitás szinkronizálása** > **Erőforráskapacitás-összesítések szinkronizálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="19499-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="19499-132">A **kapacitás-összesítés szinkronizálása** lapon állítsa a **meglévő kapacitásrekordok eltávolítása** beállítást **Igen** értékre a korábbi adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="19499-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="19499-133">Ha növekményes adatokat szeretne létrehozni, akkor állítsa **Nem** értékre.</span><span class="sxs-lookup"><span data-stu-id="19499-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="19499-134">Az **Időszak kódja** mezőben válassza ki, hogy milyen időszakra kell létrehozni az adatot.</span><span class="sxs-lookup"><span data-stu-id="19499-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="19499-135">Ha kiválaszt egy időszakkódot, a kezdő és befejező dátumot nem kell meghatározni.</span><span class="sxs-lookup"><span data-stu-id="19499-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="19499-136">Ha üresen hagyja az **Időszak kódja** mezőt, akkor az adatok generálásához válassza ki a kezdési és a befejezési dátumot.</span><span class="sxs-lookup"><span data-stu-id="19499-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="19499-137">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="19499-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="19499-138">Ezzel az általános adatokat szétotsztja a **ResRollup** táblába a környezet minden vállalatában, így a kötegelt feldolgozást csak egy jogi személyben kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="19499-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="19499-139">Ez a kötegelt feldolgozás az összes **erőforrás-elérhetőségi** nézet esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="19499-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="19499-140">Ha a kötegelt feldolgozást nem futtatják le, akkor a **ResRollup**-adatok menet közben jönnek létre, ami időt vesz igénybe.</span><span class="sxs-lookup"><span data-stu-id="19499-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]