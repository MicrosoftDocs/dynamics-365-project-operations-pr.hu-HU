---
title: Projektalapú árajánlatsor becslése
description: Ez a témakör azt ismerteti, hogyan lehet becslést létrehozni egy projektalapú árajánlatsorban.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 20a318c9f288b08a0984f9c29dced05997622f47
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003319"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektalapú árajánlatsor becslése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektalapú árajánlatsor olyan részletekkel rendelkezik, amelyek segítenek az árajánlatsor elkészítésére fordított munka költségének és potenciális bevételének becslésében.

A projektalapú árajánlatsor becsléséhez válassza ki a projektalapú árajánlatsoron az **Árajánlatsor részletei** lapot. A becsléseket kétféleképpen lehet létrehozni egy projektalapú árajánlatsorban:

- A becslés manuális létrehozása közvetlenül az árajánlatsorban az árajánlatsor részleteinek használatával. 
- Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekten az árajánlatsorhoz. A projektterv becsült értékének az árajánlatsorba való importálásának folyamata a megadott adatok alapján engedélyezve lesz.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Projektbecslések létrehozása közvetlenül egy projektalapú árajánlatsoron

Ha egy projektalapú árajánlatsor becslését szeretné létrehozni, akkor válassza ki az **Árajánlatsor részletei** lapot. Az ezen a lapon létrehozott sor összesíti az árajánlatsorhoz tartozó ajánlati értéket. 

Az ajánlati sor részleteinek létrehozásához az **Árajánlatsor részletek** alrácsán jelölje ki az **Árajánlati sorrészletek** elemet. Megnyílik egy gyorslétrehozási csúszka. Az alábbi tábla részletezi az **Árajánlatsor részletei** lap mezőit és azt, hogy az értékek hogyan befolyásolják a működést.

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Ismertetés | Gyorslétrehozás | Egy adott becslés leírása. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Tranzakció osztálya | Gyorslétrehozás | Ez a legördülő lista a projektalapú árajánlatsor **Általános** lapján szereplő tranzakcióosztályokat tartalmazza.  | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Termék kiválasztása | Gyorslétrehozás | Akkor érvényes, ha a tranzakcióosztály **Anyag**. Meghatározhatja, hogy a becsléssor a **Meglévő** (katalógus) termékhez vagy **Nem katalogizált** termékhez készült-e. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Termék | Gyorslétrehozás | A termékkatalógus termékazonosítója. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Meglévő** lehetőséget választja. Az azonosító az értékesítési ár az árajánlaton szereplő projektárlistából való lekéréséhez használható. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Nem katalogizált termék | Gyorslétrehozás | A termék nevének beírásához használt szövegdoboz. Ez a mező csak akkor érhető el, ha a **Termék kiválasztása** mezőben a **Nem katalogizált** lehetőséget választja.| Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Szerepkör | Gyorslétrehozás | Annak a személynek a szerepköre, aki elvégzi ezt a munkát, vagy benyújtja ezt a költséget. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kategória | Gyorslétrehozás | A munka vagy a költség kategóriája. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kezdő dátum | Gyorslétrehozás | A munka kezdődátuma. | Ez a mező alapértelmezés szerint az árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Befejező dátum | Gyorslétrehozás | A munka befejező dátuma. | Ez a mező alapértelmezés szerint az árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Erőforrás-kezelő részleg | Gyorslétrehozás | Az az erőforrásegység, amely ezt a költséget be fogja szedni, és biztosítani fogja a munkához szükséges erőforrást. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott és az önköltségi ár lekéréséhez használt költséghez. |
| Egységütemezés | Gyorslétrehozás | A munka, a termék vagy a költség egységcsoportja. Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak. Például a mérföld és a kilométer olyan egység, amely a távolságot leíró egységek csoportjához tartozik. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Kiszerelés | Gyorslétrehozás | A munka, a termék vagy a költség egysége. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Mennyiség | Gyorslétrehozás | A munka, a termék vagy a költség mennyisége. | Ez az érték alapértelmezés szerint a kapcsolódó árajánlatsor részletéhez kapcsolódik az automatikusan létrehozott költséghez. |
| Egységár | Gyorslétrehozás |A munkát végző szerepkör számlázási aránya, a termék egységára, vagy a termék- vagy költségkategória értékesítési ára. A mező alapértelmezett értéke, az **Idő** a projektárlista kezdő dátumra vonatkozó szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul. A **Költségek** esetén az alapértelmezett beállítása a projekt árlistájában szereplő tranzakciós kategória árbeállításából származik, amely a kezdő dátumra vonatkozik. Ha a tranzakciókategória árképzési módszere nem kiszerelésenkénti ár, akkor nincs alapértelmezett érték, és ez a mező üresen marad. Termékek esetén ez az alapértelmezett érték a projektárlista árlistán lévő **Árlistaelemen** alapul, amely a kezdő dátumra vonatkozik.| A munkát végző szerepkör költségaránya, a költségkategória kiszerelésenkénti költsége, vagy a termék kiszerelésköltsége. A mező alapértelmezett értéke, az **Idő** a projektárlista kezdő dátumra vonatkozó szerepkör ársorában szereplő árképzési dimenzióértékek kombinációján alapul. A **Költségek** esetén az alapértelmezett beállítása a projekt árlistájában szereplő tranzakciós kategória árbeállításából származik, amely a kezdő dátumra vonatkozik. Ha a tranzakciókategória árképzési módszere nem kiszerelésenkénti ár, akkor nincs alapértelmezett érték, és ez a mező üresen marad. Termékek esetén ez az alapértelmezett érték a projektárlista árlistán lévő **Árlistaelemen** alapul, amely a kezdő dátumra vonatkozik.|
| Becsült adó | Gyorslétrehozás | A munkára vagy kiadásra vonatkozó becsült adót kézzel is megadhatja. | Ennek a mezőnek nincs későbbi hatása. |
| Mennyiség | Gyorslétrehozás | Az adatokat manuálisan is beviheti ebbe a mezőbe, ha a **Mennyiség** és az **Ár** mező üresen marad. Ha ezek a mezők nem üresek, akkor ez a mező írásvédett lesz, és számítása a következőképp történik (Mennyiség \* Egységár) + Adó. | Ennek a mezőnek nincs későbbi hatása. |


