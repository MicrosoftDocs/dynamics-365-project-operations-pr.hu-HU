---
title: Javasolt erőforrások áttekintése
description: Ez a témakör információt nyújt a projekt erőforrásainak javaslatáról.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401176"
---
# <a name="review-proposed-resources"></a>Javasolt erőforrások áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az erőforrás-kezelők erőforrás-igénylés felhasználásával erőforrást javasolhatnak a projektmenedzser számára.

1. A kérési rácsból vagy maga a kérelemből válassza a **Források keresése** lehetőséget.
2. Az **Ütemezési asszisztens** oldalon válassza ki az erőforrást, majd az **Erőforrás foglalás létrehozása** ablaktáblában a **Foglalási állapot** mezőben válassza a **Foglalás** lehetőséget.

A következő állapotfrissítések történnek:

- Az **Ütemezési asszisztens** oldalon az állapotjelzők frissülnek, jelezve, hogy a foglalást javasolják, nem pedig keményen lefoglalják.
- Az erőforrás-kérésnél az állapot megváltozik: **Áttekintést igényel**.
- A projekt **Csapat** lapján az általános csapattag **Állapotkérés** értéke megváltozik **Áttekintést igényel** értékre.

A projektvezető elfogadhatja vagy elutasíthatja a javaslatot.

Amikor az erőforrás-kezelők feldolgozzák az erőforrás-kérelmeket, a következő megközelítések bármelyikét használhatják:

- Javasoljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a szükséges órák teljesítéséhez. A javasolt órákat ezután több forrásra osztják, amelyek kielégítik a szükséges órákat. Ebben a forgatókönyvben az órák nem fedhetik át egymást.
- Javasoljon kevesebb erőforrást a szükségesnél. Ebben a forgatókönyvben a javasolt erőforrás-kapacitás kevesebb, mint a kérelmező által megadott szükséges óra. Ezért, amikor a kérelmező elfogadja a javasolt erőforrásokat, nem teljesült erőforrás-követelmény jön létre a fennmaradó kereslet rögzítéséhez.
- Foglaljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a munka befejezéséhez.
- Foglaljon kevesebb erőforrást, mint amennyire szükség van. Ebben a forgatókönyvben a foglalt órák kevesebbek, mint a szükséges órák. A rendszer arra irányul, hogy erőforrásokat javasoljon a foglalás helyett, hogy a kérelmező ellenőrizhesse és nyomon tudja követni a fennmaradó igényeket.

## <a name="resource-availability"></a>Erőforrás elérhetősége

Fontos, hogy az erőforrás-kezelők képesek legyenek megtekinteni az erőforrások rendelkezésre állását és frissíteni a foglalásokat. Bizonyos esetekben nincs hivatalos igény (erőforrás-igény), de az erőforrás-kezelőnek válaszolnia kell egy nem tervezett igényre, amely csatornákon, például e-mailben, telefonhívásban vagy azonnali üzenetben érkezik. Az erőforrás-kezelők az Ütemezési táblát használják az erőforrások és a foglalások frissítésére.

Az erőforrás rendelkezésre állásának kiszámításához az erőforrás munkaidőjét vesszük alapul. Az erőforrás-foglalások felhasználják az erőforrások kapacitását.

Az Ütemezési tábla színeket és árnyalatokat használ a foglalások, a rendelkezésre állás és a túlfoglalások, valamint a foglalások állapotának megjelenítésére. Az Ütemezési tábla beállításai lehetővé teszik a jelmagyarázat megjelenítését.

Ha egy jobbra mutató nyíl jelenik meg az ütemező táblán az egyes foglalható források mellett, az erőforrás kibővíthető, hogy megjelenjen az erőforrás által lefoglalt munka részletei.

Mivel a Dynamics 365 Project Operations a Universal Resource Scheduling-motort használja, ha telepítette a Dynamics 365 Field Service rendszert is, akkor megtekintheti a projektek erőforrás-foglalási és munkarendelési részleteit, illetve minden olyan más entitás részleteit, amelyekre kiterjesztette az ütemezést.

Az egyes erőforrásokkal kapcsolatos további részletek megtekintéséhez kattintson a jobb gombbal az erőforráskártya megnyitásához.



[!INCLUDE[footer-include](../includes/footer-banner.md)]