---
title: Az értékesítési árak meghatározása a becslésekhez és a tényekhez
description: Ez a cikk arról nyújt tájékoztatást, hogyan határozzák meg a projektbecslések és -tényleges adatok értékesítési árait.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475187"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Az értékesítési árak meghatározása a becslésekhez és a tényekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az eladási árak meghatározásához a becslések és a tényleges adatok alapján a Microsoftnál Dynamics 365 Project Operations a rendszer először a dátumot és a pénznemet használja a bejövő becslésben vagy a tényleges környezetben az eladási árlista meghatározásához. Konkrétan a tényleges kontextusban a rendszer a **Tranzakció dátuma** mezőt használja annak meghatározására, hogy melyik árlista alkalmazható. A **bejövő becslés vagy tényleges tranzakciódátum-értékét** összehasonlítjuk az **árlistában szereplő Tényleges kezdés (Időzóna-független)** és **Tényleges befejezés (Időzóna-független)** értékekkel. Az eladási árlista meghatározása után a rendszer meghatározza az értékesítést vagy a számlakamatot.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Az értékesítési arányok meghatározása a tényleges és becsült sorokban az Idő számára

Az idő **kontextusának** becslése a következőkre utal:

- Idézet sor részletei az **Időhöz**.
- A szerződéssor részletei az **Időhöz**.
- Erőforrás-hozzárendelések egy projekten.

Az Idő **tényleges kontextusa** a következőkre utal:

- Bejegyzési és javítási naplósorok az **Időhöz**.
- Naplósorok, amelyek az időbevitel elküldésekor jönnek létre.
- Számlasor részletei az **Időhöz**. 

Az értékesítések árlistájának meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett számlakamat megadásához.

1. A rendszer megfelelteti a Szerepkör és **az** Erőforrásegység **mezők kombinációját az Idő** becsült vagy tényleges kontextusában **az árlistában szereplő szerepkör-ársorokkal**. Ez az egyezés feltételezi, hogy a használatra kész díjszabási dimenziókat használja a számlázási díjakhoz. Ha úgy konfigurálta a díjszabást, hogy az a Szerepkör **és** az Erőforrásegységtől **eltérő vagy azon felüli mezőkön alapuljon**, a mezők ezen kombinációja a megfelelő szerepkör-ársor lekérésére szolgál.
1. Ha a rendszer olyan szerepkör-ársort talál, amely a szerepkör **és** az erőforrásegység **kombinációhoz tartozó számlakamatot tartalmaz, akkor ezt a** számladíjat használja alapértelmezett számlázási rátaként.
1. Ha a rendszer nem tud megegyezni a Szerepkör **és** az Erőforrásegység **értékekkel, lekéri azokat a** szerepkör-ársorokat, amelyek a Szerepkör **mezőhöz egyező, az** **Erőforrásegység** mező null értékeit azonban tartalmazzák. Miután a rendszer megtalálta a megfelelő szerepkör-árrekordot, a rekordból származó számlakamat lesz az alapértelmezett számlázási ráta. Ez az egyeztetés a szerepkör **és** az erőforrásegység **relatív prioritásának** véletlenszerű konfigurációját feltételezi értékesítési árképzési dimenzióként.

> [!NOTE]
> Ha a Szerepkör **és** az **Erőforrásegység** mezők eltérő rangsorolását konfigurálja, vagy ha más dimenziói is vannak, amelyek magasabb prioritással rendelkeznek, az előző viselkedés ennek megfelelően változik. A rendszer lekéri azokat a szerepkör-árrekordokat, amelyek olyan értékeit tartalmazza, amelyek prioritási sorrendben egyeznek az egyes árképzési dimenziók értékével. Azok a sorok, amelyek null értékűek ezekhez a dimenziókhoz, az utolsók.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Az értékesítési arányok meghatározása a tényleges és a becsült sorokban a Költséghez

A költség **becsült kontextusa** a következőkre utal:

- Árajánlat sor részletei a **Költséghez**.
- A szerződéssor részletei a **Költséghez**.
- Egy projekt költségbecslési sorai.

A Költség **tényleges kontextusa** a következőkre vonatkozik:

- Bejegyzési és javítási naplósorok a **Költséghez**.
- Naplósorok, amelyek a költségbejegyzés elküldésekor jönnek létre.
- Számlasor részletei a **Költséghez**. 

Az értékesítések árlistájának meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett értékesítési egységár megadásához.

1. A rendszer megfelelteti a Költség becsült sorában **található Kategória** és **Egység** mezők kombinációját **az árlistán szereplő kategóriaársorokkal.**
1. Ha a rendszer olyan kategória-ársort talál, amely a Kategória **és** az Egység **kombináció értékesítési rátájával rendelkezik, akkor ezt az** értékesítési arányt használja alapértelmezett értékesítési arányként.
1. Ha a rendszer talál egyező kategória ársort, a rendszer az árképzési módszerrel adja meg az alapértelmezett eladási árat. Az alábbi táblázat a Project Operations költségárainak alapértelmezett viselkedését mutatja be.

    | Környezet | Árképzési mód | Alapértelmezett ár |
    | --- | --- | --- |
    | Becslés | Egységár | A kategória ársora alapján. |
    |        | Költségen | 0.00. |
    |        | Haszonkulcs feletti költség | 0.00. |
    | Tényleges | Egységár | A kategória ársora alapján. |
    |        | Költségen | A kapcsolódó tényleges költség alapján. |
    |        | Haszonkulcs feletti költség | A rendszer a kategória ársora által meghatározott felárat alkalmazza a kapcsolódó tényleges költség egységköltségi rátájára. |

1. Ha a rendszer nem tudja egyeztetni a **Kategória** és **az Egység** értéket, az értékesítési arány alapértelmezés szerint 0 **(nulla) értékre van állítva**.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Az értékesítési arányok meghatározása a tényleges és a becsült sorokban az anyaghoz

Az anyag **becsült kontextusa** a következőkre utal:

- Idézet sor részletei az **anyaghoz**.
- A Szerződéssor részletei az **anyaghoz**.
- Anyagbecslési sorok egy projekten.

Az Anyag **tényleges kontextusa** a következőkre utal:

- Bejegyzési és javítási naplósorok az **anyaghoz**.
- Naplósorok, amelyek az anyaghasználati napló elküldésekor jönnek létre.
- Számlasor részletei az **Anyaghoz**. 

Az értékesítések árlistájának meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett értékesítési egységár megadásához.

1. A rendszer egyezteti az Anyag **becsült sorának Termék** és **Egység** mezőinek **kombinációját** az árlista árlista cikksoraival.
1. Ha a rendszer olyan árlista-cikksort talál, amely értékesítési rátával rendelkezik a Termék és az **Egység** kombinációhoz, és ha az árképzési módszer **Pénznem összege**, akkor az árlista sorában megadott eladási árat **használja a rendszer.** 
1. Ha a **Termék** és **az Egység** mező értéke nem egyezés, vagy ha az árképzési módszer nem **azonos a Pénznem összegével**, az értékesítési arány alapértelmezés szerint 0 **-ra**(nulla) van állítva. Ez a viselkedés azért fordul elő, mert a Project Operations csak a **pénznemösszeg-árazási** módszert támogatja a projektben használt anyagokhoz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
