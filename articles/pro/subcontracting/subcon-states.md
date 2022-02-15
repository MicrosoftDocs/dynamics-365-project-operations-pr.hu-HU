---
title: Állami átállás egy alvállalkozón
description: Ez a témakör a Microsoft alvállalkozóinak állami átmeneteit ismerteti Dynamics 365 Project Operations az alvállalkozó létrehozása, végrehajtása és lezárása során.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903679"
---
# <a name="state-transitions-on-a-subcontract"></a>Állami átállás egy alvállalkozón 

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft alvállalkozóinak állami átmeneteit ismerteti Dynamics 365 Project Operations. Minden állam tervezetként, megerősítettként, lezártként vagy töröltként 1000.000.000.000.000.000.000. Az alábbi kép az állapotátmeneteket mutatja.

![Alvállalkozói állapotmodell](../media/SubconStates.png)  

Az alábbi táblázat leírja, hogy az egyes államok mit képviselnek a Projektműveletek alvállalkozói életciklusában.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az alvállalkozók kezdeti állapotát jelenti. Az eladóval jelenleg is folynak a tárgyalások. A sorok és az árképzés módosítások tárgyát képezik. Ebben az államban egy alvállalkozó használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. A projekt időben, költségén és anyaghasználatán is hivatkozhat. Ebben az állapotban egy alvállalkozó szerkeszthető és törölhető. | Megerősített |
| Megerősített | Ez az alvállalkozói szakaszt jelenti, miután a szállítóval folytatott tárgyalások az árképzésről és a megvásárolt sorokról befejeződtek. Az anyagok tényleges szállítása és/vagy az alvállalkozói forrásokból végzett munka azonban még folyamatban van. Ebben az államban egy alvállalkozó használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. A projekt időben, költségén és anyaghasználatán is hivatkozhat. Ebben az állapotban egy alvállalkozó nem szerkeszthető vagy törölhető. A **Mégse** gomb lehetővé teszi a megerősített alvállalkozók lemondását. Az **Újranyitás** gomb lehetővé teszi az alvállalkozó újbóli megnyitását, hogy visszaállítsa a **piszkozat** státuszba. A **Bezárás** gombbal zárjon be egy megerősített alvállalkozót. | Bezárva <br> Megszakított <br> Piszkozat |
| Bezárva | Ez az alvállalkozói szakaszt jelenti, amikor az anyagok tényleges szállítása és / vagy az alvállalkozói erőforrásokból végzett munka befejeződik. Ebben az államban az alvállalkozók már nem használhatók fel az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. Ezenkívül már nem lehet hivatkozni a projekt időben, költségén és anyaghasználatán. Ebben az állapotban egy alvállalkozó nem szerkeszthető vagy törölhető. | None |
| Megszakított | Ez az alvállalkozói szakaszt jelenti, amikor az anyagok tényleges szállítása és/vagy az alvállalkozói erőforrásokból történő munka már nincs szükség. Ebben az államban az alvállalkozók nem használhatók fel az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére, és nem hivatkozhatnak arra időben, költségként és anyagfelhasználáskor egy projekten. Ebben az állapotban egy alvállalkozó nem szerkeszthető vagy törölhető. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]