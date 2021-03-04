---
title: Újdonságok – 2021. február – Project Operations Lite központi telepítés
description: Ez a témakör információval szolgál a minőségi frissítésekről, amelyek a Project Operations Lite központi telepítés 2021 februári kiadásában váltak elérhetővé.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfc4c622c423e689938e58666ae47abbe3c23d48
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141320"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a><span data-ttu-id="c4002-103">Újdonságok – 2021. február – Project Operations Lite központi telepítés</span><span class="sxs-lookup"><span data-stu-id="c4002-103">What's new February 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="c4002-104">Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:</span><span class="sxs-lookup"><span data-stu-id="c4002-104">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="c4002-105">Project Operations a Dataverse-környezet 4.7.0.95 verzióján</span><span class="sxs-lookup"><span data-stu-id="c4002-105">Project Operations on Dataverse environment version 4.7.0.95</span></span>

## <a name="quality-updates"></a><span data-ttu-id="c4002-106">Minőségi frissítések</span><span class="sxs-lookup"><span data-stu-id="c4002-106">Quality updates</span></span>

| <span data-ttu-id="c4002-107">**Funkcióterület**</span><span class="sxs-lookup"><span data-stu-id="c4002-107">**Feature Area**</span></span> | <span data-ttu-id="c4002-108">**Hivatkozási szám**</span><span class="sxs-lookup"><span data-stu-id="c4002-108">**Reference number**</span></span> | <span data-ttu-id="c4002-109">**Minőségi frissítés**</span><span class="sxs-lookup"><span data-stu-id="c4002-109">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c4002-110">**Számlázás és árképzés**</span><span class="sxs-lookup"><span data-stu-id="c4002-110">**Billing and Pricing**</span></span> | <span data-ttu-id="c4002-111">2053736</span><span class="sxs-lookup"><span data-stu-id="c4002-111">2053736</span></span> | <span data-ttu-id="c4002-112">A számlasor részletei most már elérhetők a **Számla** > **Kapcsolódó információk** oldalon.</span><span class="sxs-lookup"><span data-stu-id="c4002-112">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="c4002-113">**Számlázás és árképzés**</span><span class="sxs-lookup"><span data-stu-id="c4002-113">**Billing and Pricing**</span></span> | <span data-ttu-id="c4002-114">2122613</span><span class="sxs-lookup"><span data-stu-id="c4002-114">2122613</span></span> | <span data-ttu-id="c4002-115">Az **Aktiválás** és **Inaktiválás** műveletek el vannak távolítva az **Árlista** társítási entitásokból.</span><span class="sxs-lookup"><span data-stu-id="c4002-115">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="c4002-116">**Számlázás és árképzés**</span><span class="sxs-lookup"><span data-stu-id="c4002-116">**Billing and Pricing**</span></span> | <span data-ttu-id="c4002-117">2128606</span><span class="sxs-lookup"><span data-stu-id="c4002-117">2128606</span></span> | <span data-ttu-id="c4002-118">A **GetEstimatesForProject** beépülő modulban megoldotta az **ullReferenceException** programmal kapcsolatos problémát.</span><span class="sxs-lookup"><span data-stu-id="c4002-118">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="c4002-119">**Központi telepítés és konfiguráció**</span><span class="sxs-lookup"><span data-stu-id="c4002-119">**Deployment and configuration**</span></span> | <span data-ttu-id="c4002-120">2140569</span><span class="sxs-lookup"><span data-stu-id="c4002-120">2140569</span></span> | <span data-ttu-id="c4002-121">Nem szabad telepíteni a Dataverse Teams környezetben a projektmegoldást.</span><span class="sxs-lookup"><span data-stu-id="c4002-121">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="c4002-122">**Központi telepítés és konfiguráció**</span><span class="sxs-lookup"><span data-stu-id="c4002-122">**Deployment and configuration**</span></span> | <span data-ttu-id="c4002-123">2086991</span><span class="sxs-lookup"><span data-stu-id="c4002-123">2086991</span></span> | <span data-ttu-id="c4002-124">A webes erőforrások korlátozott testreszabási lokalizációja.</span><span class="sxs-lookup"><span data-stu-id="c4002-124">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="c4002-125">**Lehetőségkezelés**</span><span class="sxs-lookup"><span data-stu-id="c4002-125">**Opportunity Management**</span></span> | <span data-ttu-id="c4002-126">2136794</span><span class="sxs-lookup"><span data-stu-id="c4002-126">2136794</span></span> | <span data-ttu-id="c4002-127">A megfelelő hibaüzenetet jeleníti meg, ha a **Számla megerősítése** vagy a **Számla megjelölése kifizetettként** folyamatok sikertelenek.</span><span class="sxs-lookup"><span data-stu-id="c4002-127">Display correct error message when **Confirm invoice** or **Mark invoice as paid** process fails,</span></span> |
| <span data-ttu-id="c4002-128">**Lehetőségkezelés**</span><span class="sxs-lookup"><span data-stu-id="c4002-128">**Opportunity Management**</span></span> | <span data-ttu-id="c4002-129">2146376</span><span class="sxs-lookup"><span data-stu-id="c4002-129">2146376</span></span> | <span data-ttu-id="c4002-130">A fel nem számítható tényadatok korrigált adóösszegét a számla visszaigazolásából hozzák létre.</span><span class="sxs-lookup"><span data-stu-id="c4002-130">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="c4002-131">**Projekttervezés és nyomon követés**</span><span class="sxs-lookup"><span data-stu-id="c4002-131">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c4002-132">2099879</span><span class="sxs-lookup"><span data-stu-id="c4002-132">2099879</span></span> | <span data-ttu-id="c4002-133">A Dataverse-környezet központi telepítésének létre kell hoznia egy statikus azonosítóval rendelkező alapértelmezett tranzakciókategóriát, és nem hozhat létre véletlenszerűen környezetenként egyet.</span><span class="sxs-lookup"><span data-stu-id="c4002-133">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="c4002-134">**Projekttervezés és nyomon követés**</span><span class="sxs-lookup"><span data-stu-id="c4002-134">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c4002-135">2128577</span><span class="sxs-lookup"><span data-stu-id="c4002-135">2128577</span></span> | <span data-ttu-id="c4002-136">Rögzítette a Project Service felhasználói jogosultságait, hogy frissítse a tranzakciókategóriát egy erőforrás-hozzárendelésen.</span><span class="sxs-lookup"><span data-stu-id="c4002-136">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="c4002-137">**Projekttervezés és nyomon követés**</span><span class="sxs-lookup"><span data-stu-id="c4002-137">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c4002-138">2164035</span><span class="sxs-lookup"><span data-stu-id="c4002-138">2164035</span></span> | <span data-ttu-id="c4002-139">Kijavította a **Projekt másolása** funkcióval kapcsolatos problémákat.</span><span class="sxs-lookup"><span data-stu-id="c4002-139">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="c4002-140">**Időbejegyzés**</span><span class="sxs-lookup"><span data-stu-id="c4002-140">**Time entry**</span></span> | <span data-ttu-id="c4002-141">2129161</span><span class="sxs-lookup"><span data-stu-id="c4002-141">2129161</span></span> | <span data-ttu-id="c4002-142">Szigorúbb korlátozások vonatkoznak annak biztosítására, hogy a felhasználók ne módosíthassák és ne frissíthessék a beküldött vagy jóváhagyott időbejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="c4002-142">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="c4002-143">**Időbejegyzés**</span><span class="sxs-lookup"><span data-stu-id="c4002-143">**Time entry**</span></span> | <span data-ttu-id="c4002-144">2103572</span><span class="sxs-lookup"><span data-stu-id="c4002-144">2103572</span></span> | <span data-ttu-id="c4002-145">A projekten kívüli időbejegyzések időjóváhagyása nem kereshet projektjóváhagyói szerepkört.</span><span class="sxs-lookup"><span data-stu-id="c4002-145">Time approval for non-project time entries must not be looking for project approver role.</span></span> |