---
title: Üzleti tranzakciók
description: Ez a témakör az üzleti tranzakciókról tartalmaz információkat.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 7c1fd7046783b98b7c2e823b2c2eb8bbdfb232fc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583348"
---
# <a name="business-transactions"></a>Üzleti tranzakciók

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation *üzleti tranzakciója* olyan absztrakt fogalom, amelyet nem képvisel bármely entitás. Az entitások gyakori mezői és folyamatai azonban az üzleti tranzakciók fogalmának használatára vannak kialakítva. A következő entitások használják az absztrakciót:

- Árajánlatsor részletei
- Szerződéssor részletei
- Becslés sorai
- Naplósorok
- Tények

Ezen entitások közül az Árajánlatsor részletei, a Szerződéssor részletei és a Becslés sorai a projekt életciklusának becslési fázisára vannak leképezve. A Naplósorok és a Tényadatok entitások a projekt életciklusának végrehajtási fázisára vannak leképezve.

A PSA az öt entitás rekordjait üzleti tranzakcióként kezeli. Az egyetlen különbség, hogy a becslési fázisra leképezett entitásokban lévő rekordok pénzügyi előrejelzésnek számítanak, míg a végrehajtási fázishoz leképezett entitások bejegyzései olyan pénzügyi tények, amelyek már megtörténtek.

