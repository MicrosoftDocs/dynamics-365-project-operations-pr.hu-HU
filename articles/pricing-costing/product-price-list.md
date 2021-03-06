---
title: Termékárlista
description: Ez a témakör a projektárajánlatokhoz és szerződésekhez használatos katalógusárképzésben szereplő árlistákról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898174"
---
# <a name="product-price-lists"></a>Termékárlista

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az árlisták és az árlistán szereplő elemek támogatják a termékkatalógus árképzését. Ezt a funkciót leginkább katalógusalapú sorokhoz használják projektárjánlatokon és projektszerződéseken.

Projektalapú sorok esetében egy szerződés jelenti az üzletkötést annak megszerzése után. Mivel a tárgyalási folyamat általában megelőzi a megszerzést, az árajánlathoz csatolt árat mindig egy új árlistába másolják és csatolják a szerződéshez. Ez az új árlista nem változtatható meg a szerződés hatályán kívül. Ez a korlátozás segít megvédeni a megbeszélt listaárat a fő árlistán bekövetkező bármilyen árváltozástól.

A termékeket úgy kell beállítani, hogy azok alapértelmezett költséggel és árlistákkal rendelkezzenek a termékkatalógusban. Az alapértelmezett költség és a listaárak konfigurálásához használja a listaárat, illetve a szokásos és a jelenlegi költségeket. Az alapértelmezett listaárak csak akkor használhatók az árajánlatsoron vagy a projektszerződés-soron, ha a rendszer nem találja az adott termék árlistáját az árajánlatban vagy a projektszerződésben.

A termékkatalógus-sorok bekerülési ára árajánlatok között megváltoztatható. Ez a képesség fontos, mivel ha nem pontosan követi nyomon a költségeket, akkor nem tudja meghatározni a projekt kötelezettségvállalásaiból származó működési nyereséget. Alapértelmezés szerint a termék standard költsége lesz a bekerülési ár. Az alapértelmezett bekerülési ár azonban frissíthető az árajánlatsorban, ha az árajánlat eltérő.

## <a name="price-list-items"></a>Árlistaelemek

A termékkatalógusból felveheti termékeit a különböző árlistákra. A termékek árlistasorai mindig egy adott egységre utalnak. Az árlistán szereplő termékek árképzése devizaösszegként konfigurálható. Alternatív lehetőségként a listaár, az aktuális költség vagy a standard költség függvényében is konfigurálható.

A PSA különféle kerekítési lehetőségeket támogat, ha az árakat a listaár, a standard költség vagy az aktuális költség függvényében konfigurálják. Amellett, hogy kihasználja a több árképzési módszer és a kerekítési lehetőség előnyeit, kedvezménylistákat kapcsolhat hozzá az árlisták elemeihez. 

Amikor új egyéni árlistát hoz létre egy árajánlathoz a **Projektárajánlat** lap **Saját árképzés létrehozása** részén, a rendszer másolatot készít az árlistáról, és az új árlista fejlécén található **Entitás** mező beállítása **Értékesítési entitás** lesz. Az új árlista neve az árajánlat nevéhez és az időbélyegzőhöz lesz csatolva. Az egyéni munkafolyamatokban is használhatja az új árlista nevét és az árajánlatot az egyedi árképzést alkalmazó árajánlatok további felülvizsgálatának és jóváhagyásának indításához.

 
## <a name="default-product-price-list"></a>Alapértelmezett termékárlista
Minden ügyfélrekordnak van egy **Alapértelmezett árlista** mezője, ahol megadhatja az ügyfél pénznemének megfelelő árlistát. Az alapértelmezett értékek nem kerülnek be automatikusan ebbe a mezőbe. Ha egyedi árképzési megállapodás létezik egy adott ügyféllel, akkor ezt a mezőt felhasználhatja az árlista az adott ügyféllel való társításához.

A Lehetőség, az Árajánlat és a Projektszerződés entitásai az alábbi sorrendet használják az alapértelmezett terméklisták megadására. Ugyanez a sorrend használatos a projekt árlistáira is.

1.  Ajánlat
2.  Lehetőség
3.  Ügyfél
4.  Globális beállítások 

Alapértelmezés szerint az árajánlatsor **Termék** mezője felsorolja az összes aktív terméket az árajánlat terméklistáján. Ha egy terméket inaktiváltak, vagy ha ez egy termékvázlat, akkor nem szerepel a listán még akkor sem, ha szerepel az árlistán. 

A termékkatalógus-sorok számlasorokként kerülnek hozzáadásra az első számlára, amelyet egy projektszerződéshez készítenek. A számlatervezeten törölhetők ezek a számlasorok. Ebben az esetben a sorok egy későbbi számlán jelennek meg, amíg számlázásra nem kerülnek, vagy amíg a számlát el nem küldik az ügyfélnek. Nem számlázható ki egy termékszámlasor részleges mennyisége. Amikor a projektszerződés terméksorozatait kiszámlázzák, tényadatok jönnek létre. Ezek a tényadatok azonban nem kapcsolódnak a kapcsolódó projektentitáshoz. Más szavakkal: a termék-alapú projektszerződés-sorok függetlenek minden projektalapú felhasználástól. A rendszer nem követi nyomon a projektek anyagfelhasználását.
