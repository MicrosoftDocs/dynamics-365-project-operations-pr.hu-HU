---
title: Több jóváhagyó egy költségjelentésen
description: Ez a témakör az olyan költségjelentésekről tartalmaz információkat, amelyeket több embernek kell jóváhagynia.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960610"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="f0d70-103">Több jóváhagyó egy költségjelentésen</span><span class="sxs-lookup"><span data-stu-id="f0d70-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="f0d70-104">A szervezet költség-jóváhagyási szabályzatától függően előfordulhat, hogy több személynek is jóvá kell hagynia egy munkavállaló által beküldött költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="f0d70-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="f0d70-105">Amikor beállítja a munkafolyamatot a költségjelentés jóváhagyásához, felvehet olyan munkafolyamat-elemeket, amelyek a költségjelentés egy vagy több jóváhagyójához tartozó feladatokat vagy lépéseket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="f0d70-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="f0d70-106">Előfordulhat például, hogy az összes költségjelentést először a jelentést elküldő alkalmazott vezetőjének majd a kötelezettségek koordinátorának kell jóváhagynia.</span><span class="sxs-lookup"><span data-stu-id="f0d70-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="f0d70-107">Ha úgy dönt, hogy a költségjelentést több személynek kell jóváhagynia, a következő módokon adhatja hozzá a munkafolyamat-elemeket:</span><span class="sxs-lookup"><span data-stu-id="f0d70-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="f0d70-108">Adjon hozzá egy jóváhagyási elemet, amely egyetlen lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="f0d70-108">Add one approval element that has one step.</span></span> <span data-ttu-id="f0d70-109">Előfordulhat például, hogy a lépéshez egy költségjelentést hozzá kell rendelni egy felhasználói csoporthoz, és hogy a felhasználói csoport tagjai felének jóvá kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="f0d70-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="f0d70-110">Adjon hozzá egy jóváhagyási elemet, amely több lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="f0d70-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="f0d70-111">A jóváhagyási elem például a következő lépésekből állhat:</span><span class="sxs-lookup"><span data-stu-id="f0d70-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="f0d70-112">A költségjelentést elküldő alkalmazott vezetője jóváhagyja.</span><span class="sxs-lookup"><span data-stu-id="f0d70-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="f0d70-113">A kötelezettségek adminisztrátora ellenőrzi a nyugtákat és a költségjelentés tételeit.</span><span class="sxs-lookup"><span data-stu-id="f0d70-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="f0d70-114">A költségvetés tulajdonosa jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="f0d70-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="f0d70-115">Több jóváhagyási elem hozzáadása, amelyek mindegyike egy lépésből áll.</span><span class="sxs-lookup"><span data-stu-id="f0d70-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="f0d70-116">Hozzáadhat például egy külön jóváhagyási elemet az egyes következő lépésekhez:</span><span class="sxs-lookup"><span data-stu-id="f0d70-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="f0d70-117">Az alkalmazott felettese jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="f0d70-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="f0d70-118">A költségvetés tulajdonosa jóváhagyja a költségjelentést.</span><span class="sxs-lookup"><span data-stu-id="f0d70-118">The budget owner approves the expense report.</span></span>
