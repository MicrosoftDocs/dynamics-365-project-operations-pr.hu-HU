---
title: Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással
description: Ez a témakör bemutatja, hogy a projektkövetelmények hogyan használhatók szerződéses dolgozók vagy alvállalkozói kapacitások használatával a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574645"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az általános projektcsapat tagjai alkalmazottakkal vagy szerződéses munkavállalókkal dolgozhatnak. Ha szerződéses dolgozókkal dolgozik egy projektet, a személyzeti lehetőségeket az alvállalkozói sorhoz rendelt konkrét szerződéses dolgozókra korlátozhatja. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Adott alvállalkozói sorhoz tartozó szerződéses dolgozókkal rendelkező személyzeti erőforrás-követelmények keresése

Ha egy adott alvállalkozói sorhoz tartozó szerződéses dolgozókkal szeretne erőforrás-követelményeket keresni és személyzettel ellátni, hajtsa végre az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapattagot, amely alvállalkozói és alvállalkozói sorra hivatkozik.
2. Hozzon létre egy erőforrás-követelményt ehhez az általános projektcsapattaghoz a **projektcsapattagok alrácsán található Követelmény** létrehozása gombbal.
3. Jelölje ki a csapattagsort, majd válassza a **Könyv** gombot az alrácson. 
4. Ezzel megnyitja az ütemezési táblát a követelménykörnyezettel. Más attribútumok, például dátumok, szerepkörök és szervezeti egységmezők mellett az Ütemezési tábla szűrői automatikusan ki lesznek töltve az erőforrásszükséglet szállítói, alvállalkozói és alvállalkozói sormezőivel is.
5. A rendszer olyan erőforrásokat keres, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat. 
6. Válasszon ki egy szűrt erőforrást, és foglalja le az erőforrást a követelményhez. 
7. A projektcsapat tagja alvállalkozói és alvállalkozói sorhivatkozásokkal jön létre és frissül. Nyissa meg a **Projektbecslések** lehetőséget, és válassza az Árak **frissítése lehetőséget** az erőforrás-hozzárendelés frissített költségének megtekintéséhez. 

> [!NOTE]
> Előfordulhat, hogy a projektcsapat tagjának alvállalkozói és alvállalkozói sorhivatkozással történő frissítése nem mindig lehetséges a foglalás során, ha az erőforrás több alvállalkozói sorhoz van rendelve. Ha a rendszer nem tudja frissíteni a projektcsapat tagját alvállalkozói és alvállalkozói vonallal, akkor nyissa meg a projektcsapat-tag bejegyzését, és manuálisan frissítse ezeket a mezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozó költségét.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>A munkaerő-erőforrásokra vonatkozó követelmények keresése és személyzete bármely szerződéses dolgozónál

Ha bármely szerződéses dolgozónál meg szeretné keresni és személyzettel kapcsolatos erőforrás-követelményeket, hajtsa végre az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapat-tagot.
2. Hozzon létre egy erőforrás-követelményt ehhez az általános projektcsapattaghoz a **projektcsapattagok alrácsán található Követelmény** létrehozása gombbal.
3. Jelölje ki a csapattagsort, majd válassza a **Könyv** gombot az alrácson. 
4. Ezzel megnyitja az ütemezési táblát a követelménykörnyezettel. Más attribútumok, például dátumok, szerepkörök és szervezeti egységmezők mellett az Ütemezési tábla szűrői automatikusan ki lesznek töltve az erőforrásszükséglet szállítói, alvállalkozói és alvállalkozói sormezőivel is. Mivel a követelmény nem töltött ki alvállalkozói vagy alvállalkozói sorértékeket, ezek az attribútumok üresek lesznek a szűrőpanelen.
5. A rendszer olyan erőforrásokat keres, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat.
6. Frissítse a **szűrőpanel Dolgozó típusa** mezőjét Szerződéses **dolgozóra**, hogy a keresést szerződéses dolgozókra korlátozza. A szűrőpanel szállítójának **frissítése**, ha ki szeretne választani egy szállítót, aki a keresést csak egy adott szállítóvállalathoz tartozó szerződéses dolgozók megjelenítésére korlátozza.
7. Válasszon ki egy szerződéses dolgozót a listából, és foglalja le a követelmény erőforrását.
8. Létrejön egy projektcsapat-tag. A projektcsapat tagja azonban nem frissül semmilyen alvállalkozói vagy alvállalkozói sorral, ezért az erőforrás-hozzárendelés nem kerül költségszámításra az alvállalkozói díjszabás használatával. Manuálisan frissítse a projektcsapat tagját egy alvállalkozói vonallal, és lépjen a Projektbecslések **oldalra,** és válassza az Árak **frissítése lehetőséget** az erőforrás-hozzárendelés frissített költségének megtekintéséhez.

> [!NOTE]
> Azok a projektcsapat-tagok, akik dolgozótípussal rendelkeznek **szerződéses dolgozóként** **, de nem rendelkeznek alvállalkozói hivatkozással, érvénytelenként** **vannak megjelölve a** Projektcsapat tagjai **rácson.** Ha vannak ilyen állapotú projektcsapat-tagok, nyissa meg a projektcsapat-tagbejegyzést, és manuálisan frissítse az alvállalkozói és alvállalkozói sormezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költséget a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
