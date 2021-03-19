---
title: Projektalapú szerződéssor becslése - lite
description: Ez a témakör információkat nyújt a projektalapú szerződéssorokkal kapcsolatos becslésről.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273540"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projektalapú szerződéssor becslése - lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations szolgáltatásban a projektalapú szerződéssor részletei segítenek megbecsülni a szerződéssor teljesítéséhez szükséges az adott munkához kapcsolódó költségeket és a lehetséges bevételeket.

A projektalapú szerződéssor becsléséhez nyissa meg a **Szerződéssor részletei** lapot a projektalapú **Szerződéssor** területen.  A projekt alapú szerződéssorok esetében kétféle módon lehet becslést létrehozni:

   - A szerződéssor adatainak manuális hozzáadásával létrehozhat egy becslést közvetlenül a szerződéssoron.
   - Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekt szerződéssorához. Ez lehetővé teszi azt a folyamatot, amellyel a projektterv becslését importálhatja a szerződéssorra a szerződéssoron található összetevők alapján.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Becslés létrehozása közvetlenül egy projektalapú szerződéssoron

1. Nyissa meg a szerződéssort, és válassza a **Szerződéssor részletei** lapot. Az ezen a lapon létrehozott sorokat a rendszer összefoglalja, és a **Szerződött értékként** jeleníti meg ehhez a **Szerződéssorhoz**. 
2. A **Szerződéssor részletei** alrácsban válassza a **+ Új szerződéssor-részlet** lehetőséget. Megnyílik egy gyorslétrehozás csúszka. A következő mezők a **Szerződéssorok részletei** űrlapon érhetők el:

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Leírás** | **Gyorslétrehozás** | Egy adott becslés leírása. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Tranzakció osztálya** | **Gyorslétrehozás** | Ez a legördülő lista a projekt alapú szerződéssor **Általános** lapján szereplő tranzakciós osztályok listáját tartalmazza. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Szerepkör** | **Gyorslétrehozás** | Annak a személynek a szerepköre, aki ezt a munkát teljesíti, vagy ezt a költséget viseli. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Kategória** | **Gyorslétrehozás** | A munka vagy a költség kategóriája. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Kezdő dátum** | **Gyorslétrehozás** | A munka kezdődátuma. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Befejező dátum** | **Gyorslétrehozás** | A munka befejező dátuma. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költséghez. |
| **Erőforrás-kezelő részleg** | **Gyorslétrehozás** | A beszerzési egység, amely ezt a költséget vállalja, és biztosítja az erőforrást amelyen a munkavégzés történik. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. Ez a mező az önköltségi ár beolvasása esetén is használatos. |
| **Egységütemezés** | **Gyorslétrehozás** | A munka vagy költség egységcsoportja. Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak. Például a *mérföld* és a *kilométer (km)* olyan egység, amely a távolságot leíró egységek csoportjához tartozik. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Egység** | **Gyorslétrehozás** | A munka vagy költség mértékegysége. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Mennyiség** | **Gyorslétrehozás** | A munka vagy költség mennyisége. | Ez a mező alapértelmezés szerint a kapcsolódó szerződéssor részleteit tartalmazza az automatikusan létrehozott költségekhez. |
| **Egységár** | **Gyorslétrehozás** | A munkát elvégő szerepkör számlázási díja vagy a költségkategória eladási ára. Ez a mező alapértelmezés szerint arra az **Időre** áll be, amely a szerepkör és az erőforrásbiztosító egység kombinációja alapján kezdő dátumként érvényes a projekt árlistájában. A költségek esetében a mező alapértelmezett értéke az árbeállításból származik a projekt árlistában, ami a kezdő dátumon érvényes. Ha a tranzakciós kategória árképzési módja nem **egységár**, nincs alapértelmezett érték, és ez a mező üresen marad. | A munkát elvégő szerepkör költség díja vagy a költségkategória egységára. Ennek a mezőnek az alapértelmezett értéke a **Szerepkörön alapuló idő** és az erőforrásegység kombinációja a szerepkörár során az önköltségi ár listáján, amely a kezdődátumon érvényes szerződő egységhez kapcsolódik. A költségek esetében a mező alapértelmezett értéke az önköltségi árlista kategóriaár során alapul, ami a kezdő dátumon érvényes. Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad. |
| **Becsült adó** | **Gyorslétrehozás** | A munkára vagy költségre vonatkozó becsült adó a felhasználó által bevitt adatként. | A munkára vagy költségre vonatkozó becsült adó a felhasználó által bevitt adatként. |
| **Összeg** | **Gyorslétrehozás** | Ha a **Mennyiség** és az **Ár** mező üres, akkor a felhasználó hozzáadhatja ezt az értéket ebben a mezőben. Ha a **Mennyiség** és az **Ár** ki van töltve, az **Összeg** mező írásvédett, és számítása a következő **(Mennyiségi \* Egységár) + adó**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Az árak frissítése a szerződéssorok részleteiben

Ha módosítja a szerződéshez vagy a szerződő egység önköltségi árlistájához tartozó projektárlista árait, akkor az egyes szerződéssorok részleteiben szereplő árakat frissítheti, hogy azok tükrözzék a változást. A **Szerződés** lapon válassza az **Újraszámolás** lehetőséget. Egy figyelmeztetés jelenik meg, amely közli, hogy a szerződés összes szerződéssorán az árak alaphelyzetbe lesznek állítva. Válassza az **Igen** lehetőséget, ha frissíteni szeretné az értékesítési és a költség szerződéssor-részleteinek árát is.

## <a name="access-contract-line-details-for-cost"></a>A szerződéssor részleteinek elérése költséghez

A **Szerződéssor részletei** lapon jelöljön ki egy sort a rácsban, hogy megjelenítse a műveleteket az alrács eszköztárán. Az elrács eszköztár első művelete a **Költség részleteinek megnyitása**. Ha meg szeretné tekinteni a kapcsolódó költségarányt és összeget ehhez a szerződéssorhoz akkor válassza a **Költség részleteinek megnyitása** lehetőséget. 

> [!NOTE]
> Ha módosítja a beszerzési vállalat, a beszerzési egység, a mennyiség, a dátum, a szerepkör vagy a kategória értékeit a **Költséghez** tartozó szerződéssorok részleteiben, azzal módosítja a kapcsolódó értékeket az **Értékesítés** szerződéssor-részleteiben is.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>A szerződéssorok részleteinek pénzneme a költségre és az értékesítésre vonatkozóan

Az **Értékesítés** szerződéssor részletei az alapértelmezett pénznemet határozzák meg a projektárlistából, amely a szerződéssor részlet kezdési dátumán érvényes.

A **Költség** szerződéssor részletei az alapértelmezett pénznemet határozzák meg a szerződés szerződő egységének árlistájából, amely a **Költséghez** kapcsolódó szerződéssor részlet kezdési dátumán érvényes.

A jövedelmezőségi számítások átalakítják a **Költség** és **Értékesítés** szerződéssor részleteinek összegét annak a környezetnek az alappénznemére, amelybe jelenteni kell a szerződés teljes tényleges és becsült árréseit.

> [!NOTE]
> A pénznem kerekítési hibái és a módosított árrések azért fordulhatnak elő, mert hiányoznak a dátumon érvényes átváltási árfolyamok. Ezeket a számításokat csak becslésként használhatja a projektszerződésekben, és nem a tényleges jogi vagy egyéb jelentéskészítésre, amely nagyobb pontosságot igényel az átváltási árfolyamok kerekítése és hatályossága tekintetében.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]