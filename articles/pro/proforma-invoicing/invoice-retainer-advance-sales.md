---
title: Foglaló vagy előleg számlázása
description: Ez a témakör foglaló és előleg a Project Operations rendszerben történő számlázásáról tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596195"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Foglaló vagy előleg számlázása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Dynamics 365 Project Operations támogatja az előlegen alapuló szerződéseket és az egyszeri előlegeket. A projektszerződésekben rögzítheti a foglalók vagy egy egyszeri előleg ütemezését. A projekt szerződés szintjén történő rögzítés azonban nem teszi azonnal elérhetővé a foglalót vagy az előleget. Ahhoz, hogy az ügyfelet ténylegesen terhelő számlán egy foglalót vagy előleget használjon, a foglalót vagy az előleget először ki kell számlázni.

Hajtsa végre az alábbi lépéseket egy foglaló vagy előleg számlázásához.

1. Válassza az **Értékesítés** > **Számlázás** > **Foglalók és előlegek** lehetőséget. 
2. Az **Előlegek és foglalók** lapon a szűrő segítségével jelölje ki az adott foglaló vagy előleg számláját, és jelölje ki a **Számlázásra kész** lehetőséget.
3. Hozzon létre számlát manuálisan a **Projekt-szerződések** listájából vagy a részletek oldalról. A foglaló vagy előleg megjelenik a számla vázlatában az **Előlegek és foglalók** szakaszban a **Számla** lapon.
4. Hagyja jóvá a számlát. Ezzel a foglaló vagy az előleg elérhetővé válik használatra. A számlát a **Foglalók és az előlegek** listáját tartalmazó lapon ellenőrizheti. Számlázott előleg vagy foglaló esetén a rendelkezésre álló összeg a rácsban jelenik meg.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Foglaló vagy előleg létrehozása a számla rácsból

A foglaló vagy előleg közvetlenül a számlán is létrehozható.

1. A számla vázlatában az **Előlegek és foglalók** alrácson válassza az **Új** lehetőséget, ha új foglalót vagy előleget szeretne létrehozni. 
2. A **Gyorslétrehozás** lapon adja hozzá a szükséges adatokat, majd kattintson a **Mentés** gombra. A foglaló vagy az előleg a számlához kapcsolódó projektszerződésben jön létre. A foglaló vagy előleg automatikusan **Számlázásra kész** értékkel lesz megjelölve és hozzá lesz adva a **Foglalók és előlegek** alrácsra a **Számla** oldalon.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Számlázott foglaló vagy előleg egyeztetése

A foglaló vagy az előleg számlázása után a számlákban időponttal, kiadásokkal, mérföldkövekkal vagy más projekt alapú díjakkal használhatók vagy egyeztethető. Az ügyfélnél ezen a számlán a számla összege a foglaló vagy az előleg összegével lesz csökkentve.

Minden olyan számlához, ami egy projektszerződéshez lett létrehozva, amely előlegeket vagy foglalókat számláz a Project Operation automatikusan alkalmaz egy foglalót vagy előleget a számlára.

Ez az **Alkalmazott foglalók és előlegek** rácson látható a **Számla** oldalon. A következő táblázat a **Projektszámla** oldal **Alkalmazott foglalók és előlegek** rácsával kapcsolatos mezőkre vonatkozó információkat tartalmaz.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Adatfolyam leírása | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon |Ez az írásvédett mező a számlán szereplő foglaló vagy előleg leírását tartalmazza. Ez az érték nem módosítható a számlán. Ez az érték módosítható a **Projektszerződés** lapon lévő alrácson. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, amely jelzi, hogy a számlán mely foglaló vagy előleg lesz alkalmazva. |
| Kiszállítás dátuma | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon  | Ez az írásvédett mező a számlán szereplő foglaló vagy előleg számlázási dátumát tartalmazza. Ez az érték nem módosítható a számlán. Ez az érték módosítható a **Projektszerződés** lapon lévő alrácson. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, és azt jelzi, hogy a foglaló vagy előleg mikor lett először számlázva az ügyfélnek. |
| Mennyiség | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon  | Ez az írásvédett mező a számlán szereplő foglaló vagy előleg összegét tartalmazza. Ez az érték nem módosítható a számlán. Ez az érték módosítható a **Projektszerződés** lapon lévő alrácson. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, és jelzi a foglaló vagy előleg eredeti összegét, amit az ügyfél kifizetett. |
| Felhasznált mennyiség | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon  | Ez az írásvédett mező azt a számított értéket tartalmazza, amely összefoglalja, hogy a foglaló vagy az előleg mekkora részét használták fel. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, és jelzi a foglaló vagy előleg eredeti összegét, ami már fel lett használva. |
| Kibővített összeg | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon  | Ez a szerkeszthető mező a foglaló vagy előleg összegét tartalmazza, ami fel van használva ezen a projektszámlán. Ez az összeg nem lehet nagyobb, mint ami elérhető az előleg. A rendszer ezt a mezőt automatikusan kiszámítja a rács **Összeg** és **Felhasznált összeg** mezői közötti különbségként. Csökkentheti ezt az összeget, hogy az rendelkezésre állónál kevesebbet használjon fel de a rendelkezésre álló összeg fölé nem növelheti az összeget. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, és jelzi a foglaló vagy előleg eredeti összegét, ami fel van használva a számlán. |
| Foglaló összegének egyenlege. | Az **Alkalmazott foglalók és előlegek** rács a **Projektszámla** oldalon  | Ez az írásvédett mező azt a értéket biztosítja, hogy a foglaló vagy az előleg mekkora része marad meg a számla megerősítése után. | Ez a mező a nyomtatott számlán az ügyfélnek megjeleníthető, és jelzi, hogy mennyi marad a foglaló vagy előleg eredeti összegéből a számla jóváhagyását és kifizetését követően. |
