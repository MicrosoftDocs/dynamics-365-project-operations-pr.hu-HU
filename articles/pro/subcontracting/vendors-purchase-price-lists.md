---
title: A szállítói és a beszerzési árlista kezelése a Project Operations alkalmazásban
description: A témakör nyújt tájékoztatást a szállítói adatok létrehozásához és karbantartásához, valamint az alvállalkozók árlistáihoz.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994144"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>A szállítói és a beszerzési árlista kezelése a Project Operations alkalmazásban

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

## <a name="vendors-in-project-operations"></a>Szállítók a Project Operations alkalmazásban

A Microsoft Dynamics 365 Project Operations alkalmazásban szállítói fióknak egy **Szállító** vagy **Beszállító** kapcsolattípusa van. Csak olyan partnerrekordot választhat ki, amely alvállalkozóként az ilyen kapcsolattípusok valamelyikével rendelkezik az alvállalkozói szerződésen.

Egy vagy több beszerzési árlistát társíthat egy szállítói bejegyzéshez. Azonban minden, a szállítói rekordhoz társított beszerzési árlistának külön dátumhatállyal kell bírni. A Project Operations nem támogatja a beszerzési árlisták dátumának átfedő hatályosságát.

Alapértelmezés szerint a következő mezők és fogalmak használatosak a szállító számára létrehozott alvállalkozói szerződésekhez:

- Fizetési feltételek
- Számlázás kapcsolattartónak
- Elsődleges kapcsolattartó

    > [!NOTE]
    > Alapértelmezés szerint a szállító elsődleges kapcsolattartója az alvállalkozó szállítói partnerkezelője.

- Pénznem
- Aktuális beszerzési árlisták

## <a name="purchase-price-lists-in-project-operations"></a>Beszerzési árlisták a Project Operations alkalmazásban

Az az árlista, ahol a **Környezet** mező beállítása **Beszerzés** beszerzési árlistának számít. A beszrzési árlisták az beszerzési idő, kiadások és anyagok katalógusának számítanak. A beszerzési árlisták a Project Operations költség- és értékesítési árlistáihoz hasonlítanak. A következő fogalmak a vásárlási árlistákra ugyanúgy vonatkoznak, mint a költség- és értékesítési árlistákra:

- **Hatályossági dátum** – A beszerzési árlisták hatályossági dátummal rendelkeznek. A hatályossági dátumot a kezdő és a záró dátum mező képviseli minden árlistán. A kezdő és a záró dátum közötti idő a hatályossági dátum időszaka.
- **Pénznem** – Az árlistafejlécen található pénznem az a pénznem, amelyben a beszerzési árak a katalógusban a munkához a költségkategóriákhoz és a termékekhez ki van fejezve.
- **Alapértelmezett időegység** – Az alapértelmezett időegység a vásárlások munkadíjaira vonatkozik. Az árlista időegység-mezője csak alapértelmezett értékkel használható. Ez az érték a szerepkör ársorainál módosítható.

A beszerzési árlisták csatolhatók szállítói rekordokhoz és ezek a társítások a projektárlisták. Ezek az árlisták használhatók az alapértelmezett árak alvállalkozói sorokban való megadására. Alapértelmezés szerint ha több beszerzési árlistát csatol egy szállítói rekordhoz, akkor a rendszer a legújabb árlistát használja a beszállító számára létrehozott alvállalkozói szerződésekhez. Csak azok az árlisták csatolhatóak a szállítói rekordokhoz, amelyek **Környezet** mezőjében a **Beszerzés** beállítás van beállítva.

### <a name="subcontract-specific-purchase-price-lists"></a>Alvállalkozóiszerződés-specifikus beszerzési árlisták

A beszerzési árlisták csatolhatók alvállalkozói szerződésekhez, és ezek a társítások a projektárlisták. Ezek az árlisták használhatók az alapértelmezett árak alvállalkozói sorokban való megadására. Ha egy alvállalkozóhoz több beszerzési árlistát csatolnak, alapértelmezés szerint mindegyiknek külön hatályossági dátummal kell bírni. A Project Operations nem támogatja a beszerzési árlisták dátumának átfedő hatályosságát. Csak azok az árlisták csatolhatóak a alvállalkozói szerződésekhez, amelyek **Környezet** mezőjében a **Beszerzés** beállítás van beállítva.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
