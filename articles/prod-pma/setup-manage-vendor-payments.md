---
title: Fizetéskor fizetett szállítói kifizetések beállítása és használata
description: Ez a témakör elmagyarázza, hogyan hozhat létre fizetéskor fizetett (PWP) feltételeket annak érdekében, hogy az ügyfelek kifizetése alapján kiadja a részleges szállítói kifizetéseket.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078071"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Fizetéskor fizetett szállítói kifizetések beállítása és használata

[!include [banner](../includes/banner.md)]

Ha jóváhagyja, hogy a szállító alvállalkozóként működjön, akkor előfordulhat, hogy vissza szeretné tartani a szállítónak a fizetést mindaddig, amíg az ügyfél nem fizeti a projektért. A forgatókönyv támogatásához megadhatja a fizetéskor fizetett (PWP) feltételeket, amikor beállítja a beszerzési rendelést (PO) a szállítóval.

Ha például egy ügyfél összeget fizet egy projektszámlán, akkor a szállítói számla egy részét vagy egészét is felszabadíthatja. Csak olyan PWP feltételeket állítson be, amelyek meghatározzák, hogy a szállító ki lesz fizetve, miután megkapta a kapcsolódó fizetés egy adott százalékát az ügyféltől. Ha egy ügyféltől részleges fizetést kap, a kapcsolódó szállítói számlák némelyikét manuálisan is kiadhatja kifizetésre.

A következő példa a PWP feltételek használatakor felvázolja a folyamatot.

## <a name="example"></a>Példa

A szervezete vállalja, hogy az ügyfelet 100 számítógéppel biztosítja, akik telepített szoftverrel rendelkeznek, 150,00 dollárért (USD) számítógépenként. Ezután felbérel egy szállítót, hogy biztosítsa a telepített szoftverekkel rendelkező számítógépeket. A szerződés értelmében az ügyfélnek jóvá kell hagynia a számítógépek minőségét, mielőtt kifizeti a szervezetet. A szervezet házirendje az, hogy visszatartsa a szállítók felé történő fizetést mindaddig, amíg az ügyfél ki nem fizeti. Ezért úgy állítson be a projektet, hogy PWP a 100 százalékos aránya.

A szállító elküldi Önnek a telepített szoftvert tartalmazó 100 számítógépet, valamint 10 000,00 USD-hoz tartozó számlát. Mivel a PWP feltételei a projekthez vannak beállítva, a számítógépek kézhezvételét követően nem fizeti meg a szállítót. Ehelyett a számítógépeket elküldi az ügyfélnek, valamint egy számlát a 15 000,00-ról. Az ügyfél ellenőrzi a számítógépeket, és jóváhagyja a projekt számla teljes összegét.

Miután megkapta a teljes kifizetést az ügyféltől, a szállítói számla teljes összegét kifizeti: 10 000,00.

## <a name="set-up-pwp-terms-for-a-project"></a>Projekt PWP feltételeinek beállítása

Ha egy projekthez PWP feltételeket állít be, akkor százalékértékként meg kell adnia azt a minimális összeget, amelyet az ügyfélnek ki kell fizetnie a projektért ahhoz, hogy a szállítót kifizesse. A rendszer automatikusan kiszámítja a küszöb összegét a projekthez tartozó vevői számlákban. Az alábbi lépések végrehajtásával állíthatja be a PWP kifejezésekre vonatkozó küszöbértéket.

1. Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre.
2. Keresse meg és nyissa meg azt a projektet, amelyhez be kívánja állítani a PWP vonatkozó feltételeket.
3. A **Szállítói megállapodások** gyorslapon jelölje be a **sor hozzáadása** jelölőnégyzetet.
3. Az **Partnerkód** mezőben válasszon a következő lehetőségek közül:

    - **Táblázat** – a PWP feltételei egyetlen szállítóra vonatkoznak.
    - **Csoport** – a PWP feltételei a szállítói csoport minden szállítója esetében érvényesek.
    - **Összes** – a PWP feltételei minden szállítóra vonatkoznak.

