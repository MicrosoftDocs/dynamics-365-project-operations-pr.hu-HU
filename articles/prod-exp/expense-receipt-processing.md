---
title: Költségnyugta feldolgozása
description: Ez a témakör a nyugták optikai karakterfelismeréssel (OCR) való feldolgozásáról nyújt információkat. Ez a funkció javítja a felhasználói élményt, amikor költségjelentéseket hoznak létre a Microsoft Dynamics 365 Finance alkalmazásban.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271806"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="f18b2-104">Költségnyugta feldolgozása</span><span class="sxs-lookup"><span data-stu-id="f18b2-104">Expense receipt processing</span></span>

<span data-ttu-id="f18b2-105">A költségbejegyzést továbbfejlesztettük a nyugták optikai karakterfelismeréssel (OCR) való feldolgozási funkciójának bevezetésével.</span><span class="sxs-lookup"><span data-stu-id="f18b2-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="f18b2-106">Ez a funkció javítja a felhasználói élményt, amikor költségjelentéseket hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="f18b2-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="f18b2-107">Legfontosabb funkciók</span><span class="sxs-lookup"><span data-stu-id="f18b2-107">Key features</span></span>

- <span data-ttu-id="f18b2-108">A rendszer kinyeri a kereskedő nevét, a dátumot, valamint a teljes összeget a nyugtákról.</span><span class="sxs-lookup"><span data-stu-id="f18b2-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="f18b2-109">Ez a funkció megpróbálja megfeleltetni a nem csatolt nyugtákat és a nem csatolt költségtranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="f18b2-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="f18b2-110">A nyugtákból a felhasználók létrehozhatnak manuálisan megadott költségtranzakciók.</span><span class="sxs-lookup"><span data-stu-id="f18b2-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="f18b2-111">Használati példák</span><span class="sxs-lookup"><span data-stu-id="f18b2-111">Usage examples</span></span>

<span data-ttu-id="f18b2-112">Ha a költségjelentések létrehozásakor automatikusan csatolni szeretné az olyan nyugtákat, amelyeken szerepelnek a hitelkártya-tranzakciók, tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="f18b2-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="f18b2-113">Nyissa meg a **Költségkezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="f18b2-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="f18b2-114">A **Nyugták** lapon ellenőrizze, hogy vannak-e nem csatolt nyugták.</span><span class="sxs-lookup"><span data-stu-id="f18b2-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="f18b2-115">A nyugtákat a **Nyugták** lapon fel is töltheti.</span><span class="sxs-lookup"><span data-stu-id="f18b2-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="f18b2-116">A **Költségek** lapon ellenőrizze, hogy vannak-e nem csatolt költségek.</span><span class="sxs-lookup"><span data-stu-id="f18b2-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="f18b2-117">A költségadminisztrátorok általában a hitelkártya-szolgáltatótól importálják ezeket a költségeket.</span><span class="sxs-lookup"><span data-stu-id="f18b2-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="f18b2-118">Válassza az **Új Költségjelentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f18b2-118">Select **New expense report**.</span></span> <span data-ttu-id="f18b2-119">Vegye figyelembe, hogy már a költségek és a nyugták is megadhatók a költségjelentés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="f18b2-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="f18b2-120">Ha a költségeket és a nyugtákat egyaránt hozzáadja, a rendszer automatikusan egyezteti a nyugtákat a kiadásokkal.</span><span class="sxs-lookup"><span data-stu-id="f18b2-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="f18b2-121">Ha költséget szeretne létrehozni, vagy költséget szeretne egyeztetni egy nyugtáról, tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="f18b2-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="f18b2-122">A költségjelentés **Nyugták** lapján csatoljon egy nyugtát a **Nyugták hozzáadása** lehetőséggel.</span><span class="sxs-lookup"><span data-stu-id="f18b2-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="f18b2-123">A nyugta feltöltött képe alapján találja a **Létrehozás** és az **Egyeztetés** elemet.</span><span class="sxs-lookup"><span data-stu-id="f18b2-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="f18b2-124">A **Létrehozás** lehetőséggel manuálisan megadott költségtranzakciót hozhat létre, amelyet kitölthet a nyugtáról kinyert értékekkel.</span><span class="sxs-lookup"><span data-stu-id="f18b2-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="f18b2-125">Az **Egyeztetés** lehetőség használata esetén a rendszer egy meglévő költséget próbál egyeztetni a nyugtával.</span><span class="sxs-lookup"><span data-stu-id="f18b2-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="f18b2-126">Telepítés</span><span class="sxs-lookup"><span data-stu-id="f18b2-126">Installation</span></span>

