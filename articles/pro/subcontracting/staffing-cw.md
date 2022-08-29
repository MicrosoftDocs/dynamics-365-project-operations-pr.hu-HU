---
title: Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással
description: Ez a cikk azt ismerteti, hogyan lehet a projektkövetelményeket szerződéses dolgozók vagy alvállalkozói kapacitás használatával személyzettel ellátni a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261257"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekt felszerelése szerződéses alkalmazottakkal és az alvállalkozói szerződésben rögzített kapacitással

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az általános projektcsapat tagjai alkalmazottakkal vagy szerződéses dolgozókkal együtt lehetnek alkalmazottakkal vagy szerződéses dolgozókkal. Amikor egy projektet szerződéses dolgozókkal lát el, korlátozhatja a személyzeti lehetőségeket az alvállalkozói sorhoz rendelt konkrét szerződéses alkalmazottakra. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Személyzeti erőforrás-követelmények keresése egy adott alvállalkozói sorhoz tartozó szerződéses dolgozókkal

Ha egy adott alvállalkozói sorhoz tartozó szerződéses dolgozókat szeretne keresni és személyzeterőforrás-követelményeket keresni, kövesse az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapattagot, amely alvállalkozói és alvállalkozói sorra hivatkozik.
2. Hozzon létre egy erőforrásigényt ehhez az általános projektcsapattaghoz a **projektcsapat tagjai alrács követelmény létrehozása** gombjával.
3. Jelölje ki a csapattagok sorát, majd válassza a **Foglalás** gombot az alrácson. 
4. Ez megnyitja az ütemezési táblát a követelménykörnyezettel. Más attribútumok, például dátumok, szerepkör és szervezetiegység-mezők mellett az Ütemezési tábla szűrők is automatikusan ki lesznek töltve az erőforrás-követelmény szállítói, alvállalkozói és alvállalkozói sormezőivel.
5. A rendszer megkeresi azokat az erőforrásokat, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat. 
6. Válassza ki az egyik szűrt erőforrást, és foglalja le az erőforrást a követelményhez. 
7. Létrejön a projektcsapat tagja, és frissül alvállalkozói és alvállalkozói sorhivatkozásokkal. Nyissa meg a **Projektbecslések** lapot, és válassza az Árak **frissítése lehetőséget** az erőforrás-hozzárendelés frissített költségének megtekintéséhez. 

> [!NOTE]
> Előfordulhat, hogy a projektcsapat tagjának alvállalkozói és alvállalkozói vonalhivatkozással való frissítése nem mindig lehetséges a foglalás során, ha az erőforrás több alvállalkozói sorhoz van rendelve. Ha a rendszer nem tudja frissíteni a projektcsapat tagját alvállalkozói és alvállalkozói sorral, akkor nyissa meg a projektcsapat tagrekordját, és manuálisan frissítse ezeket a mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költséget.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>A személyzet erőforrás-követelményeinek keresése és személyzete bármely szerződéses dolgozóval

Ha bármely szerződéses dolgozónál meg szeretné keresni az erőforrás-követelményeket, és személyzete számára, kövesse az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapat-tagot.
2. Hozzon létre egy erőforrásigényt ehhez az általános projektcsapattaghoz a **projektcsapat tagjai alrács követelmény létrehozása** gombjával.
3. Jelölje ki a csapattagok sorát, majd válassza a **Foglalás** gombot az alrácson. 
4. Ez megnyitja az ütemezési táblát a követelménykörnyezettel. Más attribútumok, például dátumok, szerepkör és szervezetiegység-mezők mellett az Ütemezési tábla szűrők is automatikusan ki lesznek töltve az erőforrás-követelmény szállítói, alvállalkozói és alvállalkozói sormezőivel. Mivel a követelmény nem tartalmazott alvállalkozói vagy alvállalkozói sorértékeket, ezek az attribútumok üresek lesznek a szűrőpanelen.
5. A rendszer megkeresi azokat az erőforrásokat, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat.
6. Frissítse a **szűrőpanel Dolgozó típusa** mezőjét Szerződéses dolgozóra **,** hogy a keresést a szerződéses dolgozókra korlátozza. Frissítse **a Szállítót** a szűrőpanelen, hogy kiválasszon egy szállítót, hogy a keresést csak az adott szállítóvállalathoz tartozó szerződéses dolgozók jelenjenek meg.
7. Válasszon ki egy szerződéses dolgozót a listából, és foglalja le a követelmény erőforrását.
8. Létrejön egy projektcsapattag. A projektcsapat tagja azonban nem frissül alvállalkozói vagy alvállalkozói sorral, ezért az erőforrás-hozzárendelés nem kerül az alvállalkozói díjszabás használatával. Manuálisan frissítse a projektcsapat tagját egy alvállalkozói sorral, és lépjen a Projektbecslések **elemre**, és válassza az Árak **frissítése lehetőséget** az erőforrás-hozzárendelés frissített költségének megtekintéséhez.

> [!NOTE]
> Azok a projektcsapat-tagok, akik feldolgozó típusú szerződéssel rendelkező **feldolgozói** **típusúak**, de nem rendelkeznek alvállalkozói referenciával, érvénytelenként **vannak** megjelölve a **Projektcsapat tagjai** rácsban. Ha vannak ilyen állapotú projektcsapat-tagok, nyissa meg a projektcsapat tagjainak rekordját, és manuálisan frissítse az alvállalkozói és alvállalkozói sor mezőket, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költséget a **Becslések** lapon. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
