---
title: 'Projektütemezés API-k használata a következőkkel: Power Automate'
description: Ez a témakör olyan mintafolyamatot biztosít, amely a Project ütemezési alkalmazásprogramozási felületeit (API-kat) használja.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597709"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projektütemezés API-k használata a következőkkel: Power Automate

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a témakör egy mintafolyamatot ismertet, amely bemutatja, hogyan hozhat létre teljes projekttervet a használatával Microsoft Power Automate, hogyan hozhat létre műveletkészletet, és hogyan frissíthet egy entitást. A példa bemutatja, hogyan hozhat létre projektet, projektcsapat-tagot, műveletkészleteket, projekttevékenységeket és erőforrás-hozzárendeléseket. Ez a témakör azt is ismerteti, hogyan frissíthet egy entitást, és hogyan hajthat végre egy műveletkészletet.

Az alábbiakban felsoroljuk azokat a lépéseket, amelyeket a mintafolyamat ebben a témakör dokumentált:

1. [Eseményindító létrehozása PowerApps](#1)
2. [Projekt létrehozása](#2)
3. [Változó inicializálása a csapattag számára](#3)
4. [Általános csapattag létrehozása](#4)
5. [Műveletkészlet létrehozása](#5)
6. [Projektgyűjtő létrehozása](#6)
7. [Változó inicializálása a kapcsolat állapotához](#7)
8. [Változó inicializálása a tevékenységek számához](#8)
9. [Változó inicializálása a projektfeladat-azonosítóhoz](#9)
10. [Végezze el, amíg](#10)
11. [Projektfeladat beállítása](#11)
12. [Projektfeladat létrehozása](#12)
13. [Erőforrás-hozzárendelés létrehozása](#13)
14. [Változó decrement](#14)
15. [Projektfeladat átnevezése](#15)
16. [Műveletkészlet futtatása](#16)

## <a name="assumptions"></a>Feltételezések

Ez a témakör feltételezi, hogy alapvető ismeretekkel rendelkezik a platformról, a Dataverse felhőfolyamatokról és a Project Schedule Application Programming Interface (API) alkalmazásprogramozási felületről. További információt a [témakör későbbi, Hivatkozások](#references) című részében talál.

## <a name="create-a-flow"></a>Folyamat létrehozása

### <a name="select-an-environment"></a>Válasszon környezetet

Létrehozhatja az áramlást Power Automate a környezetében.

1. Nyissa meg a webhelyet, <https://flow.microsoft.com> és a rendszergazda hitelesítő adataival jelentkezzen be.
2. A jobb felső sarokban válassza a Környezetek **lehetőséget**.
3. A listában válassza ki azt a környezetet, ahová Dynamics 365 Project Operations telepítve van.

### <a name="create-a-solution"></a>Megoldás létrehozása

Megoldásbarát folyamat [létrehozásához](/power-automate/overview-solution-flows) kövesse az alábbi lépéseket. Megoldásbarát folyamat létrehozásával könnyebben exportálhatja a folyamatot későbbi használatra.

1. A navigációs ablakban válassza a Megoldások **lehetőséget**.
2. A Megoldások lapon válassza az **Új megoldás lehetőséget** **.**
3. **Az Új megoldás** párbeszédpanelen állítsa be a szükséges mezőket, majd válassza a Létrehozás **lehetőséget**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. lépés: Eseményindító létrehozása PowerApps

1. **A Megoldások** lapon válassza ki a létrehozott megoldást, majd válassza az Új **lehetőséget**.
2. A bal oldali ablaktáblában válassza **a Felhőfolyamatok** \> **automatizálása Felhőfolyamat** \> **azonnali** \> **elemét.**
3. A Folyamat neve **mezőbe írja be** az **API-bemutató folyamat ütemezése mezőjét**.
4. A Folyamatlista **aktiválásának kiválasztása csoportban válassza a** lehetőséget **Power Apps**. Amikor létrehoz egy eseményindítót Power Apps, a logika rajtad múlik, mint szerzőn. Ebben a témakör hagyja üresen a bemeneti paramétereket tesztelés céljából.
5. Válassza a **Létrehozás** parancsot.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. lépés: Projekt létrehozása

Mintaprojekt létrehozásához kövesse az alábbi lépéseket.

1. A létrehozott folyamatban válassza az Új lépés **lehetőséget**.

    ![Új lépés hozzáadása.](media/newstep.png)

2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.

    ![Művelet kiválasztása.](media/chooseactiontab.png)

3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.

![Átnevezni egy lépést.](media/renamestep.png)

4. Nevezze át a Projekt létrehozása **lépést**.
5. A Művelet neve **mezőben válassza** az **msdyn\_ CreateProjectV1 elemet**.
6. Az msdyn tárgymezőben **válassza a \_ Dinamikus tartalom** hozzáadása lehetőséget **.**
7. **A Kifejezés** lap függvénymezőjébe írja be **a Projekt nevét - utcNow()**.
8. Válassza az **OK** lehetőséget.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. lépés: Változó inicializálása a csapattag számára

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a inicializálási változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init-csoporttagot **·**.
5. A Név **mezőbe írja be** a **TeamMemberAction parancsot**.
6. A Típus mezőben válassza a **Karakterlánc lehetőséget** **.**
7. Az Érték **mezőbe írja be** az **msdyn\_ CreateTeamMemberV1 parancsot**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. lépés: Általános csapattag létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Csapattag létrehozása **lépését**.
5. A Művelet neve **mezőben válassza** a **TeamMemberAction lehetőséget** a **Dinamikus tartalom** párbeszédpanelen.
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

    Íme egy magyarázat a paraméterekről:

    - **\@\@ odata.type** – Az entitás neve. Írja be **például a "Microsoft.Dynamics.CRM.msdyn\_ projectteam" szót**.
    - **msdyn\_ projectteamid** – A projektcsapat azonosítójának elsődleges kulcsa. Az érték egy globálisan egyedi azonosító (GUID) kifejezés.   Az azonosító a kifejezéslapról jön létre.

    - **msdyn\_ project\@ odata.bind** – A tulajdonos projekt projektazonosítója. Az érték dinamikus tartalom lesz, amely a "Projekt létrehozása" lépés válaszából származik. Győződjön meg arról, hogy beírta a teljes elérési utat, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek megadása kötelező. Írja be **például a "/msdyn\_ projects(ADD DYNAMIC CONTENT)" kifejezést**.
    - **msdyn\_ név** – A csapattag neve. Írja be **például a "ScheduleAPIDemoTM1" kifejezést**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. lépés: Műveletkészlet létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Műveletkészlet létrehozása **lépését**.
5. **A Művelet neve** mezőben válassza ki az **msdyn\_ CreateOperationSetV1** Dataverse egyéni műveletet.
6. A Megnevezés **mezőbe írja be** a **ScheduleAPIDemoOperationSet értéket**.
7. A Projekt **mezőbe írja be** az **/msdyn\_ projects(**.
8. A Dinamikus tartalom **párbeszédpanelen válassza** az **msdyn\_ CreateProjectV1Response ProjectId** lehetőséget.
9. **A Projekt** mezőbe írja be **a )**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. lépés: Projektvödör létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **az új sor hozzáadása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Gyűjtő **létrehozása lépést**.
5. A Tábla neve **mezőben válassza a** Projektvödörök **lehetőséget**.
6. A Név **mezőbe írja be** a **ScheduleAPIDemoBucket1 értéket**.
7. A Projekt mezőben válassza **az** msdyn **CreateProjectV1Response ProjectId\_ elemet a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. lépés: Változó inicializálása a kapcsolat állapotához

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a inicializálási változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init linkstatus **lépést**.
5. **A Név** mezőbe írja be **a linkstatus értéket**.
6. A Típus **mezőben válassza** az **Egész lehetőséget**.
7. **Az Érték** mezőbe írja be **a 192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. lépés: Változó inicializálása a tevékenységek számához

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a inicializálási változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a lépés **init Feladatok száma mezőjét**.
5. **A Név** mezőbe írja be **a tevékenységek** számát.
6. A Típus **mezőben válassza** az **Egész lehetőséget**.
7. **Az Érték** mezőbe írja be **az 5** értéket.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. lépés: Változó inicializálása a projekttevékenység-azonosítóhoz

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a inicializálási változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át az Init ProjectTaskID **lépést**.
5. **A Név** mezőbe írja be **a tevékenységek** számát.
6. A Típus mezőben válassza a **Karakterlánc lehetőséget** **.**
7. Az Érték **mezőhöz írja be** a **guid()** értéket a kifejezésszerkesztőbe.

## <a name="step-10-do-until"></a><a id="10"></a> 10. lépés: Csináld addig, amíg

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a do until** parancsot. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Állítsa be a feltételes utasítás első értékét a **Dinamikus tartalom** párbeszédpanel tevékenységszám **változójára**.
4. Állítsa a feltételt kisebbre, **mint egyenlőre**.
5. Állítsa a feltételes utasítás második értékét 0-ra **·**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. lépés: Projektfeladat beállítása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a set variable** parancsot. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. Az új lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Projektfeladat **beállítása lépést**.
5. A Név **mezőben válassza** az **msdyn\_ projecttaskid** elemet.
6. Az Érték **mezőhöz írja be** a **guid()** értéket a kifejezésszerkesztőbe.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. lépés: Projektfeladat létrehozása

Az alábbi lépéseket követve olyan projekttevékenységet hozhat létre, amelynek egyedi azonosítója az aktuális projekthez és a létrehozott projektvödörhöz tartozik.

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Projektfeladat létrehozása **lépését**.
5. A Művelet neve **mezőben válassza** az **msdyn\_ PssCreateV1 elemet**.
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

    Íme egy magyarázat a paraméterekről:

    - **\@\@ odata.type** – Az entitás neve. Írja be **például a "Microsoft.Dynamics.CRM.msdyn\_ projecttask" szót**.
    - **msdyn\_ projecttaskid** – a tevékenység egyedi azonosítója. Az értéket dinamikus változóra kell állítani az msdyn projecttaskid-ból **\_.**
    - **msdyn\_ project\@ odata.bind** – A tulajdonos projekt projektazonosítója. Az érték dinamikus tartalom lesz, amely a "Projekt létrehozása" lépés válaszából származik. Győződjön meg arról, hogy beírta a teljes elérési utat, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek megadása kötelező. Írja be **például a "/msdyn\_ projects(ADD DYNAMIC CONTENT)" kifejezést**.
    - **msdyn\_ tárgy** – Bármely feladatnév.
    - **msdyn\_ projectbucket\@ odata.bind** – A tevékenységeket tartalmazó projektvödör. Az érték dinamikus tartalom lesz, amely a "Vödör létrehozása" lépés válaszából származik. Győződjön meg arról, hogy beírta a teljes elérési utat, és dinamikus tartalmat ad hozzá a zárójelek közé. Idézőjelek megadása kötelező. Írja be **például a "/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)" parancsot**.
    - **msdyn\_ start** – Dinamikus tartalom a kezdési dátumhoz. A holnapi nap például "addDays(utcNow(), 1)" lesz **ábrázolva**.
    - **msdyn\_ scheduledstart** – Az ütemezett kezdési dátum. A holnapi nap például "addDays(utcNow(), 1)" lesz **ábrázolva**.
    - **msdyn\_ scheduleend** – Az ütemezett befejezési dátum. Válasszon ki egy dátumot a jövőben. Adja meg **például az "addDays(utcNow(), 5)" értéket**.
    - **msdyn\_ LinkStatus** – A kapcsolat állapota. Írja be **például a "192350000" szót**.

7. Az OperationSetId mezőben válassza **az** msdyn **CreateOperationSetV1Response\_ lehetőséget a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. lépés: Erőforrás-hozzárendelés létrehozása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Hozzárendelés **létrehozása lépést**.
5. A Művelet neve **mezőben válassza** az **msdyn\_ PssCreateV1 elemet**.
6. **Az Entitás** mezőbe írja be a következő paraméteradatokat.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Az OperationSetId mezőben válassza **az** msdyn **CreateOperationSetV1Response\_ lehetőséget a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. lépés: Változó csökkentése

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a decrement változót**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. **A Név** mezőben válassza ki **a tevékenységek** számát.
4. **Az Érték** mezőbe írja be **az 1** értéket.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. lépés: Projektfeladat átnevezése

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Projekttevékenység átnevezése **lépését**.
5. A Művelet neve **mezőben válassza** az **msdyn\_ PssUpdateV1 elemet**.
6. **Az Entitás** mezőbe írja be a következő paraméteradatokat.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Az OperationSetId mezőben válassza **az** msdyn **CreateOperationSetV1Response\_ lehetőséget a** Dinamikus tartalom **párbeszédpanelen.**

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. lépés: Műveletkészlet futtatása

1. A folyamatban válassza az Új lépés **lehetőséget**.
2. **A Művelet** kiválasztása párbeszédpanel keresési mezőjébe írja be **a Kötetlen művelet végrehajtása parancsot**. Ezután a **Műveletek** lapon válassza ki a műveletet az eredménylistában.
3. A lépésben jelölje ki az ellipszis (**...**), majd válassza az Átnevezés **lehetőséget**.
4. Nevezze át a Műveletkészlet végrehajtása **lépését**.
5. A Művelet neve **mezőben válassza** az **msdyn\_ ExecuteOperationSetV1 elemet**.
6. Az OperationSetId mezőhöz válassza **az** msdyn **CreateOperationSetV1Response OperationSetId\_ lehetőséget a** Dynamid content **párbeszédpanelen.**

## <a name="references"></a>Referenciák

- [A folyamatok integrálásának áttekintése a következővel Dataverse : - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](schedule-api-preview.md)
- [A felhőáramlások áttekintése - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [A megoldásbarát folyamatok áttekintése - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
