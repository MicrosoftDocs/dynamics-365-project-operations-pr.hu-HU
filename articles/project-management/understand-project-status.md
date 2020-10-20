---
title: Projekt állapotának megismerése
description: Ez a témakör információkat nyújt a projektekhez rendelt állapotokról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965679"
---
# <a name="understand-project-status"></a><span data-ttu-id="80726-103">Projekt állapotának megismerése</span><span class="sxs-lookup"><span data-stu-id="80726-103">Understand project status</span></span>

<span data-ttu-id="80726-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="80726-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="80726-105">Az **Állapot** szakasz a **Projektentitás** oldalon a projekt állapotának költség és erőfeszítés alapján történő összegzését tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="80726-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="80726-106">Állapot-összefoglaló mezők</span><span class="sxs-lookup"><span data-stu-id="80726-106">Status summary fields</span></span>

- <span data-ttu-id="80726-107">A **Projekt általános állapota** mező egy szerkeszthető mező, amely a projekt általános állapotát mutatja.</span><span class="sxs-lookup"><span data-stu-id="80726-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="80726-108">Ez a mező színkódolást használ, például a zöld, a sárga és a vörös, hogy jelezze a növekvő kockázatot.</span><span class="sxs-lookup"><span data-stu-id="80726-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="80726-109">A **Megjegyzések** mezőben a projektmenedzser konkrét megjegyzéseket fűzhet az állapothoz.</span><span class="sxs-lookup"><span data-stu-id="80726-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="80726-110">A **Állapotfrissítés ideje** mező nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="80726-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="80726-111">A mező értéke egy időbélyeg, amely azt jelzi, hogy mikor történt az állapot utolsó frissítése.</span><span class="sxs-lookup"><span data-stu-id="80726-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="80726-112">Az **Ütemezés teljesítménye** és a **Költségteljesítmény** mezők a követési rácsról állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="80726-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="80726-113">Ha a gyökércsomópont ütemezése és költségvarianciája az **Erőfeszítés követése** nézetben pozitív, akkor ezek a mezők **Ütemterv előtt** értékre vannak beállítva.</span><span class="sxs-lookup"><span data-stu-id="80726-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="80726-114">Ha a gyökércsomópont ütemezése és költségeltérése negatív, akkor ezeket **Ütemterv mögött** értékre vannak beállítva.</span><span class="sxs-lookup"><span data-stu-id="80726-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
