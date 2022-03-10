---
title: A Feladat rácson való munka hibaelhárítása
description: A témakör a Feladat rácson való munkavégzéshez szükséges hibaelhárítási információkat írja le.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547202"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>A Feladat rácson való munka hibaelhárítása 


_**A következőre érvényes:** Project Operations erőforrás / nem készletezett alapú forgatókönyvek, Lite telepítése – üzlet a proforma számlázáshoz, Project for the Web_

A Dynamics 365 Project Operations által használt feladatrács egy hosztolt iframe a Microsoft Dataverse-en belül. Ennek következtében a hitelesítés és az engedélyezés megfelelő működésének biztosításához specifikus követelményeknek kell teljesülniük. A témakör ismerteti a gyakori problémákat, amelyek hatással lehetnek a rács megjelenítésének képességére vagy a feladatok kezelésére a munkalebontási struktúrában (WBS).

A gyakori problémák a következők:

- A Feladat rács **Feladat** lapja üres.
- A projekt megnyitásakor nem töltődik be a projekt, és a felhasználói felület (UI) elakad a folyamatjelzőnél.
- A **Project for the Web** jogosultságok felügyelete.
- A feladatok létrehozásakor, frissítésekkor és törlésekor a rendszer nem menti a módosításokat.

## <a name="issue-the-task-tab-is-empty"></a>Probléma: A Feladat lap üres

### <a name="mitigation-1-enable-cookies"></a>1. megoldás: Cookie-k engedélyezése

A Project Operations alkalmazáshoz engedélyezni kell a külső cookie-k használatát a munkalebontási struktúra megjelenítéséhez. Ha a külső gyártótól származó cookie-k nincsenek engedélyezve, a feladatok megjelenítése helyett egy üres oldal jelenik meg, amikor a **Projekt** lapon kijelöli a **Feladatok** fület.

A következő eljárások ismertetik, hogyan lehet frissíteni a böngésző beállítását a külső cookie-k engedélyezéséhez – Microsoft Edge vagy Google Chrome böngészőknél.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Nyissa meg az Edge böngészőt.
2. A jobb felső sarokban válassza a **három pont** (...), majd a **Beállítások** lehetőséget.
3. A **Cookie-k és a webjogosultságok** lehetőség alatt válassza a **Cookie-k és a webhelyadatok** lehetőséget.
4. Kapcsolja ki a **Külső gyártótól származó cookie-k blokkolása** lehetőséget.
5. Frissítse a böngészőjét. 

#### <a name="google-chrome"></a>Google Chrome

1. Nyissa meg a Chrome böngészőt.
2. Kattintson a jobb felső sarokban levő három függőleges pontra, és válassza a **Beállítások** elemet.
3. Az **Adatvédelem és a biztonság** lehetőség alatt válassza a **Cookie-k és a egyéb webhelyadatok** lehetőséget.
4. Válassza a **Minden cookie engedélyezése** lehetőséget.
5. Frissítse a böngészőjét. 

> [!NOTE]
> Ha letiltja a harmadik fél cookie-kat, akkor az egyéb webhelyekről származó cookie-kat és webhelyadatokat letiltja a rendszer, még abban az esetben is, ha a webhely engedélyezett a kivételek listáján.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>2. megoldás: Annak ellenőrzése, hogy a PEX-végpont helyesen van-e konfigurálva

A Project Operations szolgáltatáshoz szükséges, hogy a projektparaméter a PEX végpontra hivatkozzon. A végpont szükséges a kommunikációhoz azzal a szolgáltatással, amely a munkalebontási struktúra megjelenítéséhez használatos. Ha a paraméter nincs engedélyezve, a következő hibaüzenet jelenik meg: „A projektparaméter érvénytelen”. A PEX-végpont frissítéséhez kövesse az alábbi lépéseket.

1. Adja hozzá a **PEX végpont** mezőt a **Projektparaméterek** laphoz.
2. Azonosítsa a használt terméktípust. Ez az érték a PEX-végpont beállítása során van használva. A lekéréskor a terméktípus már definiálva van a PEX-végpontban. Tartsa meg ezt az értéket.
3. Frissítse a mezőt a következő értékkel: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Az alábbi táblázat a terméktípus alapján használandó típusparamétert tartalmazza.

      | **Terméktípus**                     | **Típus paraméter** |
      |--------------------------------------|--------------------|
      | Project for the Web az alapértelmezett szervezeten   | type=0             |
      | Project for the Web a CDS elnevezésű szervezeten | type=1             |
      | Project Operations                   | type=2             |

4. Távolítsa el a mezőt a **Projektparaméterek** oldalról.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Probléma: Nem töltődik be a projekt, és a felhasználói felület elakad a betöltésjelzőnél

