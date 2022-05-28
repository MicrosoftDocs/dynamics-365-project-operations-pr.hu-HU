---
title: Project Operations telepítése – Lite
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazás telepítésével kapcsolatos információkat tartalmaz.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580735"
---
# <a name="deploy-project-operations---lite"></a>Project Operations telepítése – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_



A Project Operations több telepítési modellt támogat. A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.


> [!IMPORTANT]
> Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Dataverse-telepítését** eredményezi.

- [Projektműveletek telepítése új Dataverse környezetbe](#new)
- [Telepítés meglévő Dataverse környezetbe](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> A Project Operations telepítése új Dataverse környezetbe

1. [Project Operations licenccel rendelkező globális vagy Power Platform rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új Dataverse környezetet a [PowerPlatform Felügyeleti központban](https://admin.powerplatform.com). Győződjön meg arról, hogy **az adatbázis létrehozása ehhez a környezethez** és **a Dynamics 365-alkalmazásokhoz** engedélyezve van. További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Projektműveletek telepítése meglévő Dataverse környezetbe
1. Győződjön meg arról, hogy a környezet nincs konfigurálva kettős [írással](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), mivel a telepítés telepíti a [Project Operations for resource/non-stocked based scenarios](project-operations-integrated-deployment-overview.md) képességeket.
2. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
3. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
