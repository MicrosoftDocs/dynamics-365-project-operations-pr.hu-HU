---
title: Hatálybalépéskori árfelülírások
description: Ez a cikk azt ismerteti, hogyan állíthat be árfelülírásokat adott árakhoz az árlistában.
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
# <a name="date-effective-price-overrides"></a>Hatálybalépéskori árfelülírások 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

*Az érvényes dátum szerinti árfelülírások* lehetővé teszik az árlistában szereplő konkrét árak felülbírálását vagy módosítását. Van például egy standard árlistája, amely 2022. január 1-jétől 2022. december 31-ig érvényes. Ez az árlista számos szerepkör árait tartalmazza. A hálózati technikus **szerepkörhöz** beállított ár óránként 100 amerikai dollár (USD). Amikor egy hálózati technikus 2022. január 1. és 2022. december 31. között naplózza az időt, az idő ára 100 USD. 2022. október 1-jén csak *a* hálózati technikus **szerepkör árát** kell módosítania, óránként 100 USD óráról óránként 110 USD-ra. Az **Érvényességi ár felülbírálásának** dátuma funkció lehetővé teszi, hogy ezt a módosítást az adott szerepkör-árhoz tartozó sor felülbírálásaként állítsa be. Ezért nem kell a teljes árlistát lemásolnia, és csak az egy sor árát módosítania.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Hatálybalépéskori árfelülírások a munkaerő-árazáshoz

A projekten a munkaidő dátum-tényleges árfelülírásainak beállításának folyamata két alapvető lépésből áll.

1. Engedélyezze a **Date effective price overrides** funkciót.
1. Állítson be egy érvényes dátum szerinti árfelülírást.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Az Érvényességi ár felülbírálásának dátuma funkció engedélyezése

> [!NOTE]
> **Az Érvényességi ár felülbírálásának** dátuma funkció engedélyezése után nem tiltható le.

A Hatálybalépés dátuma szerinti árfelülírások **funkció engedélyezéséhez** kövesse az alábbi lépéseket.

1. Lépjen a **Beállítások** \> **paramétereihez**.
1. Nyissa meg a **Parameters** rekordot.
1. A Műveleti panel Funkcióvezérlő **lapján válassza a** Dátum tényleges árfelülsőinek **engedélyezése lehetőséget**.
1. A jóváhagyást kérő párbeszédpanelen válassza az **OK** lehetőséget.
1. Néhány pillanat múlva frissítse a böngészőt. A dátumalapú árfelültetési képességeknek mostantól elérhetőnek kell lenniük. Tudni fogja, hogy ezek a képességek engedélyezve vannak, ha **a Dátum tényleges árfelülírások** engedélyezése már nem jelenik meg a műveleti ablaktáblán.

### <a name="set-up-a-date-effective-price-override"></a>Hatálybalépési dátum szerinti árátrendezés beállítása

A dátum-hatályos árfelülírások a költség **-,** értékesítési **vagy** beszerzési **árlistákon** állíthatók be.

> [!NOTE]
>Az Érvényességi ár felülbírálásának **dátuma viselkedése** jelenleg a következő korlátozásokkal rendelkezik:
>
> - Csak a szerepkörárak és a szerepkör-árárak támogatják a **Project Operations tényleges árfelülírásainak** dátuma funkciót.
> - Ha az árlista részletei oldalon található **Másolás** művelettel másol egy árlistát, és amikor a szerződés létrehozása során szabványos vagy egyéni árlistából hoz létre projektárlistát, a **rendszer nem** másolja ki a forrásárlistából a tényleges árfelültetéseket **.**

Ha dátum-tényleges árfelülsőt szeretne beállítani egy szerepkörárhoz vagy egy szerepkör-árjelöléshez, kövesse az alábbi lépéseket.

1. Nyissa meg annak az árlistának az oldalát, amelyhez be szeretné állítani a hatálybalépési dátum szerinti árfelfüggesztést.
1. Válassza a **Szerepkörárak** lapot. Ez a lap felsorolja az **árlistában szereplő összes szerepkör-árrekordot**.
1. Válassza ki azt a **szerepkör-árrekordot**, amelyhez új, érvényes dátum szerinti felülbírálási árat szeretne beállítani, majd koppintson duplán (vagy kattintson duplán) **a szerepkör ára** elemre a **szerepkör árának részletei** oldal megnyitásához.
1. Válassza az **Érvényességi idő felülbírálásának** dátuma lapot. Az ezen a lapon található rács felsorolja a kiválasztott **szerepkör-árrekord** összes érvényes dátum-felülbírálását.
1. A rács feletti eszköztáron válassza az Új szerepkör árának felülbírálása **lehetőséget**. Megnyílik az **Új szerepkör árának felülbírálása** csúszka.
1. Adja meg az érvényesség dátumát, az egységet és az új árat az ár felülbírálásához. Ezután válassza a Mentés **lehetőséget**, és zárja be az űrlapot.

