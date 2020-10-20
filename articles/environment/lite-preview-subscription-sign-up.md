---
title: Regisztráció az előzetes verziós előfizetésre
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948909"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Regisztrálás a Lite telepítés – ajánlattól proforma számlázásig előzetes verziós előfizetésére

Ez a témakör a Dynamics 365 Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra előzetes verziós partnerajánlatára való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.

> [!NOTE]
> Ez a folyamat a Project Operations következő kiadásaiban változni fog.

## <a name="prerequisites"></a>Előfeltételek

- Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban. Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.
- Az előzetes verziót telepítő felhasználónak meg kell adnia egy telefonszámot és egy érvényes hitelkártyát. A regisztráció során hat hónapig nem terheljük meg a kártyát. Hat hónap elteltével le kell mondania az előfizetést. 
- Tekintse át az összes általános szerződési feltételt.

## <a name="subscribe"></a>Feliratkozás

Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben két ajánlatot kap a Microsofttól. Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:

- Dynamics 365 Customer Service előzetes próbaverzió – egyszer használatos kód
- Dynamics 365 Project Operations – előzetes próbaverzió

### <a name="dynamics-365-customer-service-paid-offer"></a>Dynamics 365 Customer Service fizetett ajánlat

1. Privát/inkognitó böngésző használatával kiválthatja az első ajánlati kódot a Dynamics 365 Customer Service termékhez. A Customer Service alkalmazásra való regisztrációhoz a következők szükségesek:

- Egy telefonszám
- Egy hitelkártya. Amikor regisztrál, hat hónapig nem terheljük meg a kártyát. Hat hónap elteltével le kell mondania az előfizetést.
- Tekintse át az összes általános szerződési feltételt.

2. Adja meg a kapcsolattartási adatait.

![Kapcsolatinformáció](./media/1ContactInformation.png)

3. Adja meg az új bérlő adatait.

![Felhasználói azonosító létrehozása](./media/2CreateUserID.png)

4. Igazolja a személyazonosságát, mentse az új felhasználói azonosítót, majd válassza a **Beállítás** lehetőséget.

![Adatok mentése](./media/3SaveInfo.png)

5. Végezze el a hitelkártya regisztrálását, és tekintse át az összes általános szerződési feltételt. 

![Hitelkártyaadatok kitöltése](./media/4CompleteCreditCard.png)

![Fizetés hitelkártyával](./media/5CreditCardCheckout.png)

![Megrendelés mentése](./media/6SaveOrder.png)

![Hitelkártya megerősítése](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>A Dynamics 365 Customer Service Enterprise ajánlat lemondása

A Dynamics 365 Customer Service Enterprise ajánlat hat hónapig ingyenes. Az ajánlat a hat hónapos időszak végén teljes áron megújítható. A megújítási dátum előtti lemondáshoz hajtsa végre az alábbi utasításokat. 

> [!NOTE]
> A lépések végrehajtása után a továbbiakban nem fogja tudni használni a Project Operations nyilvános előzetes verziós környezetet.

1. Nyissa meg a [Felügyeleti portált](https://admin.microsoft.com/), és a **Számlázás** alatt válassza ki a **Saját termékek** lehetőséget.

![Felügyeleti portál, Saját termékek oldal](./media/8AdminPortal.png)

2. Válassza a **Dynamics 365 Customer Service Enterprise ajánlat** lehetőséget.

![Előfizetés lemondása](./media/9CancelSubscription.png)

3. Válassza a **Beállítások** > **Műveletek** > **Előfizetés lemondása** lehetőséget.
4. Az **Előfizetés lemondása** űrlapon adja meg az adatokat a kötelező mezőkben.
5. Válassza a **Lemondás** > **Előfizetés** lehetőséget.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Előzetes próbaverzió

1. Váltsa ki a második ajánlatot, a Dynamics 365 Project Operations próbaverzióját az üdvözlő e-mailben megadott URL-címmel.

![2. ajánlat beváltása](./media/10RedeemOffer2.png)

2. Ellenőrizze, hogy olyan felhasználóként van-e bejelentkezve, aki ugyanahhoz a szervezethez tartozik, amely az első ajánlat kódjával előfizetett, majd folytassa az ajánlat beváltását. 
3. Válassza az **Igen, hozzáadás a fiókomhoz** lehetőséget.

![Hozzáadás a fiókhoz](./media/11AddToAccount.png)

![Kipróbálás most képernyő](./media/12TryNow.png)

![Megrendelés adatai](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Licencek hozzárendelése

> [!IMPORTANT]
> A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Office 365-portáljához.

1. Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.

![Felügyeleti központ kezdőlapja](./media/14AdminPortal.png)

2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.

![Licencek hozzárendelése](./media/15AssignLicenses.png)

3. Ellenőrizze, hogy a **Customer Service Enterprise** és a **Project operations** licenc ki van-e jelölve, majd válassza a **Módosítások mentése** lehetőséget.

## <a name="create-a-new-cds-environment"></a>Új CDS-környezet létrehozása

Építsen ki új Project Pperations CDS-telepítési környezetet a [CDS telepítési modell](lite-deployment.md) utasításait követve.

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-konfiguráció telepítése és a beállítási bemutató adatok alkalmazása

Telepítse a CDS-konfigurációt, és állítsa be a bemutató adatokat a következő témakör utasításait követve: [Bemutató beállítások és konfigurációs adatok alkalmazása](lite-apply-demo-setup-config-data.md).
