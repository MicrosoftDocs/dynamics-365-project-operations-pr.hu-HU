---
title: Projektárlisták kezelése árajánlatokon
description: Ez a témakör a Projektárlista entitásról nyújt információkat.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: da349924488fb62dc0b0bd8eaf4c48b02aa16d09
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996254"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projektárlisták kezelése árajánlatokon

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations kibővíti az árlistaentitást a Dynamics 365 Sales szolgáltatásban. 

## <a name="key-entities"></a>Kulcsfontosságú entitások

Az árlista olyan információkat tartalmaz, amelyeket négy különféle entitás nyújt:

- **Árlista**: Ez az entitás információkat tárol a kontextusról, a pénznemről, a hatályba lépés dátumáról és az árazási időegységről. A kontextus azt mutatja meg, hogy az árlista a költségarányt vagy értékesítési arányt fejez-e ki. 
- **Pénznem**: Ez az entitás tárolja az árak pénznemeit az árlistában. 
- **Dátum**: Ez az entitás akkor használatos, amikor a rendszer megpróbálja megadni az alapértelmezett árat egy tranzakcióhoz. Olyan árlista van kiválasztva, amely hatályba lépési dátuma tartalmazza a tranzakció dátumát. Ha a rendszer több, a tranzakció dátumához hatályos, és a kapcsolódó ajánlathoz, szerződéshez vagy szervezeti egységhez csatolt árlistát talál, akkor nem lesz alapértelmezett ár. 
- **Idő**: Ez az entitás tárolja azt az időegységet, amelyhez az árak tartoznak (például napi vagy óránkénti árak). 

Az Árlista entitásnak három kapcsolódó táblája van, amelyek az árakat tárolják:

  - **Szerepköralapú ár**: Ez a táblázat a szerepkör és a szervezeti egység értékei kombinációjának árait tárolja, és arra szolgál, hogy a humán erőforrásokhoz szerepköralapú árakat lehessen beállítani.
  - **Tranzakciós kategória szerinti ár**: Ez a táblázat tranzakciós kategóriák szerint tárolja az árakat, és arra szolgál, hogy költségkategória-árakat lehessen beállítani.
  - **Árlistatételek**: Ez a táblázat a katalógustermékek árait tartalmazza.
 
Az árlista egy árkártya. Az árkártya az Árlista entitás és a kapcsolódó sorok kombinációja a Szerepkör, a Tranzakciós kategória ára és az Árlistatételek tábláiban.

## <a name="resource-roles"></a>Erőforrás-szerepkörök

Az *erőforrás-szerepkör* kifejezés egy sor készséget, kompetenciát és minősítést takar, amelyekre egy személynek szüksége van ahhoz, hogy egy konkrét feladatcsoportot végrehajtson egy projektben.

A humánerőforrás-időt azon szerepkör alapján határozzák meg, amelyet egy erőforrás tölt be egy konkrét projektnél. A humánerőforrás-idő alatt a költségszámítás és a számlázás az erőforrás-szerepkörön alapul. Az idő az **Idő** egységcsoport bármely egységében árazható.

Az **Idő** egységcsoport a Project Operations telepítésekor jön létre. Alapértelmezett egysége az **Óra**. Nem törölheti, nevezheti át és nem szerkesztheti az **Idő** egységcsoport vagy **Óra** egység attribútumait. Az **Idő** egységcsoporthoz azonban további egységeket is felvehet. Ha megpróbálja törölni az **Idő** egységcsoportot vagy az **Óra** egységet, az hibákat okozhat az üzleti logikában.
 
## <a name="transaction-categories-and-expense-categories"></a>Tranzakciós kategóriák és költségkategóriák

A projekttanácsadóknál felmerült utazási és egyéb költségeket az ügyfélnek számlázzák ki. A költségkategóriák árazása árlisták használatával történik. A repülőjegy, szálloda és autókölcsönző példák a költségkategóriákra. Az egyes költségárlisták adott költségkategóriák árazását határozzák meg. Az árak költségkategóriáihoz a következő három módszer használatos:

