---
title: Projekt tényleges adatainak közvetlen szinkronizálása a Project Service Automation alkalmazásból közvetlenül a projektintegrációs naplóba a feladáshoz a pénzügy és műveletek szolgáltatásba
description: Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a tényleges projektadatok közvetlenül a Microsoft Dynamics 365 Project Service Automation alkalmazásból a pénzügyi és műveleti alkalmazásokba történő szinkronizálására szolgálnak.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 34a0a0f7277777895077d221cd95e8d962d2a902
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028981"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekt tényleges adatainak közvetlen szinkronizálása a Project Service Automation alkalmazásból közvetlenül a projektintegrációs naplóba a feladáshoz a pénzügy és műveletek szolgáltatásba

[!include[banner](../includes/banner.md)]

Ez a cikk ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a tényleges projektadatok közvetlenül a Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.

A sablon szinkronizálja a Project Service Automation tranzakcióit egy ideiglenes táblázatba a Finance rendszerben. Miután a szinkronizálás befejeződött, importálnia **kell** az adatokat az ideiglenes táblázatból az integrációs naplóba.

> [!NOTE]
> - A tényleges projektadatok integrációja a 8.0.1 verzióban érhető el.
> - Ha az Enterprise Edition 7.3.0 verzióját használja, a KB 4132657 és a KB 4132660 telepítése után használhatja a sablonokat a projektfeladatok, a költségtranzakció-kategóriák, az órabecslések, a kiadásbecslések és a tényadatok integrálására, valamint a funkciók zárolásának konfigurálására. Ha vissza kell állítania a könyvelési feloszlásokat, ajánlott a KB 4131710 telepítése is.
> - Ha 7.3.0 verziót használ, és a Project Service Automation alkalmazásból hozza át a díjtranzakciókat, akkor a díjaknak a projekt számláján való feltümntetéséhez szükség van a KB 4345320 telepítésére.
> - Ha a Project Service Automation alkalmazásban idő- vagy kiadási tranzakciókra vonatkozó áfaösszegeket ír be, telepítenie kell a Project Service Automation Update 7 frissítést. Ellenkező esetben az adó tényleges adatai nem kapcsolódnak a társított időhöz vagy költséghez, és nem lesznek szinkronizálva a Finance rendszerrel. További információkért forduljon a Támogatáshoz.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Adatfolyam a Project Service Automation és a Finance között

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között. Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a tényleges projektadatok áramlását a Project Service Automation és a Finance között.

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.

