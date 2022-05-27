---
title: Állapotátváltások az alvállalkozói szerződésben
description: Ez a témakör a Microsoft Dynamics 365 Project Operations alvállalkozói szerződésének állapotátmeneteit ismerteti az alvállalkozó létrehozása, végrehajtása és lezárása során.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579171"
---
# <a name="state-transitions-on-a-subcontract"></a>Állapotátváltások az alvállalkozói szerződésben 

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft alvállalkozói szerződésének állapotátmeneteit ismerteti Dynamics 365 Project Operations. Minden állam piszkozatként, megerősítettként, lezártként vagy visszavontként jelenik meg. Az alábbi kép az állapotátmeneteket mutatja be.

![Alvállalkozói állapotmodell](../media/SubconStates.png)  

Az alábbi táblázat leírja, hogy az egyes állapotok mit képviselnek a Projektműveletek alvállalkozás életciklusában.

| State | Description | Engedélyezett átmenetek |
| --- | --- | --- |
| Piszkozat | Ez az alvállalkozói szerződés kezdeti állapotát jelenti. A szállítóval folytatott tárgyalások folyamatban vannak. A sorok és az árképzés módosítás tárgyát képezik. Ebben az állapotban alvállalkozói szerződés használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. A projekt időben, költség- és anyaghasználatában is hivatkozhat rá. Ebben az állapotban lévő alvállalkozók szerkeszthetők és törölhetők. | Megerősített |
| Megerősített | Ez az alvállalkozói szerződés szakaszát jelenti, miután befejeződtek a szállítóval az árképzésről és a megvásárolt sortételekről folytatott tárgyalások. Az anyagok és/vagy munkák alvállalkozói erőforrásokkal történő tényleges szállítása azonban még folyamatban van. Ebben az állapotban alvállalkozói szerződés használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. A projekt időben, költség- és anyaghasználatában is hivatkozhat rá. Ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és nem törölhetők. A **Mégse** gomb lehetővé teszi a visszaigazolt alvállalkozói szerződés megszakítását. Az **Újranyitás** gomb lehetővé teszi az alvállalkozó újbóli megnyitását, hogy visszaállítsa **a Piszkozat** állapotba. **A Bezárás** gombbal zárjon be egy megerősített alvállalkozót. | Bezárva <br> Megszakított <br> Piszkozat |
| Bezárva | Ez az alvállalkozói szerződés azon szakaszát jelenti, amikor az anyagok és/vagy munkák alvállalkozói erőforrásokkal történő tényleges szállítása befejeződik. Ebben az állapotban az alvállalkozói szerződés már nem használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére. Ezenkívül már nem hivatkozhat a projekt időben, költségére és anyaghasználatára. Ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és nem törölhetők. | None |
| Megszakított | Ez az alvállalkozói szerződés azon szakaszát jelenti, amikor az anyagok és/vagy a munka alvállalkozói erőforrásokkal történő tényleges szállítása már nincs szükség. Ebben az állapotban az alvállalkozói szerződés nem használható az erőforrásokra és anyagokra vonatkozó projektkövetelmények becslésére és személyzetére, és nem hivatkozhat a projekt időben, költségére és anyaghasználatára sem. Ebben az állapotban lévő alvállalkozói szerződések nem szerkeszthetők és nem törölhetők. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
