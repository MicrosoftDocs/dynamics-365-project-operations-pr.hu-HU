---
title: Költségsablonok beállítása
description: Ez a témakör információt nyújt a költségsablonok létrehozásáról és használatáról a Project Operations szolgáltatásban.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993559"
---
# <a name="set-up-cost-templates"></a>Költségsablonok beállítása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


Ez a témakör információt nyújt a költségsablonok létrehozásáról és használatáról a Project Operations szolgáltatásban. A költségsablon határozza meg a következőket:

- A projektkategóriákat az előrejelzésekhez, és az aktuális tranzakciókat, a amelyek bele vannak számítva a projekt készenlétszámításának százalékos értékébe. Ezután a készültségi százalék értékét használja a program annak kiszámítására, hogy mekkora bevétel lett realizálva.
- Az, hogy a készültségi százalék módosítható-e, ha az automatikusan van számítva.
- Azt jelzi, hogy a készültségi százalékot összeg vagy egység alapján számítja-e a program.

## <a name="cost-template-example"></a>Példa a költségsablonra

Az ügyfél webhelyének tervezésével kapcsolatos projektjein dolgozik, ahol a 10 000 dollár átalánydíjait számít fel. Az előrejelzése szerint 100 óra (5 000 dollár) lesz szükséges projekt befejezéséhez. Emellett két repülőjegyet és négy szállodai éjszakát is becsül az ügyfél telephelyére történő utazásokhoz (1800 dollár). Ennek eredményeképpen a teljes előrejelzett költsége 6800 dollár.

Ha a rögzített árú bevételelszámolási eljárást futtatja a hónap végén becslés létrehozásához, és azt az eredményt kapja, hogy 35 órát dolgozott a projekten. Ez még nem tartalmazza a repülőjáratokat és a szállodai költségeket. Emellett egy asszisztensnek öt órányi kutatást kell végeznie a projekthez 100 dollár költségén, amelyet nem terveztek.

A projekt készültségi szintjének kiszámításakor a következő lehetőségek közül választhat:

- Kívánja szerepeltetni az összes költséget (óra és kiadások) vagy csak órákat?
- Kívánja szerepeltetni az összes órát vagy csak a tervezett órákat?
- A készültségi százalékot a tervezett órák dollárra vetített értéke (USD 5 000) vagy csak az órák száma alapján (100) szeretné kiszámítani?

Az ezekre a kérdésekre adott válaszok határozzák meg, hogy milyen beállításokat alkalmaz a költségsablonhoz, és azt, hogy milyen kategóriákat választ ki a költségsablon soraiban.

A következő táblázat a forgatókönyv készültségi szintjének számítási módszereit mutatja be.

| A teljesítés alapja | Dollárköltség vagy egységek | Készültségi százalék | Számítás |
| --- | --- | --- | --- |
| Minden óra, nincs költség | Dollárköltség | 37% 35 x USD 50 + USD 100 = USD 1850 USD 1850/USD 5 000 |
| Minden óra, nincs költség | Mértékegységek | 40% | 40 óra/100 óra (beleértve öt nem tervezett órát) |
| Tervezett órák, nincs költség | Dollárköltség vagy egység | 35% | 35/100 óra vagy 35 x 50/5000 USD |
| Minden óra és költség | Dollárköltség | 27,2% | 1850 USD / 6800 USD |

Annak eldöntése, hogy melyik megközelítési módot alkalmazza a költségkategória létrehozásához, több szempont is függhet:

