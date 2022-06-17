---
title: Több ügyfél kezelése projektalapú szerződéssorokon - Lite
description: Ez a cikk több ügyfél projektalapú szerződéssorokon történő kezeléséről nyújt tájékoztatást.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922133"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Több ügyfél kezelése projektalapú szerződéssorokon - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Projektalapú szerződéssorok tartalmazhatják a fizetésért felelős ügyfelek listáját. A projektalapú szerződéssor ügyfeleinek listája megegyezhet a szerződésben szereplő ügyfelek listájával, de ez nem kötelező. A projektárajánlat megnyerése és a projektszerződés létrehozása után az árajánlatsorban szereplő ügyféllistát a rendszer a megfelelő szerződéssorhoz másolja. Az árajánlatban szereplő ügyfeleket a rendszer a szerződésbe másolja.

A Projektszerződés számlázásakor a Projektalapú szerződéssor ügyféllistája elsőbbséget élvez a szerződésen szereplő ügyféllistával szemben. A projektszerződésben szereplő ügyféllistát csak az új szerződéssorok alapértelmezett értékeiként használja a rendszer.

Az összes szerződésügyfél a Projektszerződés **Ügyfelek** lapján alapértelmezés szerint a projektszerződéshez létrehozott bármely új szerződéssor szerződéssorügyfeleinek felel meg. A meglévő szerződéssorok nem öröklik az azokat követően létrehozott új szerződésbeli ügyfélrekordokat.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Szerződéssor ügyfélrekordjának létrehozása, módosítása és törlése

A szerződéssor ügyfelét létrehozhatja, frissítheti vagy törölheti a Projektalapú szerződéssor oldal Szerződéssorügyfelek lapján. Amikor hozzáad egy új ügyfelet a projektalapú szerződéssorhoz, a rendszer a teljes szerződéshez hozzáad egy szerződéses ügyfelet is, amelynek alapértelmezett számlázási felosztása nulla százalék. A rendszer a teljes szerződés számlázási felosztási százalékát átmásolja új szerződéssorokba és a később esetleges projektszerződésbe. A szerződésből történő számlázás esetén azonban a szerződéssor szintjén megadott számlázási felosztási százalékot használja a rendszer, és nem a teljes szerződési szinten szereplő számlázási felosztási százalékot.

Alább láthatók a projektalapú szerződéssor **szerződés** sor-ügyfélrekordjának azon mezőit, amelyeket a munkavégzés során figyelni kell:

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Partner** | A **szerződésügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél **fő**- és **gyorslétrehozási** űrlapjai. | Összes aktív partner. Ez a mező a rekord létrehozása után zárolva van. A mező frissítéséhez törölje a rekordot, és hozzon létre egy új rekordot. Ha bármilyen tényadatokat rögzített, akkor nem törölheti a rekordot. Az adott partnernél azonban a számlázási felosztás százalékos értékét megjelölheti nullaként. Ha a rekord jelölése nulla értékű, az hatással van az adott ügyfélnek tulajdonított vagy felosztott minden jövőbeli költség- és bevételi tényadatra. | Ha a partnerek főlistájából választ partnert, és azt szeretné hozzáadni és menteni, akkor a szerződéssor ügyfelet is felveszi a szerződési ügyfélként. A szerződéssor ügyfeleit a számlák létrehozásakor használja a rendszer. |
| **Számlázásfelosztás százaléka** | A **szerződésügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél **fő**- és **gyorslétrehozási** űrlapjai. | Ez a mező az egyes nem számlázott értékesítési tranzakciók azon hányadát jelenti, amelyet ez a szerződéssorügyfélhez tulajdonítanak. | A szerződéssor ügyfeleit és a számlázási felosztási százalékértékeket akkor használja a rendszer, ha a jóváhagyás után a rendszer létrehozza a tényleges adatokat, és a számla létrehozásakor. |
| **Nem meghaladandó korlát** | A **szerződésügyfelek** lapján szerkeszthető rács, valamint a szerződésügyfél **fő**- és **gyorslétrehozási** űrlapjai. | Azt jelzi, hogy van-e megállapodott korlát vagy felső határ az adott ügyfélnek a szerződéssorért számlázott teljes összegre. | A szerződéssorügyfélre vonatkozó nem meghaladandó korlátot akkor használja a rendszer, ha a tényleges adatok létrejönnek, és a számlák létrejönnek. |
| **Kerekítés** | A **szerződésügyfelek** lapján szerkeszthető rács, valamint a szerződéssorügyfél **fő**- és **gyorslétrehozási** űrlapjai. | Ez a mező azt jelzi, hogy az ügyfél a projektalapú szerződéssor alapértelmezett kerekítési ügyfele-e. | Ha a számlázás felosztásai százaléka alapján tényleges értéket hoz létre, előfordulhat, hogy némi kerekítési különbség van. Ennek az ügyfélnek tulajdonítja a kerekítési különbözeteket ebben az esetben a rendszerhez. |

## <a name="edit-billing-split-percentages"></a>Számlázásfelosztási százalékok szerkesztése

A számlázás felosztási százaléka a rácsban szerkeszthető. Ha a számlázásfelosztási százalékértékek nem tesznek ki teljes 100 százalékot, akkor hiba történik. A számlázási felosztás százalékos értékének módosítása után frissítse a lapot a hiba eltávolításához.

Kiválaszthatja az **Egyenlő elosztás** lehetőséget is az szerződéssor ügyfeleinek részrácsán. Ez a művelet egyenletesen leosztja a számlázási felosztásokat az összes szerződéssor-ügyfél számára. Ha bármilyen kerekítési tényező van, akkor a rendszer hozzáadja a kerekítési ügyfélhez. Az egyik szerződéssor ügyfele mindig úgy van címkézve, mint az a **kerekítési** ügyfél, akinél a **Kerekítés** jelző **Igen** értékre van állítva.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]