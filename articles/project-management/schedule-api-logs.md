---
title: Projektütemezési naplók
description: Ez a témakör olyan információkat és mintákat tartalmaz, amelyek segítenek a Projektütemezés naplóinak használatában a projektütemezési szolgáltatással és a projektütemezési API-kkal kapcsolatos hibák nyomon követésében.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589521"
---
# <a name="project-scheduling-logs"></a>Projektütemezési naplók

_**Vonatkozik:** Projektműveletek erőforrás/nem raktározott forgatókönyvekhez, Lite üzembe helyezés - ajánlat proforma számlázásra_, _Project for the Web_

A Microsoft Dynamics 365 Project Operations a Project for the Web [programot használja](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) elsődleges ütemezési motorként. A szabványos Microsoft Dataverse webalkalmazás-programozási felületek (API-k) használata helyett a Project Operations az új Projektütemezési API-kat használja projektfeladatok, erőforrás-hozzárendelések, tevékenységfüggőségek, projektgyűjtők és projektcsapat-tagok létrehozásához, frissítéséhez és törléséhez. Ha azonban a létrehozási, frissítési vagy törlési műveleteket programozottan futtatják a munkalebontási struktúra (WBS) entitásain, hibák léphetnek fel. A hibák és a műveletek előzményeinek nyomon követéséhez két új felügyeleti naplót valósítottunk meg: **Műveletkészlet** és **Projektütemezési szolgáltatás (PSS)**. Ezeknek a naplóknak a eléréséhez nyissa meg a **Beállítások**\> ütemezési integrációja című témakört.**·**

Az alábbi ábra a Projektütemezési naplók adatmodelljét mutatja be.

