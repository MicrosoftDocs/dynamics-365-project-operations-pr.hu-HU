---
title: Erőforrás-kapacitás szinkronizálása
description: Ez a témakör információkat tartalmaz arról, hogyan szinkronizálható az erőforrások kapacitása a naptárak és a projektek között.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078070"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="a144f-103">Erőforrás-kapacitás szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="a144f-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a144f-104">Az erőforrás-szinkronizálási folyamatok segítségével biztosítható, hogy a naptár és az alapnaptár adatai eljutnak a projekterőforrás-ütemezésébe.</span><span class="sxs-lookup"><span data-stu-id="a144f-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="a144f-105">A naptár módosítása esetén a folyamat végrehajtja a projektek erőforrásainak ütemezéséhez szükséges frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="a144f-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="a144f-106">A folyamatok a teljesítmény javítását is segítik, mivel a naptár erőforrás-információit előre szinkronizálja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a144f-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="a144f-107">Ezért gyorsabban történnek az erőforrás-ütemezési adatok frissítései.</span><span class="sxs-lookup"><span data-stu-id="a144f-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="a144f-108">Javasoljuk, hogy a folyamatokat ne egyenként, hanem kötegelve ütemezze.</span><span class="sxs-lookup"><span data-stu-id="a144f-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="a144f-109">Ellenkező esetben fennáll annak a veszélye, hogy valaki elfelejti a bezárólagos dátumokat, amikor az adatok legutóbbi szinkronizálása megtörtént.</span><span class="sxs-lookup"><span data-stu-id="a144f-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="a144f-110">Ha nem bezárólagos dátumokat használ, akkor a szinkronizálás során hézagok keletkezhetnek.</span><span class="sxs-lookup"><span data-stu-id="a144f-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Naptár szinkronizálása](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="a144f-112">Erőforráskapacitás-összesítések szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="a144f-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="a144f-113">A szinkronizálási folyamat az összes erőforrásnaptár-információ szinkronizálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="a144f-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="a144f-114">Ezek az információk a projekt erőforrásnaptár-kapacitásainak táblázatában bekövetkezett változásokkal kapcsolatos alapvető naptár-információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a144f-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="a144f-115">Ha új erőforrásokat vesz fel a projektbe, a szinkronizálás segít biztosítani, hogy a frissített naptárinformációk elérhetők legyenek.</span><span class="sxs-lookup"><span data-stu-id="a144f-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="a144f-116">A szinkronizálás bármikor végrehajtható.</span><span class="sxs-lookup"><span data-stu-id="a144f-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="a144f-117">Javasoljuk, hogy használja használjon köteget.</span><span class="sxs-lookup"><span data-stu-id="a144f-117">We recommend that you use a batch.</span></span> <span data-ttu-id="a144f-118">A beállítások a kapacitásfoglalások szinkronizálása során érhetők el.</span><span class="sxs-lookup"><span data-stu-id="a144f-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="a144f-119">Válassza a **Projektmenedzsment és könyvelés** &gt; **Időszakos** &gt; **Kapacitás szinkronizálása** &gt; **Erőforráskapacitás-összesítések szinkronizálása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a144f-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="a144f-120">Adja meg a beállításokat a következő táblázatban.</span><span class="sxs-lookup"><span data-stu-id="a144f-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="a144f-121">Beállítás</span><span class="sxs-lookup"><span data-stu-id="a144f-121">Option</span></span>      | <span data-ttu-id="a144f-122">Ismertetés</span><span class="sxs-lookup"><span data-stu-id="a144f-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="a144f-123">Időszak kódja</span><span class="sxs-lookup"><span data-stu-id="a144f-123">Period code</span></span> | <span data-ttu-id="a144f-124">Opcionálisan kiválaszthatja a főkönyvi dátum intervallumkódját az erőforráskapacitás-összesítések szinkronizálási folyamatához tartozó kezdő és záró dátumok beállításához.</span><span class="sxs-lookup"><span data-stu-id="a144f-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a144f-125">Kezdő dátum</span><span class="sxs-lookup"><span data-stu-id="a144f-125">Start date</span></span>  | <span data-ttu-id="a144f-126">Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának kezdő dátumát.</span><span class="sxs-lookup"><span data-stu-id="a144f-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a144f-127">Befejező dátum</span><span class="sxs-lookup"><span data-stu-id="a144f-127">End date</span></span>    | <span data-ttu-id="a144f-128">Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának záró dátumát.</span><span class="sxs-lookup"><span data-stu-id="a144f-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="a144f-129">[![Szinkronizálási folyamat](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="a144f-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
