---
title: Tranzakciós kapcsolatok – Különböző tranzakciótípusok tényleges adatainak összekapcsolása
description: Ez a témakör bemutatja, hogy a tranzakciós kapcsolat hogyan használható a különböző típusú tényleges adatok összekapcsolására a jövedelmezőség, a számlázási hátralék és a számlázott és a nem számlázott bevételszámítások nyomon követése érdekében.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580781"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Tranzakciós kapcsolatok – Különböző tranzakciótípusok tényleges adatainak összekapcsolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A tranzakciókapcsolati rekordok úgy jönnek létre, hogy összekapcsolják a különböző típusú tényleges adatokat, mivel az idő-, költség- vagy anyaghasználat életciklusa az ajánlat vagy az értékesítés előtti szakaszból a szerződés szakaszába, a jóváhagyásokba és/vagy visszahívásokba, a számlázásba és potenciálisan a jóváírásba vagy a helyesbítő számlázásba kerül.

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![Időbejegyzések feldolgozása a Projektműveletek mezőben.](media/basic-guide-17.png)

A Projektműveletek projekt életciklusában szereplő időbejegyzések feldolgozása az alábbi lépéseket követi: 

1. Az időtétel beküldése két naplósor létrehozását eredményezi: egyet a költséghez és egyet a nem számlázott eladásokhoz. 
2. Az időbevitel esetleges jóváhagyása két tényleges értéket eredményez: egyet a költséghez és egyet a nem számlázott értékesítésekhez. Ez a két tényleges érték tranzakciós kapcsolatokkal kapcsolódik.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre.
4. A számla megerősítésekor ez két új tényleges értéket hoz létre: egy nem számlázott értékesítési sztornírozást és egy számlázott értékesítés tényleges értékét. A meg nem oldott értékesítési sztornírozott és az eredeti nem számlázott értékesítési tényleges a tranzakciós kapcsolatok megfordításával kapcsolódik egymáshoz. A számlázott értékesítések és az eredeti, megszámlázatlan értékesítési tényleges adatok is kapcsolódnak ahhoz, hogy megmutassák az egykor elmaradt vagy folyamatban lévő munka (folyamatban lévő) bevételei és a jelenleg számlázott bevétel közötti kapcsolatot.   

A feldolgozási munkafolyamat minden eseménye elindítja a rekordok létrehozását a **Tranzakciókapcsolat** táblában. Ez segít az időbevitel, a naplósor, a tényleges és a számlasor részletei között létrehozott rekordok közötti kapcsolatok nyomának létrehozásában.

Az alábbi táblázat az előző munkafolyamat Tranzakciókapcsolati **entitásának** rekordjait mutatja be.

|Esemény                   |1. tranzakció                 |1. tranzakció szerepköre |1. tranzakció típusa       |2. tranzakció          |2. tranzakció szerepköre |2. tranzakció típusa |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Időbejegyzés elküldése   |Naplósor (értékesítés) GUID     |Számlázatlan értékesítés |msdyn_journalline            |Naplósor (költség) GUID     |Költség            |msdyn_journalline  |
|Jóváhagyási idő           |Számlázatlan tényadat (értékesítés) GUID  |Számlázatlan értékesítés |msdyn_actual                 |Tényadat költsége (költség) GUID       |Költség            |msdyn_actual       |
|Számla létrehozása        |Számlasor részletei GUID      |Számlázott értékesítés   |msdyn_invoicelinetransaction |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számla jóváhagyása    |Tényleges GUID sztornózása         |Sztornózás      |msdyn_actual                 |Eredeti számlázatlan értékesítési GUID |Eredeti        |msdyn_actual       |
|                        |Számlázott értékesítési GUID             |Számlázott értékesítés   |msdyn_actual                 |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számlatervezet helyesbítése |Számlasor-tranzakció GUID|Csere      |msdyn_invoicelinetransaction |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|Számlahelyesbítés jóváhagyása|Számlázott értékesítés sztornózási GUID  |Sztornózás      |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|                        |Új, nem számlázott értékesítési GUID azonosító |Csere            |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |


Az alábbi ábra a különböző típusú tényleges értékek között a Projektműveletek mezőben szereplő időbejegyzések példájával létrehozott hivatkozásokat mutatja be.

> ![Hogyan kapcsolódnak egymáshoz a különböző típusú tényleges értékek a Projektműveletekben?](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
