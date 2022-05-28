---
title: Állapotátmenetek szállítói számlán
description: Ez a témakör a Microsoft szállítói számláján lévő állapotátmeneteket ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584691"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Állapotátmenetek szállítói számlán

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft szállítói számláján lévő állapotátmeneteket ismerteti Dynamics 365 Project Operations. A rendszer a következő állapotokat használja: **Vázlat**, **Felülvizsgálat,** **Megerősítés**, **Várakoztatás** és **Visszavont**.

Az alábbi ábra az állapotátmeneteket mutatja be.

![Alvállalkozói állapotátmeneti modell.](../media/VI_State_Model.jpg)

Az alábbi táblázat bemutatja, hogy az egyes állapotok mit képviselnek a Szállítói számla életciklusában a Projektműveletek mezőben.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az állapot a szállítói számla kezdeti állapota. A sorok és az árak módosítás tárgyát képezik. Ebben az állapotban lévő szállítói számla szerkeszthető és törölhető. | Folyamatban |
| Ellenőrzés alatt | Ez az állapot a szállítói számla feldolgozási állapotát jelöli. Legalább egy szállítói számlasor ellenőrzési állapota **Folyamatban van**. | Megerősítve, várakoztatva |
| Megerősített | Ez az állapot a szállítói számla azon szakaszát jelöli, amelyben az alkalmazás minden szállítói számlasorhoz költségalapot hozott létre. A szállítói számlasorokkal egyeztetett kapcsolódó költségalapokat sztorníroztuk, és az adott szállítói számlasorok költségarányaival helyettesítettük. Ebben az állapotban lévő szállítói számla nem szerkeszthető és nem törölhető. A Mégse **gombbal visszavonhatja a** visszaigazolt szállítói számlát. A Mégse művelet megfordítja a Megerősítés művelet hatását. | Megszakított |
| Várakoztatva | <p>Ez az állapot a szállítói számla azon szakaszát jelöli, amelyben a szállítói számla nem tud elmozdulni a számlával vagy a szállító állapotával kapcsolatos probléma miatt. Ebben az állapotban lévő szállítói számla nem erősíthető meg, nem vonható vissza, nem törölhető és nem törölhető.</p><p>Az Újranyitás művelettel áthelyezheti a szállítói számlát a Piszkozat **vagy** a **Felülvizsgálat** állapotban állapotba. Ha a szállítói számlán legalább egy sor ellenőrzési állapota **Folyamatban** vagy **Kész**, a szállítói számla újra megnyílik a **Beellenőrzés** állapotban állapotban. Ha a szállítói számlán szereplő összes sor ellenőrzési állapota **Nem indult** el, a szállítói számla újra megnyílik a **Piszkozat** állapotban.</p> | Vázlat, Felülvizsgálat alatt |
| Megszakított | Ez az állapot az alvállalkozói szerződés azon szakaszát jelenti, amikor az anyagok és/vagy a munka alvállalkozói erőforrásokkal történő tényleges szállítása már nem szükséges. Ebben az állapotban az alvállalkozói szerződések nem használhatók az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére, és nem hivatkozhatnak a projekt időben, költségére és anyaghasználatára sem. Ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és nem törölhetők. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
