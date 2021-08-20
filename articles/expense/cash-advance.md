---
title: Készpénzelőleg
description: Ez a témakör a készpénzes előlegekről nyújt információkat.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988519"
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

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Válassza ki a költségelre vonatkozó készpénzelőlegeket
Költségjelentés elküldése előtt kiválaszthatja a jelentésben a költségtranzakciókhoz igazodó készpénzelőleget. A funkció használatához a következő két funkciót kell engedélyezni a **Szolgáltatáskezelés** munkaterületről:

  - Költségjelentések újragondolva
  - A készpénzelőlegek költségsorokba való leképezése
 
 Ha ezek a funkciók engedélyezve vannak:
 
  - Az egyes költségsorokhoz egy vagy több készpénzelőleget is hozzáadhat.
  - A készpénzelőleg rendelkezésre álló egyenlege valós időben látható a költségjelentés mentésekor. Ez lehetővé teszi a költségtranzakciók feldolgozását és a készpénztranzakció egyidőben való visszaküldését.
  - Az egyes költségtranzakciókhoz több készpénzelőleget is kiválaszthat.
  - A készpénzelőleg egyeztetési adatai lekérdezéssel érhetők el. 
 
Ha nem használja ezeket a funkciókat, a funkciók változatlanok maradnak, és a meglévő készpénzelőlegek automatikusan csökkennek a költség elküldését követően.

### <a name="example"></a>Példa 
Egy konferenciára utazik Seattle-ből New Yorkba. A konferenciával kapcsolatos becsült költségek – konferenciára szóló jegy, repjegyek, szállás, étkezések és taxi – összegéről, 3000,00 USD-ról létrehoz egy készpénzelőleg kérelmet. Ön csak akkor kapja meg ezt az összeget, ha a vezető jóváhagyja a kérelmet. Miután a vezető jóváhagyta, a kért készpénzelőleg a bankszámlájára 3000.00 USD formájában kerül kifizetésre. Ezután részt vesz a konferencián. Az utazás befejezése után megállapíthatja, hogy a teljes kiadás csak 2790,00 USD volt. Válassza a **Készpénz** lehetőséget a **Fizetési mód** mezőben, és küldje el a 2790,00 USD költségeiről szóló kérelmet. A rendszer automatikusan helyesbíti a beküldött kiadások összegét az Önnek kölcsönadott 3000,00 USD készpénzelőleg alapján. Mindössze 210,00 USD összeggel (3000,00-2790,00) tartozik a vállalatnak, ezt a **Készpénz visszautalása** költségkategória használatával tudja visszautalni.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
