---
title: Foglalások és hozzárendelések
description: Ez a témakör információkat biztosít az erőforrás-foglalások és az erőforrás-hozzárendelések közötti különbségekről.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279906"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="a0fc6-103">Foglalások és hozzárendelések</span><span class="sxs-lookup"><span data-stu-id="a0fc6-103">Bookings vs assignments</span></span>

<span data-ttu-id="a0fc6-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="a0fc6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a0fc6-105">A foglalások a források nehéz vagy puha elosztása egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a0fc6-106">A kemény foglalások felhasználják az erőforrás kapacitását.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="a0fc6-107">A foglalások a csapatok szervezeti koncepcióit képviselik, így megismerhetik, hogyan vesznek részt az erőforrások különféle projektekben.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="a0fc6-108">A Dynamics 365 Project Operations a foglalásokat projektszintű fogalomnak tekinti.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="a0fc6-109">A foglalásoktó eltérően a hozzárendelések az erőforrások kötelezettségvállalásai a projekt feladataihoz a projekt ütemtervében.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a0fc6-110">Az erőforrások lehetnek megnevezettek vagy általánosak.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-110">The resources can be named or generic.</span></span>  <span data-ttu-id="a0fc6-111">Ha egy erőforrás-követelmény a projektfeladatok hozzárendeléseiből származik, a Project Operations az erőforrások hozzárendelésének ráfordítási eloszlásokat felhasználva építik az erőforrás-követelmény részleteinek részletezett részleteit.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="a0fc6-112">Az erőforrás-hozzárendelésekre való hivatkozás azonban nem tartható fenn.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="a0fc6-113">Az erőforrás-követelményekből származó foglalások frissítései nem frissítik az erőforrás-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="a0fc6-114">Az erőforráshoz tartozó foglalások összege általában egy vagy több tevékenységen belül megegyezik az erőforrás hozzárendeléseinek összegével.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="a0fc6-115">A Project Operations azonban nem kényszeríti ezt a megállapodást.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="a0fc6-116">Az **Egyeztetés** nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.</span><span class="sxs-lookup"><span data-stu-id="a0fc6-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]