- Ha a költségsablonba nem tervezett órákat is felveszi, akkor a projekt befejezése előtt a 100 százalékos készültséget éri el. Ennek oka az, hogy a tényleges órák száma több lesz a tervezett óráknál. Ha a táblázatban felsorolt első két módszer egyikét használja, akkor módosítania kell a tervet (előrejelzett egységeket), amikor tudomást szerez az eltérésekről. Ebben az esetben a projekt befejezéséi szükségleteivel kapcsolatos ismerete alapján hozzáadhat vagy kivonhat a órákat. Ha a projekt befejezéséhez további 65 óra szükséges, öt órát kell felvennie a tervbe összesen 105 órához.. Ha tudja, hogy az asszisztens újabb öt órányi kutatást végez majd, a teljes összeg 110 óra lesz.
- Ha a táblázatban szereplő harmadik módszert használja, akkor csak a tervezett órákat frissíti a saját idejére, hogy a százalékos teljesítése számítása pontos maradjon. A jövedelmezőség változni fog, ha a nem tervezett órákat rögzíti a rendszer, de az ismert, készültségi pályán marad.
- Ha a táblázatban szereplő negyedik módszert használja, fennáll a kockázata annak, hogy a kiadások szabálytalan időpontokban fognak megjelenni, és nem tükröződnek a teljesítési folyamatban. Ezért ha a kiadások szerepeltetve vannak, akkor a készültségi százalék a kívánatosnál nagyobb mértékben ingadozhat. Például azért, mert nem repült még, a teljes készültségi szint 27%-os volt a 35 százalék vagy 37 százalék helyett, ha a számítást csak időre alapozza. Ha a két éjszakás utazás már megtörtént, és a repülési és a szállodai költségek pontosan lettek becsülve a készültségi szint 40,4 százalék lenne (1850 dollár a munkára és a 900 dollár költségekhez = 2750 USD / 6800 USD = 40,4%). Ezért mindössze egy repülőút kiadásai a készenléti százalékot 27 százalékról 40 százalékre módosítanák.

## <a name="create-cost-templates"></a>Költségsablonok létrehozása
Kövesse az alábbi a lépéseket költségsablonok létrehozásához:

1. A költségsablonok eléréséhez a Dynamics 365 Finance-környezetben nyissa meg a **Projektvezetés és könyvelés** > **Beállítás** > **Becslések** > **Költségsablon** lehetőséget.
2. Új költségsablon létrehozásához válassza az **Új** lehetőséget. Adjon meg egy nevet és egy leírást.
3. Adja meg a költségsor azonosítóját mindegyik tranzakciótípus esetében.
4. Válasszon egy alapértelmezett készültségi módszert:

  - **Automatikus**: A készültségi százalékot a program automatikusan kiszámítja a projekthez. A kapott érték nem módosítható.
  - **Manuális**: A készültségi százalékot a program automatikusan kiszámítja a projekthez. A kapott érték nem módosítható.

  > [!NOTE]
  > A manuális számítások esetén a készültségi fok a **Becslés** oldal **Általános** lapjának **Manuális számítás** szakasza alatt van tárolva.

5. **A teljesítés alapja** szakaszban válasszon a következő értékek közül:

  - **Összeg** : A könyvelési pénznemben kifejezett összeg alapján számítja ki a befejezettségi százalékot.
  - **Egység**: A mennyiség alapján van a befejezettségi százalék kiszámítva.
  - **Egyenes vonal**: A rendszer arányos módon számítja ki a teljesítés százalékos arányát a projekt kezdési és befejezési dátuma használatával a projekt hosszának meghatározásához.

6. Válassza a **Költségsorok** lehetőséget , ha szeretné áttekinteni a költségkategória költségsorait. Minden tranzakciótípus esetében legalább egy költségsor szükséges. Ugyanakkor több költségsor is létrehozható ugyanahhoz a tranzakciótípushoz, és ezekhez a sorokhoz a kívánt attribútumok beállíthatók.
7. A **Kategóriák** lapon jelölje ki a költségsablon sorában szerepeltetni kívánt projektkategóriákat.
8. Az **Általános** válassza ezt, ha a sor szerepelni fog a készenléti százalékban.
9. Válassza ki a készültségi százalék kiszámításakor használandó teljesítési költség módszert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]