4. Ha az előző lépésben kijelölte a **táblázat** vagy a **csoport** lehetőséget , akkor a **Szállító/szállítói csoport** mezőben válassza ki azt a szállítói vagy szállítói csoportot, amelyre a PWP vonatkozik. Ha az előző lépésben az **összes** lehetőséget választotta , a **szállító/szállító csoport** mezője nem szerkeszthető.
5. Ha a szállítóhoz be van állítva a szállítóhoz tartozó adatmegőrzési feltétel a projektben, akkor a **szállítói megőrzési feltételek** mezőben jelölje ki a megőrzési feltételekhez tartozó szabály azonosítóját.
6. A **PWP küszöbértéke** mezőben adja meg a projekt küszöbének százalékos értékét. A projekthez megadott százalékérték azt a minimális összeget határozza meg, amelyet az ügyfélnek ki kell fizetnie ahhoz, hogy megfizesse a szállítót.

## <a name="create-a-po-that-has-pwp-terms"></a>PWP feltételeket tartalmazó PO létrehozása

Ha a számlát a szállítótól könyveli, ha a szállító PWP feltételeket tartalmaz, akkor ezek a feltételek a PO sorokban jelennek meg. Ha PWP feltételeket tartalmazó PO-t szeretne létrehozni, hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Beszerzés** \> **Beszerzési rendelések** \> **Összes beszerzési rendelés** pontot.
2. A Művelet panelen válassza a **Új** elemet. Ezután a **beszerzési rendelés létrehozása** párbeszédpanelen adja meg a szükséges adatokat, majd kattintson az **OK** gombra.

    Másik lehetőségként nyisson meg egy meglévő PO-t az **Összes beszerzési rendelések** listaoldalon.

4. A **beszerzési rendelés** lapon, a **beszerzésirendelés-sorok** gyorslapon tekintse át a szállítóhoz tartozó Po-sor adatait. A program automatikusan kijelöli a **Fizetés fizetéskor** funkciót, és a **PWP küszöb százalékos érték** mezőjében szereplő értéket a program automatikusan átmásolja a **projektek** lap **PWP küszöb százaléka** mezőjéből.
6. Ha nem szeretne PWP feltételeket alkalmazni a szállítóhoz egy PO-sorhoz, akkor törölje a **fizetés fizetéskor** jelölőnégyzetből. Ebben az esetben a rendszer a **PWP-küszöb százalékos** mezőjét 0 (nulla) értékre állítja vissza.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ügyfélkifizetés frissítése és a szállító kifizetése

Ha egy szállító befejezi a munkát egy projekten, és számlát küld, akkor ellenőriznie kell a projekt állapotát és az ügyfelek számláit, hogy a PWP feltételei teljesültek-e a projekt esetében. Ha teljesülnek a szállító PWP feltételei, megadhatja, hogy a szállítói számla mely sorait kell kifizetni a projekt vevői kifizetései alapján. Ha úgy dönt, hogy kifizeti a szállítót annak ellenére, hogy a PWP feltételei nem teljesültek, akkor a PWP-feltételeket felülbírálhatja a **Szállítói számla fizetéskori fizetéssel** oldalon.

1. Nyissa meg a **projektkezelés és könyvelés** \> **Kérdések és jelentések** \> **Megőrzési vizsgálatok** \> **Szállítói számla fizetéskori fizetéssel**.
2. A **Szállítói számla fizetéskori fizetéssel** oldalon a keresés mezőben adja meg az áttekinteni kívánt szállítói számla megkereséséhez használandó értékeket, majd kattintson a **Keresés** gombra.
3. A **Szállítói számlasorok** gyorslapon jelölje ki a módosítani kívánt sorokat.
4. Ha a **Fizetés fizetéskor** feltételek teljesülése esetén a számla sorában, válassza a **Szállítói kifizetés kiadása** lehetőséget. A **Fizetés fizetéskor** lehetőség törölve van, és a **Fizetésre kész** mező értéke **Igen** értékre változik.
