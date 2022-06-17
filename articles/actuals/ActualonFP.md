---
title: Tényleges hatás rögzített ármegállapításban
description: Ez a cikk a Microsoft rögzített árú elköteleződésének életciklusa során a Tényleges adatok táblára gyakorolt hatásról nyújt tájékoztatást különböző eseményeken Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918131"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Tényleges hatás rögzített ármegállapításban

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különböző tranzakciótípusok tényleges adatait sorolja fel, amelyek rögzített árú elköteleződés esetén különböző eseményeken jönnek létre.

| Esemény | Tényleges költség | Számlázatlan értékesítés tényleges | Számlázott értékesítés tényleges | Példa |
|---|---|---|---|---|
| Létrejön az idő. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | <p>Bob Kozack, a Fabrikam amerikai szervezeti egységtől, amelynek költségaránya óránként 100 dollár (100 USD), egy "Arm Installation at Adatum" nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módszerre van leképezve a szerződéssoron. Íme egy minta időbejegyzés Bob Kozaktól:</p><p>Bob Kozack - 8 óra</p> |
| Az idő beküldésre kerül. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | Létrejön egy költségnapló-sor az időbevitelhez. Az alapértelmezett bekerülési érték a naplóbejegyzésben kerül megírásra. |
| A rendszer visszahívja az időbejáratot, mielőtt jóváhagyják. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| Az idő jóváhagyásra kerül. | Létrejön egy tényleges költség. | Nem alkalmazható | Nem alkalmazható | <p>Új tényleges, létrehozott tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Az időjóváhagyás megszakad. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | Nem alkalmazható | Nem alkalmazható | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |
| Az időbevitelt a rendszer a jóváhagyás után visszahívja. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | Nem alkalmazható | Nem alkalmazható | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |
| A szerződést megerősítik. | <p>A régi költség tényleges értékeinek kiigazítási állapota Korrigálva **állapotra** frissül.</p><p>A fordított költség tényleges adatai olyanok jönnek létre, amelyek kiigazítási **állapota Kiigazíthatatlan**.</p><p>Az új költség tényleges adatai a szerződéses szabályok újraértékelése után jönnek létre.</p> | Nem alkalmazható | Nem alkalmazható | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul><p>Új tényleges, amely az újraértékelt pénzügyi hatáshoz jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Létrejön egy számla. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| A számlát egy mérföldkővel erősítjük meg. | Nem alkalmazható | Nem alkalmazható | A rendszer új, mérföldkőalapú, számlázott értékesítési tényleges adatokat hoz létre. | <p>Meglévő tényleges, változatlan marad:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul><p>Új tényleges, amely a számlázott értékesítési értékek rögzítéséhez jön létre:</p><ul><li>**Tényleges számlázás:** Milestone, USD 5,000</li></ul> |
| A számlát kijavítják a mérföldkő jóváírásához. | Nem alkalmazható | Nem alkalmazható | A rendszer megfordítja a számlázott értékesítési tényleges adatokat. | <p>Meglévő tényleges, változatlan marad:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul><p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges számlázás:** Mérföldkő, USD 5,000, *korrigált*</li></ul><p>Új tényleges, amely a korábbi számlázott értékesítési értékek megfordításához jön létre:</p><ul><li>**Tényleges számlázás:** Milestone, (5,000 USD), *Kiigazíthatatlan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
