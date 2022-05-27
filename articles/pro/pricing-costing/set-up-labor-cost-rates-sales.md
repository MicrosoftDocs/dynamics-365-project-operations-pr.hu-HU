---
title: A munka költségarányának beállítása – Lite
description: Ez a témakör a Project Operations munkabérköltségeire vonatkozó díjak beállításával kapcsolatban tartalmaz tájékoztatást.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 01e3b41ca5c8fcc9146186873e0f44daad020c6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575675"
---
# <a name="set-up-labor-cost-rates---lite"></a>A munka költségarányának beállítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Minden árlistához tartalmaz egy sor munkadíj (szerepkörárak), amelyek megfelelnek az árlista tartalmának és esedékességi dátumának.

1. Hozzon létre egy árlistát, és a **szerepkörár** lap Alrács területén válassza az **Új szerepkör** lehetőséget.
2. A **gyors létrehozás** lapon jelölje ki a szerepkört és a szervezeti egységet.
3. Adja meg a többi kötelező mezők adatait.

Az alábbi táblázat néhány olyan mezőt tartalmaz, amelyek fontosak a önköltségi árlistán a munkadíjak létrehozásakor.

| Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- | --- |
| Szerepkör | **Általános** lap és a **Gyorslétrehozás** oldalak | Válassza ki a költségdíjhoz tartozó szerepkört. | A bejövő becslésen vagy a tényleges értéken szereplő szerepkört ezzel a sorral kell összehangolni a szerepkör alapértelmezett költségének meghatározásához. |
| Erőforrás-kezelő részleg | **Általános** lap és a **Gyorslétrehozás** oldalak | Válassza ki azt a szervezeti egységet vagy részleget a vállalattól, ahol ezt a szerepkört használni kívánja. Például a Fabrikam India robotikai divíziójának fejlesztője vagy a Fabrikam USA szoftveres divíziójának fejlesztője. | A bejövő becslésen vagy a tényleges értéken szereplő erőforrás-kezelő egységet ezzel a sorral kell összehangolni a szerepkör alapértelmezett költségének meghatározásához. |
| Ár | **Általános** lap és a **Gyorslétrehozás** oldalak | Állítsa be a szerepkör, az erőforrás-kezelő vállalat és az erőforrás-kezelő egység kombinációjának önköltségi arányát. Például a Fabrikam India fejlesztője 1000 INR-be kerül vagy a Fabrikam USA egyik fejlesztője 150 USD-be kerül. | Az ár azt a költséget adja meg, amely a bejövő becslés vagy a tényleges sor egységnyi költségére érvényes az **Idő** tranzakciós osztályban. |
| Pénznem | **Általános** lap és a **Gyorslétrehozás** oldalak | A pénznem értéke alapértelmezés szerint az önköltségi árlista fejlécében szereplő pénznemből származik, de felülírható. Például a Fabrikam India fejlesztőinek ára 1000 INR. Egy fejlesztő a Fabrikam USA-nál 150 USD-be kerül. | Ez a pénznem megadja a bejövő tényleges költségsor egységnyi költségére érvényes értéket az **Idő** tranzakciós osztályban. A projekt becslésében a pénznem értékét a program a projekt pénznemére váltja át, és a becslés időfázisos nézetében jelenik meg. |
| Egységütemezés | **Általános** lap és a **Gyorslétrehozás** oldalak | Az egység ütemezése alapértelmezés szerint Idő, és nem módosítható a szerepkörár entitáson, mert a rendszer időegységekkel kifejezett árfolyamot alkalmaz. | Ez nem befolyásolja az alsó szinteket. |
| Kiszerelés | **Általános** lap és a **Gyorslétrehozás** oldalak | A pénznem értéke alapértelmezés szerint az önköltségi árlista fejlécében szereplő **Időegység** értékéből származik. Az érték felülbírálható. Például a Fabrikam India fejlesztőinek ára 1000 INR **indiai naponként**. Egy fejlesztő a Fabrikam USA-nál 150 USD-be kerül **amerikai naponként**. | A rendszer az egységek rendszerét és a alapegységekre való átváltást használja az egységnyi költség kiszámításához, amely meghatározza az alapértelmezett egységárat a bejövő becslések vagy a tényleges sorok esetében. Például a becslés 10 **indiai nap** mennyiségű munkára vonatkozik egy indiai fejlesztőnél, és az egység, **indiai nap** meghatározása szerint 10 órát jelent. A becslési sor költségszámításakor az alkalmazás a becslésben a következőre számítja ki az egységköltséget: 1000 INR/10 óra = 100 INR per óra, amelyet USD-re váltunk át, és az egységnyi költségként jelennek meg a **projekt becslései** oldalon. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>A divízión vagy jogi személyen kívüli erőforrásokra vonatkozó árak és költségek átadása

