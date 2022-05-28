---
title: Szolgáltatásmódosítások a projektszolgáltatás automatizálásáról a projektműveletekre
description: Ez a témakör áttekintést nyújt a Szolgáltatás automatizálásáról a programra történő váltásokról Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595409"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Szolgáltatásmódosítások a projektszolgáltatás automatizálásáról a projektműveletekre

A Lite-ról Dynamics 365 Project Service Automation a Lite-ra Dynamics 365 Project Operations való frissítés három fázisban történik. Ez a témakör tájékoztatást nyújt azokról a főbb változásokról, amelyek a frissítés befejezésekor várhatók.

| Frissítési kézbesítés | 1. fázis <br>(2022. január) | 2. fázis <br>(2022. áprilisi hullám) | 3. fázis  |
|------------------|------------------------|---------------------------|---------------------------|
| A projektek munkalebontási struktúrájától (WBS) nem függ. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A WBS a projektműveletek jelenleg támogatott korlátai közé tartozik. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| A WBS kívül esik a Project Operations jelenleg támogatott korlátain, beleértve az asztali Project ügyfél támogatását is. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektmenedzsment

A felhasználói élményben a legjelentősebb változások a projekttervezés területén lesznek. A Project Operations új, modern élményt nyújt a munkalebontási struktúra (WBS) kezeléséhez a Project for the Web által [biztosított ütemezési képességek kihasználásával](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Az ütemezési élmény különbségei

Az alábbi táblázat a Project Service Automation és a Project Operations közötti ütemezési különbségeket foglalja össze.

|  Ütemezés     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektsablonok – Projektsablonok definiálásának és alkalmazásának képessége projekt létrehozásakor  |  &nbsp;    | :heavy_check_mark: |
| Projektmunka-bontási struktúra (WBS) integrációja asztali ügyféllel   |    &nbsp;  | :heavy_check_mark: |
| Megkötések – Legkorábban kezdődjön, de legkésőbb  | :heavy_check_mark: |   &nbsp;  |
| Mérföldkövek - Nulla időtartamú tevékenységek   | :heavy_check_mark:  |  &nbsp;  |
| Az erőforrás-alapú tevékenységek tiszteletben tartják a hozzárendelt erőforrások rendelkezésre állását   | :heavy_check_mark: |  &nbsp;    |
| Időfázisos szerkesztés - Tervek szerkesztése és napi munka   |   &nbsp;  | :heavy_check_mark: |
| Automatikus/kézi ütemezés – A Projektek ütemezési motorral automatikusan vagy manuálisan ütemezheti a tevékenységeket |  &nbsp; | :heavy_check_mark:  |
| Nagy projektek szerkesztése közvetlenül a felhasználói felületen: A szerkeszthető tervek méretére nincs korlátozás  | 500 tevékenységkorlát  | :heavy_check_mark:       |
| Készültségi szint – Tevékenység állapotának megjelölése   | :heavy_check_mark:  |  &nbsp;  |
| [Projektütemezési módok](../project-management/scheduling-modes.md) – A projekt meghatározása rögzített egységként, rögzített erőfeszítésként vagy rögzített időtartamként | :heavy_check_mark: | &nbsp; |
| Idővonal – Az ütemterv nézetének létrehozása és testreszabása az ütemezés részleteinek megjelenítéséhez és az érdekelt felekkel való kommunikációhoz. | :heavy_check_mark:  | &nbsp; |
| Munkamennyiség-vezérelt feladatok – A tevékenység munkamennyiség-vezérelt ütemezésének ütemezése  | :heavy_check_mark:  | &nbsp; |
| **Feladat adatai** párbeszédpanel – Feladat részleteinek mentése párbeszédpanelen | :heavy_check_mark:  |  &nbsp;  |
| Fogd és vidd - Feladatok többszörös kijelölése és pozíciójuk módosítása a WBS-en | :heavy_check_mark: | &nbsp;  |
| Rugalmas állandó nézetek – Tevékenységattribútumok részletesebb nézeteinek meghatározása   | :heavy_check_mark:  | &nbsp; |
| A WBS rendezése és szűrése  | :heavy_check_mark:  | &nbsp; |
| Táblák nézete a nem vízesés projekthez  | :heavy_check_mark:   | &nbsp; |
| Idővonal nézet – Interaktív Gantt-diagram a WBS megjelenítéséhez és szerkesztéséhez   | :heavy_check_mark:  | &nbsp; |
| Billentyűparancsok – Billentyűparancsok használata gyakori műveletekhez, például behúzáshoz vagy beszúráshoz  | :heavy_check_mark:  |  &nbsp; |
| Többszintű visszavonás - Végezzen "mi lenne, ha" elemzést, hogy teljes mértékben megértse a változások hatását a műveletek teljes készletének megfordításával és újra alkalmazásával | :heavy_check_mark: | &nbsp; |
| Kivágás/másolás/beillesztés – Együttműködés az ütemezés fejlesztésében az ütemezés részleteinek másolásával és beillesztésével az alkalmazások között  | :heavy_check_mark: | &nbsp; |
| Feladat-ellenőrzőlisták – Legfeljebb 20 ellenőrzőlistaelem hozzáadása egy tevékenységhez   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekt tervezése

A **Projektműveletek projektlapján** jelentős különbségek vannak a **Project szolgáltatás automatizálása Projekt** lapjához képest.

Az 1. fázisú frissítés részeként a **következő műveletek lettek eltávolítva a Projektek** lapról:

  - **Megnyitás MS Projectben**
  - **Sablon létrehozása**
  - **MS Project-kapcsolat megszüntetése**

A **Projektműveletek projektlapja** a következő új lapokat tartalmazza.

- **Anyagbecslések**
- **Feladat számlázási beállítása**

Az **Állapot** lap el lett távolítva, és az **Állapot** mező most az **Összegzés** lapon van a projekt ütemezési módjával.

   ![A Projekt lap frissítései.](media/projectform.png)

Az **Ütemezés** lap átnevezésre került a **Tevékenység** lapra, és a Project for the Web új projekttervezési élményét tartalmazza.

   ![Új Projekttevékenységek lap.](media/tasktab.png)

## <a name="scheduling-modes"></a>Ütemezési módok

A Project Operations új funkciót vezetett be, [az Ütemezési módokat](../project-management/scheduling-modes.md). Az összes meglévő Project Service Automation projekt alapértelmezés szerint Rögzített időtartam **lesz a** Projektműveletekben. Az új projektek alapértelmezett értéke azonban a Beállítások **paraméterek** > **paraméterütemezési** > **módra** > **kattintva** kezelhető.

   ![Projektparaméter-beállítások ütemezési módhoz.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekttervezési korlátok

A Project Operations a Project for the Web szolgáltatásra támaszkodik az összes projektütemezési művelethez. A Project for the Web az alábbi táblázat korlátaival kezeli a munkalebontási struktúrát.

| **Mező**                                          | **Korlát**             |
|----------------------------------------------------|-----------------------|
| Projekt maximális összfeladata                  | 500                   |
| Projekt maximális összidőtartama               | 3650 nap (10 év)  |
| Maximális teljes erőforrás egy projekthez              | 300                   |
| A linkek maximális száma (csak utód) egy projekthez | 600                   |
| Maximális teljes egyéni mezők egy projekthez          | 10                    |
| Maximális hierarchiaszint                            | 10 szint             |
| Maximális hivatkozások (utód + előzmény)            | 20                    |
| A feladat maximális időtartama                      | 1250 nap             |
| Az összesítő feladat maximális időtartama                 | 3650 nap (10 év)  |
| Egy feladathoz rendelt maximális erőforrások               | 20 erőforrás          |
| Támogatott dátumtartomány egy feladathoz                    | 1/1/2000 - 12/31/2149 |
| Ellenőrzőlista elemei                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projekttervezés bővíthetőség és fejlesztés

A Project Operations szolgáltatásra való frissítés után a Project Scheduling API-kat kell használnia a létrehozási, frissítési és törlési műveletek végrehajtásához a következő entitásokon:

|   Entitás neve           |   Entitás logikai neve       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektfeladat            | msdyn_projecttask           |
| Projektfeladat függősége | msdyn_projecttaskdependency |
| Erőforrás-hozzárendelés     | msdyn_resourceassignment    |
| Projektgyűjtő          | msdyn_projectbucket         |
| Projektcsoporttag     | msdyn_projectteam           |

Ha jelenleg olyan testreszabásokkal rendelkezik, amelyek magukban foglalják ezeket az entitásokat, olvassa el a Project ütemezési API-k használata az ütemezési entitásokkal [végzett műveletek végrehajtásához című témakört](../project-management/schedule-api-preview.md) a megvalósítási útmutatáshoz.

## <a name="data-model-changes"></a>Adatmodell-módosítások

Az 1. frissítési fázis részeként módosul az adatmodell. Ezek a módosítások elsősorban a meglévő entitások mezőmódosításai. Az 1. fázisban az entitások, **a msydn_project** és **a msdyn_projectteam** a testreszabások újrafaktorozását jelentik. 

> [!IMPORTANT]
> Ez a szakasz a jövőbeli frissítési fázisok befejezésekor további entitásokkal frissül.

A következő mezőket új mezők váltották fel.

|   Entity          |   Régi logikai név   |   Új logikai név    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

A program a következő mezőket adta hozzá.

|   Entity          |   Logikai név                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | A projekt tényleges díjeladásainak összességét jeleníti meg. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_actualmaterialcost                     | A projekt tényleges anyagköltségének összességét mutatja. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_actualmaterialsales                    | A projekt tényleges anyageladásainak összességét mutatja. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | A projekthez társított szerződéssor. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ez egy belső rendszermező, amelyet a Korrelációs azonosítóhoz kapcsolódó Projekt **másolásakor** használnak. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ez egy belső rendszermező, amelyet a munkamenet-azonosítóhoz kapcsolódó Projekt **másolásakor** használnak. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Utolsó szinkronizálás xRM globális verzió jogkivonat a Projektütemezési szolgáltatásból. |
| msdyn_project     | msdyn_msprojectdocument                      | A projekthez tartozó Microsoft Project dokumentum. |
| msdyn_project     | msdyn_plannedmaterialcost                    | A projekt tervezett anyagköltségének összesítése. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_plannedmaterialsales                   | A projekt tervezett anyagértékesítéseinek összesítése. Csak a Project Service Automation alkalmazásban használható. |
| msdyn_project     | msdyn_program                                | A program, amelyhez ez a projekt kapcsolódik. |
| msdyn_project     | msdyn_quotelineproject                       | A projekthez társított Ajánlat sor. |
| msdyn_project     | msdyn_replaylogheader                        | A visszajátszási naplók fejléce. |
| msdyn_project     | msdyn_schedulemode                           | A projekt összes tevékenységéhez használt alapértelmezett ütemezési mód.  |
| msdyn_project     | msdyn_taskearlieststart                      | A projekt bármely feladatának legkorábbi kezdési dátuma.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Az a projektcsapat-tag, akiből a projektcsapat-tagot másolták. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Azt jelzi, hogy létre kell-e hozni az erőforrás-szükségletet egy újonnan létrehozott általános csapattaghoz.  |
| msdyn_projectteam | msdyn_deletestatus                           | A csoporttag törlési állapota annak nyomon követésére, hogy van-e törlési kérelem elküldve a Projektütemezési szolgáltatásnak, és hogy sikeresen visszaküldi-e a választ a várt időablakon belül. |
| msdyn_projectteam | msdyn_effortcompleted                        | Nyomon követi a csapattag által a feladataik során elért erőfeszítéseket. |
| msdyn_projectteam | msdyn_effortremaining                        | Nyomon követi a csapattag által a feladataikra még be nem fejezett erőfeszítéseket. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Az a várakozási idő, amelytől kezdve a csapattag törlési kérelmet küld a Projektütemezési szolgáltatásnak, amíg a csapattag ténylegesen törlődik a programból Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Az időbélyeg, amelyet a csapattag törlési kérelmének a Project ütemezési szolgáltatásba történő elküldésekor rögzít. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Megjeleníti azt a projektcsoporttagot, akiről ezt a projektcsoporttagot másolták.  |

## <a name="project-templates"></a>Projektsablonok

A Project Operations nem támogatja a projektsablonokat. A Project Copy API használatával azonban replikálhatja az alapvető funkciók nagy [részét](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Asztali bővítmény támogatása

A Microsoft Project Desktop bővítmény támogatása a frissítés első két fázisában nem lesz elérhető. A 3. fázisban azok az ügyfelek, akik a Project for the Web jelenleg támogatott korlátainál nagyobb projektekkel rendelkeznek, használhatják az asztali bővítményt.

## <a name="editing-resource-assignment-contours"></a>Erőforrás-hozzárendelési kontúrok szerkesztése

Az erőforrás-hozzárendelési kontúrok szerkesztésének lehetősége akkor lesz elérhető, ha a frissítés 2. fázisa elérhető.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A project műveletekben a következő új funkciók kerültek hozzáadásra. Ezek a funkciók additív jellegűek, és nem befolyásolják a Project Service Automation adatmodellt.

- [Projektek és projektfeladatok anyagfelhasználásának rögzítése](../material/material-usage-log.md)
- [Alvállalkozói tevékenység kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [A szerződés állapota és érvényesítései nem lépik túl az állapotot és az ellenőrzéseket](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Feladatalapú számlázás](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Elavult összetevők

Az alábbi táblázatok az összes elavult mezőt dokumentálják, amelyek a frissítés után az elavult összetevők megoldásába kerülnek. További információt és a megoldásra mutató hivatkozást a 3x to Project Operations 4x elavult összetevők [Dynamics 365 Project Service Automation című témakörben talál](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_jellemző                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcekategória                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_összeg                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_százalék                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcekategória                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactionkategória                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype típus                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percent teljes                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_pályázókava elérhető                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_szám                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

