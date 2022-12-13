---
title: Bemutató beállítások és konfigurációs adatok alkalmazása – Lite
description: Ez a cikk a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811028"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Bemutató beállítások és konfigurációs adatok alkalmazása a Project Operations alkalmazáshoz – Lite 

_**Lite telepítés – ajánlattól proforma számlázásig_



## <a name="prerequisites"></a>Előfeltételek

A konfiguráció megkezdése előtt rendelkeznie kell egy Dataverse-környezettel, amelyet a Dynamics 365 Project Operations alkalmazáshoz létesítettek.


## <a name="instructions"></a>Utasítások

1. Töltse le a [telepítési adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Keresse meg a *ProjSamSampleSetupData – CE only CMT* nevű mappát, és futtassa a *DataMigrationUtility* végrehajtható fájlt.
1. A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.

    ![Konfiguráció-áttelepítés.](./media/1ConfigurationMigration.png)

1. A CMT varázsló 2. oldalán jelölje ki az **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.
1. Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.
1. Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.

   ![Konfiguráció bejelentkezés.](./media/2ConfigurationSignin.png)

1. A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.
1. A 4. lapon válassza ki a zip fájlt *SampleSetupAndConfigData* a ki nem csomagolt *ProjSamSampleSetupData - Csak CE CMT* mappából.

   ![Zip-fájl.](./media/3ZipFile.png)

   ![Válasszon egy fájlt.](./media/4SelectAFile.png)

1. A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.

   ![Adatok beolvasása.](./media/5ImportData.png)

1. Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart. Az befejeződése után lépjen ki a CMT varázslóból. 
1. Ellenőrizze a szervezet adatait a következő 18 entitásban:

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
