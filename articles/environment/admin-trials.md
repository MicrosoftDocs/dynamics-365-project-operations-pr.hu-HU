---
title: Regisztrálás a Project Operations próbaverziókra
description: Ez a témakör a Dynamics 365 Project Operations próbaverziójának telepítésével kapcsolatos információkat tartalmazza.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418460"
---
# <a name="sign-up-for-project-operations-trials"></a>Regisztrálás a Project Operations próbaverziókra 

_**A következőre vonatkozik:** Project Operations az erőforrás-/nem készletalapú forgatókönyvekhez, Lite központi telepítés – ajánlattól proforma számlázásig, illetve Project Operations a készlet-/termelésalapú forgatókönyvekhez_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ez a téma elmagyarázza, hogyan lehet előfizetni az előnézeti partnerajánlatra, és hogyan lehet telepíteni a Dynamics 365 Project Operations-környezetet.

Az új Project Operations próbaverzióval automatikusan telepítheti a három támogatott telepítési forgatókönyv bármelyikét egy kérdőív kitöltésével, amely javaslatot tesz a legjobb telepítési megközelítésre. Ez a témakör a következőkről nyújt tájékoztatást:

- A próbaverzió-ajánlat beváltása.
- Üzembe helyezés kezdeményezése.
- Kettős írás beállítása.
- Tudjon meg többet a Project Operations-ről. 

Az alábbi táblázat az új próbaverzió-ajánlat részleteit ismerteti.

| **Ajánlat eleme**               | **Részletek**                                  |
|------------------------------|----------------------------------------------|
| Ajánlat típusa                   | Ez az ajánlattípus Admin lead, így egy bérlő adminisztrátor szükséges a beváltáshoz. |
| Ajánlat használata                    | Egyszeri alkalom bérlőnként                          |
| Az ajánlat időtartama               | 30 naptári nap                             |
| Beváltások bérlőnként       | 0                                            |
| Felhasználók száma              | 25                                           |
| Bővítmény                    | 1 hosszabbítás, 30 naptári nap               |
| A próbakörnyezetek száma | 3                                            |


## <a name="admin-trial-details"></a>Admin próba részletek
A következő táblázat a próbaidőszak részleteit és az egyes telepítési típusokra való alkalmazásukat sorolja fel.

| **Tétel**                      | **Lite**                                     | **Nem készletezett anyagok** | **Készletezett anyagok** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| A megadott beállítási adatok           | Igen                                          | Igen                       | Igen (USSI)            |
| Tranzakciós adatok            | No                                           | No                        | No                    |
| Üzembe helyezési idő percben  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Előfeltételek
A Dynamics 365 Project Operations próbaverziójának telepítéséhez a következő előfeltételek szükségesek.

