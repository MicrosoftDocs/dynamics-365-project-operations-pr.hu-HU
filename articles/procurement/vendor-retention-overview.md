---
title: Szállítói visszatartás– áttekintés
description: Ez a cikk áttekintést ad a szállítói visszatartás képességről.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916843"
---
# <a name="vendor-retention-overview"></a>Szállítói visszatartás– áttekintés

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Előfordulhat, hogy a szervezetnél vissza szeretné tartani a fizetés egy részét a vállalatnál projekteken munkát vállaló szállítóknak. Mielőtt például fizet a szállítónak, lehet, hogy meg szeretne bizonyosodni arról, hogy az adott cikkek és szolgáltatások megfelelnek az elvárásainak.

Projektekhez kapcsolódó vásárlások a szállítókkal való megtárgyalása során megadhat visszatartási feltételeket, ami lehet visszatartott százalék vagy összeg. Amint a szállító tételeket és szolgáltatásokat szállítja, levonja a megadott visszatartott százalékot vagy összeget a szállítónak történő kifizetésből. Amikor a projekt befejeződött, vagy a szállítói szerződésben meghatározott ideiglenes fázisba ér, a visszatartott összeget felszabadíthatja, és létrehoz a szállítónak a kifizetést.

## <a name="vendor-retention-example"></a>Szállítói visszatartás példája

A következő példa azt mutatja be, hogyan van visszatartva a szállítói számla összegének százalékos értéke a projekthez teljesítettségének százaléka alapján.

A Contoso Robotics USA szerződést kötött a Fabrikam szállítóval, hogy 100 órás oktatóanyagot nyújt a berendezés felújítási projektje számára. A teljes szerződésérték USD 30 000, óránként 300 USD beszerzési árral.

A képzés három fázisban lesz szállítva a következő ütemezéssel:

- 1. fázis: 50 óra, vagy a projekt 50%-a
- 2. fázis: 30 óra, vagy a projekt összesen 80%-a
- 3. fázis: 20 óra, vagy a projekt 100%-a

A következő táblázat felsorolja a visszatartási feltételeket.

| **A leszállított egységek százalékos értéke** | **Visszatartott százalék** | **Kiadandó százalék** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

A tranzakciók a következő összegeket eredményezik:

- 1. fázis:
  - A kifizetendő összeg 50 x 300 vagy 15 000.
  - A az összeg 20%-a, azaz 3000 vissza van tartva, és egy későbbi fázisban lesz felszabadítva.
  - Az szállítónak kifizetett összeg 12 000.
- 2. fázis:
  - A kifizetendő összeg 30 x 300 vagy 9000.
  - Az összeg 10 százaléka, vagyis 900 vissza van tartva.
  - Az 1. fázisban megtartott 3 000 10%-a, vagyis 300 fel van szabadítva.
  - Az szállítónak kifizetett összeg 8400.. Ez az összeg 9 000, mínusz 900 visszatartás valamint az 1. fázis visszatartásából felszabadított 300.
- 3. fázis:
  - A kifizetendő összeg 20 x 300 vagy 6000.
  - Nincs visszatartott összeg.
  - A kiadott összeg 3600. Ez az összeg az 1. fázisban megtartott 3 000-ből áll, mínusz a 300, ami az 1. fázisból fel lett szabadítva a 2. fázisban, plusz a 900, ami vissza lett tartva a 2. fázisban.
  - Az szállítónak kifizetett összeg 9600. Ez az összeg a visszatartott 3600, valamint a 3. fázis befejezéséért járó 6 000 összegből áll.

A három fázis teljesítése után az szállítónak kifizetett teljes összeg 30 000, ez a megrendelés teljes összege (15 000 + 9 000 + 6 000).
