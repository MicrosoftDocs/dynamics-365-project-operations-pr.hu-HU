---
title: Szállítói számlasorok mérföldkövekhez
description: Ez a cikk azt ismerteti, hogyan hozhat létre szállítói számlasorokat az alvállalkozói szerződések mérföldköveihez.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931333"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Szállítói számlasorok mérföldkövekhez

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái rendelkezhetnek szállítói számlasorokkal az alvállalkozói sorban meghatározott mérföldkövekhez. A projektmenedzserek a mérföldkövekhez használt szállítói számlasorok segítségével rögzíthetik a projekthez beszerzett szolgáltatásokkal vagy termékekkel kapcsolatban felmerülő mérföldkő-alapú költségekként beszerzett szolgáltatások költségeit.

A mérföldkövek szállítói számlasorainak mindig olyan alvállalkozói sorra kell hivatkozniuk, amely rögzített árú számlázási módszerrel rendelkezik. Amikor a mérföldkövekhez tartozó szállítói számlasor alvállalkozói sorra hivatkozik, a projektmenedzserek egyeztethetik és ellenőrizhetik az adott alvállalkozói sorra hivatkozó idő- és költségköltségeket, költségeket vagy anyagokat a szállító által kiszámlázott mérföldkővel.

Az alábbi táblázat a szállítói számlasorok mérföldkövek mezőiről nyújt tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve, hogy segítsen az azonosításban. | Ez a név jelenik meg az első oszlopként az összes olyan keresésben, amely a szállítói számlasorokon alapul. |
| Description | A szállító által a szállítói számlasoron számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az alvállalkozás, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha alvállalkozói szerződést választ a szállítói számlához, a szállítói számla összes sora örökli ezt a beállítást. A szállítói számlák nem tartalmazhatnak olyan szállítói számlasorokat, amelyek különböző alvállalkozói szerződésekre hivatkoznak. |
| Alvállalkozói vonal | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kiválasztható alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy szállítói számlasoron alvállalkozói sor van kiválasztva a mérföldkövekhez, a Szerepkör **és** a Tranzakciós kategória **mezők, valamint a** termékkel kapcsolatos mezők irrelevánsak és nem érhetők el. A **Mennyiség**, **a Mennyiség és** a **Mennyiség csoport** mezők szintén nem relevánsak a mérföldkőalapú szállítói számlasorok esetében. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költségének tényleges költséget rögzíti a projektben. | None |
| Tranzakcióosztály | Válassza a Mérföldkő **lehetőséget** egy alvállalkozói sorban meghatározott befejezett mérföldkő szállítói számlájának rögzítéséhez. | None |
| Mérföldkő | Válassza ki a kapcsolódó alvállalkozói sorban meghatározott mérföldkövet, amely számlakészként **van** megjelölve. | Az alvállalkozói sor mérföldkövei, amelyek állapota Készen áll a **számlára**, kiválaszthatók a szállítói számlasoron. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projektfeladatnak a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha egy projekt ki van jelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ezt a mezőt üresen hagyja, a projektmenedzser a szállítói számlasort a kapcsolódó alvállalkozói sorban lévő tranzakciós osztálynak megfelelően egyeztetheti, amelyet a projekt bármely tevékenységénél rögzítenek. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz összekapcsolva a nem számlázott értékesítési tényleges adatokkal. Ebben az esetben, ha a feladatalapú számlázás be van állítva, előfordulhat, hogy a költségek nem számlázhatók ki a végfelhasználónak. |
| Mérföldkő összege | Adja meg a mérföldkő értékét, amely a számlázásra kész alvállalkozói sorban van meghatározva. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege, beleértve az adókat is. Ez a mező Mérföldkő *összege* + *Áfaként* kerül kiszámításra. | None |

> [!NOTE]
> Amikor létrejön egy alvállalkozói sor mérföldkövére hivatkozó szállítói számlasor, az alvállalkozói mérföldkő állapota létrejön **szállítói számlára**. Ezután a szállítói számla megerősítésekor az alvállalkozói sor mérföldkövének állapota a Szállítói számla visszaigazolt **állapotára** frissül.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
