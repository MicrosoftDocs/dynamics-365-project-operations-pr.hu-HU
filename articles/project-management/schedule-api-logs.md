---
title: Projektütemezési naplók
description: Ez a cikk olyan információkat és mintákat tartalmaz, amelyek segítségével a Projektütemezési naplók segítségével nyomon követheti a Projektütemezés szolgáltatással és a Projektütemezés API-kkal kapcsolatos hibákat.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923698"
---
# <a name="project-scheduling-logs"></a>Projektütemezési naplók

_**Érintett:** Projektműveletek erőforrás-/nem készletalapú forgatókönyvekhez, Egyszerűsített telepítés – ajánlat a proforma számlázáshoz_, _Project for the Web_

A Microsoft Dynamics 365 Project Operations a [Webes Projektet használja](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) elsődleges ütemezési motorként. A szabványos Microsoft Dataverse webalkalmazás-programozási felületek (API-k) használata helyett a Project Operations az új Projektütemezés API-kat használja a projekttevékenységek, erőforrás-hozzárendelések, tevékenységfüggőségek, projektkategóriák és projektcsapatok tagjainak létrehozásához, frissítéséhez és törléséhez. Ha azonban a létrehozási, frissítési vagy törlési műveletek programozott módon futnak a munkalebontási struktúra (WBS) entitásokon, hibák léphetnek fel. A hibák és a műveletek előzményeinek nyomon követéséhez két új felügyeleti naplót valósítottunk meg: a műveletkészletet és a projektütemezési szolgáltatást (PSS).To track these errors and the history of operations, it are two new administrative logs implemented to: Operation Set and Project Scheduling Service (PSS).**To track these errors and the history of operations, it have two new administrative logs implemented to:** Operation Set **and** Project Scheduling A naplók eléréséhez lépjen a **Beállítások** \> **ütemezési integrációja oldalra.**

Az alábbi ábra a Projektütemezés-naplók adatmodelljét mutatja be.

