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
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290092"
---
# <a name="deploy-project-operations---lite"></a>Project Operations telepítése – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

A Project Operations több telepítési modellt támogat. A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.


> [!IMPORTANT]
> Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Common Data Service-telepítését** eredményezi.

- [A Project Operations telepítése új CDS-környezetbe](#new)
- [Telepítés meglévő CDS-környezetbe](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>A Project Operations telepítése új CDS-környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új CDS-környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com). Ellenőrizze, hogy a **CDS-adatbázis** és a **Dynamics 365-alkalmazások** engedélyezve vannak-e. További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>A Project Operations telepítése meglévő CDS-környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
2. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]