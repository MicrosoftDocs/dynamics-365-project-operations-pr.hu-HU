---
title: Költségkezelési munkafolyamat
description: Ez a témakör elmagyarázza, hogyan használható a Microsoft Dynamics 365 Finance munkafolyamatrendszere a költségjelentések felülvizsgálatának beállításához a Költségkezelésben.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960565"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="6a12b-103">Költségkezelési munkafolyamat</span><span class="sxs-lookup"><span data-stu-id="6a12b-103">Expense management workflow</span></span>

<span data-ttu-id="6a12b-104">A munkafolyamatrendszert használhatja a költségjelentések felülvizsgálatának beállításához a Költségkezelésben.</span><span class="sxs-lookup"><span data-stu-id="6a12b-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="6a12b-105">Beállíthat egy munkafolyamatot, amely a következő feltételeket használja a költségjelentés jóváhagyójának meghatározásához:</span><span class="sxs-lookup"><span data-stu-id="6a12b-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="6a12b-106">Az alkalmazottak beosztási hierarchiája és az előre meghatározott jóváhagyási korlátok</span><span class="sxs-lookup"><span data-stu-id="6a12b-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="6a12b-107">Többszintű jóváhagyás, amely támogatja az ideiglenes jóváhagyókat és a végső jóváhagyót</span><span class="sxs-lookup"><span data-stu-id="6a12b-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="6a12b-108">Pénzügyi dimenziók és a projekt felelősségvállalása</span><span class="sxs-lookup"><span data-stu-id="6a12b-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="6a12b-109">Adott felhasználókhoz vagy felhasználói csoportokhoz való hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="6a12b-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="6a12b-110">Munkafolyamat-jóváhagyások létrehozhatók költségjelentés, utazási igénylés, készpénzelőleg és forgalmi adó (ÁFA) helyreállításához.</span><span class="sxs-lookup"><span data-stu-id="6a12b-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="6a12b-111">**Példa**</span><span class="sxs-lookup"><span data-stu-id="6a12b-111">**Example**</span></span>

<span data-ttu-id="6a12b-112">A következő folyamat egy Költségjelentég költségkezelési munkafolyamatára mutat be példát.</span><span class="sxs-lookup"><span data-stu-id="6a12b-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="6a12b-113">Egy alkalmazott létrehoz és elment egy költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="6a12b-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="6a12b-114">Az alkalmazott beküldi költségjelentést jóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="6a12b-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="6a12b-115">A jóváhagyót a munkafolyamat beállításakor meghatározott szabályok alapján határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="6a12b-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="6a12b-116">A jóváhagyó értesítést kap, hogy a költségjelentés készen áll a jóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="6a12b-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="6a12b-117">A jóváhagyó felülvizsgálja a költségjelentést, és ellenőrzi, hogy teljesülnek-e az alábbi feltételek:</span><span class="sxs-lookup"><span data-stu-id="6a12b-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="6a12b-118">A kiadások nem ütköznem semmilyen költségszabályzatba.</span><span class="sxs-lookup"><span data-stu-id="6a12b-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="6a12b-119">Ha egy költség egy szabályzatba ütközik, a jóváhagyó ellenőrzi, hogy a költségjelentés tartalmaz-e érvényes üzleti indokolást.</span><span class="sxs-lookup"><span data-stu-id="6a12b-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="6a12b-120">A költségjelentésekhez elektronikus nyugták vannak csatolva.</span><span class="sxs-lookup"><span data-stu-id="6a12b-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="6a12b-121">A jóváhagyó jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="6a12b-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="6a12b-122">A költségjelentés a Kötelezettségek koordinátorához van rendelve feladás céljából.</span><span class="sxs-lookup"><span data-stu-id="6a12b-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="6a12b-123">A következő lépések egyike történik, attól függően, hogy az automatikus feladás be van-e állítva:</span><span class="sxs-lookup"><span data-stu-id="6a12b-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="6a12b-124">Ha az automatikus feladás be van állítva, a költségjelentés feldolgozása kifizetéshez megtörténik, és a költségjelentés állapota frissül.</span><span class="sxs-lookup"><span data-stu-id="6a12b-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="6a12b-125">Ha nincs konfigurálva az automatikus feladás, a Kötelezettségek koordinátora ellenőrzi, hogy az összes eredeti nyugtát beküldték-e, és hogy a nyugták összhangban vannak-e a költségjelentés költségeivel.</span><span class="sxs-lookup"><span data-stu-id="6a12b-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="6a12b-126">A költségjelentéshez megadott összes áfakódnak helyesnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6a12b-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="6a12b-127">A követelmények ellenőrzése után a költségjelentés feladása megtörténik.</span><span class="sxs-lookup"><span data-stu-id="6a12b-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="6a12b-128">A költségjelentés feladása után a költségjelentéshez tartozó kifizetés engedélyezve lesz, és az alkalmazott visszatérítést kap.</span><span class="sxs-lookup"><span data-stu-id="6a12b-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
