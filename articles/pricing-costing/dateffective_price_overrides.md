---
title: Hatályossági dátummal rendelkező árfelülbírálások
description: Ez a cikk ismerteti, hogyan lehet árfelülbírálást beállítani adott árakhoz az árlistában.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446002"
---
# <a name="date-effective-price-overrides"></a>Hatályossági dátummal rendelkező árfelülbírálások 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A *Hatályossági dátummal rendelkező árfelülbírálások* segítségével felülbírálhat vagy módosíthat adott árakat az árlistában. Tegyük fel például, hogy van egy standard árlista, amely 2022. január 1. és 2022. december 31. között hatályos. Ez az árlista számos szerepkör árát tartalmazza. A **Hálózati technikus** szerepkör számára beállított ár óránként 100 amerikai dollár (USD). Amikor egy hálózati technikus 2022. január 1. és 2022. december 31. között időt naplóz, az idő ára 100 USD lesz. 2022 . október 1-én **csak** a *Hálózati technikus* szerepkör árát módosítja 100 USD értéktől óránként 110 USD re. A **Hatályossági dátummal rendelkező árfelülbírálások** funkció lehetővé teszi, hogy a sor felülbírálásként alkalmazza ezt a módosítást ehhez az adott szerepkörárhoz. Ezért nem kell a teljes árlistát másolni, és csak ennek az egy sornak az árát kell módosítani.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Hatályossági dátummal rendelkező árfelülbírálások munkadíjhoz

A projekten belül a munkaidíjra vonatkozó hatályossági dátummal rendelkező árfelülbírálások beállításának folyamata két alapvető lépésből áll.

1. A **Hatályossági dátummal rendelkező árfelülbírálások** funkció engedélyezése.
1. Hatályossági dátummal rendelkező árfelülbírálás beállítása.

### <a name="enable-the-date-effective-price-overrides-feature"></a>A Hatályossági dátummal rendelkező árfelülbírálások funkció engedélyezése

> [!NOTE]
> A **Hatályossági dátummal rendelkező árfelülbírálások** funkció engedélyezése után az nem tiltható le.

A **Hatályossági dátummal rendelkező árfelülbírálások** funkció engedélyezéséhez hajtsa végre a következő lépéseket.

1. Válassza a **Beállítások** \> **Paraméterek** lehetőséget.
1. Nyissa meg a **Paraméterek** rekordot.
1. A Műveletpanel **Funkcióvezérlés** lapján válassza a **Hatályossági dátummal rendelkező árfelülbírálások engedélyezése** lehetőséget.
1. A jóváhagyást kérő párbeszédpanelen válassza az **OK** lehetőséget.
1. Néhány pillanat után frissítse a böngészőjét. A Hatályossági dátummal rendelkező árfelülbírálások képességeknek most már elérhetőnek kell lennie. Tudni fogja, hogy ezek a lehetőségek engedélyezve vannak, ha az **Hatályossági dátummal rendelkező árfelülbírálások** lehetőség már nem jelenik meg a műveletablakban.

### <a name="set-up-a-date-effective-price-override"></a>Hatályossági dátummal rendelkező árfelülbírálás beállítása

A hatályossági dátummal rendelkező árfelülbírálások csak a **Költség**, **Értékesítés** vagy **Beszerzés** árlistákon állíthatók be.

> [!NOTE]
>A **Hatályossági dátummal rendelkező árfelülbírálások** jelenleg a következő korlátozásokkal rendelkezik:
>
> - Csak a szerepkörárak és a szerepkörárrések támogatják a **Hatályossági dátummal rendelkező árfelülbírálások** szolgáltatást a Project Operations alkalmazásban.
> - Ha az **Árlista részletei** lapon a **Másolás** művelettel másol egy árlistát, és amikor létrehoz egy projektárlistát egy standard vagy egyéni árlistából a szerződés létrehozása során, a hatályossági dátummal rendelkező árfelülbírálások **nem** lesznek másolva a forrás árlistából.

Hatályossági dátummal rendelkező árfelülbírálások beállításához egy szerepkörárhoz vagy a szerepkörárréshez, kövesse ezeket a lépéseket.

