---
title: Áfa-visszaigénylés a Költségkezelésben
description: Ez a témakör ismerteti, hogyan fogadhatók visszatérítések a jogosult ÁFA-tranzakciókra vonatkozóan.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908232"
---
# <a name="vat-recovery-in-expense-management"></a>Áfa-visszaigénylés a Költségkezelésben

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ahhoz, hogy visszatérítést kapjon a jogosult ÁFA-tranzakciókból, egy vállalatnak vagy szervezetnek pontos információkat kell azonosítania, összegyűjtenie, ellenőriznie és benyújtania. Ez a folyamat több feladatot is tartalmaz, és a vállalat méretétől függően több alkalmazottat vagy szerepkört is tartalmazhat.

Az ÁFA-visszaigényléshez a **Költségkezelés** modulban a következő előfeltételeket kell teljesíteni:

- A kiadási kategóriákhoz rendelt országok/régiók számára adókódokat kell létrehozni.
- Minden egyes adókód esetében létre kell hozni egy áfacsoportot.
- Minden egyes áfacsoport esetében létre kell hozni egy cikkáfakódot.

Az előfeltételek teljesítését követően a következő lépéseket kell végrehajtani az ÁFA-tranzakciókhoz tartozó visszatérítések igényléséhez.

1. A költségjelentésen a jogosult ÁFA-visszatérítések azonosításához adja meg a hitelkártya-tranzakciókra vonatkozó adózási adatokat.
2. Ellenőrizze, hogy az összes adózási információ teljes-e, majd küldje el a költségjelentést.
3. Dolgozza fel a nemzetközi HÉA-visszaigénylésre jogosult kiadásokat.
4. ÁFA-visszaigénylési adatok küldése a harmadik félnek a nemzetközi visszaigénylés benyújtásához.
5. Dolgozza fel a belföldi ÁFA-visszaigénylésre jogosult kiadásokat.

Az alábbi szakaszok olyan példákat tartalmaznak, amelyek bemutatják, hogyan hajtják végre a Contoso alkalmazottai az egyes lépéseket.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>A jogosult ÁFA-visszatérítések azonosításához adja meg a hitelkártya-tranzakciókra vonatkozó adózási adatokat

Nancy, a Contoso Egyesült Államokban tevékenykedő értékesítési képviselője a közelmúltban tért vissza egy értékesítési útról az Egyesült Királyságból. Az utazás során Nancy néhány személyes hitelkártyaköltést számolt fel az étkezésekre. Nancynek most létre kell hoznia egy költségjelentést a kiadások egyeztetéséhez.

Amikor Nancy beírja a költségjelentés adatait, az **Egyesült Királyság** lehetőséget választja ki az **Ország/régió** mezőben a **Költségjelentés szerkesztése** lapon. Ekkor a rendszer szűri az áfacsoportok listáját, hogy csak az Egyesült Királyságra érvényes csoportokat jelenítse meg. Nancy kijelöli az **Egyesült Királyság 001** áfacsoportot, majd kiválasztja az **Étkezések** cikkáfacsoportot. A következő lépésként Nancy hozzáad egy új tranzakciót a szállás esetében. Mivel az Egyesült Királyságban csak egy áfacsoport és egy cikkáfacsoport van, a rendszer ezeket az adatokat automatikusan kitölti Nancy költségjelentésében.

A Contoso irányelvei szerint minden költségnek megfelelő bizonylattal kell rendelkeznie. Ezért amikor Nancy menti a költségjelentést, egy üzenetet kap, amely értesíti arról, hogy a költségjelentésében szereplő minden tranzakcióhoz bizonylatot kell csatolni. Nancy ellenőrzi, hogy minden tranzakciós bizonylat digitális képét csatolta a költségjelentéshez, majd jóváhagyás céljából benyújtja a jelentést. Ezután elküldi a papíralapú bizonylatokat az irodai feldolgozócsapatnak. Ez a csoport elküldi az ÁFA-visszaigénylési adatokat a harmadik félnek, aki nemzetközi ÁFA-visszaigénylést nyújt be a Contoso részére.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Az adózási információk ellenőrzése és a költségjelentés feladása

