---
title: Regisztráció az előzetes verziós előfizetésre – Lite
description: Ez a cikk arról nyújt tájékoztatást, hogyan lehet előfizetni és üzembe helyezni a Project Operations lite üzembe helyezését – foglalkozni a proforma számlázással.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921259"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Regisztráció az előzetes verziós előfizetésre – Lite 

Ez a cikk bemutatja, hogyan lehet előfizetni a próbaverziós ajánlatra, és hogyan helyezheti üzembe Dynamics 365 Project Operations a lite üzembe helyezését – hogyan kezelheti a proforma számlázást.

> [!NOTE]
> Ez a folyamat a Project Operations következő kiadásaiban változni fog.

## <a name="prerequisites"></a>Előfeltételek
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie. A bérlőt az első ajánlat beválátása során hozhatja létre.

> [!IMPORTANT]
> A szervezetnél csak egy személynek, a bérlői rendszergazdának kell elvégeznie ezt a feladatot. Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.
> 
> A próbaverziók a bérlőn és egyszer használhatók. Csak egyszer lehet futtatni a próbaverziót. Javasoljuk, hogy a próbaidőszak céljára hozzon létre új bérlőt.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations próbaverzió 

Mielőtt elkezdené, ügyeljen arra, hogy a felhasználó munkafiókjával jelentkezzen be a böngészőbe abban a bérlőben, ahol a Project Operations előzetes verzióját szeretné használni.

1. Menjen a [Project Operations próbaverzió](https://aka.ms/try-po) helyre az első ajánlati kód beváltásához, **Dynamics 365 Project Operations**.
2. Hagyja jóvá a megrendelést.

  Látni fogja, hogy a megerősítő ajánlat sikeresen be lett váltva.

## <a name="assign-licenses"></a>Licencek hozzárendelése

> [!IMPORTANT]
> A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.


1. [Microsoft 365 A felügyeleti központba kattintva](https://portal.office.com/) rendelje hozzá a licenceket a felhasználókhoz.
2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.
3. Ellenőrizze, hogy a **Dynamics 365 Project Operations** licenc ki legyen jelölve. 
4. Válassza a **Módosítások mentése** lehetőséget.

## <a name="create-a-new-dataverse-environment"></a>Új Dataverse-környezet létrehozása

1. Új Project Operations Dataverse üzembe helyezési környezetet hozhat létre az üzembe helyezési modellről szóló [Dataverse cikkben található utasításokat követve](lite-deployment.md). A környezet típusának kiválasztása esetén ügyeljen arra, hogy a **Próba (előfizetés alapú)** változatot használja.

  ![Új környezet.](./media/19CreateEnvironment.png)

2. Válassz a **Dynamics 365-alkalmazások engedélyezése** beállítást, és hagyja üresen az **Alkalmazások automatikus telepítése** jelölőnégyzetet.  
3. Válassza ki a **Mentés** gombot a környezet létrehozásához.

  ![Adatbázis hozzáadása.](./media/20CreateEnvironment1.png)

4. A környezet létrehozása után telepítse a **Microsoft Dynamics 365 Project Operations** megoldást. 

![Megoldás telepítése.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-konfiguráció telepítése és a beállítási bemutató adatok alkalmazása

Telepítse a CDS-konfigurációt, és állítsa be a bemutató adatait a bemutató beállítási és konfigurációs adatainak alkalmazása című cikkben található [utasításokat követve](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
