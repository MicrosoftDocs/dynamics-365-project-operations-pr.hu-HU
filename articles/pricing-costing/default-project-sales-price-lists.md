---
title: Alapértelmezett árlisták
description: Ez a cikk a Project Operations alapértelmezett értékesítési és önköltségi árlistáiról nyújt tájékoztatást.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410265"
---
# <a name="default-price-lists"></a>Alapértelmezett árlisták

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

## <a name="sales-price-lists"></a>Értékesítési árlisták

A Dynamics 365 Project Operations rendszerben minden projektajánlat és szerződés tartalmaz egy alapértelmezett értékesítési árlistát. 

### <a name="price-list-default-on-project-quotes"></a>Árlista alapértelmezései a projektajánlatokban
A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen alapértelmezett a projektajánlatban:

1. A rendszer megvizsgálja azokat az árlistákat, amelyek a partner projektárlistáihoz kapcsolódnak. 
1. Ha a fiókrekordhoz nem csatolnak projektárlistákat, a rendszer megvizsgálja a projektparaméterekhez csatolt eladási árlistákat, amelyek megegyeznek a projekt árajánlatának pénznemével.
1. Következő lépésként a rendszer ellenőrzi a projekt ajánlat hatályossági dátumának megfelelő hatályosságú árlistákat. Pontosan azt a dátumot, amikor az árajánlatot létrehozták.
1. Ha több árlista is van, amelyek a projekt ajánlatának dátumán hatályosak, akkor az összes árlista alapértelmezés szerint szerepel a projektajánlatban.
1. Ha a projektajánlat dátumára vonatkozóan nincs hatályos árlista, akkor a projektárajánlatban nem szerepel alapértelmezett árlista. A projekt ajánlatában egy figyelmeztető üzenet fog megjelenni. Az üzenet jelzi, hogy mivel nincsenek csatolt projektárlisták, a becsült és a tényleges projektmunka és -költségek nem lesznek beárazva.

### <a name="price-list-default-on-project-contracts"></a>Árlista alapértelmezései a projektszerződésekben 
A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen alapértelmezett a projektszerződésben:

1. Ha a szerződés ajánlatból jön létre, akkor az ajánlaton szereplő projekt-árlisták átmásolása külön történik, és a projektszerződéshez kapcsolódik.
1. Ha a szerződés a semmiből jön létre, akkor a rendszer megnézi azokat az árlistákat, amelyek a Partner projektárlistáihoz kapcsolódnak. Ha a partner bejegyzéséhez a projektárlisták nincsenek csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt értékesítési árlistát keresi meg, amelyek megfelelnek a projektszerződés pénznemének.
1. Következő lépésként a rendszer ellenőrzi a projektszerződés hatályossági dátumának megfelelő hatályosságú árlistákat. Pontosan azt a dátumot, amikor a szerződést létrehozták.
1. Ha több árlista is van, amelyek a projektszerződés dátumán hatályosak, akkor az összes árlista alapértelmezés szerint szerepel a projektszerződésben.
1. Ha a projektszerződés dátumára vonatkozóan nincs hatályos árlista, akkor a projektszerződésben nem szerepel alapértelmezett árlista. A projektszerződésben egy figyelmeztető üzenet fog megjelenni. Az üzenet jelzi, hogy mivel nincsenek csatolt projektárlisták, a becsült és a tényleges projektmunka és -költségek nem lesznek beárazva.

## <a name="cost-price-lists"></a>Önköltségiár-listák

A önköltségi árlisták nem alapértelmezettek a Project Operations alkalmazásban szereplő bármely entitáshoz. A projektköltségekhez használandó önköltségi árlista meghatározása mindig tranzakciónként történik. A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen használva a projekt önköltségéhez:

1. A rendszer megvizsgálja a projekt szerződő szervezeti egységéhez csatolt árlistákat.
1. Ezután a rendszer megvizsgálja az árlisták dátumhatékonyságát, amelyek megegyeznek a bejövő becslési kontextus dátumával vagy tényleges kontextusával.

    - *A becslési kontextus* a projektműveletek három becslési környezetének bármelyikére vonatkozik:

        - Projektbecslési sor
        - Árajánlatsor részletei
        - Szerződéssor részletei

    - *A tényleges kontextus* a Project Operations tényleges adatainak három forrásának bármelyikére vonatkozik:

       - Manuálisan létrehozott bejegyzésnapló-sorok vagy korrekciós naplóban létrehozott korrekciós naplósorok
       - Naplósorok, amelyek az idő-, költség- vagy anyaghasználati naplók beküldése során jönnek létre
       - Számlasor részletei

    Ha a Project Operations a tényleges környezetben *megegyezik a bejövő naplósor vagy számlasor részleteinek* dátumhatékonyságával, akkor a **Tranzakció dátuma** mezőt használja.

    - Ha több árlista érvényes a bejövő becsült környezet vagy a tényleges környezet dátumára, akkor a legutóbb létrehozott árlista lesz kiválasztva.
    - Ha a projekt szerződő szervezeti egységéhez nincs csatolva árlista, a rendszer megvizsgálja a projekt pénznemének megfelelő projektparaméterekhez csatolt önköltségi árlistákat.

## <a name="enable-multi-currency-cost-price-list"></a>Több pénznemű önköltségiár-lista engedélyezése

Ez a beállítás a **Beállítások**\> paraméterei **oldalon** található. Az alapértelmezett érték: **Nem**.

Ha ez a beállítás engedélyezve van (azaz az érték Igen **értékre** van állítva), a rendszer a következőképpen viselkedik:

- Lehetővé teszi, hogy bármilyen pénznemben önköltségi árlistákat társítsanak a szervezeti egységhez. Például egy EUR pénznemben található önköltségi árlista csatolható egy szervezeti egységhez az USD pénznemében. A rendszer továbbra is ellenőrzi, hogy a szervezeti egységhez csatolt önköltségi árlisták nem rendelkeznek-e átfedésben lévő dátum-hatékonysággal.
- Ellenőrzi, hogy a projektparaméterekhez csatolt önköltségi árlisták nem rendelkeznek-e egymást átfedő dátum-hatékonysággal, még akkor sem, ha eltérő pénznemekkel rendelkeznek. Ez a viselkedés eltér az alapértelmezett viselkedéstől (azaz attól a viselkedéstől, amikor az érték Nem **értékre** van állítva). Az alapértelmezett viselkedésben csak az azonos **pénznemmel rendelkező önköltségi árlisták lesznek érvényesítve a** nem átfedő dátumhatékonyság szempontjából.
- Bejövő tranzakciós környezet esetén csak a dátumok hatékonysága alapján határozza meg az önköltségi árlistát. Ez a viselkedés eltér az alapértelmezett viselkedéstől, ahol a rendszer kiválasztja azt az önköltségi árlistát, amely megfelel a projekt pénznemének és a dátumhatékonyságnak is.

A viselkedés e változásai miatt a Project Operations ügyfelei képesek lesznek fenntartani egy globális önköltségi árlistát, amely az egész vállalat számára releváns lesz. Nem kell, hogy legyenek árlisták a műveletek minden pénznemében. A globális árlista dátumhatékonysággal rendelkezik, és lehetővé teszi a költségárak bármilyen pénznemben történő beállítását az árképzési dimenzióértékek adott kombinációjához. Az önköltségi árlista pénzneme csak az alapértelmezett értékek **megadására szolgál a szerepkörárak,** a kategóriaárak **és** **az árlista-elemrekordok** létrehozásakor. Nem lesz használva az árlista meghatározására.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