![Adatmodell a projektütemezési naplókhoz.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Műveleti készlet naplója

A műveletkészlet naplója nyomon követi egy olyan műveletkészlet végrehajtását, amely egy vagy több létrehozási, frissítési vagy törlési művelet futtatására szolgál egy kötegben projekteken, projekttevékenységeken, erőforrás-hozzárendeléseken, tevékenységfüggőségeken, projektkategóriákon vagy projektcsapattagokon. A **Művelet az állapotban** mező a műveletkészlet általános állapotát mutatja. A műveletkészlet hasznos adatcsomagjának részleteit a rendszer a kapcsolódó műveletikészlet-részletes rekordokban rögzíti.

### <a name="operation-set"></a>Műveletkészlet

Az alábbi táblázat a Műveletkészlet entitáshoz **kapcsolódó mezőket mutatja be**.

| Séma neve            | Description                                                                                                  | Megjelenített név            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A műveletkészlet befejezésének vagy sikertelenségének dátuma/időpontja.                                                | CompletedOn            |
| msdyn_correlationid   | A **kérés correlationId** értéke.                                                                  | CorrelationId          |
| msdyn_description     | A műveletkészlet leírása.                                                                        | Description            |
| msdyn_executedon      | A rekord futtatásának dátuma/időpontja.                                                                       | Végrehajtva            |
| msdyn_operationsetId  | Az entitáspéldányok egyedi azonosítója.                                                                   | OperationSet           |
| msdyn_Project         | A műveletkészlethez kapcsolódó projekt.                                                            | Project                |
| msdyn_projectid       | A **kérelem projectId** értéke.                                                                      | ProjectId (elavult) |
| msdyn_projectName     | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_PSSErrorLog     | A műveletkészlethez társított Project Scheduling Service hibanapló egyedi azonosítója. | PSS-hibanapló          |
| msdyn_PSSErrorLogName | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_status          | A műveletkészlet állapota.                                                                             | Állam                 |
| msdyn_statusName      | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_useraadid       | Annak Azure Active Directory a felhasználónak az objektumazonosítója,Azure AD akihez a kérés tartozik.                     | UserAADID              |

### <a name="operation-set-detail"></a>A műveletkészlet részletei

Az alábbi táblázat a Műveleti készlet részletei entitáshoz **kapcsolódó mezőket mutatja be**.

| Séma neve                 | Description                                                                                 | Megjelenített név           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | A kérelem szerializált Dataverse mezői.                                            | CdsPayload            |
| msdyn_entityname           | A kérelemhez tartozó entitás neve.                                                     | EntityName            |
| msdyn_httpverb             | A kérés módja.                                                                         | HTTP-parancs (elavult) |
| msdyn_httpverbName         | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationset         | Annak a műveletkészletnek az egyedi azonosítója, amelyhez a rekord tartozik.                      | OperationSet          |
| msdyn_operationsetdetailId | Az entitáspéldányok egyedi azonosítója.                                                  | OperationSet Detail   |
| msdyn_operationsetName     | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationtype        | A műveletkészlet részleteinek művelettípusa.                                             | OperationType         |
| msdyn_operationtypeName    | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_psspayload           | A kérelem szerializált Projektütemezési szolgáltatás mezői.                           | PssPayload            |
| msdyn_recordid             | A kérelemrekord azonosítója.                                                       | Rekordazonosító             |
| msdyn_requestnumber        | Egy automatikusan generált szám, amely azonosítja azt a sorrendet, amelyben a kérelmek érkeztek. | Kérelem száma        |

## <a name="project-scheduling-service-error-logs"></a>A Projektütemezés szolgáltatás hibanaplói

A Projektütemezési szolgáltatás hibanaplói rögzítik azokat a hibákat, amelyek akkor fordulnak elő, amikor a Projektütemezés szolgáltatás megpróbál egy **Mentési** vagy **megnyitási** műveletet. Három támogatott forgatókönyv létezik, ahol ezek a naplók jönnek létre:

- A felhasználó által kezdeményezett műveletek kritikusan meghiúsulnak (például a hiányzó jogosultságok miatt nem hozható létre hozzárendelés).
- A Projektütemezési szolgáltatás nem hozhat létre, frissíthet, törölhet és nem hajthat végre programozott módon semmilyen más lépcsőzetes műveletet egy entitáson.
- A felhasználó hibákat tapasztal, ha egy rekord nem nyílik meg (például amikor megnyitnak egy projektet, vagy frissítik egy csapattag adatait).

### <a name="project-scheduling-service-log"></a>Projektütemezési szolgáltatás naplója

Az alábbi táblázat a Projektütemezés szolgáltatás naplójában szereplő mezőket mutatja be.

| Séma neve          | Description                                                                    | Megjelenített név    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A kivétel hívásverme.                                               | Hívásverem     |
| msdyn_correlationid | A hiba korrelációs azonosítója.                                               | CorrelationId  |
| msdyn_errorcode     | A hibakód vagy a Dataverse HTTP-hibakód tárolására szolgáló mező. | Hibakód     |
| msdyn_HelpLink      | A nyilvános súgódokumentációra mutató hivatkozás.                                       | Súgó hivatkozása      |
| msdyn_log           | A Projektütemezési szolgáltatás naplója.                                   | Napló            |
| msdyn_project       | A hibanaplóhoz társított projekt.                             | Project        |
| msdyn_projectName   | A projekt neve, ha a műveletkészlet hasznos terhelése megmarad. | Nem alkalmazható |
| msdyn_psserrorlogId | Az entitáspéldányok egyedi azonosítója.                                     | PSS-hibanapló  |
| msdyn_SessionId     | A projekt munkamenetének azonosítója.                                                        | Munkamenet-azonosító     |

## <a name="error-log-cleanup"></a>Hibanapló tisztítása

Alapértelmezés szerint mind a Project Scheduling Service hibanaplói, mind a műveleti készlet naplója 90 naponta tisztítható. A 90 napnál régebbi rekordok törlődnek. A projektparaméterek **lapon a** msdyn_StateOperationSetAge **mező értékének módosításával azonban a** rendszergazdák úgy módosíthatják a tisztítási tartományt, hogy az 1 és 120 nap között legyen. Az érték módosítására számos módszer áll rendelkezésre:

- Testreszabhatja a **Projektparaméter** entitást egy egyéni oldal létrehozásával és az **Elavult műveletek beállítása kor** mező hozzáadásával.
- Használjon olyan ügyfélkódot, amely a [WebApi szoftverfejlesztői készletet (SDK) használja](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Használjon olyan SDK-kódot, amely az Xrm SDK **updateRecord metódust** (ügyfél API-referenciát) használja a modellvezérelt alkalmazásokban. Power Apps tartalmaz egy leírást és támogatott paramétereket az **updateRecord** metódushoz.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