![A projektütemezési naplók adatmodellje.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Műveletkészlet naplója

Az Operation Set napló egy olyan műveletkészlet végrehajtását követi nyomon, amely egy vagy több létrehozási, frissítési vagy törlési művelet futtatására szolgál egy kötegben projekteken, projekttevékenységeken, erőforrás-hozzárendeléseken, tevékenységfüggőségeken, projektgyűjtőkön vagy projektcsapat-tagokon. A **Művelet az állapotban** mezőben a műveletkészlet általános állapotát mutatja. A műveletkészlet hasznos terhelésének részleteit a kapcsolódó Műveletkészlet részletrekordjai rögzítik.

### <a name="operation-set"></a>Műveletkészlet

Az alábbi táblázat a Műveletkészlet **entitáshoz** kapcsolódó mezőket mutatja be.

| Séma neve            | Description                                                                                                  | Megjelenített név            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Az a dátum/idő, amikor a műveletkészlet befejeződött vagy sikertelen volt.                                                | CompletedOn            |
| msdyn_correlationid   | A **kérelem correlationId** értéke.                                                                  | CorrelationId          |
| msdyn_description     | A műveletkészlet leírása.                                                                        | Description            |
| msdyn_executedon      | A rekord futtatásának dátuma/időpontja.                                                                       | Végrehajtva            |
| msdyn_operationsetId  | Az entitáspéldányok egyedi azonosítója.                                                                   | OperationSet           |
| msdyn_Project         | A műveletkészlethez kapcsolódó projekt.                                                            | Project                |
| msdyn_projectid       | A **kérés projectId** értéke.                                                                      | ProjectId (elavult) |
| msdyn_projectName     | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_PSSErrorLog     | A műveletkészlethez társított Projektütemezési szolgáltatás hibanaplójának egyedi azonosítója. | PSS-hibanapló          |
| msdyn_PSSErrorLogName | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_status          | A műveletkészlet állapota.                                                                             | Állam                 |
| msdyn_statusName      | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_useraadid       | Azure Active Directory Annak Azure AD a felhasználónak az objektumazonosítója, akihez a kérelem tartozik.                     | UserAADID              |

### <a name="operation-set-detail"></a>Műveletkészlet részletei

Az alábbi táblázat a Műveletkészlet részlet **entitáshoz** kapcsolódó mezőket mutatja be.

| Séma neve                 | Description                                                                                 | Megjelenített név           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | A kérelem szerializált Dataverse mezői.                                            | CdsPayload            |
| msdyn_entityname           | A kérelem entitásának neve.                                                     | EntityName            |
| msdyn_httpverb             | A kérés módja.                                                                         | HTTP-parancs (elavult) |
| msdyn_httpverbName         | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationset         | Annak a műveletkészletnek az egyedi azonosítója, amelyhez a rekord tartozik.                      | OperationSet          |
| msdyn_operationsetdetailId | Az entitáspéldányok egyedi azonosítója.                                                  | OperationSet Detail   |
| msdyn_operationsetName     | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationtype        | A műveletkészlet művelettípusának típusa.                                             | OperationType         |
| msdyn_operationtypeName    | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_psspayload           | A kérelem szerializált Projektütemezési szolgáltatás mezői.                           | PssPayload            |
| msdyn_recordid             | A kérelembejegyzés azonosítója.                                                       | Rekordazonosító             |
| msdyn_requestnumber        | Automatikusan generált szám, amely azonosítja azt a sorrendet, amelyben a kérések érkeztek. | Kérelem száma        |

## <a name="project-scheduling-service-error-logs"></a>Projektütemezési szolgáltatás hibanaplói

A Project Scheduling Service hibanaplói rögzítik azokat a hibákat, amelyek akkor fordulnak elő, amikor a Projektütemezési szolgáltatás mentési **vagy megnyitási műveletet kísérel meg.** **·** Három támogatott forgatókönyv létezik, ahol ezek a naplók létrejönnek:

- A felhasználó által kezdeményezett műveletek kritikusan sikertelenek (például a hozzárendelés nem hozható létre a hiányzó jogosultságok miatt).
- A Projektütemezési szolgáltatás nem tud programozottan létrehozni, frissíteni, törölni vagy végrehajtani semmilyen más lépcsőzetes műveletet egy entitáson.
- A felhasználó hibákat tapasztal, ha egy bejegyzés nem nyílik meg (például amikor egy projektet megnyitnak, vagy egy csapattag adatait frissítik).

### <a name="project-scheduling-service-log"></a>Projektütemezési szolgáltatás naplója

Az alábbi táblázat a Projektütemezési szolgáltatás naplójában szereplő mezőket mutatja be.

| Séma neve          | Description                                                                    | Megjelenített név    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A kivétel hívásverme.                                               | Hívásverem     |
| msdyn_correlationid | A hiba korrelációs azonosítója.                                               | CorrelationId  |
| msdyn_errorcode     | A hibakód vagy a Dataverse HTTP-hibakód tárolására használt mező. | Hibakód     |
| msdyn_HelpLink      | Hivatkozás a nyilvános súgódokumentációra.                                       | Súgó hivatkozása      |
| msdyn_log           | A Projektütemezési szolgáltatás naplója.                                   | Napló            |
| msdyn_project       | A hibanaplóhoz társított projekt.                             | Project        |
| msdyn_projectName   | A projekt neve, ha a műveletkészlet hasznos terhelése megmarad. | Nem alkalmazható |
| msdyn_psserrorlogId | Az entitáspéldányok egyedi azonosítója.                                     | PSS-hibanapló  |
| msdyn_SessionId     | A projektmunkamenet azonosítója.                                                        | Munkamenet-azonosító     |

## <a name="error-log-cleanup"></a>Hibanapló karbantartása

Alapértelmezés szerint mind a Projektütemezési szolgáltatás hibanaplói, mind az Operation Set napló 90 naponta tisztítható. A 90 napnál régebbi rekordok törlődnek. A Projektparaméterek **lap msdyn_StateOperationSetAge** mezőjének értékének **módosításával azonban a** rendszergazdák módosíthatják a tisztítási tartományt úgy, hogy az 1 és 120 nap között legyen. Ennek az értéknek a módosítására számos módszer áll rendelkezésre:

- Testreszabhatja a **Projektparaméter** entitást egyéni lap létrehozásával és az **Elavult műveletek beállítása kor** mező hozzáadásával.
- Használjon olyan ügyfélkódot, amely a [WebApi szoftverfejlesztői készletet (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) használja.
- Használja az Xrm SDK **updateRecord metódust** (Client API-hivatkozás) használó Service SDK-kódot modellvezérelt alkalmazásokban. Power Apps tartalmazza az **updateRecord metódus leírását és támogatott paramétereit**.

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
