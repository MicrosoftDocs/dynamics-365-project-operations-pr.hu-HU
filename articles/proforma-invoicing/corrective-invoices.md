---
title: Kijavított számlák
description: Ez a témakör a kijavított számlákról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898084"
---
# <a name="corrected-invoices"></a><span data-ttu-id="98334-103">Kijavított számlák</span><span class="sxs-lookup"><span data-stu-id="98334-103">Corrected invoices</span></span>

<span data-ttu-id="98334-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="98334-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98334-105">A megerősített számlák szerkeszthetők.</span><span class="sxs-lookup"><span data-stu-id="98334-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="98334-106">Egy megerősített számla szerkesztésekor a kijavított számla piszkozata jön létre.</span><span class="sxs-lookup"><span data-stu-id="98334-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="98334-107">Mivel a feltételezés az, hogy meg akarja fordítani az eredeti számla összes tranzakcióját és mennyiségét, ez a kijavított számla tartalmazza az eredeti számla összes tranzakcióját, és a rajta lévő teljes mennyiség 0 (nulla).</span><span class="sxs-lookup"><span data-stu-id="98334-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="98334-108">Ha bármely tranzakció nem igényel javítást, akkor eltávolíthatja azt a korrekciós számlavázlatból.</span><span class="sxs-lookup"><span data-stu-id="98334-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="98334-109">Ha csak részleges mennyiséget kíván megfordítani, vagy visszatéríteni, az adatsor részleteit a Mennyiség mezőben szerkesztheti.</span><span class="sxs-lookup"><span data-stu-id="98334-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="98334-110">Ha kinyitja a számlasor részleteit, láthatja az eredeti számlamennyiséget.</span><span class="sxs-lookup"><span data-stu-id="98334-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="98334-111">Ezután módosíthatja az aktuális számlamennyiséget oly módon, hogy az kevesebb vagy több legyen, mint az eredeti számlamennyiség.</span><span class="sxs-lookup"><span data-stu-id="98334-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="98334-112">A korrekciós számla megerősítésekor az eredetileg számlázott tényleges értékesítés megfordul, és létrejön egy újonnan számlázott tényleges értékesítés.</span><span class="sxs-lookup"><span data-stu-id="98334-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="98334-113">Ha a mennyiséget csökkentették, a különbség egy új, nem számlázott értékesítés létrehozását is eredményezi.</span><span class="sxs-lookup"><span data-stu-id="98334-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="98334-114">Ha például az eredeti számlázott értékesítés nyolc órán keresztül történt, és a javított számla sorában lévő részlet hat óra, a rendszer megfordítja az eredeti számlázott értékesítési sort, és két új aktuális értéket hoz létre:</span><span class="sxs-lookup"><span data-stu-id="98334-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="98334-115">Hat órás tényleges számlázott értékesítés.</span><span class="sxs-lookup"><span data-stu-id="98334-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="98334-116">Nem számlázott tényleges értékesítés a fennmaradó két órára.</span><span class="sxs-lookup"><span data-stu-id="98334-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="98334-117">Ezt a tranzakciót később számlázhatják, vagy pedig díjmentesnek jelölhetik, az ügyféllel folytatott tárgyalásoktól függően.</span><span class="sxs-lookup"><span data-stu-id="98334-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
