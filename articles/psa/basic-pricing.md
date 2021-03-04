---
title: Projektárképzés
description: Ez a témakör információkat ad arról, hogyan működik az árképzés a Dynamics 365 Project Service Automation-ben.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: 176b84671ca0b5b998c44be4f306d1f8f5200c72
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148916"
---
# <a name="project-pricing"></a>Projektárképzés 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation kibővíti az árlistaentitást a Dynamics 365 Sales szolgáltatásban. 

## <a name="key-entities"></a>Kulcsfontosságú entitások

Az árlista olyan információkat tartalmaz, amelyeket négy különféle entitás nyújt:

- **Árlista** - Ez az entitás információkat tárol a kontextusról, a pénznemről, a hatálybalépés dátumáról és az árazási időegységről. A kontextus azt mutatja, hogy az árlista a költségeket vagy az értékesítési árakat fejezi ki. 
- **Pénznem** - Ez az entitás tárolja az árak pénznemeit az árlistában. 
- **Dátum** - Ezt az entitást akkor alkalmazzák, amikor a rendszer megpróbálja megadni az alapértelmezett árat egy tranzakcióhoz. A PSA árképzés kiválasztja azt az árlistát, amelynek a hatálybalépésének dátuma tartalmazza a tranzakció dátumát. Ha a PSA-árképzés egynél több, a tranzakció dátumával hatályos árlistát talál a csatolt ajánlathoz, szerződéshez vagy szervezeti egységhez, akkor nem lesz alapértelmezett ár. 
- **Idő** - Ez az entitás tárolja a időegységet, amelyre az árak kifejeződnek, például a napi vagy óránkénti árak. 

Az Árlista entitásnak három kapcsolódó táblája van, amelyek az árakat tárolják:

  - **Szerepköralapú ár** - Ez a táblázat a szerepkörök és a szervezeti egység értékek kombinációjának árait tárolja, és arra szolgál, hogy a humán erőforrásokhoz szerepköralapú árakat állítson be.
  - **Tranzakciós kategória szerinti ár** - Ez a táblázat tranzakciós kategóriák szerint tárolja az árakat, és arra szolgál, hogy költségkategória-árakat állítson fel.
  - **Árlistatételek** - Ez a táblázat a katalógustermékek árait tartalmazza.

> ![Az árak konfigurálása árlista segítségével](media/basic-guide-12.png)
 
Az árlista egy árkártya. Az árkártya az Árlista entitás és a kapcsolódó sorok kombinációja a Szerepkör, a Tranzakciós kategória ára és az Árlistatételek tábláiban.

## <a name="resource-roles"></a>Erőforrás-szerepkörök

Az *erőforrás-szerepkör* kifejezés egy sor készséget, kompetenciát és minősítést takar, amelyekre egy személynek szüksége van ahhoz, hogy egy konkrét feladatcsoportot végrehajtson egy projektben.

A humánerőforrás-időt általában annak a szerepkörnek az alapján határozzák meg, amelyet egy erőforrás tölt be egy konkrét projektnél. A humánerőforrás-idő alatt a PSA támogatja a költségszámítást és a számlázást, amelyek erőforrás-szerepkörön alapulnak. Az idő az **Idő** egységcsoport bármely egységében árazható.

Az **Idő** egységcsoport a PSA telepítésekor jön létre. Alapértelmezett egysége az **Óra**. Nem törölheti, nevezheti át és nem szerkesztheti az **Idő** egységcsoport vagy **Óra** egység attribútumait. Az **Idő** egységcsoporthoz azonban további egységeket is felvehet. Ha megpróbálja törölni az **Idő** egységcsoportot vagy az **Óra** egységet, akkor hibákat okozhat a PSA üzleti logikában.

