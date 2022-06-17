---
title: Tényleges hatás az elköteleződés értékesítés előtti szakaszában
description: Ez a cikk a Tényleges adatok táblára gyakorolt hatásról nyújt tájékoztatást különböző eseményeken, miközben a csatolás a Microsoft értékesítés előtti szakaszában van Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922363"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Tényleges hatás az elköteleződés értékesítés előtti szakaszában

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különböző tranzakciótípusok tényleges adatait sorolja fel, amelyek a projekt elköteleződésének értékesítés előtti szakaszában különböző eseményeken jönnek létre.

| Esemény | Tényleges költség | Példa |
|---|---|---|
| Létrejön az idő. | Nem alkalmazható | <p>Bob Kozack, a Fabrikam amerikai szervezeti egységtől, amelynek költségaránya óránként 100 dollár (100 USD), egy "Arm Installation at Adatum" nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módszerre van leképezve a szerződéssoron. Íme egy minta időbejegyzés Bob Kozaktól:</p><p>Bob Kozack - 8 óra</p> |
| Az idő beküldésre kerül. | Nem alkalmazható | Létrejön egy költségnapló-sor az időbevitelhez. Az alapértelmezett bekerülési érték a naplóbejegyzésben kerül megírásra. |
| A rendszer visszahívja az időbejáratot, mielőtt jóváhagyják. | Nem alkalmazható | |
| Az idő jóváhagyásra kerül. | Létrejön egy tényleges költség. | <p>Új tényleges, létrehozott tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Az időjóváhagyás megszakad. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |
| Az időbevitelt a rendszer a jóváhagyás után visszahívja. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |
| Az árajánlatot megnyerik, és létrejön egy szerződés. | <p>A régi költség tényleges értékeinek kiigazítási állapota Korrigálva **állapotra** frissül.</p><p>A fordított költség tényleges adatai olyanok jönnek létre, amelyek kiigazítási **állapota Kiigazíthatatlan**.</p><p>Az új költség tényleges adatai a szerződéses szabályok újraértékelése után jönnek létre.</p> | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul><p>Új tényleges adatok, amelyek az árajánlat megnyerésekor és a szerződés létrehozásakor az újraértékelt pénzügyi hatáshoz jönnek létre:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li><li>**Számlázatlan értékesítés tényleges:** Bob Kozack, 8 óra, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
