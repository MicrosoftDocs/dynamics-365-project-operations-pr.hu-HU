---
title: Mérföldkövek szállítói számlasorai
description: Ez a témakör bemutatja, hogyan hozhat létre szállítói számlasorokat az alvállalkozói szerződések mérföldköveihez.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590625"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Mérföldkövek szállítói számlasorai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations szállítói számlái szállítói számlasorokat tartalmazhatnak az alvállalkozói sorban definiált mérföldkövekhez. A projektmenedzserek a mérföldkövekhez szállítói számlasorok segítségével rögzíthetik a projekthez beszerzett szolgáltatások vagy termékek esetében felmerülő mérföldkőalapú költségekként beszerzett szolgáltatások költségeit.

A mérföldkövek szállítói számlasorainak mindig olyan alvállalkozói sorra kell hivatkozniuk, amely rögzített árú számlázási módszerrel rendelkezik. Amikor a mérföldkövek szállítói számlasora alvállalkozói sorra hivatkozik, a projektmenedzserek össze tudják egyeztetni és ellenőrizni tudják az adott alvállalkozói sorra hivatkozó idő, költség vagy anyag mögöttes költségét a szállító által számlázott mérföldkőhöz képest.

Az alábbi táblázat a mérföldkövek szállítói számlasoraiban szereplő mezőiről tartalmaz tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számlasor neve az azonosításhoz. | Ez a név jelenik meg első oszlopként a szállítói számlasorokon alapuló összes keresésben. |
| Description | A szállító által a szállító által a szállító számlasorban számlázott szolgáltatások rövid leírása. | None |
| Alvállalkozói szerződés | Az az alvállalkozói szerződés, amelyre a szolgáltatásokat eredetileg megrendelték. | Ha a szállítói számlához alvállalkozói szerződés van kiválasztva, a szállítói számla összes sora örökli ezt a kijelölést. A szállítói számlákon nem lehetnek különböző alvállalkozókra hivatkozó szállítói számlasorok. |
| Alvállalkozói sor | Az alvállalkozói vonal, amelyen a szolgáltatásokat megrendelték. A kijelölhető alvállalkozói sorok listája a kiválasztott alvállalkozói szerződés soraira korlátozódik. | Ha egy alvállalkozási sor a mérföldkövek szállítói számlasorában van kiválasztva, a Szerepkör **és** a Tranzakció kategória **mezők, valamint a** termékkel kapcsolatos mezők irrelevánsak és nem érhetők el. A **Mennyiség**, **az Egység** és **az Egység csoport** mezők szintén nem relevánsak a mérföldkőalapú szállítói számlasorok esetében. |
| Tranzakció dátuma | Az a dátum, amikor a szállítói számlasor tényleges költség-tényleges értékét rögzítik a projektben. | None |
| Tranzakcióosztály | Válassza a Mérföldkő **lehetőséget** egy alvállalkozói sorban definiált befejezett mérföldkő szállítói számlájának rögzítéséhez. | None |
| Mérföldkő | Válassza ki a kapcsolódó alvállalkozói sorban definiált mérföldkövet, amely a Számlázásra **készként** van megjelölve. | A szállítói számlasorban kiválaszthatók azok az alvállalkozói **sor mérföldkövek, amelyek állapota Kész számla**. |
| Project | Annak a projektnek a neve, amelyen a számlázandó szolgáltatásokat használták. | Ez a mező kötelező, és nem hagyható üresen. |
| Feladatok | Annak a projekttevékenységnek a neve, amelyen a számlázandó szolgáltatásokat használták. Ez a mező csak akkor érhető el, ha projekt van kijelölve. A projekttevékenység kiválasztása nem kötelező. | Ha ez a mező üresen marad, a projektmenedzser a szállítói számlasort a kapcsolódó alvállalkozói sor tranzakcióosztályával egyeztetheti, amely a projekt bármely tevékenységén rögzítésre kerül. Ha a szállítói számlasor nem hivatkozik alvállalkozói sorra, és ez a mező üresen marad, a szállítói számlasor által létrehozott tényleges költség nem lesz hozzárendelve nem hozzárendelt értékesítési tényleges értékekkel. Ebben az esetben, ha feladatalapú számlázás van beállítva, előfordulhat, hogy a költségeket nem lehet számlázni a végfelhasználónak. |
| Mérföldkő összege | Adja meg a számlázásra kész alvállalkozói sorban definiált mérföldkő értékét. | None |
| Forgalmi adó | Adja meg az áfa összegét. | None |
| Végösszeg | A szállítói számlasor teljes összege az adókkal együtt. Ezt a mezőt a program Mérföldkő összege *Áfa áfaként* + *számítja* ki. | None |

> [!NOTE]
> Amikor létrejön egy alvállalkozói sor mérföldkőjére hivatkozó szállítói számlasor, az alvállalkozói mérföldkő állapota a létrehozott **Szállító számlára** frissül. Ezután a szállítói számla megerősítésekor az alvállalkozói sor mérföldkőjének állapota a szállítói számla megerősítésére **frissül**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
