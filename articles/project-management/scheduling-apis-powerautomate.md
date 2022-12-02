---
title: Projektütemezési API-k használata a Power Automate-tel
description: A cikk olyan mintafolyamatot tartalmaz, amely a Projekt ütemezés alkalmazásprogramozási felületeket (API-kat) használ.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404456"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projektütemezési API-k használata a Power Automate-tel

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A cikk egy olyan mintafolyamatot ismertet, amely bemutatja, hogyan lehet teljes projekttervet létrehozni a Microsoft Power Automate használatával, hogyan hozható létre művelethalmaz, illetve hogyan frissíthető egy entitás. A példa bemutatja, hogyan hozhat létre projektet, projektcsoport-tagokat, művelethalmazokat, projektfeladatokat és erőforrás-hozzárendeléseket. Ez a cikk azt is ismerteti, hogyan lehet frissíteni egy entitást, illetve végrehajtani egy művelethalmazt.

A következő felsorolásban azok a lépések teljes listája szerepel, amelyek dokumentálva vannak a cikk mintafolyamatában:

1. [PowerApps-trigger létrehozása](#1)
2. [Projekt létrehozása](#2)
3. [Változó inicializálása a csoporttaghoz](#3)
4. [Általános csoporttag létrehozása.](#4)
5. [Műveleti halmaz létrehozása](#5)
6. [Projektgyűjtő létrehozása](#6)
7. [Változó inicializálása a hivatkozás állapotához](#7)
8. [Változó inicializálása a feladatok számához](#8)
9. [Változó inicializálása a projektfeladat-azonosítóhoz](#9)
10. [Eddig végrehajtandó](#10)
11. [Projektfeladat beállítása](#11)
12. [Projektfeladat létrehozása](#12)
13. [Erőforrás-hozzárendelések létrehozása](#13)
14. [Egy változó értékének csökkentése](#14)
15. [Projektfeladat átnevezése](#15)
16. [Műveleti halmaz futtatása](#16)

## <a name="assumptions"></a>Feltételezések

A cikk feltételezi, hogy alapismeretekkel rendelkezik a Dataverse-platformról, a felhőfolyamatokról és a Projekt ütemezési alkalmazásprogramozási felületről (API). További információért tekintse meg a jelen témakör későbbi [Hivatkozások](#references) című szakaszát.

## <a name="create-a-flow"></a>Folyamat létrehozása

### <a name="select-an-environment"></a>Válasszon környezetet

Létrehozhatja a Power Automate-folyamatot a környezetében.

1. Nyissa meg a <https://flow.microsoft.com> weblapot, és jelentkezzen be a rendszergazdai hitelesítő adataival.
2. Válassza a jobb felső sarokban a **Környezetek** lehetőséget.
3. A listában jelölje ki azt a környezetet, ahol Dynamics 365 Project Operations telepítve van.

### <a name="create-a-solution"></a>Megoldás létrehozása

A következő lépésekkel hozhat létre ilyen [megoldásérzékeny folyamatokat](/power-automate/overview-solution-flows). Egy megoldásérzékeny folyamat létrehozásával sokkal könnyebben exportálhatja a folyamatot, hogy később használhassa.

1. Válassza a navigációs ablaktáblában található **Megoldás** elemet.
2. A **Megoldások** lapon válassza az **Új megoldás** lehetőséget.
3. Az **Új megoldás** párbeszédpanelen állítsa be a kötelező mezőket, majd kattintson az **Létrehozás** gombra.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Első lépés: Hozzon létre egy PowerApps-triggert

1. A **Megoládsok** oldalon válassza ki a létrehozott megoldást, majd válassza az **Új** lehetőséget.
2. A bal oldali ablaktáblában válassza a **Felhőfolyamatok** \> **Automatizálás** \> **Felhőfolyamat** \> **Azonnali** lehetőséget.
3. A **Folyamat neve** mezőben írja be a **Schedule API Demo Flow** értéket.
4. A **Válassza ki, hogyan aktiválja ezt a folyamatot** listában válassza a **Power Apps** lehetőséget. A Power Apps-trigger létrehozásakor a logikáról Ön, a szerző dönt. Ebben a cikkben a tesztelési célokból hagyja üresen a bemeneti paramétereket.
5. Válassza a **Létrehozás** parancsot.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. lépés: Projekt létrehozása

Kövesse az alábbi a lépéseket munkaprojekt létrehozásához.

1. A létrehozott felhasználói felületben válassza az **Új lépés** lehetőséget.

    ![Új lépés hozzáadása.](media/newstep.png)

2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.

    ![Egy művelet kiválasztása.](media/chooseactiontab.png)

3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.

![Egy lépés átnevezése.](media/renamestep.png)

4. Nevezze át a **Projekt létrehozása** lépést.
5. A **Művelet neve** mezőben válassza az **msdyn\_CreateProjectV1** lehetőséget .
6. Az **msdyn\_subject** mező alatt válassza a **Dinamikus tartalom hozzáadása** lehetőséget.
7. A **Kifejezés** lap függvénymezőjében írja be a **Project name – utcNow()** kifejezést.
8. Válassza az **OK** lehetőséget.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. lépés: Változó inicializálása a csoporttaghoz

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó inicializálása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Init team member** lépést.
5. A **Név** mezőbe írja be a **TeamMemberAction** szöveget.
6. A **Típus** mezőben válassza ki a **Sztring** lehetőséget.
7. Az **Érték** mezőben adja meg az **msdyn\_CreateTeamMemberV1** értéket.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. lépés: Általános csoporttag létrehozása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a **Csoporttag létrehozása** lépést.
5. A **Művelet neve** mezőben válassza a **TeamMemberAction** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.
6. A **Műveletparaméterek** mezőben adja meg a következő paraméterinformációkat.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Itt látható a paraméterek magyarázata:

    - **\@\@odata.type** – Az entitás neve. Például írja be a következőt: **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – A projekt csoportazonosítójának elsődleges kulcsa. Az érték egy globálisan egyedi azonosító (GUID) kifejezés.   Az azonosító a kifejezés lapról jön létre.

    - **msdyn\_project\@odata.bind** – A tulajdonos projekt projektazonosítója. Az érték a „Projekt létrehozása” lépés válaszának megfelelő dinamikus tartalom lesz. Ügyeljen arra, hogy a teljes elérési útat írja be, és adjon hozzá dinamikus tartalmat a zárójelek közé. Az idézőjelek kötelezőek. Például írja be a következőt: **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – A csoporttag neve. Például adja meg a következőt: **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5. lépés: Műveleti halmaz létrehozása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a **Műveleti halmaz létrehozása** lépést.
5. A **Művelet neve** mezőben jelölje ki a **msdyn\_CreateOperationSetV1** Dataverse egyéni műveletet.
6. Írja be a **Leírás** mezőbe a **ScheduleAPIDemoOperationSet** értéket.
7. A **Projekt** mezőbe írja be a következőt: **/msdyn\_projects(**.
8. A **Dinamikus tartalom** párbeszédpanelen válassza az **msdyn\_CreateProjectV1Response ProjectId** lehetőséget.
9. A **Projekt** mezőbe, írja be: **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. lépés: Projektgyűjtő létrehozása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be az **új sor hozzáadása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a **Gyűjtő létrehozása** lépést.
5. A **Táblanév** mezőben jelölje ki a **Projektgyűjtők** lehetőséget.
6. Írja be a **ScheduleAPIDemoBucket1** szöveget a **Név** mezőbe.
7. A **Projekt** mezőhöz válassza az **msdyn\_CreateProjectV1Response ProjectId** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. lépés: Változó inicializálása a hivatkozás állapotához

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó inicializálása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Init linkstatus** lépést.
5. A **Név** mezőbe írja be a **linkstatus** szöveget.
6. A **Típus** mezőben válassza ki az **Egész szám** lehetőséget.
7. Az **Érték** mezőbe írja be: **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. lépés Változó inicializálása a feladatok számához

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó inicializálása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a lépést az **Init number of tasks** lépést.
5. Írja be a **feladatok száma** szöveget a **Név** mezőbe.
6. A **Típus** mezőben válassza ki az **Egész szám** lehetőséget.
7. Az **Érték** mezőbe írja be: **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. lépés Változó inicializálása a projektfeladat-azonosítóhoz

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó inicializálása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Init ProjectTaskID** lépést.
5. Írja be a **feladatok száma** szöveget a **Név** mezőbe.
6. A **Típus** mezőben válassza ki a **Sztring** lehetőséget.
7. Az **Érték** mezőhöz írja be a **guid()** kifejezést a kifejezésszerkesztőbe.

## <a name="step-10-do-until"></a><a id="10"></a>10. lépést: Do Until

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **do until** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Állítsa be a feltételes utasításban az első értéket a **feladatok száma** változó számára a **Dinamikus tartalom** párbeszédpanelen.
4. Állítsa be a feltételt **kisebb vagy egyenlő** értékre.
5. Állítsa a feltételes utasítás második értékét **0**-ra .

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. lépés: Projektfeladat beállítása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó beállítása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Az új lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Projektfeleadat beállítása** lépést.
5. A **Név** mezőben, válassza az **msdyn\_projecttaskid** elemet.
6. Az **Érték** mezőhöz írja be a **guid()** kifejezést a kifejezésszerkesztőbe.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. lépés: Projektfeladat létrehozása

A következő lépésekkel hozzon létre egy olyan projektfeladatot, amely az aktuális projekthez és a létrehozott projektgyűjtőhöz tartozó egyedi azonosítóval rendelkezik.

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. A lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Projektfeleadat létrehozása** lépést.
5. A **Művelet neve** mezőben válassza az **msdyn\_PssCreateV1** lehetőséget.
6. Az **Entitás** mezőben adja meg a következő paraméterinformációkat.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Itt látható a paraméterek magyarázata:

    - **\@\@odata.type** – Az entitás neve. Például írja be a következőt: **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – A feladat egyedi azonosítója. Az értéket az **msdyn\_projecttaskid** dinamikus változójára kell állítani.
    - **msdyn\_project\@odata.bind** – A tulajdonos projekt projektazonosítója. Az érték a „Projekt létrehozása” lépés válaszának megfelelő dinamikus tartalom lesz. Ügyeljen arra, hogy a teljes elérési útat írja be, és adjon hozzá dinamikus tartalmat a zárójelek közé. Az idézőjelek kötelezőek. Például írja be a következőt: **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Bármely feladatnév.
    - **msdyn\_projectbucket\@odata.bind** – A feladatokat tartalmazó projektgyűjtő. Az érték a „Projekt gyűjtőlétrehozása” lépés válaszának megfelelő dinamikus tartalom lesz. Ügyeljen arra, hogy a teljes elérési útat írja be, és adjon hozzá dinamikus tartalmat a zárójelek közé. Az idézőjelek kötelezőek. Például írja be a következőt: **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Dinamikus tartalom a kezdő dátumhoz. Például a holnapi napnak a következő felel meg **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – A művelet kezdetének ütemezett dátuma. Például a holnapi napnak a következő felel meg **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Az ütemezett záró dátum. Válasszon ki egy Jövőbeli dátumot. Például adja meg az **"addDays(utcNow(), 5)"** értéket.
    - **msdyn\_LinkStatus** – A hivatkozás állapota. Például adja meg a következőt: **"192350000"**.

7. Az **OperationSetId** mezőhöz válassza az **msdyn\_CreateOperationSetV1Response** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13. lépés: Erőforrás-hozzárendelés létrehozása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. A lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a **Projekt hozzárendelése** lépést.
5. A **Művelet neve** mezőben válassza az **msdyn\_PssCreateV1** lehetőséget.
6. Az **Entitás** mezőben adja meg a következő paraméterinformációkat.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Az **OperationSetId** mezőhöz válassza az **msdyn\_CreateOperationSetV1Response** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. lépés: Egy változó értékének csökkentése

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **változó értéknek csökkentése** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. Válassza a **feladatok száma** lehetőséget a **Név** mezőben.
4. Az **Érték** mezőbe írja be: **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. lépés: Projektfeladat átnevezése

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. A lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át az **Projektfeleadat átnevezése** lépést.
5. A **Művelet neve** mezőben válassza az **msdyn\_PssUpdateV1** lehetőséget.
6. Az **Entitás** mezőben adja meg a következő paraméterinformációkat.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Az **OperationSetId** mezőhöz válassza az **msdyn\_CreateOperationSetV1Response** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16. lépés: Műveleti halmaz futtatása

1. A folyamatban válassza az **Új lépés** lehetőséget.
2. A **Művelet kiválasztása** párbeszédpanel keresési mezőjébe írja be a **nem kötési művelet végrehajtása** szöveget. Ezután a **Műveletek** lapon jelölje ki a műveletet az eredmények listájában.
3. A lépésben jelölje ki a három pontot (**...**), és válassza az **Átnevezés** lehetőséget.
4. Nevezze át a **Műveleti halmaz végrehajtása** lépést.
5. A **Művelet neve** mezőben válassza az **msdyn\_ExecuteOperationSetV1** lehetőséget.
6. Az **OperationSetId** mezőhöz válassza az **msdyn\_CreateOperationSetV1Response OperationSetId** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="references"></a>Referenciák

- [A Dataverse-folyamatok Power Automate-tel való integrálásának áttekintése](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](schedule-api-preview.md)
- [A felhőfolyamatok áttekintése – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [A megoldásérzékeny folyamatok áttekintése – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
