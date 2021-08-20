---
title: Bemutató beállítások és konfigurációs adatok alkalmazása – Lite
description: Ez a témakör a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e25d358f1fd7705d580855d372d85690f6a5e265d3ba2b60fc26742bf3edc86f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993289"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Bemutató beállítások és konfigurációs adatok alkalmazása a Project Operations alkalmazáshoz – Lite 

_**Lite telepítés – ajánlattól proforma számlázásig_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Előfeltételek

A konfiguráció megkezdése előtt rendelkeznie kell egy Common Data Service (CDS) környezettel, amelyet a Dynamics 365 Project Operations alkalmazáshoz létesítettek.


## <a name="instructions"></a>Útmutatások

1. Töltse le a [fő adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Keresse meg a *ProjSamSampleSetupData – CE only CMT* nevű mappát, és futtassa a *DataMigrationUtility* végrehajtható fájlt.
3. A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.

    ![Konfiguráció-áttelepítés.](./media/1ConfigurationMigration.png)

4. A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.
5. Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.
6. Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.

   ![Konfiguráció bejelentkezés.](./media/2ConfigurationSignin.png)

7. A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.
8. A 4. lapon válassza ki a zip fájlt *SampleSetupAndConfigData* a ki nem csomagolt *ProjSamSampleSetupData - Csak CE CMT* mappából.

   ![Zip-fájl.](./media/3ZipFile.png)

   ![Válasszon egy fájlt.](./media/4SelectAFile.png)

9. A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.

   ![Adatok beolvasása.](./media/5ImportData.png)

10. Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart. Az befejeződése után lépjen ki a CMT varázslóból. 
11. Ellenőrizze a szervezet adatait a következő 18 entitásban:

    -   Pénznem
    -   Fiók
    -   Szervezeti egység
    -   Kapcsolat
    -   Kiszerelés
    -   Egységcsoport
    -   Árlista
    -   Projektparaméter árlistája 
    -   Számlázási gyakoriság
    -   Lefoglalható erőforrás kategóriája
    -   Tranzakció kategóriája
    -   Költségkategória
    -   Szerepkörár
    -   Tranzakciókategória ára
    -   Jellemző
    -   Lefoglalható erőforrás
    -   Lefoglalható erőforrás kategóriatársítása
    -   Lefoglalható erőforrás jellemzője

    ![Importálás befejezése.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
