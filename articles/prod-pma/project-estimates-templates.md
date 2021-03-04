---
title: A projektbecslések szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe
description: Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektórabecslések és a projektkiadás-becslések közvetlenül a Microsoft Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078220"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>A projektbecslések szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe

[!include[banner](../includes/banner.md)]

Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektórabecslések és a projektkiadás-becslések közvetlenül a Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.

> [!NOTE]
> - A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.
> - A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Adatfolyam a Project Service Automation és a Finance között

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között. Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projekt órabecsléseivel és a projekt költségbecsléseivel kapcsolatos adatok áramlását a Project Service Automation és a Finance között.

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.

[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekt órabecslései

### <a name="template-and-tasks"></a>Sablon és feladatok

A rendelkezésre álló sablonok eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.

A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a projekt órabecsléseit a Project Service Automation alkalmazásból a Finance rendszerbe:

- **A sablon neve az adatintegrációban:** Projekt órabecslései (PSA – Fin és Ops)
- **A feladat neve a projektben:**

    - Tranzakciókapcsolatok
    - Költség becslések

### <a name="entity-set"></a>Entitáskészlet

| Project Service Automation | Pénzügy                                       |
|----------------------------|-----------------------------------------------|
| Projektfeladatok              | Integrációs entitás a projekt órabecsléseihez |

### <a name="entity-flow"></a>Entitásfolyam

A projekt órabecslései a Project Service Automation alkalmazásban kezelhetők, és a program projektóra-előrejelzésekként szinkronizálja őket a Finance rendszerbe.

### <a name="prerequisites"></a>Előfeltételek

A projekt ürabecsléseinek szinkronizálása előtt szinkronizálnia kell a projekteket, a projektfeladatokat és a projekt költségeinek tranzakciós kategóriáit.

### <a name="power-query"></a>Power Query

A projekt órabecsléseinek sablonjában az Excelhez készült Microsoft Power Query használatával kell végrehajtania ezeket a feladatokat:

- Állítsa be az alapértelmezett előrejelzési modell azonosítóját, amelyet akkor használ a rendszer, ha az integráció új óra-előrejelzéseket hoz létre.
- Szűrjön ki a feladatban minden olyan erőforrás-specifikus rekordot, amely miatt meghiúsul az óra-előrejelzésekkel való integráció.
- Szűrje ki az összes üres tranzakciós kategória sorát. A feladat végrehajtásának elmulasztása helytelen óra-előrejelzéseket eredményezhet.

#### <a name="set-the-default-forecast-model-id"></a>Az alapértelmezett előrejelzési modell azonosítójának beállítása

A sablonban az alapértelmezett előrejelzési modell azonosítójának frissítéséhez kattintson a **Leképezés** nyílra a leképezés megnyitásához. Ezután jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást.

- Ha az alapértelmezett Projekt órabecslései (PSA – Fin és Ops) sablont használja, akkor jelölje ki a **Beszúrt feltétel** lehetőséget az **Alkalmazott lépések** listájában. A **Funkció** bejegyzésében cserélje le au **O\_forecast** elemet az integrációval használni kívánt előrejelzési modell azonosítójával. Az alapértelmezett sablon egy előrejelzési modell azonosítóval rendelkezik a demó adatokból.
- Ha új sablont hoz létre, akkor ezt az oszlopot kell felvennie. A Power Query alkalmazásban jelölje be a **Feltételes oszlop hozzáadása** jelölőnégyzetet, és adja meg az új oszlop nevét, például **ModelID**. Adja meg az oszlop feltételeit, ahol, ha a projektfeladat nem nulla, akkor \<enter the forecast model ID\>, egyébként nulla.

#### <a name="filter-out-resource-specific-records"></a>Erőforrás-specifikus bejegyzések kiszűrése

A Projekt órabecslései (PSA – Fin és Ops) sablon egy alapértelmezett szűrővel rendelkezik, amely eltávolítja az erőforrás-specifikus bejegyzéseket. Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia. Válassza ki a **Speciális lekérdezés és szűrés** hivatkozást a **msdyn\_islinetask** oszlop szűréséhez, hogy csak a **Hamis** rekordok maradjanak.

#### <a name="filter-out-empty-transaction-category-rows"></a>Az üres tranzakciós kategória sorok kiszűrése

Hozzá kell adnia egy szűrőt az üres tranzakciós kategóriákat tartalmazó sorok eltávolításához. Ez a feladat kötelező, függetlenül attól, hogy az alapértelmezett sablont használja-e, vagy saját sablont hoz létre. Ez a szűrő eltávolítja a Project Service Automation minden összesítő sorát, amelyek miatt az óra-előrejelzések helytelenek lehetnek a Finance rendszerben. Válassza a **Speciális lekérdezés és szűrés** hivatkozást a null rekordok kiszűréséhez a **msdyn\_transactioncategory\_value** oszlopban.

### <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![Sablonfeladat leképezése az adatintegrációban](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekt költségbecslései

### <a name="template-and-tasks"></a>Sablon és feladatok

A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a projekt költségbecsléseit a Project Service Automation alkalmazásból a Finance rendszerbe:

- **A sablon neve az adatintegrációban:** Projekt költségbecslései (PSA – Fin és Ops)
- **A feladat neve a projektben:**

    - Tranzakciókapcsolatok 
    - Költség becslések

### <a name="entity-set"></a>Entitáskészlet

| Project Service Automation | Pénzügy                                                  |
|----------------------------|----------------------------------------------------------|
| Tranzakciós kapcsolatok    | A projekt tranzakciókapcsolatainak integrációs entitása |
| Becsléssorok             | Integrációs entitás a projekt költségbecsléseihez         |

### <a name="entity-flow"></a>Entitásfolyam

A projekt költségbecslései a Project Service Automation alkalmazásban kezelhetők, és a program projektköltség-előrejelzésekként szinkronizálja őket a Finance rendszerbe.

### <a name="prerequisites"></a>Előfeltételek

A projekt költségbecsléseinek szinkronizálása előtt szinkronizálnia kell a projekteket, a projektfeladatokat és a projekt költségeinek tranzakciós kategóriáit.

### <a name="power-query"></a>Power Query

A projekt költségbecsléseinek sablonjában a Power Query használatával kell végrehajtania a következő feladatokat:

- Végezzen szűrést, hogy csak a költségbecslés sorrekordjai szerepeljenek.
- Állítsa be az alapértelmezett előrejelzési modell azonosítóját, amelyet akkor használ a rendszer, ha az integráció új óra-előrejelzéseket hoz létre.
- Alakítsa át a számlázási típusokat.
- Alakítsa át a tranzakciótípusokat.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Szűrés, amellyel csak a költségbecslés sorai szerepelnek

A Projekt költségbecslései (PSA – Fin és Ops) sablon egy alapértelmezett szűrővel rendelkezik, amely csak az integrációban szereplő költségsorokat tartalmazza. Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia. Jelölje ki a **Tranzakciókapcsolatok** feladatot, majd kattintson a **Leképezés** nyílra a leképezés megnyitásához. Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást. Szűrje a **msdyn\_transactiontype1** oszlopot úgy, hogy csak a **msdyn\_estimateline** elemeket tartalmazza.

#### <a name="set-the-default-forecast-model-id"></a>Az alapértelmezett előrejelzési modell azonosítójának beállítása

A sablonban az alapértelmezett előrejelzési modell azonosítójának frissítéséhez válassza a **Költségbecslések** feladatot, majd kattintson a **Leképezés** nyílra a leképezés megnyitásához. Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást.

- Ha az alapértelmezett Projekt költségbecslései (PSA – Fin és Ops) sablont használja, akkor a Power Query alkalmazásban jelölje ki az első **Beszúrt feltétel** lehetőséget az **Alkalmazott lépések** szakaszból. A **Funkció** bejegyzésében cserélje le au **O\_forecast** elemet az integrációval használni kívánt előrejelzési modell azonosítójával. Az alapértelmezett sablon egy előrejelzési modell azonosítóval rendelkezik a demó adatokból.
- Ha új sablont hoz létre, akkor ezt az oszlopot kell felvennie. A Power Query alkalmazásban jelölje be a **Feltételes oszlop hozzáadása** jelölőnégyzetet, és adja meg az új oszlop nevét, például **ModelID**. Adja meg az oszlop feltételeit, ahol, ha a becslési sor azonosítója nem nulla, akkor \<enter the forecast model ID\>, egyébként nulla.

#### <a name="transform-the-billing-types"></a>Számlázási típusok átalakítása

A Projekt költségbecslései (PSA – Fin és Ops) sablonja tartalmaz egy feltételes oszlopot, amellyel átalakíthatja a Project Service Automation szolgáltatásból kapott számlázási típusokat az integráció során. Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia. Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást, majd válassza a **Feltételes oszlop hozzáadása** lehetőséget. Adja meg az új oszlop nevét, például **BillingType**. Ezután adja meg a következő feltételt:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>A tranzakciótípusok átalakítása

A Projekt költségbecslései (PSA – Fin és Ops) sablonja tartalmaz egy feltételes oszlopot, amellyel átalakíthatja a Project Service Automation szolgáltatásból kapott tranzakciótípusokat az integráció során. Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia. Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást, majd válassza a **Feltételes oszlop hozzáadása** lehetőséget. Adja meg az új oszlop nevét, például **TransactionType**. Ezután adja meg a következő feltételt:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábra példákat mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![A költségbecslés-tranzakciók sablon szerinti leképezése](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![A költségbecslések sablon szerinti leképezése](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]