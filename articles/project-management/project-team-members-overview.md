---
title: Projektcsoporttagok
description: Ez a témakör a projektcsapattagok információinak, attribútumainak és ütemezésének kezelését ismerteti.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908229"
---
# <a name="project-team-members"></a><span data-ttu-id="b930d-103">Projektcsoporttagok</span><span class="sxs-lookup"><span data-stu-id="b930d-103">Project team members</span></span>

<span data-ttu-id="b930d-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="b930d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b930d-105">A projektcsapattagok azok a projektrésztvevők, akik végrehajtják a munkát a projekten.</span><span class="sxs-lookup"><span data-stu-id="b930d-105">Project team members are the project participants who complete the work on a project.</span></span> <span data-ttu-id="b930d-106">A csoporttagrács célja, hogy megadja olyan névvel rendelkező erőforrások listáját, akik elkötelezettek a tevékenységgel kapcsolatban, valamint olyan általános csapattagokat, akik helyőrzőként szolgálnak, és később kerülnek betöltésre.</span><span class="sxs-lookup"><span data-stu-id="b930d-106">The objective of the team member grid is to provide a list of named resources who are committed to the engagement, and generic team members who are place holder resources and will be staffed later.</span></span>

<span data-ttu-id="b930d-107">A csapattagok rácsából a projektmenedzser és a többi projektrésztvevő láthatja, hogy ki lett elkötelezve a projektre.</span><span class="sxs-lookup"><span data-stu-id="b930d-107">From the team member grid, the Project manager and the other project participants have the ability to see who has been committed to the project.</span></span> <span data-ttu-id="b930d-108">Emellett megtekinthetik a foglalásaik összefoglalását, a tervezett erőfeszítést és az egyes erőforrás-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="b930d-108">They can also view a summary of their bookings, planned effort, and individual resource assignments.</span></span> <span data-ttu-id="b930d-109">A csoporttagok rácsa lehetővé teszi, hogy a projektmenedzserek meghatározzák az általános csoporttagok erőforrás-követelményeit, és kezeljék a meglévő csoporttagok foglalásait.</span><span class="sxs-lookup"><span data-stu-id="b930d-109">The team member grid allows Project managers to define resource requirements for generic team members and manage the bookings of existing team members.</span></span>

<span data-ttu-id="b930d-110">A következő táblázat a projektcsoport egyik tagjának legfontosabb attribútumait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="b930d-110">The following table lists the key attributes of a project team member.</span></span>

