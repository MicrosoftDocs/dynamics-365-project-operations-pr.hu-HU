---
title: Tényleges hatás egy rögzített árú megbízásban
description: Ez a témakör a Microsoft rögzített árú kötelezettségvállalásának életciklusa során a Ténylegesek táblára gyakorolt hatásról nyújt tájékoztatást Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579231"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Tényleges hatás egy rögzített árú megbízásban

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat felsorolja a különböző tranzakciótípusok tényleges adatait, amelyek különböző eseményeken, rögzített árú megbízásban jönnek létre.

| Esemény | Tényleges költség | Számlázatlan értékesítés tényleges | Számlázott értékesítés tényleges | Példa |
|---|---|---|---|---|
| Az idő létrejön. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | <p>Bob Kozack, a Fabrikam amerikai szervezeti egységtől, amelynek költségára óránként 100 amerikai dollár (100 USD), egy olyan projekten dolgozik, amelynek neve "Arm Installation at Adatum". Ez a projekt a szerződéssorban szereplő rögzített árú számlázási módszerhez van leképezve. Íme egy minta idő bejegyzés Bob Kozaktól:</p><p>Bob Kozack - 8 óra</p> |
| Az idő benyújtásra kerül. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | Az időtételhez költségnaplósor jön létre. Az alapértelmezett költségkamatlábat a naplóbejegyzés írja be. |
| Az időbejegyzést a rendszer a jóváhagyás előtt visszahívja. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| Az idő jóváhagyva. | Létrejön egy tényleges költség. | Nem alkalmazható | Nem alkalmazható | <p>Új tényleges, amely létrejött:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Az időjóváhagyás megszakad. | <p>Az eredeti tényleges költség helyesbítési állapota helyesbítve **lesz a módosított értékre**.</p><p>Olyan tényleges sztornírozási költség jön létre, amelynek helyesbítési állapota **Nem igazítható**.</p> | Nem alkalmazható | Nem alkalmazható | <p>A frissített tényleges tényleges érték:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *Korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás megfordítására jött létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Nem módosítható*</li></ul> |
| Az időbejegyzést a rendszer a jóváhagyás után visszahívja. | <p>Az eredeti tényleges költség helyesbítési állapota helyesbítve **lesz a módosított értékre**.</p><p>Olyan tényleges sztornírozási költség jön létre, amelynek helyesbítési állapota **Nem igazítható**.</p> | Nem alkalmazható | Nem alkalmazható | <p>A frissített tényleges tényleges érték:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *Korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás megfordítására jött létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Nem módosítható*</li></ul> |
| A szerződés megerősítést nyert. | <p>A régi költség tényleges értékének helyesbítési állapota Helyesbítve **értékre** frissül.</p><p>A sztornírozási költség tényleges adatai olyan sztornírozási költségmegállapítások jönnek létre, amelyek helyesbítési állapota **Nem igazítható**.</p><p>A szerződéses szabályok újraértékelése után új költségalapokat hoznak létre.</p> | Nem alkalmazható | Nem alkalmazható | <p>A frissített tényleges tényleges érték:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *Korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás megfordítására jött létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Nem módosítható*</li></ul><p>Új tényleges, amely az újraértékelt pénzügyi hatás érdekében jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Létrejön egy számla. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| A számlát egy mérföldkővel erősítik meg. | Nem alkalmazható | Nem alkalmazható | Új mérföldkő alapú számlázott értékesítési tényleges értékek jönnek létre. | <p>Meglévő tényleges, változatlan marad:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul><p>A számlázott eladási értékek rögzítésére létrehozott új tényleges érték:</p><ul><li>**Számlázott értékesítés tényleges:** Milestone, USD 5,000</li></ul> |
| A program kijavítja a számlát a mérföldkő jóváírásához. | Nem alkalmazható | Nem alkalmazható | A program sztornírozott értékesítési tényleges adatokat hoz létre. | <p>Meglévő tényleges, változatlan marad:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul><p>A frissített tényleges tényleges érték:</p><ul><li>**Számlázott értékesítés tényleges:** Mérföldkő, USD 5,000, *Helyesbítve*</li></ul><p>Az előző számlázott eladási értékek sztornírozására létrehozott új tényleges érték:</p><ul><li>**Számlázott értékesítés tényleges:** Milestone, (USD 5,000), *Nem kiigazítható*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
