---
title: Szerződéses munkavállalókkal és alvállalkozói kapacitással rendelkező projekt személyzete
description: Ez a témakör elmagyarázza, hogy a projektkövetelmények hogyan használhatók szerződéses alkalmazottakkal vagy a Microsoft alvállalkozói kapacitásával Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903684"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Szerződéses munkavállalókkal és alvállalkozói kapacitással rendelkező projekt személyzete

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az általános projektcsapat tagjai alkalmazottakkal vagy szerződéses munkavállalókkal is együttműködhetnek. Ha szerződéses alkalmazottakkal dolgozik egy projekten, a személyzeti lehetőségeket az alvállalkozói vonalhoz rendelt szerződéses munkavállalókra korlátozhatja. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Személyzeti erőforrás-követelmények keresése egy adott alvállalkozói vonalhoz tartozó szerződéses munkavállalókkal

Ha egy adott alvállalkozói vonalhoz tartozó szerződéses munkavállalókkal szeretne erőforrás-követelményeket keresni és személyzettel keresni, kövesse az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapattagot, amely alvállalkozói és alvállalkozói vonalra hivatkozik.
2. Erőforrás-követelmény létrehozása ehhez az általános projektcsapattaghoz a **projektcsapattagok** alrácsának Követelmény létrehozása gombjának használatával.
3. Jelölje ki a csapattag sorát, majd válassza az **alrács Könyv** gombját. 
4. Ezzel megnyitja az Ütemezési táblát a követelménykörnyezettel. Más attribútumokkal, például dátumokkal, szerepkör- és szervezeti egységmezőkkel együtt az Ütemezési tábla szűrői automatikusan feltöltve vannak az erőforrás-követelmény szállítói, alvállalkozói és alvállalkozói sormezőivel is.
5. A rendszer olyan erőforrásokat keres, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat. 
6. Válassza ki a szűrt erőforrások egyikét, és foglalja le a követelmény erőforrását. 
7. A projektcsapat tagja alvállalkozói és alvállalkozói vonali hivatkozásokkal jön létre és frissül. Lépjen a **Projektbecslések** elemre, és válassza az Árak frissítése lehetőséget **az** erőforrás-hozzárendelés frissített költségének megtekintéséhez. 

> [!NOTE]
> Előfordulhat, hogy a projektcsapat tagjának alvállalkozói és alvállalkozói vonalra való hivatkozással történő frissítése nem mindig lehetséges a foglalás során, ha az erőforrás több alvállalkozói sorhoz van rendelve. Ha a rendszer nem tudja frissíteni a projektcsapat tagját alvállalkozói és alvállalkozói sorokkal, nyissa meg a projektcsapat tagjának rekordját, és manuálisan frissítse ezeket a mezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze az alvállalkozói költségeket.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Erőforrás-követelmények keresése és személyzeti erőforrás-követelményeinek keresése bármely szerződéses alkalmazottal

Ha bármely szerződéses dolgozóval keresni és személyzeti erőforrás-követelményeket szeretne keresni, kövesse az alábbi lépéseket:

1. Hozzon létre egy általános projektcsapattagot.
2. Erőforrás-követelmény létrehozása ehhez az általános projektcsapattaghoz a **projektcsapattagok** alrácsának Követelmény létrehozása gombjának használatával.
3. Jelölje ki a csapattag sorát, majd válassza az **alrács Könyv** gombját. 
4. Ezzel megnyitja az Ütemezési táblát a követelménykörnyezettel. Más attribútumokkal, például dátumokkal, szerepkör- és szervezeti egységmezőkkel együtt az Ütemezési tábla szűrői automatikusan feltöltve vannak az erőforrás-követelmény szállítói, alvállalkozói és alvállalkozói sormezőivel is. Mivel a követelmény nem tartalmazott alvállalkozói vagy alvállalkozói sorértékeket, ezek az attribútumok üresek lesznek a szűrőablakban.
5. A rendszer olyan erőforrásokat keres, amelyek megfelelnek a szűrési feltételeknek, és felsorolja azokat.
6. Frissítse a **szűrőablak Dolgozó típusa** mezőjét **Szerződés-feldolgozóra,** hogy a keresést szerződéses dolgozókra korlátozza. Frissítse **a** szállítót a szűrőablakban, és válasszon ki egy szállítót, hogy korlátozza a keresést, hogy csak egy adott szállítóvállalathoz tartozó szerződéses dolgozók jelenjenek meg.
7. Válasszon ki egy szerződéses dolgozót a listából, és foglalja le a követelmény erőforrását.
8. Létrejön a projektcsapat tagja. A projektcsapat tagja azonban nem frissül semmilyen alvállalkozói vagy alvállalkozói vonallal, ezért az erőforrás-hozzárendelés nem kerül költségszámításra az alvállalkozói díjszabással. Manuálisan frissítse a projektcsapat tagját egy alvállalkozói sorra, majd lépjen a **Projektbecslések** elemre, és válassza az Árak frissítése lehetőséget **az** erőforrás-hozzárendelés frissített költségének megtekintéséhez.

> [!NOTE]
> Azok a projektcsapat-tagok, amelyek **feldolgozói típussal rendelkeznek** szerződéses **dolgozóként, de nem rendelkeznek** alvállalkozói hivatkozással, érvénytelenként vannak megjelölve **a** **Projektcsapat tagjai** rácson. Ha vannak ilyen állapotú projektcsapattagok, nyissa meg a projektcsapat tagjának rekordját, és manuálisan frissítse az alvállalkozói és alvállalkozói sormezőket úgy, hogy a pénzügyi költségbecslés pontosan tükrözze a Becslések lapon szereplő **alvállalkozói költségeket.** 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
