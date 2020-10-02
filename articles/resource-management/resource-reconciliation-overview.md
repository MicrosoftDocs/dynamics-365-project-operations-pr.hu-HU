---
title: Erőforrás-egyeztetés áttekintése
description: Ez a témakör az erőforrások és a hozzárendelések lefoglalásáról igazított projektekhez való hozzárendeléséről nyújt információt.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897454"
---
# <a name="resource-reconciliation-overview"></a>Erőforrás-egyeztetés áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A csapat tagjai számára a foglalások és a megbízások lazán kapcsolódnak egymáshoz. Más szavakkal: az erőforrásoknak lehetnek hozzárendelései, de foglalásai nem, vagy lehetnek foglalásaik, de nem lehet hozzárendeléseik. Ideális esetben a foglalásokat és a feladatokat össze kell hangolni, hogy az erőforrások képesek legyenek a feladat-hozzárendelések végrehajtására. Előfordulhat azonban, hogy a foglalások rendelkezésre álláson alapulnak, és a projekt folytatásakor a feladatok ütemezése változhat. Ezért a foglalások és feladatok laza csatolása rugalmasságot biztosít.

A **Projekt** űrlap **Egyeztetés** lapján a projektmenedzserek összehangolhatják a csapattagok foglalásait és a projektcsoportokhoz rendelt hozzárendeléseiket.

Az **Egyeztetés** lap ezenkívül a foglalásokat és a hozzárendeléseket az egyes csoporttagok egyedi feladat-hozzárendelésének szintjéig mutatja. Az órák olyan cellákban jelennek meg, amelyek hónapoktól napokig terjedő időszakokat jelölnek.

A lapon a projekt teljes nettó összértéke, valamint az **Összesen** oszlop is látható.

Az egyes erőforrások esetében a fül kiszámítja a különbséget a csapattag foglalása és a csoporttag feladatainak összeállítása között. Ideális esetben ennek a különbségnek 0-nak (nulla) kell lennie. Más szavakkal, nem lehet különbség a foglalások és a megbízások között. A különbségek színesek és árnyaltak, hogy felhívják a figyelmet két körülményre:

- **Foglalási hiány** - Foglalási hiány akkor fordul elő, ha az erőforrás több hozzárendeléssel rendelkezik, mint a foglalások. Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére.
- **Többletfoglalások** - Többletfoglalások akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz. Ez a feltétel elfogadható lehet azokban az esetekben, amikor az erőforrást a projekthez a feladat-hozzárendelés megtörténte előtt lefoglalták. Más esetekben azonban az erőforrást nem tervezik feladatokhoz rendelni. Ezekben az esetekben a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak visszavonását, hogy a kapacitás felhasználható legyen egy másik projekthez.

Bizonyos esetekben, ha az időt a napi szintnél magasabb szinten nézi (például a hónap szintjén), akkor az erőforrás nettó különbsége nulla lehet (más szóval, foglalások = megbízások). Ha azonban az időt heti szinten tekinti, akkor láthatja, hogy az első héten nulla órás megbízások és 40 órás foglalások vannak, a második héten pedig 40 órás megbízások és nulla órás foglalások vannak. Összességében a foglalások és a feladatok összeegyeztethetők, de hetente különböznek.

Ha az időt magasabb szinteken tekinti meg, akkor az **Egyeztetés** lapon lévő cellák jelzik, hogy az alacsonyabb szinteken eltérések vannak. Ha egy cellába duplán kattint, nagyíthat, hogy megnézze a különbséget. Ezután jobb egérgombbal kattinthat a kicsinyítéshez. Ha kiválaszt egy erőforrást, majd használja a rács eszköztár **Következő különbség** vezérlőjét, a következő különbséghez ugorhat az adott erőforrás foglalása és hozzárendelése között. Ezután az **Előző különbség** vezérlővel visszatérhet. A különbségjelzőt és a navigációs viselkedést a **Beállítások** alatt is kikapcsolhatja.


Ha az erőforráshoz feladatok vannak hozzárendelve, de nincs foglalása, akkor a **Projektek** oldalon, az **Egyeztetés** lapon válassza ki a foglalási hiányt, majd válassza a **Foglalás kiterjesztése** lehetőséget. Megjelenik a **Foglalás kiterjesztése** párbeszédpanel, amely megmutatja az erőforrás hiányának kezeléséhez szükséges foglalást. Ezenkívül megmutatja az erőforrás meglévő foglalásait az összes projektben vagy más ütemezhető entitásban. Ha az **OK** lehetőséget választja az erőforrás foglalásának elkészítéséhez, az erőforrás elérhetőségétől függetlenül túlfoglalást okozhat.

A projektmenedzser vagy az erőforrás-kezelő ezután felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás túlfoglalása meghaladja a kapacitást.

