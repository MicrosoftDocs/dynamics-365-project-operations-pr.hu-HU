---
title: Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása és alkalmazása
description: Ez a témakör a szállítói kifizetések visszatartási feltételeinek beállításával és karbantartásával kapcsolatban tartalmaz tájékoztatást.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270951"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="e3a81-103">Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása és alkalmazása</span><span class="sxs-lookup"><span data-stu-id="e3a81-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="e3a81-104">A szállítói fizetési visszatartási feltételek beállítása egy projekthez akkor lehet hasznos, ha a szervezet vissza szeretné tartani a szállítónak teljesített fizetések egy részét.</span><span class="sxs-lookup"><span data-stu-id="e3a81-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="e3a81-105">Ha például egy szállító esetében vissza szeretne tartani kifizetést, amíg a leszállított termékek meg nem felelnek az elvárásainak.</span><span class="sxs-lookup"><span data-stu-id="e3a81-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="e3a81-106">A szállítói kifizetések visszatartási feltételei megadhatók a szállítói szerződés tárgyalása során.</span><span class="sxs-lookup"><span data-stu-id="e3a81-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="e3a81-107">Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="e3a81-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="e3a81-108">Megadhatja a visszatartandó szállítói kifizetés százalékértékét, és a korábban visszatartott és felszabadítandó összegek százalékos arányát.</span><span class="sxs-lookup"><span data-stu-id="e3a81-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="e3a81-109">Az összegek a szállítói számlákhoz automatikusan vissza lesznek tartva mindaddig, amíg a szerződés el nem éri a megadott teljesítési állapotot.</span><span class="sxs-lookup"><span data-stu-id="e3a81-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="e3a81-110">Miután beállította a visszatartási feltételeket, az adott szállítóhoz tartozó bármely projektre alkalmazhatja őket.</span><span class="sxs-lookup"><span data-stu-id="e3a81-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="e3a81-111">A következő lépésekkel állíthatja be és tarthatja karban a szállítói kifizetések visszatartási feltételeit.</span><span class="sxs-lookup"><span data-stu-id="e3a81-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="e3a81-112">Nyissa meg a **Projektmenedzsment és könyvelés** > **Visszatartás** > **Szállítói kifizetések visszatartási feltétele** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e3a81-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="e3a81-113">Új Szállítói visszatartási feltétel hozzáadásához válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e3a81-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="e3a81-114">A rendszer automatikusan beviszi az új feltételhez tartozó **Szabályazonosító** értékét.</span><span class="sxs-lookup"><span data-stu-id="e3a81-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="e3a81-115">Írjon be egy rövid leírást a **Leírás** mezőbe, és a **Feltételek** gyorslapon válassza a **Sor hozzáadása** lehetőséget, hogy megadja a feltételek értékeit a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="e3a81-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="e3a81-116">**A leszállított egységek százalékos aránya**: Adja meg a kifejezés teljesítésének százalékos értékét.</span><span class="sxs-lookup"><span data-stu-id="e3a81-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="e3a81-117">Az összegek a szállítói számlákhoz automatikusan vissza lesznek tartva mindaddig, amíg a projekt teljesítési állapota el nem éri a megadott teljesítési százalékértéket.</span><span class="sxs-lookup"><span data-stu-id="e3a81-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="e3a81-118">Ha például az 50,00 értéket adja meg, akkor a program az összegeket mindaddig visszatartja amíg a projekt 50%-ban be nem fejeződött.</span><span class="sxs-lookup"><span data-stu-id="e3a81-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="e3a81-119">**Megtartás százalékos aránya**: Adja meg a visszatartott szállítói számlaösszeg százalékos értékét.</span><span class="sxs-lookup"><span data-stu-id="e3a81-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="e3a81-120">Ha például a 10,00 értéket adja meg, akkor a program a szállítói számlán szereplő összeg 10%-át tartja vissza, amíg a projekt e nem éri a **A leszállított egységek százalékos aránya** mezőben meghatározott teljesítési százalékot.</span><span class="sxs-lookup"><span data-stu-id="e3a81-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="e3a81-121">**Százalék felszabadításhoz**: Válassza a **Sor hozzáadása** a korábban visszatartott összegek százalékértéknek megadásához a kiválasztott projektteljesítési szinthez.</span><span class="sxs-lookup"><span data-stu-id="e3a81-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="e3a81-122">Ha a projektek teljesítésének különböző szintjeihez több mérföldkő is tartozik, akkor minden egyes visszatartási szabályhoz adjon meg egy külön szállítói visszatartásifeltétel-sort.</span><span class="sxs-lookup"><span data-stu-id="e3a81-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="e3a81-123">Mindegyik sor megadhat egy másik visszatartási százalékértéket és egy másik felszabadítási százalékértéket a projektek teljesítésének egyes meghatározott szintjeire vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="e3a81-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="e3a81-124">Miután létrehozta a szállítói visszatartási feltételeket egy szállítóhoz, a feltételeket egy projekthez alkalmazhatja.</span><span class="sxs-lookup"><span data-stu-id="e3a81-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="e3a81-125">Szállítói visszatartási feltételek alkalmazása egy projektre</span><span class="sxs-lookup"><span data-stu-id="e3a81-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="e3a81-126">Nyissa meg a **Projektmenedzsment és könyvelés** > **Projektek** > **Minden projekt** lehetőséget, és nyissa meg a projektet a projektlista lapról.</span><span class="sxs-lookup"><span data-stu-id="e3a81-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="e3a81-127">A **Szállítói megállapodások** gyorslapon jelölje be a **sor hozzáadása** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="e3a81-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="e3a81-128">Az **Partnerkód mezőben** válasszon a következő lehetőségek közül:</span><span class="sxs-lookup"><span data-stu-id="e3a81-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="e3a81-129">**Táblázat**: A szállítói visszatartási feltételek egyetlen szállítóra vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="e3a81-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="e3a81-130">**Csoport** – a szállítói visszatartási feltételek a szállítói csoport minden szállítója esetében érvényesek.</span><span class="sxs-lookup"><span data-stu-id="e3a81-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="e3a81-131">**Összes**: A szállítói visszatartási feltételek az összes szállítóra vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="e3a81-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="e3a81-132">A **Szállító/szállítói csoport mezőben** válassza ki azt a szállítót vagy szállítói csoportot, amelyikre a szállítói visszatartási feltételek vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="e3a81-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="e3a81-133">Ha az előző lépésben az **Összes** lehetőséget választotta, akkor ez a mező nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="e3a81-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="e3a81-134">A **Szállítói visszatartási feltételek** mezőben jelölje ki az előző eljárásban létrehozott visszatartási feltételeket.</span><span class="sxs-lookup"><span data-stu-id="e3a81-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="e3a81-135">Ha a projekt a szállítóra vonatkozóan fizetéskor fizetett (PWP) feltételek is be vannak állítva, akkor adja meg a projekt küszöbértékét a **PWP-küszöb százalékértéke** mezőben.</span><span class="sxs-lookup"><span data-stu-id="e3a81-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="e3a81-136">A szállítóhoz létrehozott beszerzési megrendeléseken a szállítói visszatartási feltételek is megjelennek.</span><span class="sxs-lookup"><span data-stu-id="e3a81-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]