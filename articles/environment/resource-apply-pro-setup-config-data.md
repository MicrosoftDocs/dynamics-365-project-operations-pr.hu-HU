---
title: Konfigurációs adatok beállítása és alkalmazása a Microsoft Dataverse szolgáltatásban
description: Ez a cikk a konfigurációs adatok Project Operationsben való beállításáról és alkalmazásáról nyújt tájékoztatást.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230240"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_



## <a name="prerequisites"></a>Előfeltételek

Mielőtt elkezdené konfigurálni az adatokat a Microsoft Dataverse, a következő előfeltételeknek kell teljesülniük:

1.  Dataverse Környezet és Dynamics 365 Finance környezet kiépítése a Project Operations számára.
2.  A Dynamics 365 Finance jogi személy adatait megosztjuk a Dataverse környezettel. Ez azt jelenti, hogy a **Vállalat** entitása Dataverse a következő vállalati rekordokkal rendelkezik:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Beállítási és konfigurációs adatok telepítése

1. Töltse le, oldja fel, és csomagolja ki a [Beállítási és konfigurációs adatcsomagot](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Keresse meg a kibontott mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.
3. A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.

![Konfiguráció-áttelepítés.](./media/1ConfigurationMigration.png)

4. A CMT varázsló 2. oldalán jelölje ki az **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.
5. Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.
6. Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.

![Konfiguráció bejelentkezés.](./media/2ConfigurationSignin.png)

7. A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.
8. A 4. oldalon jelölje ki a *SampleSetupAndConfigData* zip-fájlt a kicsomagolt mappából.

![Zip-fájl kiválasztása.](./media/3ZipFile.png)

![Válasszon egy fájlt.](./media/4SelectAFile.png)

9. A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.

![Adatok beolvasása.](./media/5ImportData.png)

10. Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart. Az importálás befejeződése után lépjen ki a CMT varázslóból. 
11. Ellenőrizze a szervezet adatait a következő 26 entitásban:

  - Pénznem
  - Számlatükör
  - Pénzügyi naptár
  - Pénzváltásiárfolyam-típusok
  - Fizetésnap
  - Fizetési ütemezés
  - Fizetési feltételek
  - Szervezeti egység
  - Kapcsolat
  - Adócsoport
  - Ügyfélcsoport
  - Szállítói csoport
  - Kiszerelés
  - Egységcsoport
  - Árlista
  - Projektparaméter árlistája
  - Számlázási gyakoriság
  - Lefoglalható erőforrás kategóriája
  - Tranzakció kategóriája
  - Költségkategória
  - Szerepkörár
  - Tranzakciókategória ára
  - Jellemző
  - Lefoglalható erőforrás
  - Lefoglalható erőforrás kategóriatársítása
  - Lefoglalható erőforrás jellemzője

![Importálás befejezése.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>A Project Operations-konfigurációk frissítése

1. Navigáljon a CE-környezethez. Ezt megtalálhatja a [Power Platform felügyeleti központ](https://admin.powerplatform.microsoft.com/environments) megnyitásával, a környezet kiválasztásával és a **Környezet megnyitása** lehetőség kiválasztásával. 

![Környezet megnyitása.](./media/7OpenEnvironment.png)

2. Nyissa meg a **Projektek** > **Erőforrások** részt, és válassza az **Új** lehetőséget foglalható erőforrás létrehozásához a felhasználó számára.

![Lefoglalható erőforrások.](./media/8BookableResources.png)

3. Az **Általános** lapon válassza ki a rendszergazdai felhasználót. Ellenőrizze, hogy az időzóna megegyezik-e az Ön által használt időzónával. 

![Új foglalható erőforrás.](./media/9NewBookableResource.png)

4. Az **Ütemezés** lap **Vállalat** mezőjében válassza ki az **USPM** vállalatot, majd válassza a **Mentés** lehetőséget. 

![Ütemezés lap.](./media/10SchedulingTab.png)

5. Válassza a **Munkaórák** lapot.  

![Munkaidő.](./media/11WorkHours.png)

6. Kattintson duplán a naptár tetszőleges értékére, és válassza a **Szerkesztés** > **Minden esemény a sorozatban** lehetőséget. 

![Munkanaptár.](./media/12WorkCalendar.png)

7. Módosítsa a munkaidőt nyolc (8) órás munkanapra, a hétvégék munkavégzés nélküli napokra történő megjelölésével, és győződjön meg arról, hogy az időzóna megfelel az Ön időzónájának. 
8. Válassza a **Mentés és bezárás** lehetőséget.

![Naptár frissítése.](./media/13UpdateCalendar.png)

9. Nyissa meg a **Beállítások** > **Naptársablonok** részt, és válassza az **Új** lehetőséget.
 
 ![Naptársablonok.](./media/14CalendarTemplates.png)
 
 10. Adja meg a nevet, jelölje ki a létrehozott sablonerőforrást, majd válassza a **Mentés** lehetőséget. 
 
 ![Naptársablon mentése.](./media/15SaveCalendarTemplate.png)
 
 11. Nyissa meg a **Paraméterek** részt és kattintson duplán a rekordra. 
 
 ![Projektparaméterek.](./media/16ProjectParameters.png)
 
12. Frissítse a következő mezőket:

 - **Alapértelmezett vállalat**: USPM
 - **Alapértelmezett szervezeti egység** : Contoso Robotics Global
 - **Számlázási gyakoriság**: Hetedik és utolsó nap
 - **Munkaidősablon**: Váltson a létrehozott sablonra.

13. Válassza a **Mentés** parancsot. 

![Frissített projektparaméterek.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
