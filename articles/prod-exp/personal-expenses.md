---
title: Személyes kiadások egy költségjelentésen
description: Ez a témakör ismerteti, hogyan lehet kezelni a dolgozók személyes kiadásait a Microsoft Dynamics 365 Finance szolgáltatásban.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf6bfc714751fa64914e684f67d37552b2df162e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271401"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="c43d8-103">Személyes kiadások egy költségjelentésen</span><span class="sxs-lookup"><span data-stu-id="c43d8-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="c43d8-104">Az üzleti utazás során a dolgozók néha személyes kiadásokat is terhelhetnek a vállalati hitelkártyákra.</span><span class="sxs-lookup"><span data-stu-id="c43d8-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="c43d8-105">Ha nem határoz meg a személyes kiadások kezelésére szolgáló folyamatot, akkor előfordulhat, hogy a költségjelentés jóváhagyási folyamata megszakad, amikor a munkavállalók elküldik a részletezett Költségjelentéseket.</span><span class="sxs-lookup"><span data-stu-id="c43d8-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="c43d8-106">A dolgozók személyes költségeinek kezeléséhez két módszer áll rendelkezésre:</span><span class="sxs-lookup"><span data-stu-id="c43d8-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="c43d8-107">**Alkalmazott által fizetendő** - A szervezet nem fizeti ki a személyes költségeket, amelyek megjelennek a vállalati hitelkártya számláján.</span><span class="sxs-lookup"><span data-stu-id="c43d8-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="c43d8-108">Ehelyett létrehoz egy jelentést, amely megjeleníti a személyes költségeket a vállalati hitelkártyára terhelt vállalati kiadásokkal együtt.</span><span class="sxs-lookup"><span data-stu-id="c43d8-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="c43d8-109">**Vállalat által fizetendő** - A szervezet kifizeti a vállalati hitelkártya teljes számláját, majd levonja a dolgozó számlájáról a személyes kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="c43d8-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="c43d8-110">Megadhatja, hogy a szervezet milyen módszert használ a **költségkezelési paraméterek** lapon.</span><span class="sxs-lookup"><span data-stu-id="c43d8-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]