1. Nyissa meg annak az árlistának az oldalát, amelyhez be szeretné állítani a hatályossági dátummal rendelkező árfelülbírálást.
1. Válassza a **Szerepkörárak** lapot. Ez a lap az árlista **Szerepkörár** rekordjait sorolja fel.
1. Válassza ki azt a **Szerepkörár** rekordot amelyhez be szeretné állítani az Hatályossági dátummal rendelkező árfelülbírálást, majd koppintson duplán (vagy kattintson duplán) a **Szerepkörár** elemre a **Szerepkörár részletei** lap megnyitásához.
1. Válassza a **Hatályossági dátummal rendelkező árfelülbírálások** lapot . A lap rácsa felsorolja a kijelölt **Szerepkörár** rekord összes hatályossági dátummal rendelkező árfelülbírálását.
1. A rács feletti eszköztáron válassza az **Új szerepkörár-felülbírálás** lehetőséget. Megnyílik az **Új szerepkörár felülbírálás** csúszka.
1. Adja meg a hatályosság kezdődátumát, az egységet és az új árat az árfelülbírálásához. Majd válassz a **Mentés** lehetőséget, és zárja be az űrlapot.

> [!NOTE]
> - A Hatályossági dátummal rendelkező árfelülbírálás egy szerepkörárhoz vagy szerepkörárréshez ugyanazon árazási dimenzióértékek kombinációjára érvényes, amelyek a szülő **Szerepkörár** vagy **Szerepkörárrés** soron léteznek.
> - Az **Érvényesség kezdete** mezőben kiválasztott dátumnak a fölérendelt árlista érvényességi dátumán belül kell lennie. Az árfelülbírálás az **Érvényesség kezdete** mezőben kiválasztott dátumon lép életbe, és a fölérendelt árlista záró dátumának végéig érvényes. Ha ugyanazon a szerepköráron további hatályossági dátummal rendelkező árfelülbírálást állít be, az első árfelülbírálás az **Érvényesség kezdete** mezőben kijelölt dátumon lép hatályba, és a második felülbírálás kezdetéig érvényes.

## <a name="examples"></a>Példák

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1. példa: Az érvényességi dátum meghatározása egy olyan szerepkörárhoz, amely szerepkörár-felülbírálásokkal rendelkezik

A következő példa azt mutatja be, hogyan határozható meg a az érvényességi dátum egy adott szerepkörárnál, amelyhez szerepkörár-felülbírálások vannak beállítva.

**A árlista: Január 1. és június 30. között**

*Szerepkörár*

| Szerepkörár | Kiszerelés | Ár | A bejövő tranzakciók árképzésére gyakorolt hatás |
|---|---|---|---|
| Hálózati technikus | Óra | 100 | Ezt az árat kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma január 1. és március 14. között van. |

*Szerepkörár-felülbírálás*

| Érvényesség kezdete | Kiszerelés | Ár | A bejövő tranzakciók árképzésére gyakorolt hatás |
|---|---|---|---|
| 15. március | Óra | 110 | Ezt az árat kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma március 15. és március 30. között van. |
| 1. ápr. | Óra | 120 | Ezt az árat kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma április 1. és június 30. között van. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2. példa: Az érvényességi dátum meghatározása egy olyan szerepkörárréshez, amely szerepkörárrés-felülbírálásokkal rendelkezik

A következő példa azt mutatja be, hogyan határozható meg a az érvényességi dátum egy adott szerepkörárrésnél, amelyhez szerepkörárrés-felülbírálások vannak beállítva.

**A árlista: Január 1. és június 30. között**

*Szerepkörár*

| Szerepkörár | Munkaórák | Kiszerelés | Ár | A bejövő tranzakciók árképzésére gyakorolt hatás |
|---|---|---|---|---|
| Hálózati technikus | Szabályos | Óra | 100 | Ezt az árat kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma január 1. és március 14. között van. |

*Szerepkörárrés*

| Szervezeti egység | Munkaórák | Árrés % |
|---|---|---|
| Contoso USA | Túlóra | 10% |

*Szerepkörárrés felülbírálása*

| Érvényesség kezdete | Ár | A bejövő tranzakciók árképzésére gyakorolt hatás |
|---|---|---|
| 15. március | 20% | Ezt az árrés százalékértéket kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma március 15. és március 30. között van. |
| 1. ápr. | 25% | Ezt az árrést kell használni minden olyan tranzakciónál, ahol a tranzakció dátuma április 1. és június 30. között van. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
