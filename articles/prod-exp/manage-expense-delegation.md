---
title: Költségdelegálás kezelése
description: A költségdelegált felhasználó a szervezet egy másik alkalmazottja nevében hozhat létre és kezelhet költségjelentéskat.
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2ce1d1cf35745ef4372258e07fd4d2b108ed4827
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078244"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="0fd73-103">Költségdelegálás kezelése</span><span class="sxs-lookup"><span data-stu-id="0fd73-103">Manage expense delegation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fd73-104">A költségdelegált felhasználó a szervezet egy másik alkalmazottja nevében hozhat létre és kezelhet költségjelentéskat.</span><span class="sxs-lookup"><span data-stu-id="0fd73-104">An expense delegate user can create and manage expense reports on behalf of another employee in the organization.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="0fd73-105">Költségdelegálás konfigurálása</span><span class="sxs-lookup"><span data-stu-id="0fd73-105">Configuring expense delegation</span></span>

<span data-ttu-id="0fd73-106">A felhasználó költségdelegáltként való beállításához nyissa meg a **Költségkezelés > Beállítás > Általános > Delegáltak** pontot a **Delegáltak** oldal megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="0fd73-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates** to open the **Delegates** page.</span></span> <span data-ttu-id="0fd73-107">Válassza az **Új** elemet, majd jelölje ki azt az alkalmazottat, akinek delegáltat kíván megadni.</span><span class="sxs-lookup"><span data-stu-id="0fd73-107">Select **New** and then select the employee that will have a delegate defined.</span></span> <span data-ttu-id="0fd73-108">Adja meg a delegált felhasználó aliasát, valamint a delegálási időszak kezdő és záró dátumát.</span><span class="sxs-lookup"><span data-stu-id="0fd73-108">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a><span data-ttu-id="0fd73-109">Költségdelegálás kezelése egy másik alkalmazott nevében</span><span class="sxs-lookup"><span data-stu-id="0fd73-109">Managing expense delegation on behalf of another employee</span></span>

<span data-ttu-id="0fd73-110">Ha a **Költségdelegáltak listaoldal engedélyezése** funkciókezelési kulcs engedélyezve van, akkor elérhetővé válik a **Hozzám delegált költségek** listaoldal a **Költségkezelés > Saját költségek > Hozzám delegált költségek** lapról.</span><span class="sxs-lookup"><span data-stu-id="0fd73-110">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available by navigating to **Expense management > My expenses > Expenses delegated to me**.</span></span>

<span data-ttu-id="0fd73-111">A delegált felhasználó gyorsan szűrheti és keresheti a felhasználóhoz delegált meglévő költségjelentéseket.</span><span class="sxs-lookup"><span data-stu-id="0fd73-111">A delegate user can quickly filter and search on existing expense reports that hae been delegated to the user.</span></span> <span data-ttu-id="0fd73-112">A felhasználó új költségjelentést is gyorsan létrehozhat más felhasználók nevében az **Új költségjelentés** lehetőség kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="0fd73-112">The user can also quickly create a new expense report on behalf of other users by clicking **New expense report**.</span></span>

<span data-ttu-id="0fd73-113">A delegált felhasználók létrehozhatnak és kezelhetnek költségjelentéseket más alkalmazottak nevében is a **Költségkezelés > Saját költségek > Költségjelentések** rész megnyitásával, majd a **Más felhasználó költségeinek megnyitása** gomb választásával.</span><span class="sxs-lookup"><span data-stu-id="0fd73-113">Delegate users can also create and manage expense reports on behalf of other employees by navigating to **Expense management > My expenses > Expense reports** and clicking the **Open other user's expenses** button.</span></span>
