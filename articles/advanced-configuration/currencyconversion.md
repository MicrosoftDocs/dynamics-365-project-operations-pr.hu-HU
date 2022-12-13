---
title: Pénznemátváltás beállítása az eladási árak önköltségi árfolyamokból való kiszámításához
description: Ez a cikk bemutatja, hogyan konfigurálhatja a Microsoftban Dynamics 365 Project Operations használt pénznemátváltási viselkedést, amikor az értékesítési tranzakciókat költségtranzakciókból generálják.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816691"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Pénznemátváltás beállítása az eladási árak önköltségi árfolyamokból való kiszámításához

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Microsoftban Dynamics 365 Project Operations a költségkategóriák eladási árai beállíthatók numerikus értékekként, vagy beállíthatók úgy, hogy a felmerült költségek alapján számítsák ki őket.

Ha úgy vannak beállítva, hogy a felmerült költségek alapján legyenek kiszámítva, a következő lehetőségek állnak rendelkezésre:

- Költségen
- Százalékos áremelkedés a költséghez képest

Azokban az esetekben, amikor a költség olyan pénznemben merül fel, amely eltér a projektszerződés értékesítési pénznemétől, pénznemátváltásra van szükség az eladási ár költség alapján történő kiszámításához.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Natív Dataverse árfolyamokat használó pénznemátváltási viselkedés

Alapértelmezés szerint a Project Operations a Pénznem táblában tárolt valutaárfolyamokat használja Dataverse. Ha úgy szeretné beállítani a Project Operations rendszert, hogy natív árfolyamokat használjon az eladási árak költségből való kiszámításához, kövesse az alábbi lépéseket.

1. Lépjen a Project Operations **beállításainak \> paraméterei lapra \>**.
1. Nyissa meg a **Projektparaméter** részletei lapot.
1. Állítsa a **Pénznemek közötti átváltási logika** mezőt üres értékre.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>A pénzügy- és műveletalkalmazások árfolyamait használó pénznemátváltási viselkedés

A Pénznem táblában szereplő átváltási árfolyamok, amelyek natív módon elérhetők Dataverse , nem érvényesek. Ezért előfordulhat, hogy nem mindig az eladási árak költségdíjakból történő kiszámításához szükséges követelményekhez vannak méretezve.

A pénzügyi és üzemeltetési környezet árfolyamai segítségével kiszámíthatja az eladási árat az értékesítési pénznemben a költség pénznemében lévő költségárfolyamból. A pénznemek közötti átváltási viselkedés konfigurálásához kövesse az alábbi lépéseket.

1. A **Projektparaméterek** lapon adja hozzá a **Pénznemátváltási logika** mezőt. Ezután mentse és tegye közzé a testreszabást.
1. Lépjen a Project Operations **beállításainak \> paraméterei lapra \>**.
1. Nyissa meg a **Projektparaméter** részletei lapot. 
1. Állítsa a **Pénznemek közötti átváltási viselkedés** mezőt Kiterjesztettre, alapértelmezettre **állítva**.
1. Adjon engedélyt a Kettős írású alkalmazás felhasználó **biztonsági szerepkör globális**  olvasási **engedélyének a** következő táblákhoz:

    - MSDYN\_ Valutaátváltási árfolyamok
    - MSDYN\_ ValutaÁrfolyampárok
    - MSDYN\_ árfolyamtípusok

1. A pénzügyi és üzemeltetési környezetben futtassa a következő kettős írású leképezéseket a kezdeti szinkronizálással:

    - Árfolyamtípus (msdyn\_ árfolyamtípusok)
    - Árfolyam devizapár (msdyn\_ currencyexchangeratepairs)
    - CDS árfolyamok (msdyn\_ valutaárfolyamok)

Miután ezek a módosítások befejeződtek, a kettős írás elérhetővé teszi a pénzügyi és üzemeltetési környezet Dataverse árfolyamait. A Project Operations ezután ezeket az árfolyamokat használja a költségárfolyamok átváltására a szerződés értékesítési pénznemére.

> [!NOTE]
> Ez a pénznemek közötti átváltási viselkedés csak az eladási árak költségárfolyamokból történő kiszámítására vonatkozik. Nem használható az alapdevizaértékek általános kiszámításához. Az alappénznem-értékek mindig natív Dataverse árfolyamokat fognak használni, függetlenül attól, hogy végrehajtja-e ezt az eljárást.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
