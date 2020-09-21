---
title: Erőforrás-kezelési GYIK
description: Ez a témakör válaszokat ad az erőforrás-kezeléssel kapcsolatos gyakran feltett kérdésekre.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752277"
---
# <a name="resource-management-faq"></a><span data-ttu-id="b0c8a-103">Erőforrás-kezelési GYIK</span><span class="sxs-lookup"><span data-stu-id="b0c8a-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="b0c8a-104">Mi a különbség a csapat tagja és az erőforrás igény között?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="b0c8a-105">A projektcsoport tagjai hozzárendelhetők a feladatokhoz, lefoglalhatók vagy túlfoglalva, és jóváhagyóként állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="b0c8a-106">Erőforrásigény létezhet egy projektcsoport tagja nélkül, a keresletjegyzet tervezeteként.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="b0c8a-107">Mi a különbség a javasolt és a puha foglalású órák között?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="b0c8a-108">A javasolt órák és a puha foglalású órák eltérnek a láthatóságtól.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="b0c8a-109">A javasolt órák csak azoknak az erőforrás-kezelőknek és a projektmenedzsernek láthatók, akik erőforrás-igénylés alapján kezdeményezték a keresletet.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="b0c8a-110">A nem lefoglalt órák mindenki számára láthatóak, akik hozzáférhetnek az Ütemezési táblához.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="b0c8a-111">Hogyan láthatom a csoport erőforrásainak puhán lekötött óráit?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="b0c8a-112">A puha foglalást akkor lehet elvégezni, amikor egy erőforrás-igényt foglal le.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="b0c8a-113">Azok a források, amelyeket egy projektcsapatnál lefoglalnak, olyan csapattagként jelennek meg, akiknek kevés a lefoglalása.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="b0c8a-114">Megjelennek az Ütemezési táblán.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="b0c8a-115">Hogyan változtathatom meg a lefoglalt erőforrás (általános vagy megnevezett) szükséges óráit, valamint a kezdési és befejezési dátumát?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="b0c8a-116">Az erőforrások lefoglalása után válassza ki a **Foglalások karbantartása** elemet a szükséges módosítások elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="b0c8a-117">Milyen erőforrás-típusokat támogat a Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="b0c8a-118">**Felhasználó** és **Kapcsolat** az egyetlen erőforrás típusok támogatottak a Dynamics 365 Project Service Automation rendszerben.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="b0c8a-119">Bár lehet létrehozni más típusú erőforrások (például **Berendezések** és **Csoport**), nincs end-to-end használat támogatva.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="b0c8a-120">Mi a különbség a megbízás és a foglalás között?</span><span class="sxs-lookup"><span data-stu-id="b0c8a-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="b0c8a-121">A hozzárendelések az erőforrások hozzárendelése a projekt feladataihoz a projekt ütemtervében.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="b0c8a-122">Az erőforrások lehetnek valós vagy általános erőforrások.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="b0c8a-123">A foglalások a források nehéz vagy puha elosztása egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="b0c8a-124">A kemény foglalások felhasználják az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="b0c8a-125">Ideális esetben a valós források esetében a foglalásoknak és a feladatoknak egyezniük kell, mert nem különböznek egymástól.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="b0c8a-126">A PSA azonban nem hajtja végre ezt a megállapodást.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="b0c8a-127">Az egyeztetés nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.</span><span class="sxs-lookup"><span data-stu-id="b0c8a-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
