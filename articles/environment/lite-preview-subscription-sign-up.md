---
title: Regisztráció az előzetes verziós előfizetésre – Lite
description: Ez a cikk a Project Operations Lite telepítés – ajánlattól proforma számlázásig alkalmazásra való regisztrálással és annak telepítésével kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410036"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Regisztráció az előzetes verziós előfizetésre – Lite 

Ez a cikk ismerteti, hogyan lehet előfizetni a próbaverziós ajánlatra és kiépíteni a Dynamics 365 Project Operations egyszerű telepítését a proforma számlázás kezeléséhez.

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


1. Nyissa meg a [Microsoft 365 felügyeleti központot](https://portal.office.com/), és rendelje hozzá a licenceket a felhasználókhoz.
2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.
3. Ellenőrizze, hogy a **Dynamics 365 Project Operations** licenc ki legyen jelölve. 
4. Válassza a **Módosítások mentése** lehetőséget.

## <a name="create-a-new-dataverse-environment"></a>Új Dataverse-környezet létrehozása

1. Építsen ki új Project Operations Dataverse-telepítési környezetet a [Dataverse-telepítési modell](lite-deployment.md) cikk utasításait követve. A környezet típusának kiválasztása esetén ügyeljen arra, hogy a **Próba (előfizetés alapú)** változatot használja.

  ![Új környezet.](./media/19CreateEnvironment.png)

2. Válassz a **Dynamics 365-alkalmazások engedélyezése** beállítást, és hagyja üresen az **Alkalmazások automatikus telepítése** jelölőnégyzetet.  
3. Válassza ki a **Mentés** gombot a környezet létrehozásához.

  ![Adatbázis hozzáadása.](./media/20CreateEnvironment1.png)

4. A környezet létrehozása után telepítse a **Microsoft Dynamics 365 Project Operations** megoldást. 

![Megoldás telepítése.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Demóadatok beállítása

Állítsa be a bemutató adatokat a következő cikk utasításait követve: [Bemutató beállítások és konfigurációs adatok alkalmazása](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
