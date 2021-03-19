---
title: Nyugta rögzítése OCR használatával
description: Ez a témakör a nyugták optikai karakterfelismeréssel (OCR) való feldolgozásáról nyújt információkat.
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
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499854"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="1fd89-103">Nyugta rögzítése OCR használatával</span><span class="sxs-lookup"><span data-stu-id="1fd89-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="1fd89-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="1fd89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1fd89-105">A költségbejegyzést továbbfejlesztettük a nyugták optikai karakterfelismeréssel (OCR) való feldolgozási funkciójának bevezetésével.</span><span class="sxs-lookup"><span data-stu-id="1fd89-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="1fd89-106">Ez a funkció egyszerűbbé teszi a költségjelentések létrehozását.</span><span class="sxs-lookup"><span data-stu-id="1fd89-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="1fd89-107">Legfontosabb funkciók</span><span class="sxs-lookup"><span data-stu-id="1fd89-107">Key features</span></span>

- <span data-ttu-id="1fd89-108">A rendszer kinyeri a kereskedő nevét, a dátumot, valamint a nyugtákon lévő teljes összeget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="1fd89-109">Ezenkívül megpróbálja megfeleltetni a nem csatolt nyugtákat és a nem csatolt költségtranzakciókat.</span><span class="sxs-lookup"><span data-stu-id="1fd89-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="1fd89-110">A nyugtákból hozhatók létre manuálisan megadott költségtranzakciók.</span><span class="sxs-lookup"><span data-stu-id="1fd89-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="1fd89-111">Nyugták csatolása költségjelentéshez</span><span class="sxs-lookup"><span data-stu-id="1fd89-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="1fd89-112">Ha a költségjelentések létrehozásakor automatikusan csatolni szeretné az olyan nyugtákat, amelyeken szerepelnek a hitelkártya-tranzakciók, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="1fd89-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="1fd89-113">Nyissa meg a **Költségkezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="1fd89-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="1fd89-114">A **Nyugták** lapon ellenőrizze, hogy vannak-e nem csatolt nyugták.</span><span class="sxs-lookup"><span data-stu-id="1fd89-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="1fd89-115">A nyugtákat a **Nyugták** lapon fel is töltheti.</span><span class="sxs-lookup"><span data-stu-id="1fd89-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="1fd89-116">A **Költségek** lapon ellenőrizze, hogy vannak-e nem csatolt költségek.</span><span class="sxs-lookup"><span data-stu-id="1fd89-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="1fd89-117">A költségadminisztrátorok általában a hitelkártya-szolgáltatótól importálják ezeket a költségeket.</span><span class="sxs-lookup"><span data-stu-id="1fd89-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="1fd89-118">Válassza az **Új Költségjelentés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-118">Select **New expense report**.</span></span> <span data-ttu-id="1fd89-119">Vegye figyelembe, hogy már a költségek és a nyugták is megadhatók a költségjelentés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="1fd89-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="1fd89-120">Ha a költségeket és a nyugtákat egyaránt hozzáadja, a rendszer automatikusan egyezteti a nyugtákat a kiadásokkal.</span><span class="sxs-lookup"><span data-stu-id="1fd89-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="1fd89-121">Nyugták létrehozása és egyeztetése költségjelentéshez</span><span class="sxs-lookup"><span data-stu-id="1fd89-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="1fd89-122">Ha költséget szeretne létrehozni, vagy költséget szeretne egyeztetni egy nyugtáról, hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="1fd89-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="1fd89-123">A költségjelentés **Nyugták** lapján csatoljon egy nyugtát a **Nyugták hozzáadása** lehetőséggel.</span><span class="sxs-lookup"><span data-stu-id="1fd89-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="1fd89-124">A nyugta feltöltött képe alapján találja a **Létrehozás** és az **Egyeztetés** elemet.</span><span class="sxs-lookup"><span data-stu-id="1fd89-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="1fd89-125">A **Létrehozás** lehetőséggel manuálisan megadott költségtranzakciót hozhat létre, amelyet kitölthet a nyugtáról kinyert értékekkel.</span><span class="sxs-lookup"><span data-stu-id="1fd89-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="1fd89-126">Az **Egyeztetés** lehetőség használata esetén a rendszer egy meglévő költséget próbál egyeztetni a nyugtával.</span><span class="sxs-lookup"><span data-stu-id="1fd89-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="1fd89-127">Telepítés</span><span class="sxs-lookup"><span data-stu-id="1fd89-127">Installation</span></span>