Mielőtt April, a Contoso Kötelezettségek-koordinátora egy költségjelentést nyújthatna be, meg kell adnia minden hiányzó adózási információt. Megnyitja a **Költségjelentés részletei** oldalt, és látja, hogy Nancy jóváhagyta a költségjelentést. April ezután megnyitja a költségjelentést a tranzakciók részleteinek megtekintéséhez. Látja, hogy Nancy nem adott meg egy cikkáfacsoportot az egyik tranzakcióhoz. Mivel ezek az információk nincsenek megadva, a költségjelentés nem könyvelhető. Ezért a Költségkezelés lapon megkeresi az **Adókonfigurációk** oldalt, és megkeresi az országhoz/régióhoz tartozó megfelelő cikkáfacsoport és a tranzakciótípus értékét. April most már könyvelheti a költségjelentés a főkönyvbe.

Amikor April feladja a költségjelentést, a rendszer létrehozza a visszaigényelhető áfájú munkatételt. Ezt a munkaelemet a rendszer az irodai feldolgozócsoport valamelyik tagjához rendeli hozzá. April egy olyan üzenetet kap, amely igazolja a feladás sikerességét. Ez az üzenet felsorolja a visszaigénylésre azonosított ÁFA-tranzakciók számát is.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>A nemzetközi ÁFA-visszaigénylésre jogosult kiadások feldolgozása

Arnie, a Contoso irodai feldolgozócsoportjának tagja felelős annak ellenőrzéséért, hogy az ÁFA-visszaigényléshez szükséges összes információt tartalmazza-e a költségjelentés. Megnyitja a **Költségadó-visszaigénylés** oldalt, és kijelöli a Nancy által beküldött költségjelentést. Arnie ezután ellenőrzi, hogy az összes szükséges bizonylat csatolva van-e, és hogy a megfelelő áfacsoport és cikkáfakódok lettek-e megadva.

Amikor Arnie megkapja a papíralapú bizonylatokat Nancytől, ellenőrzi azokat a digitális bizonylatokkal összevetve, majd a költségjelentés állapotát a **Visszaigénylésre kész** értékre módosítja.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>ÁFA-visszaigénylési adatok küldése a harmadik félnek

Amikor Arnie készen áll arra, hogy elküldje a költségjelentés adatait a harmadik félnek, amely az ÁFA-visszaigénylést benyújtja, megnyitja a **Költségadó-visszaigénylés** oldalt. Az oldalt úgy szűri, hogy csak azokat a költségjelentéseket jelenítse meg, amelyek **Visszaigénylésre kész** jelzéssel rendelkeznek. Arnie ezután kiválasztja a **Fájl** &gt; **Exportálás Excelbe** lehetőséget. Az ÁFA-adatok a költségjelentésből egy Microsoft Excel munkalapra kerülnek exportálásra. Arnie elküldi ezt a munkalapot a harmadik félnek, és egy olyan üzenetet mellékel, amely tájékoztat arról, hogy a papíralapú bizonylatok futár útján kerülnek elküldésre.

## <a name="process-expenses-for-domestic-vat-recovery"></a>A belföldi ÁFA-visszaigénylésre jogosult kiadások feldolgozása

Arnie-nak ellenőriznie kell, hogy a költségjelentés tranzakciói jogosultak-e az ÁFA-visszaigénylésre, és hogy a digitális bizonylatok csatolva vannak-e a jelentésekhez. A belföldi visszaigénylésre jogosult kiadások feldolgozásának megkezdéséhez Anna megnyitja a **Költségadó-visszaigénylés** oldalt, és kiválasztja az ellenőrzést igénylő költségjelentést. Ellenőrzi, hogy a nyugták a vállalat nevére, és nem az alkalmazott nevére lettek kiállítva. (ÁFA-visszaigényléshez a bizonylatoknak a vállalat nevére kell szólniuk.) Arnie ezután ellenőrzi, hogy az összes szükséges bizonylat csatolva van-e, és hogy a megfelelő áfacsoport és cikkáfakódok lettek-e megadva.

Amikor Arnie megkapja a papíralapú bizonylatokat, a költségjelentést **Visszaigénylésre kész** állapotba állítja. Ezután benyújthatja a visszaigénylést a megfelelő adóhatósághoz. Ebben az esetben a megfelelő adóhatóság az Egyesült Államokban az Internal Revenue Service (IRS).
