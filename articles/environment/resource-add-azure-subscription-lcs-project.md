---
title: Azure-előfizetés hozzáadása LCS-projekthez
description: Ez a témakör az Azure-előfizetésnek egy LCS-projekttel való összekapcsolásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 839c510838b0bccb718b8ca8a4f71a1c46e7ea3f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595915"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-előfizetés hozzáadása LCS-projekthez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A felhőalapú környezeteket meglévő Azure-előfizetések segítségével kell telepíteni. Ez a témakör bemutatja a meglévő Azure-előfizetésének egy LCS-projekttel való összekapcsolását. 

## <a name="grant-admin-consent"></a>Rendszergazdai jóváhagyás megadása

1. Az LCS-projektjében, a **Környezetek** részen válassza a **Microsoft Azure beállításai** lehetőséget.

![Microsoft Azure-beállítások.](./media/1MicrosoftAzureSettings.png)

2. A **Projekt beállításai** oldalon, az **Azure-összekötők** lapon válassza az **Engedélyezés** lehetőséget. Ez lehetővé teszi a környezetek telepítését ehhez a projekthez.

![Azure-összekötők.](./media/2AzureConnectors.png)

3. A rendszergazdai hozzájárulás biztosítása érdekében ismét válassza az **Engedélyezés** lehetőséget.

![Rendszergazdai jóváhagyás megadása.](./media/3GrantAdminConsent.png)

4. Fogadja el az engedélykérést.

![Engedélykérés elfogadása.](./media/4AcceptPermissionRequest.png)

Az engedélyezés most már kész. 

![Sikeres engedélyezés.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez

1. Ugorjon a [Microsoft Azure-számlázás](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) lehetőségre, és válassza ki az előfizetését. A Dynamics Deployment Services hozzáférést igényel ehhez az előfizetéshez, hogy képes legyen környezeteket telepíteni.

![Azure-előfizetés részletei.](./media/6AzureSubscription.png)

2. Válassza a navigációs ablak **Hozzáférés-vezérlés (IAM)** elemét, majd válassza a **Szerepkör-hozzárendelés hozzáadása** lehetőséget.
3. A jobb oldalon lévő csúszka kiválasztásával jelölje ki a **Közreműködő szerepkör** elemet, és a megjelenő listájában keresse meg és jelölje ki a **Dynamics Deployment Services** szolgáltatást. 
4. Válassza a **Mentés** parancsot.

![Hozzáférés az előfizetéshez.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Előfizetés-összekötő hozzáadása egy LCS-projekthez

1. Az LCS-projektjében a **Microsoft Azure beállításai** oldalon válassza a **Hozzáadás** lehetőséget új összekötő hozzáadásához.
2. Adja meg az Azure-előfizetés azonosítóját. Az Azure-előfizetésének azonosítóját az [Azure Portal](https://ms.portal.azure.com/) webhelyen, a képernyő bal alsó részén található **Beállítások** alatt találja.
3. Az **Azure Resource Manager használatának konfigurálása** mezőben válassza az **Igen** lehetőséget.
4. Ügyeljen arra, hogy az Azure-előfizetésének AAD bérlői tartománya megfeleljen a tartományt birtokló Azure-előfizetésnek, amelyet használ, és válassza a **Következő** lehetőséget.
5. A **Microsoft Azure beállítása** képernyőn válassza a **Tovább** lehetőséget a megerősítéshez. Ha a képernyőn hibaüzenet jelenik meg, akkor térjen vissza a témakör [Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez](#provide) szakaszához, és ellenőrizze, hogy az összes lépést végrehajtotta-e.
6. Töltse le az Azure felügyeleti tanúsítványt a számítógép egy helyi mappájába. Kérje meg az Azure előfizetés-rendszergazdát, hogy töltse fel a tanúsítványt az Azure felügyeleti portálra az előfizetés kiválasztásával és a **Beállítások** > **Felügyeleti tanúsítványok** pontra lépve. Ez a tanúsítvány teszi lehetővé, hogy a LCS az Ön nevében kommunikáljon az Azure-ral. Ezt a lépést kihagyhatja, ha a felhasználó hozzáféréssel rendelkezik az előfizetéshez.
7. Válassza a **Következő** lehetőséget.
8. Válassza ki a telepítendő Azure-régiót, és jelöljön ki egy olyan adatközpontot, amely közel van ahhoz a helyhez, ahol a rendszert használni kívánja.
9.  Válassza a **Kapcsolódás** lehetőséget.

Sikeresen kapcsolódott az Azure-előfizetéséhez. Most már üzembe helyezheti Dynamics 365 Finance felhőben üzemeltetett környezeteket.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
