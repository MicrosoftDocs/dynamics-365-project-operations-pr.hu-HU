---
title: Project Operations telepítése – Lite
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazás telepítésével kapcsolatos információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642186"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="bbf00-103">Project Operations telepítése – Lite</span><span class="sxs-lookup"><span data-stu-id="bbf00-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="bbf00-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="bbf00-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bbf00-105">A Project Operations több telepítési modellt támogat.</span><span class="sxs-lookup"><span data-stu-id="bbf00-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="bbf00-106">A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.</span><span class="sxs-lookup"><span data-stu-id="bbf00-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="bbf00-107">Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Common Data Service-telepítését** eredményezi.</span><span class="sxs-lookup"><span data-stu-id="bbf00-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="bbf00-108">A Project Operations telepítése új CDS-környezetbe</span><span class="sxs-lookup"><span data-stu-id="bbf00-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="bbf00-109">Telepítés meglévő CDS-környezetbe</span><span class="sxs-lookup"><span data-stu-id="bbf00-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="bbf00-110">A Project Operations telepítése új CDS-környezetbe</span><span class="sxs-lookup"><span data-stu-id="bbf00-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="bbf00-111">Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új CDS-környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="bbf00-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="bbf00-112">Ellenőrizze, hogy a **CDS-adatbázis** és a **Dynamics 365-alkalmazások** engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="bbf00-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="bbf00-113">További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="bbf00-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="bbf00-114">Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.</span><span class="sxs-lookup"><span data-stu-id="bbf00-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="bbf00-115">A Project Operations telepítése meglévő CDS-környezetbe</span><span class="sxs-lookup"><span data-stu-id="bbf00-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="bbf00-116">Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="bbf00-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="bbf00-117">Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.</span><span class="sxs-lookup"><span data-stu-id="bbf00-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="bbf00-118">További információ: [Dynamics 365-alkalmazások kezelése](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="bbf00-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


