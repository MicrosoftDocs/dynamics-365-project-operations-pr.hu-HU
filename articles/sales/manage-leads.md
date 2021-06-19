---
title: Érdeklődők kezelése
description: Ez a témakör információkat nyújt a projektalapú érdeklődőkkel kapcsolatban.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee4b7ce76953909a44e35a2ce044185f89b5ddd5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012724"
---
# <a name="manage-leads"></a>Érdeklődők kezelése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú érdeklődők kezelhetők és minősíthetők a Project Operationsben. Az érdeklődők kezelésének folyamata magában foglalja a munkaalapú érdeklődők létrehozását és ezen érdeklődők minősítését. 

## <a name="project-sales-leads"></a>Projekt érdeklődői

Az **Értékesítés** területen, a bal navigációs panelen nyissa meg az **Érdeklődők** listaoldalt a rendszerben lévő összes érdeklődőrekord listájának megjelenítéséhez. A megjelenített érdeklődők listája munkaalapú és más típusú érdeklődőkből áll, amelyek létrehozhatók akkor is, ha a Dynamics 365 Sales vagy a Dynamics 365 Field Service alkalmazásokkal rendelkezik.

Létrehozhat egy szűrt nézetet, amely csak a projektalapú érdeklődőket tekinti meg a **Típus** értékére vonatkozó szűrő létrehozásával. Megadhatja például, hogy csak a munkaalapú érdeklődők jelenjenek meg.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Új érdeklődő létrehozása projektalapú üzlethez

Projekten alapuló érdeklődő minősítésekor egy lehetőség és egy partner jön létre. A projektalapú lehetőség a Lehetőség fázisában az értékesítést szolgáló tevékenységek kiindulási pontja. A projektalapú lehetőségek egyedi képességekkel rendelkeznek, amelyek a projekt munkájának értékesítéséhez szükségesek. Ezek a lehetőségek többek között a következők:

- Idő és anyag, valamint Fix áras számlázási mód
- Több dátummal hatályos, a projekt során felszámított humán erőforrásokra, kiadásokra és anyagokra érvényes árlisták

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

Az érdeklődők minősítésével kapcsolatos további tudnivalókért lásd: [Érdeklődők minősítése vagy átalakítása](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Érdeklődő minősítése és jogi entitás információi 

Ha a telepítési móddal végzi a Project Operations futtatását, akkor az erőforrás-/nem készletezett alapú esetekhez tartozó projekttevékenységek esetén minden ügyfélnek és lehetőségnek meg kell adnia a **Tulajdonos vállalat** mező értékét. A tulajdonos vállalat a szervezetének egy olyan jogi entitása, amely birtokolja a projekt teljesítését. Minden ügyfél vagy ügyfél kapcsolati típussal rendelkező partner esetében be kell állítani a **Tulajdonos vállalat** mező értékét arra a jogi entitásra, amely ezzel az ügyféllel szerződést köt és tárgyal. Az ügyfél csak egy jogi entitásban lehet.

Az érdeklődő minősítése esetén a létrehozott ügyfél- és lehetőségrekordok esetében a **Tulajdonos vállalat** mező az aktuális felhasználó lefoglalható erőforrásrekordjának vállalatára lesz beállítva.

Ha az aktuális felhasználó által foglalható erőforrásrekord üres, akkor a rendszer a felhasználói rekord **Tulajdonos vállalat** mezőjének értékét használja fel alapértelmezettként az ügyfél- és lehetőségrekordok esetében.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]