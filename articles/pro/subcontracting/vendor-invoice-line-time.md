---
title: Szállítói számlasorok időhöz
description: Ez a cikk ismerteti, hogyan rögzítheti a szállítói számlasorokat az alvállalkozók által megadott időköltségekre.
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

A Microsoft Dynamics 365 Project Operations szállítói számlái rendelkeznek időhöz kapcsolódó szállítóiszámla-sorokkal A projektvezetők időre vonatkozó a szállítóiszámla-sorokat használhatja az alvállalkozók időköltségének rögzítésére a projekteken.

Az időhöz kapcsolódó szállítói számlasorok hivatkoznak egy alvállalkozói sorra az idő vonatkozásában. Ha egy időhöz kapcsolódó alvállalkozó számlasor egy alvállalkozói szerződésre hivatkozik, akkor a projektvezetők egyeztetnie, illetve ellenőrizni tudják a szállító számlasorában szereplő időt az alvállalkozók által rögzített és a projektmenedzserek által jóváhagyott idővel szemben.

Az alábbi táblázat ismerteti az időhöz kapcsolódó szállítói számlasorok mezőit.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve, amely segítséget nyújt az azonosításában. | Ez a név lesz megjelenítve első oszlopként minden olyan keresésben, amelyek a szállítói számlasorokon alapulnak. |
| Description | Az alvállalkozói számlán a beszállító által számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozó, amelytől a szolgáltatásokat eredetileg megrendelték. | Amikor egy alvállalkozói szerződés ki van jelölve a szállítói számlához, a szállítói számla minden sora örökli ezt a beállítást. A szállítói számlákon nem lehetnek olyan szállítói számlasorokat, amelyek más alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozóiszerződés-sor | Az az alvállalkozói sor, amelytől a szolgáltatásokat megrendelték. A választható alvállalkozói sorok listája a kijelölt alvállalkozó szerződés soraira van korlátozva. | Ha egy alvállalkozó sort kiválaszt egy időhöz kapcsolódó szállító számlasoron, akkor a **Projekt**, a **Szerepkör** és a **Foglalható erőforrás** mezők alapértelmezett értékeit a program az alvállalkozósor megfelelő mezőiből adja meg. Ha a kijelölt alvállalkozói sornak értékei vannak a **Projekt**, a **Szerepkör** és a **Foglalható** mezőkben, a szállítói számlasor megfelelő mezőinek értékei nem térhetnek el azoktól az értékektől. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségét rögzíteni fogják a projekthez. | None |
| Tranzakcióosztály | Alapértelmezett értéke **Idő**. | Az **Idő** érték azt jelzi, hogy a szállítói számlasor az alvállalkozó által megadott idő rögzítésére használatos. |
| Project | Annak a projektnek a neve, amelyhez a számlázott szolgáltatásokat felhasználták. | Ez egy kötelező mező, és nem lehet üres. |
| Feladatok | Annak a projektfeladatnak a neve, amelyhez a számlázott szolgáltatásokat felhasználták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projektfeladat kiválasztása nem kötelező. | Ha a mezőt üresen hagyja, akkor a projektvezető a szállító számlasorát megfeleltetheti az alvállalkozói erőforrások által a projekt bármely feladatához rögzített időnek. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz társítva egyetlen nem számlázatlan tényleges értékesítéshez sem. Ebben az esetben a feladatalapú számlázás beállítása esetén előfordulhat, hogy a költségeket nem lehet a végfelhasználónak kiszámlázni. |
| Beosztás | Azon alvállalkozói erőforrások szerepe, akiknek az idejét számlázzák. | Ez a mező azt a szerepkört adja meg, amelyet az alvállalkozói erőforrások végeznek el, akik ideje a szállító számláján ki van számlázva. |
| Lefoglalható erőforrás | Annak az alvállalkozónak a neve, akiknek az idejét számlázzák. A foglalható erőforrás kiválasztása nem kötelező. | Ha a mezőt üresen hagyja, akkor a projektvezető a szállító számlasorát megfeleltetheti az időnek, amit egy olyan erőforrás rögzített, a melyik a szállítói számlasor szállítójához tartozik. |
| Mennyiség | Adja meg, hogy hány órán át számláz a szállító a számlasoron. |None |
| Egységcsoport | Az alapértelmezett érték az **Időegység csoport**, és ez nem módosítható. | None |
| Kiszerelés | Az alapértelmezett érték az órák időegység-csoportja az idő egységcsoportból. Ezt az értéket úgy módosíthatja, hogy az időegység csoport bármelyik egységét, például napot vagy hetet vásárolhassa meg. | A rendszer a **Szerepkör** és az **Egység** értékek kombinációját használja az alvállalkozói szerződéssor **Egységár** mezőjének alapértelmezett vagy számított értékeként. |
| Egységár | Az alapértelmezett egységár projektárlistában szereplő, az alvállalkozói szerződéssor kért tranzakciójának napjára vonatkozó **Szerep** és **Egység** kombinációjából adódik. | Ha az alkalmazandó projektárlistában beállított ár eltér a szállítói számlában szereplő egységtől eltérő egységben határozza meg, a rendszer az egységár kiszámításához az egységre történő átváltást használja. |
| Részösszeg | Ez a csak olvasható mező automatikusan a *Mennyiség* &times; *Egységár* képlettel lesz kiszámítva, ha mind a **Mennyiség**, mind az **Egységár** mezőben megadnak értékeket. Ha a mezők egyike üres, akkor ebben a mezőben megadhat értéket. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | Az szállítói számlasor teljes összege az adókkal együtt. Ez a mező a *Részösszeg* + *Forgalmi adó* képlettel kerül kiszámításra. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
