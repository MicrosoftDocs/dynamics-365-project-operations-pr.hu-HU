---
title: Projektütemezési naplók
description: Ez a témakör olyan információkat és mintákat tartalmaz, amelyek segítenek a Projektütemezési naplók használatával nyomon követni a Projektütemezési szolgáltatással és a Projektütemezési API-kkal kapcsolatos hibákat.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877511"
---
# <a name="project-scheduling-logs"></a>Projektütemezési naplók

_**Vonatkozik:** Projektműveletek erőforrás/nem raktározott alapú forgatókönyvekhez, Lite üzembe helyezés - üzlet a proforma számlázáshoz_, Project for the _Web_

A Microsoft Dynamics 365 Project Operations [a Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) elsődleges ütemezési motorját használja. A webalkalmazások programozási felületeinek (API-k) szabványos Microsoft Dataverse helyett a Project Operations az új Projektütemezési API-kat használja projekttevékenységek, erőforrás-hozzárendelések, tevékenységfüggőségek, projekt-gyűjtők és projektcsapatok tagjainak létrehozásához, frissítéséhez és törléséhez. Ha azonban a létrehozási, frissítési vagy törlési műveletek programozott módon futnak a munkalebontási struktúra (WBS) entitásokon, hibák léphetnek fel. A hibák és a műveletek előzményeinek nyomon követéséhez két új felügyeleti naplót valósított meg: **Műveletkészlet** és **Projektütemezési szolgáltatás (PSS)**. Ezeknek a naplóknak a eléréséhez nyissa meg a **Beállítások** \> **ütemezése integráció** lehetőséget.

Az alábbi ábra a Projektütemezési naplók adatmodelljét mutatja be.

