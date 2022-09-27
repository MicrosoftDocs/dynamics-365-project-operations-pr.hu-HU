---
title: Fizetés a szállítói kifizetések kifizetése esetén
description: Ez a témakör elmagyarázza, hogyan kell használni a fizetés fizetése fizetéskor (PWP) forgatókönyvet.
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
# <a name="pay-when-paid-vendor-payments"></a>Fizetés a szállítói kifizetések kifizetése esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör elmagyarázza, hogyan kell használni a fizetés fizetése fizetéskor (PWP) forgatókönyvet.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>PwP-feltételekkel rendelkező beszerzési rendelés létrehozása

Amikor számlát ad fel egy szállítótól, ha a szállítóra PWP-feltételek vonatkoznak, ezek a feltételek megjelennek a beszerzési rendelés (PO) soraiban. Ha PWP feltételeket tartalmazó PO-t szeretne létrehozni, hajtsa végre az alábbi lépéseket.

1. A Microsoft Dynamics 365 Finance alkalmazásban kövesse az alábbi lépések egyikét:

    - Nyissa meg a **Beszerzés** \> **Beszerzési rendelések** \> **Összes beszerzési rendelés** pontot. A Művelet panelen válassza a **Új** elemet. **A Beszerzési rendelés** létrehozása párbeszédpanelen válassza ki azt a szállítót, amelyhez a PWP-feltételek be vannak állítva a projekthez, adja meg az egyéb szükséges adatokat, majd kattintson **az OK gombra**.
    - Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre. A műveleti ablaktábla Kezelés **lapján válassza az** Elemfeladat **lehetőséget**. Válassza ki a beszerzési rendelést. Válassza ki azt a szállítót, amelyhez a PWP-feltételek be vannak állítva a projekthez, majd kattintson **az OK gombra**.

2. **A Beszerzési rendelés** lap Beszerzési rendelés sorainak **gyors lapján válassza a** Sor **hozzáadása lehetőséget** egy beszerzésirendelés-sor létrehozásához.
3. Válassza ki a cikkszámot vagy a beszerzési kategóriát, és adja meg a többi szükséges adatot. Tekintse át a szállító beszerzési rendelési sorának részleteit.

    A program automatikusan kijelöli a **Fizetés fizetéskor** funkciót, és a **PWP küszöb százalékos érték** mezőjében szereplő értéket a program automatikusan átmásolja a **projektek** lap **PWP küszöb százaléka** mezőjéből.

4. Ha nem szeretne PWP feltételeket alkalmazni a szállítóhoz egy PO-sorhoz, akkor törölje a **fizetés fizetéskor** jelölőnégyzetből. Ebben az esetben a **beszerzési rendelési sor PWP-küszöbérték százalékos** mezője visszaáll 0-ra **·**(nulla).
5. **A Beszerzési rendelés** lap Műveleti ablaktábláján, a Vásárlás **lapon válassza a** Megerősítés **lehetőséget** a beszerzési rendelés megerősítéséhez.
6. A Műveleti ablaktábla Számla **lapján válassza a** Számla **lehetőséget** a beszerzési rendelés számlájának létrehozásához.

## <a name="create-a-project-invoice-proposal"></a>Projektszámla-javaslat létrehozása

A projektszámla-javaslatok a vevő projektszámláinak létrehozására szolgálnak. A PWP-forgatókönyvben a szállítói kifizetések a PWP-beállításoknak megfelelő vevői kifizetésektől függenek. Vannak azonban olyan lehetőségek, amelyek lehetővé teszik a kifizetések felszabadítását anélkül, hogy a kifizetéseket az ügyfelek fizetése nélkül kellene. Ha projektszámlát szeretne létrehozni a vevő számára, kövesse az alábbi lépéseket.

1. Az ügyfélkapcsolati alkalmazásokban lépjen a Project Projects (Projektprojektek **·**\>)**lapra**, és válassza ki a projektet.
2. **A Tényleges adatok** lapon válassza ki azt a tényleges sort, amelyet a Nem számlázott értékesítési **tranzakciótípussal rendelkező** beszerzési rendelés generál. Ezután válassza a Készen áll a számlára **lehetőséget**.
3. Lépjen az **Értékesítési** \> **értékesítési** \> **projekt szerződése elemre**, és válassza ki a projektszerződést.
4. A Műveleti ablaktáblán válassza a Számla **lehetőséget** a vevői számla létrehozásához.
5. A Finance (Pénzügyek) területen lépjen a **Projektvezetés és könyvelés** \> **időszakos importálás szakaszos** \> **importálás átmeneti táblázatból** elemre, és kattintson **az OK gombra** a Projektműveletek integrációs naplójának létrehozásához.
6. Lépjen a Projektvezetési és **könyvelési**\> projektszámlák **·**\> Projektszámla-javaslat **elemre**, és válassza a Feladás **lehetőséget** a projekthez létrehozott számlajavaslat feladásához.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Ügyfélkifizetés frissítése és a szállító kifizetése

Amikor egy szállító befejezi a projektet, és számlát küld Önnek, át kell tekintenie a projekt állapotát és a vevői számlákat annak megállapításához, hogy teljesültek-e a pwp-feltételek a projekt esetében. Ha teljesülnek a szállító PWP feltételei, megadhatja, hogy a szállítói számla mely sorait kell kifizetni a projekt vevői kifizetései alapján. Ha úgy dönt, hogy kifizeti a szállítót annak ellenére, hogy a PWP feltételei nem teljesültek, akkor a PWP-feltételeket felülbírálhatja a **Szállítói számla fizetéskori fizetéssel** oldalon.

1. A Pénzügyek területen lépjen a Projektvezetési és **könyvelési**\> projektek **·**\> Minden projekt **elemre**, és válassza ki a projektet.
2. A Műveleti ablaktáblán válassza **a Vezérlés**, majd a Szállítói számlák **lehetőséget** a projekthez létrehozott összes szállítói számla megjelenítéséhez.
3. A **Szállítói számla fizetéskori fizetéssel** oldalon a keresés mezőben adja meg az áttekinteni kívánt szállítói számla megkereséséhez használandó értékeket, majd kattintson a **Keresés** gombra.
4. Válassza a **Fizetés fizetéskor** lehetőséget, ha csak a PWP-számlákat szeretné megtekinteni.
5. **A Szállítói számlasorok** Gyors lapján válassza ki azokat a sorokat, amelyeket fel szeretne szabadítani fizetésre.
6. Válassza a Szállítói kifizetés **felszabadítása lehetőséget**. A **Fizetés fizetéskor** lehetőség törölve van, és a **Fizetésre kész** mező értéke **Igen** értékre változik.
