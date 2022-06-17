---
title: Tranzakciós eredetek – Tényleges adatok csatolása a forrásukhoz
description: Ez a cikk azt ismerteti, hogy a tranzakciós eredet fogalmát hogyan használják a tényleges adatok eredeti forrásrekordokhoz, például időbevitelhez, költségbevitelhez vagy anyaghasználati naplókhoz való csatolására.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921305"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Tranzakciós eredetek – Tényleges adatok csatolása a forrásukhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A tranzakciós eredetrekordok azért jönnek létre, hogy a tényleges adatokat a forrásukhoz kössék, például az időbejegyzéseket, a költségbejegyzéseket, az anyaghasználati naplókat és a projektszámlákat.

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![Teljes feldolgozási idő a Project Operationsben.](media/basic-guide-17.png)
 
1. Az időbevitel beküldése két naplósor létrehozását eredményezi: egyet a költségekhez, egyet pedig a számlázatlan értékesítésekhez.
2. Az időbevitel esetleges jóváhagyása két tényleges értéket eredményez: egyet a költségekhez, egyet pedig a számlázatlan értékesítésekhez.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre.
4. A számla megerősítését követően két új tényadat jön létre: a nem számlázott értékesítés sztornózása és a számlázott értékesítés tényadata.

A feldolgozási munkafolyamat minden eseménye elindítja rekordok létrehozását a Tranzakció eredete entitásban, hogy segítsen felépíteni a kapcsolatok nyomon követését e rekordok között, amelyek az időbevitel, a naplósor, a tényleges és a számlasor részletei között jönnek létre.

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


Az alábbi ábra azokat a hivatkozásokat mutatja be, amelyek a tényleges adatok és azok forrásai között jönnek létre különböző eseményeken, a Project Operations időbejegyzéseinek példáján keresztül.

> ![Hogyan kapcsolódnak a tényleges adatok a forrásrekordokhoz a Project Operationsben.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
