---
title: Újdonságok és változások a Project Service Automation 3. verziójában – 2020 1. hullám
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 3. verziójában – 2020. 1. hullám.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752221"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="a2e7c-103">Újdonságok és változások a Project Service Automation 3-as verziójában – 2020 1. hullám</span><span class="sxs-lookup"><span data-stu-id="a2e7c-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="a2e7c-104">A témakör bemutatja a legfontosabb frissítés szempontjait a Project Service Automation (PSA) 3. x 2020 1. hullám legújabb verziójára történő átállás során.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="a2e7c-105">Időbejegyzés</span><span class="sxs-lookup"><span data-stu-id="a2e7c-105">Time entry</span></span>
<span data-ttu-id="a2e7c-106">Az időbevitel élménye bővítve lett, hogy az időbevitel több ügyfél-forgatókönyvre is kiterjedjen.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="a2e7c-107">Ez magában foglalja a bejegyzéstípusok hozzáadását is, amelyek adott viselkedést váltanak ki a **Időbevitel beállításai** mezőséma névben, amely **Időforrás** néven jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="a2e7c-108">Frissítéssel kapcsolatos megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a2e7c-108">Upgrade consideration</span></span>
<span data-ttu-id="a2e7c-109">A szolgáltatás támogatásához a PSA-ban lévő szerepkörök frissítve lettek, hogy új jogosultságokat tartalmazzanak.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="a2e7c-110">Ezek a jogosultságok olvasási hozzáférést biztosítanak az új **Időbevitel beállításai** entitásnak.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="a2e7c-111">Az időpontot naplózó felhasználóknak a meglévő szerepkörökön kívül meg kell adni az **Időbeviteli felhasználó** felhasználói szerepkört is.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="a2e7c-112">Ez a szerepkör tartalmazza az új funkciókat, és gondoskodik arról, hogy az időbejegyzés továbbra is működjön.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="a2e7c-113">Jelenleg meghosszabbított időbejegyzés-változások</span><span class="sxs-lookup"><span data-stu-id="a2e7c-113">Currently extended time entry changes</span></span>
<span data-ttu-id="a2e7c-114">Hogy ez a lehető legkevésbé befolyásolja az időbejegyzést jelenleg használó felhasználókat, ez a szerepkörmódosítás az egyetlen alapvető feltétele az időbejegyzés további használatának.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="a2e7c-115">Ha egyéni nézeteket vagy különálló időbeviteli élményeket hozott létre, akkor az **Időbevitel beállítása** mezőket a megfelelő PSA-értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="a2e7c-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
