---
title: Időbejegyzések készítése
description: Ez a témakör információkat nyújt az időbejegyzések létrehozásáról.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b8f88da372cd56b19bed82ad6918da6ddd6f202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593523"
---
# <a name="create-time-entries"></a>Időbejegyzések készítése

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation korábbi verzióiban az időbejegyzéseket hetenként adták meg. A Project Service Automation 3. verziójában az időbejegyzéseket naponta kell beírni. Néhány alkalommal a bejegyzések létrehozása után azonban tömegesen létrehozhat vagy lemásolhatja azokat.

## <a name="create-a-time-entry"></a>Időbejegyzés létrehozása

Időbejegyzés létrehozásához kövesse ezeket a lépéseket.

1. Az **Időbejegyzés** oldalon válassza az **Új** lehetőséget.
2. A **Gyors létrehozás: Időbevitel** párbeszédpanelen adja meg az időbevitel időtartamát percben, órában vagy napban. Az időtartamot a következő formátumban kell megadni: *x* perc, *x* óra vagy *x* nap. Órák és napok decimális értékként is megadhatók, például *xx* óra vagy *xx* nap.
3. Válassza ki az időbevitel típusát és azt a projektet, amelyhez beírja az időbejegyzést.
4. A **Projektfeladat** mezőben keresse meg az időbejegyzés feladatát.

    > [!NOTE]
    > Ha létrehoz egy időbejegyzést a feladathoz, amely nincs hozzárendelve egy felhasználóhoz, a **Projektfeladat** mezőben válassza ki a **Keresés** gombot, válassza a **Nézet módosítása** elemet, majd válassza az **Összes aktív projektfeladat** elemet az összes feladat felsorolásához.

5. Írja be a leírást, ha leírásra van szükség, majd válassza a **Mentés és bezárás** lehetőséget.

Az időbejegyzés létrehozása és mentése után szerkesztheti azt az időbeviteli rácsban. Az időbeviteli rács két formátumot támogat:

- Az időbevitelt **hh:mm** formátumban adhatja meg. Ezt a formátumot ezután órákra és frakciókra konvertálják.
- Az órákat és a frakciókat közvetlenül megadhatja.

Vegye figyelembe, hogy az egy óra töredéke nem perc. Ezért az 1,5 óra 1 óra és 30 perc. Ugyanez a szabály vonatkozik a napi részekre. Egy nap 24 óra, a 0,5 nap pedig 12 órát jelent.

## <a name="bulk-create-time-entries"></a>Időbejegyzések tömeges létrehozása

Néhány időbejegyzés létrehozása után másolhatja őket, hogy tömegesen hozzon létre további időbejegyzéseket.

1. Az **Időbevitel** oldalon válassza a **Hét másolása** lehetőséget.
2. A **Periódusból** mezőcsoportban a **Kezdő dátum** és **Befejező dátum** mezőkben határozza meg az időtartományt, ahonnan az időbejegyzéseket másolni lehet.
3. A **Periódusba** mezőcsoportban a **Kezdő dátum** mezőben adja meg a dátumot, ahova időbejegyzéseket hozhat létre.
4. Válassza a **Másolás** lehetőséget , hogy az **Periódusba** mezőcsoportban megadott hét napjának megfelelő időbejegyzések másolatát hozzon létre. Például a múlt hét hétfőjének időbejegyzését átmásolja arra a hét hétfőjére, amelyet a **Periódusba** mezőcsoport határoz meg.

## <a name="import-data-for-time-entries"></a>Adatok importálása az időbejegyzésekhez

Adatokat importálhat a projektfoglalásokból és a megbízásokból. Adatok importálásakor meghatározhatja az importálandó foglalások dátumtartományát, majd kifejezetten kiválaszthatja azokat a foglalásokat, amelyeket **Vázlat** időbejegyzésként kell létrehozni.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Csoportosítás, rendezés, keresés és szűrési lehetőségek

Az időbejegyzéseket az oszlopokban megadott méretek szerint csoportosíthatja és szűrheti. A **Csoportosítás** mezőben válassza ki az időbejegyzések szűréséhez használandó dimenziót. Az időbeviteli rekordokat növekvő vagy csökkenő sorrendbe is rendezheti az oszlopfejléceken található rendezési nyíl segítségével. Ezenkívül a bejegyzéseket megjelenítheti vagy elrejtheti, ha kiválasztja a **Szűrés** gombot az oszlopfejlécekben, majd a **Keresés** mezőbe írja be azt a szöveget, amelyet az időbejegyzés keresésére használnak a projekt neve, a projekt feladata, az idő szerint bejegyzés vagy erőforrás.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