A hitelesítés céljából engedélyezni kell az előugró ablakokat a Feladat rács betöltéséhez. Ha az előugró ablakok nincsenek engedélyezve, a képernyő elakad a betöltésjelzőnél. Az alábbi ábra egy URL-címet mutat letiltott előugró ablak jelölőjével a címsorban, ennek következtében a betöltésjelző beakad miközben megpróbálja betölteni az oldalt. 

   ![Elakadt betöltésjelző és előugró ablakok blokkolása.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>1. megoldás: Előugró ablakok engedélyezése

Ha a projekt elakad a betöltésjelzőnél, lehetséges, hogy az előugró ablakok nincsenek engedélyezve.

#### <a name="microsoft-edge"></a>Microsoft Edge

Az előugró ablakok kétféleképpen engedélyezhetők a Microsoft Edge böngészőben.

1. A Microsoft Edge böngészőben válassza ki az értesítést a böngésző jobb felső sarkában.
2. Válassza az **Előugró ablakok és átirányítások engedélyezése mindig** az adott Dataverse környezethez.
 
     ![Blokkolt előugró ablakok ablak.](media/enablepopups.png)

Másik lehetőségként elvégezheti a következő lépéseket.

1. Nyissa meg az Edge böngészőt.
2. A jobb felső sarokban jelölje ki a **három pont** (...) szimbólumot, majd válassza a **Beállítások** > **Webhelyre vonatkozó jogosultságok** > **Előugró ablakok és átirányítások** lehetőséget.
3. Kapcsolja az **Előugró ablakok és átirányítások** kapcsolót ki az előugró ablakok blokkolásához, vagy kapcsolja be az előugró ablakok blokkolásához az eszközön.
4. Az előugró ablakok engedélyezése után frissítse a böngészőt. 

#### <a name="google-chrome"></a>Google Chrome
1. Nyissa meg a Chrome böngészőt.
2. Lépjen arra az oldalra, ahol az előugró ablakok le vannak tiltva.
3. Válassza a címsorban az **Előugró ablakok letiltva** lehetőséget.
4. Jelölje ki a megjeleníteni kívánt előugró ablak hivatkozását.
5. Az előugró ablakok engedélyezése után frissítse a böngészőt. 

> [!NOTE]
> Ha mindig látni kívánta a webhely előugró ablakát, válassza az **Előugró ablakok és átirányítások engedélyezése mindig az [site] webhelyen** lehetőséget, majd válassza a **Kész** lehetőséget.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>3. probléma: A Project for the Web jogosultságok felügyelete

A Project Operations egy külső ütemezési szolgáltatásra támaszkodik. A szolgáltatáshoz szükséges, hogy egy felhasználóhoz több szerepkör legyen hozzárendelve, így a felhasználók a WBS szolgáltatáshoz kapcsolódó entitásokat írhatják és olvashatják. Ezekhez az entitásokhoz kapcsolódnak projektfeladatok, erőforrás-hozzárendelések és feladatfüggőségek. Ha egy felhasználó nem tudja megjeleníteni a WBS-et a **Feladatok** lapra való navigáláskor, ennek oka valószínűleg az, hogy a **Projekt** a **Project Operations** alkalmazáshoz nincs engedélyezve. A felhasználónak egy biztonsági szerepkör hibát vagy egy hozzáférésmegtagadási hibát kell kapnia.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>1. megoldás: Az alkalmazás felhasználója és a végfelhasználó biztonsági szerepkörök ellenőrzése

1. Menjen a **Beállítások** > **Biztonság** > **Felhasználók** > **Alkalmazásfelhasználók** lehetőségre.  

   ![Alkalmazásolvasó.](media/applicationuser.jpg)
   
2. A következők ellenőrzéshez kattintson duplán az alkalmazásfelhasználó rekordjára:

     - A felhasználó hozzáféréssel rendelkezik a projekthez. Ehhez ellenőrizze, hogy a felhasználó rendelkezik-e a **Projektmenedzser** biztonsági szerepkörrel.
     - A Microsoft Project alkalmazás felhasználója létezik, és megfelelően van konfigurálva.
 
3. Ha a felhasználó nem létezik, hozzon létre új felhasználói rekordot. 
4. Válassza az **Új felhasználók** lehetőséget, módosítsa az entitás űrlapját **Alkalmazás felhasználója** értékre, majd adja hozzá az **Alkalmazásazonosítót**.

   ![Alkalmazás felhasználó részletei.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>4. probléma: A feladatok létrehozásakor, frissítésekkor és törlésekor a rendszer nem menti a módosításokat

A WBS egy vagy több frissítése esetén a változtatások sikertelenek, és nem kerülnek mentésre. Hiba történik az ütemezési rácsban, és a következő üzenet jelenik meg: "A legutóbbi változtatását nem sikerült menteni".

### <a name="mitigation-1-validate-the-license-assignment"></a>1. megoldás: A licenc hozzárendelésének ellenőrzése

1. Ellenőrizze, hogy a felhasználóhoz a megfelelő licenc van-e hozzárendelve, és hogy a szolgáltatás engedélyezve van-e a licenc szolgáltatási terveiben.  
2. Ellenőrizze, hogy a felhasználó meg tudja-e nyitni a **project.microsoft.com** webhelyet.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>2. megoldás: A Project alkalmazás felhasználójának ellenőrzése
1. Ellenőrizze, hogy létrejött-e a Project alkalmazás felhasználója.
2. A következő biztonsági szerepköröket alkalmazza a felhasználóra:
  
  - Dataverse felhasználó vagy Alapfelhasználó
  - A Project Operations rendszer
  - Projektrendszer
  - Project Operations kettős írási rendszer. Ez a szerepkör a Project Operations erőforrás-/nem készletalapú telepítésű forgatókönyvei esetén szükséges.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