A projektalapú vállalatokban gyakori a különböző jogi személyek vagy részlegek alkalmazottainak használata projekteken. Egy projektet elvégezhet egy jogi személy, de a projekten dolgozó alkalmazottak vagy tanácsadók jöhetnek ugyanabból a jogi személyből vagy egy másikból, vagy a kettő kombinációjából. A Dynamics 365 Project Operations alkalmazásban ban a projekt szállítását birtokló jogi személy a **Tulajdonos vállalat**, a szállítást birtokló részleg pedig a **Szerződéskötési egység**. Az erőforrásokat biztosító egyéb jogi személyek az **Erőforrás-kezelő vállalatok**, és az erőforrásokat biztosító részlegek az **Erőforrás-kezelő egységek**. A legtöbb országban a vállalatoknak meg kell győződniük arról, hogy az erőforrás-kezelő jogi személy vagy részleg megterheli a tulajdonos vállalatot és a szerződő egységet az erőforrások használatáért.

A Fabrikam vállalatnak például biztosítania kell, hogy a Fabrikam India-Robotics rendelkezik egyeztetett költségdíjkártyával a Fabrikam US-Robotics vagy a Fabrikam UK-Robotics felé.

Egy fejlesztő a Fabrikam India-Roboticsnél $100-ba kerül, amikor kölcsönadják a Fabrikam US-Roboticsnak és $150, amikor kölcsönadta a Fabrikam UK-Roboticsnak.

### <a name="set-up-costs-for-outside-resources"></a>A külső erőforrások költségeinek beállítása

1. Hozzon létre egy önköltségi árlistát *Fabrikam US-Robotics költségdíjak* néven, és állítsa be a dátum effektív tartományát.
2. Az önköltségi ár listájában állítsa be a díjtételeket az alábbi táblázatban szereplő információk alapján. 

| Szerepkör | Erőforrás-kezelő vállalat | Erőforrás-kezelő részleg | Költségarány |
| --- | --- | --- | --- |
| Fejlesztői | Fabrikam India | Fabrikam India-Robotics | 100 dollár |
| Fejlesztői | Fabrikam-Fülöp-szigetek | Fabrikam-Fülöp-szigetek-Robotics | $90 |
| Fejlesztői | Fabrikam US | Fabrikam US-Robotics | $150 |

3. Ezt az önköltségi árlistát csatolja a Fabrikam US-Robotics szervezeti egységhez.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Transzferárazás beállítása az erőforrásra a megfelelő pénznemben 

A Project Operationsban az erőforrás-árazás bármilyen pénznemben megadható. A pénznem alapértelmezés szerint az árlista fejlécében látható, de módosítható.

A transzferár beállításának példája alapján az adatok a következőre módosíthatók:

A Fabrikam vállalatnak biztosítania kell, hogy a Fabrikam India-Robotics rendelkezik egyeztetett költségdíjjal a Fabrikam US-Robotics vagy a Fabrikam UK-Robotics felé.

Egy fejlesztő a Fabrikam India-Roboticsnél $5000 INR-ba kerül, amikor kölcsönadják a Fabrikam US-Roboticsnak és $5500 INR-ba, amikor kölcsönadta a Fabrikam UK-Roboticsnak.

A Fabrikam US-Robotics önköltségi árlistáján a költség aránya a következő módon fejezhető ki:

| Szerepkör | Erőforrás-kezelő vállalat | Költség |
| --- | --- | --- |
| Fejlesztői | Fabrikam India | 5000 INR |
| Fejlesztői | Fabrikam US | 115 USD |

A Fabrikam UK-Robotics önköltségi árlistáján a költség aránya a következő módon fejezhető ki:

| Szerepkör | Erőforrás-kezelő vállalat | Költség |
| --- | --- | --- |
| Fejlesztői | Fabrikam India | 5500 INR |
| Fejlesztői | Fabrikam UK | 115 GBP |

Az önköltségi árlistából több pénznemben is megadható a munkabérdíj. A projektre vonatkozó költségbecslés létrehozásakor a Project Operations ezeket a költségeket átminősíti a projekt pénznemére, és megjeleníti a felhasználó számára. Ha egy időbejegyzés jóváhagyása megtörténik, és a tényleges költség létrejön, akkor a tényleges költség ára a megfelelő szerepkörársor pénznemében történik az önköltségi árlista listáján. Egy projektnél az időpontokra vonatkozó tényleges költség több pénznemben is rögzíthető. Ha azonban a projekt szintjén a tényleges munkaköltséget összesítik, vagy összefoglalják, a Project Operations az összes munkaköltséget átváltja a projekt pénznemére, amelyet a felhasználó megtekinthet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]