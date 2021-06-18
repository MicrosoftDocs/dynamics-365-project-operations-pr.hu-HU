---
title: Projekt árajánlatsorának becslése
description: Ez témakör a projekt árajánlatsorának becslésének létrehozásáról nyújt tájékoztatást.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: adb5a7f113b15abd2fe7364fa9b592d2c02db389
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000709"
---
# <a name="estimate-a-project-quote-line"></a>Projekt árajánlatsorának becslése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektalapú árajánlatsor olyan részletekkel rendelkezik, amelyek segítenek az árajánlatsor elkészítésére fordított munka költségének és potenciális bevételének becslésében.

Projektalapú árajánlatsor becsléséhez az árajánlat sorban válassza az **Árajánlatsor részletei** fület. A projektalapú árajánlatsorok becslésének két módja van:

   - A becslés manuális létrehozása közvetlenül az árajánlatsorban az árajánlatsor részleteinek használatával. 
   - Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekten az árajánlatsorhoz. A projektterv becsült értékének az árajánlatsorba való importálásának folyamata a megadott adatok alapján engedélyezve lesz.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Projektbecslések létrehozása közvetlenül egy projektalapú árajánlatsoron

Ahhoz, hogy közvetlenül a projektalapú árajánlatsoron tudjon becsléseket létrehozni, kövesse az alábbi lépéseket:

1. Ha egy projektalapú árajánlatsor becslését szeretné létrehozni, akkor válassza ki az **Árajánlatsor részletei** lapot. Az ezen a lapon létrehozott sor összesíti az árajánlatsorhoz tartozó ajánlati értéket. 
2. Az ajánlati sor részleteinek létrehozásához az **Árajánlatsor részletek** alrácsán jelölje ki az **Árajánlati sorrészletek** elemet. Megnyílik egy gyorslétrehozási csúszka. Az **Árajánlatsor** lap következő mezői.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Ismertetés | Gyorslétrehozás | Egy adott becslés leírása. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Tranzakció osztálya | Gyorslétrehozás | Ez a legördülő lista a projektalapú árajánlatsor **Általános** lapján szereplő tranzakciós osztályokat tartalmazza.  | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Termék kiválasztása | Gyorslétrehozás | Akkor érvényes, ha a tranzakcióosztály **Anyag**. Meghatározhatja, hogy a becsléssor a **Meglévő** (katalógus) termékhez vagy **Nem katalogizált** termékhez készült-e. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Termék | Gyorslétrehozás | A termékkatalógus termékazonosítója. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Meglévő** lehetőséget választja. Az azonosító az értékesítési ár az árajánlaton szereplő projektárlistából való lekéréséhez használható. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Nem katalogizált termék | Gyorslétrehozás | A szövegdoboz, amelybe a termék nevét kell beírni. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Nem katalogizált** lehetőséget választja.| Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Szerepkör | Gyorslétrehozás | Annak a személynek a szerepköre, aki elvégzi ezt a munkát, vagy benyújtja ezt a költséget. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kategória | Gyorslétrehozás | A munka vagy a költség kategóriája. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kezdő dátum | Gyorslétrehozás | A munka kezdődátuma. | Ez a mező alapértelmezés szerint az árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Befejező dátum | Gyorslétrehozás | A munka befejező dátuma. | Ez a mező alapértelmezés szerint az árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Erőforrás-kezelő vállalat | Gyorslétrehozás | Az az erőforrás-kezelő vállalat vagy jogi személy, aki ezt a költséget beszedi, és biztosítja a munkához szükséges erőforrást. | Az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott és az önköltségi ár lekéréséhez használt költséghez. |
| Erőforrás-kezelő részleg | Gyorslétrehozás | Az az erőforrásegység, amely ezt a költséget beszedi, és biztosítja a munkához szükséges erőforrást. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott és az önköltségi ár lekéréséhez használt költséghez. |
| Egységütemezés | Gyorslétrehozás | A munka, a termék vagy a költség egységcsoportja. Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak. Például a mérföld és a kilométer olyan egység, amely a távolságot leíró egységek csoportjához tartozik. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kiszerelés | Gyorslétrehozás | A munka, a termék vagy a költség egysége. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Mennyiség | Gyorslétrehozás | A munka, a termék vagy a költség mennyisége. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Egységár | Gyorslétrehozás |A munkát végző szerepkör számlázási aránya, a termék egységára, vagy a termék- vagy költségkategória értékesítési ára. Az **Idő** alapértelmezett értéke a projektárlista kezdő dátumra vonatkozó szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul. A **Költségek** esetén az alapértelmezett beállítása a projekt árlistájában szereplő tranzakciós kategória árbeállításából származik, amely a kezdő dátumra vonatkozik. Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad. Termékek esetén ez a mező alapértelmezett értéke a projektárlista árlistán lévő **Árlistaelemen** alapul, amely a kezdő dátumra vonatkozik.| A munkát végző szerepkör költségaránya, a költségkategória kiszerelésenkénti költsége, vagy a termék kiszerelésköltsége. Az **Idő** alapértelmezett értéke a szerződő kiszereléshez csatolt önköltségi tárlista szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul, amely a kezdő dátumra vonatkozik. A költségek esetén az alapértelmezett beállítása a szerződő kiszereléshez csatolt önköltségi árlista kategória árlistáján alapszik, amely a kezdő dátumra vonatkozik. Ha a tranzakciókategória árképzési módszere nem kiszerelésenkénti ár, akkor nincs alapértelmezett érték, és ez a mező üresen marad. A termékek esetén ennek a mezőnek az alapértelmezett beállítása a szerződő kiszereléshez csatolt önköltségi árlistalista **Árlistaelem** soron alapszik, amely a kezdő dátumra vonatkozik.|
| Becsült adó | Gyorslétrehozás | A munkára vagy kiadásra vonatkozó becsült adót kézzel is megadhatja. | Ennek a mezőnek nincs későbbi hatása. |
| Mennyiség | Gyorslétrehozás | Az adatokat manuálisan is beviheti ebbe a mezőbe, ha a **Mennyiség** és az **Ár** mező üresen marad. Ha ezek a mezők nem üresek, akkor ez a mező írásvédett lesz, és számítása a következőképp történik (Mennyiség \* Egységár) + Adó. | Ennek a mezőnek nincs későbbi hatása. |

