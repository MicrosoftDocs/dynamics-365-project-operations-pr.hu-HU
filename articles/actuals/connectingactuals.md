---
title: Tranzakciókapcsolatok – Különböző tranzakciótípusok tényadatainak csatolása
description: Ez a cikk bemutatja, hogyan használható a tranzakciós kapcsolat a különböző típusú tényleges adatok összekapcsolására a jövedelmezőség, a számlázási hátralék és a számlázott és a nem számlázott bevételi számítások nyomon követése érdekében.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926089"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Tranzakciókapcsolatok – Különböző tranzakciótípusok tényadatainak csatolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A tranzakciós kapcsolati rekordok azért jönnek létre, hogy összekapcsolják a különböző típusú tényleges adatokat, mivel az idő, a költség vagy az anyaghasználat életciklusa során az árajánlatból vagy az értékesítés előtti szakaszból a szerződéses szakaszba, a jóváhagyások és/vagy visszahívások, a számlázás, valamint az esetleges jóváírási vagy korrekciós számlázás felé halad.

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![Feldolgozási időbejegyzések a Project Operationsben.](media/basic-guide-17.png)

A Project Operations-projekt életciklusában az időbejegyzések feldolgozása az alábbi lépéseket követi: 

1. Az időbevitel beküldése két naplósor létrehozását eredményezi: egyet a költségekhez, egyet pedig a számlázatlan értékesítésekhez. 
2. Az időbevitel esetleges jóváhagyása két tényleges értéket eredményez: egyet a költségekhez, egyet pedig a számlázatlan értékesítésekhez. Ez a 2 tényleges adat tranzakciós kapcsolatokon keresztül kapcsolódik egymáshoz.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre.
4. A számla megerősítésekor ez két új tényleges adatot hoz létre: egy számlázatlan értékesítési fordulatot és egy tényleges számlázott értékesítést. A számlázatlan értékesítési fordulat és az eredeti, számlázatlan értékesítések tényleges visszafordításával kapcsolódnak össze a tranzakciós kapcsolatok visszafordításával. A számlázott értékesítések és az eredeti, számlázatlan értékesítési tényleges adatok szintén kapcsolódnak egymáshoz, hogy megmutassák az egykor hátralékból vagy folyamatban lévő munkából (WIP) származó bevétel és a most kiszámlázott bevétel közötti kapcsolatot.   

A feldolgozási munkafolyamat minden eseménye elindítja a rekordok létrehozását a **Tranzakciós kapcsolat** táblában. Ez segít felépíteni a kapcsolatok az időbevitel, a naplósor, a tényleges és a számlasor részletei között létrehozott rekordok között.

Az alábbi táblázat az előző munkafolyamat Tranzakciós kapcsolat **entitásának** rekordjait mutatja be.

|Esemény                   |1. tranzakció                 |1. tranzakció szerepköre |1. tranzakció típusa       |2. tranzakció          |2. tranzakció szerepköre |2. tranzakció típusa |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Időbejegyzés elküldése   |Naplósor (értékesítés) GUID     |Számlázatlan értékesítés |msdyn_journalline            |Naplósor (költség) GUID     |Költség            |msdyn_journalline  |
|Jóváhagyási idő           |Számlázatlan tényadat (értékesítés) GUID  |Számlázatlan értékesítés |msdyn_actual                 |Tényadat költsége (költség) GUID       |Költség            |msdyn_actual       |
|Számla létrehozása        |Számlasor részletei GUID      |Számlázott értékesítés   |msdyn_invoicelinetransaction |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számla jóváhagyása    |Tényleges GUID sztornózása         |Sztornózás      |msdyn_actual                 |Eredeti számlázatlan értékesítési GUID |Eredeti        |msdyn_actual       |
|                        |Számlázott értékesítési GUID             |Számlázott értékesítés   |msdyn_actual                 |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számlatervezet helyesbítése |Számlasor-tranzakció GUID|Csere      |msdyn_invoicelinetransaction |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|Számlahelyesbítés jóváhagyása|Számlázott értékesítés sztornózási GUID  |Sztornózás      |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|                        |Új, számlázatlan értékesítési GUID |Csere            |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |


Az alábbi ábra azokat a hivatkozásokat mutatja be, amelyek a különböző események különböző típusú tényleges adatai között jönnek létre a Project Operations időbejegyzéseinek példáján keresztül.

> ![Hogyan kapcsolódnak egymáshoz a különböző típusú tényleges adatok a Project Operationsben.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
