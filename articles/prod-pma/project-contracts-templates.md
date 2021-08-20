---
title: Projektszerződések és projektek szinkronizálása közvetlenül a Project Service Automation rendszerből a Pénzügybe
description: Ez a témakör ismerteti azt a sablont és azokat az alapul szolgáló feladatokat, amelyek a szerződések és a projektek közvetlenül a Microsoft Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: acb87be977cc009f89ceac5b01c9028d6741b552a441ef49e024b6b078a188d4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001074"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Projektszerződések és projektek szinkronizálása közvetlenül a Project Service Automation rendszerből a Pénzügybe 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ez a témakör ismerteti azt a sablont és azokat az alapul szolgáló feladatokat, amelyek a szerződések és a projektek közvetlenül a Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.

> [!NOTE] 
> Ha Enterprise Edition 7.3.0 verzit használ, akkor a KB 4074835 telepítésére van szükség.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Adatfolyam a Project Service Automation és a Finance között

> [!NOTE]
> Mielőtt használhatná a Project Service Automation és Finance közötti integrációs megoldást, ismernie kell a Dynamics 365 adatintegrációs funkcióját.

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között. Az adatintegrációs szolgáltatással elérhető integrációs sablon lehetővé teszi a projektszerződésekkel, projektekkel, projektszerződéssorokkal és projektszerződéssorok mérföldköveivel kapcsolatos adatok áramlását a Project Service Automation és a Finance között.

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.

