---
title: Projekttámogatások
description: Ez a témakör elmagyarázza, hogyan hozhat létre és módosíthat egy támogatást.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289372"
---
# <a name="project-grants"></a><span data-ttu-id="1991f-103">Projekttámogatások</span><span class="sxs-lookup"><span data-stu-id="1991f-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1991f-104">A támogatás egy adott célra vagy projektre vonatkozó pénzajándék.</span><span class="sxs-lookup"><span data-stu-id="1991f-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="1991f-105">Általában vannak olyan korlátozások, amelyekkel a támogatás elkölthető.</span><span class="sxs-lookup"><span data-stu-id="1991f-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="1991f-106">A projektmenedzsment és a könyvelés során megadhatja és nyomon követheti a támogatásokat, és meghatározhatja a projektekre és a projektszerződésekre vonatkozó kapcsolatokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="1991f-107">Például az alábbi feladatokat elvégezheti:</span><span class="sxs-lookup"><span data-stu-id="1991f-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="1991f-108">A támogatások projektekkel és finanszírozási forrásokkal történő társítása a **projekt** és a **projekt szerződés részletei** oldalaira mutató hivatkozások segítségével.</span><span class="sxs-lookup"><span data-stu-id="1991f-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="1991f-109">Adja meg és kövesse nyomon a támogatás változásait, ahogy az egyik állapotból a másikba költözik.</span><span class="sxs-lookup"><span data-stu-id="1991f-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="1991f-110">Adja meg és kövesse nyomon a költségeket, a kért összegeket és a díjazott összegeket.</span><span class="sxs-lookup"><span data-stu-id="1991f-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="1991f-111">Hozzon létre fő támogatásokat, és társítson hozzájuk altámogatásokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="1991f-112">A támogatást létrehozhatja egy új rekord összes adatának megadásával, illetve a részletek átmásolásával egy meglévő támogatásból, majd frissítheti azokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="1991f-113">Új támogatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1991f-113">Create a new grant</span></span>

