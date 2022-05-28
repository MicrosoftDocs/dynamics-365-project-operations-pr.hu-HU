---
title: Szállítói számlasorok az időhöz
description: Ez a témakör bemutatja, hogyan rögzíthetők a szállítói számlasorok az alvállalkozók által beírt időköltségekhez.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597203"
---
# <a name="vendor-invoice-lines-for-time"></a>Szállítói számlasorok az időhöz

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számláihoz szállítói számlasorok tartozhatnak. A projektmenedzserek a szállítói számlasorokat idővel rögzíthetik az alvállalkozói idő költségeinek rögzítésére a projekteken.

A szállítói számlasorok az időhöz lehet, hogy nem hivatkoznak alvállalkozói sorra. Ha egy szállítói számlasor alvállalkozói szerződésre hivatkozik, a projektmenedzserek össze tudják egyeztetni és ellenőrizni tudják, hogy a szállítói számlasor mennyi időt számláz ki az alvállalkozók által rögzített és a projektmenedzserek által jóváhagyott idővel.

Az alábbi táblázat a szállítói számlasorok időbeli mezőiről tartalmaz tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve az azonosításhoz. | Ez a név jelenik meg első oszlopként a szállítói számlasorokon alapuló összes keresésben. |
| Description | A szállító által a szállító számlasorban számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozói szerződés, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha a szállítói számlához alvállalkozói szerződés van kiválasztva, a szállítói számla összes sora örökli ezt a kijelölést. A szállítói számlákon nem lehetnek különböző alvállalkozókra hivatkozó szállítói számlasorok. |
| Alvállalkozói sor | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kijelölhető alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy alvállalkozói sor időrendben van kiválasztva egy szállítói számlasorban, a Projekt **,** a Szerepkör **és** a **Könyvelhető erőforrás** mezők alapértelmezett értékeit az alvállalkozósor megfelelő mezőiből kell megadni. Ha a kijelölt alvállalkozói sor értékei szerepelnek a Projekt **,** Szerepkör **és** **Könyvelhető** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költség-tényleges értékét rögzítik a projektben. | None |
| Tranzakcióosztály | Alapértelmezett értéke **Idő**. | Az Idő **érték** azt jelzi, hogy a szállítói számlasor az alvállalkozói idő számlaösszegének rögzítésére szolgál. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projekttevékenységnek a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha projekt van kijelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort összevetheti az alvállalkozói erőforrások által a projekt bármely tevékenységén rögzített idővel. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz hozzárendelve nem hozzárendelt értékesítési tényleges értékekkel. Ebben az esetben, ha feladatalapú számlázás van beállítva, előfordulhat, hogy a költségeket nem lehet számlázni a végfelhasználónak. |
| Beosztás | Annak az alvállalkozói erőforrásoknak a szerepe, amelyeknek az ideje számlázás alatt áll. | Ez a mező azt a szerepkört adja meg, amelyet azok az alvállalkozói erőforrások hajtanak végre, amelyeknek az ideje a szállítói számlán van számlázva. |
| Lefoglalható erőforrás | Annak az alvállalkozónak a neve, akinek az idejét kiszámlázzák. A lefoglalható erőforrás kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser egyeztetheti a szállítói számlasort a szállítói számlasorban szereplő szállítóhoz tartozó erőforrások által rögzített idővel. |
| Mennyiség | Adja meg a szállító által a számlasorban számlázott órák számát. |None |
| Egységcsoport | Az alapértelmezett érték az Időegységcsoport **,** és nem módosítható. | None |
| Kiszerelés | Az alapértelmezett érték az időegységcsoport óra alapegysége. Ezt az értéket módosíthatja, hogy az időegységcsoport bármely egységében, például a napban vagy a héten vásároljon. | A szerepkör és az **Egység** értékek kombinációja lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett **vagy számított értéke.** |
| Egységár | Az alapértelmezett egységár a szállítói számlasor tranzakciós dátumára **alkalmazandó projektárlista Szerepkör** és **Egység** értékeinek kombinációját használja. | Ha a megfelelő projektárlista ára olyan egységben van beállítva, amely eltér a szállítói számlasorban szereplő egységtől, a rendszer az egységátalakítást használja az egységár kiszámításához. |
| Részösszeg | Ezt az írásvédett mezőt a program *Mennyiségi*&times; egységárként *számítja* ki, ha az értékeket mind a Mennyiség **, mind** az **Egységár** mezőben beírja. Ha az egyik vagy mindkét mező üres, ebben a mezőben megadhat egy értéket. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege az adókkal együtt. Ezt a mezőt a program részösszeg *áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
