---
title: A tényadatok hatásai rögzített árú együttműködésben
description: Ez a cikk a különböző események a Tényadatok táblára gyakorolt hatásról nyújt tájékoztatást, egy rögzített árú együttműködés során a Microsoft Dynamics 365 Project Operations alkalmazásban.
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
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>A tényadatok hatásai rögzített árú együttműködésben

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különféle tranzakciótípusok tényadatait sorolja fel, amelyek egy rögíztett árú együttműködésben a különböző eseményekhez létrejönnek.

| Event | Tényleges költség | Számlázatlan értékesítés tényleges | Számlázott értékesítési tényadat | Példa |
|---|---|---|---|---|
| Létrehozás időpontja. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | <p>Péter, a Fabrikam US szervezeti egységtől, amely 100 dollár (100 USD) óradíjjal dolgozik egy „Arm Installation at Adatum” nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módra van leképezve a szerződéssoron. Íme Bob Balak minta időbevitele:</p><p>Bob Kozack – 8 óra</p> |
| Idő benyújtva. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | Az időbejegyzéshez létrejön egy költségnaplósor. Az alapértelmezett költségdíjat megadják a naplóbejegyzésben. |
| A jóváhagyás előtt visszahívják az időbevitelt. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| Az idő jóvá lett hagyva. | A tényleges költség létrejön. | Nem alkalmazható | Nem alkalmazható | <p>Létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul> |
| Az idő jóváhagyását visszavonják. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | Nem alkalmazható | Nem alkalmazható | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |
| A jóváhagyás után visszahívják az időbevitelt. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | Nem alkalmazható | Nem alkalmazható | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |
| A szerződést megerősítették. | <p>A program az eredeti tényleges költség korrekciós állapotát **Korrigálva** értékre módosítja.</p><p>Létrejönnek a sztornírozott költség tényadatok amelyek helyesbítési állapota **Nem korrigálható**.</p><p>A szerződéses szabályok újraértékelése után létrejönnek az új aktuális költségek.</p> | Nem alkalmazható | Nem alkalmazható | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul><p>Az átértékelt pénzügyi hatáshoz létrejött új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul> |
| Létrejön egy számla. | Nem alkalmazható | Nem alkalmazható | Nem alkalmazható | |
| A számlát egy mérföldkővel megerősítik. | Nem alkalmazható | Nem alkalmazható | Létrejönnek az új, mérföldkőalapú számlázott értékesítési tényadatok. | <p>Változatlan meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul><p>A számlázott értékesítési értékek rögzítéséhez létrehozott új tényadat:</p><ul><li>**Számlázott tényleges értékesítés:** Mérföldkő, 5 000 USD</li></ul> |
| A számla javításra kerül a mérföldkő jóváírásaként. | Nem alkalmazható | Nem alkalmazható | A sztornírozott számlázott értékesítések tényadatok létrejönnek. | <p>Változatlan meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul><p>Frissített meglévő tényadat:</p><ul><li>**Számlázott tényleges értékesítés:** Mérföldkő, 5 000 USD, *Korrigált*</li></ul><p>A korábban számlázott értékesítési értékek sztornírozásához létrehozott új tényadat:</p><ul><li>**Számlázott tényleges értékesítés:** Mérföldkő, (5 000 USD), *Nem korrigálható*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
