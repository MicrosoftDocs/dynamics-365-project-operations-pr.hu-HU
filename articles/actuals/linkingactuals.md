---
title: Tranzakció eredete – Tényleges adatok csatolása a forrásukhoz
description: Ez a témakör bemutatja, hogy a tranzakció eredetének fogalmát hogyan használják a tényleges adatok eredeti forrásrekordokhoz, például időbevitelhez, költségbevitelhez vagy anyaghasználati naplókhoz való kapcsolására.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584829"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Tranzakció eredete – Tényleges adatok csatolása a forrásukhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A tranzakció eredetrekordjai úgy jönnek létre, hogy a tényleges adatokat összekapcsolják a forrásukkal, például az időtételekkel, a költségtételekkel, az anyaghasználati naplókkal és a projektszámlákkal.

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![A feldolgozási idő teljes egészében a Projektműveletekben.](media/basic-guide-17.png)
 
1. Az időtétel beküldése két naplósor létrehozását eredményezi: egyet a költséghez és egyet a nem számlázott eladásokhoz.
2. Az időbevitel esetleges jóváhagyása két tényleges értéket eredményez: egyet a költséghez és egyet a nem számlázott értékesítésekhez.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre.
4. A számla megerősítését követően két új tényadat jön létre: a nem számlázott értékesítés sztornózása és a számlázott értékesítés tényadata.

A feldolgozási munkafolyamat minden eseménye elindítja a Tranzakciók származási entitásában lévő rekordok létrehozását, hogy segítsen az időbevitel, a naplósor, a tényleges és a számlasor részletei között létrehozott rekordok közötti kapcsolatok nyomának létrehozásában.

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
| Helyesbítő számla GUID      | Számla                  | Új, számlázatlan értékesítési tényadat GUID    | Tényleges                            |                          |


Az alábbi ábra a tényleges adatok és forrásaik között különböző eseményeken létrehozott hivatkozásokat mutatja be a Projektműveletek időbejegyzéseinek példájával.

> ![Hogyan kapcsolódnak a tényleges adatok a Projektműveletek forrásrekordjaihoz?](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
