---
title: Újdonságok és változások a Project Service Automation 3. verziójában – 2020 1. hullám
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 3. verziójában – 2020. 1. hullám.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150941"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="3267d-103">Újdonságok és változások a Project Service Automation 3-as verziójában – 2020 1. hullám</span><span class="sxs-lookup"><span data-stu-id="3267d-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3267d-104">A témakör bemutatja a legfontosabb frissítés szempontjait a Project Service Automation (PSA) 3. x 2020 1. hullám legújabb verziójára történő átállás során.</span><span class="sxs-lookup"><span data-stu-id="3267d-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="3267d-105">Időbejegyzés</span><span class="sxs-lookup"><span data-stu-id="3267d-105">Time entry</span></span>
<span data-ttu-id="3267d-106">Az időbevitel élménye bővítve lett, hogy az időbevitel több ügyfél-forgatókönyvre is kiterjedjen.</span><span class="sxs-lookup"><span data-stu-id="3267d-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="3267d-107">Ez magában foglalja a bejegyzéstípusok hozzáadását is, amelyek adott viselkedést váltanak ki a **Időbevitel beállításai** mezőséma névben, amely **Időforrás** néven jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="3267d-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="3267d-108">A funkció támogatása érdekében új megoldást adtunk hozzá, amelynek neve: Idő, költség, állapotkezelés és jóváhagyások (TESA).</span><span class="sxs-lookup"><span data-stu-id="3267d-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="3267d-109">Frissítéssel kapcsolatos megjegyzések</span><span class="sxs-lookup"><span data-stu-id="3267d-109">Upgrade consideration</span></span>
<span data-ttu-id="3267d-110">A szolgáltatás támogatásához a PSA-ban lévő szerepkörök frissítve lettek, hogy új jogosultságokat tartalmazzanak.</span><span class="sxs-lookup"><span data-stu-id="3267d-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="3267d-111">Ezek a jogosultságok olvasási hozzáférést biztosítanak az új **Időbevitel beállításai** entitásnak.</span><span class="sxs-lookup"><span data-stu-id="3267d-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="3267d-112">Az időpontot naplózó felhasználóknak a meglévő szerepkörökön kívül meg kell adni az **Időbeviteli felhasználó** felhasználói szerepkört is.</span><span class="sxs-lookup"><span data-stu-id="3267d-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="3267d-113">Ez a szerepkör tartalmazza az új funkciókat, és gondoskodik arról, hogy az időbejegyzés továbbra is működjön.</span><span class="sxs-lookup"><span data-stu-id="3267d-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="3267d-114">Emellett ha bármilyen egyéni alkalmazás-modullal rendelkezik, amely tartalmazza az időbejegyzés entitás összes űrlapját, akkor a modulból el kell távolítania a **TESA időbejegyzés gyorslétrehozási űrlapját**.</span><span class="sxs-lookup"><span data-stu-id="3267d-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="3267d-115">Jelenleg meghosszabbított időbejegyzés-változások</span><span class="sxs-lookup"><span data-stu-id="3267d-115">Currently extended time entry changes</span></span>
<span data-ttu-id="3267d-116">Hogy ez a lehető legkevésbé befolyásolja az időbejegyzést jelenleg használó felhasználókat, ez a szerepkörmódosítás az egyetlen alapvető feltétele az időbejegyzés további használatának.</span><span class="sxs-lookup"><span data-stu-id="3267d-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="3267d-117">Ha egyéni nézeteket vagy különálló időbeviteli élményeket hozott létre, akkor az **Időbevitel beállítása** mezőket a megfelelő PSA-értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="3267d-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
