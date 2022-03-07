---
title: Könyvelés javítása a tervezet állapotú projektszámla-ajánlatokon
description: Ez témakör ismerteti, hogyan módosíthatók a könyvelési információk egy vázlat állapotú számlajavaslaton.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251225"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Könyvelés javítása a tervezet állapotú projektszámla-ajánlatokon

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektszámlák *Műveleti részleteit* a projektmenedzser egy pro számlán tartja fenn. Az adatok közé tartozik a számlázható órákról, kiadásokról, anyagokról és mérföldkövekről szóló döntés, az árak, valamint az alkalmazott előlegek és a foglalók összegei. Miután megerősített az eredeti pro pro számlát, módosíthatja a műveleti részleteket egy [helyesbítő pro számla](../proforma-invoicing/corrective-invoices.md) létrehozásával és megerősítésével.

A projektszámlák *könyvelési adatait* az ügyfél számára elérhető számladokumentum tartalmazza. Az adatok közé tartozik a áfa számítása és a számlára alkalmazott pénzügyi dimenziók. A témakör részletesen bemutatja, hogyan módosíthatók ezek a könyvelési adatok a projekt számla tervezetén.

## <a name="adjust-sales-tax"></a>Áfakorrekció

Az alapértelmezett számlázási áfacsoportok és a cikkáfacsoportok közvetlenül módosítható a számlajavaslat dokumentumon. A csoportok módosításához válassza a **Szerkesztés** lehetőséget, majd mindegyik projektszámla-javaslat soron adjon meg egy új értéket az **Áfacsoport** vagy a **Cikkáfacsoport** mezőben.

## <a name="adjust-financial-dimensions"></a>Pénzügyi dimenziók korrekciója

A pénzügyi dimenziók nem szerkeszthetők közvetlenül a projektszámla-javaslat sorában. Ehelyett a következő lépésekkel módosíthatja a projektszámlára-javaslat pénzügyi dimenzióit.

1. A projektszámla-javaslaton válassza az **Összes törlése** lehetőséget a projektszámla-javaslat sorainak eltávolításához.

    > [!NOTE]
    > Az **Összes törlése** gomb csak akkor érhető el, ha a rendszergazda engedélyezte a **Számlajavaslat-sorok törlés a Project Operations használatakor erőforrás-/nem készletalapú forgatókönyvek esetén** funkciót a **Funkciókezelés** mukaterületen.

2. A pénzügyi dimenziók korrekciója:

    - **Számlatranzakciók (számlázási mérföldkövek):** Válassza az **Összes projekt** \> **Kezelés** \> **Számlatranzakciók** lehetőséget, majd válassza ki azt a mérföldkövet, amelyhez a korrekció szükséges. Ezután a **Pénzügyi dimenziók** lapon szükség szerint frissítse az értékeket.
    - **Idő-, költség- és anyagtranzakciók**: A **Feladott projekttranzakciók** lapon válassza a **Könyvelés korrigálása** lehetőséget a pénzügyi dimenziók frissítéséhez.

3. Miután befejezte a pénzügyidimenzió-értékek korrigálását, menjen a **Projektvezetés és a könyvelés** \> **Időszakos** \> **Project Operations integrációja** menübe, és válassza az **Importálás előkészítő táblázatból** lehetőséget a periodikus folyamat futtatásához. A folyamat a frissített pénzügyidimenzió-értékek alapján hozza létre újra a projektszámla-javaslat sorait. Ezután a frissített értékeket használja a projekt alszámláján és főkönyben a projekt számla közzétételekor.
