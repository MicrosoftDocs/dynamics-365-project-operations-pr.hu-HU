---
title: Bemutató beállítások és konfigurációs adatok alkalmazása – Lite
description: Ez a témakör a bemutató beállítás és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401266"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Bemutató beállítások és konfigurációs adatok alkalmazása a Project Operations alkalmazáshoz – Lite 

_**Lite telepítés – ajánlattól proforma számlázásig_

## <a name="prerequisites"></a>Előfeltételek

A konfiguráció megkezdése előtt rendelkeznie kell egy Common Data Service (CDS) környezettel, amelyet a Dynamics 365 Project Operations alkalmazáshoz létesítettek.


## <a name="instructions"></a>Útmutatások

1. Töltse le a [fő adatcsomagot](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Keresse meg a *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.
3. A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.
5. Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.
6. Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.
8. A 4. oldalon jelölje ki a *MasterAndSetupData* zip-fájlt a kicsomagolt *ProjOpsDemoDataSetupAndMaster - Integrated CMT* mappából.

![Zip-fájl](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.

![Adatok beolvasása](./media/5ImportData.png)

10. Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart. Az befejeződése után lépjen ki a CMT varázslóból. 
11. Ellenőrizze a szervezet adatait a következő 20 entitásban:

-   Pénznem
-   Fiók
-   Szervezeti egység
-   KAPCSOLATTARTÓ
-   Adócsoport
-   Ügyfélcsoport
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

![Importálás befejezése](./media/6CompleteImport.png)
