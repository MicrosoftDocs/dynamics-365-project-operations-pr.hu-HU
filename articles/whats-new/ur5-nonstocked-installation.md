---
title: A Finance környezetben való Project Operations frissítése
description: Ez a témakör információt nyújt a Dynamics 365 Finance környezetben való Project Operations frissítéséről.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816628"
---
# <a name="update-project-operations-in-your-finance-environment"></a>A Finance környezetben való Project Operations frissítése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


Ez a témakör információt nyújt a Dynamics 365 Finance környezetben való Dynamics 365 Project Operations frissítéséről. A Project Operations Update 5 (UR5) lehetőségre való frissítéséhez három művelet szükséges:

- [A csomag importálása az előzetes verzió projektjébe](#import)
- [A frissítés telepítése](#apply)
- [Saját Dataverse környezet frissítése](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>A csomag importálása az LCS projektjébe

1. Bejelentkezés a [Lifecycle Services (LCS)](https://lcs.dynamics.com/) szolgáltatásba Projekttulajdonosként vagy Környezetkezelőként.
2. A Projektek listájából válassza az LCS projektjét.
3. A **Projekt** lap **Környezetek** csoportjában nyissa meg a frissíteni kívánt környezetet.
4. Erősítse meg, hogy a környezet működik. Ha nem indul el, indítsa el a környezetet.
5. A **Rendelkezésre álló frissítések** rész **Új kiadás** szakaszában válassza a **Frissítés megtekintése** lehetőséget a 10.0.15-ös frissítéshez.

![Frissítés gomb megtekintése](media/view-update.png)

6. A **Bináris frissítések** oldalon válassza a **Csomag mentése** lehetőséget.
7. A **Frissítések áttekintése és mentése** oldalon válassza a **Csomag mentése** lehetőséget.
8. A megnyíló **Csomag mentése az eszköztárba** ablaktáblán adja meg a csomag nevét, majd válassza a **Csomag mentése** lehetőséget.
9. Amikor az LCS befejezte a csomag mentését, a **Kész** gomb engedélyezve lesz. Válassza a **Kész** lehetőséget. Az LCS ellenőrzi a csomagot. Az ellenőrzés eltarthat néhány percig, de legfeljebb egy óráig.


## <a name="apply-the-package-update"></a><a name="apply"></a>Alkalmazza a csomag frissítését

1. Az LCS-ben, a **Környezet részletei** lapon válassza a **Karbantartás** > **Frissítések alkalmazása** lehetőséget.
2. Válassza ki a listában a korábban mentett csomagot, majd válassza az **Alkalmaz** lehetőséget.
3. A csomag telepítésének megerősítéséhez válassza az **Igen** lehetőséget.

![Csomagtelepítés megerősítése párbeszédpanel](media/confirm-package-deployment.png)

4. Az alkalmazás frissítésének megerősítéséhez válassza az **Igen** lehetőséget.

![Alkalmazásfrissítés megerősítése párbeszédpanel](media/confirm-application-update.png)

Elindul a telepítés és az alkalmazás frissítése. 

A **Környezet részletei** lapon, a jobb felső sarokban a környezet állapota **Szolgáltatás** állapotra frissül. Körülbelül két órán belül befejeződik a frissítés. Az alkalmazás kiadási információi **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** érékre, a környezet állapota pedig **Telepítve** értékre frissül.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Saját Dataverse környezet frissítése

1. Jelentkezzen be a [Power Platform felügyeleti központjába](https://admin.powerplatform.com/).
2. Keresse és nyissa meg a listában azt a környezetet, amelyet a Project Operations telepítéséhez használt.
3. A **Környezetek** lapon válassza az **Erőforrás** > **Dynamics 365 alkalmazások** lehetőséget.
4. Keresse meg a listán a **Microsoft Dynamics 365 Project Operations**, az **Állapot** oszlopban pedig válassza az **Elérhető frissítés** lehetőséget.
5. Jelölje be az **Elfogadom a szolgáltatási feltételeket** jelölőnégyzetet, majd válassza a **Frissítés** lehetőséget. A megoldás legújabb verziója kerül telepítésre.

A telepítés befejezését követően telepítve lesz a 4.5.0.134-es verzió.

## <a name="configure-new-features"></a>Új funkciók konfigurálása

### <a name="enable-dual-write-mapping"></a>Kettős írás leképezésének engedélyezése

A Finance and Dataverse környezetek frissítésének befejezése után engedélyezheti a kettős írás leképezéseket. Fejezze be az alábbi műveleteket a kettős írás leképezéseinek engedélyezéséhez.

- [A Customer Engagement környezet biztonsági beállításainak frissítése](#security)
- [Adatok frissítése entitásokban](#refresh)
- [A kettős írású leképezések frissítése és futtatása](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>A Dataverse környezet biztonsági beállításainak frissítése

Az entitások biztonsági jogosultságának alábbi frissítései az UR5-ös verzióra való frissítés részeként szükségesek.

1. A Dataverse környezetben válassza a **Beállítások** lehetőséget, és a **Rendszer** csoportban válassza a **Biztonság** lehetőséget.

![Dataverse-környezet beállításai](media/Picture21.png)

2. Válassza a **Biztonsági szerepkörök** lehetőséget.
3. A szerepkörök listájából válassza ki a **kettős írású alkalmazásfelhasználót**, majd válassza az **Egyéni entitások** fület. 
4. Ellenőrizze, hogy rendelkezik-e a szerepkörhöz **Olvasás** és **Hozzáfűzés** jogosultságokkal a következőhöz:

      - **Pénznem árfolyamának típusa**
      - **Partnerek diagramja** 
      - **Pénzügyi naptár** 
      - **Főkönyv**

5. A biztonsági szerepkör után menjen a **Beállítások** > **Biztonsági** > **Csoportok** lehetőségre. Ellenőrizze, hogy a **kettős írású alkalmazásfelhasználói** szerepkör alkalmazva van-e a csoportra. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Adatentitások frissítése a frissítésből

1. Nyissa meg a Finance környezetben az **Adatkezelés** munkaterületet, majd nyissa meg a **Keretrendszer paraméterei** oldalt.
2. Az **Entitásbeállítások** lapon válassza az **Entitáslista frissítése** lehetőséget.
3. Az entitás frissítésének megerősítéséhez válassza a **Bezárás** lehetőséget.

 > [!NOTE]
 > Ez a művelet körülbelül 20 percet vesz igénybe. A frissítés befejezéséről értesítést fog kapni.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Kettős írás leképezéseinek frissítése

1. Az **Adatkezelés** munkaterületen válassza a **Kettős írás** lehetőséget.
2. Válassza a **Megoldások alkalmazása** lehetőséget, jelölje ki mindkét megoldást a listában, majd válassza az **Alkalmaz** lehetőséget.
3. A **Kettős írás** lapon jelölje ki az alábbi táblákat, majd válassza a **Leállítás** lehetőséget.

    - **Project Operations integrációjának tényleges adatai (msdyn_actuals)**
    - **Project Operations integrációs projekt költségkategóriái (msdyn_expensecategories)**
    - **Project Operations integrációs tényleges projektköltségek exportálási entitása (msdyn_expenses)**

4. A **Tábla leképezési verziója** lapon alkalmazza a leképezés új verzióját mindhárom entitásra.
5. A **Kettős írás** lapon válassza a futtatás lehetőséget a leképezések újraindításához.
6. A leképezések listájában válassza ki a **Főkönyvi (msdyn_ledgers)** leképezés minden előfeltételét, majd jelölje ki a **Kezdeti szinkronizálás** jelölőnégyzetet. 
7. Válassza ki a **Kezdeti szinkronizálás fő eleme** mezőjében az **Finance and Operations alkalmazásokat**, majd válassza a **Futtatás** lehetőséget.
 
 ![Főkönyvi leképezés szinkronizálása](media/DW6.png)
 
