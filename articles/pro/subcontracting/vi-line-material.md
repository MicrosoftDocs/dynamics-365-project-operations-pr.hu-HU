---
title: Szállítói számlasorok termékekhez
description: Ez a cikk elmagyarázza, hogyan rögzítse a szállítói számláját, és hogyan használja a különböző mezőket a szállítóktól történő termékbeszerzések rögzítésére.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261561"
---
# <a name="vendor-invoice-lines-for-products"></a>Szállítói számlasorok termékekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái a termékek (más néven anyagok) szállítói számlasorait tartalmazják. A projektvezetők termékekre vonatkozó a szállítóiszámla-sorokat használhatja a projektekhez beszerzett termékek költségének rögzítéséhez.

A termékekhez kapcsolódó szállítói számlasorok hivatkoznak egy alvállalkozói sorra az anyag vonatkozásában. Ha egy termékekhez kapcsolódó alvállalkozó számlasor egy alvállalkozói szerződésre hivatkozik, akkor a projektvezetők egyeztetnie, illetve ellenőrizni tudják a szállító számlasorában szereplő termékeket az alvállalkozók által rögzített és a projektmenedzserek által jóváhagyott beszerzett termékekkel szemben.

Az alábbi táblázat ismerteti az termékekhez kapcsolódó szállítói számlasorok mezőit.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve, amely segítséget nyújt az azonosításában. | Ez a név lesz megjelenítve első oszlopként minden olyan keresésben, amelyek a szállítói számlasorokon alapulnak. |
| Description | Az alvállalkozói számlán a beszállító által számlázott termékek rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozó, amelytől a termékeket eredetileg megrendelték. | Amikor egy alvállalkozói szerződés ki van jelölve a szállítói számlához, a szállítói számla minden sora örökli ezt a beállítást. A szállítói számlákon nem lehetnek olyan szállítói számlasorokat, amelyek más alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozóiszerződés-sor | Az az alvállalkozói sor, amelytől a termékeket megrendelték. A választható alvállalkozói sorok listája a kijelölt alvállalkozó szerződés soraira van korlátozva. | Ha egy alvállalkozó sort kiválaszt egy termékekhez kapcsolódó szállító számlasoron, akkor a **Projekt**, a **Feladat** és a **Termék** mezők alapértelmezett értékeit a program az alvállalkozósor megfelelő mezőiből adja meg. Ha a kijelölt alvállalkozói sornak értékei vannak a **Projekt**, a **Feladat** és a **Termék** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el azoktól az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségét rögzíteni fogják a projekthez. | None|
| Tranzakcióosztály | A termékek számlázásakor ezt a mezőt **Anyag** értékre kell beállítani. | Az **Anyag** érték azt jelzi, hogy a szállító számlasor vásárolt anyagokhoz kapcsolódó számlaösszeg rögzítésére szolgál. |
| Project | Annak a projektnek a neve, amelyhez a számlázott termékeket felhasználták. | Ez egy kötelező mező, és nem lehet üres. |
| Feladatok | Annak a projektfeladatnak a neve, amelyhez a számlázott termékeket felhasználták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projektfeladat kiválasztása nem kötelező. | Ha a mezőt üresen hagyja, akkor a projektvezető a szállító számlasorát megfeleltetheti azokkal a beszerzett termékekkel, amelyek fel lettek használva a projekt bármelyik feladatán. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz társítva egyetlen nem számlázatlan tényleges értékesítéshez sem. Ebben az esetben a feladatalapú számlázás beállítása esetén a költségeket nem lehet a végfelhasználónak kiszámlázni. |
| Termék kiválasztása | Adja meg, hogy a számlázott termék szerepel-e egy meglévő termékkatalógusában vagy nem katalogizált termék. | Az alapértelmezett érték az alvállalkozói sorból lesz megadva az alvállalkozói sor kiválasztásakor. |
| Termék | Válassza ki a terméket a katalógusból. Ha termék nem katalogizált termék, adja meg a termék nevét. | Ebben a mezőben a meglévő termékek alapértelmezett beszerzési árait lehet megadni. |
| Mennyiség | Adja meg a számlasoron a szállító által számlázott anyag mennyiségét. | None |
| Egységcsoport | Válassza ki annak az egységnek az egységcsoportját, amelyben a számlázandó mennyiség ki van kifejezve. | None |
| Kiszerelés | Az alapértelmezett érték a kijelölt egységcsoport alapegysége. Ezt az értéket úgy módosíthatja, hogy a kijelölt egységcsoport bármelyik egységében lehessen fizetni. | A rendszer a **Termék** és az **Egység** értékek kombinációját használja az alvállalkozói szerződéssor **Egységár** mezőjének alapértelmezett vagy számított értékeként. |
| Egységár | Az alapértelmezett egységár projektárlistában szereplő, az alvállalkozói szerződéssor kért tranzakciójának napjára vonatkozó **Termék** és **Egység** kombinációjából adódik. | None |
| Részösszeg | Ez a csak olvasható mező automatikusan a *Mennyiség* &times; *Egységár* képlettel lesz kiszámítva, ha mind a **Mennyiség**, mind az **Egységár** mezőben megadnak értékeket. Ha a mezők egyike üres, akkor ebben a mezőben megadhat értéket. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | Az szállítói számlasor teljes összege az adókkal együtt. Ez a mező a *Részösszeg* + *Forgalmi adó* képlettel kerül kiszámításra. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
