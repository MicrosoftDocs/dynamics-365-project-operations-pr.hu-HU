---
title: Projektalapú árajánlatsor becslése
description: Ez a témakör azt ismerteti, hogyan lehet becslést létrehozni egy projektalapú árajánlatsorban.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180375"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektalapú árajánlatsor becslése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektalapú árajánlatsor olyan részletekkel rendelkezik, amelyek segítenek az árajánlatsor elkészítésére fordított munka költségének és potenciális bevételének becslésében.

A projektalapú árajánlatsor becsléséhez válassza ki a projektalapú árajánlatsoron az **Árajánlatsor részletei** lapot. A becsléseket kétféleképpen lehet létrehozni egy projektalapú árajánlatsorban:

- A becslés manuális létrehozása közvetlenül az árajánlatsorban az árajánlatsor részleteinek használatával 
- Hozzon létre egy projektet és egy projekttervet, majd társítsa a projektet és a feladatokat a projekten az árajánlatsorhoz. A projektterv becsült értékének az árajánlatsorba való importálásának folyamata a megadott adatok alapján engedélyezve lesz.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Projektbecslések létrehozása közvetlenül egy projektalapú árajánlatsoron

Ha egy projektalapú árajánlatsor becslését szeretné létrehozni, akkor válassza ki az **Árajánlatsor részletei** lapot. Az ezen a lapon létrehozott sor összesíti az árajánlatsorhoz tartozó ajánlati értéket. 

Az ajánlati sor részleteinek létrehozásához az **Árajánlatsor részletek** alrácsán jelölje ki a **+ új ajánlati sorrészletek** elemet. Megnyílik egy gyorslétrehozási csúszka. Az **Árajánlatsor** űrlap következő mezői:

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Adatfolyam leírása | Gyorslétrehozás | Egy adott becslés leírása. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Tranzakció osztálya | Gyorslétrehozás | Ez a legördülő lista a projektalapú árajánlatsor **Általános** lapján szereplő tranzakciós osztályokat tartalmazza.  | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Szerepkör | Gyorslétrehozás | Az a személy, aki ezt a munkát végrehajtja, vagy akinél ez a kiadás felmerül. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Kategória | Gyorslétrehozás | A munka vagy kiadás kategóriája. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Kezdő dátum | Gyorslétrehozás | A munka kezdő dátuma. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Befejező dátum | Gyorslétrehozás | A munka záró dátuma. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Erőforrás-kezelő részleg | Gyorslétrehozás | A beszerzési egység, amelynél felmerül ez a költség, és biztosítja az erőforrást az azon végzett munkához. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. Ez a mező az önköltségi ár beolvasása esetén is használatos. |
| Egységütemezés | Gyorslétrehozás | A munka vagy kiadás egységcsoportja. Az egységek egy egységütemezéshez vagy egységcsoporthoz tartoznak. Például a mérföldek és kilométerek távolságot leíró egységek egy csoportjába tartozik. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Kiszerelés | Gyorslétrehozás | A munka vagy kiadás egysége. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Mennyiség | Gyorslétrehozás | A munka vagy kiadás mennyisége. | Ez a mező az automatikusan létrehozott költség kapcsolódó árajánlatsor-részletére áll be. |
| Egységár | Gyorslétrehozás | A költségkategóriára vonatkozó munkát végrehajtó szerepkör számlázási ára vagy az értékesítési ár. Ez a mező alapértelmezés szerint arra az időre áll be, amely a szerepkör és az erőforrásbiztosító egység kombinációja alapján kezdő dátumként érvényes a projekt árlistájában. A kiadások esetében ez a mező alapértelmezés szerint a kezdő dátumnál érvényben lévő, a projekt árlistájában szereplő tranzakciós kategóriához tartozó árból kerül beállításra. Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad. | A költségkategóriára vonatkozó munkát végrehajtó szerepkör költségára vagy az egységár. Ez a mező alapértelmezés szerint arra az időre áll be, amely a szerepkör és az erőforrásbiztosító egység kombinációja alapján kezdő dátumként érvényes az árajánlat árlistájához tartozó szerződő egység áránál. A kiadások esetében ez a mező alapértelmezés szerint a kezdő dátumnál érvényben lévő, a szerződő egység költség-árlistájában szereplő tranzakciós kategóriához tartozó árból kerül beállításra. Ha a tranzakciós kategória árképzési módja nem egységár, nincs alapértelmezett érték, és ez a mező üresen marad. |
| Becsült adó | Gyorslétrehozás | A munkára vagy kiadásra vonatkozó becsült adót kézzel is megadhatja. | Ennek a mezőnek nincs későbbi hatása. |
| Mennyiség | Gyorslétrehozás | Az adatokat manuálisan is beviheti ebbe a mezőbe, ha a **Mennyiség** és az **Ár** mező üresen marad. Ha ezek a mezők nem üresek, akkor ez a mező írásvédett lesz, és számítása a következőképp történik (Mennyiség \* Egységár) + Adó. | Ennek a mezőnek nincs későbbi hatása. |

