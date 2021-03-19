---
title: Időzónák kezelése
description: A projekt létrehozásakor az időzónája a munkaidősablonban megadott időzónán alapul.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279546"
---
# <a name="manage-time-zones"></a>Időzónák kezelése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


## <a name="projects"></a>Projektek

A projekt létrehozásakor az időzónája az alkalmazott munkaidősablonban megadott időzónán alapul. A **Projekt** esetében a dátumok mindig az egyes lapokon bejelentkezett felhasználó időzónájához viszonyítva jelennek meg, kivéve a **Feladat** lapot. Ha megtekinti a munkalebontási struktúrát, akkor a dátumok mindig a projekt időzónájában jelennek meg.

## <a name="tasks"></a>Tevékenységek

A feladat létrehozásakor a kezdő időt, a záró időt és az órát/napot a projekt munkaideje szabályozza. Ha például egy feladat egy olyan projekttel jön létre, amelynek időzónája -8 PST, és a következő munkaidővel rendelkezik: 9:00 – 17:00, hétfőtől péntekig, a hozzárendelés nélkül létrehozott bármely feladat tiszteletben tartja a projektnaptár kezdő időpontját és befejező időpontját.

## <a name="manage-resources-with-time-zones"></a>Erőforrások kezelése időzónákkal

A **Foglalás kiterjesztése** funkció használatakor a pontos és kiszámítható eredmény érdekében két alapvető követelménynek kell teljesülnie:  

- A felhasználónak konfigurálnia kell az eszköz időzónáját, hogy az megfeleljen a rendszer **Személyre szabási beállítások** részében megadott időzónának.
 
  ![Időzóna-beállítások a Windows 10 rendszerben](media/reconcile-assignments-03.png)

  ![Időzóna-beállítások a testreszabási beállításokban](media/reconcile-assignments-04.png)
 
- A foglalható erőforrásnak legalább egy perc munkaidővel kell rendelkeznie, amely átfedésben van az elosztásokkal, amelyeket a kért hosszabbítás definiálásához használnak. A következő erőforrások például 9:00 és 19:00 óra közötti munkaórákkal rendelkeznek. 

  ![Az erőforrás-eloszlások összehasonlítása](media/reconcile-assignments-05.png)

Az alábbi táblában a következők láthatók:

- Egy projektnaptársablon
- A erőforrás: Ennek az erőforrásnak ugyanaz a naptára, és ugyanabban az időzónában van, mint a projekt. A foglalások kezdő időpontja 9:00 lesz.
- B erőforrás: Ez az erőforrás a projekttől eltérő időzónában helyezkedik el, és 7:00 órakor kezdőd az időzónájában. A foglalások azonban 9:00 órakor kezdődnek, mert ez a hozzárendelési felosztás legkorábbi kezdési időpontja.
- C és D erőforrások: Az erőforrások különböző időzónákban találhatók, mindkettő eltér egymástól és a projektétől, és a foglalásuk a rendelkezésre álló kezdő időpontokhoz képest nem korábban kezdődik.

|Entitás  |Naptár  |
|-|-|
|Projektnaptár-sablon   | ![projektnaptár](media/reconcile-assignments-06.png) |
|A erőforrás  | ![A erőforrás naptárja](media/reconcile-assignments-06.png) |
|B erőforrás  |  ![B erőforrás naptárja](media/reconcile-assignments-07.png) |
|C erőforrás  |  ![C erőforrás naptárja](media/reconcile-assignments-08.png) |
|D erőforrás  | ![D erőforrás naptárja](media/reconcile-assignments-09.png)  |
 
Amikor megnyitja az **Egyeztetés** nézetet, az erőforrás-hozzárendelések és a hozzájuk tartozó foglalási hiány jelenik meg.

![Egyeztetési nézet a bővítés előtt](media/reconcile-assignments-10.png)

Miután minden erőforráshoz kiterjeszti a foglalási funkciót, a rendszer sikeresen kiterjeszti a foglalásokat az egyes erőforrások esetében, mivel az egyes erőforrások munkaideje átfedésben van a hiány kontúrjaival.

![Egyeztetési nézet a foglalás meghosszabbítása után](media/reconcile-assignments-11.png) 

Figyelje meg, hogy a foglalások részletes vizsgálata a foglalások kezdő időpontjában jelentkező különbségeket mutatja. A foglalások legkorábban a hozzárendelési kontúrok kezdési időpontjában jelennek meg, és legkorábban az erőforrás rendelkezésre álló kezdési időpontjában.

![Erőforrások új foglalásai az ütemezési táblában](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]