- Regisztráljon a [Dynamics 365 Project Operations - előzetes próbaverziójára](https://www.aka.ms/try-po).
- Az előzetes verziót telepítő felhasználónak Azure-bérlői globális rendszergazdai jogosultsággal kell rendelkeznie.

> [!IMPORTANT]
> Egy szervezetben csak egy személynek, a bérlő rendszergazdának kell elvégeznie ezt a feladatot. Ha nem Ön ennek a kiadásnak az előfizetője, várjon, amíg a szervezete regisztrálva lesz, és megkapta a felhasználói hitelesítő adatokat.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Előzetes próbaverzió 

Mielőtt elkezdené, jelentkezzen be egy böngészőbe a felhasználói munkafiókkal abban a bérleményben, ahol a Project Operations előzetes verzióját szeretné használni.

1. Váltsa be az első ajánlati kódot, **Dynamics 365 Project Operations - Előzetes próbaverzió** a böngésző URL-címébe való beillesztésével.

    ![Ajánlat beváltása](./media/16RedeemFirstOfferNew.png)

2. Hagyja jóvá a megrendelést.

    ![Ellenőrizze a sorrendet](./media/17ConfirmOrderNew.png)

  Látni fogja, hogy a visszaigazoló ajánlatot sikeresen beváltotta.

   ![Jóváhagyás](./media/18OrderConfirmationNew.png)

  A rendszer átirányítja Önt a [Power Platform adminisztrációs központba](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Kérdőív és üzembe helyezés

1.  Menjen a [Power Platform adminisztrációs központba](https://admin.powerplatform.com/projectoperationstrial), és töltse ki a kérdőívet.  
2.  Tekintse át az ajánlott telepítési típust, és válassza a **Beállítás kezdése** pontot az üzembe helyezés megkezdéséhez.
3.  Tekintse át a feltételeket, majd válassza a **Start** lehetőséget.

   Miután elindult az üzembe helyezés, a rendszer átirányítja Önt a Power Platform admin központban található környezetlistára. Amíg az üzembe helyezés folyamatban van, a környezet állapota **PreparingInstance**.
 
  Az üzembe helyezés befejezése után a környezet állapota **Kész**.
 
4.  Ha az üzembe helyezés befejeződött, válassza ki a megfelelő Microsoft Dataverse URL-címet és a Finance and Operations alkalmazások URL-címét a telepítés érvényesítéséhez.

## <a name="demo-data-installation"></a>Demo adatok telepítése

Az alábbi linkeken keresztül elérheti a nem készletezett anyagok és a könnyű telepítési forgatókönyvek demó adatcsomagjait. 
- [Nem készletezett anyagok demó adatai](resource-apply-pro-setup-config-data.md)
- [Könnyű demo adatok](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Kettős írás beállítása
Kizárólag nem készletezett anyagok telepítése esetén konfigurálja a kettős írási hozzárendeléseket. További információért lásd: [Project Operations kettős írásos térképverziók](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Licencek hozzárendelése

A következő lépések végrehajtásához rendszergazdai hozzáféréssel kell rendelkeznie a szervezete Microsoft 365-portáljához.

1. Menjen a [Microsoft 365 admin központba](https://portal.office.com/), hogy hozzárendelje a licenceket a felhasználókhoz.

   ![Felügyeleti központ kezdőlapja](./media/14AdminPortal.png)

2. Az **Aktív felhasználók** oldalon jelölje ki azokat a felhasználókat, akikhez licencet szeretne rendelni.

   ![Licencek hozzárendelése](./media/15AssignLicenses.png)

3. Ellenőrizze, hogy a **Dynamics 365 Project Operations Előnézet** licenc van-e kiválasztva, majd válassza a **Módosítások mentése** lehetőséget.

## <a name="additional-resources"></a>További információforrások

Az alábbi források hasznos útmutatást nyújtanak a Project Operations-szal kapcsolatos munka megkezdéséhez:

- [Videósorozat - Project Operations áttekintés, funkciók részletezése és ütemterv](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [A telepítés típusának meghatározása](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Mi a helyzet, ha ALM vagy ELM szükséges a Finance and Operations alkalmazáskörnyezetemhez?

- Azon partnerek számára, akiknek teljes körű környezet-életciklus-kezelési képességekre van szükségük, tekintse meg a [Partner tesztkörnyezeti licenckérelmet](https://experience.dynamics.com/requestlicense) az új partneri ajánlat áttekintéséhez. 
- A belső felhasználási jogokról bővebb információt kereső partnerek számára lásd: [Belső felhasználási jogok felhő- és szoftverelőny (microsoft.com](https://partner.microsoft.com/membership/internal-use-software)).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Meghosszabbíthatom a próbaidőszakomat 30 napon túl?
A próbaidőszak meghosszabbításához hajtsa végre a következő lépéseket.

1. A **Microsoft 365 Admin Centerben** lépjen a **Számlázás**  > **Termékek** menüpontba.
2. Válassza ki a **Dynamics 365 Project Operations (CE) - Előzetes próbaverzió** elemet.
3. A **Lejárat dátuma** alatt válassza a **Dátum meghosszabbítása** lehetőséget.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Frissíthetek a lite telepítésről az erőforrás/nem készletezett alapú forgatókönyv telepítésre?
Jelenleg nincs támogatás arra, hogy egy környezetet lite-ról nem készletezett alapú telepítésre frissítsenek.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Hozzáférhetek a Lifecycle Services (LCS) szolgáltatáshoz a pénzügyi környezetemben?  
Szám Ezeknél a próbaverzióknál a telepítés a Power Platform Admin Center segítségével történik. A pénzügyi környezethez való hozzáférés korlátozott.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Telepíthetem a próbaverziómat egy meglévő környezetre?
Ha van már meglévő környezete, akkor a Power Platform Admin központból telepítheti a könnyű rendszert egy meglévő értékesítési Dataverse környezetre.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
