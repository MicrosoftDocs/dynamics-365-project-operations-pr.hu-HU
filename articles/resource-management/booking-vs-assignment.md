---
title: Foglalások és hozzárendelések
description: Ez a témakör információkat biztosít az erőforrás-foglalások és az erőforrás-hozzárendelések közötti különbségekről.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077941"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="86400-103">Foglalások és hozzárendelések</span><span class="sxs-lookup"><span data-stu-id="86400-103">Bookings vs assignments</span></span>

<span data-ttu-id="86400-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="86400-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="86400-105">A foglalások a források nehéz vagy puha elosztása egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="86400-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="86400-106">A kemény foglalások felhasználják az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="86400-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="86400-107">A hozzárendelések az erőforrások hozzárendelése a projekt feladataihoz a projekt ütemtervében.</span><span class="sxs-lookup"><span data-stu-id="86400-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="86400-108">Az erőforrások valós vagy általános erőforrások lehetnek.</span><span class="sxs-lookup"><span data-stu-id="86400-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="86400-109">Ideális esetben a valós források esetében a foglalásoknak és a feladatoknak egyezniük kell, mert nem különböznek egymástól.</span><span class="sxs-lookup"><span data-stu-id="86400-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="86400-110">A Microsoft Dynamics Project Operations azonban nem hajtja végre ezt a megállapodást.</span><span class="sxs-lookup"><span data-stu-id="86400-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="86400-111">Az **Egyeztetés** nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.</span><span class="sxs-lookup"><span data-stu-id="86400-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