További információért lásd: [Becslések](estimates.md) és [Tényadatok](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Az üzleti tranzakciók esetében egyedi fogalmak
A következő fogalmak egyediek az üzleti tranzakciók fogalma esetében:

- Tranzakció típusa
- Tranzakcióosztály
- Tranzakcióeredet
- Tranzakciós kapcsolat

### <a name="transaction-type"></a>Tranzakció típusa

A tranzakció típusa a projektre gyakorolt pénzügyi hatás időzítését és kontextusát jelenti. Egy értékkészlet képviseli, amelynek a következő támogatott értékei a PSA-ban szerepelnek:
- Költség
- Projektszerződés
- Számlázatlan értékesítés
- Számlázott értékesítés
- Szervezetek közötti értékesítések
- Erőforrás-kezelő részleg költsége

### <a name="transaction-class"></a>Tranzakcióosztály

A tranzakciós osztály a projektekkel kapcsolatban felmerülő költségek különböző típusait jelöli. Egy értékkészlet képviseli, amelynek a következő támogatott értékei a PSA-ban szerepelnek:

- Time
- Költség
- Anyag
- Díj
- Mérföldkő
- Adó

A **Mérföldkő** értékét általában az üzleti logika használja a rögzített árú számlázáshoz a PSA-ban.

### <a name="transaction-origin"></a>Tranzakcióeredet

A tranzakció eredete az egyes üzleti tranzakciók eredetét tároló entitás. A projektek végrehajtása során minden üzleti tranzakció egy másik üzleti tranzakciót fog előhozni, amely aztán létrehoz egy másikat, és így tovább. A tranzakció származása entitás célja az egyes tranzakciók eredetére vonatkozó adatok tárolása a jelentéskészítés és a nyomon követhetőség érdekében. 

### <a name="transaction-connection"></a>Tranzakciós kapcsolat

A tranzakciós kapcsolat olyan entitás, amely két hasonló üzleti tranzakció közötti kapcsolatot tárolja, például a költség és a kapcsolódó értékesítések tényleges értékét, vagy a tranzakció sztornózását, amelyet számlázási tevékenységek, például a számla visszaigazolása vagy a számla helyesbítése eredményeznek.

A tranzakció eredete és a tranzakciós kapcsolatok együttesen segítenek nyomon követni az üzleti tranzakciók és az olyan műveletek közötti kapcsolatokat, amelyek egy adott üzleti tranzakció létrehozását okozzák.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Példa: Hogyan működik a tranzakció eredete a tranzakciós kapcsolattal?

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a PSA projekt életciklusában.

> ![Feldolgozási idő entitások a Project Service életciklusban.](media/basic-guide-17.png)
 
1. Az időbejegyzések beküldése két naplósor létrehozását eredményezi: egy a költségről, egy pedig a nem számlázott értékesítésekről.
2. Az időbejegyzés végleges jóváhagyása két tényadat létrehozását eredményezi: egy a költségről, egy pedig a nem számlázott értékesítésekről.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre. 
4. A számla megerősítését követően két új tényadat jön létre: a nem számlázott értékesítés sztornózása és a számlázott értékesítés tényadata.

Az események mindegyike elindítja a tranzakció eredete és a tranzakciós kapcsolatok entitásban lévő rekordok létrehozását, így nyomon követheti az időpontentitásokon keresztül létrehozott rekordok közötti kapcsolatok nyomkövetését, a naplósort, a tényadatokat és a számlasor részleteit.

A következő táblázat az előző munkafolyamat tranzakció eredete entitásának rekordjait mutatja be.

| Esemény                        | Eredet                   | Eredet típusa                       | Tranzakció                       | Tranzakció típusa         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Időbejegyzés elküldése        | Időbejegyzés-rekord GUID   | Időbejegyzés                        | Naplósor-bejegyzés GUID (költség)   | Naplósor             |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Naplósor-bejegyzés GUID (értékesítés)  | Naplósor                      |                          |
| Jóváhagyási idő                | Naplósor-bejegyzés GUID | Naplósor                      | Számlázatlan értékesítési rekord GUID        | Tény                   |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Számlázatlan értékesítési rekord GUID        | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Költség tényleges rekordja GUID           | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Költség tényleges rekordja GUID           | Tény                            |                          |
| Számla létrehozása             | Időbejegyzés-rekord GUID   | Időbejegyzés                        | Számlasor-tranzakció GUID     | Számlasor-tranzakció |
| Naplósor-bejegyzés GUID     | Naplósor             | Számlasor-tranzakció GUID     | Számlasor-tranzakció          |                          |
| Számla jóváhagyása         | Számlasor GUID        | Számla sora                      | Számlázott értékesítési rekord GUID          | Tény                   |
| Számla GUID                 | Számla                  | Számlázott értékesítési rekord GUID          | Tény                            |                          |
| Számlasor részletei GUID     | Számlasor részletei      | Számlázott értékesítési rekord GUID          | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Számlázott értékesítési rekord GUID          | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Számlázott értékesítési rekord GUID          | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Sztornózott számlázatlan értékesítés GUID      | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Sztornózott számlázatlan értékesítés GUID      | Tény                            |                          |
| Számlatervezet helyesbítése     | Régi ILD GUID             | Számlasor-tranzakció          | Helyesbítési ILD GUID               | Számlasor-tranzakció |
| Régi IL GUID                  | Számla sora             | Helyesbítési ILD GUID               | Számlasor-tranzakció          |                          |
| Régi számla GUID             | Számla                  | Helyesbítési ILD GUID               | Számlasor-tranzakció          |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Helyesbítési ILD GUID               | Számlasor-tranzakció          |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Helyesbítési ILD GUID               | Számlasor-tranzakció          |                          |
| Jóváhagyott számla helyesbítése | Régi ILD GUID             | Számlasor-tranzakció          | Sztornózott számlájú értékesítési tényadat GUID | Tény                   |
| Régi IL GUID                  | Számla sora             | Sztornózott számlájú értékesítési tényadat GUID | Tény                            |                          |
| Régi számla GUID             | Számla                  | Sztornózott számlájú értékesítési tényadat GUID | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Sztornózott számlájú értékesítési tényadat GUID | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Sztornózott számlájú értékesítési tényadat GUID | Tény                            |                          |
| Régi ILD GUID                 | Számlasor-tranzakció | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Régi IL GUID                  | Számla sora             | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Régi számla GUID             | Számla                  | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Helyesbítési ILD GUID          | Számlasor-tranzakció | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Helyesbítési IL GUID           | Számla sora             | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |
| Helyesbítő számla GUID      | Számla                  | Új, számlázatlan értékesítési tényadat GUID    | Tény                            |                          |

A következő táblázat az előző munkafolyamat tranzakciós kapcsolat entitásának rekordjait mutatja be.

| Esemény                          | 1. tranzakció                 | 1. tranzakció szerepköre | 1. tranzakció típusa           | 2. tranzakció                | 2. tranzakció szerepköre | 2. tranzakció típusa |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Időbejegyzés elküldése          | Naplósor (értékesítés) GUID     | Számlázatlan értékesítés     | msdyn_journalline            | Naplósor (költség) GUID     | Költség               | msdyn_journalline  |
| Jóváhagyási idő                  | Számlázatlan tényadat (értékesítés) GUID  | Számlázatlan értékesítés     | msdyn_actual                 | Tényadat költsége (költség) GUID       | Költség               | msdyn_actual       |
| Számla létrehozása               | Számlasor részletei GUID      | Számlázott értékesítés       | msdyn_invoicelinetransaction | Számlázatlan értékesítési tényleges GUID   | Számlázatlan értékesítés     | msdyn_actual       |
| Számla jóváhagyása           | Tényleges GUID sztornózása         | Sztornózás          | msdyn_actual                 | Eredeti számlázatlan értékesítési GUID | Eredeti           | msdyn_actual       |
| Számlázott értékesítési GUID              | Számlázott értékesítés                  | msdyn_actual       | Számlázatlan értékesítési tényleges GUID   | Számlázatlan értékesítés               | msdyn_actual       |                    |
| Számlatervezet helyesbítése       | Számlasor-tranzakció GUID | Csere          | msdyn_invoicelinetransaction | Számlázott értékesítési GUID            | Eredeti           | msdyn_actual       |
| Számlahelyesbítés jóváhagyása     | Számlázott értékesítés sztornózási GUID    | Sztornózás          | msdyn_actual                 | Számlázott értékesítési GUID            | Eredeti           | msdyn_actual       |
| Új, számlázatlan értékesítési tényadat GUID | Csere                     | msdyn_actual       | Számlázott értékesítési GUID            | Eredeti                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
