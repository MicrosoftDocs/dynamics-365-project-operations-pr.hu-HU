---
title: Jóváhagyási készletek
description: Ez témakör információkat tartalmaz a jóváhagyási készletről, a kérelmekről, valamint ezen műveletek részhalmazairól.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116874"
---
# <a name="approval-sets"></a><span data-ttu-id="0012c-103">Jóváhagyási készletek</span><span class="sxs-lookup"><span data-stu-id="0012c-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0012c-104">A jóváhagyási készletek a jóváhagyás-kérelmeket a műveletek kisebb részhalmazaiba csoportosítja.</span><span class="sxs-lookup"><span data-stu-id="0012c-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="0012c-105">Ez a csoportosítás lehetővé teszi a jóváhagyások sorrendben való feldolgozását a Projekt által, és lehetővé teszi az újrapróbálkozást és a sorrendezést.</span><span class="sxs-lookup"><span data-stu-id="0012c-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="0012c-106">A csoportosítás javítja a jóváhagyás-feldolgozás megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén.</span><span class="sxs-lookup"><span data-stu-id="0012c-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="0012c-107">A jóváhagyási készletek jelzik a kapcsolódó bejegyzések teljes feldolgozási állapotát.</span><span class="sxs-lookup"><span data-stu-id="0012c-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="0012c-108">Amikor egy jóváhagyási rekord feldolgozása egy jóváhagyási készlet használatával történik, a bejegyzés átlép a **Beküldött** állapotból **Jóváhagyott** állapotba, és nem lesz csatolva a jóváhagyási készlethez.</span><span class="sxs-lookup"><span data-stu-id="0012c-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="0012c-109">Ha egy rekord meghiúsul, amikor el van jelölve jóváhagyásra, a bejegyzés **Beküldött** állapotú marad, és a jóváhagyási készlet sikertelenként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="0012c-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="0012c-110">A jóváhagyási készlet naplózza a hiba hibaüzenetét.</span><span class="sxs-lookup"><span data-stu-id="0012c-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="0012c-111">Jóváhagyások és jóváhagyási készletek feldolgozása</span><span class="sxs-lookup"><span data-stu-id="0012c-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="0012c-112">A feldolgozási sorban várakozó jóváhagyások a **Jóváhagyások feldolgozása** nézetben láthatók.</span><span class="sxs-lookup"><span data-stu-id="0012c-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="0012c-113">A rendszer megpróbálja az összes bejegyzést aszinkron módon feldolgozni, beleértve a jóváhagyás újrapróbálkozási kísérletét is, ha a korábbi próbálkozások sikertelenek voltak.</span><span class="sxs-lookup"><span data-stu-id="0012c-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="0012c-114">A **Jóváhagyási készlet élettartama** mező rögzíti, hogy hány kísérlet maradt a készlet feldolgozására, mielőtt sikertelenként jelölték volna meg.</span><span class="sxs-lookup"><span data-stu-id="0012c-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="0012c-115">Meghiúsult jóváhagyások és jóváhagyási készletek</span><span class="sxs-lookup"><span data-stu-id="0012c-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="0012c-116">A **Sikertelen jóváhagyások** nézet felsorolja a felhasználói beavatkozást igénylő összes jóváhagyást.</span><span class="sxs-lookup"><span data-stu-id="0012c-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="0012c-117">Nyissa meg a társított jóváhagyási készlet naplóit, hogy azonosítsa a hiba okát.</span><span class="sxs-lookup"><span data-stu-id="0012c-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="0012c-118">Ha kiválasztja az **Újrapróbálkozás** hozzáadja a a jóváhagyási készlet életciklusszámát, és visszahelyezi a jóváhagyási készletet **Feldolgozás** állapotba, és megpróbálja feldolgozni a fennmaradó rekordokat.</span><span class="sxs-lookup"><span data-stu-id="0012c-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="0012c-119">Jóváhagyási készletek konfigurálása</span><span class="sxs-lookup"><span data-stu-id="0012c-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="0012c-120">A Jóváhagyási készletek funkció engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0012c-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="0012c-121">A Jóváhagyáskészletek funkció engedélyezése előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.</span><span class="sxs-lookup"><span data-stu-id="0012c-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="0012c-122">Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások engedélyezése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0012c-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="0012c-123">Kapcsolja ki a Jóváhagyási készletek funkciót</span><span class="sxs-lookup"><span data-stu-id="0012c-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="0012c-124">A Jóváhagyáskészletek funkció kikapcsolása előtt ellenőrizze, hogy nincsenek-e jóváhagyások feldolgozás alatt.</span><span class="sxs-lookup"><span data-stu-id="0012c-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="0012c-125">Menjen a **Projektparaméterek** oldalra, és válassza a **Funkcióvezérlés** > **Modern jóváhagyások letiltása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="0012c-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="0012c-126">Az aszinkron küszöbérték konfigurálása</span><span class="sxs-lookup"><span data-stu-id="0012c-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="0012c-127">A jóváhagyási készletek létrehozásakor a feldolgozás a háttérbe kerül, ha a jóváhagyásra kijelölt bejegyzések száma meghaladja a jelzett küszöbértéket.</span><span class="sxs-lookup"><span data-stu-id="0012c-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="0012c-128">Az **Aszinkron küszöbérték** mező segítségével konfigurálhatja, hogy a jóváhagyás feldolgozása mikor fusson szinkronizált vagy aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="0012c-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="0012c-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0012c-129">Valid values are:</span></span>

  - <span data-ttu-id="0012c-130">Nulla: Minden kérést aszinkron módon kell feldolgozni.</span><span class="sxs-lookup"><span data-stu-id="0012c-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="0012c-131">Nullánál nagyobb számok: A jóváhagyások feldolgozása csak akkor történik meg aszinkron módon, ha a beküldött jóváhagyások száma meghaladja ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="0012c-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
