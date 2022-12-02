---
title: Projektütemezési naplók
description: A cikk olyan tudnivalókat és mintákat tartalmaz, amelyek segítenek a Projektütemezési naplók segítségével nyomon követni a projektütemezési szolgáltatáshoz és a projektütemezési API-khoz kapcsolódó hibák.
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

_**A következőre érvényes:** Project Operations erőforrás / nem készletezett alapú forgatókönyvek_, Lite telepítése – üzlet a proforma számlázáshoz, _Project for the Web_

A Microsoft Dynamics 365 Project Operations a [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) alkalmazást használja elsődleges ütemezési motorként. A normál Microsoft Dataverse webes alkalmazásokprogramozási felületek (API-k) használata helyett a Project Operations az új projektütemezési API-kat használják a projektfeladatok, erőforrás-hozzárendelések, feladat függőségek, projektütemezések és projektcsoporttagok létrehozására, frissítésére és törlésére. Azonban a létrehozási, frissítési vagy törlési műveletek programozott módon futnak a munkalebontási struktúra (WBS) entitásain hibák fordulhatnak elő. Az ilyen hibák és a műveletek előzményeinek nyomon követéséhez két új felügyeleti napló lett bevezetve: **Művelethalmaz** és **Projektütemezési szolgáltatás** (PSS). Ha hozzá szeretne férni ezekhez a naplókhoz, akkor menjen a **Beállítások** \> **Ütemezési integráció** menüpontba.

A következő ábrán a Projektütemezési naplók adatmodellje látható.

