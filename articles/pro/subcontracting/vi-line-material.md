---
title: Szállítói számlasorok termékekhez
description: Ez a cikk azt ismerteti, hogyan rögzítheti a termékek szállítói számlasorait, és hogyan használhatja a különböző mezőket a szállítóktól származó termékvásárlások rögzítésére.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931379"
---
# <a name="vendor-invoice-lines-for-products"></a>Szállítói számlasorok termékekhez

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlája szállítói számlasorokat tartalmazhat a termékekhez (más néven anyagokhoz). A projektmenedzserek a termékek szállítói számlasorai segítségével rögzíthetik a projekteken vásárolt termékek költségeit.

Előfordulhat, hogy a termékek szállítói számlasorai nem hivatkoznak alvállalkozói sorra az anyagokhoz, vagy nem. Ha a termékekhez tartozó szállítói számlasor alvállalkozói szerződésre hivatkozik, a projektmenedzserek egyeztethetik és ellenőrizhetik a szállítói számlasor által számlázott termékeket a projektmenedzserek által rögzített és jóváhagyott vásárolt termékek használatával.

Az alábbi táblázat a termékek szállítói számlasorainak mezőiről nyújt tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve, hogy segítsen az azonosításban. | Ez a név jelenik meg az első oszlopként az összes olyan keresésben, amely a szállítói számlasorokon alapul. |
| Description | A szállító által a szállítói számlasoron számlázandó termékek rövid leírása. | None |
| Alvállalkozói szerződés | Az alvállalkozói szerződés, amelyre a termékeket eredetileg megrendelték. | Ha alvállalkozói szerződést választ a szállítói számlához, a szállítói számla összes sora örökli ezt a beállítást. A szállítói számlák nem tartalmazhatnak olyan szállítói számlasorokat, amelyek különböző alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozói vonal | Az alvállalkozói vonal, amelyen a termékeket megrendelték. A kiválasztható alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy alvállalkozói sor van kiválasztva egy szállítói számlasoron a termékekhez, a Projekt **,** a Tevékenység **és** a **Termék** mezők alapértelmezett értékei az alvállalkozói sor megfelelő mezőiből kerülnek beírásra. Ha a kiválasztott alvállalkozói sor értékeket tartalmaz a Projekt **,** a Tevékenység **és** a **Termék** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el ezektől az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségének tényleges költséget rögzíti a projektben. | None|
| Tranzakcióosztály | A termékek számlázásakor ezt a mezőt Anyag **értékre** kell állítani. | Az Anyag **érték** azt jelzi, hogy a szállítói számlasort használják a megvásárolt anyagok számlaösszegének rögzítésére. |
| Project | Annak a projektnek a neve, amelyről a számlázandó termékeket felhasználták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projekttevékenységnek a neve, amelyről a számlázandó termékeket felhasználták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort a projekt bármely tevékenységéhez használt megvásárolt termékkel egyeztetheti. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz összekapcsolva a nem számlázott értékesítési tényleges adatokkal. Ebben az esetben, ha a feladatalapú számlázás be van állítva, a költségek nem lesznek képesek számlázni a végfelhasználónak. |
| Termék kiválasztása | Válassza ki, hogy a számlázandó termék a katalógus meglévő terméke vagy egy beírt termék. | Az alapértelmezett érték az alvállalkozói sorból kerül megírásra, ha egy alvállalkozói sor van kiválasztva. |
| Termék | Válassza ki a terméket a katalógusból. Ha a termék egy beírt termék, adja meg a termék nevét. | Ez a mező a meglévő termékek alapértelmezett beszerzési árainak megadására szolgál. |
| Mennyiség | Adja meg a szállító által számlázandó anyagmennyiséget ebben a számlasorban. | None |
| Egységcsoport | Válassza ki annak az egységnek az egységcsoportját, amelyben a számlázandó mennyiség ki van fejezve. | None |
| Kiszerelés | Az alapértelmezett érték a kiválasztott egységcsoport alapegysége. Ezt az értéket módosíthatja úgy, hogy a kiválasztott egységcsoport bármely egységében fizessen. | A termék **- és** egységértékek **kombinációja** lesz a szállítói számlasor Egységár **mezőjének** alapértelmezett vagy számított értéke. |
| Egységár | Az alapértelmezett egységár a termék és **az egység** értékének **kombinációját** használja a projekt árlistájából, amely a szállítói számlasor tranzakciós dátumára vonatkozik. | None |
| Részösszeg | Ezt a csak olvasható mezőt a rendszer *Mennyiség*&times; egységárként *számítja* ki, ha az értékeket a Mennyiség **mezőben és az** Egységár **mezőben is** meg van adva. Ha az egyik vagy mindkét mező üres, megadhat egy értéket ebben a mezőben. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege, beleértve az adókat is. Ezt a mezőt a rendszer részösszeg *szerinti áfaként* + *számítja* ki. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
