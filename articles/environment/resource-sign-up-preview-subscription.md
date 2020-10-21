---
title: Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információt nyújt arról, hogyan lehet regisztrálni és telepíteni a Dynamics 365 Project Operations alkalmazást erőforrás-/nem készletalapú forgatókönyvek esetén.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948912"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Regisztráció a Project Operations előzetes verziós előfizetésekre az erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör ismerteti, hogyan lehet előfizetni az előzetes verzióra/partnerajánlatra, és telepíteni a Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvek esetén.

## <a name="prerequisites"></a>Előfeltételek

- Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban. Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.
- A Finance-környezet telepítéséhez érvényes Azure-előfizetésre van szükség, amely környezetenként kerül számlázásra. A kezdéshez használhatja a szervezet meglévő előfizetését, vagy egy [Azure-próbaverziót](https://azure.microsoft.com/en-us/free/). A CDS-környezet korlátozott, 30 napos időszakra ingyenesen biztosítva lesz.

## <a name="subscribe"></a>Feliratkozás

Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben két ajánlatot kap a Microsofttól. Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:

- Dynamics 365 Project Operations – Előzetes próbaverzió
- Dynamics 365 for Finance and Operations előzetes próbaverzió.

> [!IMPORTANT]
> A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot. Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Előzetes próbaverzió

1. Váltsa ki az első ajánlatot, a **Dynamics 365 Project Operations próbaverzióját** az üdvözlő e-mailben megadott URL-címmel.

![Első ajánlat](./media/1FirstOffer.png)

2. Ellenőrizze, hogy olyan felhasználóként jelentkezett-e be, aki ahhoz a szervezethez tartozik, amely a szolgáltatásra elő fog fizetni.
3. Folytassa az ajánlat beváltását. 
4. Válassza az **Igen, hozzáadás a fiókomhoz** lehetőséget.

![Ajánlat beváltása](./media/2RedeemFirstOffer.png)

![Ajánlat megerősítése](./media/3ConfirmFirstOffer.png)

![Ajánlat beváltva](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance előzetes próbaverzió

Ismételje meg ugyanezeket a lépéseket az üdvözlő e-mailben szereplő második ajánlattal.

## <a name="assign-licenses"></a>Licencek hozzárendelése

> [!IMPORTANT]
> A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Office 365-portáljához.

1. Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.

![Office felügyeleti portál](./media/5OfficeAdminPortal.png)

2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.

![Licencek hozzárendelése](./media/6AssignLicenses.png)

3. Ellenőrizze, hogy a Project Operations licence ki van-e jelölve, majd válassza a **Módosítások mentése** lehetőséget. 

> [!NOTE]
> A Finance próbaverziójának ajánlatát nem kell felhasználóhoz rendelni.

## <a name="start-a-new-project-in-lcs"></a>Új projekt indítása LCS-ben

Hozzon létre egy új LCS-projektet a következő témakörben leírtak szerint: [Új projekt indítása LCS-ben](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure-előfizetés hozzáadása LCS-projekthez

A feladat végrehajtásához hajtsa végre a következő témakör lépéseit: [Azure-előfizetés hozzáadása LCS-projekthez](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>A Finance-bemutatókörnyezet telepítése a Project Operations erőforrás-/nem készletalapú forgatókönyvekhez alkalmazással

A telepítés végrehajtásához kövesse a következő témakör útmutatását: [Új környezet kiépítése](resource-provision-new-environment.md). Használja a [bemutatókörnyezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) telepítési típust az előzetes verzióhoz.

## <a name="install-cds-setup-and-configuration-data"></a>CDS beállításainak és konfigurációs adatainak telepítése

Telepítse a CDS beállításait és konfigurációs adatait a következő témakörben leírtak szerint: [Beállítás és konfigurációs adatok alkalmazása a Common Data Service rendszerben](resource-apply-pro-setup-config-data.md).

