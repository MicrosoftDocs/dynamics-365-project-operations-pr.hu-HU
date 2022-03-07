---
title: Projektszerződéssor becslése
description: Ez témakör a projektszerződéssor becsléséről nyújt tájékoztatást.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ae2d96170348a00b58f1571b6c9b31af894c281bdfdfcb00f4e348b2705186c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986899"
---
# <a name="estimate-a-project-contract-line"></a>Projektszerződéssor becslése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_ 

A Dynamics 365 Project Operations szolgáltatásban a projektalapú szerződéssor részletei segítenek megbecsülni a szerződéssor teljesítéséhez szükséges az adott munkához kapcsolódó költségeket és a lehetséges bevételeket.

A projektalapú szerződéssor becsléséhez nyissa meg a **Szerződéssor részletei** lapot a projektalapú **Szerződéssor** területen.  A projekt alapú szerződéssorok esetében kétféle módon lehet becslést létrehozni:

   - A szerződéssor adatainak manuális hozzáadásával létrehozhat egy becslést közvetlenül a szerződéssoron.
   - Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekt szerződéssorához. Ez lehetővé teszi azt a folyamatot, amellyel a projektterv becslését importálhatja a szerződéssorra a szerződéssoron található összetevők alapján.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Becslések létrehozása közvetlenül egy projektszerződéssoron

Ahhoz, hogy közvetlenül a projektszerződéssoron tudjon becsléseket létrehozni, kövesse az alábbi lépéseket:

1. Nyissa meg a szerződéssort, és válassza a **Szerződéssor részletei** lapot. Az ezen a lapon létrehozott sorokat a rendszer összefoglalja, és a **Szerződött értékként** jeleníti meg ehhez a **Szerződéssorhoz**. 
2. A **Szerződéssor részletei** alrácsban válassza az **Új szerződéssor-részlet** lehetőséget. Megnyílik egy gyorslétrehozás csúszka. A következő mezők a **Szerződéssor részletei** lapon érhetők el.

| Mező | Hely | Ismertetés | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| **Leírás** | **Gyorslétrehozás** | Egy adott becslés leírása. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Tranzakcióosztály** | **Gyorslétrehozás** | A tranzakcióosztályok listája a projektalapú szerződéssor **Általános** fülön található. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Termék kiválasztása** | **Gyorslétrehozás** | Akkor érvényes, ha a tranzakcióosztály **Anyag**. Meghatározhatja, hogy a becsléssor a **Meglévő** (katalógus) termékhez vagy **Nem katalogizált** termékhez készült-e. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Termék** | **Gyorslétrehozás** | A termékkatalógus termékazonosítója. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Meglévő termék** lehetőséget választja. Az azonosító az értékesítési ár szerződésen szereplő projektárlistából való lekéréséhez használható. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Nem katalogizált termék** | **Gyorslétrehozás** | A termék nevének beírásához használt szövegmező. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Nem katalogizált** lehetőséget választja.| Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Szerepkör** | **Gyorslétrehozás** | Annak a személynek a szerepköre, aki ezt a munkát teljesíti, vagy ezt a költséget viseli. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez.|
| **Kategória** | **Gyorslétrehozás** | A munka vagy a költség kategóriája. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez.|
| **Kezdő dátum** | **Gyorslétrehozás** | A munka kezdődátuma. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Befejező dátum** | **Gyorslétrehozás** | A munka befejező dátuma. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Erőforrás-kezelő vállalat** | **Gyorslétrehozás** | Az az erőforrás-kezelő vállalat vagy jogi személy, aki ezt a költséget beszedi, és biztosítja a munkához szükséges erőforrást. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott és az önköltségi ár lekéréséhez használt költséghez. |
| **Erőforrás-kezelő részleg** | **Gyorslétrehozás** | Az az erőforrásegység, amely ezt a költséget beszedi, és biztosítja a munkához szükséges erőforrást. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott és az önköltségi ár lekéréséhez használt költséghez. |
| **Egységütemezés** | **Gyorslétrehozás** | A munka, a termék vagy a költség egységcsoportja. Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak. Például a *mérföld* és a *kilométer (km)* olyan egység, amely a távolságot leíró egységek csoportjához tartozik. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Kiszerelés** | **Gyorslétrehozás** | A munka, a termék vagy a költség egysége. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Mennyiség** | **Gyorslétrehozás** | A munka, a termék vagy a költség mennyisége. | Ez az érték alapértelmezés szerint a kapcsolódó szerződéssor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| **Egységár** | **Gyorslétrehozás** | A munkát végző szerepkör számlázási aránya, a termék egységára, vagy a termék- vagy költségkategória értékesítési ára. Az **Idő** alapértelmezett értéke a projektárlista kezdő dátumra vonatkozó szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul. A **Költségek** esetén ennek a mezőnek az alapértelmezett beállítása a projekt árlistájában szereplő tranzakciós kategória árbeállításából származik, amely a kezdő dátumra vonatkozik. Ha a tranzakciós kategória árképzési módja nem **egységár**, nincs alapértelmezett érték, és ez a mező üresen marad. Termékek esetén ez a mező alapértelmezett értéke a projektárlista árlistán lévő **Árlistaelemen** alapul, amely a kezdő dátumra vonatkozik.| A munkát végző szerepkör költségaránya, vagy a költségkategória kiszerelésenkénti költsége, vagy a termék kiszerelésköltsége. Az **Idő** alapértelmezett értéke a szerződő kiszereléshez csatolt önköltségi tárlista szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul, amely a kezdő dátumra vonatkozik. A **Költségek** esetén ennek a mezőnek az alapértelmezett beállítása a szerződő kiszereléshez csatolt önköltségi árlista kategória árlistáján alapszik, amely a kezdő dátumra vonatkozik. Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad. A termékek esetén ennek a mezőnek az alapértelmezett beállítása a szerződő kiszereléshez csatolt önköltségi árlistalista **Árlistaelem** soron alapszik, amely a kezdő dátumra vonatkozik.|
| **Becsült adó** | **Gyorslétrehozás** | A munkára vagy költségre vonatkozó becsült adó a felhasználó által bevitt adatként. | &nbsp; |
| **Mennyiség** | **Gyorslétrehozás** | Ebben a mezőben az érték hozzáadható, ha a **Mennyiség** és az **Ár** mezőket üresen hagyja. Ha a **Mennyiség** és az **Ár** mezők ki vannak töltve, az **Összeg** mező csak olvasható, és a program **(Mennyiség \* Egységár) + Adóként** kerül kiszámításra. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Az árak frissítése a szerződéssorok részleteiben