## <a name="update-prices-on-quote-line-details"></a>Árak frissítése az árajánlatsor részleteiben

Ha megváltoztatta az árakat az árajánlathoz mellékelt projektárlistán vagy a szerződési egység önköltségiár-listáján, akkor az **Árajánlat** oldalon az **Újraszámolás** lehetőségre kattinthat, és az egyes árajánlatsor-részletekben szereplő árakat frissítheti, hogy azok tükrözzék ezt a változást. Ha kiválasztja az **Újraszámítás** lehetőséget, akkor megjelenik egy figyelmeztetés, hogy az árajánlatsorban az árajánlat sorainak árai alaphelyzetbe állnak. Válassza az **Igen** lehetőséget, ha az mind az értékesítés, mind a költség árajánlatsor-részletek árait frissíteni szeretné.

## <a name="access-quote-line-details-for-cost"></a>A költség árajánlatsor-részleteinek elérése

A költség áeajánlatsor részleteinek eléréséhez kövesse az alábbi lépéseket:

1. Az **Árajánlatsor részletei** fülön jelöljön ki egy sort a rácsban, hogy engedélyezze a műveleteket az alrács eszköztárán. 
2. Válassza a **Költség részleteinek megnyitása** lehetőséget az árajánlatsorhoz kapcsolódó költségarány és -összeg megtekintéséhez.

> [!NOTE]
> Az erőforrásbiztosító egység, mennyiség, dátumok, szerep vagy kategória értékek módosítása a költség árajánlatsor-részletein módosítani fogja az értékesítések árajánlatsor-részleteinek megfelelő értékét.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Az költség és értékesítések ajánlatsor-részleteinek pénzneme

Az értékesítéshez tartozó árajánlatsorban szereplő pénznem abból a projektárlistából származik, amely az árajánlatsor részleteinek kezdő dátumára vonatkozik.

A költséghez tartozó árajánlatsorban szereplő pénznem abból az árajánlat szerződő kiszerelésének árlistából származik, amely az árajánlatsor részleteinek kezdő dátumára vonatkozik.

> [!NOTE]
> A jövedelmezőségi számítások átváltják a költség és értékesítések árajánlatsor-részleteiben szereplő összeget a környezet alappénznemére az árajánlat teljes becsült hasznának jelentéséhez. A pénznem kerekítési hibái és a módosított árrések azért fordulhatnak elő, mert hiányoznak a dátumon érvényes átváltási árfolyamok. Ezeket a számításokat csak projektárajánlatokon használja, mivel ezek csak becslések, és nem való tényleges törvényi vagy egyéb jelentésekre, amelyek nagyobb pontosságot igényelnek az árfolyamok kerekítéséhez és a dátumhatékonyságra való figyelemfelhíváshoz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
