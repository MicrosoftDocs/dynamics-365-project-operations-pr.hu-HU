---
title: Javasolt erőforrások áttekintése
description: Ez a cikk információt nyújt a projekt erőforrásainak javaslatáról.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183977"
---
# <a name="review-proposed-resources"></a>Javasolt erőforrások áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az erőforrás-kezelők erőforrás-igénylés felhasználásával erőforrást javasolhatnak a projektmenedzser számára.

A javasolt erőforrások felülvizsgálatához kövesse az alábbi lépéseket:

1. A **Kérelem** rácson vagy magán a kérésen válassza az **Erőforrások keresése** lehetőséget.
2. Az **Ütemezési asszisztens** oldalon válassza ki az erőforrást, majd erősítse meg, hogy az összes javasolt órát tartalmazza a javasolt foglalás.
3. Az **Erőforrásfoglalás létrehozása** ablaktáblán állítsa a **Foglalási státusz** mezőt **Javasoltra**, majd válassza a **Foglalás** lehetőséget.

    > [!NOTE]
    > A **Foglalási státusz** **Javasoltra** állítása nem foglalja le az erőforrást, és nem helyettesíti az általános erőforrást a megnevezett csapattaggal.

    A következő állapotfrissítések történnek:

    - Az **Ütemezési asszisztens** oldalon a státuszjelzők frissülnek, hogy jelezzék, hogy a foglalás javasolt, nem pedig véglegesen lefoglalt.
    - Az erőforrás-kérelmen a kérelem felülvizsgálójának át kell változtatnia az állapotot **Áttekintés igényel** értékre.
    - A projekt **Csapat** lapján az általános csapattag **Állapotkérés** értéke automatikusan megváltozik **Áttekintést igényel** értékre.

A projektmenedzser elfogadhatja vagy elutasíthatja a javaslatot.

Amikor az erőforrás-kezelők feldolgozzák az erőforrás-kérelmeket, a következő megközelítések bármelyikét használhatják:

- Javasoljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a szükséges órák teljesítéséhez. A javasolt órákat ezután több forrásra osztják, amelyek kielégítik a szükséges órákat. Ebben a forgatókönyvben az órák nem fedhetik át egymást.
- Javasoljon kevesebb erőforrást a szükségesnél. Ebben a forgatókönyvben a javasolt erőforrás-kapacitás kevesebb, mint a kérelmező által megadott szükséges óra. Ha az igénylő elfogadja a javasolt erőforrásokat, akkor a fennmaradó igény kielégítetlen erőforrásigényét a rendszer létrehozza.
- Foglaljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a munka befejezéséhez.
- A szükségesnél kevesebb erőforrást foglaljon le. Ebben a forgatókönyvben a foglalt órák kevesebbek, mint a szükséges órák. A rendszer a foglalások helyett erőforrás-ajánlatokat tesz, így az igénylő ellenőrizheti és nyomon követheti a fennmaradó igényeket.

## <a name="resource-availability"></a>Erőforrás elérhetősége

Az erőforrás-kezelőknek képesnek kell lenniük az erőforrások elérhetőségének megtekintésére és a foglalások frissítésére. Egyes esetekben nincs hivatalos igény (erőforrás-kérelem). Az erőforrás-kezelőnek azonban reagálnia kell a nem tervezett, más csatornákon, például e-maileken, telefonhívásokon vagy azonnali üzeneteken keresztül érkező igényekre. Az erőforrás-menedzserek az erőforrások és foglalások frissítésére az **ütemezőtáblát** használják.

Az erőforrás munkaidejét használják az erőforrás rendelkezésre állásának kiszámításának alapjául. Az erőforrás-foglalások felhasználják az erőforrások kapacitását.

Az **Ütemezési tábla** színekkel és árnyékolással mutatja a foglalásokat, a rendelkezésre állást, a túlfoglalásokat és a foglalások állapotát. Az **Ütemezési tábla** egy beállítása lehetővé teszi a jelmagyarázat megjelenítését.

Ha egy jobbra mutató nyíl jelenik meg egy foglalható erőforrás mellett az **Ütemezési táblán**, az erőforrás kibontható, és megjelenítheti az erőforrással lefoglalt munka részleteit.

Mivel a Dynamics 365 Project Operations a Universal Resource Scheduling motort használja, ha telepítette a Dynamics 365 Field Service rendszert is, akkor megtekintheti a projektek erőforrás-foglalási, munkamegrendelési és minden más entitás részleteit, amelyekre az ütemezést kiterjesztette.

Ha további részleteket szeretne megtudni egy erőforrásról, kattintson rá a jobb gombbal, és nyissa meg az erőforráskártyát.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
