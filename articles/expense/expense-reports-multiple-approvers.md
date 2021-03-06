---
title: Költségjelentések és több jóváhagyó
description: Ez a témakör az olyan költségjelentésekről tartalmaz információkat, amelyeket több személynek kell jóváhagynia.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897094"
---
# <a name="expense-reports-and-multiple-approvers"></a>Költségjelentések és több jóváhagyó

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A szervezet költség-jóváhagyási szabályzatától függően előfordulhat, hogy több személynek is jóvá kell hagynia egy elküldött költségjelentést. Amikor beállítja a munkafolyamatot a költségjelentés jóváhagyásához, felvehet olyan munkafolyamat-elemeket, amelyek a költségjelentés egy vagy több jóváhagyójához tartozó feladatokat vagy lépéseket tartalmaznak. Előfordulhat például, hogy az összes költségjelentést két külön személynem kell jóváhagynia: a jelentést elküldő alkalmazott vezetőjének és a kötelezettségek koordinátorának.

Ha úgy dönt, hogy a költségjelentést több személynek kell jóváhagynia, a következő módokon adhatja hozzá a munkafolyamat-elemeket:

- Adjon hozzá egy jóváhagyási elemet, amely egyetlen lépésből áll. Előfordulhat például, hogy a lépéshez egy költségjelentést hozzá kell rendelni egy felhasználói csoporthoz, és hogy a felhasználói csoport tagjai felének jóvá kell hagynia.
- Adjon hozzá egy jóváhagyási elemet, amely több lépésből áll. A jóváhagyási elem például a következő lépésekből állhat:

    1. A költségjelentést elküldő alkalmazott vezetője jóváhagyja.
    2. A kötelezettségek adminisztrátora ellenőrzi a nyugtákat és a költségjelentés tételeit.
    3. A költségvetés tulajdonosa jóváhagyja a költségjelentést.

- Több jóváhagyási elem hozzáadása, amelyek mindegyike egy lépésből áll. Hozzáadhat például egy külön jóváhagyási elemet az egyes következő lépésekhez:

    1. Az alkalmazott felettese jóváhagyja a költségjelentést.
    2. A költségvetés tulajdonosa jóváhagyja a költségjelentést.
