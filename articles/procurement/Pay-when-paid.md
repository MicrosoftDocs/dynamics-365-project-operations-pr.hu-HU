---
title: Fizetéskor fizetett szállítói kifizetések
description: Ez témakör ismerteti, hogyan használható a fizetéskor fizetett (PWP) forgatókönyv.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525384"
---
# <a name="pay-when-paid-vendor-payments"></a>Fizetéskor fizetett szállítói kifizetések

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez témakör ismerteti, hogyan használható a fizetéskor fizetett (PWP) forgatókönyv.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>PWP fizetési feltételekkel rendelkező megrendelés létrehozása

Ha egy számlát a szállítótól könyvel, ha a szállító PWP feltételeket tartalmaz, akkor ezek a feltételek a beszerzési rendelések (PO) soraiban jelennek meg. Ha PWP feltételeket tartalmazó PO-t szeretne létrehozni, hajtsa végre az alábbi lépéseket.

1. A Microsoft Dynamics 365 Finance alkalmazásban kövesse az alábbi lépéseket:

    - Nyissa meg a **Beszerzés** \> **Beszerzési rendelések** \> **Összes beszerzési rendelés** pontot. A Művelet panelen válassza a **Új** elemet. A **Beszerzési rendelés létrehozása** párbeszédpanelen jelölje ki azt a szállítót, akihez a projekten be vannak állítva a PWP feltételek, adja meg az egyéb szükséges adatokat, majd válassza az **OK** lehetőséget.
    - Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre. A Művelet panelen válassza a **Kezelés** lap **Cikkfeladat** elemét. Jelölje ki a beszerzési rendelést. Jelölje ki azt a szállítót, akihez a projekten be vannal állítva a PWP-feltételek, majd válassza az **OK** gombot.

2. A **Beszerzési rendelés** oldalon a **Beszerzésirendelés-sorok** gyorslapon válassza a **Sor hozzáadása** lehetőséget a megrendeléssor létrehozásához.
3. Válassza ki a cikkszámot vagy a beszerzési kategóriát, majd adja meg a többi kötelező adatot. Nézze át beszállítóhoz tartozó beszerzésirendelés-sor részleteit.

    A program automatikusan kijelöli a **Fizetés fizetéskor** funkciót, és a **PWP küszöb százalékos érték** mezőjében szereplő értéket a program automatikusan átmásolja a **projektek** lap **PWP küszöb százaléka** mezőjéből.

4. Ha nem szeretne PWP feltételeket alkalmazni a szállítóhoz egy PO-sorhoz, akkor törölje a **fizetés fizetéskor** jelölőnégyzetből. Ebben az esetben a rendszer a **PWP-küszöb százalékos értéke** mezőjét **0** (nulla) értékre állítja vissza a beszerzési rendeléshez.
5. A Műveleti ablaktáblán, a **Beszerzési rendelés** oldalon, a **Beszerzés** fülön kattintson a **Megerősítés** elemre a beszerzési rendelés megerősítéséhez.
6. A Műveletpanelen, a **Számla** lapon válassza a **Számla** lehetőséget a beszerzési rendeléshez tartozó számla létrehozásához.

## <a name="create-a-project-invoice-proposal"></a>Projektszámla-javaslat létrehozása

A projektszámla ajánlatok arra használhatók, hogy projektszámla ajánlatokat hozzanak létre az ügyfélnek. A PWP-forgatókönyv esetén a szállítók kifizetése az ügyfél fizetésétől függ a PWP-beállításoknak megfelelően. Vannak azonban lehetőségek arra, hogy anélkül is engedélyezze a kifizetést, hogy az ügyfél fizetne. A következő lépések végrehajtásával hozhatja létre a projektszámlát az ügyfélnek.

1. Az ügyfélkapcsolati alkalmazásokban válassza a **Projekt** \> **Projektek** lehetőséget majd válassza ki a projektet.
2. A **Tényadatok** lapon válassza ki azt a tényadatsort, amelyet a PO generált, és **Számlázatlan értékesítés** tranzakciótípusa van. Ezután válassza a **Számlázásra kész** lehetőséget.
3. Válassza az **Értékesítés** \> **Értékesítés** \> **Projektszerződés** lehetőséget, és jelölje ki a projektszerződést.
4. Az ügyfélszámla generálásához a műveleti ablaktáblán válassza a **Számla** lehetőséget.
5. A Finance-ben válassza a **Projektmenedzsment és könyvelés** \> **Időszakos** \> **Importálás előkészítő táblából** menüpontot, majd válassza az **OK** lehetőséget a Project Operations integrációs naplójának generálásához.
6. Nyissa meg a **Projektmenedzsment és a könyvelés** \> **Projektszámlák** \> **Projektszámla javaslat** menüpontot, majd válassza a **Feladás** lehetőséget a projekthez generált számlajavaslat feladásához.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ügyfélkifizetés frissítése és a szállító kifizetése

Ha egy szállító befejezi a munkát egy projekten, és számlát küld, akkor ellenőriznie kell a projekt állapotát és az ügyfelek számláit, hogy a PWP feltételei teljesültek-e a projekt esetében. Ha teljesülnek a szállító PWP feltételei, megadhatja, hogy a szállítói számla mely sorait kell kifizetni a projekt vevői kifizetései alapján. Ha úgy dönt, hogy kifizeti a szállítót annak ellenére, hogy a PWP feltételei nem teljesültek, akkor a PWP-feltételeket felülbírálhatja a **Szállítói számla fizetéskori fizetéssel** oldalon.

1. A Finance-ben válassza ki a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** lehetőséget, és válassza ki a projektet.
2. A műveleti ablaktáblán válassza a **Vezérlő** lehetőséget, majd válassza a **Szállítói számláik** elemet az összes a projekthez generált szállítói számla megjelenítéséhez.
3. A **Szállítói számla fizetéskori fizetéssel** oldalon a keresés mezőben adja meg az áttekinteni kívánt szállítói számla megkereséséhez használandó értékeket, majd kattintson a **Keresés** gombra.
4. Válassza a **Fizetés fizetéskor** lehetőséget, ha csak a PWP-számlákat szeretné megtekinteni.
5. A **Szállítói számlasorok** gyorslapon jelölje ki a sorokat, amelyekhez engedélyezni szeretné a kifizetést.
6. Válassza a **Szállítói kifizetés kiadása** lehetőséget. A **Fizetés fizetéskor** lehetőség törölve van, és a **Fizetésre kész** mező értéke **Igen** értékre változik.
