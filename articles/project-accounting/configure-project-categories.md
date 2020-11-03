---
title: Projektkategóriák konfigurálása
description: Ez a témakör információkat nyújt a projektkategóriák beállításáról.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077988"
---
# <a name="configure-project-categories"></a><span data-ttu-id="ece9b-103">Projektkategóriák konfigurálása</span><span class="sxs-lookup"><span data-stu-id="ece9b-103">Configure project categories</span></span>

<span data-ttu-id="ece9b-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="ece9b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ece9b-105">A Project Operations megbízható lehetőségeket biztosít a projektek bevételeinek és kiadásainak kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="ece9b-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="ece9b-106">A kategóriák lehetőséget nyújtanak a projekttranzakciók jelentésére és elemzésére, valamint a főkönyvbe való beküldésre.</span><span class="sxs-lookup"><span data-stu-id="ece9b-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="ece9b-107">A következő ábra a tranzakciók kategóriái, a megosztott kategóriák és a projektkategóriák közötti korrelációt szemlélteti.</span><span class="sxs-lookup"><span data-stu-id="ece9b-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="ece9b-108">A tranzakciós kategóriák a projekttranzakciók alapvető csoportosítása.</span><span class="sxs-lookup"><span data-stu-id="ece9b-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="ece9b-109">Az adott csoportosításon belül van egy sor megosztott kategória, amelyek az alkalmazások és modulok között megoszthatók.</span><span class="sxs-lookup"><span data-stu-id="ece9b-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="ece9b-110">Részletesebben vizsgálva a projektkategóriák a legrészletesebb szintű kategóriák.</span><span class="sxs-lookup"><span data-stu-id="ece9b-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="ece9b-111">A projektkategóriák a jogi entitásra, a modulra és az alkalmazásra vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="ece9b-111">Project categories are specific to legal entity, module, and application.</span></span>

![A tranzakciók kategóriái, a megosztott kategóriák és a projektkategóriák közötti korreláció](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="ece9b-113">Tranzakciókategóriák</span><span class="sxs-lookup"><span data-stu-id="ece9b-113">Transaction categories</span></span>

<span data-ttu-id="ece9b-114">A tranzakciós kategóriák a projekttranzakciók alapvető csoportosítását jelentik, és nem vállalat- vagy tranzakciótípus-specifikusak.</span><span class="sxs-lookup"><span data-stu-id="ece9b-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="ece9b-115">A Contoso Robotics például tervezési, utazási, telepítési és szolgáltatási tranzakciós kategóriákat használ a projekttranzakciók csoportosításához.</span><span class="sxs-lookup"><span data-stu-id="ece9b-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="ece9b-116">A tranzakciós kategóriákat a Project Operations modul definiálja.</span><span class="sxs-lookup"><span data-stu-id="ece9b-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="ece9b-117">Az űrlap megnyitásához lépjen a **Beállítások** \> **Tranzakciós kategóriák** menüpontra.</span><span class="sxs-lookup"><span data-stu-id="ece9b-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="ece9b-118">Hozzon létre új tranzakciós kategóriát akár az **Új** lehetőség választásával, vagy az **Importálás az Excelből** kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="ece9b-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="ece9b-119">Megosztott kategóriák</span><span class="sxs-lookup"><span data-stu-id="ece9b-119">Shared categories</span></span>

<span data-ttu-id="ece9b-120">A Dynamics 365 a megosztott kategóriák koncepciója segítségével kategorizálja a különböző alkalmazások, például a Dynamics 365 Finance, Dynamics 365 Supply Chain és a Dynamics 365 Project Operations kiadásait.</span><span class="sxs-lookup"><span data-stu-id="ece9b-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="ece9b-121">Minden létrehozott tranzakciós kategória esetében a Project Operations automatikusan négy kapcsolódó megosztott kategóriát hoz létre: az órákat, a költségeket, a díjakat és a cikkeket.</span><span class="sxs-lookup"><span data-stu-id="ece9b-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="ece9b-122">A megosztott kategóriákat áttekintheti és módosíthatja, ha a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Megosztott kategóriák** menüpontra lép.</span><span class="sxs-lookup"><span data-stu-id="ece9b-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="ece9b-123">Projektkategóriák</span><span class="sxs-lookup"><span data-stu-id="ece9b-123">Project categories</span></span>

<span data-ttu-id="ece9b-124">A projektkategóriák a kategória konfigurációjának legrészletesebb szintjét jelentik, és ezeket külön kell konfigurálni mindegyik vállalatnál egy projektkönyvelőnek.</span><span class="sxs-lookup"><span data-stu-id="ece9b-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="ece9b-125">Nyissa meg a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Projektkategóriák** menüpontot.</span><span class="sxs-lookup"><span data-stu-id="ece9b-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="ece9b-126">Válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ece9b-126">Select **New**.</span></span>
3. <span data-ttu-id="ece9b-127">Válassza ki az előző szakaszban létrehozott megosztott kategória **Kategóriaazonosító** elemét.</span><span class="sxs-lookup"><span data-stu-id="ece9b-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="ece9b-128">A Project Operations csak azoknak a megosztott kategóriáknak a használatát engedélyezi, amelyek tranzakciós kategóriákhoz vannak társítva.</span><span class="sxs-lookup"><span data-stu-id="ece9b-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="ece9b-129">Válasszon kategóriacsoportot.</span><span class="sxs-lookup"><span data-stu-id="ece9b-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="ece9b-130">Kategóriacsoportok</span><span class="sxs-lookup"><span data-stu-id="ece9b-130">Category groups</span></span>

<span data-ttu-id="ece9b-131">A kategóriacsoportok segítségével megoszthatók a tulajdonságok, elsősorban a feladási profilok a kapcsolódó projektkategóriák között.</span><span class="sxs-lookup"><span data-stu-id="ece9b-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="ece9b-132">Az egyes tranzakciótípusok mindegyikéhez legalább egy kategóriacsoport szükséges, és minden egyes projektkategóriához egy csoport tartozik.</span><span class="sxs-lookup"><span data-stu-id="ece9b-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="ece9b-133">A Project Operationsben szereplő könyvelési előírásokat a projekt költség- és bevételi profiljának szabályai, a projektkategóriák és a kategóriacsoportok határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="ece9b-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="ece9b-134">A kategóriacsoportok a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Kategóriacsoportok** segítségével állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="ece9b-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
