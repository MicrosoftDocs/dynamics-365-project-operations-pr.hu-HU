---
title: Új környezet kiépítése
description: Ez a témakör az új Project Operations-környezet kialakításának módjával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121176"
---
# <a name="provision-a-new-environment"></a>Új környezet kiépítése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör információt nyújt arról, hogyan lehet új Dynamics 365 Project Operations-környezetet létrehozni az erőforrás-/nem készletalapú forgatókönyvek esetén.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Az automatizált Project Operations-kiépítés engedélyezése egy LCS-projektben

A következő lépésekkel engedélyezheti az automatizált Project Operations-kiépítést az LCS-projektjéhez.

1. Lépjen az [LCS](https://lcs.dynamics.com/v2) lehetőségre, és válassza az **Előnézeti funkció kezelése** csempét.
2. Az **Előzetes funkció** listában jelölje ki a **Project Operations funkció** lehetőséget, majd válassza az **Előzetes funkció engedélyezve** lehetőséget a Project Operations engedélyezéséhez.

> [!NOTE]
> Ez a lépés csak egy alkalommal hajtható végre LCS-projektenként.

## <a name="provision-a-project-operations-environment"></a>Project Operations-környezet kiépítése

1. Nyisson meg egy új Dynamics 365 Finance [bemutató környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vagy [teszt-/éles környezet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) telepítést. 
2. Haladjon végig a **Környezet kiépítése** varázslón. 

> [!IMPORTANT]
> Ügyeljen arra, hogy a kijelölt alkalmazás verziója 10.0.13 vagy magasabb legyen.

3. A Project Operations kiépítéséhez az **Speciális beállítások** területen válassza a **Common Data Service** lehetőséget. 
4. Engedélyezze a **Common Data Service beállítást** az **Igen** kiválasztásával, majd adja meg az adatokat a kötelező mezőkben:

  - Adatfolyam neve
  - Régió
  - Nyelv
  - Pénznem
 
5. A **Common Data Service-sablon** mezőben jelölje ki a **Project Operations** lehetőséget. 

6. Válassza ki a telepítésének környezettípusát. Az előfizetésen alapuló próbaverzió 30 napig teszi lehetővé a CDS-környezet telepítését. 

![Telepítés beállításai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Válassza az **Elfogadom** lehetőséget a szolgáltatási feltételek elfogadásához, majd válassza a **Kész** lehetőséget a telepítési beállításokhoz való visszatéréshez.

![Telepítési hozzájárulás](./media/2DeploymentConsent.png)

7. Töltse ki a többi kötelező mezőt a varázslóban, és erősítse meg a telepítést. A környezet kiépítési ideje a környezet típusától függően változik. A kiépítés akár hat óráig is eltarthat.

  A telepítés sikeres végrehajtása után a környezet **Telepített** állapottal jelenik meg.

8. A környezet sikeres telepítésének ellenőrzéséhez válassza a **Bejelentkezés** lehetőséget, és jelentkezzen be a környezetbe a megerősítéshez.

![A  környezetek részletei](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance bemutató adatainak alkalmazása (nem kötelező lépés)

A Project Operations Finance bemutató adatait a 10.0.13-as szervizkiadású felhőben szolgáltatott környezethez az [ebben a cikkben](resource-apply-finance-demo-data.md) leírtak szerint alkalmazhatja.

## <a name="apply-updates-to-the-finance-environment"></a>A Finance-környezet frissítéseinek alkalmazása.

A Project Operations egy Finance-környezetet igényel **10.0.13 (10.0.569.20009)** vagy újabb verziószámú alkalmazással.

Előfordulhat, hogy a Finance-környezetre minőségi frissítéseket kell alkalmaznia ahhoz, hogy ezt a verziót kapja.

1. A LCS **Környezet részletei** oldalán a **Rendelkezésre álló frissítések** területen válassza a **Frissítések megtekintése** lehetőséget.

![Frissítések megtekintése](./media/5ViewUpdates.png)

2. A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.

![Csomag mentése](./media/6SavePackage.png)

3. Kattintson az **Összes kiválasztása** elemre, majd válassza a **Csomag mentése** lehetőségre.

![Frissítések áttekintése és mentése](./media/7ReviewAndSaveUpdates.png)

4. Adja meg a csomag nevét és leírását, majd kattintson a **Mentés** gombra. Az internetkapcsolattól függően ez a folyamat eltarthat egy ideig.

![Csomag feltöltése az Eszközök könyvtárba](./media/8UploadPackageToAssetsLibrary.png)

5. A csomag mentése után válassza a **Kész** lehetőséget, és mentse a csomagot az LCS-projekt Eszközök könyvtárába.

A csomag mentése és ellenőrzése ~15 percet is igénybe vehet.

6. A frissítés alkalmazásához keresse meg a **Környezet részletei** oldalt az LCS-ben, és válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.

![Környezetek karbantartása](./media/9MaintainEnvironment.png)

7. A frissítések listájában jelölje ki a létrehozott csomagot, majd válassza az **Alkalmaz** lehetőséget.

![Frissítések alkalmazása](./media/10ApplyUpdates.png)

A környezet javítása eltarthat egy ideig. Miután befejeződött, a környezet visszatér egy telepített állapotba.

![Környezet telepítve](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Kettős írási kapcsolat létrehozása 

1. A LCS-projektben nyissa meg a **Környezet részletei** oldalt.
2. A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.
3. A hivatkozás létrejöttét követően válassza ismét az **A CDS for Apps hivatkozása** lehetőséget. A rendszer átirányítja a kettős írásra a Finance-ben.

![A CDS for Apps hivatkozása](./media/12LinktoCDS.png)

4. Válassza **Megoldás alkalmazása** lehetőséget az integrációba leképezni kívánt entitások eléréséhez.

![Megoldások alkalmazása](./media/13ApplySolutions.png)

5. Válassza ki a **Dynamics 365 Finance and Operations kettős írású entitások leképezése** és a **Dynamics 365 Project Operations kettős írású entitások leképezése** elemet, majd válassza az **Alkalmaz** lehetőséget.

![Megoldások megerősítése](./media/14ConfirmSolutions.png)

A megoldások alkalmazása után a kettős írási entitások alkalmazásra kerülnek a környezetre.

![Megoldások alkalmazása](./media/15ApplyingSolutions.png)

Az entitások alkalmazása után az összes elérhető leképezés megjelenik a környezetben.

![Kettős írású leképezések](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Az adatentitások frissítése a frissítés után

1. A Finance-ben nyissa meg az **Adatkezelés** munkaterületet.

![Adatkezelési munkaterület](./media/16DataManagement.png)

2. Válassza ki a **Keretrendszer paraméterei** csempét.

![Keretrendszer paraméterei](./media/17FrameworkParameters.png)

3. Az **Entitás beállításai** oldalon válassza az **Entitások listájának frissítése** lehetőséget.

![Entitáslista frissítése](./media/18RefreshEntityList.png)

A frissítés megközelítőleg 20 percet vesz igénybe. A rendszer értesítést küld, amikor elkészült.

![Frissítés megerősítése](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Project Operations kettős írás leképezéseinek futtatása

1. A LCS-projektben nyissa meg a **Környezet részletei** oldalt.
2. A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget. Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.
3. Indítsa el a leképezéseket következő táblázatban leírtak szerint. Ügyeljen arra, hogy a listában szereplő sorrendet kövesse.

| **Entitásleképezés** | **Entitás frissítése** | **Kezdeti szinkronizálás** | **Kezdeti szinkronizálás fő eleme** | **Előfeltételek futtatása** | **Előfeltételek kezdeti szinkronizálása** |
| --- | --- | --- | --- | --- | --- |
| **Az összes vállalat projekterőforrás-szerepkörei (bookableresourcecategories)** | Nincs | Igen | Common Data Service | Nincs | N. a. |
| **Jogi entitások (cdm\_companies)** | Nincs | Igen | Finance and Operations alkalmazások | Nincs | N. a. |
| **Projekttevékenységek integrációjának tényleges adatai (msdyn\_actuals)** | Nincs | Nincs | N. a. | Igen | Nincs |
| **Projektszerződéssorok (salesorderdetails)** | Nincs | Nincs | N. a. | Nincs | Nincs |
| **A projekt tranzakciókapcsolatainak integrációs entitása (msdyn\_transactionconnections)** | Nincs | Nincs | N. a. | Nincs | N. a. |
| **A Project Operations integráció szerződéssor-mérföldkövei (msdyn\_contractlinesscheduleofvalues)** | Nincs | Nincs | N. a. | Nincs | N. a. |
| **A Project Operations integrációs entitása kiadások becsléséhez (msdyn\_estimateslines)** | Nincs | Nincs | N. a. | Nincs | N. a. |
| **Project Operations integráció projektköltség-kategóriák exportálási entitása (msdyn\_expensecategories)** | Nincs | Nincs | N. a. | Nincs | N. a. |
| **Project Operations integráció projektkiadások exportálási entitása (msdyn\_expenses)** | Igen | Nincs | N. a. | Nincs | N. a. |
| **A Project Operations integrációs entitása órabecslésekhez (msdyn\_resourceassignments)** | Igen | Nincs | N. a. | Nincs | N. a. |


4. Az entitás frissítéséhez jelölje ki a leképezés nevét, majd válassza az **Entitások frissítése** lehetőséget. 


![Leképezés frissítése](./media/20RefreshMapping.png)

5. A frissítés befejeződése után futtassa a leképezést. A következő leképezés engedélyezése előtt ellenőrizze, hogy a táblázatban a leképezés **Fut** állapotban van-e. A nagy számú előfeltétellel rendelkező leképezések futtatása eltarthat egy ideig.

Az előfeltételekkel rendelkező leképezés futtatásához engedélyezze a **Kapcsolódó entitásleképezések megjelenítése** kapcsolót. Ha a táblázat azt jelzi, hogy az **Előfeltétel kezdeti szinkronizálása** értéke **Nem**, ellenőrizze, hogy a **Kezdeti szinkronizálás** jelző **Ki** állapotban van-e minden előfeltétel leképezés előtt, mielőtt futtatá azokat.

![Leképezés futtatása](./media/21RunMap.png)

6. Ellenőrizze, hogy a projekthez kapcsolódó leképezések mindegyike futó állapotban van.

![Minden leképezés fut](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható CDS rendszerben (nem kötelező)

Ha alkalmazott bemutató adatokat a Finance környezetre, tekintse meg a [Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban a Project Operationshoz](resource-apply-pro-setup-config-data.md) cikket a bemutató adatok CDS-környezetre való alkalmazásához.


A Project Operations-környezet most már ki van alakítva, és konfigurálva van. 
