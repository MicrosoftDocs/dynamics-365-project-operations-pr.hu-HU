---
title: Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk információt nyújt arról, hogyan lehet regisztrálni és telepíteni a Project Operations alkalmazást erőforrás-/nem készletalapú forgatókönyvek esetén.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920109"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_



Ez a cikk ismerteti, hogyan lehet előfizetni a próbaverziós ajánlatra, és hogyan lehet Project Operations környezetet telepíteni erőforrás-/nem készletalapú forgatókönyvekhez.

## <a name="prerequisites"></a>Előfeltételek
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie. A bérlőt az első ajánlat beválátása során hozhatja létre. 
- A Finance-környezet telepítéséhez érvényes Azure-előfizetésre van szükség, amely környezetenként kerül számlázásra. A kezdéshez használhatja a szervezet meglévő előfizetését, vagy egy [Azure-próbaverziót](https://azure.microsoft.com/free/). A CDS-környezet korlátozott, 30 napos időszakra ingyenesen biztosítva lesz.

> [!IMPORTANT]
> A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot. Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.
> 
> A próbaverziók a bérlőn és egyszer használhatók. Csak egyszer lehet futtatni a próbaverziót. Javasoljuk, hogy a próbaidőszak céljára hozzon létre új bérlőt.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - előzetes verziójú próbeverzió 

Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.

1. Váltsa be az első ajánlatkódot **Dynamics 365 Project Operations** itt [Project Operations próbaverzió](https://aka.ms/try-po).
2. Hagyja jóvá a megrendelést.

  A megerősítő ajánlatot sikeres beváltását láthatja.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance előnézeti próbaverzió

Menjen a [Dynamics 365 for Finance előzetesverzió kipróbálása](https://aka.ms/trypoche) helyre, és ismételje meg az előző szakasz lépéseit az ajánlattal, Iratkozzon fel a Felhőben szolgáltatott környezetre.  

## <a name="assign-licenses"></a>Licencek hozzárendelése

> [!IMPORTANT]
> A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.

1. Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.

2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.

3. Ellenőrizze, hogy a **Dynamics 365 Project Operations** licenc ki legyen jelölve, majd válassza a **Módosítások mentése** lehetőséget.

> [!NOTE]
> A Finance próbaverziójának ajánlatát nem kell felhasználóhoz rendelni.

## <a name="start-a-new-project-in-lcs"></a>Új projekt indítása LCS-ben

Hozzon létre egy új LCS-projektet a következő cikkben leírtak szerint: [Új projekt indítása LCS-ben](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-előfizetés hozzáadása LCS-projekthez

A feladat végrehajtásához hajtsa végre a következő cikk lépéseit: [Azure-előfizetés hozzáadása LCS-projekthez](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>A Finance-bemutatókörnyezet telepítése a Project Operations erőforrás-/nem készletalapú forgatókönyvekhez alkalmazással

A telepítés végrehajtásához kövesse a következő cikk útmutatását: [Új környezet kiépítése](resource-provision-new-environment.md). Használja a [bemutatókörnyezet](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) telepítési típust az előzetes verzióhoz. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS beállításainak és konfigurációs adatainak telepítése

Telepítse a CDS beállításait és konfigurációs adatait a következő cikkben leírtak szerint: [Beállítás és konfigurációs adatok alkalmazása a Common Data Service-rendszerben](resource-apply-pro-setup-config-data.md).
Ezt a lépést csak a Finance bemutatókörnyezet telepítése és a bemutatóadatok elkészülte után hajtsa végre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
