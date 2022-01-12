---
title: Új környezet kiépítése
description: Ez a témakör az új Project Operations-környezet kialakításának módjával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a00426678d23000dc19386792d346318eab74ed9
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928664"
---
# <a name="provision-a-new-environment"></a>Új környezet kiépítése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ez a témakör arról tartalmaz tájékoztatást, hogyan építhet ki új Dynamics 365 Project Operations-környezetet erőforrás-/nem készletalapú forgatókönyvekhez.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Az automatizált Project Operations-kiépítés engedélyezése egy LCS-projektben

A következő lépésekkel engedélyezheti az automatizált Project Operations-kiépítést az LCS-projektjéhez.

1. Lépjen az [LCS](https://lcs.dynamics.com/v2) lehetőségre, és válassza az **Előnézeti funkció kezelése** csempét.
2. Az **Előzetes funkció** listában jelölje ki a **Project Operations funkció** lehetőséget, majd válassza az **Előzetes funkció engedélyezve** lehetőséget a Project Operations engedélyezéséhez.

   > [!NOTE]
   > Ez a lépés csak egy alkalommal hajtható végre LCS-projektenként.

## <a name="provision-a-project-operations-environment"></a>Project Operations-környezet kiépítése

1. Nyisson meg egy új Dynamics 365 Finance [bemutató környezet](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vagy [teszt-/éles környezet](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) telepítést. 
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

     ![Telepítés beállításai.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Válassza az **Elfogadom** lehetőséget a szolgáltatási feltételek elfogadásához, majd válassza a **Kész** lehetőséget a telepítési beállításokhoz való visszatéréshez.
    >
    >![Telepítési hozzájárulás.](./media/2DeploymentConsent.png)

7. Választható – Bemutató adatok alkalmazása a környezetre. Menjen a **Speciális beállítások** lehetőségre, válassza az **SQL Database konfiguráció testreszabása** lehetőséget, és állítsa be az **Alkalmazásadatbázis adathalmazának megadása** lehetőséget **Bemutató** lehetőségre.
8. Töltse ki a többi kötelező mezőt a varázslóban, és erősítse meg a telepítést. A környezet kiépítési ideje a környezet típusától függően eltér. A kiépítés akár hat óráig is eltarthat.

   A telepítés sikeres végrehajtása után a környezet **Telepített** állapottal jelenik meg.

9. A környezet sikeres telepítésének megerősítéséhez válassza a **Bejelentkezés** lehetőséget, majd a megerősítéshez jelentkezzen be a környezetbe.

    ![Környezet részletei.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>A Finance-környezet frissítéseinek alkalmazása.

A Project Operations egy Finance-környezetet igényel **10.0.13 (10.0.569.20009)** vagy újabb verziószámú alkalmazással.

Előfordulhat, hogy a Finance-környezetre minőségi frissítéseket kell alkalmaznia ahhoz, hogy ezt a verziót kapja.

1. A LCS **Környezet részletei** oldalán a **Rendelkezésre álló frissítések** területen válassza a **Frissítések megtekintése** lehetőséget.

    ![Frissítések megtekintése.](./media/5ViewUpdates.png)

2. A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.

    ![Csomag mentése.](./media/6SavePackage.png)

3. Kattintson az **Összes kiválasztása** elemre, majd válassza a **Csomag mentése** lehetőségre.

    ![Frissítések áttekintése és mentése.](./media/7ReviewAndSaveUpdates.png)

4. Adja meg a csomag nevét és leírását, majd kattintson a **Mentés** gombra. Az internetkapcsolattól függően ez a folyamat eltarthat egy ideig.

    ![Csomag feltöltése az Eszközök könyvtárba.](./media/8UploadPackageToAssetsLibrary.png)

5. A csomag mentése után válassza a **Kész** lehetőséget, és mentse a csomagot az LCS-projekt Eszközök könyvtárába.

   A csomag mentése és ellenőrzése ~15 percet is igénybe vehet.

6. A frissítés alkalmazásához keresse meg a **Környezet részletei** oldalt az LCS-ben, és válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.

    ![Környezetek karbantartása.](./media/9MaintainEnvironment.png)

7. A frissítések listájában jelölje ki a létrehozott csomagot, majd válassza az **Alkalmaz** lehetőséget.

    ![Frissítések alkalmazása.](./media/10ApplyUpdates.png)

   A környezet javítása eltarthat egy ideig. Miután befejeződött, a környezet visszatér egy telepített állapotba.

    ![Környezet telepítve.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Kettős írási kapcsolat létrehozása 

1. A LCS-projektben nyissa meg a **Környezet részletei** oldalt.
2. A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget.
3. A hivatkozás létrejöttét követően válassza ismét az **A CDS for Apps hivatkozása** lehetőséget. A rendszer átirányítja a kettős írásra a Finance-ben.

    ![A CDS for Apps hivatkozása.](./media/12LinktoCDS.png)

4. Válassza **Megoldás alkalmazása** lehetőséget az integrációba leképezni kívánt entitások eléréséhez.

    ![Megoldások alkalmazása.](./media/13ApplySolutions.png)

5. Válassza a mindkét megoldást: **Dynamics 365 Finance and Operations kettős írású entitásleképezés** és **Dynamics 365 Project Operations kettős írású entitásleképezése**, majd válassza az **Alkalmaz** lehetőséget.

    ![Megoldások megerősítése.](./media/14ConfirmSolutions.png)

    A megoldások alkalmazása után a kettős írási entitások alkalmazásra kerülnek a környezetre.

    ![Megoldások alkalmazása.](./media/15ApplyingSolutions.png)

    Az entitások alkalmazása után az összes elérhető leképezés megjelenik a környezetben.

    ![Kettős írású leképezések.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Az adatentitások frissítése a frissítés után

1. A Finance-ben nyissa meg az **Adatkezelés** munkaterületet.

    ![Adatkezelési munkaterület.](./media/16DataManagement.png)

2. Válassza ki a **Keretrendszer paraméterei** csempét.

    ![Keretrendszer paraméterei.](./media/17FrameworkParameters.png)

3. Az **Entitás beállításai** oldalon válassza az **Entitások listájának frissítése** lehetőséget.

    ![Entitáslista frissítése.](./media/18RefreshEntityList.png)

A frissítés megközelítőleg 20 percet vesz igénybe. A rendszer értesítést küld, amikor elkészült.

  ![Frissítés megerősítése.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>A Dataverse Project Operations biztonsági beállításainak frissítése

1. Menjen a Project Operations lehetőségre a Dataverse-környezetben. 
2. Válassza a **Beállítások** > **Biztonság** > **Biztonsági szerepkörök** elemet. 
3. A **Biztonsági szerepkörök** oldalon, a szerepkörök listájából válassza ki a **kettős írású alkalmazásfelhasználót**, majd válassza az **Egyéni entitások** fület.  
4. Ellenőrizze, hogy a szerepkörhöz **Olvasás** és **Hozzáfűzés** engedélyekkel rendelkezik-e a következő entitásokhoz:
      
      - **Pénznem árfolyamának típusa**
      - **Partnerek diagramja**
      - **Pénzügyi naptár**
      - **Főkönyv**
      - **Vállalat**
      - **Költség**

5. A biztonsági szerepkör frissítése után válassza a **Beállítások** > **Biztonság** > **Csoportok** lehetőséget, és válassza ki az alapértelmezett csoportot a **Helyi vállalattulajdonos** csoportnézetben.
6. Válassza a **Szerepkörök kezelése** lehetőséget, és ellenőrizze, hogy az alkalmazás **kettős írású alkalmazásfelhasználó** biztonsági jogosultsága érvényes-e erre a csoportra.

## <a name="run-project-operations-dual-write-maps"></a>Project Operations kettős írás leképezéseinek futtatása

1. A LCS-projektben nyissa meg a **Környezet részletei** oldalt.
2. A **Common Data Service-környezet információi** területen válassza az **A CDS for Apps hivatkozása** lehetőséget. Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.
3. Indítsa el a leképezéseket. További információért lásd: [Project Operations kettős írásos leképezésverziók](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Ellenőrizze, hogy a projekthez kapcsolódó leképezések mindegyike futó állapotban van.

    ![Minden leképezés fut.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigurációs adatok alkalmazása a Project Operations szolgáltatáshoz használható CDS rendszerben (nem kötelező)

Ha alkalmazott bemutató adatokat a Finance környezetre, tekintse meg a [Konfigurációs adatok beállítása és alkalmazása a Common Data Service szolgáltatásban a Project Operationshoz](resource-apply-pro-setup-config-data.md) cikket a bemutató adatok CDS-környezetre való alkalmazásához.


A Project Operations-környezet most már ki van alakítva, és konfigurálva van. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
