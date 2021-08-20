---
title: A Feladat rácson való munka hibaelhárítása
description: A témakör a Feladat rácson való munkavégzéshez szükséges hibaelhárítási információkat írja le.
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989104"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>A Feladat rácson való munka hibaelhárítása 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A témakör azt ismerteti, hogyan tudja kijavítani a költségkezelés során esetleg felmerülő problémákat.

## <a name="enable-cookies"></a>Cookie-k engedélyezése

A Project Operations szolgáltatáshoz engedélyezni kell a külső gyártótól származó cookie-kat annak érdekében, hogy a munkalebontási struktúra elérhető legyen. Ha a külső gyártótól származó cookie-k nincsenek engedélyezve, a feladatok megjelenítése helyett egy üres oldal jelenik meg, amikor a **Projekt** lapon kijelöli a **Feladatok** fület.

![Üres fül jelenik meg, ha a külső gyártótól származó cookie-k nincsenek engedélyezve.](media/blankschedule.png)


### <a name="workaround"></a>Megoldás
A következő eljárások ismertetik, hogyan lehet frissíteni a böngésző beállítását a külső cookie-k engedélyezéséhez – Microsoft Edge vagy Google Chrome böngészőknél.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Nyissa meg az Edge böngészőt.
2. A jobb felső sarokban válassza a **három pont** (...), majd a **Beállítások** lehetőséget.
3. A **Cookie-k és a webjogosultságok** lehetőség alatt válassza a **Cookie-k és a webhelyadatok** lehetőséget.
4. Kapcsolja ki a **Külső gyártótól származó cookie-k blokkolása** lehetőséget.

#### <a name="google-chrome"></a>Google Chrome

1. Nyissa meg a Chrome böngészőt.
2. Kattintson a jobb felső sarokban levő három függőleges pontra, és válassza a **Beállítások** elemet.
3. Az **Adatvédelem és a biztonság** lehetőség alatt válassza a **Cookie-k és a egyéb webhelyadatok** lehetőséget.
4. Válassza a **Minden cookie engedélyezése** lehetőséget.

> [!IMPORTANT]
> Ha letiltja a harmadik fél cookie-kat, akkor az egyéb webhelyekről származó cookie-kat és webhelyadatokat letiltja a rendszer, még abban az esetben is, ha a webhely engedélyezett a kivételek listáján.

## <a name="pex-endpoint"></a>PEX-végpont

A Project Operations szolgáltatáshoz szükséges, hogy a projektparaméter a PEX végpontra hivatkozzon. A végpontnak kommunikálnia kell a munkalebontási struktúra megjelenítéséhez használt szolgáltatással. Ha a paraméter nincs engedélyezve, a következő hibaüzenet jelenik meg: „A projektparaméter érvénytelen”. 

### <a name="workaround"></a>Megoldás

1. Adja hozzá a **PEX végpont** mezőt a **Projektparaméterek** laphoz.
2. Azonosítsa a használt terméktípust. Ez az érték a PEX-végpont beállítása során van használva. A lekéréskor a terméktípus már definiálva van a PEX-végpontban. Tartsa meg ezt az értéket. 
   
    ![A projektparaméteren lévő PEX végpont mező.](media/pex-endpoint.png)

3. Frissítse a mezőt a következő értékkel: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`.

   
   | Terméktípus                         | Típus paraméter |
   |--------------------------------------|----------------|
   | Project for the Web az alapértelmezett szervezeten   | type=0         |
   | Project for the Web a CDS elnevezésű szervezeten | type=1         |
   | Project Operations                   | type=2         |
   
4. Távolítsa el a mezőt a **Projektparaméterek** oldalról.

## <a name="privileges-for-project-for-the-web"></a>Webes projekt jogosultságai

A Project Operations egy külső ütemezési szolgáltatásra támaszkodik. A szolgáltatáshoz a felhasználónak több szerepkörrel kell rendelkeznie ahhoz, hogy elolvashassa és írhasson a munkalebontási struktúrához kapcsolódó entitásokhoz. Ezekhez az entitásokhoz kapcsolódnak projektfeladatok, erőforrás-hozzárendelések és feladatfüggőségek. Ha egy felhasználó a **Feladatok** fül megnyitásakor nem tudja leképezni a munkalebontási struktúrát, annak valószínűleg az az oka, hogy a Project Operations projektje még nincs engedélyezve. A felhasználónak egy biztonsági szerepkör hibát vagy egy hozzáférésmegtagadási hibát kell kapnia.


## <a name="workaround"></a>Megoldás

1. Menjen a **Beállítások > Biztonság > Felhasználók > Alkalmazásfelhasználók** lehetőségre.  

   ![Alkalmazásolvasó.](media/applicationuser.jpg)
   
2. Kattintson duplán az alkalmazás felhasználói bejegyzésére a következő jóváhagyásához:

 - A felhasználó hozzáféréssel rendelkezik a projekthez. Az ellenőrzés általában annak biztosításával történik, hogy a felhasználó **Projektmenedzser** biztonsági szerepkörrel rendelkezik.
 - A Microsoft Project alkalmazás felhasználója létezik, és megfelelően van konfigurálva.
 
3. Ha ez a felhasználó nem létezik, létrehozhat egy új felhasználói rekordot. **Új felhasználó** kijelölése. Módosítsa a bejegyzési űrlapot **Alkalmazás felhasználó** lehetőségre, majd adja meg az **Alkalmazásazonosító** értékét.

   ![Alkalmazás felhasználó részletei.](media/applicationuserdetails.jpg)

4. Ellenőrizze, hogy a felhasználóhoz a megfelelő licenc van-e hozzárendelve, és hogy a szolgáltatás engedélyezve van-e a licenc szolgáltatási terveiben.
5. Ellenőrizze, hogy a felhasználó meg tudja-e nyitni a project.microsoft.com webhelyet.
6. Ellenőrizze a projekt paraméterein keresztül, hogy a rendszer a megfelelő projektvégpontra mutat-e.
7. Ellenőrizze, hogy létrejött-e a projektalkalmazás felhasználója.
8. A következő biztonsági szerepköröket alkalmazza a felhasználóra:

  - Dataverse-felhasználó
  - A Project Operations rendszer
  - Projektrendszer

## <a name="error-when-updating-the-work-breakdown-structure"></a>Hiba a munkalebontási struktúra frissítésekor

Ha egy vagy több frissítést eszközölnek a munkalebontási struktúrában, akkor a változtatások sikertelenek lesznek, és nem kerülnek mentésre. Hiba történik az ütemezési rácsban, és „A legutóbbi módosításait nem lehet menteni” üzenetet fog kapni.

### <a name="workaround"></a>Megoldás

1. Ellenőrizze, hogy a felhasználóhoz a megfelelő licenc van-e hozzárendelve, és hogy a szolgáltatás engedélyezve van-e a licenc szolgáltatási terveiben.
2. Ellenőrizze, hogy a felhasználó meg tudja-e nyitni a project.microsoft.com webhelyet.
3. Ellenőrizze, hogy a rendszer a megfelelő projektvégpontra mutat-e.
4. Ellenőrizze, hogy létrejött-e a Projektalkalmazás felhasználója.
5. A következő biztonsági szerepköröket alkalmazza a felhasználóra:
  
  - Dataverse felhasználó vagy Alapfelhasználó
  - A Project Operations rendszer
  - Projektrendszer
  - A Project Operations kettős írási rendszere (Ez a szerepkör akkor szükséges, ha Project Operations erőforrását/nem készleten alapuló forgatókönyvét telepíti.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
