---
title: Projektcsoporttagok
description: Ez a témakör a projektcsapattagok információinak, attribútumainak és ütemezésének kezelését ismerteti.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 273736219aff9c2ed4ffa8cf616d6ea656bd7294
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010924"
---
# <a name="project-team-members"></a>Projektcsoporttagok

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektcsapattagok azok a projektrésztvevők, akik végrehajtják a munkát a projekten. A csoporttagrács célja, hogy megadja olyan névvel rendelkező erőforrások listáját, akik elkötelezettek a tevékenységgel kapcsolatban, valamint olyan általános csapattagokat, akik helyőrzőként szolgálnak, és később kerülnek betöltésre.

A csapattagok rácsából a projektmenedzser és a többi projektrésztvevő láthatja, hogy ki lett elkötelezve a projektre. Emellett megtekinthetik a foglalásaik összefoglalását, a tervezett erőfeszítést és az egyes erőforrás-hozzárendeléseket. A csoporttagok rácsa lehetővé teszi, hogy a projektmenedzserek meghatározzák az általános csoporttagok erőforrás-követelményeit, és kezeljék a meglévő csoporttagok foglalásait.

A következő táblázat a projektcsoport egyik tagjának legfontosabb attribútumait sorolja fel.

| Mező neve          | Adatfolyam leírása                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Felosztási mód        | Az erőforrások projekten való könyveléséhez használt felosztási módszer.                                                                         |
| Számlázási típus             | Adja meg, hogy a csoporttag számlázhatóként van-e osztályozva.                                                                                                                                       |
| Lefoglalható erőforrás        | Az általános erőforrás helyettesítésére kijelölt foglalható erőforrás.                                                                                                                   |
| Törlési állapot            | A csoporttag törlési állapotával nyomon követheti, hogy van-e a PSS-nek küldött törlési kérelem, illetve, hogy a PSS sikeresen visszaküldte-e a választ a várt időkereten belül. |
| Összes munkamennyiség (óra)     | A csoporttag feladatokkal kapcsolatos munkamennyiségének összege.                                                                                                                         |
| Befejezett munkamennyiség (óra) | A csoporttag feladattal kapcsolatos elvégzett munkamennyiségének nyomon követése.                                                                                           |
| Hátralévő munkamennyiség (óra) | A csoporttag feladattal kapcsolatos, még el nem végzett munkamennyiségének nyomon követése.                                                                                    |
| Befejezés                   | Az erőforrás csoporttagságának befejező dátuma.                                                                                                                                            |
| Véglegesen lefoglalt órák száma        | A csoporttag véglegesen lefoglalt órái.                                                                                                                                                                |
| Pozíció neve            | Az általános erőforrás azonosítására használt név.                                                                                                                                   |
| Erőforrás-kezelő részleg          | A munkát végrehajtó erőforrás szervezeti egysége.                                                                                                                      |
| Projekt jóváhagyója         | Adja meg, hogy a csoporttag jóváhagyhatja-e az időt és a költségeket.                                                                                                                     |
| Szükséges óraszám           | Csoporttag szükséges órái a csoporttagra vonatkozó követelményekből.                                                                                                                       |
| Szerepkör                     | A csoport tagja által betöltött szerepkör.                                                                                                                                |
| Pozíció leírása     | Adja meg a csoporttag szerepkörének leírását.                                                                                                                             |
| Ideiglenesen lefoglalt órák száma        | A csoporttag ideiglenesen lefoglalt órái.                                                                                                                                                                 |
| Kezdet                    | Az erőforrás csoporttagságának kezdő dátuma.                                                                                                                                          |

A csoporttagok rácsából a következő műveleteket hajthatja végre:

- **Foglalás**: A hibrid foglalási módszertant kihasználó szervezetek esetében a foglalási művelet lehetővé teszi, hogy a felhasználók egy elnevezett erőforrást foglaljanak le az általános csoporttag által előállított szükséges követelmények alapján.
- **Követelmény létrehozása**: Ez a művelet hozza létre a követelményt.
- **Minta megadása**: Lehetővé teszi, hogy a projektmenedzserek részletes szinten módosítsák az erőforrás-szükségletet. A projektmenedzserek a projekt konkrét igényeinek megfelelően módosíthatják azokat az eseteket, amikor az alapértelmezett elosztás nem megfelelő.
- **Kérés elküldése**: A központi foglalási módszert alkalmazó szervezetek számára.
- **Szerkesztés**: A csoporttagok attribútumai szerkeszthetők, beleértve a szervezeti egységet, a szerepkört és a pozíció nevét.
- **Lefoglalások megőrzése**: Amikor az erőforrások foglalását frissíteni kell, a foglalások megőrzése lehetővé teszi, hogy a projektmenedzser módosítsa a következőket:

    - Kezdet
    - End
    - Teljes munkamennyiség elosztása

- **Új**: Az erőforrások közvetlenül az ütemezésből való hozzáadásán túl a projektmenedzserek új névvel rendelkező vagy általános csoporttagokat vehet fel a csoporttagok rácsába.
- **Törlés**: Egy vagy több csoporttag kijelölésével a projektmenedzser törölheti azokat az erőforrásokat, akik már nem fognak részt venni a projektben. A csoporttagok törlésével az összes társított erőforrás-hozzárendelés is törlődik, és a meglévő foglalások visszavonhatók.


[!INCLUDE[footer-include](../includes/footer-banner.md)]