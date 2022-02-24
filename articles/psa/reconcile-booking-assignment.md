---
title: Összehangolja a foglalásokat és a feladatokat
description: Ez a témakör az aktuális tényezőkről nyújt információkat.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147926"
---
# <a name="reconcile-bookings-and-assignments"></a>Összehangolja a foglalásokat és a feladatokat

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projektcsoport tagjainak projektfoglalása és a projektfeladatok lazán kapcsolódnak egymáshoz. Ezért egy erőforrásnak lehet olyan feladat-hozzárendelése, amely nem felel meg a foglalásoknak, és olyan foglalások, amelyek nem felelnek meg a feladat-hozzárendeléseknek. Ideális esetben a projektfoglalások és a feladatok összehangolva vannak, így az erőforrások képesek voltak feladataik elvégzésére. A valóság azonban az, hogy a foglalások rendelkezésre állásuk alapján történhetnek, és a feladatok ütemezése megváltozhat, amikor a projekt folytatja az életciklusát. Ezért a laza csatlakozás rugalmasságot tesz lehetővé.

A projektfoglalások és a feladatkiosztások laza csatolása miatt az **Összehangolás** lap szerepel a Projekt entitásban. Ez a lap segít a projektmenedzsereknek összeegyeztetni a csapattagok foglalásait és feladataikat a projektcsapatuk számára.

Az **Összehangolás** lapon minden megnevezett csapattag számára a foglalások és az egyes feladatokhoz rendelt hozzárendelések jelennek meg. Órákat mutat a cellákban, amelyek hónapoktól napokig tartó időszakokat reprezentálhatnak.

Az **Időkeret** mezőben kiválaszthatja a **Hó**, **Hét** vagy **Nap** lehetőséget. Alapértelmezésben a **Hét** kiválasztva. Az alapértelmezett értéket azonban a **Beállítások** gomb megnyomásával módosíthatja. Amikor megnyitja az **Összehangolás** fület, megjeleníti az aktuális dátumot, de a naptárvezérlővel előre vagy hátra mozoghat. Ha egy projektnek a jövőbeni kezdő dátuma van, akkor a fül megjeleníti azt a dátumot, amikor megnyitja. A naptárvezérlőnek olyan opciói is vannak, amelyek lehetővé teszik a projekt kezdő és befejező dátumára való áttérést.

Az egyes erőforrások kibővítő vezérlőkkel megjelenítheti az erőforrás foglalásainak részleteit. Az egyes erőforrások hozzárendeléseit az egyes feladatok szintjére is kibővítheti.

Az **Összeegyeztetés** lap alján látható a projekt teljes nettó összértéke, és a fül egy teljes oszlopot is tartalmaz. Mindegyik erőforrás esetében a lap figyelembe veszi a különbséget a csapattag projektenkénti foglalása és a csapattag feladatainak összerakása között. Ideális esetben a különbség 0 (nulla) legyen. Más szavakkal, nem szabad különbséget tenni az erőforrás foglalása és a feladat-hozzárendelés között. Az esetleges különbségeket a szín és az árnyékolás jelöli, hogy két feltételre hivatkozzon:

- **Foglaláshiány** - A foglaláshiány akkor fordul elő, ha egy erőforráshoz több hozzárendelés tartozik, mint foglalásokhoz. Mivel ez a kapacitás nem volt fenntartva, a projektmenedzser javíthatja ezt a feltételt az erőforrás foglalásainak kiterjesztésével, hogy fedezze a hiányt.
- **Többletfoglalások** - Többletfoglalások akkor fordulnak elő, amikor egy erőforrást lefoglaltak a projekthez, de nem rendeltek hozzá feladatokhoz. Ez a feltétel elfogadható lehet, ha például az erőforrást a feladat-hozzárendelés megtörténte előtt lefoglalták. Más esetekben azonban előfordulhat, hogy az erőforrás nem rendelhető hozzá. Ezekben az esetekben a projektmenedzsernek fontolóra kell vennie az erőforrás foglalásainak visszavonását, hogy a kapacitás felhasználható legyen egy másik projekthez.

> [!NOTE]
> Lehet, hogy ezeknek a feltételeknek a legendája rejtett, hogy több hely maradjon a rács számára. Ebben az esetben a jelmagyarázat láthatóvá **Beállítások** gomb megnyomásával.

Bizonyos esetekben, ha az **Időskála** mezőt olyan értékre állítja, amely magasabb, mint a **Nap**, a különbségeket 0 (nulla) értékre lehet számítani. Például **Hónap** szinten az erőforrás nettó különbsége lehet 0 (nulla), jelezve, hogy a foglalások azonosak a hozzárendelésekkel. Ha azonban a **Hét** szintre nézzük, akkor láthatjuk, hogy a hónap első hetében 0 (nulla) óra foglalást és 40 órás foglalást, 40 órát és 0 (nulla) foglalást végeznek óra a hónap második hetében. Noha a hónap összes foglalása és megbízása egyenlő, hetenként különböznek.

A magasabb időszint megtekintésekor az **Összehangolás** lapon megjelenik egy cellaindikátor, amely értesíti Önt, hogy alacsonyabb időszinteken vannak különbségek. Például a következő ábrán egy cellát jelző jelenik meg a cellában 2018. októberi hónapban az erőforrásnak, amelynek neve Katelyn Merritt. Ezért láthatja, hogy annak ellenére, hogy az erőforrás könyvelése és hozzárendelése egyenlő, ha **Hónap** szinten aggregálják, az alacsonyabb szinteken nem egyeznek.