## <a name="update-prices-on-quote-line-details"></a>Árak frissítése az árajánlatsor részleteiben

Ha módosította az árakat az árajánlathoz csatolt projektárlistában vagy a szerződéskötési kiszerelés önköltségi árlistájában, akkor válassza az **Újraszámítás** lehetőséget az **Árajánlat** lapon, hogy frissítse az egyes ajánlatsorok adatait, és ezzel tükrözze ezt a változást. Ha kiválasztja az **Újraszámítás** lehetőséget, akkor megjelenik egy figyelmeztetés, hogy az árajánlatsorban az árajánlat sorainak árai alaphelyzetbe állnak. Válassza az **Igen** lehetőséget, ha az mind az értékesítés, mind a költség árajánlatsor-részletek árait frissíteni szeretné.

## <a name="access-quote-line-details-for-cost"></a>A költség árajánlatsor-részleteinek elérése

Az **Ajánlatsor részletei** lapon jelöljön ki egy sort a rácsban, hogy lehetővé tegyen bizonyos műveleteket az alrács eszköztárán. Az alrács eszköztár első művelete, amikor az ajánlati sor részletei be vannak jelölve a **Költség részleteinek megnyitása**. Válassza a **Költség részleteinek megnyitása** lehetőséget az árajánlatsorhoz kapcsolódó költségarány és -összeg megtekintéséhez.

> [!NOTE]
> Az erőforrásbiztosító egység, mennyiség, dátumok, szerep vagy kategória értékek módosítása a költség árajánlatsor-részletein módosítani fogja az értékesítések árajánlatsor-részleteinek megfelelő értékét.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Az költség és értékesítések ajánlatsor-részleteinek pénzneme

Az értékesítések árajánlatsor-részleteinek pénzneme az árajánlatsor-részlet kezdő dátuma esetében érvényes projektárlistából veszi az alapértelmezett értékét.

A költség árajánlatsor-részleteinek pénzneme az költség árajánlatsor-részletének kezdő dátuma esetében érvényes árajánlat szerződési egységének árlistájából veszi az alapértelmezett értékét.

A jövedelmezőségi számítások átváltják a költség és értékesítések árajánlatsor-részleteiben szereplő összeget a környezet alappénznemére az árajánlat teljes becsült hasznának jelentéséhez.

> [!MEGJEGYZÉS
> > A pénznem kerekítési hibái és a módosított árrések azért fordulhatnak elő, mert hiányoznak a dátumon érvényes átváltási árfolyamok. Ezeket a számításokat csak projektszerződéseken használja, mivel ezek csak becslések, és nem való tényleges törvényi vagy egyéb jelentésekre, amelyek nagyobb pontosságot igényelnek az árfolyamok kerekítéséhez és a dátumhatékonyságra való figyelemfelhíváshoz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
