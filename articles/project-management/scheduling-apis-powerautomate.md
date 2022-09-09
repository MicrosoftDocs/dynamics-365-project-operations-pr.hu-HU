---
title: Projektütemezési API-k használata a Power Automate-tel
description: Ez a cikk egy mintafolyamatot tartalmaz, amely a Project ütemezési alkalmazásprogramozási felületeit (API-kat) használja.
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

Ez a cikk egy mintafolyamatot ismertet, amely bemutatja, hogyan hozhat létre teljes projekttervet a használatával Microsoft Power Automate, hogyan hozhat létre műveletkészletet, és hogyan frissíthet egy entitást. A példa bemutatja, hogyan hozhat létre projektet, projektcsapattagot, műveletkészleteket, projekttevékenységeket és erőforrás-hozzárendeléseket. Ez a cikk azt is ismerteti, hogyan frissíthet egy entitást, és hogyan hajthat végre egy műveletkészletet.

Az alábbiakban felsoroljuk a cikkben a mintafolyamatban dokumentált lépéseket:

1. [Eseményindító létrehozása PowerApps](#1)
2. [Projekt létrehozása](#2)
3. [Változó inicializálása a csapattag számára](#3)
4. [Általános csapattag létrehozása](#4)
5. [Műveletkészlet létrehozása](#5)
6. [Projektkategória létrehozása](#6)
7. [Változó inicializálása a hivatkozás állapotához](#7)
8. [Változó inicializálása a tevékenységek számához](#8)
9. [Változó inicializálása a projekttevékenység-azonosítóhoz](#9)
10. [Csináld, amíg](#10)
11. [Projekttevékenység beállítása](#11)
12. [Projekttevékenység létrehozása](#12)
13. [Erőforrás-hozzárendelés létrehozása](#13)
14. [Változó dekrementálása](#14)
15. [Projekttevékenység átnevezése](#15)
16. [Műveletkészlet futtatása](#16)

## <a name="assumptions"></a>Feltételezések

Ez a cikk feltételezi, hogy alapvető ismeretekkel rendelkezik a platformról, a Dataverse felhőfolyamatokról és a Projektütemezés alkalmazásprogramozási felületéről (API). További információt a [cikk későbbi, Hivatkozások](#references) című szakaszában talál.

## <a name="create-a-flow"></a>Folyamat létrehozása

### <a name="select-an-environment"></a>Válasszon környezetet

A folyamatot a Power Automate környezetben is létrehozhatja.

1. Lépjen a <https://flow.microsoft.com>, és használja a rendszergazdai hitelesítő adatait a bejelentkezéshez.
2. A jobb felső sarokban válassza a Környezetek **lehetőséget**.
3. A listában válassza ki azt a környezetet, ahol Dynamics 365 Project Operations telepítve van.

### <a name="create-a-solution"></a>Megoldás létrehozása

Kövesse az alábbi lépéseket egy [megoldásbarát folyamat](/power-automate/overview-solution-flows) létrehozásához. Ha megoldásbarát folyamatot hoz létre, könnyebben exportálhatja a folyamatot, hogy később használhassa.

1. A navigációs panelen válassza a Megoldások **lehetőséget**.
2. A Megoldások **lapon válassza az** Új megoldás **lehetőséget**.
3. **Az Új megoldás** párbeszédpanelen állítsa be a szükséges mezőket, majd válassza a Létrehozás **lehetőséget**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. lépés: Eseményindító létrehozása PowerApps

1. **A Megoldások** lapon válassza ki a létrehozott megoldást, majd válassza az Új **lehetőséget**.
2. A bal oldali panelen válassza a Cloud **Flows**\> Automation **·**\> Cloud **Flow**\> Instant lehetőséget.**·**
3. A Folyamat neve **mezőbe írja be a** következőt: **API-bemutató folyamat** ütemezése.
4. A Folyamat aktiválásának **kiválasztása listában válassza** a **Power Apps** lehetőséget. Eseményindító létrehozásakor Power Apps a logika rajtad, mint szerzőn múlik. Ebben a cikkben hagyja üresen a bemeneti paramétereket tesztelési célokra.
5. Válassza a **Létrehozás** parancsot.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. lépés: Projekt létrehozása

Kövesse az alábbi lépéseket egy mintaprojekt létrehozásához.

1. A létrehozott folyamatban válassza az Új lépés **lehetőséget**.

    ![Új lépés hozzáadása.](media/newstep.png)

2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.

    ![Művelet kiválasztása.](media/chooseactiontab.png)

3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.

![Egy lépés átnevezése.](media/renamestep.png)

4. Nevezze át a Projekt létrehozása **lépést**.
5. A Művelet neve **mezőben válassza az** msdyn **CreateProjectV1 lehetőséget\_**.
6. Az msdyn **tárgymező\_ alatt válassza a** Dinamikus tartalom **hozzáadása lehetőséget**.
7. A Kifejezés **lap függvénymezőjébe írja be** a **Project name - utcNow() nevet**.
8. Válassza az **OK** lehetőséget.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. lépés: Változó inicializálása a csapattag számára

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a változó inicializálása kifejezést**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init csapattag **lépést**.
5. A Név **mezőbe írja be** a **TeamMemberAction nevet**.
6. A Típus **mezőben válassza a** Karakterlánc **lehetőséget**.
7. Az Érték **mezőbe írja be** az **msdyn\_ CreateTeamMemberV1 értéket**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. lépés: Általános csapattag létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Csapattag **létrehozása lépést**.
5. A Művelet neve **mezőben válassza a** TeamMemberAction **lehetőséget** a **Dinamikus tartalom** párbeszédpanelen.
6. **A Műveletparaméterek** mezőbe írja be a következő paraméteradatokat.

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

    Íme a paraméterek magyarázata:

    - **\@\@ odata.type** – Az entitás neve. Írja be **például a "Microsoft.Dynamics.CRM.msdyn\_ projectteam" nevet**.
    - **msdyn\_ projectteamid** – A projektcsapat azonosítójának elsődleges kulcsa. Az érték egy globálisan egyedi azonosító (GUID) kifejezés.   Az azonosító a kifejezés lapról jön létre.

    - **msdyn\_ projekt\@ odata.bind** – A tulajdonos projekt azonosítója. Az érték dinamikus tartalom lesz, amely a "Projekt létrehozása" lépés válaszából származik. Győződjön meg arról, hogy a teljes elérési utat adta meg, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek szükségesek. Írja be például a következőt: **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ név** – A csapattag neve. Írja be például a következőt: **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. lépés: Műveletkészlet létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Műveletkészlet **létrehozása lépést**.
5. **A Művelet neve** mezőben válassza ki az **msdyn\_ CreateOperationSetV1** Dataverse egyéni műveletet.
6. A Leírás **mezőbe írja be a** következőt: **ScheduleAPIDemoOperationSet**.
7. A Projekt **mezőbe írja be** az **/msdyn\_ projects( parancsot**.
8. A Dinamikus tartalom **párbeszédpanelen válassza** az **msdyn\_ CreateProjectV1Response ProjectId lehetőséget**.
9. A Projekt **mezőbe írja be a** következőt: **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. lépés: Projektvödör létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet kiválasztása párbeszédpanel keresési** mezőjébe írja be **az új sor hozzáadása kifejezést**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Gyűjtő **létrehozása lépést**.
5. A Tábla neve **mezőben válassza a** Project Buckets (Projektzónák) **lehetőséget**.
6. A Név **mezőbe írja be a** következőt: **ScheduleAPIDemoBucket1**.
7. A Projekt **mezőben válassza** az **msdyn\_ CreateProjectV1Response ProjectId** lehetőséget a **Dinamikus tartalom** párbeszédpanelen.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. lépés: Változó inicializálása a hivatkozás állapotához

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a változó inicializálása kifejezést**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init linkstatus **lépést**.
5. A Név **mezőbe írja be** a **linkstatus nevet**.
6. A Típus **mezőben válassza az** Egész szám **lehetőséget**.
7. Az Érték **mezőbe írja be** a **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. lépés: Változó inicializálása a feladatok számához

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a változó inicializálása kifejezést**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init Number of tasks **lépést**.
5. A Név **mezőbe írja be** a **tevékenységek** számát.
6. A Típus **mezőben válassza az** Egész szám **lehetőséget**.
7. Az Érték **mezőbe írja be** az **5 értéket**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. lépés: Változó inicializálása a projekttevékenység-azonosítóhoz

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a változó inicializálása kifejezést**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init ProjectTaskID **lépést**.
5. A Név **mezőbe írja be** a **tevékenységek** számát.
6. A Típus **mezőben válassza a** Karakterlánc **lehetőséget**.
7. Az Érték **mezőbe írja be** a **guid()** szót a kifejezésszerkesztőbe.

## <a name="step-10-do-until"></a><a id="10"></a> 10. lépés: Tegye meg, amíg

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet kiválasztása párbeszédpanel keresési** mezőjébe írja be **a do until parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Állítsa a feltételes utasítás első értékét a **Dinamikus tartalom** párbeszédpanelen a **tevékenységek** száma változóra.
4. Állítsa a feltételt **egyenlőnél kisebbre**.
5. Állítsa a feltételes utasítás második értékét 0-ra **·**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. lépés: Projektfeladat beállítása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a set változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Projektfeladat **beállítása lépést**.
5. A Név **mezőben válassza az** msdyn **projecttaskid\_ lehetőséget**.
6. Az Érték **mezőbe írja be** a **guid()** szót a kifejezésszerkesztőbe.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. lépés: Projekttevékenység létrehozása

Kövesse az alábbi lépéseket egy olyan projekttevékenység létrehozásához, amely egyedi azonosítóval rendelkezik, amely az aktuális projekthez és a létrehozott projektkategóriához tartozik.

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Projektfeladat **létrehozása lépést**.
5. A Művelet neve mezőben válassza az **msdyn** PssCreateV1 lehetőséget **\_.**
6. **Az Entitás** mezőbe írja be a következő paraméteradatokat.

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

    Íme a paraméterek magyarázata:

    - **\@\@ odata.type** – Az entitás neve. Írja be **például a "Microsoft.Dynamics.CRM.msdyn\_ projecttask" nevet**.
    - **msdyn\_ projecttaskid** – A feladat egyedi azonosítója. Az értéket az msdyn **projecttaskid\_ dinamikus változójára** kell állítani.
    - **msdyn\_ projekt\@ odata.bind** – A tulajdonos projekt azonosítója. Az érték dinamikus tartalom lesz, amely a "Projekt létrehozása" lépés válaszából származik. Győződjön meg arról, hogy a teljes elérési utat adta meg, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek szükségesek. Írja be például a következőt: **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ tárgy** – Bármely feladat neve.
    - **msdyn\_ projectbucket\@ odata.bind** – A tevékenységeket tartalmazó projektvödör. Az érték dinamikus tartalom lesz, amely a "Vödör létrehozása" lépés válaszából származik. Győződjön meg arról, hogy a teljes elérési utat adta meg, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek szükségesek. Írja be például a következőt: **"/msdyn\_ projectbuckets(DYNAMIC CONTENT HOZZÁADÁSA)"**.
    - **msdyn\_ start** – Dinamikus tartalom a kezdési dátumhoz. Például a holnap az "addDays(utcNow(), 1)"**lesz.**
    - **msdyn\_ scheduledstart** – A tervezett kezdési dátum. Például a holnap az "addDays(utcNow(), 1)"**lesz.**
    - **msdyn\_ scheduleend** – A tervezett befejezési dátum. Válasszon ki egy dátumot a jövőben. Adja meg **például az "addDays(utcNow(), 5)" értéket**.
    - **msdyn\_ LinkStatus** – A hivatkozás állapota. Írja be **például a "192350000" értéket**.

7. Az OperationSetId mezőben válassza az **msdyn** CreateOperationSetV1Response **lehetőséget \_ a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. lépés: Erőforrás-hozzárendelés létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Hozzárendelés **létrehozása lépést**.
5. A Művelet neve mezőben válassza az **msdyn** PssCreateV1 lehetőséget **\_.**
6. **Az Entitás** mezőbe írja be a következő paraméteradatokat.

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

7. Az OperationSetId mezőben válassza az **msdyn** CreateOperationSetV1Response **lehetőséget \_ a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. lépés: Változó dekrementálása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet kiválasztása párbeszédpanel keresési** mezőjébe írja be **a decrement változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. **A Név** mezőben válassza ki **a tevékenységek** számát.
4. Az Érték **mezőbe írja be** az **1 értéket**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. lépés: Projekttevékenység átnevezése

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Lépés **átnevezése Projektfeladatot**.
5. A Művelet neve mezőben válassza az **msdyn** PssUpdateV1 lehetőséget **\_.**
6. **Az Entitás** mezőbe írja be a következő paraméteradatokat.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Az OperationSetId mezőben válassza az **msdyn** CreateOperationSetV1Response **lehetőséget \_ a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. lépés: Műveletkészlet futtatása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Határtalan művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben válassza ki a három pontot (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Műveletkészlet **végrehajtása lépést**.
5. A Művelet neve mezőben válassza az **msdyn** ExecuteOperationSetV1 lehetőséget **\_.**
6. Az OperationSetId **mezőben válassza az** msdyn **CreateOperationSetV1Response OperationSetId\_ lehetőséget** a **Dynamid tartalom** párbeszédpanelen.

## <a name="references"></a>Referenciák

- [A folyamatok integrálásának áttekintése a következővel Dataverse : - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](schedule-api-preview.md)
- [A felhőfolyamatok áttekintése - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [A megoldástudatos folyamatok áttekintése - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
