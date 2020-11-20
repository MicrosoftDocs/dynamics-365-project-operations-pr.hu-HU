---
title: Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban
description: Ez a témakör a beállításról és a konfigurációs adatok Project Operations rendszerben való alkalmazásáról tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401131"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="prerequisites"></a>Előfeltételek

Az adatok Common Data Service (CDS) felületén történő konfigurálásának megkezdése előtt a következő előfeltételeknek kell teljesülnie:

1.  CDS-környezet és Dynamics 365 Finance-környezet kiépítése a Project Operationshoz.
2.  A jogi személy adatait meg kell osztani a Dynamics 365 Finance-ből a CDS-környezetbe. Ez azt jelenti, hogy a **vállalat** entitás a CDS-ben a következő vállalati rekordokkal rendelkezik:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Beállítási és konfigurációs adatok telepítése

1. Töltse le, oldja fel, és csomagolja ki a [Beállítási és konfigurációs adatcsomagot](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Keresse meg a kibontott mappát, és futtassa a végrehajtható *DataMigrationUtility* fájlt.
3. A Common Data Service konfigurációáttelepítő (CMT) varázsló 1. oldalán válassza az **Adatok importálása** lehetőséget, majd válassza a **Folytatás** lehetőséget.

![Konfiguráció-áttelepítés](./media/1ConfigurationMigration.png)

4. A CMT varázsló 2. oldalán jelölje ki a **Microsoft 365** lehetőséget a **Telepítési típus** értékeként.
5. Jelölje be az **Elérhető szervezetek listájának megjelenítése** és a **Speciális megjelenítése** jelölőnégyzeteket.
6. Válassza ki a bérlő régióját, adja meg a hitelesítő adatait, majd válassza a **Bejelentkezés** lehetőséget.

![Konfiguráció bejelentkezés](./media/2ConfigurationSignin.png)

7. A 3. oldalon, a bérlő szervezeteinek listájából válassza ki azt a szervezetet, amelybe importálni szeretné a bemutató adatokat, és válassza a **Bejelentkezés** lehetőséget.
8. A 4. oldalon jelölje ki a *SampleSetupAndConfigData* zip-fájlt a kicsomagolt mappából.

![Zip-fájl kiválasztása](./media/3ZipFile.png)

![Jelöljön ki fájlt](./media/4SelectAFile.png)

9. A zip-fájl kijelölése után válassza az **Adatok importálása** lehetőséget.

![Adatok beolvasása](./media/5ImportData.png)

10. Az Importálás a hálózat sebességétől függően körülbelül két-tíz percig tart. Az importálás befejeződése után lépjen ki a CMT varázslóból. 
11. Ellenőrizze a szervezet adatait a következő 19 entitásban:

  - Pénznem
  - Szervezeti egység
  - KAPCSOLATTARTÓ
  - Adócsoport
  - Ügyfélcsoport
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

![Importálás befejezése](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>A Project Operations-konfigurációk frissítése

1. Navigáljon a CE-környezethez. Ezt megtalálhatja a [Power Platform felügyeleti központ](https://admin.powerplatform.microsoft.com/environments) megnyitásával, a környezet kiválasztásával és a **Környezet megnyitása** lehetőség kiválasztásával. 

![Környezet megnyitása](./media/7OpenEnvironment.png)

2. Nyissa meg a **Projektek** > **Erőforrások** részt, és válassza az **Új** lehetőséget foglalható erőforrás létrehozásához a felhasználó számára.

![Lefoglalható erőforrások](./media/8BookableResources.png)

3. Az **Általános** lapon válassza ki a rendszergazdai felhasználót. Ellenőrizze, hogy az időzóna megegyezik-e az Ön által használt időzónával. 

![Új foglalható erőforrás](./media/9NewBookableResource.png)

4. Az **Ütemezés** lap **Vállalat** mezőjében válassza ki az **USPM** vállalatot, majd válassza a **Mentés** lehetőséget. 

![Ütemezés lap](./media/10SchedulingTab.png)

5. Válassza a **Munkaórák** lapot.  

![Munkaórák](./media/11WorkHours.png)

6. Kattintson duplán a naptár tetszőleges értékére, és válassza a **Szerkesztés** > **Minden esemény a sorozatban** lehetőséget. 

![Munkanaptár](./media/12WorkCalendar.png)

7. Módosítsa a munkaidőt nyolc (8) órás munkanapra, a hétvégék munkavégzés nélküli napokra történő megjelölésével, és győződjön meg arról, hogy az időzóna megfelel az Ön időzónájának. 
8. Válassza a **Mentés és bezárás** lehetőséget.

![Naptár frissítése](./media/13UpdateCalendar.png)

9. Nyissa meg a **Beállítások** > **Naptársablonok** részt, és válassza az **Új** lehetőséget.
 
 ![Naptársablonok](./media/14CalendarTemplates.png)
 
 10. Adja meg a nevet, jelölje ki a létrehozott sablonerőforrást, majd válassza a **Mentés** lehetőséget. 
 
 ![Naptársablon mentése](./media/15SaveCalendarTemplate.png)
 
 11. Nyissa meg a **Paraméterek** részt és kattintson duplán a rekordra. 
 
 ![Projektparaméterek](./media/16ProjectParameters.png)
 
12. Frissítse a következő mezőket:

 - **Alapértelmezett vállalat**: USPM
 - **Alapértelmezett szervezeti egység** : Contoso Robotics Global
 - **Számlázási gyakoriság**: Hetedik és utolsó nap
 - **Munkaidősablon**: Váltson a létrehozott sablonra.

13. Válassza a **Mentés** parancsot. 

![Frissített projektparaméterek](./media/17UpdatedProjectParameters.png)
