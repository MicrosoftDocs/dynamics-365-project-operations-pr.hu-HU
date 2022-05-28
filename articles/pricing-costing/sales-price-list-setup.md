---
title: Értékesítési árlista beállítása
description: Ez a témakör az értékesítési árlisták projektek árképzéséhez történő beállítását ismerteti.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cb4153e05359c17c1536e06f220e21465be899fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582667"
---
# <a name="set-up-a-sales-price-list"></a>Értékesítési árlista beállítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektárajánlatok és -szerződések esetében a projekt árlistájának eltérő árfelülbírálási mintázata van, mint egy termék árlistájának. Egy termékkatalóguson alapuló árajánlati soron felülbírálhatja az árat a szerepkörökre és kategóriákra közvetlenül az árajánlatsorban, mert minden ajánlati sor pontosan egy katalóguselemre mutat. Projektalapú árajánlati soron azonban nem lehet felülbírálni az árakat szerepkörökre és kategóriákra közvetlenül az árajánlati soron. A projekt árlistája két külön felülbírálási mintával használható.

> [!NOTE]
> Javasoljuk, hogy legyen külön árlista a projekterőforrásokhoz és a katalóguselemekhez, a kettő közötti viselkedési különbségek miatt az árak felülbírálásakor.

A következő entitások mindegyike rendelkezik egy vagy több kapcsolódó értékesítési árlistával a projekt árazásához:

- Ügyfél (fiók) 
- Lehetőség 
- Ajánlat 
- Projektszerződés

Ezeknek az entitásoknak az árlistához való társulását a projekt árlistái jelzik. Egy vagy több árlistát társíthat az Ügyfél, a Lehetőség, az Ajánlat és a Projektszerződés értékesítési entitásokhoz.

Az alapértelmezett projektárlistát nem automatikusan írják be az ügyfélrekordba. A projekt árlistáját azonban manuálisan csatolhatja az ügyfélrekordhoz. Ennek ellenére csak akkor kell manuálisan csatolnia a projekt árlistáját, ha egyedi árazási megállapodást kötött az ügyféllel. 

Ha egy projektárlistát csatolnak egy értékesítési entitáshoz, a rendszer a következő információkat ellenőrzi:

- Az árlista rendelkezik **Értékesítés** környezettel. 
- Az árlista pénzneme megegyezik az ügyfél pénznemével. 

A projektszerződéseken a következő prioritási sorrend használatos a kapcsolódó projektárlisták automatikus beállításához:

1. Ajánlat
2. Lehetőség
3. Ügyfél 
4. Globális beállítások 

Amikor egy projektárlistát alapértelmezés szerint ad meg, a rendszer ellenőrzi, hogy a pénznem megegyezik-e az ügyfél pénznemével, és hogy a megadott alapértelmezett árlisták az **Értékesítés** kontextusban vannak-e.

Összekapcsolhat több projektárlistát az Ügyfél, a Lehetőség, az Ajánlat és a Projekt szerződéses entitásokkal. Ez a képesség támogatja a hosszú ideje működő projektszerződés dátum-specifikus alapértelmezett árait, ahol több árlistára lehet szükség az infláció miatt bekövetkező árfrissítések elszámolására. Azonban ha az Ügyfél, a Lehetőség, az Ajánlat vagy a Projektszerződés entitással társított árlisták hatálya átfedésben van, akkor az alapértelmezett árak helytelenek lehetnek. Ezért biztosítania kell, hogy az átfedő hatályú projektárak ne legyenek társítva ezekhez az entitásokhoz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]