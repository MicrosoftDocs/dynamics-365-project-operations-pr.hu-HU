---
title: Erőforrás-egyeztetés áttekintése
description: Ez a cikk olyan információkat tartalmaz, amelyek segítenek biztosítani, hogy a projektek erőforrás-foglalásai és hozzárendelései igazodjanak egymáshoz.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926319"
---
# <a name="resource-reconciliation-overview"></a>Erőforrás-egyeztetés áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A csapat tagjai számára a foglalások és a megbízások lazán kapcsolódnak egymáshoz. Más szavakkal: az erőforrásoknak lehetnek hozzárendelései, de foglalásai nem, vagy lehetnek foglalásaik, de nem lehetnek hozzárendeléseik. Ideális esetben a foglalásokat és a feladatokat össze kell hangolni, hogy az erőforrások képesek legyenek a feladat-hozzárendelések végrehajtására. Előfordulhat azonban, hogy a foglalások rendelkezésre álláson alapulnak, és a projekt folytatásakor a feladatok ütemezése változhat. Ezért a foglalások és feladatok laza csatolása rugalmasságot biztosít.

A **Projektek** oldalon lévő **Egyeztetés** fül lehetővé teszi a projektmenedzserek számára, hogy összehangolják a csapattagok foglalásait és a projektcsoportokhoz rendelt megbízásaikat.

Az **Egyeztetés** lap a foglalásokat és a hozzárendeléseket az egyes csoporttagok egyedi feladat-hozzárendelésének szintjéig mutatja. Az órák megjelennek a cellákban, amelyek hónapoktól napokig tartó időszakokat reprezentálhatnak. A lapon a projekt teljes nettó összértéke, valamint az **Összesen** oszlop is látható.

Az egyes erőforrások esetében az **Egyeztetés** fül kiszámítja a különbséget a csapattag foglalása és a csoporttag feladatainak összeállítása között. Ideális esetben ennek a különbségnek 0-nak (nulla) kell lennie. Más szavakkal, nem lehet különbség a foglalások és a megbízások között. A különbségek színesek és árnyaltak, hogy felhívják a figyelmet két körülményre:

- **Foglalási hiány** - Foglalási hiány akkor fordul elő, ha az erőforrás több hozzárendeléssel rendelkezik, mint a foglalások. Mivel a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt azáltal, hogy az erőforrás foglalásait kiterjeszti a hiány fedezésére.
- **Többletfoglalások** - Többletfoglalások akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz. Ez a feltétel elfogadható lehet azokban az esetekben, amikor az erőforrást a projekthez a feladat-hozzárendelés megtörténte előtt lefoglalták. Más esetekben azonban, amikor nincs terv az erőforrás feladatokhoz való hozzárendelésére, a projektmenedzsernek meg kell fontolnia az erőforrás foglalásának törlését. Így a kapacitás másik projekthez is felhasználható.

Bizonyos esetekben, ha az időt a napi szintnél magasabb szinten nézi (például a hónap szintjén), akkor az erőforrás nettó különbsége nulla lehet (más szóval, foglalások egyenlőek a megbízásokkal). Ha azonban az időt heti szinten tekinti, akkor láthatja, hogy az első héten nulla órás megbízások és 40 órás foglalások vannak, a második héten pedig 40 órás megbízások és nulla órás foglalások vannak. Összességében a foglalások és a feladatok összeegyeztethetők, de hetente különböznek.

Ha az időt magasabb szinteken tekinti meg, akkor az **Egyeztetés** lapon lévő cellák jelzik, hogy az alacsonyabb szinteken eltérések vannak. Ha egy cellába duplán koppint, nagyíthat, hogy megnézze a különbséget. Ezután nyomja meg és tartsa nyomva (vagy jobb egérgombbal kattintson) a kicsinyítéshez. Ha kiválaszt egy erőforrást, majd használja a rács eszköztár **Következő különbség** vezérlőjét, a következő különbséghez ugorhat az adott erőforrás foglalása és hozzárendelése között. Ezután az **Előző különbség** vezérlővel visszatérhet. A különbségjelzőt és a navigációs viselkedést a **Beállítások** alatt is kikapcsolhatja.

Ha az erőforráshoz feladatok vannak hozzárendelve, de nincs foglalása, akkor a **Projektek** oldalon az **Egyeztetés** fülön lévő foglalási hiányt, majd válassza a **Foglalás kiterjesztése** lehetőséget. Megjelenik a **Foglalás kiterjesztése** párbeszédpanel, amely megmutatja az erőforrás hiányának kezeléséhez szükséges foglalást. A párbeszédpanel ezenkívül megmutatja az erőforrás meglévő foglalásait az összes projektben vagy más ütemezhető entitásban. Ha az **OK** lehetőséget választja az erőforrás foglalásának elkészítéséhez, az erőforrás elérhetőségétől függetlenül túlfoglalást okozhat.

A **Foglalás kiterjesztése** művelettel létrehozott foglalások az elsődleges projektkövetelményhez kapcsolódnak. A bővítmény kezdeményezésekor nem lehet meghatározni a kiterjesztendő konkrét követelményt, mivel az erőforrás a projekt több követelményéhez is hozzá lehet társítva.

A projektmenedzser vagy az erőforrás-kezelő ezután felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás túlfoglalása meghaladja a kapacitást.


[!INCLUDE[footer-include](../includes/footer-banner.md)]