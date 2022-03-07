---
title: Több jóváhagyó egy költségjelentésen
description: Ez a témakör az olyan költségjelentésekről tartalmaz információkat, amelyeket több embernek kell jóváhagynia.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005254"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Több jóváhagyó egy költségjelentésen

A szervezet költség-jóváhagyási szabályzatától függően előfordulhat, hogy több személynek is jóvá kell hagynia egy munkavállaló által beküldött költségjelentést. Amikor beállítja a munkafolyamatot a költségjelentés jóváhagyásához, felvehet olyan munkafolyamat-elemeket, amelyek a költségjelentés egy vagy több jóváhagyójához tartozó feladatokat vagy lépéseket tartalmaznak. Előfordulhat például, hogy az összes költségjelentést először a jelentést elküldő alkalmazott vezetőjének majd a kötelezettségek koordinátorának kell jóváhagynia.

Ha úgy dönt, hogy a költségjelentést több személynek kell jóváhagynia, a következő módokon adhatja hozzá a munkafolyamat-elemeket:

- Adjon hozzá egy jóváhagyási elemet, amely egyetlen lépésből áll. Előfordulhat például, hogy a lépéshez egy költségjelentést hozzá kell rendelni egy felhasználói csoporthoz, és hogy a felhasználói csoport tagjai felének jóvá kell hagynia.
- Adjon hozzá egy jóváhagyási elemet, amely több lépésből áll. A jóváhagyási elem például a következő lépésekből állhat:

    1. A költségjelentést elküldő alkalmazott vezetője jóváhagyja.
    2. A kötelezettségek adminisztrátora ellenőrzi a nyugtákat és a költségjelentés tételeit.
    3. A költségvetés tulajdonosa jóváhagyja a költségjelentést.

- Több jóváhagyási elem hozzáadása, amelyek mindegyike egy lépésből áll. Hozzáadhat például egy külön jóváhagyási elemet az egyes következő lépésekhez:

    1. Az alkalmazott felettese jóváhagyja a költségjelentést.
    2. A költségvetés tulajdonosa jóváhagyja a költségjelentést.


[!INCLUDE[footer-include](../includes/footer-banner.md)]