> ![Az árak konfigurálása szerepkörök szerint](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Tranzakciós kategóriák és költségkategóriák

A projekttanácsadóknál felmerült utazási és egyéb költségeket általában az ügyfél fizeti. A PSA az árlisták használatával támogatja a költségkategóriák árazását. A repülőjegy, szálloda és autókölcsönző példák a költségkategóriákra. Az egyes költségárlisták adott költségkategóriák árazását határozzák meg. A költségkategóriák árazásához a PSA a következő három árképzési módszert támogatja:

- **Költségalapon** - A költségeket az ügyfél fizeti, és nem alkalmaznak felárat.
- **Felár százalék** - A tényleges költségek feletti százalékos arányt számlázzák az ügyfélnek. 
- **Egységenkénti ár** - A költségkategória minden egységére külön számlázási ár van beállítva. Az ügyfélnek kiszámlázott összeget azoknak a költségegységeknek a számával számolják, amelyet a tanácsadó jelent. A futásteljesítmény az egységenkénti árképzési módszert használja. Például a futásteljesítmény-kategóriát naponta 30 dollárra (USD) vagy mérföldenként 2 USD-re lehet konfigurálni. Amikor egy tanácsadó beszámol egy projekt futásteljesítményéről, a számlázandó összeget a tanácsadó által jelentett mérföldszám alapján számítják ki.

> ![A költségkategóriánkénti árképzés konfigurálása](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Projekt értékesítési árképzés és felülbírálás

A projektárajánlatok és -szerződések esetében a projekt árlistájának eltérő árfelülbírálási mintázata van, mint egy termék árlistájának. Egy termékkatalóguson alapuló árajánlati soron felülbírálhatja az árat a szerepkörökre és kategóriákra közvetlenül az árajánlatsorban, mert minden ajánlati sor pontosan egy katalóguselemre mutat. Projektalapú árajánlati soron azonban nem lehet felülbírálni az árakat szerepkörökre és kategóriákra közvetlenül az árajánlati soron. A két különálló felülbírálási mintázat támogatása érdekében a PSA új árlistaszövetséget vezetett be, a projektárlistát.

> [!NOTE]
> Javasoljuk, hogy legyen külön árlista a projekterőforrásokhoz és a katalóguselemekhez, a kettő közötti viselkedési különbségek miatt az árak felülbírálásakor.

A következő entitások mindegyike rendelkezik egy vagy több kapcsolódó értékesítési árlistával a projekt árazásához:

- Ügyfél (fiók) 
- Lehetőség 
- Ajánlat 
- Projektszerződés

Ezeknek az entitásoknak az árlistához való társulását a projekt árlistái jelzik. Egy vagy több árlistát társíthat az Ügyfél, a Lehetőség, az Ajánlat és a Projektszerződés értékesítési entitásokhoz.

Az alapértelmezett projektárlistát nem automatikusan írják be az ügyfélrekordba. A projekt árlistáját azonban manuálisan csatolhatja az ügyfélrekordhoz. Ennek ellenére csak akkor kell manuálisan csatolnia a projekt árlistáját, ha egyedi árazási megállapodást kötött az ügyféllel. 

Ha egy projektárlistát csatolnak egy értékesítési entitáshoz, a PSA ellenőrzi a következő információkat:

- Az árlista az **Értékesítés** összefüggésében található. 
- Az árlista pénzneme megegyezik az ügyfél pénznemével. 

Projektszerződésen a PSA a következő prioritási sorrendet használja a kapcsolódó projektárlisták automatikus beállításához:

1. Ajánlat
2. Lehetőség
3. Ügyfél 
4. A PSA globális beállításai

Amikor egy projekt árlistát alapértelmezés szerint ad meg, a PSA ellenőrzi, hogy a pénznem megegyezik-e az ügyfél pénznemével, és hogy a megadott alapértelmezett árlisták az **Értékesítés** kontextusban vannak-e.

Összekapcsolhat több projektárlistát az Ügyfél, a Lehetőség, az Ajánlat és a Projekt szerződéses entitásokkal. Ez a képesség támogatja a hosszú ideje működő projektszerződés dátum-specifikus alapértelmezett árait, ahol több árlistára lehet szükség az infláció miatt bekövetkező árfrissítések elszámolására. Azonban ha az Ügyfél, a Lehetőség, az Ajánlat vagy a Projektszerződés entitással társított árlisták hatálya átfedésben van, akkor az alapértelmezett árak helytelenek lehetnek. Ezért biztosítania kell, hogy az átfedő hatályú projektárak ne legyenek társítva ezekhez az entitásokhoz.

### <a name="deal-specific-price-overrides"></a>Az ügylet-specifikus árak felülbírálása

A PSA-ban ügylet-specifikus felülbírálásokat hozhat létre a kiválasztott árakhoz a projekt árlistáiban, amelyek alapértelmezés szerint vannak megadva egy ajánlatban vagy projektszerződésben.

Alapértelmezés szerint a projektszerződés mindig megkapja a fő eladási árlista másolatát, ahelyett, hogy ehhez közvetlenül kapcsolódna. Ez a viselkedés segít garantálni, hogy az ügyféllel a munkadokumentum (SOW) alapján megkötött ármegállapodások nem változnak, ha megváltozik a mester árlista.

Árajánlatban azonban használhat mester árlistát. Alternatívaként átmásolhatja a mester árlistát, szerkesztheti azt, és létrehozhat egy egyedi árat, amely csak erre az árajánlatra vonatkozik. Az árajánlathoz tartozó új árlista létrehozásához az **Árajánlat** oldalon válassza a **Saját árképzés létrehozása** lehetőséget. Csak az ajánlatból érheti el az ügyletspecifikus projektárlistát. 

Egyéni projektárlista létrehozásakor csak az árlista projektösszetevői kerülnek másolásra. Más szavakkal: egy új árlista jön létre a meglévő projektárlista másolataként, amelyet az ajánlathoz csatolnak, és ez az új árlista csak a kapcsolódó szerepkör- és tranzakciós kategóriák árait tartalmazza.

> ![A projektszerződés egyedi árainak megtekintése és konfigurálása](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Követési költségek

A PSA nyomon követi a humán erőforrások felhasználásának költségeit a projekteknél. Ezenkívül nyomon követi a projekt során felmerült egyéb költségeket, például utazási költségeket.

A számlázási díjakhoz hasonlóan az emberi erőforrások költségei árlisták alapján is beállíthatók. Az alábbiakban bemutatjuk a fő különbségeket a beszerzési és az eladási árlista viselkedésében:

- Egy erőforrás költségét nem lehet felülbírálni egy adott projekt, szerződés vagy ajánlat esetén. A számlázott árakat azonban ügyleti alapon felül lehet bírálni, ha az ügylet jellegére jellemző változtatásokat hajtanak végre. 

- A következő sorrend alapján oldható fel a költségek árlistája:

    1. A szervezeti egységhez csatolt költségárlista.
    2. A Project Service paraméterekhez csatolt költségárlista. Mivel a Project Service paraméterekhez számos különféle pénznemben megadott költségátlisták csatolhatók, a PSA egyeztet egy pénznemet a projekt szervezeti egysége, szerződés vagy árajánlat pénzneme és a költségárlista pénzneme között.
    3. Költségeknél a bekerülési és a haszonkulcs-felárazási módszerek nem vonatkoznak a költségárlistákra. Még ha ezeket az árképzési módszereket használják is a költségárlista sorokban a tranzakciós kategóriák költségeinek beállításához, a rendszer figyelmen kívül hagyja őket, és nem kerül megadásra az alapértelmezett költségár.


[!INCLUDE[footer-include](../includes/footer-banner.md)]