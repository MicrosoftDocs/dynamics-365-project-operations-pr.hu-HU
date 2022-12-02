---
title: Project Operations telepítése – Lite
description: Ez a cikk a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazás telepítésével kapcsolatos információkat tartalmaz.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930321"
---
# <a name="deploy-project-operations---lite"></a>Project Operations telepítése – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_



A Project Operations több telepítési modellt támogat. A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.


> [!IMPORTANT]
> Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Dataverse-telepítését** eredményezi.

- [A Project Operations telepítése új Dataverse-környezetbe](#new)
- [Telepítés meglévő Dataverse-környezetbe](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>A Project Operations telepítése új Dataverse-környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új Dataverse-környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com). Ügyeljen arra, hogy engedélyezve legyen az **Adatbázis létrehozása ehhez a környezethez** és a **Dynamics 365 alkalmazások**. További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>A Project Operations telepítése meglévő Dataverse-környezetbe
1. Gondoskodjon róla , hogy a környezet ne legyen konfigurálva [kettős írással](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), mivel ekkor a telepítés részeként telepítve lesznek a [Project Operations erőforrás-/nem készletalapú forgatókönyvek](project-operations-integrated-deployment-overview.md) képességek.
2. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
3. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
