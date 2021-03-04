---
title: Készpénzelőleg
description: Ez a témakör a készpénzes előlegekről nyújt információkat.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098887"
---
# <a name="cash-advance"></a>Készpénzelőleg

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A készpénzes előleg lehetővé teszi, hogy az alkalmazottak pénzt kölcsönözzenek a vállalattól a kiadások felmerülése előtt. A kért készpénzelőleg jóváhagyása és kifizetése esetén az alkalmazott a pénzösszeget felhasználhatja az esetlegesen felmerülő üzleti költségekre. 

## <a name="create-and-submit-a-cash-advance-request"></a>Készpénzelőleg-igénylés létrehozása és küldése
Új készpénzelőleg létrehozásához és készpénzelőleg kérelem benyújtásához tegye a következőket: 

1. A **Saját kiadások** alatt válassza a **Készpénzelőleg** > **Új** lehetőséget. 
2. Az **Új készpénzelőleg kérése** oldalon adja meg a kiadás célját, és válassza ki, hogy a költség hol fog felmerülni.
3. Adja meg a kért összeget és pénznemet, majd kattintson a **Mentés** gombra. 
4. Amikor készen áll a készpénzelőleg-igénylés elküldésére, a **Készpénzelőleg-igénylés** oldalon válassza a **Munkafolyamat** > **Küldés** lehetőséget.

## <a name="modify-a-cash-advance-request"></a>Készpénzelőleg-igénylés módosítása

A készpénzelőleg-igénylések akkor módosíthatók, ha még nincsenek elküldve jóváhagyásra.

1. Keresse meg és jelölje ki a szerkeszteni kívánt készpénzelőleget a **Saját kiadások: Készpénzelőleg** lehetőség alatt.
2. Válassza a **Szerkesztés** lehetőséget, és hajtsa végre a szükséges módosításokat a készpénzelőleg-igénylésben. 
3. Válassza a **Mentés és bezárás** lehetőséget.


## <a name="view-cash-advance-requests"></a>Készpénzelőleg-kérések megtekintése
Áttekintheti az összes olyan készpénzelőleg listáját, amely vázlat, beküldött, áttekintés alatt vagy fizetett állapotban van a **Saját kiadások: Készpénzelőlegek** alatt. 

## <a name="approve-cash-advance-requests"></a>Készpénzelőleg-kérések jóváhagyása

A munkafolyamatban jóváhagyóként konfigurált vezetők vagy felhasználók jóváhagyhatják a hozzájuk áttekintésre beküldött készpénzelőlegeket. 

1. A készpénzelőleg jóváhagyásához a **Készpénzelőlegek feldolgozása** területen jelölje ki a **Készpénzelőlegek saját áttekintésre** lehetőséget.
2. Válassza ki az áttekinteni kívánt készpénzelőleget, és válassza a **Jóváhagyás** lehetőséget.  

## <a name="pay-cash-advances"></a>Készpénzelőlegek kifizetése 
A következő eljárást általában egy könyvelő vagy egy könyvelési engedéllyel rendelkező felhasználó végzi el.

1. A jóváhagyott készpénzelőlegek könyveléséhez válassza a **Jóváhagyott készpénzelőlegek** lehetőséget, majd válassza a **Fizetés és átutalás** lehetőséget.  
2. Adja meg a naplóadatokat a készpénzelőlegekhez, majd kattintson az **OK** gombra. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Költségjelentés küldése a kifizetett készpénzelőleghez 

A már kapott készpénzelőleg költségjelentésének létrehozásakor és elküldésekor a kiadások automatikusan az előleghez igazítják. Ha a készpénzelőleg nagyobb, mint a kiadott összeg, akkor az egyenleget vissza kell juttatnia a vállalathoz a **Készpénz visszaadása** költségkategória használatával. Ha a vállalat által kifizetett készpénzelőleg kevesebb, mint a korábban kifizetett összeg, a vállalatnak vissza kell fizetnie Önnek az egyenleget. 

### <a name="example"></a>Példa
Egy konferenciára utazik Seattle-ből New Yorkba. A konferenciával kapcsolatos becsült költségek – konferenciára szóló jegy, repjegyek, szállás, étkezések és taxi – összegéről, 3000,00 USD-ról létrehoz egy készpénzelőleg kérelmet. Ön csak akkor kapja meg ezt az összeget, ha a vezető jóváhagyja a kérelmet. Miután a vezető jóváhagyta, a kért készpénzelőleg a bankszámlájára 3000.00 USD formájában kerül kifizetésre. Ezután részt vesz a konferencián. Az utazás befejezése után megállapíthatja, hogy a teljes kiadás csak 2790,00 USD volt. Válassza a **Készpénz** lehetőséget a **Fizetési mód** mezőben, és küldje el a 2790,00 USD költségeiről szóló kérelmet. A rendszer automatikusan helyesbíti a beküldött kiadások összegét az Önnek kölcsönadott 3000,00 USD készpénzelőleg alapján. Mindössze 210,00 USD összeggel (3000,00-2790,00) tartozik a vállalatnak, ezt a **Készpénz visszautalása** költségkategória használatával tudja visszautalni.



[!INCLUDE[footer-include](../includes/footer-banner.md)]