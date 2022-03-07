---
title: Termékárlista
description: Ez a témakör a projektárajánlatokhoz és szerződésekhez használatos katalógusárképzésben szereplő árlistákról nyújt információkat.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999229"
---
# <a name="product-price-lists"></a>Termékárlisták

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

 A Project Operations, a **Termékárlisták** és a kapcsolódó árlistaelem-entitások támogatják a termékalapú árajánlaton és szerződéssorokon alapuló árképzési termékek funkcióit. A projektekben használt termékek esetében a projektárlisták árlistarekordjait használja a elem. 

A termékeket úgy kell beállítani, hogy azok alapértelmezett költséggel és árlistákkal rendelkezzenek a termékkatalógusban. Az alapértelmezett költség és a listaárak konfigurálásához használja a listaárat, illetve a szokásos és a jelenlegi költségeket. Az alapértelmezett listaárak csak akkor használhatók az árajánlatsoron vagy a projektszerződés-soron, ha a rendszer nem találja az adott termék árlistáját az árajánlatban vagy a projektszerződésben.

A termékkatalógus-sorok bekerülési ára árajánlatok között megváltoztatható. Ez a képesség fontos, mivel ha nem pontosan követi nyomon a költségeket, akkor nem tudja meghatározni a projekt kötelezettségvállalásaiból származó működési nyereséget. Alapértelmezés szerint a termék standard költsége lesz a bekerülési ár. Az alapértelmezett bekerülési ár azonban frissíthető az árajánlatsorban, ha az árajánlat eltérő.

## <a name="price-list-items"></a>Árlistaelemek

A termékkatalógusból felveheti termékeit a különböző árlistákra. A termékek árlistasorai mindig egy adott egységre utalnak. Az árlistán szereplő termékek árképzése devizaösszegként konfigurálható. Alternatív lehetőségként a listaár, az aktuális költség vagy a standard költség függvényében is konfigurálható.

Az árképzési funkció különféle kerekítési lehetőségeket támogat, ha a termékárakat a listaár, a standard költség vagy az aktuális költség függvényében konfigurálják. Amellett, hogy kihasználja a több árképzési módszer és a kerekítési lehetőség előnyeit, kedvezménylistákat kapcsolhat hozzá az árlisták elemeihez. 

 
## <a name="default-product-price-list"></a>Alapértelmezett termékárlista
Minden ügyfélrekordnak van egy **Alapértelmezett árlista** mezője, ahol megadhatja az ügyfél pénznemének megfelelő árlistát. Az alapértelmezett értékek nem kerülnek be automatikusan ebbe a mezőbe. Ha egyedi árképzési megállapodás létezik egy adott ügyféllel, akkor ezt a mezőt felhasználhatja az árlista az adott ügyféllel való társításához.

A Lehetőség, az Árajánlat és a Projektszerződés entitásai az alábbi sorrendet használják az alapértelmezett terméklisták megadására. Ugyanez a sorrend használatos a projekt árlistáira is.

1.  Ajánlat
2.  Lehetőség
3.  Ügyfél
4.  Globális beállítások 

Alapértelmezés szerint az árajánlatsor **Termék** mezője felsorolja az összes aktív terméket az árajánlat terméklistáján. Ha egy terméket inaktiváltak, vagy ha ez egy termékvázlat, akkor nem szerepel a listán még akkor sem, ha szerepel az árlistán. 

A termékkatalógus-sorok számlasorokként kerülnek hozzáadásra az első számlára, amelyet egy projektszerződéshez készítenek. A számlatervezeten törölhetők ezek a számlasorok. Ebben az esetben a sorok egy későbbi számlán jelennek meg, amíg számlázásra nem kerülnek, vagy amíg a számlát el nem küldik az ügyfélnek. Nem számlázható ki egy termékszámlasor részleges mennyisége. Amikor a projektszerződés terméksorozatait kiszámlázzák, tényadatok jönnek létre. Ezek a tényadatok azonban nem kapcsolódnak a kapcsolódó projektentitáshoz. Más szavakkal: a termék-alapú projektszerződés-sorok függetlenek minden projektalapú felhasználástól. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
