---
title: Készpénzelőleg
description: Ez a témakör a készpénzes előlegekről nyújt információkat.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077975"
---
# <a name="cash-advance"></a>Készpénzelőleg

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A készpénzes előleg lehetővé teszi, hogy az alkalmazottak pénzt kölcsönözzenek a vállalattól a kiadások felmerülése előtt. A kért készpénzelőleg jóváhagyása és kifizetése esetén az alkalmazott a pénzösszeget felhasználhatja az esetlegesen felmerülő üzleti költségekre. 

## <a name="create-and-submit-a-cash-advance-request"></a>Készpénzelőleg-igénylés létrehozása és küldése

1. A **Saját kiadások** területen válassza a **Készpénzelőleg** > **Új** lehetőséget új készpénzelőleg létrehozásához. 
2. Az **Új készpénzelőleg kérése** oldalon adja meg a kiadás célját, és válassza ki, hogy a költség hol fog felmerülni.
3. Adja meg a kért összeget és pénznemet, majd kattintson a **Mentés** gombra. 
4. Amikor készen áll a készpénzelőleg-igénylés elküldésére, a **Készpénzelőleg-igénylés** oldalon válassza a **Munkafolyamat** > **Küldés** lehetőséget.

## <a name="modify-a-cash-advance-request"></a>Készpénzelőleg-igénylés módosítása

A készpénzelőleg-igénylések akkor módosíthatók, ha még nincsenek elküldve jóváhagyásra.

1. A **Saját kiadások: Készpénzelőleg** területen keresse meg és jelölje ki a módosítani kívánt készpénzelőleget.
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

Ha a már megkapott készpénzelőleghez költségjelentést hoz létre és küld el, a rendszer automatikusan helyesbíti a költségeket az adott előleghez képest. Ha a készpénzelőleg nagyobb, mint a kiadott összeg, akkor az egyenleget vissza kell juttatnia a vállalathoz a **Készpénz visszaadása** költségkategória használatával. Ha a vállalat által fizetett készpénzelőleg kisebb, mint a kiadott összeg, a vállalatnak meg kell térítenie a különbözetet. 

### <a name="example"></a>Példa
Seattle-ből New York városába szeretne utazni egy konferenciára. 3000,00 USD összegű készpénzelőleg-igénylést hoz létre, mivel úgy becsülte, hogy a konferenciajegy, a repülőjáratok, a szálloda, az étkezés és a taxi költsége nagyjából ezt az összeget teszi ki. Csak akkor kapja meg a kifizetést, ha a vezetője jóváhagyta ezt a kérést. Miután a vezető jóváhagyta, a kért készpénzelőleg a bankszámlájára 3000.00 USD formájában kerül kifizetésre. Ezután részt vesz a konferencián. Az utazás befejezése után megállapíthatja, hogy a teljes kiadás csak 2790,00 USD volt. Válassza a **Készpénz** lehetőséget a **Fizetési mód** mezőben, és küldje el a 2790,00 USD-t kitevő kiadásait. A rendszer automatikusan helyesbíti a beküldött kiadások összegét az Önnek kölcsönadott 3000,00 USD készpénzelőleg alapján. Így a vállalat felé fennálló tartozásának egyenlege 210,00 USD (3000,00-2790,00), amelyet a **Készpénz visszaadása** költségkategória használatával vissza tud adni a vállalatnak. 
