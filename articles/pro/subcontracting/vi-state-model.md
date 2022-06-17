---
title: Állapotátváltások szállítói számlán
description: Ez a cikk a szállítói számla állapotáttűnéseit ismerteti a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934323"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Állapotátváltások szállítói számlán

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a szállítói számla állapotáttűnéseit ismerteti a Microsoftban Dynamics 365 Project Operations. A rendszer a következő állapotokat használja: **Piszkozat**, **Felülvizsgálat alatt**, **Megerősítve**, **Várakoztatva** és **Törölve**.

Az alábbi ábrák az állapotátmeneteket mutatják be.

![Alvállalkozásba adási állapotátmeneti modell.](../media/VI_State_Model.jpg)

Az alábbi táblázat bemutatja, hogy az egyes állapotok mit jelentenek a szállítói számla életciklusában a Project Operationsben.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az állapot a szállítói számla kezdeti állapota. A sorok és az árak változhatnak. Az ebben az állapotban lévő szállítói számla szerkeszthető és törölhető. | Folyamatban |
| Ellenőrzés alatt | Ez az állapot a szállítói számla feldolgozási állapotát jelöli. Legalább egy szállítói számlasor ellenőrzési állapota **Folyamatban** van. | Megerősítve, várakoztatva |
| Megerősített | Ez az állapot a szállítói számla azon szakaszát jelöli, amelyben az alkalmazás költség-tényleges adatokat hozott létre az egyes szállítói számlasorokhoz. A szállítói számlasorokkal egyeztetett csatolt költség tényleges adatait a rendszer visszavonta, és lecserélte az adott szállítói számlasorokból származó tényleges költségre. Az ebben az állapotban lévő szállítói számla nem szerkeszthető vagy törölhető. A Mégse **gombbal törölheti a** visszaigazolt szállítói számlát. A Mégse művelet visszafordítja a Megerősítés művelet hatását. | Megszakított |
| Várakoztatva | <p>Ez az állapot a szállítói számla azon szakaszát jelöli, ahol a szállítói számla nem helyezhető át a számlával vagy a szállító állapotával kapcsolatos probléma miatt. Az ebben az állapotban lévő szállítói számla nem erősíthető meg, nem törölhető, nem törölhető, nem szerkeszthető és nem törölhető.</p><p>Az Újranyitás művelettel áthelyezheti a szállítói számlát Piszkozat **vagy** **Ellenőrzés alatt** állapotba. Ha a szállítói számlán legalább egy sor ellenőrzési állapota **Folyamatban** vagy **Befejezve**, a szállítói számla újbóli megnyitása Ellenőrzés **alatt** állapotban történik. Ha a szállítói számla összes sora ellenőrzési állapota **Nem kezdődött el**, a szállítói számla Újratervezet **állapotban** lesz.</p> | Tervezet, felülvizsgálat alatt |
| Megszakított | Ez az állapot az alvállalkozói szerződés azon szakaszát jelenti, ahol az anyagok és/vagy az alvállalkozásba adott erőforrásokkal történő tényleges leszállítása már nem szükséges. Ebben az állapotban az alvállalkozói szerződés nem használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetének növelésére, és nem is lehet hivatkozni a projekt időben, költség- és anyaghasználatára. Az ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők vagy törölhetők. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
