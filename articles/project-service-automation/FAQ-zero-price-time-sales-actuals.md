---
title: Az ár miért alapértelmezett nulla a tényleges a tényleges időértékesítéseknél?
description: Annak meghatározása, hogy az ár miért alapértelmezett nulla a tényleges a tényleges időértékesítéseknél
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752247"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Az ár miért alapértelmezett nulla a tényleges a tényleges időértékesítéseknél?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ez a gyakori kérdések rész azokra a tényleges költségekre vonatkozik, ahol a tranzakcióosztály Idő értékre van állítva, és tranzakció Számlázatlan értékesítés. A következő három ellenőrzés segít a hibaelhárításban, hogy az ár (számlázási díj) miért alapértelmezetten 0 a tényleges időköltségeknél.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>1. ellenőrzés: Azonosítsa az értékesítési árlistát a projekthez

Keresés a projektet a tényleges projektmezőjében, és ugorjon a projektlapra. Majd menjen az Értékesítés lapra, és Projektszerződés sorai rácson kattintson a hivatkozásra a Projektszerződés mezőben. A projektszerződés oldal jelenik meg. A Projektszerződés oldalon nyissa meg a Projektárlisták lapot. Ellenőrizze, hogy legalább egy árlista van-e itt. Ha a Projektszerződés Árlisták rácsában nincs csatolva egyetlen árlista sem, azonosította a problémát. Csatoljon egy árlistát a Projektárlisták rácshoz. Az árlistáknak, amelyeket itt csatolni lehet rendelkezniük kell egy kontextusmezővel a Sales-hez, és az árlista a pénznem mezőjének egyeznie kell a pénznem mezőjével. Amikor kész a szükséges javításokkal, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy a számlázatlan aktuális értékesítés az érvényes árat mutatja-e. 

Ha több csatolt árlista van csatolva a Projektárlisták rácshoz, ugorjon a következő ellenőrzésre a dokumentumban.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>2. ellenőrzés: A fentebb felsorolt árlisták bármelyike érvényese a tényleges időértékesítés napján?

Ahhoz, hogy a Project Service alapértelmezett árként vegye figyelembe az árlistát, az árlistának vonatkoznia kell az időértékesítés dátumán. Ellenőrizze a következőket, hogy a fentebb felsorolt árlisták érvényesek-e:
- Ellenőrizze, hogy a csatolt árlisták kezdő és befejező dátumai nem üresek-e az Általános lapon. Ha a kezdő és befejező dátumok fent azonosított árlistáknál üresek, akkor azonosította a problémát. 
- Jegyezze fel a tényleges időértékesítés kezdő dátum mezőjének tartalmát és ellenőrizze, hogy az azonosított árlisták bármelyike vonatkozik-e erre a dátumra. Például a tényleges időértékesítés dátuma az árlista kezdő és befejező dátuma közé kell essen. 
    - Ha nincs olyan árlista, amely vonatkozik a tényleges időértékesítés dátumára, akkor a problémát azonosította. Módosítsa az árlista kezdő és befejező dátumait annak érdekében, hogy az árlista vonatkozzon az időértékesítés a dátumára. 
    - Ha több olyan árlista van, amely vonatkozik a tényleges időértékesítés dátumára, akkor a problémát azonosította. Ezt úgy javíthatja, hogy az árlisták kezdő- és befejező dátumait úgy módosítja hogy csak egy árlista vonatkozzon, a tényleges időértékesítés dátumára. 
    - Ha csak egy árlista érvényes a tényleges időértékesítés dátumára, ugorjon a 3. ellenőrzésre.
Amikor kész a szükséges javításokkal, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy a tényleges időértékesítés az érvényes árat mutatja-e.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>3. ellenőrzés: Van egy ár az árlistában az árazási dimenziókhoz a tényleges időértékesítéshez?

Ha sikeresen befejezte az 1. és 2 ellenőrzést, most már rendelkezik csak egy árlistával rendelkezik, amely érvényes a tényleges időértékesítés napján. Nyissa meg a ezt az árlistát, és lépjen a Szerepkörárak lapra. Győződjön meg arról, hogy van egy sor a rácson az árazási dimenziókhoz a tényleges időértékesítésnél.

Ha nincs sor a szerepkörár rácson az árazási dimenzióhoz a tényleges időértékesítésnél, azonosította a problémát. Hozzon létre egy sort Szerepkörárak rácson az árazási dimenziókhoz a tényleges időértékesítésnél. Amikor végzett ezzel, hozzon létre újra egy időbejegyzést, és győződjön meg arról, hogy a tényleges időértékesítés az érvényes árat mutatja-e.

Ha még mindig nem látható érvényes árat az tényleges időértékesítésnél miután elvégezte a három ellenőrzést, hozzon létre egy támogatási jegyet. 

