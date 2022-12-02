---
title: Szállítói számlasorok költségkategóriákhoz
description: Ez a cikk azt ismerteti, hogyan rögzíthetők a szállítói számlasorok költségkategóriákhoz.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261685"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Szállítói számlasorok költségkategóriákhoz

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái rendelkeznek költségkategóriákhoz kapcsolódó szállítóiszámla-sorokkal A projektvezetők a költségkategóriákhoz tartozó szállítói számlasorokat használhatják a költségkategóriákként nyújtott szolgáltatások költségeinek rögzítésére.

Az költségkategóriákhoz kapcsolódó szállítói számlasorok hivatkoznak egy alvállalkozói sorra a költségkategóriák vonatkozásában. Ha egy költségkategóriákhoz kapcsolódó alvállalkozó számlasor egy alvállalkozói szerződésre hivatkozik, akkor a projektvezetők egyeztetnie, illetve ellenőrizni tudják a szállító számlasorában szereplő költségkategóriákat az alvállalkozók által rögzített és a projektmenedzserek által jóváhagyott költségekkel szemben.

Az alábbi táblázat ismerteti a költségkategóriákhoz kapcsolódó szállítói számlasorok mezőit.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve, amely segítséget nyújt az azonosításában. | Ez a név lesz megjelenítve első oszlopként minden olyan keresésben, amelyek a szállítói számlasorokon alapulnak. |
| Description | Az alvállalkozói számlán a beszállító által számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozó, amelytől a szolgáltatásokat eredetileg megrendelték. | Amikor egy alvállalkozói szerződés ki van jelölve a szállítói számlához, a szállítói számla minden sora örökli ezt a beállítást. A szállítói számlákon nem lehetnek olyan szállítói számlasorokat, amelyek más alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozóiszerződés-sor | Az az alvállalkozói sor, amelytől a szolgáltatásokat megrendelték. A választható alvállalkozói sorok listája a kijelölt alvállalkozó szerződés soraira van korlátozva. | Ha egy alvállalkozó sort kiválaszt egy költségkategóriákhoz kapcsolódó szállító számlasoron, akkor a **Projekt**, a **Feladat** és a **Tranzakciókategória** mezők alapértelmezett értékeit a program az alvállalkozósor megfelelő mezőiből adja meg. Ha a kijelölt alvállalkozói sornak értékei vannak a **Projekt**, a **Projektfeladat** és a **Tranzakciókategória** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el azoktól az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségét rögzíteni fogják a projekthez. |None |
| Tranzakcióosztály | Válassza a **Költség** lehetőséget egy szállítói számla rögzítéséhez egy költségkategóriához. | A **Költség** érték azt jelzi, hogy a szállító számlasor olyan szolgáltatásokhoz kapcsolódó számlaösszeg rögzítésére szolgál, amelyek költségkategóriákként lettek előállítva. |
| Project | Annak a projektnek a neve, amelyhez a számlázott szolgáltatásokat felhasználták. | Ez egy kötelező mező, és nem lehet üres. |
| Feladatok | Annak a projektfeladatnak a neve, amelyhez a számlázott szolgáltatásokat felhasználták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projektfeladat kiválasztása nem kötelező. | Ha a mezőt üresen hagyja, akkor a projektvezető a szállító számlasorát megfeleltetheti azokkal a költségekkel, amelyek rögzítve lettek a projekt bármelyik feladatához. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz társítva egyetlen nem számlázatlan tényleges értékesítéshez sem. Ebben az esetben a feladatalapú számlázás beállítása esetén előfordulhat, hogy a költségeket nem lehet a végfelhasználónak kiszámlázni. |
| Tranzakció kategóriája | A számlázott tranzakciókategória. A kiválasztott tranzakciókategóriához egy kapcsolódó költségkategóriát kell létrehozni. | A rendszer a **Tranzakciókategória** és az **Egység** értékek kombinációját használja az alvállalkozói szerződéssor **Egységár** mezőjének alapértelmezett vagy számított értékeként. |
| Mennyiség | Adja meg a számlasoron a szállító által számlázott mennyiséget. |None|
| Egységcsoport | A megadott alapértelmezett érték a kiválasztott tranzakció kategóriához beállított alapértelmezett egységcsoporton alapul. | None |
| Kiszerelés | Az alapértelmezett érték a kijelölt egységcsoport alapegysége. Ezt az értéket úgy módosíthatja, hogy az egységcsoport bármelyik egységében lehessen vásárolni. | A rendszer a **Tranzakciókategória** és az **Egység** értékek kombinációját használja az alvállalkozói szerződéssor **Egységár** mezőjének alapértelmezett vagy számított értékeként. |
| Egységár | Az alapértelmezett egységár projektárlistában szereplő, az alvállalkozói szerződéssor kért tranzakciójának napjára vonatkozó **Tranzakciókategória** és **Egység** kombinációjából adódik. | Ha az alkalmazandó projektárlistában beállított ár eltér a szállítói számlában szereplő egységtől eltérő egységben határozza meg, a rendszer az egységár kiszámításához az egységre történő átváltást használja. |
| Részösszeg | Ez a csak olvasható mező automatikusan a *Mennyiség* &times; *Egységár* képlettel lesz kiszámítva, ha mind a **Mennyiség**, mind az **Egységár** mezőben megadnak értékeket. Ha a mezők egyike üres, akkor ebben a mezőben megadhat értéket.| None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | Az szállítói számlasor teljes összege az adókkal együtt. Ez a mező a *Részösszeg* + *Forgalmi adó* képlettel kerül kiszámításra. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
