---
title: Szállítói számlasorok mérföldkövekhez
description: Ez a cikk ismerteti, hogyan lehet alvállalkozói szerződésen létrehozni a szállító számlasorokat a mérföldkövek számára.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260998"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Szállítói számlasorok mérföldkövekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái az alvállalkozói sorban definiált mérföldkövekhez szállítói számlasorokat tartalmazhatnak. A projektvezetők a mérföldkövek szállítói számlasorait használhatják a projekthez kapcsolódó, mérföldköveken alapuló költségekként beszerzett szolgáltatásokhoz vagy termékekhez kapcsolódó költségeket.

A mérföldkövek szállítói számlasorának mindig hivatkozni kell egy Rögzített árú számlázási módú alvállalkozói sorhoz. Ha egy mérföldkövekhez tartozó szállítói számlasor egy alvállalkozói sorra hivatkozik, a projektvezetők egyeztethetik és ellenőrizhetik a mögöttes idő, kiadások vagy anagyok költségét, amelyek az alvállalkozói sorra hivatkoznak a szállító által számlázott mérföldkővel szemben.

Az alábbi táblázat ismerteti a mérföldkövekhez kapcsolódó szállítói számlasorok mezőit.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve, amely segítséget nyújt az azonosításában. | Ez a név lesz megjelenítve első oszlopként minden olyan keresésben, amelyek a szállítói számlasorokon alapulnak. |
| Description | Az alvállalkozói számlán a beszállító által számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozó, amelytől a szolgáltatásokat eredetileg megrendelték. | Amikor egy alvállalkozói szerződés ki van jelölve a szállítói számlához, a szállítói számla minden sora örökli ezt a beállítást. A szállítói számlákon nem lehetnek olyan szállítói számlasorokat, amelyek más alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozóiszerződés-sor | Az az alvállalkozói sor, amelytől a szolgáltatásokat megrendelték. A választható alvállalkozói sorok listája a kijelölt alvállalkozó szerződés soraira van korlátozva. | Ha egy alvállalkozó sort kiválaszt egy mérföldkövekhez tartozó szállítói számlasoron, akkor a **Szerepkör** és a **Tranzakciókategória** mezők, illetve a termékhez kapcsolódó mezők nem érhetők el. A **Mennyiség**, az **Egység** és az **Egységcsoport** mező nem releváns a mérföldkő alapú szállítói számlasorok szempontjából. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségét rögzíteni fogják a projekthez. | None |
| Tranzakcióosztály | Válassza a **Mérföldkő** lehetőséget, hogy rögzítsen egy szállítói számlát egy teljesített mérföldkőhöz, amely egy alvállalkozói soron lett definiálva. | None |
| Mérföldkő | Válassza ki azt a mérföldkövet, amely a **Számlázásra kész** jelölésű kapcsolódó alvállalkozói sorban van definiálva. | A **Számlázásra kész** állapottal rendelkező alvállalkozóisor-mérföldkövek nem jelölhetők ki egy szállítói számlasoron. |
| Project | Annak a projektnek a neve, amelyhez a számlázott szolgáltatásokat felhasználták. | Ez egy kötelező mező, és nem lehet üres. |
| Feladatok | Annak a projektfeladatnak a neve, amelyhez a számlázott szolgáltatásokat felhasználták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projektfeladat kiválasztása nem kötelező. | Ha a mezőt üresen hagyja, akkor a projektvezető a szállító számlasorát megfeleltetheti az a projekt bármelyik feladatához rögzített kapcsolódó alvállalkozói sor tranzakcióosztályainak. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz társítva egyetlen nem számlázatlan tényleges értékesítéshez sem. Ebben az esetben a feladatalapú számlázás beállítása esetén előfordulhat, hogy a költségeket nem lehet a végfelhasználónak kiszámlázni. |
| Mérföldkő összege | Adja meg annak a mérföldkőnek az értékét, amely a számlázásra kész alvállalkozói sorban van definiálva. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | Az szállítói számlasor teljes összege az adókkal együtt. A mező számításának képlete *Mérföldkő összege* + *Áfa*. | None |

> [!NOTE]
> Az alvállalkozói sor mérföldkövére hivatkozó szállítói számlasor létrehozásakor az alvállalkozói mérföldkövek állapota **Szállítói számla létrehozva** értékre módosul. Ezt követően, amikor a szállító számlája megerősítést nyer, az alvállalkozói sor mérföldkövének állapota **Szállítói számla megerősítve** értékre lesz frissítve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