1. <span data-ttu-id="1991f-114">Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.</span><span class="sxs-lookup"><span data-stu-id="1991f-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="1991f-115">Válassza az **Új** \> **Támogatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1991f-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="1991f-116">A támogatás részletei lap **általános** gyorslapján, a **támogatási azonosító** mezőben adja meg a támogatás alfanumerikus azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="1991f-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="1991f-117">A **Támogatás neve** mezőben adjon egy egyedi nevet a támogatásnak.</span><span class="sxs-lookup"><span data-stu-id="1991f-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="1991f-118">A **Leírás** mezőben adja meg az új támogatás részleteit.</span><span class="sxs-lookup"><span data-stu-id="1991f-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="1991f-119">Az oldal többi mezőjének nagy része nem kötelezően kitöltendő, és a kívánt módon annyi adatot ad meg, amennyit szeretne.</span><span class="sxs-lookup"><span data-stu-id="1991f-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="1991f-120">A következő felsorolás a támogatási részletek oldal egyes gyorslapján megadott információkat ismerteti:</span><span class="sxs-lookup"><span data-stu-id="1991f-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="1991f-121">**Általános** – adja meg a támogatás nevét, az állapotot, a megnevezést, a célt és az összeget.</span><span class="sxs-lookup"><span data-stu-id="1991f-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="1991f-122">**Kapcsolatfelvételi adatok** – adja meg a munkatársakra vonatkozó adatokat, a támogatást kezelő részleget, valamint a támogatás ügyfél vagy a támogatás szervezeti forrását.</span><span class="sxs-lookup"><span data-stu-id="1991f-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="1991f-123">Azt is megadhatja, hogy a szervezet átadó entitás-e, amely megkapja a támogatást, majd átadja egy másik címzettnek.</span><span class="sxs-lookup"><span data-stu-id="1991f-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="1991f-124">Válassza a **Hozzáadás** lehetőséget a kapcsolattartói adatok (például telefonszámok és e-mail-címek) hozzáadásához a támogatást biztosító szervezet számára.</span><span class="sxs-lookup"><span data-stu-id="1991f-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="1991f-125">**Dátumok és határidők** – adja meg a támogatáshoz és a támogatási kérelemhez kapcsolódó időpontokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="1991f-126">A példák közé tartozik a pályázat határideje, a beküldési dátum, valamint a támogatás jóváhagyása vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="1991f-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="1991f-127">**Társított projektek és projektszerződések** – csak akkor adhat meg adatokat ezen a gyorslapon, ha az **Általános** gyorslapon a **támogatási állapot** mező **aktív** vagy **Díjazott** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="1991f-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="1991f-128">A kapcsolódó feladat végrehajtásához válasszon a következő lehetőségek közül:</span><span class="sxs-lookup"><span data-stu-id="1991f-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="1991f-129">**Finanszírozási forrás hozzáadása** – új finanszírozási forrás hozzáadása a támogatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1991f-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="1991f-130">Most megadhatja az összes adatot, vagy használhatja az alapértelmezett adatokat, majd később frissítheti.</span><span class="sxs-lookup"><span data-stu-id="1991f-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="1991f-131">**Projektszerződés hozzáadása** – projektszerződés adatainak hozzáadása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="1991f-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="1991f-132">**Projekt hozzáadása** – a projekt részleteinek hozzáadása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="1991f-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="1991f-133">**Beállítás** – adja meg a megfelelő alapok adatait, ha ez szükséges.</span><span class="sxs-lookup"><span data-stu-id="1991f-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="1991f-134">A támogatásokat odaítélő szervezetek közül sokak számára szükséges, hogy a támogatottak saját pénzük vagy erőforrásaik adott összegét költsék el, amely megfelel a támogatásban odaítélt összegnek.</span><span class="sxs-lookup"><span data-stu-id="1991f-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="1991f-135">A **helyi projekt- vagy követési azonosító** mezőben megadhat egy azonosítót, amely eltér a projekt azonosítójától.</span><span class="sxs-lookup"><span data-stu-id="1991f-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1991f-136">Ha a támogatás egy részét egy másik szervezetnek ítélik oda, akkor állítsa a **Résztámogató** értéket **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="1991f-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="1991f-137">Az Egyesült Államokban odaítélt támogatások esetében megadhatja, hogy a támogatást állami megbízás vagy szövetségi megbízás alapján ítélik-e oda.</span><span class="sxs-lookup"><span data-stu-id="1991f-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="1991f-138">**Lehívási adatok** – információ hozzáadása vagy frissítése arról, hogy milyen gyakran hívhatók le a támogatási pénzalapok, milyen gyakran számlázhatók vagy költhetők.</span><span class="sxs-lookup"><span data-stu-id="1991f-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="1991f-139">Új támogatás létrehozása másolatból</span><span class="sxs-lookup"><span data-stu-id="1991f-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="1991f-140">Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.</span><span class="sxs-lookup"><span data-stu-id="1991f-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="1991f-141">Válassza az **Új** \> **Másolat támogatásból** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1991f-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="1991f-142">Adja meg az új támogatás alfanumerikus azonosítóját és nevét, majd kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="1991f-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="1991f-143">A támogatás részletei lapon tekintse át a másolt támogatás részleteit, és végezze el a szükséges módosításokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="1991f-144">A lapon található mezők nagy része nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1991f-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="1991f-145">A támogatási adatok megtekintése vagy módosítása</span><span class="sxs-lookup"><span data-stu-id="1991f-145">View or modify grant details</span></span>

1. <span data-ttu-id="1991f-146">Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.</span><span class="sxs-lookup"><span data-stu-id="1991f-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="1991f-147">Válassza ki a módosítani kívánt támogatást.</span><span class="sxs-lookup"><span data-stu-id="1991f-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="1991f-148">A Műveleti ablaktáblán a **Támogatás** lapon, a **Karbantartás** csoportban válassza a **Szerkesztés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1991f-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="1991f-149">Tekintse át a támogatási adatokat, és végezze el a szükséges módosításokat.</span><span class="sxs-lookup"><span data-stu-id="1991f-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]