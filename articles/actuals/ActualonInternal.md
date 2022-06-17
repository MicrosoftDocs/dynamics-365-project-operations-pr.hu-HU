---
title: A belső projekt tényleges hatása
description: Ez a cikk a Microsoft belső projektjének különböző eseményeire gyakorolt tényleges adatok táblázatára gyakorolt hatásról nyújt tájékoztatást Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921351"
---
# <a name="actuals-impact-for-an-internal-project"></a>A belső projekt tényleges hatása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a belső projektmegjegyzés különböző eseményein létrehozott különböző tranzakciótípusok tényleges adatait sorolja fel.

| Esemény | Tényleges költség | Példa |
|---|---|---|
| Létrejön az idő. | Nem alkalmazható | <p>Bob Kozack, a Fabrikam amerikai szervezeti egységtől, amelynek költségaránya óránként 100 dollár (100 USD), egy "Arm Installation at Adatum" nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módszerre van leképezve a szerződéssoron. Íme egy minta időbejegyzés Bob Kozaktól:</p><p>Bob Kozack - 8 óra</p> |
| Az idő beküldésre kerül. | Nem alkalmazható | Létrejön egy költségnapló-sor az időbevitelhez. Az alapértelmezett bekerülési érték a naplóbejegyzésben kerül megírásra. |
| A rendszer visszahívja az időbejáratot, mielőtt jóváhagyják. | Nem alkalmazható | |
| Az idő jóváhagyásra kerül. | Létrejön egy tényleges költség. | <p>Új tényleges, létrehozott tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800</li></ul> |
| Az idő-jóváhagyás megszakad. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |
| Az időbevitelt a rendszer a jóváhagyás után visszahívja. | <p>Az eredeti tényleges költség kiigazítási állapota Korrigáltra **frissül**.</p><p>Létrejön egy tényleges visszafordítási költség, amelynek kiigazítási **állapota Kiigazíthatatlan**.</p> | <p>Meglévő tényleges, frissített tényleges:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, USD 800, *korrigált*</li></ul><p>Új tényleges, amely a korábbi pénzügyi hatás visszafordítására jön létre:</p><ul><li>**Tényleges költség:** Bob Kozack, (8 óra), (800 USD), *Kiigazíthatatlan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
