---
title: Alapértelmezett árlisták
description: Ez a cikk az alapértelmezett értékesítési és önköltségi árlistákról nyújt tájékoztatást a Project Operations alkalmazásban.
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
1. Ha a partner bejegyzéséhez nincsenek projektárlisták csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt értékesítési árlistát keresi meg, amelyek megfelelnek a projektajánlat pénznemének.
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

A önköltségi árlisták nem alapértelmezettek a Project Operations alkalmazásban szereplő bármely entitáshoz. Az önköltségi árlisták meghatározására a projekt költségeihez való használathoz mindig tranzakciónként kerül sor. A rendszer a következő folyamatot hajtja végre annak meghatározásához, hogy mely árlista legyen használva a projekt önköltségéhez:

1. A rendszer a projektajánlatkérő szervezeti egységéhez kapcsolt árlisták listáját vizsgálja meg.
1. A rendszer ezt követően azon árlisták hatályossági dátumát tekinti meg, amelyek megfelelnek a bejövő becslési környezet vagy a tényleges környezet dátumának.

    - Ebben az esetben a *Becslési környezet* a Project Operations alkalmazásban a becslések mindhárom kontextusára vonatkozik:

        - Projektbecslési sor
        - Árajánlatsor részletei
        - Szerződéssor részletei

    - Ebben az esetben az *Aktuális környezet* a Project Operations alkalmazásban a tényadatok mindhárom forrására vonatkozik:

       - Manuálisan létrehozott beviteli naplósorok vagy a helyesbítési naplóban létrehozott helyesbítési naplósorok
       - Idő-, költség- vagy anyaghasználati naplók benyújtásakor létrehozott naplósorok
       - Számlasor részletei

    Ha a Project Operations alkalmazásban a *tényleges környezetben* megegyezik a bejövő naplósor vagy számlasor részletei elemmel, a **Tranzakció dátuma** mezőt használja.

    - Ha a bejövő becslés vagy a tényadat dátumára vonatkozóan több olyan árlista is van, a legutóbb létrehozott árlista lesz kiválasztva.
    - Ha a projekt szerződő szervezeti egységéhez nincsenek árlisták csatolva, akkor a rendszer a projekthez tartozó paraméterekhez csatolt önköltségi árlistát keresi meg, amelyek megfelelnek a projektajánlat pénznemének.

## <a name="enable-multi-currency-cost-price-list"></a>Több pénznemű önköltségiár-lista engedélyezése

Ez a beállítás a **Beállítások** \> **Paraméterek** között található. Az alapértelmezett érték: **Nem**.

Ha engedélyezve van ez a beállítás (tehát az érték **Igen**), a rendszer a következő módon viselkedik:

- Lehetővé teszi, hogy az önköltségi árlisták bármely pénznemben hozzá legyenek társítva a szervezeti egységhez. Például az EUR pénznemben lévő költségárlista például csatolható egy USD-pénznemet használó szervezeti egységhez. A rendszer továbbra is ellenőrzi, hogy a szervezeti egységhez csatolt költségárlistáknak ne legyenek átfedő dátumai.
- A program ellenőrzi, hogy a projektparaméterhez kapcsolt önköltségi árlistáknak ne legyenek átfedésben lévő hatályossági dátumai, még akkor sem, ha pénznemük eltérő. Ez a viselkedés különbözik az alapértelmezett viselkedéstől (tehát az a viselkedés, amikor az érték beállítása **Nem**). Alapértelmezett viselkedés szerint csak az **azonos** pénznemű önköltségi árlistákat ellenőrzi a rendszer nem átfedő hatályossági dátumok szempontjából.
- Bejövő tranzakciós környezet esetén az önköltségi árlistát csak a hatályossági dátumok segítségével határozza meg. Ez a viselkedés különbözik az alapértelmezett viselkedéstől, amelyben a rendszer a projekt pénznemének és hatályossági dátumának megfelelő önköltségi árlistát választja ki.

A viselkedés ezen változásai miatt a Project Operations ügyfelei képesek lesznek karbantartani a teljes vállalatra vonatkozó globális önköltségi árlistát. Nem kell mindegyik pénznemben önköltségi árlistával rendelkezniük. A globális árlista rendelkezik hatályossági dátumma, és lehetővé teszi az önköltségi ráták beállítását bármilyen pénznemben az árképzési dimenzióértékek adott kombinációjához. Az önköltségi árlista pénzneme csak akkor használatos alapértelmezett értékek megadására, ha a **Szerepkörárak**, a **Kategóriaárak** és az **Árlista** elem rekordjai létre vannak hozva. Nem lesz használva az árlista meghatározására.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
