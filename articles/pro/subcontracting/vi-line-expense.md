---
title: Szállítói számlasorok költségkategóriákhoz
description: Ez a cikk azt ismerteti, hogyan rögzítheti a szállítói számlasorokat a költségkategóriákhoz.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925885"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Szállítói számlasorok költségkategóriákhoz

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számláinak szállítói számlasorai lehetnek a költségkategóriákhoz. A projektmenedzserek a szállítói számlasorok használatával költségkategóriákhoz rögzíthetik a költségkategóriákként beszerzett szolgáltatások költségeit.

Előfordulhat, hogy a költségkategóriák szállítói számlasorai nem hivatkoznak alvállalkozói sorra a költségkategóriákhoz. Ha a költségkategóriák szállítói számlasora alvállalkozói szerződésre hivatkozik, a projektmenedzserek egyeztethetik és ellenőrizhetik a szállítói számlasor által számlázott költségeket az ezeken a költségkategóriákban rögzített és a projekt projektmenedzserei által jóváhagyott költségekkel.

Az alábbi táblázat a szállítói számlasorok költségkategóriákra vonatkozó mezőiről nyújt tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve, hogy segítsen az azonosításban. | Ez a név jelenik meg az első oszlopként az összes olyan keresésben, amely a szállítói számlasorokon alapul. |
| Description | A szállító által a szállítói számlasoron számlázandó szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az alvállalkozás, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha alvállalkozói szerződést választ a szállítói számlához, a szállítói számla összes sora örökli ezt a beállítást. A szállítói számlák nem tartalmazhatnak olyan szállítói számlasorokat, amelyek különböző alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozói vonal | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kiválasztható alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy szállítói számlasoron alvállalkozói sort jelöl ki a költségkategóriákhoz, a Projekt, a Tevékenység **és** a **Tranzakció kategória** mezők alapértelmezett értékei az alvállalkozói sor megfelelő mezőiből kerülnek be. **·** Ha a kiválasztott alvállalkozói sor értékeket tartalmaz a Projekt **,** a Projekt tevékenység **és** a **Tranzakció kategória** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségének tényleges költséget rögzíti a projektben. |None |
| Tranzakcióosztály | Válassza a Költség lehetőséget **egy** költségkategória szállítói számlájának rögzítéséhez. | A Költség **érték** azt jelzi, hogy a szállítói számlasort használják a költségkategóriákként beszerzett szolgáltatások számlaösszegének rögzítésére. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projektfeladatnak a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort a projekt bármely tevékenységén rögzített költségekkel egyeztetheti. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz összekapcsolva a nem számlázott értékesítési tényleges adatokkal. Ebben az esetben, ha a feladatalapú számlázás be van állítva, előfordulhat, hogy a költségek nem számlázhatók ki a végfelhasználónak. |
| Tranzakció kategóriája | A számlázandó tranzakciós kategória. Létre kell hozni egy megfelelő költségkategóriát a kiválasztott tranzakciós kategóriához. | A Tranzakciós kategória és az Egység **értékek kombinációja** lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett vagy számított **értéke.** |
| Mennyiség | Adja meg a szállító által számlázandó mennyiséget a számlasoron. |None|
| Egységcsoport | Az alapértelmezett érték a kiválasztott tranzakciós kategória egységcsoportja alapján kerül megadásra. | None |
| Kiszerelés | Az alapértelmezett érték a kiválasztott egységcsoport alapegysége. Ezt az értéket úgy módosíthatja, hogy az egységcsoport bármely egységében vásároljon. | A Tranzakciós kategória és az Egység **értékek kombinációja** lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett vagy számított **értéke.** |
| Egységár | Az alapértelmezett egységár a tranzakciós kategória **és** a egység **értékek kombinációját** használja a projekt árlistájából, amely a szállítói számlasor tranzakciós dátumára vonatkozik. | Ha az alkalmazandó projektárlista ára olyan egységben van beállítva, amely eltér a szállítói számlasor egységétől, a rendszer az egységátváltást használja az egységár kiszámításához. |
| Részösszeg | Ezt a csak olvasható mezőt a rendszer *Mennyiség*&times; egységárként *számítja* ki, ha az értékeket a Mennyiség **mezőben és az** Egységár **mezőben is** meg van adva. Ha az egyik vagy mindkét mező üres, megadhat egy értéket ebben a mezőben.| None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege, beleértve az adókat is. Ezt a mezőt a rendszer részösszeg *szerinti áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
