---
title: Költségjelentések és több jóváhagyó
description: Ez a témakör az olyan költségjelentésekről tartalmaz információkat, amelyeket több személynek kell jóváhagynia.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120996"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d690b-103">Költségjelentések és több jóváhagyó</span><span class="sxs-lookup"><span data-stu-id="d690b-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="d690b-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d690b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d690b-105">A szervezet költség-jóváhagyási szabályzatától függően előfordulhat, hogy több személynek is jóvá kell hagynia egy elküldött költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="d690b-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="d690b-106">Amikor beállítja a munkafolyamatot a költségjelentés jóváhagyásához, felvehet olyan munkafolyamat-elemeket, amelyek a költségjelentés egy vagy több jóváhagyójához tartozó feladatokat vagy lépéseket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="d690b-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d690b-107">Előfordulhat például, hogy az összes költségjelentést két külön személynem kell jóváhagynia: a jelentést elküldő alkalmazott vezetőjének és a kötelezettségek koordinátorának.</span><span class="sxs-lookup"><span data-stu-id="d690b-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="d690b-108">Ha úgy dönt, hogy a költségjelentést több személynek kell jóváhagynia, a következő módokon adhatja hozzá a munkafolyamat-elemeket:</span><span class="sxs-lookup"><span data-stu-id="d690b-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d690b-109">Adjon hozzá egy jóváhagyási elemet, amely egyetlen lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="d690b-109">Add one approval element that has one step.</span></span> <span data-ttu-id="d690b-110">Előfordulhat például, hogy a lépéshez egy költségjelentést hozzá kell rendelni egy felhasználói csoporthoz, és hogy a felhasználói csoport tagjai felének jóvá kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="d690b-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d690b-111">Adjon hozzá egy jóváhagyási elemet, amely több lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="d690b-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d690b-112">A jóváhagyási elem például a következő lépésekből állhat:</span><span class="sxs-lookup"><span data-stu-id="d690b-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d690b-113">A költségjelentést elküldő alkalmazott vezetője jóváhagyja.</span><span class="sxs-lookup"><span data-stu-id="d690b-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d690b-114">A kötelezettségek adminisztrátora ellenőrzi a nyugtákat és a költségjelentés tételeit.</span><span class="sxs-lookup"><span data-stu-id="d690b-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d690b-115">A költségvetés tulajdonosa jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="d690b-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d690b-116">Több jóváhagyási elem hozzáadása, amelyek mindegyike egy lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="d690b-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d690b-117">Hozzáadhat például egy külön jóváhagyási elemet az egyes következő lépésekhez:</span><span class="sxs-lookup"><span data-stu-id="d690b-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d690b-118">Az alkalmazott felettese jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="d690b-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d690b-119">A költségvetés tulajdonosa jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="d690b-119">The budget owner approves the expense report.</span></span>
