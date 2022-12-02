---
title: A tényadatok hatása egy belső projektben
description: Ez a cikk a különböző események a Tényadatok táblára gyakorolt hatásról nyújt tájékoztatást egy belső projekthez Microsoft Dynamics 365 Project Operations alkalmazásban.
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
# <a name="actuals-impact-for-an-internal-project"></a>A tényadatok hatása egy belső projektben

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű központi telepítés – proforma számlázás_

Az alábbi táblázat a különféle tranzakciótípusok tényadatait sorolja fel, amelyek egy belső projektben a különböző eseményekhez létrejönnek.

| Event | Tényleges költség | Példa |
|---|---|---|
| Létrehozás időpontja. | Nem alkalmazható | <p>Péter, a Fabrikam US szervezeti egységtől, amely 100 dollár (100 USD) óradíjjal dolgozik egy „Arm Installation at Adatum” nevű projekten dolgozik. Ez a projekt egy rögzített árú számlázási módra van leképezve a szerződéssoron. Íme Bob Balak minta időbevitele:</p><p>Bob Kozack – 8 óra</p> |
| Idő benyújtva. | Nem alkalmazható | Az időbejegyzéshez létrejön egy költségnaplósor. Az alapértelmezett költségdíjat megadják a naplóbejegyzésben. |
| A jóváhagyás előtt visszahívják az időbevitelt. | Nem alkalmazható | |
| Az idő jóvá lett hagyva. | A tényleges költség létrejön. | <p>Létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD</li></ul> |
| Az időjóváhagyást visszavonják. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |
| A jóváhagyás után visszahívják az időbevitelt. | <p>A program az eredeti tényleges költség állapotát **Helyesbítve** értékre módosítja .</p><p>Létrejön egy sztornírozott költség tényadat amelynek helyesbítési állapota **Nem korrigálható**.</p> | <p>Frissített meglévő tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack, 8 óra, 800 USD *Korrigált*</li></ul><p>Az előző pénzügyi hatás sztornírozásához létrehozott új tényadat:</p><ul><li>**Tényleges költség:** Bob Kozack (8 óra), (800 USD) *Nem korrigálható*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