> [!NOTE]
> - A szerepkör árának vagy a szerepkör árának felárazásának dátum szerinti érvényes árfelülsője a díjszabási dimenzióértékek ugyanazon kombinációjára vonatkozik, amely a szülőszerepeltetési **árában** vagy **a szerepkör árjelölő** sorában található.
> - Az Érvényesség kezdete **mezőben kiválasztott** dátumnak a szülőárlista érvényességi dátumán belül kell lennie. Az árfelülsőlés az Érvényesség **kezdete mezőben kiválasztott** napon lép hatályba, és a szülőárlista záró dátumának végéig érvényes. Ha ugyanahhoz a szerepkör-árhoz egy másik hatálybalépési dátum-árfelülsőt állít be, az első árfelirtás az Érvényesség kezdete **mezőben kiválasztott** napon lép hatályba, és a második felülírás kezdetéig érvényes lesz.

## <a name="examples"></a>Példák

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1. példa: A szerepkör árának dátum-effektivitásának meghatározása olyan szerepkör-árhoz, amely szerepkör-ár-felülbírálásokkal rendelkezik

Az alábbi példa bemutatja, hogyan határozzák meg a dátumhatékonyságot egy adott szerepkör-árhoz, amelyre a szerepkör árának felülbírálásai be vannak állítva.

**Árlista A: január 1-jétől június 30-ig**

*Szerepkör ára*

| Szerepkör ára | Kiszerelés | Ár | A bejövő tranzakciók díjszabására gyakorolt hatás |
|---|---|---|---|
| Hálózati technikus | Óra | 100 | Ezt az árat minden olyan tranzakciónál felhasználjuk, ahol a tranzakció dátuma január 1. és március 14. között van. |

*Szerepkör-ár felülbírálása*

| Hatékony a | Kiszerelés | Ár | A bejövő tranzakciók díjszabására gyakorolt hatás |
|---|---|---|---|
| 15. március | Óra | 110 | Ezt az árat használjuk minden olyan tranzakciónál, ahol a tranzakció dátuma március 15. és március 30. között van. |
| 1. ápr. | Óra | 120 | Ezt az árat használjuk minden olyan tranzakciónál, ahol a tranzakció dátuma április 1. és június 30. között van. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2. példa: Dátum-hatékonyság meghatározása olyan szerepkör-ármegállapozáshoz, amelynek szerepkör-ármegállapítási felülbírálásai vannak

Az alábbi példa bemutatja, hogyan határozzák meg a dátumok hatékonyságát egy adott szerepkör-árjelentkezéshez, amelyhez a szerepkör árjelentőjel-felülbírálásai be vannak állítva.

**Árlista A: január 1-jétől június 30-ig**

*Szerepkör ára*

| Szerepkör ára | Munkaórák | Kiszerelés | Ár | A bejövő tranzakciók díjszabására gyakorolt hatás |
|---|---|---|---|---|
| Hálózati technikus | Szabályos | Óra | 100 | Ezt az árat minden olyan tranzakciónál felhasználjuk, ahol a tranzakció dátuma január 1. és március 14. között van. |

*Szerepkör szerinti árjelentkezés*

| Szervezeti egység | Munkaórák | Felár felszámítása % |
|---|---|---|
| Contoso USA | Túlóra | 10% |

*Szerepkör-árjelek felülbírálása*

| Hatékony a | Ár | A bejövő tranzakciók díjszabására gyakorolt hatás |
|---|---|---|
| 15. március | 20% | Ezt a felár százalékos arányt minden olyan tranzakciónál felhasználjuk, ahol a tranzakció dátuma március 15. és március 30. között van. |
| 1. ápr. | 25% | Ezt a jelölést minden olyan tranzakciónál felhasználjuk, ahol a tranzakció dátuma április 1. és június 30. között van. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