![Nem egyező lefoglalások és hozzárendelések a havi szinten](media/reconcile-assignments-01.JPG)

Kattintson duplán a cellára a következő alsó szintre való nagyításhoz és a különbség megtekintéséhez. Például, ha duplán kattint a Katelyn Merritt 2018. októberi különbségére, akkor a **Hét** szintre fúródik le. Ezután láthatja, hogy az erőforrás 16 órás foglalással rendelkezik, de október első két hetében nem rendelkezik hozzárendeléssel, és október harmadik hetében 16 órás foglalkozással rendelkezik, de nem foglal le.

![Nem egyező lefoglalások és hozzárendelések a heti szinten](media/reconcile-assignments-02.JPG)

Kattintson a jobb gombbal egy cellára, hogy kicsinyítse a következő magasabb szintet. A cella jelzőjét a **Beállítások** gomb megnyomásával is kikapcsolhatja. 

A rács feletti **Előző** és **Következő** gombokat a projekt bármilyen különbségének átlépésére is felhasználhatja. E gombok használatához először ki kell választania egy erőforrást. Válassza a **Következő** menüpontot a következő különbség eléréséhez az erőforrás foglalásainak és hozzárendelései között. Az előző különbség eléréséhez válassza az **Előző** lehetőséget.

Olyan helyzetekben, amikor erőforrás-feladatokat rendel, de nincs foglalása, kiválaszthatja a foglalási hiányt, majd a **Foglalás kiterjesztése** lehetőséget. Ezután láthatja a szükséges foglalást az erőforrás hiányának kiküszöböléséhez. Megtekintheti az erőforrás jelenlegi és más projektekre vonatkozó foglalásait is. Válassza az **OK** lehetőséget az erőforrás foglalásának az aktuális elérhetőség figyelembevétele nélkül történő létrehozásához. A projektmenedzser vagy az erőforrás-kezelő ezt követően felhasználhatja az Ütemezési táblát olyan helyzetek kezelésére, amikor egy erőforrás kapacitáson túl van túlfoglalva, mert a megrendelései meghosszabbodtak.

## <a name="managing-with-time-zones"></a>Kezelés időzónákkal
A Foglalás meghosszabbítása használatakor pontos és kiszámítható eredmények biztosítása érdekében két alapvető követelménynek kell teljesülnie:  

- A felhasználónak konfigurálnia kell az eszköze időzónáját, hogy az megfeleljen a rendszer Testreszabási beállításaiban megadott időzónának.
 
  ![Időzóna-beállítások a Windows 10 rendszerben](media/reconcile-assignments-03.png)

  ![Időzóna-beállítások a testreszabási beállításokban](media/reconcile-assignments-04.png)
 
- A foglalt erőforrásnak legalább egy perc munkaidővel kell rendelkeznie, amely átfedésben van az elosztásokkal, amelyeket a kért hosszabbítás definiálásához használnak. Például a következő példa áttekintett erőforrásokat mutat be, amelyek munkaórái 09:00 és 19:00 közé esnek. 

  ![Az erőforrás-eloszlások összehasonlítása](media/reconcile-assignments-05.png)

Az alábbi táblában a következők láthatók:

- Egy projektnaptár-sablon.
- A erőforrás: Ennek az erőforrásnak ugyanaz a naptára, és ugyanabban az időzónában van, mint a projekt. A foglalások kezdő időpontja 9:00 lesz.
- B erőforrás: Ez az erőforrás a projekttől eltérő időzónában van, ezért a 7:00-kor kezd az ő időzónája szerint. A foglalások azonban 9:00 órakor kezdődnek, mert ez a hozzárendelési felosztás legkorábbi kezdési időpontja.
- C és D erőforrások: Az erőforrások a különböző időzónákban találhatók mindkettő eltér egymástól és a projekttől is, és a foglalásuk nem kezdődik előbb, mint a hozzájuk tartozó elérhető kezdési idő.

|Entitás  |Naptár  |
|-|-|
|Projektnaptár-sablon   | ![projektnaptár](media/reconcile-assignments-06.png) |
|A erőforrás  | ![A erőforrás naptárja](media/reconcile-assignments-06.png) |
|B erőforrás  |  ![B erőforrás naptárja](media/reconcile-assignments-07.png) |
|C erőforrás  |  ![C erőforrás naptárja](media/reconcile-assignments-08.png) |
|D erőforrás  | ![D erőforrás naptárja](media/reconcile-assignments-09.png)  |
 
Az egyeztetési nézetre való navigáláskor az erőforrás-hozzárendelések és a kapcsolódó foglalási hiányok jelennek meg.
 ![Egyeztetési nézet a bővítés előtt](media/reconcile-assignments-10.png)

Miután az összes erőforráson végrehajtja a foglalás meghosszabbítása funkciót, a foglalások sikeresen meg lesznek hosszabbítva az összes erőforráshoz. Ennek oka az, hogy az egyes erőforrások munkaideje átfedésben van a hiány körvonalával.
 ![Egyeztetési nézet a foglalás meghosszabbítása után](media/reconcile-assignments-11.png) 

Azonban a foglalások részleteinek alaposabb tanulmányozásakor láthatóvá válnak a különbségek a foglalások kezdőidőpontjai között. A foglalások legkorábban a hozzárendelési felosztás kezdési időpontjában kezdődnek és nem korábban, mint az erőforráshoz elérhető kezdési idő.
 ![Erőforrások új foglalásai az ütemezési táblában](media/reconcile-assignments-12.png)
