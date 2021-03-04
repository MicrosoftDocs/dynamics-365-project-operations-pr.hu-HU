---
title: Költség áttekintése
description: Ez a témakör a Project Operations Költség funkciójával kapcsolatos információkat tartalmaz.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764912"
---
# <a name="expense-home-page"></a><span data-ttu-id="b80d2-103">Költség kezdőlap</span><span class="sxs-lookup"><span data-stu-id="b80d2-103">Expense home page</span></span>

<span data-ttu-id="b80d2-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="b80d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b80d2-105">A Dynamics 365 Project Operations támogatja a költségeket feldolgozó képességet.</span><span class="sxs-lookup"><span data-stu-id="b80d2-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="b80d2-106">A költségfeldolgozás a projektekkel vagy anélkül, házirendek, tranzakciós kategóriák és jóváhagyások testreszabható munkafolyamata használatával történik.</span><span class="sxs-lookup"><span data-stu-id="b80d2-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="b80d2-107">A Project Operationsben a Költség két támogatott telepítési modellje:</span><span class="sxs-lookup"><span data-stu-id="b80d2-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="b80d2-108">**Teljes**: A teljes telepítés elérhető a **Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén** illetve a **Project Operations termelésirendelés-alapú forgatókönyvek esetén** esetében.</span><span class="sxs-lookup"><span data-stu-id="b80d2-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="b80d2-109">**Alapszintű**: Az alapszintű telepítés elérhető az **Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén**, illetve a **Lite telepítés – ajánlattól proforma számlázásig** esetében.</span><span class="sxs-lookup"><span data-stu-id="b80d2-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="b80d2-110">Teljes</span><span class="sxs-lookup"><span data-stu-id="b80d2-110">Full</span></span> 
<span data-ttu-id="b80d2-111">A teljes költségű központi telepítés teljes körű irányelvérvényesítést biztosít, amely magában foglalja a szabályzatok létrehozására vonatkozó képességet, például:</span><span class="sxs-lookup"><span data-stu-id="b80d2-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="b80d2-112">Költségkategória-korlátok</span><span class="sxs-lookup"><span data-stu-id="b80d2-112">Expense category limits</span></span>
  - <span data-ttu-id="b80d2-113">Utazás</span><span class="sxs-lookup"><span data-stu-id="b80d2-113">Travel</span></span>
  - <span data-ttu-id="b80d2-114">Napidíj</span><span class="sxs-lookup"><span data-stu-id="b80d2-114">Per diem</span></span>
  - <span data-ttu-id="b80d2-115">Hitelkártya-importálások</span><span class="sxs-lookup"><span data-stu-id="b80d2-115">Credit card imports</span></span>
  - <span data-ttu-id="b80d2-116">Bizonylat optikai karakterfelismerése</span><span class="sxs-lookup"><span data-stu-id="b80d2-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="b80d2-117">Alap</span><span class="sxs-lookup"><span data-stu-id="b80d2-117">Basic</span></span> 
<span data-ttu-id="b80d2-118">A Költség alapszintű telepítési forgatókönyve csak az alapvető kiadások rögzítését teszi lehetővé a projektekhez.</span><span class="sxs-lookup"><span data-stu-id="b80d2-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="b80d2-119">További információkért lásd: [Költségbejegyzés (Lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="b80d2-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="b80d2-120">A Költség telepítési típusának meghatározása</span><span class="sxs-lookup"><span data-stu-id="b80d2-120">Determine your Expense deployment</span></span>
<span data-ttu-id="b80d2-121">Annak megállapításához, hogy az alapszintű költségkezelési telepítést futtatja-e, ellenőrizze, hogy a cím URL-címe a **.crm.dynamics.com** végződéssel rendelkezik-e.</span><span class="sxs-lookup"><span data-stu-id="b80d2-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
