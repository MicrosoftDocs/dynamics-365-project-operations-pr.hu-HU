---
title: Regisztráció az előzetes verziós előfizetésre – Lite
description: Ez a témakör a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997424"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Regisztráció az előzetes verziós előfizetésre – Lite 

Ez témakör ismerteti, hogyan lehet előfizetni az előzetes verziós partneri ajánlatra és a Dynamics 365 Project Operations Egyszerű központi telepítés – ajánlattól proforma számlázásig termékre.

> [!NOTE]
> Ez a folyamat a Project Operations következő kiadásaiban változni fog.

## <a name="prerequisites"></a>Előfeltételek

- Kapni fog egy e-mailt, amely meghívja, hogy részt vegyen az előzetes verzióban. Előzetes verziót kérhet a [Project Operations webhelyén](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.
- Tekintse át az összes általános szerződési feltételt.

## <a name="subscribe"></a>Feliratkozás

Amikor megkapja az [előzetes verzióra vonatkozó kérelem](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) jóváhagyását, e-mailben két ajánlatot kap a Microsofttól. Ez lehetővé teszi, hogy telepítse a Project Operations előzetes verzióját:

- Dynamics 365 Project Operations (CRM) – előzetes próbaverzió
- Office 365 Project Operations – Előzetes próbaverzió

> [!IMPORTANT]
> A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot. Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – előzetes próbaverzió 

Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.

1. Váltsa be az első ajánlat kódot, **Dynamics 365 Project Operations (CRM) – előzetes próbaverzió** a böngésző URL-címébe történő beillesztéssel.

![Ajánlat beváltása](./media/16RedeemFirstOfferNew.png)

2. Hagyja jóvá a megrendelést.
![Ellenőrizze a sorrendet](./media/17ConfirmOrderNew.png)

A megerősítő ajánlat sikeres beváltását láthatja.

![Jóváhagyás](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Előzetes próbaverzió

Ismételje meg ugyanazokat a lépéseket, mint az első ajánlatkóddal. Ügyeljen arra, hogy a második ajánlatkódot ugyanazzal a felhasználói fiókkal adja hozzá, amelyet az első ajánlatkódhoz használt.

## <a name="assign-licenses"></a>Licencek hozzárendelése

> [!IMPORTANT]
> A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.


1. Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.

![Felügyeleti központ kezdőlapja](./media/14AdminPortal.png)

2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.

![Licencek hozzárendelése](./media/15AssignLicenses.png)

3. Ellenőrizze, hogy ki vannak-e jelölve a **Dynamics 365 Project Operations (CRM) előzetes verzió** és az **Office 365 Project Operations – előzetes verzió** licencek. 
4. Válassza a **Módosítások mentése** lehetőséget.

## <a name="create-a-new-cds-environment"></a>Új CDS-környezet létrehozása

1. Építsen ki új Project Pperations CDS-telepítési környezetet a [CDS telepítési modell](lite-deployment.md) utasításait követve. A környezet típusának kiválasztása esetén ügyeljen arra, hogy a **Próba (előfizetés alapú)** változatot használja.
![Új környezet](./media/19CreateEnvironment.png)

2. Válassz a **Dynamics 365-alkalmazások engedélyezése** beállítást, és hagyja üresen az **Alkalmazások automatikus telepítése** jelölőnégyzetet.  
3. Válassza ki a **Mentés** gombot a környezet létrehozásához.

![Adatbázis hozzáadása](./media/20CreateEnvironment1.png)

4. A környezet létrehozása után telepítse a **Microsoft Dynamics 365 Project Operations** megoldást. 

![Megoldás telepítése](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-konfiguráció telepítése és a beállítási bemutató adatok alkalmazása

Telepítse a CDS-konfigurációt, és állítsa be a bemutató adatokat a következő témakör utasításait követve: [Bemutató beállítások és konfigurációs adatok alkalmazása](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]