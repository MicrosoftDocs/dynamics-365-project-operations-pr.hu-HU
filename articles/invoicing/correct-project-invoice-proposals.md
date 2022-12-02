---
title: Könyvelés javítása a tervezet állapotú projektszámla-ajánlatokon
description: Ez cikk ismerteti, hogyan módosíthatók a könyvelési információk egy vázlat állapotú számlajavaslaton.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921213"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Könyvelés javítása a tervezet állapotú projektszámla-ajánlatokon

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektszámlák *Műveleti részleteit* a projektmenedzser egy pro számlán tartja fenn. Az adatok közé tartozik a számlázható órákról, kiadásokról, anyagokról és mérföldkövekről szóló döntés, az árak, valamint az alkalmazott előlegek és a foglalók összegei. Miután megerősített az eredeti pro pro számlát, módosíthatja a műveleti részleteket egy [helyesbítő pro számla](../proforma-invoicing/corrective-invoices.md) létrehozásával és megerősítésével.

A projektszámlák *könyvelési adatait* az ügyfél számára elérhető számladokumentum tartalmazza. Az adatok közé tartozik a áfa számítása és a számlára alkalmazott pénzügyi dimenziók. A cikk részletesen bemutatja, hogyan módosíthatók ezek a könyvelési adatok a projekt számla tervezetén.

## <a name="adjust-sales-tax"></a>Áfakorrekció

Az alapértelmezett számlázási áfacsoportok és a cikkáfacsoportok közvetlenül módosítható a számlajavaslat dokumentumon. A csoportok módosításához válassza a **Szerkesztés** lehetőséget, majd mindegyik projektszámla-javaslat soron adjon meg egy új értéket az **Áfacsoport** vagy a **Cikkáfacsoport** mezőben.

## <a name="adjust-financial-dimensions"></a>Pénzügyi dimenziók korrekciója

### <a name="header-dimensions"></a>Fejlécdimenziók

Alapértelmezés szerint a számla pénzügyi dimenziói a számlázatlan projekttranzakció-rekordokból származnak, amelyek számlázás alatt állnak. A rendszerbeállítások segítségével azonban lehetséges a projektszámlák-javaslatok fejlécében lévő pénzügyi dimenziók használata az ügyfélegyenlegek feladásához. A funkció engedélyezéséhez válassza a **Projektmenedzsment és a Könyvelési paraméterek** oldal **Pénzügyek** lapján a **Projektdimenziók frissítéseinek engedélyezése a kintlévőségekhez**.

A számlafejlécek pénzügyi dimenziói a számla feladása előtt szerkeszthetők. A **Projekt számlajavaslat** lapon váltson a **Fejléc** nézetre, majd szerkessze az értékeket a **Pénzügyi dimenziók** lapon.

A **Fejléc** nézet csak akkor érhető el, ha a rendszergazda engedélyezte a **Projektszámla-ajánlat és számlanapló űrlapok használata Fejléc és Sorok nézetben** funkciót a **Funkciókezelés** mukaterületen. A funkcióhoz 10.0.25-ös vagy újabb Finance frissítés szükséges.

### <a name="line-dimensions"></a>Sordimenziók

A pénzügyi dimenziók nem szerkeszthetők közvetlenül a projektszámla-javaslat sorában. Ehelyett a következő lépésekkel módosíthatja a projektszámlára-javaslat pénzügyi dimenzióit.

1. A projektszámla-javaslaton válassza az **Összes törlése** lehetőséget a projektszámla-javaslat sorainak eltávolításához.

    Az **Összes törlése** gomb csak akkor érhető el, ha a rendszergazda engedélyezte a **Számlajavaslat-sorok törlés a Project Operations használatakor erőforrás-/nem készletalapú forgatókönyvek esetén** funkciót a **Funkciókezelés** mukaterületen.

2. A pénzügyi dimenziók korrekciója:

    - **Számlatranzakciók (számlázási mérföldkövek):** Válassza az **Összes projekt** \> **Kezelés** \> **Számlatranzakciók** lehetőséget, majd válassza ki azt a mérföldkövet, amelyhez a korrekció szükséges. Ezután a **Pénzügyi dimenziók** lapon szükség szerint frissítse az értékeket.
    - **Idő-, költség- és anyagtranzakciók**: A **Feladott projekttranzakciók** lapon válassza a **Könyvelés korrigálása** lehetőséget a pénzügyi dimenziók frissítéséhez.

3. Miután befejezte a pénzügyidimenzió-értékek korrigálását, menjen a **Projektvezetés és a könyvelés** \> **Időszakos** \> **Project Operations integrációja** menübe, és válassza az **Importálás előkészítő táblázatból** lehetőséget a periodikus folyamat futtatásához. A folyamat a frissített pénzügyidimenzió-értékek alapján hozza létre újra a projektszámla-javaslat sorait. Ezután a frissített értékeket használja a projekt alszámláján és főkönyben a projekt számla közzétételekor.
