---
title: A pénzügyi dimenzió alapértelmezései
description: Ez a témakör a pénzügyi dimenzió alapértelmezéseinek beállításával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013309"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="4f15f-103">A pénzügyi dimenzió alapértelmezései</span><span class="sxs-lookup"><span data-stu-id="4f15f-103">Financial dimension defaults</span></span>

<span data-ttu-id="4f15f-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="4f15f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f15f-105">A Dynamics 365 Project Operations a [Pénzügyi dimenziók](/dynamics365/finance/general-ledger/financial-dimensions) keretrendszert használja a Dynamics 365 Finance alkalmazásban, hogy betekintést nyújtson a projektek alkönyvei és a főkönyvek tranzakcióiba.</span><span class="sxs-lookup"><span data-stu-id="4f15f-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="4f15f-106">Az alapértelmezett pénzügyi dimenziókat az ügyfél, a projekt finanszírozása, a mérföldkő, a projekt szerződéssor vagy a projekt szintjén lehet beállítani.</span><span class="sxs-lookup"><span data-stu-id="4f15f-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="4f15f-107">Az ügyfél alapértelmezett pénzügyi dimenzióinak definiálása</span><span class="sxs-lookup"><span data-stu-id="4f15f-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="4f15f-108">Az ügyfelek dimenzióinak alapértékei a Finance-ben vannak meghatározva.</span><span class="sxs-lookup"><span data-stu-id="4f15f-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="4f15f-109">A dimenziók alapértelmezéseinek beállításához hajtsa végre az alábbi műveleteket.</span><span class="sxs-lookup"><span data-stu-id="4f15f-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="4f15f-110">Nyissa meg a **Kinnlevőségek** > **Ügyfelek** > **Összes ügyfél** menüpontot.</span><span class="sxs-lookup"><span data-stu-id="4f15f-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="4f15f-111">Az **Ügyfelek** lap **Pénzügyi dimenziók** fülén állítsa be adott ügyfél pénzügyidimenzió-értékeit.</span><span class="sxs-lookup"><span data-stu-id="4f15f-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="4f15f-112">Az projektszerződések alapértelmezett pénzügyi dimenzióinak definiálása</span><span class="sxs-lookup"><span data-stu-id="4f15f-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="4f15f-113">A projektszerződések a Common Data Service (CDS) szolgáltatásban hozhatók létre és tarthatók karban.</span><span class="sxs-lookup"><span data-stu-id="4f15f-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="4f15f-114">A projektszerződések számlázási attribútumait a **Projektmenedzsment és könyvelés** modulban lehet beállítani a Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="4f15f-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="4f15f-115">Pénzügyi dimenziók beállítása a projektek finanszírozási forrásaihoz</span><span class="sxs-lookup"><span data-stu-id="4f15f-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="4f15f-116">Lépjen a **Projektvezetés és könyvelés** > **Projektek** > **Projektszerződések** elemre.</span><span class="sxs-lookup"><span data-stu-id="4f15f-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="4f15f-117">Jelölje ki a frissíteni kívánt rekordot, majd a **Projektszerződés** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="4f15f-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="4f15f-118">Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Finanszírozási források** lapot.</span><span class="sxs-lookup"><span data-stu-id="4f15f-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="4f15f-119">Állítsa be a pénzügyi dimenzió alapértelmezéseit.</span><span class="sxs-lookup"><span data-stu-id="4f15f-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="4f15f-120">Figyelje meg, hogy a pénzügyi dimenziók alapértelmezései az ügyfélfiókból származnak.</span><span class="sxs-lookup"><span data-stu-id="4f15f-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="4f15f-121">Pénzügyi dimenziók beállítása a projektszerződés-sorhoz</span><span class="sxs-lookup"><span data-stu-id="4f15f-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="4f15f-122">Lépjen a **Projektvezetés és könyvelés** > **Projektek** > **Projektszerződések** elemre.</span><span class="sxs-lookup"><span data-stu-id="4f15f-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="4f15f-123">Jelölje ki a frissíteni kívánt rekordot, majd a **Projektszerződés** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="4f15f-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="4f15f-124">Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Szerződéssorok** lapot.</span><span class="sxs-lookup"><span data-stu-id="4f15f-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="4f15f-125">Állítsa be a pénzügyi dimenzió alapértelmezéseit.</span><span class="sxs-lookup"><span data-stu-id="4f15f-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="4f15f-126">A pénzügyi dimenzió alapértelmezései érvényesek, és csak rögzített áras (mérföldkő) szerződéssorokhoz használhatók.</span><span class="sxs-lookup"><span data-stu-id="4f15f-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="4f15f-127">Ezek az alapértelmezések a kapcsolódó projekt számlatranzakciói és számlasorai esetén használhatók.</span><span class="sxs-lookup"><span data-stu-id="4f15f-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="4f15f-128">Az projektek alapértelmezett pénzügyi dimenzióinak definiálása</span><span class="sxs-lookup"><span data-stu-id="4f15f-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="4f15f-129">A projektek CDS szolgáltatásban hozhatók létre és tarthatók karban.</span><span class="sxs-lookup"><span data-stu-id="4f15f-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="4f15f-130">A projektek számlázási attribútumait a **Projektmenedzsment és könyvelés** modulban lehet beállítani a Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="4f15f-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="4f15f-131">Lépjen a **Projektmenedzsment és könyvelés** > **Projektek** > **Minden projekt** elemre.</span><span class="sxs-lookup"><span data-stu-id="4f15f-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="4f15f-132">Jelölje ki a frissíteni kívánt rekordot, majd a **Projekt** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="4f15f-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="4f15f-133">Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Beállítások** lapot.</span><span class="sxs-lookup"><span data-stu-id="4f15f-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="4f15f-134">Állítsa be a pénzügyi dimenzió alapértelmezéseit.</span><span class="sxs-lookup"><span data-stu-id="4f15f-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="4f15f-135">Figyelje meg, hogy a pénzügyi dimenziók alapértelmezései az ügyfélfiókból származnak.</span><span class="sxs-lookup"><span data-stu-id="4f15f-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="4f15f-136">Ha a projekt olyan szerződéssorhoz van társítva, amely több szerződésese ügyfelet tartalmaz, akkor az elsődleges ügyfél lesz használva a pénzügyi dimenzió alapértelmezéseiben.</span><span class="sxs-lookup"><span data-stu-id="4f15f-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="4f15f-137">A projekt alapértelmezett pénzügyi dimenziói az idő-, költség-és díj tranzakciók naplósorai alapértelmezéseinek beállítására szolgálnak a **Project Operations integrációs naplóban** és a kapcsolódó projektszámla-sorokban.</span><span class="sxs-lookup"><span data-stu-id="4f15f-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]