| <span data-ttu-id="b930d-111">Mező neve</span><span class="sxs-lookup"><span data-stu-id="b930d-111">Field name</span></span>          | <span data-ttu-id="b930d-112">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="b930d-112">Description</span></span>                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b930d-113">Felosztási mód</span><span class="sxs-lookup"><span data-stu-id="b930d-113">Allocation method</span></span>        | <span data-ttu-id="b930d-114">Az erőforrások projekten való könyveléséhez használt felosztási módszer.</span><span class="sxs-lookup"><span data-stu-id="b930d-114">The allocation method used to book resources on the project.</span></span>                                                                         |
| <span data-ttu-id="b930d-115">Számlázási típus</span><span class="sxs-lookup"><span data-stu-id="b930d-115">Billing Type</span></span>             | <span data-ttu-id="b930d-116">Adja meg, hogy a csoporttag számlázhatóként van-e osztályozva.</span><span class="sxs-lookup"><span data-stu-id="b930d-116">Select whether the team member is classified as billable.</span></span>                                                                                                                                       |
| <span data-ttu-id="b930d-117">Lefoglalható erőforrás</span><span class="sxs-lookup"><span data-stu-id="b930d-117">Bookable Resource</span></span>        | <span data-ttu-id="b930d-118">Az általános erőforrás helyettesítésére kijelölt foglalható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b930d-118">The bookable resource selected to replace the generic resource.</span></span>                                                                                                                   |
| <span data-ttu-id="b930d-119">Törlési állapot</span><span class="sxs-lookup"><span data-stu-id="b930d-119">Delete Status</span></span>            | <span data-ttu-id="b930d-120">A csoporttag törlési állapotával nyomon követheti, hogy van-e a PSS-nek küldött törlési kérelem, illetve, hogy a PSS sikeresen visszaküldte-e a választ a várt időkereten belül.</span><span class="sxs-lookup"><span data-stu-id="b930d-120">The delete status of the team member to track if there is a delete request sent to PSS and whether PSS sends back response successfully and within the expected time window.</span></span> |
| <span data-ttu-id="b930d-121">Összes munkamennyiség (óra)</span><span class="sxs-lookup"><span data-stu-id="b930d-121">Total Effort (Hours)</span></span>     | <span data-ttu-id="b930d-122">A csoporttag feladatokkal kapcsolatos munkamennyiségének összege.</span><span class="sxs-lookup"><span data-stu-id="b930d-122">The sum of the team member's effort on their assignments.</span></span>                                                                                                                         |
| <span data-ttu-id="b930d-123">Befejezett munkamennyiség (óra)</span><span class="sxs-lookup"><span data-stu-id="b930d-123">Effort Completed (Hours)</span></span> | <span data-ttu-id="b930d-124">A csoporttag feladattal kapcsolatos elvégzett munkamennyiségének nyomon követése.</span><span class="sxs-lookup"><span data-stu-id="b930d-124">A tracking of the effort accomplished by the team member on their assignments.</span></span>                                                                                           |
| <span data-ttu-id="b930d-125">Hátralévő munkamennyiség (óra)</span><span class="sxs-lookup"><span data-stu-id="b930d-125">Effort Remaining (Hours)</span></span> | <span data-ttu-id="b930d-126">A csoporttag feladattal kapcsolatos, még el nem végzett munkamennyiségének nyomon követése.</span><span class="sxs-lookup"><span data-stu-id="b930d-126">A tracking of the effort not yet completed by the team member on their assignments.</span></span>                                                                                    |
| <span data-ttu-id="b930d-127">Befejezés</span><span class="sxs-lookup"><span data-stu-id="b930d-127">Finish</span></span>                   | <span data-ttu-id="b930d-128">Az erőforrás csoporttagságának befejező dátuma.</span><span class="sxs-lookup"><span data-stu-id="b930d-128">The resource team membership end date.</span></span>                                                                                                                                            |
| <span data-ttu-id="b930d-129">Véglegesen lefoglalt órák száma</span><span class="sxs-lookup"><span data-stu-id="b930d-129">Hard Booked Hours</span></span>        | <span data-ttu-id="b930d-130">A csoporttag véglegesen lefoglalt órái.</span><span class="sxs-lookup"><span data-stu-id="b930d-130">The hard booked hours of the team member.</span></span>                                                                                                                                                                |
| <span data-ttu-id="b930d-131">Pozíció neve</span><span class="sxs-lookup"><span data-stu-id="b930d-131">Position Name</span></span>            | <span data-ttu-id="b930d-132">Az általános erőforrás azonosítására használt név.</span><span class="sxs-lookup"><span data-stu-id="b930d-132">The name used to identify the generic resource.</span></span>                                                                                                                                   |
| <span data-ttu-id="b930d-133">Erőforrás-kezelő részleg</span><span class="sxs-lookup"><span data-stu-id="b930d-133">Resourcing Unit</span></span>          | <span data-ttu-id="b930d-134">A munkát végrehajtó erőforrás szervezeti egysége.</span><span class="sxs-lookup"><span data-stu-id="b930d-134">The organizational unit of the resource performing the work.</span></span>                                                                                                                      |
| <span data-ttu-id="b930d-135">Projekt jóváhagyója</span><span class="sxs-lookup"><span data-stu-id="b930d-135">Project Approver</span></span>         | <span data-ttu-id="b930d-136">Adja meg, hogy a csoporttag jóváhagyhatja-e az időt és a költségeket.</span><span class="sxs-lookup"><span data-stu-id="b930d-136">Select whether the team member can approve time and expenses.</span></span>                                                                                                                     |
| <span data-ttu-id="b930d-137">Szükséges óraszám</span><span class="sxs-lookup"><span data-stu-id="b930d-137">Required Hours</span></span>           | <span data-ttu-id="b930d-138">Csoporttag szükséges órái a csoporttagra vonatkozó követelményekből.</span><span class="sxs-lookup"><span data-stu-id="b930d-138">The required hours of the team member from team member requirement.</span></span>                                                                                                                       |
| <span data-ttu-id="b930d-139">Szerepkör</span><span class="sxs-lookup"><span data-stu-id="b930d-139">Role</span></span>                     | <span data-ttu-id="b930d-140">A csoport tagja által betöltött szerepkör.</span><span class="sxs-lookup"><span data-stu-id="b930d-140">The role the team member fills on this team.</span></span>                                                                                                                                |
| <span data-ttu-id="b930d-141">Pozíció leírása</span><span class="sxs-lookup"><span data-stu-id="b930d-141">Position Description</span></span>     | <span data-ttu-id="b930d-142">Adja meg a csoporttag szerepkörének leírását.</span><span class="sxs-lookup"><span data-stu-id="b930d-142">Enter a description of the role for this team member.</span></span>                                                                                                                             |
| <span data-ttu-id="b930d-143">Ideiglenesen lefoglalt órák száma</span><span class="sxs-lookup"><span data-stu-id="b930d-143">Soft Booked Hours</span></span>        | <span data-ttu-id="b930d-144">A csoporttag ideiglenesen lefoglalt órái.</span><span class="sxs-lookup"><span data-stu-id="b930d-144">The soft booked hours of the team member.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="b930d-145">Kezdet</span><span class="sxs-lookup"><span data-stu-id="b930d-145">Start</span></span>                    | <span data-ttu-id="b930d-146">Az erőforrás csoporttagságának kezdő dátuma.</span><span class="sxs-lookup"><span data-stu-id="b930d-146">The resource team membership start date.</span></span>                                                                                                                                          |

