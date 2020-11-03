---
title: Azure-előfizetés hozzáadása LCS-projekthez
description: Ez a témakör az Azure-előfizetésnek egy LCS-projekttel való összekapcsolásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077963"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Azure-előfizetés hozzáadása LCS-projekthez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A felhőalapú környezeteket meglévő Azure-előfizetések segítségével kell telepíteni. Ez a témakör bemutatja a meglévő Azure-előfizetésének egy LCS-projekttel való összekapcsolását. 

## <a name="grant-admin-consent"></a>Rendszergazdai jóváhagyás megadása

1. Az LCS-projektjében, a **Környezetek** részen válassza a **Microsoft Azure beállításai** lehetőséget.

![Microsoft Azure beállításai](./media/1MicrosoftAzureSettings.png)

2. A **Projekt beállításai** oldalon, az **Azure-összekötők** lapon válassza az **Engedélyezés** lehetőséget. Ez lehetővé teszi a környezetek telepítését ehhez a projekthez.

![Azure-összekötők](./media/2AzureConnectors.png)

3. A rendszergazdai hozzájárulás biztosítása érdekében ismét válassza az **Engedélyezés** lehetőséget.

![Rendszergazdai jóváhagyás megadása](./media/3GrantAdminConsent.png)

4. Fogadja el az engedélykérést.

![Engedélykérés elfogadása](./media/4AcceptPermissionRequest.png)

Az engedélyezés most már kész. 

![Sikeres engedélyezés](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez

1. Ugorjon a [Microsoft Azure-számlázás](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) lehetőségre, és válassza ki az előfizetését. A Dynamics Deployment Services hozzáférést igényel ehhez az előfizetéshez, hogy képes legyen környezeteket telepíteni.

![Azure előfizetési adatok](./media/6AzureSubscription.png)

2. Válassza a navigációs ablak **Hozzáférés-vezérlés (IAM)** elemét, majd válassza a **Szerepkör-hozzárendelés hozzáadása** lehetőséget.
3. A jobb oldalon lévő csúszka kiválasztásával jelölje ki a **Közreműködő szerepkör** elemet, és a megjelenő listájában keresse meg és jelölje ki a **Dynamics Deployment Services** szolgáltatást. 
4. Válassza a **Mentés** parancsot.

![Hozzáférés az előfizetéshez](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Előfizetés-összekötő hozzáadása egy LCS-projekthez

1. Az LCS-projektjében a **Microsoft Azure beállításai** oldalon válassza a **Hozzáadás** lehetőséget új összekötő hozzáadásához.
2. Adja meg az Azure-előfizetés azonosítóját. Az Azure-előfizetésének azonosítóját az [Azure Portal](https://ms.portal.azure.com/) webhelyen, a képernyő bal alsó részén található **Beállítások** alatt találja.
3. Az **Azure Resource Manager használatának konfigurálása** mezőben válassza az **Igen** lehetőséget.
4. Ügyeljen arra, hogy az Azure-előfizetésének AAD bérlői tartománya megfeleljen a tartományt birtokló Azure-előfizetésnek, amelyet használ, és válassza a **Következő** lehetőséget.
5. A **Microsoft Azure beállítása** képernyőn válassza a **Tovább** lehetőséget a megerősítéshez. Ha a képernyőn hibaüzenet jelenik meg, akkor térjen vissza a témakör [Hozzáférés biztosítása a Dynamics Deployment Services számára az Azure-előfizetéshez](#provide) szakaszához, és ellenőrizze, hogy az összes lépést végrehajtotta-e.
6. Töltse le az Azure felügyeleti tanúsítványt a számítógép egy helyi mappájába, majd töltse fel az Azure felügyeleti portálra a **Beállítások** > **Felügyeleti tanúsítványok** lehetőségről. Ez a tanúsítvány lehetővé teszi, hogy az LCS az Ön nevében kommunikáljon az Azure-ral. Ezt a lépést kihagyhatja, ha a felhasználó hozzáféréssel rendelkezik az előfizetéshez.
7. Válassza a **Következő** lehetőséget.
8. Válassza ki a telepítendő Azure-régiót, és jelöljön ki egy olyan adatközpontot, amely közel van ahhoz a helyhez, ahol a rendszert használni kívánja.
9.  Válassza a **Kapcsolódás** lehetőséget.

Sikeresen kapcsolódott az Azure-előfizetéséhez. Most már telepítheti a Dynamics 365 Finance felhőalapú környezeteit.


