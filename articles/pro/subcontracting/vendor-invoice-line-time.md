---
title: Szállítói számlasorok időhöz
description: Ez a cikk azt ismerteti, hogyan rögzítheti a szállítói számlasorokat az alvállalkozók által bevitt időköltségekről.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262015"
---
# <a name="vendor-invoice-lines-for-time"></a>Szállítói számlasorok időhöz

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számláinak szállítói számlasorai lehetnek az időre vonatkozóan. A projektmenedzserek a szállítói számlasorok segítségével rögzíthetik a projektek alvállalkozói idejének költségeit.

Előfordulhat, hogy a szállítói számlasorok az időre vonatkozóan hivatkoznak alvállalkozói sorra, vagy nem. Ha az idő szállítói számlasor alvállalkozói szerződésre hivatkozik, a projektmenedzserek egyeztethetik és ellenőrizhetik a szállítói számlasor által számlázandó időt az alvállalkozók által rögzített és a projektmenedzserek által jóváhagyott idővel.

Az alábbi táblázat a szállítói számlasorok idő szerinti mezőiről tartalmaz információkat.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve, hogy segítsen az azonosításban. | Ez a név jelenik meg az első oszlopként az összes olyan keresésben, amely a szállítói számlasorokon alapul. |
| Description | A szállító által a szállítói számlasoron számlázandó szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az alvállalkozás, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha alvállalkozói szerződést választ a szállítói számlához, a szállítói számla összes sora örökli ezt a beállítást. A szállítói számlák nem tartalmazhatnak olyan szállítói számlasorokat, amelyek különböző alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozói vonal | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kiválasztható alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy alvállalkozói sor ki van választva egy szállítói számlasoron az időre vonatkozóan, a Projekt **,** a Szerepkör **és** a **Foglalható erőforrás** mezők alapértelmezett értékei az alvállalkozói sor megfelelő mezőiből kerülnek be. Ha a kiválasztott alvállalkozói sor értékeket tartalmaz a Projekt **,** a Szerepkör **és** a **Foglalható** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségének tényleges költséget rögzíti a projektben. | None |
| Tranzakcióosztály | Alapértelmezett értéke **Idő**. | Az Idő **érték** azt jelzi, hogy a szállítói számlasort használja az alvállalkozói idő számlaösszegének rögzítésére. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projektfeladatnak a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser egyeztetheti a szállítói számlasort a projekt bármely tevékenységén az alvállalkozói erőforrások által rögzített idővel. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz összekapcsolva a nem számlázott értékesítési tényleges adatokkal. Ebben az esetben, ha a feladatalapú számlázás be van állítva, előfordulhat, hogy a költségek nem számlázhatók ki a végfelhasználónak. |
| Beosztás | Azoknak az alvállalkozói erőforrásoknak a szerepe, amelyek idejét kiszámlázzák. | Ez a mező határozza meg azt a szerepkört, amelyet azok az alvállalkozói erőforrások végeznek, amelyek idejét a szállítói számlán számlázzák ki. |
| Lefoglalható erőforrás | Annak az alvállalkozónak a neve, akinek az idejét kiszámlázzák. A foglalható erőforrás kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort egyeztetheti azzal az idővel, amelyet a szállítói számlasor szállítójához tartozó bármely erőforrás rögzít. |
| Mennyiség | Adja meg a szállító által a számlasorban számlázandó órák számát. |None |
| Egységcsoport | Az alapértelmezett érték az Időegység-csoport **,** és nem módosítható. | None |
| Kiszerelés | Az alapértelmezett érték az időegység-csoport óráinak alapegysége. Ezt az értéket úgy módosíthatja, hogy az időegység-csoport bármely egységében, például nap vagy hét egységben vásároljon. | A rendszer a **Szerepkör** és **az Egység** értékek kombinációját használja alapértelmezett vagy számított értékként a **szállítói számlasor Egységár** mezőjéhez. |
| Egységár | Az alapértelmezett egységár a szállítói számlasor tranzakciós dátumára vonatkozó projektárlistából származó Szerepkör **és** Egység **értékek kombinációját** használja. | Ha az alkalmazandó projektárlista ára olyan egységben van beállítva, amely eltér a szállítói számlasor egységétől, a rendszer az egységátváltást használja az egységár kiszámításához. |
| Részösszeg | Ezt a csak olvasható mezőt a rendszer *Mennyiség*&times; egységárként *számítja* ki, ha az értékeket a Mennyiség **mezőben és az** Egységár **mezőben is** meg van adva. Ha az egyik vagy mindkét mező üres, megadhat egy értéket ebben a mezőben. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege, beleértve az adókat is. Ezt a mezőt a rendszer részösszeg *szerinti áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
