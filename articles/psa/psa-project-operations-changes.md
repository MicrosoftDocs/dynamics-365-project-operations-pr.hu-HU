---
title: A Project Service Automation szolgáltatásról Project Operations alkalmazás közötti funkcióváltozások
description: A cikk áttekintést a Project Service Automation és a Dynamics 365 Project Operations közötti változásokról ad tájékoztatást.
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

A Dynamics 365 Project Service Automation és a Dynamics 365 Project Operations Lite közötti frissítés három fázisban lesz szállítva. Ez a cikk a frissítés befejezésére várható főbb változásokról nyújt tájékoztatást.

| Frissítés kézbesítése | 1. fázis <br>(2022. január) | 2. fázis <br>(2022. november) | 3. fázis  |
|------------------|------------------------|---------------------------|---------------------------|
| Nincs függőség projektek munkalebontási struktúrájával (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS a Project Operations jelenleg támogatott korlátaiban szerepel. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS a Project Operations jelenleg támogatott korlátain kívül, beleértve a Project Desktop Client támogatását is. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektmenedzsment

A felhasználói élményben a legfontosabb változás a projekttervezés területén lesz. A Project Operations a [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) által biztosított ütemezési lehetőségekre építve új, modern élményt nyújt a munkalebontási struktúra kezeléséhez.

## <a name="differences-in-the-scheduling-experience"></a>Az ütemezési élmény eltérései

Az alábbi táblázat az ütemezés különbségeit foglalja össze a Project Service Automation és a Project Operations között.

|  Ütemezés     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektsablonok – Projektsablonok definiálhatók és alkalmazhatók a projekt létrehozásakor  |  &nbsp;    | :heavy_check_mark: |
| Projekt munkalebontási struktúra (WBS) integrációja az asztali ügyfélprogrammal   |    &nbsp;  | :heavy_check_mark: |
| Megkötések – Nem kezdődhet korábban, és fejeződhet be később  | :heavy_check_mark: |   &nbsp;  |
| Mérföldkövek – Nulla időtartamú feladatok   | :heavy_check_mark:  |  &nbsp;  |
| Az erőforrás alapú feladatok a hozzárendelt erőforrások rendelkezésre állását be fogják tartani   | :heavy_check_mark: |  &nbsp;    |
| Időszakos szerkesztés – A tervek és a munka szerkesztése napi szinten   |   &nbsp;  | :heavy_check_mark: |
| Automatikus/manuális ütemezés – A feladatok automatikus vagy manuális ütemezése a Projektütemezési motor segítségével |  &nbsp; | :heavy_check_mark:  |
| Nagy projektek szerkesztése közvetlenül a felhasználói felületen: A szerkeszthető tervek méretére vonatkozóan nincs korlátozás  | 500 feladatos korlát  | :heavy_check_mark:       |
| Készültségi százalék – A feladatok előrehaladásának jelölése   | :heavy_check_mark:  |  &nbsp;  |
| [Projekt ütemezési módok](../project-management/scheduling-modes.md) – A projekt definiálása rögzített egységekként, rögzített erőfeszítésként vagy rögzített időtartamként | :heavy_check_mark: | &nbsp; |
| Idősor – Idővonalnézet létrehozása és testreszabása az ütemezés részleteinek megjelenítéséhez és az résztvevőkkel folytatott kommunikációhoz. | :heavy_check_mark:  | &nbsp; |
| Erőfeszítésre épülő feladatok – Az ütemezési motor támogatja egy feladat munkamennyiség alapúként ütemezését  | :heavy_check_mark:  | &nbsp; |
| **Feladatinformációk** párbeszédpanel – A feladatok részleteinek mentése egy párbeszédpanel használatával | :heavy_check_mark:  |  &nbsp;  |
| Fogd és vidd – Kijelölhet több feladatot, és módosíthatja pozíciójukat a WBS-ben | :heavy_check_mark: | &nbsp;  |
| Rugalmas állandó nézetek – a feladatattribútumok granuláltabb nézeteinek definiálásához   | :heavy_check_mark:  | &nbsp; |
| A WBS szűrése és rendezése  | :heavy_check_mark:  | &nbsp; |
| A táblák néz projekt teljesítéséhez nem vízesés elven  | :heavy_check_mark:   | &nbsp; |
| Idővonal nézet – A WBS megjelenítésére és szerkesztésére használt interaktív Gantt-diagram   | :heavy_check_mark:  | &nbsp; |
| Billentyűparancsok – Billentyűparancsok a gyakori műveletekhez, például behúzáshoz vagy beszúráshoz  | :heavy_check_mark:  |  &nbsp; |
| Többszintű visszavonás – Ha-akkor elemzés végrehajtása a változtatások hatásának teljes kiértékeléséhez, a műveletek teljes halmazának megfordításával és újbóli alkalmazásával | :heavy_check_mark: | &nbsp; |
| Kivágás/másolás/beillesztés – Együttműködés az ütemezésé kidolgozásában az ütemezés részleteinek alkalmazások közötti másolásával és beillesztésével  | :heavy_check_mark: | &nbsp; |
| Feladat-ellenőrzőlisták – Akár 20 feladatlista-elem felvétele egy feladathoz   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekt tervezése

A Project Operations **Projekt** oldalán számos különbséggel tapasztalható a Project Service Automation **Projekt** oldalához képest.

A következő műveleteket el lettek távolítva a **Projektek** oldalról az 1. fázisú frissítésben:

  - **Megnyitás MS Projectben**
  - **Sablon létrehozása**
  - **MS Project-kapcsolat megszüntetése**

A Project Operations **Projekt** oldalán a következő új lapok jelentek meg.

- **Anyagbecslések**
- **Feladat számlázási beállítása**

Az **Állapot** lap el lett távolítva, és az **Állapot** mező most az **Összegzés** lapon látható a projekt ütemezési módjával.

   ![A Projekt oldal frissítései.](media/projectform.png)

Az **Ütemezés** lap át van nevezve a **Feladat** lapra, és a Project for the Web új projekttervezési élményét tartalmazza.

   ![Új Projekt feladatok lap.](media/tasktab.png)

## <a name="scheduling-modes"></a>Ütemezési módok

A Project Operations új szolgáltatást, az [Ütemezési módokat](../project-management/scheduling-modes.md) vezette be. Alapértelmezés szerint minden meglévő Project Service Automation-projekt **Rögzített időtartamú** lesz a Project Operationsben. Az új projektek alapértelmezése azonban a **Beállítások** > **Paramétere** > **Paraméter** > **Ütemezési mód** menüben kezelhető.

   ![Projektparaméter-beállítások az Ütemezési módhoz.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekttervezési korlátok

A Project Operations minden projektütemezési művelethez a Project for The Web szolgáltatásra támaszkodik. A Project for the Web az alábbi táblázatban található korlátok alkalmazásával a munkalebontási struktúrát.

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

A Project Operations alkalmazásra való frissítést követően a projektütemezési API-kat kell használnia végrehajtási, létrehozási, frissítési és törlési műveletekhez a következő entitások esetén:

|   Entitás neve           |   Entitás logikai neve       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektfeladat            | msdyn_projecttask           |
| Projektfeladat függősége | msdyn_projecttaskdependency |
| Erőforrás-hozzárendelés     | msdyn_resourceassignment    |
| Projektgyűjtő          | msdyn_projectbucket         |
| Projektcsoporttag     | msdyn_projectteam           |

Ha jelenleg olyan testreszabásai vannak, amelyek ezeket az entitásokat érintik, a megvalósítással kapcsolatos útmutatásért lásd: [Ütemezési API-k használata műveletek elvégzéséhez az ütemezési entitásokkal](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Adatmodell változásai

Az 1. frissítési fázis részeként módosul az adatmodell. Ezek a változtatások elsősorban a meglévő entitások mezőváltozása. Az 1. fázisban az **msydn_project** és **msdyn_projectteam** entitások testreszabások refaktorálásai. 

> [!IMPORTANT]
> Ez a szakasz a későbbi frissítés fázisai során további entitásokkal bővül.

A következő mezőket új mezők váltják fel.

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
| msdyn_project     | msdyn_actualfeesales                         | Megjeleníti a projekt összesített tényleges díjértékesítését. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_actualmaterialcost                     | Megjeleníti a projekt összesített tényleges anyagköltségét. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_actualmaterialsales                    | Megjeleníti a projekt összesített tényleges anyagértékesítését. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | A projekthez társított szerződéssor. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ez egy belső rendszermező, amely a korrelációs azonosítóhoz kapcsolatos **Projekt másoláshoz** használatos. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ez egy belső rendszermező, amely a munkamenet-azonosítóhoz kapcsolatos **Projekt másoláshoz** használatos. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Utolsó szinkronizálás xRM globális felülvizsgálási lexikális eleme a Projektütemezés szolgáltatásból. |
| msdyn_project     | msdyn_msprojectdocument                      | A projekthez tartozó Microsoft Project-dokumentum. |
| msdyn_project     | msdyn_plannedmaterialcost                    | A projekt összesített tervezett anyagköltsége. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_plannedmaterialsales                   | A projekt összesített tervezett anyagértékesítése. Csak a Project Service Automationben használható. |
| msdyn_project     | msdyn_program                                | A program, amelyhez ez a projekt kapcsolódik. |
| msdyn_project     | msdyn_quotelineproject                       | A projekthez társított árajánlatsor. |
| msdyn_project     | msdyn_replaylogheader                        | A visszajátszási naplók fejléce. |
| msdyn_project     | msdyn_schedulemode                           | A projekthez tartozó összes feladatnál használt alapértelmezett ütemezési mód.  |
| msdyn_project     | msdyn_taskearlieststart                      | A projekt bármely feladatának legkorábbi kezdési dátuma.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Az a projektcsoporttag, akiről ezt a projektcsoporttagot másolták. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Jelzi, hogy létre szeretné-e hozni az újonnan létrehozott általános csoporttag erőforrás-követelményét.  |
| msdyn_projectteam | msdyn_deletestatus                           | A csoporttag törlési állapotával nyomon követheti, hogy van-e a Projektütemezési szolgáltatásnak küldött törlési kérelem, illetve, hogy az sikeresen visszaküldte-e a választ a várt időkereten belül. |
| msdyn_projectteam | msdyn_effortcompleted                        | A csoporttag feladattal kapcsolatos elvégzett munkamennyiséget követi nyomon. |
| msdyn_projectteam | msdyn_effortremaining                        | A csoporttag feladattal kapcsolatos, elvégzendő munkamennyiséget követi nyomon. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Várakozási idő attól kezdve amikor a csoporttag törlési kérelmet küld a Projektütemezési szolgáltatásnak, amíg a csoporttagot valójában törlik a Microsoft Dataverse-ből.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Az a lejegyzendő időbélyeg, amikor a csoporttag törlési kérelmét elküldték a Projektütemezési szolgáltatásnak. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Megjeleníti azt a projektcsoporttagot, akiről ezt a projektcsoporttagot másolták.  |

## <a name="project-templates"></a>Projektsablonok

A Project Operations nem támogatja a projektsablonokat. Az alapfunkciók nagy része azonban replikálható a [Projektmásolás API](../project-management/dev-copy-project.md) használatával.

## <a name="desktop-add-in-support"></a>Asztali bővítmény támogatása

A Microsoft Project asztali bővítmény támogatása nem lesz elérhető a frissítés első 2 szakaszában. A 3. fázisban azok az ügyfelek, akik a Project for the Web jelenleg támogatott korlátainál nagyobb projektekkel rendelkeznek használhatják az asztali bővítményt.

## <a name="editing-resource-assignment-contours"></a>Erőforrás-hozzárendelési kontúrok szerkesztése

Az erőforrás-hozzárendelési kontúrok módosítási lehetősége akkor lesz elérhető, ha a frissítés 2. fázisa elérhető lesz.

## <a name="billing-and-pricing"></a>Számlázás és árképzés

A következő új funkciók lettek hozzáadva a Project Operations szolgáltatáshoz. Ezek a szolgáltatások additív jellegűek, és nincsenek hatással a Project Service Automation adatmodellre.

- [Anyaghasználat rögzítése projekteknél és projektfeladatoknál](../material/material-usage-log.md)
- [Alvállalkozók kezelése](../pro/subcontracting/managing-subcontracts-overview.md)
- [Foglalón alapuló szerződések beállítása](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Nem meghaladandó állapot és ellenőrzések szerződésen](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Feladat alapú számlázás](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Elavult összetevők

Az alábbi táblázatok minden elavult mezőt dokumentálnak, amelyek átkerülnek az elavult összetevők megoldásába a frissítés után. A további információk és a megoldásra mutató hivatkozás kapcsán lásd: [Dynamics 365 Project Service Automation 3x és Project Operations 4x közötti elavult összetevők](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

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
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
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
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
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
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Mezők                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
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

