---
title: Üzleti tranzakciók a projektműveletekben
description: Ez a témakör áttekintést nyújt a Microsoft üzleti tranzakcióinak fogalmáról Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582207"
---
# <a name="business-transactions-in-project-operations"></a>Üzleti tranzakciók a projektműveletekben

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

A Microsoftban Dynamics 365 Project Operations *az üzleti tranzakció* olyan absztrakt fogalom, amelyet egyetlen entitás sem képvisel. Az entitások gyakori mezői és folyamatai azonban az üzleti tranzakciók fogalmának használatára vannak kialakítva. A következő entitások használják az absztrakciót:

- Árajánlatsor részletei
- Szerződéssor részletei
- Becslés sorai
- Naplósorok
- Tények

Ezen entitások közül az Ajánlatsor részletei, a Szerződéssor részletei és a Becslés sorok a *projekt életciklusának becslési fázisához* vannak leképezve. A Naplósorok és a Tényleges értékek entitások a *projekt életciklusának végrehajtási fázisához* vannak rendelve.

A Project Operations mind az öt entitás rekordjait üzleti tranzakcióként kezeli. Az egyetlen különbség az, hogy a becslési fázishoz rendelt entitások rekordjai (Ajánlatsor részletei, Szerződéssor részletei és Becslés sorok) pénzügyi előrejelzéseknek minősülnek *, míg a végrehajtási szakaszhoz rendelt entitások rekordjai (Naplósorok és Tényleges adatok) már megtörtént pénzügyi tényeknek* minősülnek *.*

További információért lásd: [Becslések](../project-management/estimating-projects-overview.md) és [Tényadatok](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Az üzleti tranzakciók esetében egyedi fogalmak

A következő fogalmak egyediek az üzleti tranzakciók fogalma esetében:

- Tranzakció típusa
- Tranzakcióosztály
- Tranzakcióeredet
- Tranzakciós kapcsolat

### <a name="transaction-type"></a>Tranzakció típusa

A tranzakció típusa a projektre gyakorolt pénzügyi hatás időzítését és kontextusát jelenti. Ezt egy olyan értékkészlet határozza meg, amely a következő támogatott értékekkel rendelkezik a Projektműveletekben:

- Költség
- Projektszerződés
- Számlázatlan értékesítés
- Számlázott értékesítés
- Szervezetek közötti értékesítések
- Erőforrás-kezelő részleg költsége

### <a name="transaction-class"></a>Tranzakcióosztály

A tranzakciós osztály a projektekkel kapcsolatban felmerülő költségek különböző típusait jelöli. Ezt egy olyan értékkészlet határozza meg, amely a következő támogatott értékekkel rendelkezik a Projektműveletekben:

- Idő
- Költség
- Anyag
- Díj
- Mérföldkő
- Adó

> [!NOTE]
> A **Milestone** értéket általában az üzleti logika használja a rögzített árú számlázáshoz a Projektműveletek programban.

### <a name="transaction-origin"></a>Tranzakcióeredet

A tranzakció eredete olyan entitás, amely tárolja az egyes üzleti tranzakciók eredetét, hogy segítse a jelentéstételt és a nyomonkövethetőséget. A projektvégrehajtás megkezdésekor minden üzleti tranzakció létrehoz egy másik üzleti tranzakciót, amely viszont létrehoz egy másik üzleti tranzakciót, és így tovább.

### <a name="transaction-connection"></a>Tranzakciós kapcsolat

A tranzakciós kapcsolat olyan entitás, amely két hasonló üzleti tranzakció közötti kapcsolatot tárolja, például a költség és a kapcsolódó értékesítési tényleges értékek vagy a számlázási tevékenységek, például a számla-visszaigazolás vagy a számlajavítások által kiváltott tranzakció-sztornírozások között.

A Tranzakció eredete és a Tranzakciókapcsolati entitások együttesen segítenek nyomon követni kapcsolatok az üzleti tranzakciók és az adott üzleti tranzakció létrehozását eredményező műveletek között.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