- **Költségalapon**: A költségeket az ügyfélnek számlázzák ki, és nincs árrés.
- **Felár százalék**: A tényleges költségek feletti százalékos arányt számlázzák az ügyfélnek. 
- **Egységenkénti ár**: A költségkategória minden egységére külön számlázási ár van beállítva. Az ügyfélnek kiszámlázott összeget azoknak a költségegységeknek a számával számolják, amelyet a tanácsadó jelent. A futásteljesítmény az egységenkénti árképzési módszert használja. Például a futásteljesítmény-kategóriát naponta 30 dollárra (USD) vagy mérföldenként 2 USD-re lehet konfigurálni. Amikor egy tanácsadó beszámol egy projekt futásteljesítményéről, a számlázandó összeget a tanácsadó által jelentett mérföldszám alapján számítják ki.
 
## <a name="project-sales-pricing-and-overrides"></a>Projekt értékesítési árképzés és felülbírálás

A projektárajánlatok és -szerződések esetében a projekt árlistájának eltérő árfelülbírálási mintázata van, mint egy termék árlistájának. Egy termékkatalóguson alapuló árajánlati soron felülbírálhatja az árat a szerepkörökre és kategóriákra közvetlenül az árajánlatsorban, mert minden ajánlati sor pontosan egy katalóguselemre mutat. Projektalapú árajánlati soron azonban nem lehet felülbírálni az árakat szerepkörökre és kategóriákra közvetlenül az árajánlati soron. A projekt árlistájával használható a két külön felülbírálási minta.

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

### <a name="deal-specific-price-overrides"></a>Az ügylet-specifikus árak felülbírálása

Ügyletspecifikus felülbírálásokat hozhat létre a kiválasztott árakhoz a projekt árlistáiban, amelyek alapértelmezés szerint vannak megadva egy ajánlatban vagy projektszerződésben.

Alapértelmezés szerint a projektszerződés mindig megkapja a fő eladási árlista másolatát, ahelyett, hogy ehhez közvetlenül kapcsolódna. Ez a viselkedés segít garantálni, hogy az ügyféllel a munkadokumentum (SOW) alapján megkötött ármegállapodások nem változnak, ha megváltozik a mester árlista.

Árajánlatban azonban használhat mester árlistát. Alternatívaként átmásolhatja a mester árlistát, szerkesztheti azt, és létrehozhat egy egyedi árat, amely csak erre az árajánlatra vonatkozik. Az árajánlathoz tartozó új árlista létrehozásához az **Árajánlat** oldalon válassza a **Saját árképzés létrehozása** lehetőséget. Csak az ajánlatból érheti el az ügyletspecifikus projektárlistát. 

Egyéni projektárlista létrehozásakor csak az árlista projektösszetevői kerülnek másolásra. Más szavakkal: egy új árlista jön létre a meglévő projektárlista másolataként, amelyet az ajánlathoz csatolnak, és ez az új árlista csak a kapcsolódó szerepkör- és tranzakciós kategóriák árait tartalmazza.
  
## <a name="tracking-costs"></a>Követési költségek

A Project Operations nyomon követi a humán erőforrások felhasználásának költségeit a projekteknél. Ezenkívül nyomon követi a projekt során felmerült egyéb költségeket, például az utazási költségeket.

A számlázási díjakhoz hasonlóan az emberi erőforrások költségei árlisták alapján is beállíthatók. Az alábbiakban bemutatjuk a fő különbségeket a beszerzési és az eladási árlista viselkedésében:

- Egy erőforrás költségét nem lehet felülbírálni egy adott projekt, szerződés vagy ajánlat esetén. A számlázott árakat azonban ügyleti alapon felül lehet bírálni, ha az ügylet jellegére jellemző változtatásokat hajtanak végre. 

- A következő sorrend alapján oldható fel a költségek árlistája:

    1. A szervezeti egységhez csatolt költségárlista.
    2. A Project Operations paramétereihez csatolt önköltségi-árlista. Mivel a paraméterekhez számos különféle pénznemben megadott önköltségi-árlista csatolható, a rendszer egyezteti a pénznemet a projekt szerződő szervezeti egysége, a szerződés vagy az árajánlat pénzneme és az önköltségi-árlista pénzneme között.
    3. Költségeknél a bekerülési és a haszonkulcs-felárazási módszerek nem vonatkoznak a költségárlistákra. Még ha ezeket az árképzési módszereket használják is a költségárlista sorokban a tranzakciós kategóriák költségeinek beállításához, a rendszer figyelmen kívül hagyja őket, és nem kerül megadásra az alapértelmezett költségár.


[!INCLUDE[footer-include](../includes/footer-banner.md)]