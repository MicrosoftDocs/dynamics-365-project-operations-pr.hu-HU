---
title: Több ügyfél kezelése projektalapú árajánlatsorokon
description: Ez a témakör azt ismerteti, hogyan lehet több ügyfelet kezelni projektalapú árajánlatsorokban.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6bb675a6e0b71e88a8176bee2f91152faa53997f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996389"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Több ügyfél kezelése projektalapú árajánlatsorokon

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú árajánlatsorok olyan eseteket támogatnak, ahol minden árajánlatsorban szerepel azoknak az ügyfeleknek a listája, akik fizetnek érte. A projektalapú árajánlatsorban szereplő ügyfelek listája megegyező lehet az árajánlatban szereplő ügyfelek listájával. Másik lehetőségként megváltoztathatja az ügyfelek listáját is. Ha a projektárajánlat megnyerése után létre szeretné hozni a végleges projektszerződést, a program átmásolja a projektalapú árajánlatsorban szereplő ügyféllistát a megfelelő projektalapú szerződéssorra. A projektalapú árajánlatban szereplő ügyfeleket a program a projektszerződésbe másolja.

A végleges projektszerződés számlázásakor a projektalapú szerződéssor ügyféllistája elsőbbséget élvez a projektszerződésben szereplő listával szemben. A projektszerződésben szereplő ügyféladatokat csak az alapértelmezett új projektszerződéssorokhoz lehet felhasználni.

Az összes árajánlati ügyfél a projektárajánlat **Ügyfelek** lapján az árajánlatsori ügyfél alapértelmezett értékkel rendelkezik az árajánlathoz létrehozott minden új projektalapú árajánlatsor esetében. A meglévő projektalapú árajánlatsorok nem fogják örökölni az utánuk létrehozott új árajánlati ügyfélrekordokat.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Árajánlatsori ügyfélrekord létrehozása, módosítása és törlése

Létrehozhat, frissíthet vagy törölhet egy árajánlatsori ügyfelet az **Árajánlatsor ügyfelei** lapon, a **Projektalapú árajánlatsor** oldalon. Amikor hozzáad egy új ügyfelet a projektalapú árajánlatsorhoz, az ügyfél az általános árajánlathoz is hozzáadásra kerül árajánlati ügyfélként, amelynek a teljes árajánlatra vonatkozó alapértelmezett számlázási felosztása 0%. A rendszer a teljes árajánlatra vonatkozó számlázási felosztási százalékértéket az új árajánlat soraiba, illetve a végleges projektszerződésbe másolja. Ha azonban a szerződésből számláz, akkor a rendszer az árajánlatsorban szereplő számlázási felosztási százalékértéket használja, nem a teljes szerződés szintjén érvényes számlázási felosztási százalékértéket. 

Az alábbi táblázat megjeleníti a mezőket a projektalapú árajánlatsor árajánlatsorii ügyfélrekordjában.

| Mező | Hely | Leírás és útmutatás | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Partner** | Szerkeszthető rács az árajánlatsori ügyfél **Árajánlatsori ügyfelek** lapján, fő űrlapján és gyorslétrehozás űrlapján. | Felsorolja az összes aktív partnert. Ez a mező a rekord létrehozása után zárolva van. Ha frissítenie kell a mezőt, törölje, majd hozza létre újra a rekordot. Ha tényleges adatokat rögzített, a bejegyzés nem törölhető. | Ha a hozzáadandó partnerek főlistájából választ ki egy partnert, akkor az árajánlati sor ügyfele is hozzáadásra kerül árajánlati ügyfélként. Az árajánlatsori ügyfelek az árajánlat megnyerése után átmásolásra kerülnek a projektszerződéssori ügyfelekbe is. |
| **Számlázásfelosztás százaléka** | Szerkeszthető rács az árajánlatsori ügyfél **Árajánlatsori ügyfelek** lapján, fő űrlapján és gyorslétrehozás űrlapján. | Az adott árajánlatsori ügyfélnek tulajdonított, nem számlázott értékesítési tranzakciók százalékos arányát jeleníti meg. | Átmásolásra kerül a szerződéssori ügyfelekhez. |
| **Nem meghaladandó korlát** | Szerkeszthető rács az árajánlatsori ügyfél **Árajánlatsori ügyfelek** lapján, fő űrlapján és gyorslétrehozás űrlapján. | Azt jelzi, hogy van-e megállapodás szerinti korlát vagy felső határ az adott ügyfélnek ezzel az árajánlatsorral kapcsolatban számlázott teljes összegre vonatkozóan. | Az árajánlat megnyerése esetén a projektszerződéssorok ügyfeleire másolódik. |
| **Tulajdonos vállalat** | Szerkeszthető rács az árajánlatsori ügyfél **Árajánlatsori ügyfelek** lapján, fő űrlapján és gyorslétrehozás űrlapján. | Az a jogi entitás, amelyben ez az ügyfél be van állítva a **Projektmenedzsment és könyvelés** modulban. Ez a mező írásvédett, és az árajánlat tulajdonos vállalatára van beállítva. A **Partner** mezőben hozzáadni kívánt ügyfelek listáját a rendszer már szűri az adott vállalattól származó listára a Project Operations **Projektmenedzsment és könyvelés** moduljában. | A tulajdonos vállalat felel a jogi személy fogalmának. A projektből származó összes költséget és bevételt a tulajdonos vállalat főkönyvében kell könyvelni. |
| **Kerekítés** | Szerkeszthető rács az árajánlatsori ügyfél **Árajánlatsori ügyfelek** lapján, fő űrlapján és gyorslétrehozás űrlapján. | Jelzi, hogy az ügyfél a projektalapú árajánlatsor alapértelmezett kerekítési ügyfele-e. | Az árajánlat megnyerése esetén a projektszerződés ügyfeleire másolódik. |

## <a name="edit-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázásfelosztási százalékértékek a rendszerben módosíthatók. Ha a számlázásfelosztási százalékok összege nem 100%, hiba lép fel. A számlázásfelosztási százalékok szerkesztése után frissítse az árajánlatsor oldalát a hiba eltávolításához.

Az árajánlatsori ügyfelek alrácsában az egyenletes elosztás műveletet használhatja a számlázási felosztás szétosztására az összes árajánlatsor ügyfélre. Ha van kerekítési tényező, az hozzáadódik a kerekítő ügyfélhez. Az egyik árajánlatsori ügyfelet a rendszer mindig a kerekítési ügyfélként címkézi fel, ami azt jelenti, hogy az árajánlatsori ügyfélrekord kerekítési jelzője **Igen** értékre van beállítva. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]