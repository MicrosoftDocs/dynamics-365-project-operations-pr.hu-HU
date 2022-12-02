---
title: Üzleti tranzakciók a Project Operations alkalmazásban
description: A cikk áttekintést ad az üzleti tranzakcióinak fogalmáról a Microsoft Dynamics 365 Project Operations alkalmazásban.
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

A Microsoft Dynamics 365 Project Operations *üzleti tranzakciója* olyan absztrakt fogalom, amelyet nem képvisel bármely entitás. Az entitások gyakori mezői és folyamatai azonban az üzleti tranzakciók fogalmának használatára vannak kialakítva. A következő entitások használják az absztrakciót:

- Árajánlatsor részletei
- Szerződéssor részletei
- Becslés sorai
- Naplósorok
- Tények

Ezen entitások közül az Árajánlatsor részletei, a Szerződéssor részletei és a Becsléssorok a projekt életciklusának *becslési fázisára* vannak leképezve. A Naplósorok és a Tényadat-entitások a projekt életciklusának *végrehajtási fázisára* vannak leképezve.

A Project Operations mind az öt entitás rekordjait üzleti tranzakcióként kezeli. Az egyetlen különbség, hogy a becslési fázisra (Árajánlatsor részletei, Szerződéssor részletei és Becsléssorok) leképezett entitásokban lévő rekordok *pénzügyi előrejelzésnek* számítanak, míg a végrehajtási fázishoz (Naplósorok és Tényadatok) leképezett entitások bejegyzései olyan *pénzügyi tények*, amelyek már megtörténtek.

További információért lásd: [Becslések](../project-management/estimating-projects-overview.md) és [Tényadatok](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Az üzleti tranzakciók esetében egyedi fogalmak

A következő fogalmak egyediek az üzleti tranzakciók fogalma esetében:

- Tranzakció típusa
- Tranzakcióosztály
- Tranzakcióeredet
- Tranzakciós kapcsolat

### <a name="transaction-type"></a>Tranzakció típusa

A tranzakció típusa a projektre gyakorolt pénzügyi hatás időzítését és kontextusát jelenti. Ezt egy értékkészlet definiálja, amelynek a következő támogatott értékei a Project Operations szolgáltatásban szerepelnek:

- Költség
- Projektszerződés
- Számlázatlan értékesítés
- Számlázott értékesítés
- Szervezetek közötti értékesítések
- Erőforrás-kezelő részleg költsége

### <a name="transaction-class"></a>Tranzakcióosztály

A tranzakciós osztály a projektekkel kapcsolatban felmerülő költségek különböző típusait jelöli. Ezt egy értékkészlet definiálja, amelynek a következő támogatott értékei a Project Operations szolgáltatásban szerepelnek:

- Idő
- Költség
- Anyag
- Díj
- Mérföldkő
- Adó

> [!NOTE]
> A **Mérföldkő** értékét általában az üzleti logika használja a rögzített árú számlázáshoz a Project Operations szolgáltatásban.

### <a name="transaction-origin"></a>Tranzakcióeredet

A tranzakció eredeti entitás az egyes tranzakciók eredetére vonatkozó adatokat tárolja a jelentéskészítés és a nyomon követhetőség érdekében. A projektek végrehajtása indulásakor minden üzleti tranzakció egy másik üzleti tranzakciót fog előhozni, amely aztán létrehoz egy másik üzleti tranzakciót, és így tovább.

### <a name="transaction-connection"></a>Tranzakciós kapcsolat

A tranzakciós kapcsolat olyan entitás, amely két hasonló üzleti tranzakció közötti kapcsolatot tárolja, például a költség és a kapcsolódó értékesítések tényleges értékét, vagy a tranzakció sztornózását, amelyet számlázási tevékenységek, például a számla visszaigazolása vagy a számla helyesbítései eredményeznek.

A tranzakció eredete és a tranzakciós kapcsolatok entitásai együttesen segítenek nyomon követni az üzleti tranzakciók és az olyan műveletek közötti kapcsolatokat, amelyek egy adott üzleti tranzakció létrehozását okozzák.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
