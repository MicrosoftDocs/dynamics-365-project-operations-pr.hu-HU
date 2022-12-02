---
title: A tényadatok hatása egy együttműködés értékesítés előtti fázisában
description: Ez a cikk a különböző események a Tényadatok táblára gyakorolt hatásról nyújt tájékoztatást, amikor egy bevonás értékesítés előtti állapotban van a Microsoft Dynamics 365 Project Operations alkalmazásban.
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
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>A tényadatok hatása egy együttműködés értékesítés előtti fázisában

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különféle tranzakciótípusok tényadatait sorolja fel, amelyek a projekt bevonás értékesítési előtti szakaszában a különböző eseményekhez létrejönnek.

| Event | Tényleges költség | Példa |
|---|---|---|
| Létrehozás időpontja. | Nem alkalmazható | <p>Péter, a Fabrikam US szervezeti egységtől, amely 100 dollár (100 USD) óradíjjal dolgozik egy „Arm Installation at Adatum” nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módra van leképezve a szerződéssoron. Íme Bob Balak minta időbevitele:</p><p>Bob Kozack – 8 óra</p> |
| Idő benyújtva. | Nem alkalmazható | Az időbejegyzéshez létrejön egy költségnaplósor. Az alapértelmezett költségdíjat megadják a naplóbejegyzésben. |
| A jóváhagyás előtt visszahívják az időbevitelt. | Nem alkalmazható | |
| Az idő jóvá lett hagyva. | A tényleges költség létrejön. | <p>Létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul> |
| Az idő jóváhagyását visszavonják. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |
| A jóváhagyás után visszahívják az időbevitelt. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |
| Az árajánlatot megnyerik, és létrejön egy szerződés. | <p>A program az eredeti tényleges költség korrekciós állapotát **Korrigálva** értékre módosítja.</p><p>Létrejönnek a sztornírozott költség tényadatok amelyek helyesbítési állapota **Nem korrigálható**.</p><p>A szerződéses szabályok újraértékelése után létrejönnek az új aktuális költségek.</p> | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul><p>Az új tényadatok, amelyeket atértékelt pénzügyi jöttek létre, amikor az árajánlatot elnyerték, és létrehozták a szerződést:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li><li>**Nem számlázott értékesítési tényadat:** Bob Kozack, 8 óra, 1 600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
