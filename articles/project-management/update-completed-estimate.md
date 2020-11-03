---
title: Befejezéskori költség becslésének frissítése
description: Ez a témakör a projektráfordítások leképezésének frissítéséről nyújt információt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078275"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="4ae0f-103">Befejezéskori költség becslésének frissítése</span><span class="sxs-lookup"><span data-stu-id="4ae0f-103">Update estimate at completion</span></span>

<span data-ttu-id="4ae0f-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="4ae0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ae0f-105">Általában a projektmenedzser felülvizsgálja a feladat eredeti becsléseit.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="4ae0f-106">A projekt újratervezése a projekt menedzserének a becslésről alkotott felfogása, a projekt jelenlegi helyzetére tekintettel.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="4ae0f-107">Nem javasoljuk azonban, hogy a projektvezetők megváltoztassák az alapszintet, mivel a projekt alapvonala a megállapított igazságforrást képviseli a projekt ütemterve és költségbecslése szempontjából, és a projekt összes érdekeltje egyetértett azzal.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="4ae0f-108">Kétféle módon tudja egy projektmenedzser újraprogramozni a feladatokat:</span><span class="sxs-lookup"><span data-stu-id="4ae0f-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="4ae0f-109">Felülbírálja a befejezésre vonatkozó becslés alapértelmezett értékét a feladattal kapcsolatos tényleges hátralévő erőfeszítések becslésével.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="4ae0f-110">A feladat valódi előrehaladásának új becslésével felülbírálja az alapértelmezett haladási százalékot.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="4ae0f-111">Ezeknek a megközelítéseknek a segítségével át kell számítani a feladat ETC-jét, a befejezéskori költség becslését és az előrehaladási százalékot, valamint a feladatra várható erőfeszítési varianciát.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="4ae0f-112">Az EAC, az ETC-t és az összefoglaló feladatok előrehaladási százalékát újraszámolja, és új leképezést ad az erőfeszítés varianciájára.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