![A projektütemezési naplók adatmodellje.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Műveleti halmaz napló

Az műveleti halmaz napló nyomon követi egy művelethalmaz végrehajtását, amely egy vagy több létrehozási, frissítési vagy törlési művelet futtatására használatos egy kötegben projekteken, projektfeladatokon, erőforrás-hozzárendeléseken, feladat-függőségeken, projektgyűjtőkön vagy projekt csoporttagokon. Az **Művelet állapota** mezőben megmutatja művelethalmaz általános állapotát. A művelethalmaz hasznos terhelésének részleteit a rendszer a kapcsolódó Művelethalma részletei rekordokban rögzíti.

### <a name="operation-set"></a>Műveleti halmaz

A következő táblázat mutatja a mezőket, a **Műveleti halmaz** entitáshoz kapcsolódnak.

| Séma neve            | Description                                                                                                  | Megjelenített név            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A művelethalmaz befejezésének vagy meghiúsulásának dátuma és időpontja.                                                | CompletedOn            |
| msdyn_correlationid   | A kérelem **correlationId** értéke.                                                                  | CorrelationId          |
| msdyn_description     | A műveleti halmaz leírása.                                                                        | Description            |
| msdyn_executedon      | A rekord futtatásának dátuma és időpontja.                                                                       | Végrehajtva            |
| msdyn_operationsetId  | Az entitáspéldányok egyedi azonosítója.                                                                   | OperationSet           |
| msdyn_Project         | A műveleti halmazhoz kapcsolódó projekt.                                                            | Project                |
| msdyn_projectid       | A kérelem **projectId** értéke.                                                                      | ProjectId (elavult) |
| msdyn_projectName     | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_PSSErrorLog     | A művelethalmazhoz társított Projektütemezésiszolgáltatás-hibanapló egyedi azonosítója. | PSS-hibanapló          |
| msdyn_PSSErrorLogName | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_status          | A műveleti halmaz állapota.                                                                             | Állam                 |
| msdyn_statusName      | Nem alkalmazható.                                                                                              | Nem alkalmazható         |
| msdyn_useraadid       | Azon felhasználó Azure Active Directory (Azure AD) objektumazonosítója, akihez ez a kérelem tartozik.                     | UserAADID              |

### <a name="operation-set-detail"></a>Műveleti halmaz adatai

A következő táblázat bemutatja a mezőket, amelyek **Műveleti halmaz részletei** entitáshoz kapcsolódnak.

| Séma neve                 | Description                                                                                 | Megjelenített név           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Szerializált Dataverse-mezők a kérelem.                                            | CdsPayload            |
| msdyn_entityname           | Az entitás neve ehhez kéréshez.                                                     | EntityName            |
| msdyn_httpverb             | A kérelmi metódus.                                                                         | HTTP-parancs (elavult) |
| msdyn_httpverbName         | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationset         | A művelethalmaz egyedi azonosítója, amelyhez a rekord tartozik.                      | OperationSet          |
| msdyn_operationsetdetailId | Az entitáspéldányok egyedi azonosítója.                                                  | OperationSet Detail   |
| msdyn_operationsetName     | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_operationtype        | A művelethalmaz részleteinek művelettípusa.                                             | OperationType         |
| msdyn_operationtypeName    | Nem alkalmazható.                                                                             | Nem alkalmazható        |
| msdyn_psspayload           | A kérelem szericializált projektütemezésiszolgáltatás-mezői.                           | PssPayload            |
| msdyn_recordid             | A kérelemrekord elsődleges azonosítója.                                                       | Rekordazonosító             |
| msdyn_requestnumber        | Egy automatikusan létrehozott szám, amely azonosítja a kérések beérkezésének sorrendjét | Kérelem száma        |

## <a name="project-scheduling-service-error-logs"></a>A projektütemezési szolgáltatási hibanaplói

A Projektütemezési szolgáltatás hibanaplók rögzítik a Projektütemezési szolgáltatás **Mentés** és **Megnyitás** műveletének megkísérlésekor előforduló hibákat. Ezek a naplók három támogatott alkalmazási helyzetből vannak generálva:

- A felhasználó által indított műveletek végrehajtása kritikusan meghiúsul (például hiányzó jogosultságok miatt nem lehet hozzárendelést létrehozni).
- A Projektütemezési szolgáltatás nem tud programozott módon létrehozni, frissíteni, törölni vagy más kaszkádolt műveletet végrehajtani egy entitáson.
- A felhasználó hibát tapasztal, ha egy rekordnem nyílik meg (például projekt megnyitásakor vagy egy csoporttagjainak információinak frissítésekor).

### <a name="project-scheduling-service-log"></a>Projektütemezési szolgáltatás naplója

A következő táblázat mutatja a mezőket, amelyek szerepelnek a Projektütemezési szolgáltatás naplójában.

| Séma neve          | Description                                                                    | Megjelenített név    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A kivétel hívásverme.                                               | Hívásverem     |
| msdyn_correlationid | A hiba korrelációs azonosítója.                                               | CorrelationId  |
| msdyn_errorcode     | A Dataverse-hibakód vagy a HTTP-hibakód tárolására használt mező. | Hibakód     |
| msdyn_HelpLink      | A nyilvános súgódokumentációra mutató hivatkozás.                                       | Súgó hivatkozása      |
| msdyn_log           | A Projektütemezési szolgáltatás naplója.                                   | Napló            |
| msdyn_project       | A hibanaplóhoz társított projekt.                             | Project        |
| msdyn_projectName   | A projekt neve, ha a művelethalmaz hasznos terhelése megmarad. | Nem alkalmazható |
| msdyn_psserrorlogId | Az entitáspéldányok egyedi azonosítója.                                     | PSS-hibanapló  |
| msdyn_SessionId     | Projekt munkamenet-azonosítója.                                                        | Munkamenet-azonosító     |

## <a name="error-log-cleanup"></a>Hibanapló-törlés

Alapértelmezés szerint a Projektütemezési szolgáltatás hibanaplói és a Művelethalmaz naplója is 90 naponta an törölve. Minden 90 napnál régebbi rekord törlésre kerül. Azonban a **Projektparaméterek** oldalon az **msdyn_StateOperationSetAge** mező értékének módosításával a rendszergazdák módosíthatják a tisztítási tartományt úgy, hogy az 1 és 120 nap között legyen. Az érték módosítására többféle módszer áll rendelkezésre:

- Szabja testre a **Projektparaméter** entitást egy egyéni lap létrehozásával és az **Elavult műveletek korának beállítása** mezőjének hozzáadásával.
- A [WebApi szoftverfejlesztői készletet (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) használó ügyfélkód használata.
- A Modellalapú alkalmazásokban az Xrm SDK **updateRecord** metódust (ügyfél API reference) használó Service SDK-kód használata. A Power Apps leírást és a támogatott paramétereket tartalmazza a **updateRecord** metódushoz.

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
