---
title: A Project Operations Lite üzembe helyezése
description: Ez a cikk a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazás telepítésével kapcsolatos információkat tartalmaz.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810981"
---
# <a name="deploy-project-operations-lite"></a>A Project Operations Lite üzembe helyezése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_



A Project Operations több telepítési modellt támogat. A legjobb telepítési modell meghatározásához tekintse meg a [Telepítési típusok](determine-deployment-type.md) című témakört.


> [!IMPORTANT]
> Ez a Lite telepítés – ajánlattól proforma számlázásig telepítés a **Project Operations csak Dataverse-telepítését** eredményezi.

- [A Project Operations telepítése új Dataverse-környezetbe](#new)
- [Telepítés meglévő Dataverse-környezetbe](#existing)
- [Telepítés olyan meglévő Dataverse környezetbe, amely kettős írási összetevőkkel rendelkezik](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> A Project Operations Lite telepítése új Dataverse környezetbe

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) hozzon létre egy új Dataverse-környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com). Ügyeljen arra, hogy engedélyezve legyen az **Adatbázis létrehozása ehhez a környezethez** és a **Dynamics 365 alkalmazások**. További információkért lásd: [Környezetek létrehozása és kezelése a Power Platform felügyeleti központban](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Válassza a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> A Project Operations Lite telepítése meglévő Dataverse környezetbe 
1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
1. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> A Project Operations Lite telepítése egy meglévő Dataverse környezetbe, ahol a kettős írási megoldások már jelen vannak

Ha továbbra is Egyszerűsített üzembe helyezési módban szeretné futtatni a Project Operations rendszert, kövesse az alábbi lépéseket:

1. Project Operations licenccel rendelkező [globális vagy Power Platform-rendszergazdaként](/power-platform/admin/global-service-administrators-can-administer-without-license) keresse meg a környezetet a [PowerPlatform felügyeleti központban](https://admin.powerplatform.com), ahol a projekteket telepíteni szeretné.
1. Telepítse a **Microsoft Dynamics 365 Project Operations** lehetőséget a Dynamics 365 alkalmazások telepítési listájából. További információ: [Dynamics 365-alkalmazások kezelése](/power-platform/admin/manage-apps).
1. Mivel a környezet kettős írási összetevőkkel rendelkezik, amelyek segítenek a telepített pénzügyi és üzemeltetési alkalmazások integrációjában, a Project Operations telepítése a Projecttel kapcsolatos adatok pénzügyi és üzemeltetési alkalmazásokba való integrálásához szükséges képességeket és bővítményeket is telepíti. Mivel a Project Operations Lite környezetben szeretné futtatni, ezeket az integrációs összetevőket el kell távolítani, mivel korlátozásokat és többletterhelést okoznak a Lite üzembe helyezési forgatókönyvekben. Manuálisan távolítsa el a Kettős írás **Dynamics 365 Project Operations és** a Kettős írási entitástérképek **Dynamics 365 Project Operations megoldásokat** az összetevők eltávolításához.
1. Nyissa meg a **Project Operations -> Beállítások -> paramétereit**. Nyissa meg a Projektparaméter **részletei lapot, és állítsa a**  **Megoldásfrissítési viselkedés** mezőt Csak **egyszerűsített értékre**. Ez biztosítja, hogy a Project Operations későbbi frissítései ne hozzák vissza az integrációs összetevőket a Project Operationsbe.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
