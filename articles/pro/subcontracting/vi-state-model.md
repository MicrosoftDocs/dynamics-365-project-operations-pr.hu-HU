---
title: Állapotátváltások szállítói számlán
description: Ez a cikk ismerteti a szállítói számlára vonatkozó állapotátváltásokat a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261019"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Állapotátváltások szállítói számlán

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk ismerteti a szállítói számlára vonatkozó állapotátváltásokat a Microsoft Dynamics 365 Project Operations alkalmazásban. A következő állapotok használatosak: **Vázlat**, **Ellenőrzés alatt**, **Megerősítve**, **Visszatartva** és **Visszavonva**.

A következő ábrán ezek az állapotátmenetek láthatók:

![Az alvállalkozói szerződés állapotátmeneti modellje.](../media/VI_State_Model.jpg)

A következő táblázat azt mutatja be, hogy az egyes állapotok mit képviselnek a Project Operations szállítóiszámla-életciklusában.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az állapot a szállítói számlák kezdeti állapota. A sorok és az árképzés is változhatnak. Az ebben az állapotban lévő szállítói számla nem szerkeszthető vagy törölhető. | Folyamatban |
| Ellenőrzés alatt | Ez az állapot a szállítói számlák feldolgozási állapotát jelenti. Legalább egy szállítói számla ellenőrzési állapota **Folyamatban**. | Megerősítve, Visszatartva |
| Megerősítve | Ez az állapot a szállítói számláknak azt a fázisát jelenti, ahol az alkalmazás minden egyes szállítói számlasorhoz létrehozta a költség tényadatait. A rendszer minden, a szállító számlasorával egyeztetett költség-tényadatot visszavont, és lecserélte az adott szállítói számla soraiból származó költség-tényadatokkal. Az ebben az állapotban lévő szállítói számla nem szerkeszthető vagy törölhető. A **Mégse** gomb segítségével visszavonhatja a megerősített szállítói számlát. A Mégse művelet visszavonja a Megerősítés művelet hatását. | Megszakított |
| Várakoztatva | <p>Ez az állapot a szállítói számlák egy olyan fázisát jelenti, ahol a szállítói számla nem tud haladni mert a számlával vagy a szállító állapotával probléma van. Az ebben az állapotban lévő szállítói számla nem erősíthető meg, vonható vissza, szerkeszthető vagy törölhető.</p><p>Az Újranyitás művelet segítségével áthelyezheti a szállító számláját **Vázlat** vagy **Ellenőrzés alatt** állapotba. Ha a szállítói számla legalább egy sorának állapota **Folyamatban** vagy **Kész**, a szállító számláját a rendszer újra megnyitja **Ellenőrzés alatt** állapotban. Ha a szállítói számla minden sorának **Nincs elindítva** az ellenőrzési állapota, a szállítói számla **Vázlat** állapotból újra meg lesz nyitva.</p> | Vázlat, Ellenőrzés alatt |
| Megszakított | Ez az fázis az alvállalkozói szerződésnek az a fázisa, amikor az anyagok szállítása és/vagy az alvállalkozói erőforrások által történő elvégzése már nem szükséges. Az ebben az állapotban alvállalkozói szerződés nem használhatók fel az erőforrások és anyagok projektkövetelményének becslésére és személyzeti hozzárendelésére, és nem hivatkozhat egy projekten időre, költségre és anyaghasználatra sem. Az ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és törölhetők. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
