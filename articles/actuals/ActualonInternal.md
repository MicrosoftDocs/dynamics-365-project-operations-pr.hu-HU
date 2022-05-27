---
title: A belső projekt tényleges hatása
description: Ez a témakör a Microsoft belső projektjeinek különböző eseményeinél a Ténylegesek táblára gyakorolt hatásról nyújt tájékoztatást Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579769"
---
# <a name="actuals-impact-for-an-internal-project"></a>A belső projekt tényleges hatása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különböző tranzakciótípusok tényleges adatait sorolja fel, amelyek a belső projektkapcsolat különböző eseményein jönnek létre.

| Esemény | Tényleges költség | Példa |
|---|---|---|
| Az idő létrejön. | Nem alkalmazható | <p>Bob Kozack, a Fabrikam amerikai szervezeti egységtől, amelynek költségára óránként 100 amerikai dollár (100 USD), egy olyan projekten dolgozik, amelynek neve "Arm Installation at Adatum". Ez a projekt a szerződéssorban szereplő rögzített árú számlázási módszerhez van leképezve. Íme egy minta idő bejegyzés Bob Kozaktól:</p><p>Bob Kozack - 8 óra</p> |
| Az idő benyújtásra kerül. | Nem alkalmazható | Az időtételhez költségnaplósor jön létre. Az alapértelmezett költségkamatlábat a naplóbejegyzés írja be. |
| Az időbejegyzést a rendszer a jóváhagyás előtt visszahívja. | Nem alkalmazható | |
| Az idő jóváhagyva. | Létrejön egy tényleges költség. | <p>Új tényleges, amely létrejött:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Az időjóváhagyás megszakad. | <p>Az eredeti tényleges költség helyesbítési állapota helyesbítve **lesz a módosított értékre**.</p><p>Olyan tényleges sztornírozási költség jön létre, amelynek helyesbítési állapota **Nem igazítható**.</p> | <p>A frissített tényleges tényleges érték:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *Korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás megfordítására jött létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Nem módosítható*</li></ul> |
| Az időbejegyzést a rendszer a jóváhagyás után visszahívja. | <p>Az eredeti tényleges költség helyesbítési állapota helyesbítve **lesz a módosított értékre**.</p><p>Olyan tényleges sztornírozási költség jön létre, amelynek helyesbítési állapota **Nem igazítható**.</p> | <p>A frissített tényleges tényleges érték:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *Korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás megfordítására jött létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Nem módosítható*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