<span data-ttu-id="f18b2-127">Ez a funkció a **Költségjelentések újragondolva** funkcióval együtt működik , amely segít leegyszerűsíteni a költségvetések élményét.</span><span class="sxs-lookup"><span data-stu-id="f18b2-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="f18b2-128">Ez a funkció csak 2+ szintű +-környezetek esetén érhető el, amelyek teszt vagy éles környezetek.</span><span class="sxs-lookup"><span data-stu-id="f18b2-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="f18b2-129">A költségek ilyen speciális funkcióinak használatához telepíteni kell a Költségkezelési szolgáltatás bővítményt a Microsoft Dynamics 365 Finance rendszerhez, és be kell kapcsolni a funkciókat a példányban.</span><span class="sxs-lookup"><span data-stu-id="f18b2-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="f18b2-130">A bővítményt a projektből, a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból érheti el.</span><span class="sxs-lookup"><span data-stu-id="f18b2-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="f18b2-131">Jelentkezzen be az LCS rendszerbe, és nyissa meg a kívánt környezetet.</span><span class="sxs-lookup"><span data-stu-id="f18b2-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="f18b2-132">Válassza a **Minden részlet** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f18b2-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="f18b2-133">Válassza a **Karbantartás** lehetőséget, vagy görgessen le a **Környezeti bővítmények** gyorslaphoz.</span><span class="sxs-lookup"><span data-stu-id="f18b2-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="f18b2-134">Válassza az **Új bővítmény telepítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f18b2-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="f18b2-135">Válassza a **Költségkezelési szolgáltatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f18b2-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="f18b2-136">Kövesse a telepítési útmutatót, és fogadja el a használati feltételeket.</span><span class="sxs-lookup"><span data-stu-id="f18b2-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="f18b2-137">Válassza a **Telepítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f18b2-137">Select **Install**.</span></span>

<span data-ttu-id="f18b2-138">A **Szolgáltatások kezelése** munkaterületen kapcsolja be a következő szolgáltatásokat:</span><span class="sxs-lookup"><span data-stu-id="f18b2-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="f18b2-139">Költségjelentések újragondolva</span><span class="sxs-lookup"><span data-stu-id="f18b2-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="f18b2-140">Automatikus egyeztetés és költség létrehozása nyugtából</span><span class="sxs-lookup"><span data-stu-id="f18b2-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="f18b2-141">Amikor bekapcsolja ezeket a funkciókat, a következő műveleteket hajtja végre a rendszer:</span><span class="sxs-lookup"><span data-stu-id="f18b2-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="f18b2-142">A meglévő **Költségkezelés** munkaterület az új munkaterületre cserélődik.</span><span class="sxs-lookup"><span data-stu-id="f18b2-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="f18b2-143">A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.</span><span class="sxs-lookup"><span data-stu-id="f18b2-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="f18b2-144">A korábbi **Költségjelentés** lapot továbbra is megnyithatja a **Költségkezelés > Saját kiadások > Költségjelentések** beállítással.</span><span class="sxs-lookup"><span data-stu-id="f18b2-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="f18b2-145">A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.</span><span class="sxs-lookup"><span data-stu-id="f18b2-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="f18b2-146">A nyugtákat a rendszer a Microsoft Azure Cognitive Services szolgáltatáson keresztül dolgozza fel; a metaadatokat kinyeri és hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="f18b2-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="f18b2-147">A rendszer hozzáad egy olyan beállítást, amellyel a megfeleltetett, nem csatolt nyugtákat tartalmazó költségjelentések hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="f18b2-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="f18b2-148">A rendszer hozzáad egy olyan beállítást a költségjelentésekhez, amellyel költségsor készíthető egy nyugtából, illetve amellyel megpróbálható a meglévő nyugták és költségsorok egyeztetése.</span><span class="sxs-lookup"><span data-stu-id="f18b2-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="f18b2-149">A költségjelentések újragondolása funkcióval kapcsolatos további információk: [Költségjelentések újragondolva](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="f18b2-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f18b2-150">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="f18b2-150">Frequently asked questions</span></span>

<span data-ttu-id="f18b2-151">**Használja a Microsoft az adataimat a modelljeihez?**</span><span class="sxs-lookup"><span data-stu-id="f18b2-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="f18b2-152">Nem, a Microsoft általános gépi tanulás modellt készített a nyugtákat feldolgozó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="f18b2-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="f18b2-153">Ez a modell nem a feltöltött nyugtákon alapul.</span><span class="sxs-lookup"><span data-stu-id="f18b2-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="f18b2-154">**Hol érhető el és hol kerül feldolgozásra a szolgáltatás?**</span><span class="sxs-lookup"><span data-stu-id="f18b2-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="f18b2-155">Jelenleg az Egyesült Államokban támogatott.</span><span class="sxs-lookup"><span data-stu-id="f18b2-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="f18b2-156">**Hová kerülnek a nyugtáim?**</span><span class="sxs-lookup"><span data-stu-id="f18b2-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="f18b2-157">A Finance a Cognitive Services használatával nyeri ki a mezők adatait.</span><span class="sxs-lookup"><span data-stu-id="f18b2-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="f18b2-158">A Cognitive Services legfeljebb 24 óráig, a feldolgozáshoz őrzi meg a nyugták másolatát.</span><span class="sxs-lookup"><span data-stu-id="f18b2-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="f18b2-159">A feldolgozás befejezése után a Cognitive Services eltávolítja a nyugtát.</span><span class="sxs-lookup"><span data-stu-id="f18b2-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="f18b2-160">A Finance továbbra is tárolja majd a nyugtákat.</span><span class="sxs-lookup"><span data-stu-id="f18b2-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="f18b2-161">További információ: [A nyugták Form Recognizer új funkciójával történő felismerésének engedélyezése](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="f18b2-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]