[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Sablonok és feladatok

A rendelkezésre álló sablonok eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.

A következő sablonok és a mögöttes feladatok segítségével szinkronizálhatja a projektszerződéseket és projekteket a Project Service Automation alkalmazásból a Finance rendszerbe:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrálás a Dynamics 365 Project Service Automation v2.x verzióval
- A **Sablon neve az Adatintegrációban:** Projektek és szerződések (Project Service Automation rendszerből a Pénzügybe)
- **A feladat neve a projektben:**

    - Projektszerződések Project Service Automation rendszerből a Pénzügybe
    - Projektek – Project Service Automation rendszerből a Pénzügybe
    - Projekt szerződéssorok – Project Service Automation rendszerből a Pénzügybe
    - Projekt szerződéssor-mérföldkövek – Project Service Automation rendszerből a Pénzügybe
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrálás a Dynamics 365 Project Service Automation v3.x verzióval
A Project Service Automation alkalmazásban egy sémaváltás történt, amely hatással van a projektszerződéssor mérföldkövének sablonjára, és a sablon v2 verziójának használatára van szükség a Project Service Automation v3.x alkalmazásnak a Dynamics 365 alkalmazással való integrálásához.

- A **Sablon neve az Adatintegrációban:** Projektek és szerződések (Project Service Automation 3.x rendszerből a Pénzügybe) – v2
- **A feladat neve a projektben:**

    - Projektszerződések Project Service Automation rendszerből a Pénzügybe
    - Projektek – Project Service Automation rendszerből a Pénzügybe
    - Projekt szerződéssorok – Project Service Automation rendszerből a Pénzügybe
    - Projekt szerződéssor-mérföldkövek – Project Service Automation rendszerből a Pénzügybe

A projektszerződések és projektek szinkronizálása előtt szinkronizálnia kell a partnereket.

## <a name="entity-set"></a>Entitáskészlet

| Project Service Automation       | Pénzügy                                                |
|----------------------------------|--------------------------------------------------------|
| Megrendelések                           | A projektszerződés integrációs entitása                |
| Projektek                         | A projekt integrációs entitása                         |
| Rendelési sorok                      | A projektszerződéssor integrációs entitása           |
| Projektszerződéssor mérföldkövei | A projektszerződéssor mérföldkövének integrációs entitása |

## <a name="entity-flow"></a>Entitásfolyam

A projektszerződések a Project Service Automation alkalmazásban kezelhetők, és a program projektszerződésekként szinkronizálja őket a Finance rendszerbe. Az integrációs sablon részeként beállíthatja az integrációs forrást a projektszerződéshez a Finance rendszerben.

Az idő-, anyag- és rögzített árú projekteket a Project Service Automation rendszerben kezelik és a Pénzügyekbe projektekként szinkronizálják. A sablonintegráció részeként beállíthatja a projekt integrációs forrását a Pénzügyben. Jelenleg csak az időpontok és az anyagok és a rögzített árú projektek támogatottak.


A projektszerződéssorok a Project Service Automation alkalmazásban kezelhetők, és a program projektszerződés számlázási szabályaiként szinkronizálja őket a Finance rendszerbe. Ha a számlázási mód eltér az alapértelmezett projekttípustól, akkor a szinkronizálás frissíti a szerződéssor projektjének és a projektcsoportnak a projekttípusát.

A projektszerződéssor mérföldkövei a Project Service Automation alkalmazásban kezelhetők, és a program projektszerződés számlázási szabályának mérföldköveiként szinkronizálja őket a Finance rendszerbe.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation és Finance közötti integrációs megoldás

A **Projektszerződés azonosítója** mező a **Projektszerződések** oldalon érhető el. Ez a mező természetes és egyedi kulcsként lett létrehozva az integráció támogatásához.

Amikor egy új projektszerződés jön létre, akkor ha a **Projektszerződés azonosítója** érték még nem létezik, a rendszer automatikusan generálja egy számsorozat használatával. Az érték az **ORD** elemből és az azt követő növekményes számsorozatből, valamint egy hat karakteres utótagból áll. Íme egy példa: **ORD-01022-Z4M9Q0**.

A **Projektszám** mező a **Projektek** oldalon érhető el. Ez a mező természetes és egyedi kulcsként lett létrehozva az integráció támogatásához.

Amikor egy új projektszerződés jön létre, akkor ha a **Projektszám** érték még nem létezik, a rendszer automatikusan generálja egy számsorozat használatával. Az érték a **PRJ** elemből és az azt követő növekményes számsorozatből, valamint egy hat karakteres utótagból áll. Íme egy példa: **PRJ-01049-CCNID0**.

Amikor a Project Service Automation és a Finance közötti integrációs megoldást alkalmazza, egy frissítási parancsfájl beállítja a **Projektszerződés azonosítója** mezőt a meglévő projektszerződések és a **Projektszám** mezőt a meglévő projektek esetében a Project Service Automation alkalmazásban.

## <a name="prerequisites-and-mapping-setup"></a>Előfeltételek és leképezési beállítások

- A projektszerződések és projektek szinkronizálása előtt szinkronizálnia kell a partnereket.
- A kapcsolati készletben vegyen fel egy integrációs kulcsmező leképezést a **msdyn\_organizationalunits** és a **msdyn\_name \[Name\]** között. Előfordulhat, hogy előbb hozzá kell adnia egy projektet a kapcsolati készlethez. További információkért lásd: [Adatok integrálása a Common Data Service for Apps rendszerbe](/powerapps/administrator/data-integrator).
- A kapcsolati készletben vegyen fel egy integrációs kulcsmező leképezést a **msdyn\_projects** és a **msdynce\_projectnumber \[Project Number\]** között. Előfordulhat, hogy előbb hozzá kell adnia egy projektet a kapcsolati készlethez. További információkért lásd: [Adatok integrálása a Common Data Service for Apps rendszerbe](/powerapps/administrator/data-integrator).
- A projektszerződések és projektek **SourceDataID** eleme frissíthetp egy eltérő értékre, vagy eltávolítható a leképezésből. Az alapértelmezett sablon értéke a **Project Service Automation**.
- A **PaymentTerms** leképezést frissíteni kell, hogy az tükrözze a Finance érvényes fizetési feltételeit. Eltávolíthatja továbbá a leképezést a projektfeladatból is. Az alapértelmezett érték leképezése alapértelmezett értékekkel rendelkezik a demó adatokhoz. A következő táblázat a Project Service Automation értékeit mutatja be.

    | Value | Ismertetés   |
    |-------|---------------|
    | 0     | 30 napon belül        |
    | 2     | 30 napon belül (10 napon belül fizetve 2% engedmény) |
    | 3     | 45 napon belül        |
    | 4     | 60 napon belül        |

## <a name="power-query"></a>Power Query

Az Excelhez készült Microsoft Power Query segítségével szűrheti az adatokat, ha teljesülnek a következő feltételek:

- Értékesítésekkel rendelkezik a Dynamics 365 Sales alkalmazásban.
- A Project Service Automation alkalmazásban több szervezeti egység is van, és ezek a szervezeti egységek több entitásra lesznek leképezve a Finance rendszerben.

Ha Power Query alkalmazást kell használnia, kövesse az alábbi irányelveket:

- A Projektek és szerződések (PSA – Fin és Ops) sablonhoz egy alapértelmezett szűrő tartozik, amely csak a **Work item (msdyn\_ordertype = 192350001)** típusú értékesítési rendeléseket tartalmazza. Ez a szűrő segít biztosítani, hogy ne jöjjenek létre projektszerződések a Finance számára létrehozott értékesítési rendelésekhez. Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia.
- Hozzon létre egy Power Query szűrőt, amely csak azokat a szerződéssel rendelkező szervezeteket tartalmazza, amelyeket az integrációs kapcsolatcsoport jogi entitással kell szinkronizálni. Például az Contoso US szerződéses szervezeti egységgel fennálló projektszerződéseket az USSI jogi entitással kell szinkronizálni, de a Contoso Global szerződéses szervezeti egységgel fennálló projektszerződéseket az USMF jogi entitással kell szinkronizálni. Ha nem adja hozzá ezt a szűrőt a feladatleképezéshez, akkor a program az összes projektszerződést szinkronizálja a kapcsolati készlethez definiált jogi entitással, függetlenül a szerződéses szervezeti egységtől.

## <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

> [!NOTE] 
> A **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** és **AddressZipCode** mezők nem szerepelnek a projektszerződések alapértelmezett leképezésében. A leképezéseket hozzáadhatja, ha szükséges, hogy az adatok szinkronizálása megtörténjen a projektszerződések esetében.
>
> A **Leírás**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** és **ProjectType** mezők nem szerepelnek a projektek alapértelmezett leképezésében. A leképezéseket hozzáadhatja, ha szükséges, hogy az adatok szinkronizálása megtörténjen a projektek esetében.

A következő ábra példákat mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![A projekt szerződéssablon-leképezése.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![A projektsablon-leképezése.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![A projekt szerződéssor sablonleképezése.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![A projekt szerződéssor-mérföldkő sablonleképezése.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projektszerződéssor mérföldkő-leképezése a Projektek és a szerződések (PSA 3.x – Dynamics) - v2 sablonban:

[![A projekt szerződéssor-mérföldkő leképezése két sablonnal.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]