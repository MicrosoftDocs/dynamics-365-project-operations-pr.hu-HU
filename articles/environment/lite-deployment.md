---
title: Project Operations Lite telepítés telepítése – ajánlattól proforma számlázásig
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazás telepítésével kapcsolatos információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077956"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a>Project Operations Lite telepítés telepítése – ajánlattól proforma számlázásig

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Project Operations több telepítési modellt támogat. A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.


> [!IMPORTANT]
> Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Common Data Service-telepítését** eredményezi.

- [A Project Operations telepítése új CDS-környezetbe](#new)
- [Telepítés meglévő CDS-környezetbe](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>A Project Operations telepítése új CDS-környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új CDS-környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com). Ellenőrizze, hogy a **CDS-adatbázis** és a **Dynamics 365-alkalmazások** engedélyezve vannak-e. További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365-alkalmazások telepítési listájából.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>A Project Operations telepítése meglévő CDS-környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
2. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365-alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](https://docs.microsoft.com/power-platform/admin/manage-apps).


