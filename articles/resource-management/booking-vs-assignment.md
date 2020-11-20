---
title: Foglalások és hozzárendelések
description: Ez a témakör információkat biztosít az erőforrás-foglalások és az erőforrás-hozzárendelések közötti különbségekről.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130221"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="d8de5-103">Foglalások és hozzárendelések</span><span class="sxs-lookup"><span data-stu-id="d8de5-103">Bookings vs assignments</span></span>

<span data-ttu-id="d8de5-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="d8de5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8de5-105">A foglalások a források nehéz vagy puha elosztása egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="d8de5-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="d8de5-106">A kemény foglalások felhasználják az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="d8de5-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="d8de5-107">A foglalások a csapatok szervezeti koncepcióit képviselik, így megismerhetik, hogyan vesznek részt az erőforrások különféle projektekben.</span><span class="sxs-lookup"><span data-stu-id="d8de5-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="d8de5-108">A Dynamics 365 Project Operations a foglalásokat projektszintű koncepcióként kezeli.</span><span class="sxs-lookup"><span data-stu-id="d8de5-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="d8de5-109">A foglalásoktó eltérően a hozzárendelések az erőforrások kötelezettségvállalásai a projekt feladataihoz a projekt ütemtervében.</span><span class="sxs-lookup"><span data-stu-id="d8de5-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="d8de5-110">Az erőforrások lehetnek megnevezettek vagy általánosak.</span><span class="sxs-lookup"><span data-stu-id="d8de5-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="d8de5-111">Az erőforráshoz tartozó foglalások összege általában egy vagy több tevékenységen belül megegyezik az erőforrás hozzárendeléseinek összegével.</span><span class="sxs-lookup"><span data-stu-id="d8de5-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="d8de5-112">A Project Operations azonban nem kényszeríti ezt a megállapodást.</span><span class="sxs-lookup"><span data-stu-id="d8de5-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="d8de5-113">Az **Egyeztetés** nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.</span><span class="sxs-lookup"><span data-stu-id="d8de5-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