## <a name="update-prices-on-quote-line-details"></a>Árak frissítése az árajánlatsor részleteiben

Ha megváltoztatta az árakat az árajánlathoz mellékelt projektárlistán vagy a szerződési egység önköltségiár-listáján, akkor az **Árajánlat** oldalon az **Újraszámolás** lehetőségre kattinthat, és az egyes árajánlatsor-részletekben szereplő árakat frissítheti, hogy azok tükrözzék ezt a változást. Amikor az **Újraszámolás** lehetőséget választja, egy figyelmeztetés jelenik meg, hogy az árajánlatban szereplő összes árajánlatsor árajánlatsor-részleteihez tartozó árak alaphelyzetbe kerülnek. Válassza az **Igen** lehetőséget, ha az mind az értékesítés, mind a költség árajánlatsor-részletek árait frissíteni szeretné.

## <a name="access-quote-line-details-for-cost"></a>A költség árajánlatsor-részleteinek elérése

Az **Ajánlatsor részletei** lapon jelöljön ki egy sort a rácsban, hogy lehetővé tegyen bizonyos műveleteket az alrács eszköztárán. Az alrács eszköztár első művelete, amikor az ajánlati sor részletei be vannak jelölve a **Költség részleteinek megnyitása**. Válassza a **Költség részleteinek megnyitása** lehetőséget az árajánlatsorhoz kapcsolódó költségarány és -összeg megtekintéséhez.

> [!NOTE]
> Az erőforrásbiztosító egység, mennyiség, dátumok, szerep vagy kategória értékek módosítása a költség árajánlatsor-részletein módosítani fogja az értékesítések árajánlatsor-részleteinek megfelelő értékét.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Az költség és értékesítések ajánlatsor-részleteinek pénzneme

Az értékesítések árajánlatsor-részleteinek pénzneme az árajánlatsor-részlet kezdő dátuma esetében érvényes projektárlistából veszi az alapértelmezett értékét.

A költség árajánlatsor-részleteinek pénzneme az költség árajánlatsor-részletének kezdő dátuma esetében érvényes árajánlat szerződési egységének árlistájából veszi az alapértelmezett értékét.

A jövedelmezőségi számítások átváltják a költség és értékesítések árajánlatsor-részleteiben szereplő összeget a környezet alappénznemére az árajánlat teljes becsült hasznának jelentéséhez.

Ennek következtében a pénznemek kerekítési hibái és a nyereségek módosulhatnak a tényleges átváltási árfolyamok hiánya miatt. Ezeket a számításokat a projektárajánlatok esetében csak közelítésként használja és nem a tényleges törvényi vagy egyéb jelentéskészítéshez, amely nagyobb kerekítési pontosságot vagy az átváltási árfolyamok érvényességének ismeretét követeli meg.