<span data-ttu-id="b930d-147">A csoporttagok rácsából a következő műveleteket hajthatja végre:</span><span class="sxs-lookup"><span data-stu-id="b930d-147">From the team member grid, the following actions can be taken:</span></span>

- <span data-ttu-id="b930d-148">**Foglalás**: A hibrid foglalási módszertant kihasználó szervezetek esetében a foglalási művelet lehetővé teszi, hogy a felhasználók egy elnevezett erőforrást foglaljanak le az általános csoporttag által előállított szükséges követelmények alapján.</span><span class="sxs-lookup"><span data-stu-id="b930d-148">**Book**: For organizations that execute leveraging the hybrid bookings methodology, the book action will allow users to book a named resource based on the require requirements generated from the generic team member</span></span>
- <span data-ttu-id="b930d-149">**Követelmény létrehozása**: Ez a művelet hozza létre a követelményt.</span><span class="sxs-lookup"><span data-stu-id="b930d-149">**Generate Requirement**: This action generates the requirement.</span></span>
- <span data-ttu-id="b930d-150">**Minta megadása**: Lehetővé teszi, hogy a projektmenedzserek részletes szinten módosítsák az erőforrás-szükségletet.</span><span class="sxs-lookup"><span data-stu-id="b930d-150">**Specify Pattern**: Allows project managers to adjust resource requirement contours at a granular level.</span></span> <span data-ttu-id="b930d-151">A projektmenedzserek a projekt konkrét igényeinek megfelelően módosíthatják azokat az eseteket, amikor az alapértelmezett elosztás nem megfelelő.</span><span class="sxs-lookup"><span data-stu-id="b930d-151">Project managers can adjust for the specific needs of the project in instances where the default distribution does not fit.</span></span>
- <span data-ttu-id="b930d-152">**Kérés elküldése**: A központi foglalási módszert alkalmazó szervezetek számára.</span><span class="sxs-lookup"><span data-stu-id="b930d-152">**Submit Request**: For organizations using the central bookings methodology.</span></span>
- <span data-ttu-id="b930d-153">**Szerkesztés**: A csoporttagok attribútumai szerkeszthetők, beleértve a szervezeti egységet, a szerepkört és a pozíció nevét.</span><span class="sxs-lookup"><span data-stu-id="b930d-153">**Edit**: Team member attributes can be edited including organizational unit, role, and position name.</span></span>
- <span data-ttu-id="b930d-154">**Lefoglalások megőrzése**: Amikor az erőforrások foglalását frissíteni kell, a foglalások megőrzése lehetővé teszi, hogy a projektmenedzser módosítsa a következőket:</span><span class="sxs-lookup"><span data-stu-id="b930d-154">**Maintain Bookings**: When resources bookings need to be updated, maintain bookings allow the Project manager to adjust the:</span></span>

    - <span data-ttu-id="b930d-155">Kezdet</span><span class="sxs-lookup"><span data-stu-id="b930d-155">Start</span></span>
    - <span data-ttu-id="b930d-156">End</span><span class="sxs-lookup"><span data-stu-id="b930d-156">End</span></span>
    - <span data-ttu-id="b930d-157">Teljes munkamennyiség elosztása</span><span class="sxs-lookup"><span data-stu-id="b930d-157">Total effort allocation</span></span>

- <span data-ttu-id="b930d-158">**Új**: Az erőforrások közvetlenül az ütemezésből való hozzáadásán túl a projektmenedzserek új névvel rendelkező vagy általános csoporttagokat vehet fel a csoporttagok rácsába.</span><span class="sxs-lookup"><span data-stu-id="b930d-158">**New**: In addition to adding resources directly from the schedule, Project managers can add new named or generic team members from the team member grid.</span></span>
- <span data-ttu-id="b930d-159">**Törlés**: Egy vagy több csoporttag kijelölésével a projektmenedzser törölheti azokat az erőforrásokat, akik már nem fognak részt venni a projektben.</span><span class="sxs-lookup"><span data-stu-id="b930d-159">**Delete**: By selecting one or many team members, the Project manager can delete resources who are no longer going to be participating on the project.</span></span> <span data-ttu-id="b930d-160">A csoporttagok törlésével az összes társított erőforrás-hozzárendelés is törlődik, és a meglévő foglalások visszavonhatók.</span><span class="sxs-lookup"><span data-stu-id="b930d-160">Deleting a team member will also delete all associated resource assignments and  cancel all existing bookings.</span></span>