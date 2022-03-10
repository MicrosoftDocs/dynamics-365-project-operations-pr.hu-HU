---
title: Tények csatolása az eredeti rekordokhoz
description: Ez témakör ismerteti, hogyan kapcsolhatja össze a tényleges adatokat az eredeti rekordokkal, például az időbejegyzési, költségbejegyzési vagy anyaghasználati naplókkal.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991759"
---
# <a name="link-actuals-to-original-records"></a>Tények csatolása az eredeti rekordokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A Dynamics 365 Project Operations-ben lévő *üzleti tranzakció* olyan absztrakt fogalom, amelyet nem képvisel semmilyen entitás. Az entitások gyakori mezői és folyamatai azonban az üzleti tranzakciók fogalmának használatára vannak kialakítva. A következő entitások használják a fogalmat:

- Árajánlatsor részletei
- Szerződéssor részletei
- Becslés sorai
- Naplósorok
- Tények

Ezen entitások közül az **Árajánlatsor részletei**, a **Szerződéssor részletei** és a **Becsléssorok** a projekt életciklusának becslési fázisára vannak leképezve. A **Naplósorok** és a **Tényadat-entitások** a projekt életciklusának végrehajtási fázisára vannak leképezve.

A Project Operations az öt entitás rekordjait üzleti tranzakcióként ismeri el. Az egyetlen különbség, hogy a becslési fázisra leképezett entitásokban lévő rekordok pénzügyi előrejelzésnek számítanak, míg a végrehajtási fázishoz leképezett entitások bejegyzései olyan pénzügyi tények, amelyek már megtörténtek.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Az üzleti tranzakciók esetében egyedi fogalmak
A következő fogalmak egyediek az üzleti tranzakciók fogalma esetében:

- Tranzakció típusa
- Tranzakcióosztály
- Tranzakcióeredet
- Tranzakciós kapcsolat

### <a name="transaction-type"></a>Tranzakció típusa

A tranzakció típusa a projektre gyakorolt pénzügyi hatás időzítését és kontextusát jelenti. Ezt egy értékkészlet képviseli, amelynek a következő támogatott értékei a Project Operations szolgáltatásban szerepelnek:

  - Költség
  - Projektszerződés
  - Számlázatlan értékesítés
  - Számlázott értékesítés
  - Szervezetek közötti értékesítések
  - Erőforrás-kezelő részleg költsége

### <a name="transaction-class"></a>Tranzakcióosztály

A tranzakciós osztály a projektekkel kapcsolatban felmerülő költségek különböző típusait jelöli. Ezt egy értékkészlet képviseli, amelynek a következő támogatott értékei a Project Operations szolgáltatásban szerepelnek:

  - Idő
  - Költség
  - Anyag
  - Díj
  - Mérföldkő
  - Adó

A **Mérföldkő** értékét általában az üzleti logika használja a rögzített árú számlázáshoz a Project Operations szolgáltatásban.

### <a name="transaction-origin"></a>Tranzakcióeredet

A **Tranzakció eredete** az egyes üzleti tranzakciók eredetét tároló entitás. Ahogy a projekt elindul, minden üzleti tranzakció egy másik üzleti tranzakciót fog generálni, ami szintén létrehoz egy másikat, és így tovább. A tranzakció eredeti entitásának célja az egyes tranzakciók eredetére vonatkozó adatok tárolása a jelentéskészítés és a nyomon követhetőség érdekében. 

### <a name="transaction-connection"></a>Tranzakciós kapcsolat

A **tranzakciós kapcsolat** olyan entitás, amely két hasonló üzleti tranzakció közötti kapcsolatot tárolja, például a költség és a kapcsolódó értékesítések tényleges értékét, vagy a tranzakció sztornózását, amelyet számlázási tevékenységek, például a számla visszaigazolása vagy a számla helyesbítése eredményeznek.

A **tranzakció eredete** és a **tranzakciós kapcsolat** együttesen segítenek nyomon követni az üzleti tranzakciók és az olyan műveletek közötti kapcsolatokat, amelyek egy adott üzleti tranzakció létrehozását okozzák.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Példa: Hogyan működik a tranzakció eredete a tranzakciós kapcsolattal?

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![Feldolgozási idő entitások a Project Service életciklusban.](media/basic-guide-17.png)
 
1. Az időbejegyzések beküldése két naplósor létrehozását eredményezi: egyet a költségről, és egyet pedig a nem számlázott értékesítésekről.
2. Az időbejegyzés végleges jóváhagyása két tényadat létrehozását eredményezi: egy tényadatot a költségről, egy tényadatot pedig a nem számlázott értékesítésekről.
3. Amikor egy új projektszámla jön létre, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre. 
4. A számla megerősítését követően két új tényadat jön létre: a nem számlázott értékesítés sztornózása tényadata és a számlázott értékesítés tényadata.

Ezen események mindegyike rekordot hoz létre a **Tranzakció eredete** és a **Tranzakciókapcsolat** entitásokban. Ezek az új rekordok segítenek létrehozni egy kapcsolati előzményt a rekordok között, amelyek az időbejegyzés, a naplósor, a tényadatok és a számlasor részletei között jönnek létre.

A következő tábla a munkafolyamat **tranzakció eredete** entitásának rekordjait mutatja be.

| Esemény                        | Eredet                   | Eredet típusa                       | Tranzakció                       | Tranzakciótípus         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Időbejegyzés elküldése        | Időbejegyzés-rekord GUID   | Időbejegyzés                        | Naplósor-bejegyzés GUID (költség)   | Naplósor             |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Naplósor-bejegyzés GUID (értékesítés)  | Naplósor                      |                          |
| Jóváhagyási idő                | Naplósor-bejegyzés GUID | Naplósor                      | Számlázatlan értékesítési rekord GUID        | Tény                   |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Számlázatlan értékesítési rekord GUID        | Tény                            |                          |
| Naplósor-bejegyzés GUID     | Naplósor             | Költség tényleges rekordja GUID           | Tény                            |                          |
| Időbejegyzés-rekord GUID       | Időbejegyzés               | Költség tényleges rekordja GUID           | Tényleges                            |                          |
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

A következő tábla a munkafolyamat **tranzakció kapcsolat** entitásának rekordjait mutatja be.

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
