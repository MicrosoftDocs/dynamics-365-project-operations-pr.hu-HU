---
title: A Project Service Automation szolgáltatásról Project Operations alkalmazás közötti funkcióváltozások
description: Ez a cikk áttekintést nyújt a szolgáltatás változásairól a Project Service Automationről a Dynamics 365 Project Operations.
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459929"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>A Project Service Automation szolgáltatásról Project Operations alkalmazás közötti funkcióváltozások

A Lite-ról Dynamics 365 Project Service Automation való Dynamics 365 Project Operations frissítés három fázisban történik. Ez a cikk azokról a főbb változásokról nyújt tájékoztatást, amelyekre számíthat, amikor a frissítés befejeződött.

| Frissítés kézbesítése | 1. fázis <br>(2022. január) | 2. fázis <br>(November 2022) | 3. fázis  |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség a projektek munkalebontási struktúrájától (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúrát a Project Operations jelenleg támogatott korlátai tartalmazzák. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| A munkalebontási struktúra a Project Operations jelenleg támogatott korlátain kívül esik, beleértve a Project asztali ügyfélprogramjának támogatását is. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektmenedzsment

A felhasználói élmény legjelentősebb változásai a projekttervezés területén lesznek. A Project Operations új, modern felhasználói élményt alkalmaz a munkalebontási struktúra (WBS) kezeléséhez a Project for the Web által [biztosított ütemezési képességek kihasználásával](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Az ütemezési élmény különbségei

Az alábbi táblázat összefoglalja a Project Service Automation és a Project Operations közötti ütemezési különbségeket.

|  Ütemezés     |   Project Operations   |   Psa   |
|-----------------|------------------------|---------|
| Projektsablonok – Projektsablonok definiálása és alkalmazása projektsablonok létrehozása a projekt létrehozásakor  |  &nbsp;    | :heavy_check_mark: |
| Projektmunka-bontási struktúra (WBS) integrációja asztali ügyféllel   |    &nbsp;  | :heavy_check_mark: |
| Megszorítások - Kezdés legkorábban, mint a következő időpontokban:  | :heavy_check_mark: |   &nbsp;  |
| Mérföldkövek – Nulla időtartamú feladatok   | :heavy_check_mark:  |  &nbsp;  |
| Az erőforrás-vezérelt tevékenységek tiszteletben tartják a hozzárendelt erőforrások rendelkezésre állását   | :heavy_check_mark: |  &nbsp;    |
| Időfázisos szerkesztés - Tervek szerkesztése és napi szintű munka   |   &nbsp;  | :heavy_check_mark: |
| Automatikus/manuális ütemezés – A Project ütemezési motorjának használata a tevékenységek automatikus vagy manuális ütemezéséhez |  &nbsp; | :heavy_check_mark:  |
| Nagy projektek szerkesztése közvetlenül a felhasználói felületen: Nincs korlátozva a szerkeszthető csomagok mérete  | 500 feladatkorlát  | :heavy_check_mark:       |
| Készültségi szint – Tevékenységállapot megjelölése   | :heavy_check_mark:  |  &nbsp;  |
| [Projektütemezési módok](../project-management/scheduling-modes.md) – A projekt meghatározása rögzített egységként, fix erőfeszítésként vagy rögzített időtartamként | :heavy_check_mark: | &nbsp; |
| Idővonal – Az idővonal-nézetet az ütemezés részleteinek megjelenítéséhez és az érdekelt felekkel való kommunikációhoz hozhatja létre és testre szabhatja. | :heavy_check_mark:  | &nbsp; |
| Erőfeszítésvezérelt feladatok – Motortámogatás ütemezése egy feladat erőfeszítésvezérelt ütemezéséhez  | :heavy_check_mark:  | &nbsp; |
| **Feladatinformáció** párbeszédpanel – Feladatadatok mentése párbeszédpanel használatával | :heavy_check_mark:  |  &nbsp;  |
| Fogd és vidd – Feladatok többszörös kiválasztása és pozíciójuk módosítása a munkalebontási struktúrán | :heavy_check_mark: | &nbsp;  |
| Rugalmas, állandó nézetek – A feladatattribútumok részletesebb nézeteinek definiálása   | :heavy_check_mark:  | &nbsp; |
| A munkalebontási struktúrából való kitárolás és szűrés  | :heavy_check_mark:  | &nbsp; |
| Táblák nézete a nem vízeséses projektek megvalósításához  | :heavy_check_mark:   | &nbsp; |
| Idővonal nézet – A WBS vizualizálásához és szerkesztéséhez használt interaktív Gantt-diagram   | :heavy_check_mark:  | &nbsp; |
| Billentyűparancsok – Billentyűparancsok használata a gyakori műveletekhez, például behúzáshoz vagy beszúráshoz  | :heavy_check_mark:  |  &nbsp; |
| Többszintű visszavonás – Lehetőségelemzés végrehajtása a módosítások hatásának teljes megértéséhez a műveletek teljes készletének megfordításával és újraalkalmazásával | :heavy_check_mark: | &nbsp; |
| Kivágás/másolás/beillesztés – Együttműködés az ütemezési fejlesztésben az ütemezés részleteinek az alkalmazások közötti másolásával és beillesztésével  | :heavy_check_mark: | &nbsp; |
| Feladat-ellenőrzőlisták – Legfeljebb 20 ellenőrzőlista elem hozzáadása egy feladathoz   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekt tervezése

A **Project Operations Projekt** lapja jelentős számú eltérést mutat a **Project Service Automation Projekt** oldalához képest.

A következő műveletek el lettek távolítva a **Projektek** lapról az 1. fázisú frissítés részeként:

  - **Megnyitás MS Projectben**
  - **Sablon létrehozása**
  - **MS Project-kapcsolat megszüntetése**

A **Project Operations Projekt** lapja a következő új lapokat tartalmazza.

- **Anyagbecslések**
- **Feladat számlázási beállítása**

Az **Állapot** lap el lett távolítva, és az **Állapot** mező most az **Összegzés** lapon található a projekt ütemezési módjával.

   ![Frissítések a Projekt laphoz.](media/projectform.png)

Az **Ütemezés** lap új lett átnevezve a **Tevékenység** lapra, és az új projekttervezési élményt a Project for the Web szolgáltatással mutatja be.

   ![Új Projekttevékenységek lap.](media/tasktab.png)

## <a name="scheduling-modes"></a>Ütemezési módok

A Project Operations bevezetett egy új funkciót, az [Ütemezési módokat](../project-management/scheduling-modes.md). Az összes meglévő Project Service Automation-projekt alapértelmezés szerint rögzített időtartamú **lesz a** Projektműveletekben. Az új projektek alapértelmezett értéke azonban kezelhető a Beállítások **paraméterei paraméterütemezési** > **módba** > **való belépéssel** > **·**.

   ![A Project paraméterbeállításai ütemezési módhoz.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekttervezési korlátok

A Project Operations a Project for the Webre támaszkodik minden projektütemezési művelethez. A Webes Projekt az alábbi táblázatban szereplő korlátok alapján kezeli a munkalebontási struktúrát.

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

## <a name="project-planning-extensibility-and-development"></a>Projekttervezés bővíthetősége és fejlesztése

Miután frissített a Project Operationsre, a Projektütemezés API-kat kell használnia a létrehozási, frissítési és törlési műveletek végrehajtásához a következő entitásokon:

|   Entitás neve           |   Entitás logikai neve       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektfeladat            | msdyn_projecttask           |
| Projektfeladat függősége | msdyn_projecttaskdependency |
| Erőforrás-hozzárendelés     | msdyn_resourceassignment    |
| Projektgyűjtő          | msdyn_projectbucket         |
| Projektcsoporttag     | msdyn_projectteam           |

Ha jelenleg olyan testreszabásokkal rendelkezik, amelyek ezeket az entitásokat érintik, a megvalósítási útmutatóért lásd: [Projektütemezési API-k használata műveletek végrehajtásához ütemezési entitásokkal](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Az adatmodell változásai

Az 1. frissítési fázis részeként az adatmodell módosul. Ezek a változások elsősorban a meglévő entitások mezőváltozásai. Az 1. fázisban az entitások, **a msydn_project** és **a msdyn_projectteam** a testreszabások újrabontása. 

> [!IMPORTANT]
> Ez a szakasz további entitásokkal frissül, ahogy a jövőbeli frissítési fázisok befejeződnek.

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

A következő mezők lettek hozzáadva.

|   Entity          |   Logikai név                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | A projekten belüli tényleges díjeladások összesítését jeleníti meg. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_actualmaterialcost                     | A projekt tényleges anyagköltségének összesítését jeleníti meg. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_actualmaterialsales                    | A projekt tényleges anyageladásainak összesítését jeleníti meg. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | A projekthez társított szerződéssor. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ez egy belső rendszermező, amely a Korrelációs azonosítóhoz kapcsolódó Copy Projecthez **használatos**. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ez egy belső rendszermező, amely a munkamenet-azonosítóhoz kapcsolódó Copy Projecthez **használatos**. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Utoljára szinkronizálja az xRM globális revíziós tokent a Projektütemezés szolgáltatásból. |
| msdyn_project     | msdyn_msprojectdocument                      | A projekthez tartozó Microsoft Project-dokumentum. |
| msdyn_project     | msdyn_plannedmaterialcost                    | A projekt tervezett anyagköltségének összesítése. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_plannedmaterialsales                   | A projekt tervezett anyagértékesítésének összesítése. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_program                                | A program, amelyhez ez a projekt kapcsolódik. |
| msdyn_project     | msdyn_quotelineproject                       | A projekthez társított Idézet sor. |
| msdyn_project     | msdyn_replaylogheader                        | A visszajátszási naplók fejléce. |
| msdyn_project     | msdyn_schedulemode                           | A projekt összes tevékenységéhez használt alapértelmezett ütemezési mód.  |
| msdyn_project     | msdyn_taskearlieststart                      | A projekt bármely feladatának legkorábbi kezdési dátuma.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | A projektcsapat tagja, akitől a projektcsapat tagja másolt. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Azt jelzi, hogy létre kell-e hozni az erőforrás-követelményt egy újonnan létrehozott általános csapattag számára.  |
| msdyn_projectteam | msdyn_deletestatus                           | A csapattag törlési állapota annak nyomon követéséhez, hogy van-e elküldve törlési kérelem a Projekt ütemezési szolgáltatásának, és hogy sikeresen küld-e választ a várt időablakon belül. |
| msdyn_projectteam | msdyn_effortcompleted                        | Nyomon követi a csapattag által a feladataik során elért erőfeszítéseket. |
| msdyn_projectteam | msdyn_effortremaining                        | Nyomon követi a csapattag által a feladataikkal kapcsolatban még elvégzendő erőfeszítéseket. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | A várakozási idő attól kezdve, hogy a csapattag törlési kérelmet küld a Projekt ütemezési szolgáltatásának, amíg a csapattag ténylegesen törlődik Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Az időbélyeg, amelyet rögzíteni kell, amikor a csapattag törlési kérelmét elküldi a projekt ütemezési szolgáltatásának. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Megjeleníti azt a projektcsoporttagot, akiről ezt a projektcsoporttagot másolták.  |

## <a name="project-templates"></a>Projektsablonok

A Project Operations nem támogatja a projektsablonokat. A Project Copy API használatával [azonban az alapvető funkciók nagy részét replikálhatja](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Asztali bővítmény támogatása

A Microsoft Project Desktop bővítmény támogatása nem lesz elérhető a frissítés első 2 fázisában. A 3. fázisban azok az ügyfelek, akiknek a projektjei nagyobbak, mint a Webes Project jelenleg támogatott korlátai, használhatják az asztali bővítményt.

## <a name="editing-resource-assignment-contours"></a>Erőforrás-hozzárendelési eloszlások szerkesztése

Az erőforrás-hozzárendelési eloszlások szerkesztésének lehetősége akkor lesz elérhető, ha a frissítés 2. fázisa elérhető.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A következő új funkciók lettek hozzáadva a Project Operationshez. Ezek a funkciók additív jellegűek, és nincsenek hatással a Project Service Automation adatmodelljére.

- [Anyaghasználat rögzítése projekteken és projektfeladatokon](../material/material-usage-log.md)
- [Alvállalkozói szerződések kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [A szerződés állapota és érvényesítése nem haladhatja meg a státuszt és az érvényesítést](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Feladatalapú számlázás](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Elavult összetevők

Az alábbi táblázatok az összes elavult mezőt dokumentálják, amelyek a frissítés után átkerülnek az elavult összetevők megoldásába. További információ és a megoldásra [Dynamics 365 Project Service Automation mutató hivatkozás: 3x a Project Operations 4x elavult összetevőire](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

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
| msdyn_characteristicreqforteammember.msdyn_jellemzőreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_jellemzőtípus                                 |
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
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
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
| msdyn_opportunitylinetransaction.msdyn_documentdate fájl                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_százalék                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_árlista                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_projekt                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

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
| msdyn_project.msdyn_szakasznév                                                                 |
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
| msdyn_projecttask.msdyn_number ofsources                                                     |
| msdyn_projecttask.msdyn_megmaradthours                                                        |
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
| msdyn_projecttaskstatususer.msdyn_várta, hogy teljesítsen                                     |
| msdyn_projecttaskstatususer.msdyn_is befejeződött                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_kérelmező száma                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
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
| msdyn_projecttransactioncategory.msdyn_projekt                                                |
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
| msdyn_resourceassignment.msdyn_óra                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name (angolul)                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid fájlt                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