![A Projektütemezési naplók adatmodellje.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Műveletkészlet naplója

Az Operation Set napló egy olyan műveletkészlet végrehajtását követi nyomon, amely egy vagy több művelet létrehozására, frissítésére vagy törlésére szolgál egy kötegben projekteken, projekttevékenységeken, erőforrás-hozzárendeléseken, tevékenységfüggőségeken, projekt-gyűjtőkön vagy projektcsapattagokon. A **Művelet az Állapotban** mezőben a műveletkészlet általános állapota látható. A műveletkészlet hasznos adatának részleteit a kapcsolódó műveletkészlet részletei rekordjai rögzítik.

### <a name="operation-set"></a>Műveletkészlet

Az alábbi táblázat az Operation Set entitáshoz kapcsolódó mezőket mutatja **be**.

| Séma neve            | Description                                                                                                  | Megjelenített név            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A műveletkészlet befejezésének vagy sikertelennek a dátuma/időpontja.                                                | CompletedOn            |
| msdyn_correlationid   | A **kérelem korrelációs** értéke.                                                                  | CorrelationId          |
| msdyn_description     | A műveletkészlet leírása.                                                                        | Description            |
| msdyn_executedon      | A rekord futtatásának dátuma/időpontja.                                                                       | Végrehajtva            |
| msdyn_operationsetId  | Az entitáspéldányok egyedi azonosítója.                                                                   | OperationSet           |
| msdyn_Project         | A műveletkészlethez kapcsolódó projekt.                                                            | Project                |
| msdyn_projectid       | A **kérelem projectId** értéke.                                                                      | ProjectId (elavult) |
| msdyn_projectName     | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_PSSErrorLog     | A műveletkészlethez társított Projektütemezési szolgáltatás hibanaplójának egyedi azonosítója. | PSS-hibanapló          |
| msdyn_PSSErrorLogName | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_status          | A műveletkészlet állapota.                                                                             | Állam                 |
| msdyn_statusName      | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_useraadid       | Annak a felhasználónak a Azure Active Directory (Azure AD) objektumazonosítója, amelyhez a kérelem tartozik.                     | UserAADID              |

### <a name="operation-set-detail"></a>Műveletkészlet részletei

Az alábbi táblázat az Operation Set Detail entitáshoz kapcsolódó mezőket mutatja **be**.

| Séma neve                 | Description                                                                                 | Megjelenített név           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | A kérelem szerializált Dataverse mezői.                                            | CdsPayload            |
| msdyn_entityname           | A kérelem entitásának neve.                                                     | EntityName            |
| msdyn_httpverb             | A kérési módszer.                                                                         | HTTP-parancs (elavult) |
| msdyn_httpverbName         | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationset         | Annak a műveletkészletnek az egyedi azonosítója, amelyhez a rekord tartozik.                      | OperationSet          |
| msdyn_operationsetdetailId | Az entitáspéldányok egyedi azonosítója.                                                  | OperationSet Detail   |
| msdyn_operationsetName     | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationtype        | A műveletkészlet művelettípusának részlete.                                             | OperationType         |
| msdyn_operationtypeName    | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_psspayload           | A kérelem szerializált projektütemezési szolgáltatás mezői.                           | PssPayload            |
| msdyn_recordid             | A kérelemrekord azonosítója.                                                       | Rekordazonosító             |
| msdyn_requestnumber        | Automatikusan generált szám, amely azonosítja a kérelmek beérkezésének sorrendjét. | Kérelem száma        |

## <a name="project-scheduling-service-error-logs"></a>Projektütemezési szolgáltatás hibanaplói

A Projektütemezési szolgáltatás hibanaplója rögzíti a Projektütemezési szolgáltatás Mentési vagy Megnyitási műveletének sikertelenésekor **előforduló** **hibákat**. Három támogatott forgatókönyv létezik, ahol ezek a naplók létrejönnek:

- A felhasználó által kezdeményezett műveletek kritikusan sikertelenek (például a hozzárendelés nem hozható létre a hiányzó jogosultságok miatt).
- A Projektütemezési szolgáltatás nem hozhat létre, nem frissíthet, törölhet vagy hajthat végre más lépcsőzetes műveletet egy entitáson.
- A felhasználó hibákat tapasztal, ha egy rekord nem nyílik meg (például egy projekt megnyitásakor vagy a csapattag adatainak frissítésekor).

### <a name="project-scheduling-service-log"></a>Projektütemezési szolgáltatás naplója

Az alábbi táblázat a Projektütemezési szolgáltatás naplójában szereplő mezőket mutatja be.

| Séma neve          | Description                                                                    | Megjelenített név    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A kivétel hívásverme.                                               | Hívásverem     |
| msdyn_correlationid | A hiba korrelációs azonosítója.                                               | CorrelationId  |
| msdyn_errorcode     | A Dataverse hibakód vagy a HTTP-hibakód tárolására használt mező. | Hibakód     |
| msdyn_HelpLink      | Hivatkozás a nyilvános súgódokumentációra.                                       | Súgó hivatkozása      |
| msdyn_log           | A projektütemezési szolgáltatás naplója.                                   | Napló            |
| msdyn_project       | A hibanaplóhoz társított projekt.                             | Project        |
| msdyn_projectName   | A projekt neve, ha a műveletkészlet hasznos terhelése megmarad. | Nem alkalmazható |
| msdyn_psserrorlogId | Az entitáspéldányok egyedi azonosítója.                                     | PSS-hibanapló  |
| msdyn_SessionId     | A projekt munkamenetének azonosítója.                                                        | Munkamenet-azonosító     |

## <a name="error-log-cleanup"></a>Hibanapló-tisztítás

Alapértelmezés szerint mind a Projektütemezési szolgáltatás hibanaplói, mind az Operation Set napló 90 naponta törölhető. A 90 napnál régebbi rekordok törlődnek. A Projektparaméterek lap msdyn_StateOperationSetAge mezőjének értékének módosításával azonban **a** **rendszergazdák** módosíthatják a tisztítási tartományt úgy, hogy az 1 és 120 nap között legyen. Az érték módosítására számos módszer áll rendelkezésre:

- Testreszabhatja a **Project Parameter** entitást egy egyéni lap létrehozásával és az **Elavult műveletek készletkora mező** hozzáadásával.
- A [WebApi szoftverfejlesztő készletet (SDK) használó ügyfélkód](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) használata.
- Használja az Xrm SDK **updateRecord** metódust (Ügyfél API-hivatkozás) használó Service SDK-kódot a modellvezérelt alkalmazásokban. Power Apps tartalmazza az updateRecord metódus leírását és támogatott **paramétereit**.

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