[![Adatáramlás a Project Service Automation és a pénzügyi és műveleti alkalmazások integrációjához](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Tényleges projektadatok a Project Service Automation alkalmazásból

### <a name="template-and-tasks"></a>Sablon és feladatok

A rendelkezésre álló sablonok eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.

A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a tényleges projektadatokat a Project Service Automation alkalmazásból a Finance rendszerbe:

- **A sablon neve az adatintegrációban:** Tényleges projektadatok (PSA – Fin és Ops)
- **A feladat neve a projektben:**

    - Tényadatok
    - Tranzakciókapcsolatok

### <a name="entity-set"></a>Entitáskészlet

| Project Service Automation | Pénzügy                                   |
|----------------------------|----------------------------------------------------------|
| Tényadatok                    | A tényleges projektadatok integrációs entitása                   |
| Tranzakciós kapcsolatok    | A projekt tranzakciókapcsolatainak integrációs entitása |

### <a name="entity-flow"></a>Entitásfolyam

A tényleges projektadatok a Project Service Automation alkalmazásban kezelhetők, és a program projektintegrációs naplóba kerülnek szinkronizálásra a Finance rendszerbe. A rendszer az alapértelmezett pénzügyi dimenziók és a feladási beállítás alapján alkalmazza a könyvelést.

### <a name="prerequisites"></a>Előfeltételek

A tényadatok szinkronizálása előtt be kell állítania a Project Service Automation integrációs paramétereit, és szinkronizálni kell a projekteket, a projektfeladatokat és a projekt költségtranzakciós kategóriáit.

### <a name="power-query"></a>Power Query

A tényleges projektadatok sablonjában az Excelhez készült Microsoft Power Query használatával kell végrehajtania ezeket a feladatokat:

- Alakítsa át a tranzakció típusát a Project Service Automation szolgáltatásban a megfelelő tranzakciótípusra a Finance rendszerben. Ez az átalakítás már meg van adva a Tényleges projektadatok (PSA – Fin és Ops) sablonban.
- Alakítsa át a számlázás típusát a Project Service Automation szolgáltatásban a megfelelő számlázástípusra a Finance rendszerben. Ez az átalakítás már meg van adva a Tényleges projektadatok (PSA – Fin és Ops) sablonban. Ezután a számlázási típus leképezésre kerül a sortulajdonságra a **Project Service Automation integrációs paraméterei** oldalon található konfiguráció alapján.
- Szűrje az adott erőforrás szervezeti egységeit, amelyeket szinkronizálni kell ezzel a sablonnal.
- Ha a vállalatközi időt vagy a vállalatközi költségeket a program a Finance rendszerrel szinkronizálja, akkor a szerződés szervezeti egységét a Finance megfelelő entitásához kell alakítania. A Tényleges projektadatok (PSA – Fin és Ops) sablonban egy feltételes oszlop van meghatározva a demóadatok alapján. Frissítenie kell az utolsó beszúrt feltételes oszlopot a megfelelő jogi entitásokra. Máskülönben előfordulhat, hogy integrációs hiba történik, vagy helytelen tényleges tranzakciók lesznek importálva a Finance alkalmazásba.
- Ha a vállalatközi időt vagy a vállalatközi költségeket a program nem szinkronizálja a Finance rendszerrel, akkor törölnie kell az utolsó beszúrt feltételes oszlopot a sablonból. Máskülönben előfordulhat, hogy integrációs hiba történik, vagy helytelen tényleges tranzakciók lesznek importálva a Finance alkalmazásba.

#### <a name="contract-organizational-unit"></a>Szerződéses szervezeti egység
A sablonban a beszúrt feltételes oszlop frissítéséhez kattintson a **Leképezés** nyílra a leképezés megnyitásához. Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást a Power Query felé.

- Ha az alapértelmezett Tényleges projektadatok (PSA – Fin és Ops) sablont használja, akkor a Power Query-ben jelölje ki az utolsó **Beszúrt feltétel** lehetőséget az **Alkalmazott lépések** szakaszból. A **Funkció** bejegyzésében cserélje le az **USSI** elemet az integrációval használni kívánt jogi entitás azonosítójával. Szükség szerint adjon hozzá további feltételeket a **Funkció** bejegyzéshez, és frissítse az **else** feltételt az **USMF** értékről a megfelelő jogi entitásra.
- Ha új sablont hoz létre, akkor a vállalatközi idő és kiadások támogatásához hozzá kell adnia az oszlopot. Válassza ki a **Feltételes oszlop hozzáadása** jelölőnégyzetet, és adja meg az új oszlop nevét, például **LegalEntity**. Adja meg az oszlop feltételeit, ahol, ha a **msdyn\_contractorganizationalunitid.msdyn\_name** értéke \<organizational unit\>, akkor \<enter the legal entity\>, egyébként nulla.

### <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábrák egy példát mutatnak be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![Sablonok leképezése – Aktualitások.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Sablonok leképezése – tranzakciós kapcsolatok.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importálás az ideiglenes táblázatból a Project Service Automation alkalmazásból való integrációt követően

Az Importálás az ideiglenes táblázatból időszakos folyamatot a tényleges adatok Project Service Automation alkalmazásból a Finance rendszerbe való szinkronizálását követően kell futtatni. Ezzel a folyamattal importálja a projekt tranzakcióit az ideiglenes táblázatból a Project Service Automation integrációs naplóba, ahol a könyvelést alkalmazzák, és az importált tranzakciókat fel lehet adni. Javasoljuk, hogy kötegelt módban futtassa ezt a folyamatot. Beállítható úgy is, hogy ismétlődő kötegként fusson.

## <a name="update-actuals-from-finance"></a>A tényadatok frissítése a Finance rendszerből

### <a name="template-and-tasks"></a>Sablon és feladatok

A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a könyvelt projekttranzakciók bizonylatszámát és áfáját a Finance rendszerből a Project Service Automation alkalmazásba:

- **A sablon neve az adatintegrációban:** Tényleges projektadatok frissítése (Fin Ops – PSA)
- **A feladat neve a projektben:**

    - Tényadatok 
    - Tranzakciókapcsolatok

### <a name="entity-set"></a>Entitáskészlet

| Pénzügy                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| A tényleges projektadatok integrációs entitása                   | Tényadatok                    |
| A projekt tranzakciókapcsolatainak integrációs entitása | Tranzakciós kapcsolatok    |

### <a name="entity-flow"></a>Entitásfolyam

A tényleges projektadatok a Project Service Automation alkalmazásban kezelhetők, és a program projektintegrációs naplóba kerülnek szinkronizálásra a Finance rendszerbe. A tényleges adatok Finance rendszerbe való feladását követően a program frissíti őket a Project Service Automation alkalmazásban a Finance rendszerből származó bizonylatszámmal. Ha a Finance rendszerben hozzáadásra került áfa, akkor új tényleges adók kerülnek létrehozásra a Project Service Automation alkalmazásban.

### <a name="power-query"></a>Power Query

A tényleges projektadatok frissítési sablonjában a Power Query használatával kell végrehajtania ezeket a feladatokat:

- Alakítsa át a tranzakció típusát a Finance rendszerben a megfelelő tranzakciótípusra a Project Service Automation alkalmazásban. Ez az átalakítás már meg van adva a Tényleges projektadatok frissítése (Fin Ops – PSA) sablonban.
- Alakítsa át a számlázás típusát a Finance rendszerben a megfelelő számlázástípusra a Project Service Automation alkalmazásban. Ez az átalakítás már meg van adva a Tényleges projektadatok frissítése (Fin Ops – PSA) sablonban.

### <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábra példákat mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Finance rendszerből a Project Service Automation alkalmazásba lesznek szinkronizálva.

[![Sablonok leképezése – Tényleges értékek frissítése.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Sablonok leképezése – Tranzakció frissítése.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]