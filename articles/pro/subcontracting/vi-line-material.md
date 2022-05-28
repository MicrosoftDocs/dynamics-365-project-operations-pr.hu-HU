---
title: Termékek szállítói számlasorai
description: Ez a témakör bemutatja, hogyan rögzítheti a termékek szállítói számlasorait, és hogyan rögzítheti a különböző mezőket a szállítóktól származó termékbeszerzések rögzítéséhez.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599181"
---
# <a name="vendor-invoice-lines-for-products"></a>Termékek szállítói számlasorai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoftban Dynamics 365 Project Operations a szállítói számlák szállítói számlasorai lehetnek a termékekhez (más néven anyagokhoz). A projektmenedzserek a termékek szállítói számlasoraival rögzíthetik a projekteken beszerzett termékek költségeit.

A termékek szállítói számlasorai hivatkozhatnak vagy nem hivatkoznak alvállalkozói sorra az anyagokhoz. Ha a termékek szállítói számlasora alvállalkozói szerződésre hivatkozik, a projektmenedzserek össze tudják egyeztetni és ellenőrizni tudják a szállítói számlasor által számlázott termékeket a projektmenedzserek által rögzített és jóváhagyott beszerzett termékek használatával.

Az alábbi táblázat a termékek szállítói számlasorainak mezőiről tartalmaz tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve az azonosításhoz. | Ez a név jelenik meg első oszlopként a szállítói számlasorokon alapuló összes keresésben. |
| Description | A szállító által a szállító számlasorban számlázott termékek rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozói szerződés, amelyre a termékeket eredetileg megrendelték. | Ha a szállítói számlához alvállalkozói szerződés van kiválasztva, a szállítói számla összes sora örökli ezt a kijelölést. A szállítói számlákon nem lehetnek különböző alvállalkozókra hivatkozó szállítói számlasorok. |
| Alvállalkozói sor | Az az alvállalkozói sor, amelyen a termékeket megrendelték. A kijelölhető alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha a termékek szállítói számlasorában alvállalkozói sor van kiválasztva, a Program, **a Tevékenység** és **a Termék** mezők alapértelmezett értékeit a **program** az alvállalkozósor megfelelő mezőiből adja meg. Ha a kijelölt alvállalkozói sor értékei a Projekt **,** a Tevékenység **és** a **Termék** mezőben találhatók, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költség-tényleges értékét rögzítik a projektben. | None|
| Tranzakcióosztály | A termékek számlázásakor ezt a mezőt Anyag **értékre** kell állítani. | Az Anyag **érték** azt jelzi, hogy a szállítói számlasor a beszerzett anyagok számlaösszegének rögzítésére szolgál. |
| Project | Annak a projektnek a neve, amelyen a számlázandó termékeket használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projekttevékenységnek a neve, amelyen a számlázandó termékeket használták. Ez a mező csak akkor érhető el, ha projekt van kijelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort a projekt bármely tevékenységéhez használt beszerzett termékkel egyeztetheti. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz hozzárendelve nem hozzárendelt értékesítési tényleges értékekkel. Ebben az esetben, ha feladatalapú számlázás van beállítva, a költségeket nem lehet számlázni a végfelhasználónak. |
| Termék kiválasztása | Válassza ki, hogy a számlázandó termék a katalógusból származó meglévő termék vagy beírt termék. | Az alapértelmezett érték az alvállalkozói sorból lesz beírva, amikor alvállalkozói sor van kijelölve. |
| Termék | Válassza ki a terméket a katalógusból. Ha a termék beírt termék, adja meg a termék nevét. | Ez a mező a meglévő termékek alapértelmezett beszerzési árainak megadására szolgál. |
| Mennyiség | Adja meg a számlasorban szereplő szállító által számlázott anyag mennyiségét. | None |
| Egységcsoport | Válassza ki annak az egységnek az egységcsoportját, amelyben a számlázandó mennyiség kifejeződik. | None |
| Kiszerelés | Az alapértelmezett érték a kijelölt egységcsoport alapegysége. Ezt az értéket a kijelölt egységcsoport bármely egységében módosíthatja. | A program a Termék **és** az **Egység** értékek kombinációját használja alapértelmezett vagy számított értékként a **szállítói számlasor Egységár** mezőjéhez. |
| Egységár | Az alapértelmezett egységár a szállítói **számlasor tranzakciós dátumára alkalmazandó projektárlista Termék** - és **Egységértékeinek** kombinációját használja. | None |
| Részösszeg | Ezt az írásvédett mezőt a program *Mennyiségi*&times; egységárként *számítja* ki, ha az értékeket mind a Mennyiség **, mind** az **Egységár** mezőben beírja. Ha az egyik vagy mindkét mező üres, ebben a mezőben megadhat egy értéket. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege az adókkal együtt. Ezt a mezőt a program részösszeg *áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
