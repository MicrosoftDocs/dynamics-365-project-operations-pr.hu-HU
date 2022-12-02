---
title: Tranzakciókapcsolatok – Különböző tranzakciótípusok tényadatainak csatolása
description: Ez a cikk azt mutatja be, hogyan használható egy tranzakciókapcsolat különböző típusú tényadatok összekapcsolásához az jövedelmezőség, a számlázási hátralék és a számlázott és a számlázatlan bevételek nyomon követése érdekében.
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

A tranzakciókapcsolati rekordok különféle típusú tényadatokat kapcsolnak össze, ahogy az idő-, költség- vagy anyaghasználati mozog az életciklus során az ajánlattól vagy az értékesítés előtti fázistól a szerződés fázisig, a jóváhagyásokat és/vagy a visszahívásokat, a számlázást és esetlegesen a jóváírási vagy helyesbítő számlázást.

A következő példa az időbejegyzések tipikus feldolgozását mutatja be a Project Operations projekt életciklusában.

> ![Időbejegyzések feldolgozása a Project Operations alkalmazásban.](media/basic-guide-17.png)

Az időbejegyzések feldolgozásához Project Operations projekt életciklusában kövesse az alábbi lépéseket: 

1. Az időbejegyzések beküldése két naplósor létrehozását eredményezi: egy a költségről, egy pedig a nem számlázott értékesítésekről. 
2. Az időbejegyzés végleges jóváhagyása két tényadat létrehozását eredményezi: egy a költségről, egy pedig a nem számlázott értékesítésekről. Ez a 2 tényadat tranzakciókapcsolatok segítségével kapcsolódik.
3. Amikor a felhasználó létrehoz egy projektszámlát, a számlasor tranzakcióját a rendszer a nem számlázott értékesítésből származó tényadatok felhasználásával hozza létre.
4. A számla megerősítését követően ez két új tényadatot hoz létre: a nem számlázott értékesítés sztornózása és a számlázott értékesítés tényadata. A nem számlázott értékesítés sztornózása és az eredeti nem számlázott értékesítési tényadat sztornózó tranzakciókapcsolatokkal van összekapcsolva. A számlázott értékesítések és az eredeti számlázatlan értékesítések tényadatai is kapcsolatban állnak a, hogy mutassák a kapcsolatot a néhai hátralék vagy folyamatban lévő munk bevételével, ami immár számlázott bevétel.   

A feldolgozási munkafolyamat minden eseménye elindítja rekordok létrehozását a **Tranzakciókapcsolat** táblában. Ez segít létrehozni egy kapcsolati útvonalat a rekordok között, amelyek az időbejegyzés, a naplósor, a tényadat és a számlasor részletei között jönnek létre.

A következő táblázat az előző munkafolyamat **Tranzakciós kapcsolat** entitásának rekordjait mutatja be.

|Esemény                   |1. tranzakció                 |1. tranzakció szerepköre |1. tranzakció típusa       |2. tranzakció          |2. tranzakció szerepköre |2. tranzakció típusa |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Időbejegyzés elküldése   |Naplósor (értékesítés) GUID     |Számlázatlan értékesítés |msdyn_journalline            |Naplósor (költség) GUID     |Költség            |msdyn_journalline  |
|Jóváhagyási idő           |Számlázatlan tényadat (értékesítés) GUID  |Számlázatlan értékesítés |msdyn_actual                 |Tényadat költsége (költség) GUID       |Költség            |msdyn_actual       |
|Számla létrehozása        |Számlasor részletei GUID      |Számlázott értékesítés   |msdyn_invoicelinetransaction |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számla jóváhagyása    |Tényleges GUID sztornózása         |Sztornózás      |msdyn_actual                 |Eredeti számlázatlan értékesítési GUID |Eredeti        |msdyn_actual       |
|                        |Számlázott értékesítési GUID             |Számlázott értékesítés   |msdyn_actual                 |Számlázatlan értékesítési tényleges GUID   |Számlázatlan értékesítés  |msdyn_actual       |
|Számlatervezet helyesbítése |Számlasor-tranzakció GUID|Csere      |msdyn_invoicelinetransaction |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|Számlahelyesbítés jóváhagyása|Számlázott értékesítés sztornózási GUID  |Sztornózás      |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |
|                        |Új számlázatlan értékesítések GUID |Csere            |msdyn_actual                 |Számlázott értékesítési GUID            |Eredeti        |msdyn_actual       |


Az alábbi ábra a Project Operations időbejegyzéseinek példája segítségével mutatja be a különböző eseményeken létrehozott különböző ténytípusok között létrehozott hivatkozásokat mutatja be.

> ![Hogyan kapcsolódnak a különböző típusú tényadatok egymáshoz a Project Operations alkalmazásban.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
