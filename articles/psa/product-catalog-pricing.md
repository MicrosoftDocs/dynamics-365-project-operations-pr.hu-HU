---
title: Termékkatalógus árképzése
description: Ez a cikk a termékkatalógus díjszabásának (PSA) működéséről Dynamics 365 Project Service Automation nyújt tájékoztatást.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 61d35a9ce16bb58abc66edab5e21dd83d607184e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913393"
---
# <a name="product-catalog-pricing"></a>Termékkatalógus árképzése 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Az árlisták és az árlistán szereplő elemek támogatják a termékkatalógus árképzését. Ezt a funkciót leginkább katalógusalapú sorokhoz használják projektárjánlatokon és projektszerződéseken.

Projektalapú sorok esetében egy szerződés jelenti az üzletkötést annak megszerzése után. Mivel a tárgyalási folyamat általában megelőzi a megszerzést, az árajánlathoz csatolt árat mindig egy új árlistába másolják és csatolják a szerződéshez. Ez az új árlista nem változtatható meg a szerződés hatályán kívül. Ez a korlátozás segít megvédeni a megbeszélt listaárat a fő árlistán bekövetkező bármilyen árváltozástól.

A termékeket úgy kell beállítani, hogy azok alapértelmezett költséggel és árlistákkal rendelkezzenek a termékkatalógusban. Az alapértelmezett költség és a listaárak konfigurálásához a listaárat, a szokásos és a jelenlegi költségeket kell használni. Az alapértelmezett listaárak csak akkor használhatók az árajánlatsoron vagy a projektszerződés-soron, ha a rendszer nem találja az adott termék árlistáját az árajánlatban vagy a projektszerződésben.

A termékkatalógus-sorok bekerülési ára árajánlatok között megváltoztatható. Ez a képesség fontos, mivel ha nem pontosan követi nyomon a költségeket, akkor nem tudja meghatározni a projekt kötelezettségvállalásaiból származó működési nyereséget. Alapértelmezés szerint a termék standard költsége lesz a bekerülési ár. Az alapértelmezett bekerülési ár azonban frissíthető az árajánlatsorban, ha az árajánlat eltérő.

## <a name="price-list-items"></a>Árlistaelemek

A termékkatalógusból felveheti termékeit a különböző árlistákra. A termékek árlistasorai mindig egy adott egységre utalnak. Az árlistán szereplő termékek árképzése devizaösszegként konfigurálható. Alternatív lehetőségként a listaár, az aktuális költség vagy a standard költség függvényében is konfigurálható.

A PSA különféle kerekítési lehetőségeket támogat, ha az árakat a listaár, a standard költség vagy az aktuális költség függvényében konfigurálják. Amellett, hogy kihasználja a több árképzési módszer és a kerekítési lehetőség előnyeit, kedvezménylistákat kapcsolhat hozzá az árlisták elemeihez. 

> ![Termékek hozzáadása egy katalógusból különböző árlistákhoz.](media/basic-guide-16.png)

Amikor új egyéni árlistát hoz létre egy árajánlathoz a **Projektárajánlat** lap **Saját árképzés létrehozása** részén, a PSA másolatot készít az árlistáról, és az új árlista fejlécén található **Entitás** mező beállítása **Értékesítési entitás** lesz. Az új árlista neve az árajánlat nevéhez és az időbélyegzőhöz lesz csatolva. Az egyéni munkafolyamatokban is használhatja az új árlista nevét és az árajánlatot az egyedi árképzést alkalmazó árajánlatok további felülvizsgálatának és jóváhagyásának indításához.

 
## <a name="default-product-price-list"></a>Alapértelmezett termékárlista
Minden ügyfélrekordnak van egy **Alapértelmezett árlista** mezője, ahol megadhatja az ügyfél pénznemének megfelelő árlistát. A PSA esetén az alapértelmezett érték nem automatikusan kerül be ebbe a mezőbe. Ha egyedi árképzési megállapodás létezik egy adott ügyféllel, akkor ezt a mezőt felhasználhatja az árlista az adott ügyféllel való társításához.

A Lehetőség, az Árajánlat és a Projektszerződés entitásai az alábbi sorrendet használják az alapértelmezett terméklisták megadására. Ugyanez a sorrend használatos a projekt árlistáira is.

1.  Ajánlat
2.  Lehetőség
3.  Ügyfél
4.  A PSA globális beállításai

Alapértelmezés szerint az árajánlatsor **Termék** mezője felsorolja az összes aktív terméket az árajánlat terméklistáján. Ha egy terméket inaktiváltak, vagy ha ez egy termékvázlat, akkor nem szerepel a listán még akkor sem, ha szerepel az árlistán. 

A termékkatalógus-sorok számlasorokként kerülnek hozzáadásra az első számlára, amelyet egy projektszerződéshez készítenek. A számlatervezeten törölhetők ezek a számlasorok. Ebben az esetben a sorok egy későbbi számlán jelennek meg, amíg számlázásra nem kerülnek, vagy amíg a számlát el nem küldik az ügyfélnek. A PSA-ban nem számlázható ki egy termékszámlasor részleges mennyisége. Amikor a projektszerződés terméksorozatait kiszámlázzák, tényadatok jönnek létre. Ezek a tényadatok azonban nem kapcsolódnak a kapcsolódó projektentitáshoz. Más szavakkal: a termék-alapú projektszerződés-sorok függetlenek minden projektalapú felhasználástól. A PSA nem követi nyomon a projektek anyagfelhasználását.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
