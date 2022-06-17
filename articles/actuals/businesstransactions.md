---
title: Üzleti tranzakciók a Project Operations alkalmazásban
description: Ez a cikk áttekintést nyújt az üzleti tranzakciók fogalmáról a Microsoftban Dynamics 365 Project Operations.
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
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923283"
---
# <a name="business-transactions-in-project-operations"></a>Üzleti tranzakciók a Project Operations alkalmazásban

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

A Microsoftban Dynamics 365 Project Operations *az üzleti tranzakció* egy absztrakt fogalom, amelyet egyetlen entitás sem képvisel. Az entitások gyakori mezői és folyamatai azonban az üzleti tranzakciók fogalmának használatára vannak kialakítva. A következő entitások használják az absztrakciót:

- Árajánlatsor részletei
- Szerződéssor részletei
- Becslés sorai
- Naplósorok
- Tények

Ezen entitások közül az Árajánlat sor részletei, a Szerződéssor részletei és a Becsült sorok a *projekt életciklusának becslési fázisára* vannak leképezve. A Naplósorok és a Tényleges adatok entitások a *projekt életciklusának végrehajtási fázisára* vannak leképezve.

A Project Operations mind az öt entitás rekordjait üzleti tranzakcióként kezeli. Az egyetlen különbség az, hogy az entitások azon rekordjai, amelyek a becslési fázisra vannak leképezve (Árajánlatsor részletei, Szerződéssor részletei és Becsült sorok), pénzügyi előrejelzéseknek minősülnek *, míg a végrehajtási fázisra leképezett entitások (Naplósorok és Tényleges adatok) rekordjai már megtörtént pénzügyi tényeknek* minősülnek *.*

További információért lásd: [Becslések](../project-management/estimating-projects-overview.md) és [Tényadatok](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Az üzleti tranzakciók esetében egyedi fogalmak

A következő fogalmak egyediek az üzleti tranzakciók fogalma esetében:

- Tranzakció típusa
- Tranzakcióosztály
- Tranzakcióeredet
- Tranzakciós kapcsolat

### <a name="transaction-type"></a>Tranzakció típusa

A tranzakció típusa a projektre gyakorolt pénzügyi hatás időzítését és kontextusát jelenti. Ezt egy olyan értékkészlet határozza meg, amely a következő támogatott értékekkel rendelkezik a Project Operationsben:

- Költség
- Projektszerződés
- Számlázatlan értékesítés
- Számlázott értékesítés
- Szervezetek közötti értékesítések
- Erőforrás-kezelő részleg költsége

### <a name="transaction-class"></a>Tranzakcióosztály

A tranzakciós osztály a projektekkel kapcsolatban felmerülő költségek különböző típusait jelöli. Ezt egy olyan értékkészlet határozza meg, amely a következő támogatott értékekkel rendelkezik a Project Operationsben:

- Idő
- Költség
- Anyag
- Díj
- Mérföldkő
- Adó

> [!NOTE]
> A **Mérföldkő** értéket általában az üzleti logika használja a rögzített árú számlázáshoz a Project Operationsben.

### <a name="transaction-origin"></a>Tranzakcióeredet

A tranzakció eredete olyan entitás, amely tárolja az egyes üzleti tranzakciók eredetét, hogy segítse a jelentéseket és a nyomonkövethetőséget. A projekt végrehajtásának megkezdésekor minden üzleti tranzakció létrehoz egy másik üzleti tranzakciót, amely viszont egy másik üzleti tranzakciót hoz létre, és így tovább.

### <a name="transaction-connection"></a>Tranzakciós kapcsolat

A tranzakciós kapcsolat olyan entitás, amely két hasonló üzleti tranzakció, például a költség- és kapcsolódó értékesítési tényleges adatok vagy a tranzakció-visszafordítások közötti kapcsolatot tárolja, amelyeket olyan számlázási tevékenységek váltanak ki, mint a számla megerősítése vagy a számlakorrekciók.

A Tranzakció eredete és a Tranzakciókapcsolat entitások együttesen segítenek nyomon követni az üzleti tranzakciók és az adott üzleti tranzakció létrehozását okozó műveletek közötti kapcsolatok.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