<span data-ttu-id="1fd89-128">A költségek ilyen speciális funkcióinak használatához telepíteni kell a Költségkezelési szolgáltatás bővítményt a Microsoft Dynamics 365 Finance rendszerhez, és be kell kapcsolni a funkciókat a példányban.</span><span class="sxs-lookup"><span data-stu-id="1fd89-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="1fd89-129">A bővítményt a projektből, a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból érheti el.</span><span class="sxs-lookup"><span data-stu-id="1fd89-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="1fd89-130">Jelentkezzen be az LCS rendszerbe, és nyissa meg a kívánt környezetet.</span><span class="sxs-lookup"><span data-stu-id="1fd89-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="1fd89-131">Válassza a **Minden részlet** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="1fd89-132">Válassza a **Karbantartás** lehetőséget, vagy görgessen le a **Környezeti bővítmények** gyorslaphoz.</span><span class="sxs-lookup"><span data-stu-id="1fd89-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="1fd89-133">Válassza az **Új bővítmény telepítése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="1fd89-134">Válassza a **Költségkezelési szolgáltatás** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="1fd89-135">Kövesse a telepítési útmutatót, és fogadja el a használati feltételeket.</span><span class="sxs-lookup"><span data-stu-id="1fd89-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="1fd89-136">Válassza a **Telepítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1fd89-136">Select **Install**.</span></span>

<span data-ttu-id="1fd89-137">A **Szolgáltatások kezelése** munkaterületen kapcsolja be a következő szolgáltatásokat:</span><span class="sxs-lookup"><span data-stu-id="1fd89-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="1fd89-138">Költségjelentések újragondolva</span><span class="sxs-lookup"><span data-stu-id="1fd89-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="1fd89-139">Automatikus egyeztetés és költség létrehozása nyugtából</span><span class="sxs-lookup"><span data-stu-id="1fd89-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="1fd89-140">Amikor bekapcsolja ezeket a funkciókat, a következő műveleteket hajtja végre a rendszer:</span><span class="sxs-lookup"><span data-stu-id="1fd89-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="1fd89-141">A meglévő **Költségkezelés** munkaterület az új munkaterületre cserélődik.</span><span class="sxs-lookup"><span data-stu-id="1fd89-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="1fd89-142">A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.</span><span class="sxs-lookup"><span data-stu-id="1fd89-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="1fd89-143">A korábbi **Költségjelentés** lapot továbbra is megnyithatja a **Költségkezelés > Saját kiadások > Költségjelentések** beállítással.</span><span class="sxs-lookup"><span data-stu-id="1fd89-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="1fd89-144">A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.</span><span class="sxs-lookup"><span data-stu-id="1fd89-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="1fd89-145">A nyugtákat a rendszer a Microsoft Azure Cognitive Services szolgáltatáson keresztül dolgozza fel; a metaadatokat kinyeri és hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="1fd89-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="1fd89-146">A rendszer hozzáad egy olyan beállítást, amellyel a megfeleltetett, nem csatolt nyugtákat tartalmazó költségjelentések hozhatók létre.</span><span class="sxs-lookup"><span data-stu-id="1fd89-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="1fd89-147">A rendszer hozzáad egy olyan beállítást a költségjelentésekhez, amellyel költségsor készíthető egy nyugtából, illetve amellyel megpróbálható a meglévő nyugták és költségsorok egyeztetése.</span><span class="sxs-lookup"><span data-stu-id="1fd89-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1fd89-148">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="1fd89-148">Frequently asked questions</span></span>

<span data-ttu-id="1fd89-149">**Használja a Microsoft az adataimat a modelljeihez?**</span><span class="sxs-lookup"><span data-stu-id="1fd89-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="1fd89-150">Nem, a Microsoft általános gépi tanulás modellt készített a nyugtákat feldolgozó szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="1fd89-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="1fd89-151">Ez a modell nem a feltöltött nyugtákon alapul.</span><span class="sxs-lookup"><span data-stu-id="1fd89-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="1fd89-152">**Hol érhető el és hol kerül feldolgozásra a szolgáltatás?**</span><span class="sxs-lookup"><span data-stu-id="1fd89-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="1fd89-153">Jelenleg az Egyesült Államokban támogatott.</span><span class="sxs-lookup"><span data-stu-id="1fd89-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="1fd89-154">**Hová kerülnek a nyugtáim?**</span><span class="sxs-lookup"><span data-stu-id="1fd89-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="1fd89-155">A Finance a Cognitive Services használatával nyeri ki a mezők adatait.</span><span class="sxs-lookup"><span data-stu-id="1fd89-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="1fd89-156">A Cognitive Services legfeljebb 24 óráig, a feldolgozáshoz őrzi meg a nyugták másolatát.</span><span class="sxs-lookup"><span data-stu-id="1fd89-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="1fd89-157">A feldolgozás befejezése után a Cognitive Services eltávolítja a nyugtát.</span><span class="sxs-lookup"><span data-stu-id="1fd89-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="1fd89-158">A Finance továbbra is tárolja majd a nyugtákat.</span><span class="sxs-lookup"><span data-stu-id="1fd89-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="1fd89-159">További információ: [A nyugták Form Recognizer új funkciójával történő felismerésének engedélyezése](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="1fd89-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
