---
title: Entitás, vezérlés és a felhasználói felület változásai (Project Service Automation 3.x)
description: Ez a cikk leírja a Microsoft Dynamics Project Service Automation 3.x megoldásbeli változásait.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926871"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Entitás, vezérlés és a felhasználói felület változásai (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


A Service Project Service Automation (PSA) 3.x Microsoft Dynamics kiadásával számos változtatást hajtottak végre az entitásokban, a vezérlőkben, a nézetekben és a felhasználói felületen. Ez a cikk információkat nyújt ezekről a fontos változásokról.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>A szülő-gyermek kapcsolatok értékesítési dokumentumokhoz, értékesítési dokumentumsorokhoz, értékesítési dokumentumsorokhoz tartozó entitások
A Dynamics 365 Project Service Automation (PSA) 3.0 verzió megjelenése előtti verziókban az értékesítési dokumentumok, az értékesítési dokumentumsorok és az értékesítési dokumentumsorok részletek entitások közötti egyes kapcsolatok olyan karakterlánc-mezők segítségével valósultak meg, amelyek a kapcsolódó entitás karakterlánc GUID-jének karakterlánc reprezentációját tartalmazták. Ennek oka a platform korlátai voltak, amelyek miatt jelentős egyedi kód volt szükséges a megoldás szerver- és kliens oldalán ahhoz, hogy ezek a kapcsolatok hasonlóan működjenek a tipikus Dynamics CRM-entitáskapcsolatokkal, és hogy a karakterláncmezők úgy működjenek, mint keresési mezők.

A PSA 3.0 frissítésének célja, hogy kiaknázza az értékesítési dokumentum és az értékesítési dokumentumsor entitásai közötti új entitáskapcsolatokat.

Mivel a keresési mezők mostantól az entitásokra való hivatkozások jelzésére használhatók, a korábbi verziókban a kapcsolódó entitás GUID-jének karakterláncértékét megtartó mezőkre már nincs szükség, és ezért elavultak. Az egyéni kliens és a szerveroldali kód, amely az örökölt karakterláncmezők által meghatározott kapcsolatokat kezeli, szintén elavult.

### <a name="entity-schema-changes"></a>Az entitás sémájában történt változások
Az alábbi táblázat az elavult karakterláncmezők és az entitások új keresési mezőinek egy az egyhez listáját tartalmazza. 

 Entitás |   Elavult mező (karakterlánc) | Új mező (keresés)
--- | --- | ---
invoicedetail (számlasor) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Téynadat) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Projekt szerződéssori számlaütemezése) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Projektszerződéssori mérföldkő) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Tény) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Számlasor részlete) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Naplósor) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Projektszerződéssori erőforrás kategóriája) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Projektszerződéssor részlete) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Projektszerződéssori tranzakciós kategória) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Projektszerződéssori tranzakciós osztály) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Árajánlatsor számlaütemezése) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Árajánlatsor erőforráskategóriája) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Árajánlatsor mérföldköve) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Árajánlatsor részlete) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Árajánlatsor tranzakciós kategóriája) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Árajánlatsor tranzakciós osztálya) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Megrendeléssor) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Elavult egyéni nézetek és vezérlők
A következő egyéni nézetek és vezérlők, valamint a hozzájuk kapcsolódó melléktermékek elavultak.

- Tölthetőség nézet.
- Egyéni rácsvezérlők az árajánlatsor részleteinek megjelenítéséhez a **Projekt adatai** oldalon az árajánlatsorhoz.
- Egyedi rácsvezérlők a projekt szerződéssora részleteinek megjelenítéséhez a **Projekt adatai** oldalon az értékesítési megrendeléssorhoz.

> [!NOTE]
> Az elavult erőforrások teljes listáját lásd: [Elavult webes erőforrások a Project Service Automation v3.x verzióban](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Egységesített kliens interfész alkalmazásmodul
Az egységesített kliens interfész (UCI) alkalmazásmodulok bevezetésével a PSA oldaltérképének bejegyzéseit eltávolításra kerültek a rendszerből.  
A Lehetőség, az Árajánlat, a Megrendelés, a Számla űrlapváltással kapcsolatos funkciók elavultak, mivel már nincs rájuk szükség, mert az UCI alkalmazásmodul csak az űrlapok PSA-verzióit tartalmazza.  

A következő webes erőforrások elavultak:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Az elavult erőforrások teljes listáját lásd: [Elavult webes erőforrások a Project Service Automation v3.x verzióban](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