Ha módosítja a szerződéshez vagy a szerződő egység önköltségi árlistájához tartozó projektárlista árait, akkor az egyes szerződéssorok részleteiben szereplő árakat frissítheti, hogy azok tükrözzék a változást. A **Szerződés** lapon válassza az **Újraszámolás** lehetőséget. Egy figyelmeztetés tájékoztatja Önt arról, hogy a szerződés összes szerződéssorának ára alaphelyzetbe állt. Válassza az **Igen** lehetőséget, ha frissíteni szeretné az értékesítési és a költség szerződéssor-részleteinek árát is.

## <a name="access-contract-line-details-for-cost"></a>A szerződéssor részleteinek elérése költséghez

A **Szerződéssor részletei** lapon jelöljön ki egy sort a rácsban, hogy megjelenítse a műveleteket az alrács eszköztárán. Az elrács eszköztár első művelete a **Költség részleteinek megnyitása**. Ha meg szeretné tekinteni a kapcsolódó költségarányt és összeget ehhez a szerződéssorhoz akkor válassza a **Költség részleteinek megnyitása** lehetőséget. 

> [!NOTE]
> Ha módosítja a beszerzési vállalat, a beszerzési egység, a mennyiség, a dátum, a szerepkör vagy a kategória értékeit a **Költséghez** tartozó szerződéssorok részleteiben, azzal módosítja a kapcsolódó értékeket az **Értékesítés** szerződéssor-részleteiben is.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>A szerződéssorok részleteinek pénzneme a költségre és az értékesítésre vonatkozóan

Az **Értékesítés** szerződéssor részletei az alapértelmezett pénznemet határozzák meg a projektárlistából, amely a szerződéssor részlet kezdési dátumán érvényes.

A **Költség** szerződéssor részletei az alapértelmezett pénznemet határozzák meg a szerződés szerződő egységének árlistájából, amely a **Költséghez** kapcsolódó szerződéssor részlet kezdési dátumán érvényes.

A jövedelmezőségi számítások átalakítják a **Költség** és **Értékesítés** szerződéssor részleteinek összegét annak a környezetnek az alappénznemére, amelybe jelenteni kell a szerződés teljes tényleges és becsült árréseit.

> [!NOTE]
> A pénznem kerekítési hibái és a módosított árrések azért fordulhatnak elő, mert hiányoznak a dátumon érvényes átváltási árfolyamok. Ezeket a számításokat csak projektszerződéseken használja, mivel ezek csak becslések, és nem való tényleges törvényi vagy egyéb jelentésekre, amelyek nagyobb pontosságot igényelnek az árfolyamok kerekítéséhez és a dátumhatékonyságra való figyelemfelhíváshoz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
