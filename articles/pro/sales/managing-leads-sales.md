---
title: Érdeklődők kezelése - Lite
description: Ez a témakör információkat nyújt a projektalapú érdeklődőkkel kapcsolatban (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e789295d4b1f5a53fcf179a2998f60d35f48f99
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513792"
---
# <a name="manage-leads---lite"></a>Érdeklődők kezelése - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektalapú érdeklődők kezelhetők és minősíthetők a Project Operationsben. Az érdeklődők kezelésének folyamata magában foglalja a munkaalapú érdeklődők létrehozását és ezen érdeklődők minősítését. 

## <a name="list-of-project-sales-leads"></a>Projekt érdeklődőinek listája

Az **Értékesítés** területen, a bal navigációs panelen nyissa meg az **Érdeklődők** listaoldalt a rendszerben lévő összes érdeklődőrekord listájának megjelenítéséhez. A listában szereplő érdeklődők munkaalapúak és más típusú érdeklődők is létrehozhatók, ha rendelkezik a Dynamics 365 Sales vagy a Dynamics 365 Field Service alkalmazással.

Létrehozhat egy szűrt nézetet, amely csak a projektalapú érdeklődőket tekinti meg a **Típus** értékére vonatkozó szűrő létrehozásával. Megadhatja például, hogy csak a munkaalapú érdeklődők jelenjenek meg.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Új érdeklődő létrehozása projektalapú üzlethez

Projekten alapuló érdeklődő minősítésekor egy lehetőség és egy partner jön létre. A projektalapú lehetőség a Lehetőség fázisában az értékesítést szolgáló tevékenységek kiindulási pontja. A projektalapú lehetőségek egyedi képességekkel rendelkeznek, amelyek a projekt munkájának értékesítéséhez szükségesek. Ezek a lehetőségek többek között a következők:

- Idő és anyag, valamint Fix áras számlázási mód
- Több dátummal hatályos, a projekt során felszámított humán erőforrásokra, kiadásokra és anyagokra érvényes árlisták.

Ahhoz, hogy a minősített érdeklődő automatikusan lehetőséget hozzon létre, állítsa a **Típus** attribútumot **Munkaalapú** értékre az érdeklődő létrehozásakor. Ha másik típust választ, akkor az érdeklődő nem hoz létre projekten alapuló lehetőséget a minősítésekor. Ha a projekten alapuló lehetőség nem jön létre, a projektspecifikus lehetőségek nem lesznek elérhetők a későbbi értékesítési folyamatokban.

Az alábbi táblázat az érdeklődő fontos mezőinek adatait, valamint ezeknek a mezőknek az alsóbb rétegbeli hatásait tartalmazza.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Téma | Általános lap | Ennek a szöveges mezőnek az üzlet rövid leírását kell tartalmaznia. | Az érdeklődő témaköre alapértelmezés szerint a Lehetőség, valamint az Árajánlat és Projektszerződés neve lesz. |
| Típus szerint | Általános lap | Ez a értékkészlet mező a következő értékekkel rendelkezik:</br>- Munkaalapú (csak akkor érhető el, ha a Project Operations telepítve van)</br>- Cikkalapú (csak akkor érhető el, ha a Project Operations és a Sales telepítve van)</br>- Szolgáltatáskarbantartás-alapú (elérhető, ha a Field Service telepítve van) | Ha ennek a mezőnek az értéke **Munkaalapú** az érdeklődőn, akkor az érdeklődő minősítve van egy projektalapú lehetőség létrehozására. A projektalapú lehetőség szükséges ahhoz, hogy az adott üzletre vonatkozóan a későbbi értékesítési folyamatban az összes projektspecifikus kiterjesztés és funkció engedélyezve legyen. |
| Keresztnév | Általános lap | Az érdeklődő kapcsolattartójának utóneve | Az érdeklődő minősítésekor egy partner, egy kapcsolattartó és egy lehetőség jön létre. A kapcsolattartó utóneve az itt megadott érték. |
| Vezetéknév | Általános lap | Az érdeklődő kapcsolattartójának vezetékneve | Az érdeklődő minősítésekor egy partner, egy kapcsolattartó és egy lehetőség jön létre. A kapcsolattartó vezetékneve az itt megadott érték. |
| Vállalat | Általános lap | Az érdeklődő ügyfél vállalatának neve | Az érdeklődő minősítésekor egy partner, egy kapcsolattartó és egy lehetőség jön létre. A létrehozott partner neve az itt megadott érték. |
| Pénznem | Részletek lap | Érdeklődő ügyfél pénzneme | Az érdeklődő minősítésekor egy partner, egy kapcsolattartó és egy lehetőség jön létre. A létrehozott partner pénzneme az itt megadott érték. |

## <a name="qualify-a-new-project-based-lead"></a>Új projektalapú érdeklődő minősítése

Az olyan érdeklődőket, akiknek a **Típus** értéke **Munkaalapú**, azokat projektalapú érdeklődőknek nevezzük. A projektalapú érdeklődők minősítése esetén a következő jön létre:

- Egy partner, amely az érdeklődő **Vállalat** mezőjét használja.
- A partnerhez társított kapcsolattartó-bejegyzés, amely az érdeklődő **Utónév** és **Vezetéknév** mezőinek értékein alapul.
- Olyan projektalapú lehetőség, amelynek **Típus** mezője **Munkaalapú** értékre van beállítva.

Az érdeklődők minősítésével kapcsolatos további tudnivalókért lásd: [Érdeklődők minősítése vagy átalakítása](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Üzleti folyamat a projektalapú üzletekhez

A következő üzleti folyamatok támogatottak a Project Operations projektalapú üzletei esetében:

- Érdeklődőből lehetőség üzleti folyamat
- Lehetőség értékesítési folyamata

Az Érdeklődőből lehetőség üzleti folyamat a következő fázisokat támogatja:

| Fázis neve | Leképezett entitás | Funkció |
| --- | --- | --- |
| Megfelel | Érdeklődő | Minősítse az érdeklődőt egy partner, kapcsolattartó vagy lehetőség létrehozásához. |
| Fejlesztés | Lehetőség | Fejlessze tovább a lehetőséget, hogy további információkat tudjon megadni az érintett munkára, a legfontosabb résztvevőkre és a versenytársakra vonatkozóan. |
| Ajánlat | Lehetőség | Fejlessze a javaslatot, és szerezzen jóváhagyást a belső ellenőrzési csoporttól. |
| Bezárás | Lehetőség | Nyerje meg a lehetőséget, és zárja le az üzletet. |
