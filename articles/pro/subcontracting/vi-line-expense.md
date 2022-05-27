---
title: Szállítói számlasorok költségkategóriákhoz
description: Ez a témakör bemutatja, hogyan rögzíthetők a szállítói számlasorok a költségkategóriákhoz.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579539"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Szállítói számlasorok költségkategóriákhoz

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái tartalmazhatnak költségkategóriákhoz tartozó szállítói számlasorokat. A projektmenedzserek a költségkategóriákhoz tartozó szállítói számlasorok segítségével rögzíthetik a költségkategóriákként beszerzett szolgáltatások költségeit.

A költségkategóriák szállítói számlasorai a költségkategóriákhoz alvállalkozói sorra hivatkozhatnak vagy nem. Ha a költségkategóriák szállítói számlasora alvállalkozói szerződésre hivatkozik, a projektmenedzserek össze tudják egyeztetni és ellenőrizni tudják a szállítói számlasor által számlázott költségeket az ezeken a költségkategóriákon rögzített és a projektmenedzserek által a projekten jóváhagyott költségekkel.

Az alábbi táblázat a költségkategóriák szállítói számlasoraiban szereplő mezőiről tartalmaz tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve az azonosításhoz. | Ez a név jelenik meg első oszlopként a szállítói számlasorokon alapuló összes keresésben. |
| Description | A szállító által a szállító számlasorban számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozói szerződés, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha a szállítói számlához alvállalkozói szerződés van kiválasztva, a szállítói számla összes sora örökli ezt a kijelölést. A szállítói számlákon nem lehetnek különböző alvállalkozókra hivatkozó szállítói számlasorok. |
| Alvállalkozói sor | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kijelölhető alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha a költségkategóriák szállítói számlasorában alvállalkozói sor van kiválasztva, a Projekt, **a Tevékenység** és **a Tranzakció kategória** mezők alapértelmezett értékeit a **program** az alvállalkozói sor megfelelő mezőiből adja meg. Ha a kijelölt alvállalkozósor értékei szerepelnek a Projekt, a **Projekt tevékenység** és **a Tranzakció kategória** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől **.** |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költség-tényleges értékét rögzítik a projektben. |None |
| Tranzakcióosztály | Válassza a Költség lehetőséget **egy** költségkategória szállítói számlájának rögzítéséhez. | A Költség **érték** azt jelzi, hogy a szállítói számlasort a költségkategóriaként beszerzett szolgáltatások számlaösszegének rögzítésére használják. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projekttevékenységnek a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha projekt van kijelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort a projekt bármely tevékenységén rögzített költségekkel egyeztetheti. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz hozzárendelve nem hozzárendelt értékesítési tényleges értékekkel. Ebben az esetben, ha feladatalapú számlázás van beállítva, előfordulhat, hogy a költségeket nem lehet számlázni a végfelhasználónak. |
| Tranzakció kategóriája | A számlázandó tranzakciókategória. A kijelölt tranzakciókategóriához létre kell hozni egy megfelelő költségkategóriát. | A tranzakciós kategória és az **Egységértékek** kombinációja lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett vagy számított **értéke.** |
| Mennyiség | Adja meg a szállító által a számlasorban számlázott mennyiséget. |None|
| Egységcsoport | Az alapértelmezett érték a kijelölt tranzakciókategória egységcsoportja alapján történik. | None |
| Kiszerelés | Az alapértelmezett érték a kijelölt egységcsoport alapegysége. Ezt az értéket módosíthatja, hogy az egységcsoport bármely egységében vásároljon. | A tranzakciós kategória és az **Egységértékek** kombinációja lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett vagy számított **értéke.** |
| Egységár | Az alapértelmezett egységár a szállítói számlasor tranzakciós dátumára **alkalmazandó tranzakciós árlista Tranzakciós kategóriájának** és **Egységértékeinek** kombinációját használja. | Ha a megfelelő projektárlista ára olyan egységben van beállítva, amely eltér a szállítói számlasorban szereplő egységtől, a rendszer az egységátalakítást használja az egységár kiszámításához. |
| Részösszeg | Ezt az írásvédett mezőt a program *Mennyiségi*&times; egységárként *számítja* ki, ha az értékeket mind a Mennyiség **, mind** az **Egységár** mezőben beírja. Ha az egyik vagy mindkét mező üres, ebben a mezőben megadhat egy értéket.| None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege az adókkal együtt. Ezt a mezőt a program részösszeg *áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
