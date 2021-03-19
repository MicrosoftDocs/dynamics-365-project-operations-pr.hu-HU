---
title: Költségkezelési paraméterek
description: A következő paraméterek szabályozzák a költség-menedzsment általános működését.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 498d597fe811192ce313a1b0384de81e7ef55c58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271915"
---
# <a name="expense-management-parameters"></a>Költségkezelési paraméterek


Ez a paraméter szabályozza a költség-menedzsment általános működését.

### <a name="general"></a>Általános

| **Mező**                                                | **Adatfolyam leírása**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standard útiköltségtérítés**                             | Adja meg a útiköltség-kiadások megtérítési arányát. Ezt az arányt szorozza meg a rendszer a költséghez megadott útiköltséggel, hogy kiszámítsa az utazási költségre visszatérített összeget.                       |
|**Személyes kiadások kifizetője**                             | Válassza ki, hogy ki felel a személyesként kategorizált hitelkártya-tranzakciók összegének megfizetéséért.                                                                                                     |
|**Teljes költségjelentés megjelenítése visszakövetés esetén**               | Jelölje be ezt a jelölőnégyzetet, ha egy költségjelentés összes költségét meg szeretné jeleníteni, amikor az eredeti dokumentum adatait egy adott bizonylatra vonatkozóan tekinti meg, amely a költségjelentés könyvelésekor jött létre.              |
|**Az utazás előzetes engedélyezése kötelező**                 | Jelölje be ezt a jelölőnégyzetet, ha azt szeretné, hogy utazási igénylést kelljen benyújtani és jóváhagyni ahhoz, hogy egy alkalmazott költségjelentést küldhessen be.                                                                    |
|**Elosztások szerkesztésének engedélyezése a feladás előtt**            | Adja meg, hogy a költségjelentés felosztásai a feladás előtt szerkeszthetők-e.                                                                                                                 |
|**Költséggazdálkodási alapszabályok kiértékelése**                     | Adja meg, hogy a költségek értékelése esetén megsértésre került-e egy költségszabály. A kiadások ellenőrizhetők a kiadási bejegyzés bevitelekor és mentésekor, illetve a kiadás jóváhagyás céljából történő elküldésekor. A program a kiadási sor mentésekor ellenőrzi a bizonylatok szükséges irányelvszabályait.                   |
|**Vállalatközi kiadási sorok engedélyezése**                         | Válassza ki, hogy engedélyezett-e más jogi entitások kiadásainak megadása egy költségjelentésben.                                                                                                          |
|**A hitelkártya-kiadásokra vonatkozó átváltási árfolyam módosításának engedélyezése** | Jelölje be ezt a beállítást, ha engedélyezni szeretné, hogy a felhasználó módosíthassa az importált hitelkártya-kiadások átváltási árfolyamát.                                                                        |
|**Megjelenítendő többszintű hierarchiamezők**                  | Adja meg, hogy mely jóváhagyói mezők jelenjenek meg, ha a költségjelentés munkafolyamat-hozzárendelés típusa hierarchia, és a hierarchia kiválasztása a jóváhagyási hierarchia, költség többszintű jóváhagyása értékre van beállítva. A többszintű jóváhagyási hierarchia munkafolyamathoz való használatakor a kijelölt mezők megjelennek a Költségjelentésben, és módosíthatók. |
|**Az alkalmazotti hitelkártya számának megadása (2017. júliusi frissítés)**     | Adja meg, hogy egy 15 karakterből vagy 16 karakterből álló szám adható-e meg, és menthető-e el az alkalmazotthoz tartozó **Hitelkártyák** oldal **Kártyaazonosító** mezőjében.                                                                          |

### <a name="financial"></a>Pénzügyi szolgáltató

| **Mező**                                                            | **Leírás**     |
|----------------------------------------------------------------------|------------------------------------|
|**Főkönyvi napi napló neve**                                         | Válassza ki annak a főkönyvi naplónak a nevét, amelyhez a jóváhagyott költségjelentéseket könyveli a rendszer.            |
|**Költségadó-visszaigénylés engedélyezése**                                  | Válassza ezt a lehetőséget, ha engedélyezni szeretné a költségadó-visszaigénylést az arra jogosult kiadások esetében. Ez a beállítás nem engedélyezhető, ha az USA áfa- és importadó-szabályok engedélyezve vannak.      |
|**Készpénzes előlegek azonnali feladása**                                     | Válassza ezt a lehetőséget, ha a fizetési és átadási folyamat befejezése után feladásra kerüljön egy jóváhagyott készpénzelőleg. Ha ez a beállítás nincs bejelölve, akkor a fizetési és átadási folyamat egy könyveletlen főkönyvi naplót hoz majd létre. |
|**Helyes könyvelési dátum feladás közben**                             | Jelölje be ezt a beállítást, ha frissíteni szeretné a könyvelési dátumot a kiadások könyvelésekor, ha az aktuális időszak függőben vagy lezárva van. A rendszer a következő nyitott időszakra állítja a könyvelési dátumot.   |
|**Tranzakciók csoportosításának engedélyezése a fizetési módban megadott ellenszámla alapján**      | Jelölje be ezt a jelölőnégyzetet, ha szeretné összesíteni a költségjelentés költségtranzakcióit a kiadások fizetési módjában megadott ellenszámla alapján.   
|**Adóval együtt**                                                   | Válassza ezt a beállítást, ha a kiadás összegében alapértelmezés szerint szerepeltetni szeretné az áfát.             |
|**Kötelezettségvállalások felszabadítása utazásigénylések lezárásakor**            | Válassza ezt a lehetőséget, ha a jóváhagyott utazási igénylés lezárásakor fel szeretné szabadítani a terhelt forrásokat.                                                                                   |
|**Utazásigénylés benyújtásának engedélyezése a költségvetés túllépésekor a költségvetésjegyzék és a projektköltségvetés számára** | Válassza ezt a lehetőséget, ha lehetővé teszi, hogy az alkalmazottak utazási igényléseket nyújtsanak be jóváhagyásra, ha túllépik a költségvetés-jegyzékben beállított engedélyezett költségvetést vagy a projekt engedélyezett költségvetését.            |
|**Költségjelentés benyújtásának engedélyezése a költségvetés túllépésekor a költségvetésjegyzék és a projektköltségvetés számára**    | Válassza ezt a lehetőséget, ha lehetővé teszi, hogy az alkalmazottak költségjelentéseket nyújtsanak be jóváhagyásra, ha túllépik a költségvetés-jegyzékben beállított engedélyezett költségvetést vagy a projekt engedélyezett költségvetését.                |
|**Költségjelentés jóváhagyásának engedélyezése a költségvetés túllépésekor kizárólag a költségvetésjegyzék számára**                | Válassza ezt a lehetőséget, ha engedélyezni szeretné, hogy a jóváhagyók jóváhagyják a költségvetési tételjegyzékben beállított, engedélyezett költségvetést meghaladó költségjelentéseket.                                                                       |

### <a name="per-diem"></a>Napidíj

| **Mező**                             | **Adatfolyam leírása**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Napidíj minimális órakövetelménye**           | Adja meg az alapértelmezett minimális óraszámot, ameddig egy alkalmazottnak napi szinten kell dolgoznia ahhoz, hogy az utazáshoz kapcsolódó kiadások esetében napidíjat kapjon.  Ez az érték alapértelmezett értékként csak a napidíjszintek Minimális óraszám mezőjében használható.                                                                                      |
|**Étkezés százaléka**                          | Adja meg a napidíj alapértelmezett étkezésekre vonatkozó százalékát az utazáshoz kapcsolódó költség első és utolsó napjain, amikor az **Étkezési levonás számításának alapja:** mező **Étkezéstípus nap szerint** vagy **Étkezések száma naponta** értékre van beállítva. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg ezeken a napokon eltérhet az általános összegtől. Ha a százalékérték 0 (nulla), akkor az első és az utolsó napok levonása 0,00 lesz. |
|**Szálloda százaléka**                        | Adja meg a napidíj alapértelmezett százalékát az utazáshoz kapcsolódó kiadások első és utolsó napjaiban használt szállodáknál. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg ezeken a napokon eltérhet az általános összegtől. Ha a százalékérték 0 (nulla), akkor az első és az utolsó napok levonása 0,00 lesz.                                              |
|**Egyéb százalék**                        | Adja meg a napidíj alapértelmezett százalékát az egyéb kiadások esetében az utazáshoz kapcsolódó kiadások első és utolsó napjaiban. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg ezeken a napokon eltérhet az általános összegtől. Ha a százalékérték 0 (nulla), akkor az első és az utolsó napok levonása 0,00 lesz.                                                                                                     |
|**A reggeli miatti levonás százalékban** | Adja meg azt az összeget, amellyel a napidíj a reggeli miatt csökken. Ha például egy alkalmazott ingyenes reggelit kap, előfordulhat, hogy 10 százalékkal csökkenteni szeretné a napidíj összegét.                               |
|**Az ebéd miatti levonás százalékban**    | Adja meg azt az összeget, amellyel a napidíj az ebéd miatt csökken. Ha például egy alkalmazott ingyenes ebédet kap, előfordulhat, hogy 15 százalékkal csökkenteni szeretné a napidíj összegét.                                       |
|**A vacsora miatti levonás százalékban**   | Adja meg azt az összeget, amellyel a napidíj a vacsora miatt csökken. Ha például egy alkalmazott ingyenes vacsorát kap, előfordulhat, hogy 25 százalékkal csökkenteni szeretné a napidíj összegét.                                     |
|**Étkezési levonás számításának alapja:**         | Válassza ki, hogy a rendszer hogyan számítsa ki a napidíj étkezés miatti levonását, kiválasztva, hogy a csökkentés az utazásonkénti vagy napi étkezéstípuson vagy az étkezések naponta engedélyezett számán alapul-e.|
|**Napidíj kerekítése**                  | Válassza ki, hogy milyen típusú kerekítést használ a rendszer a napidíjhoz kapcsolódó kiadásokhoz. Ha a normál kerekítés lehetőséget választja, akkor a 0,50 összegű napidíjat legfeljebb 1,00-ig kerekíti a rendszer, és minden olyan napidíjat, amelynek összege kisebb, mint 0,50, lefelé kerekíti a 0,00 értékre.                                                                                              |
|**Napi kalkuláció alapja**         | Adja meg, hogy a napidíj összege naptári napon vagy 24 órás időszakon alapuljon-e.       |

### <a name="fax-cover-pages"></a>Faxfedőlapok

| **Mező**                      | **Adatfolyam leírása**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Útmutatások**                   | Adja meg, hogy az alkalmazottak milyen utasításokat kövessenek, amikor létrehoznak egy fedőlapot egy olyan faxhoz, amely a költségjelentéshez kapcsolódó bizonylatok küldéséhez szükséges. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, kattintson a **Fordítások** gombra. |
|**Felhasználóazonosító (vonalkód-információ)** | Válassza ezt a beállítást, ha az alkalmazott egyedi azonosítóját a fax fedőlapján lévő vonalkódban szeretné tárolni.                 |
|**Vonalkód**                      | Válassza ki a fax fedőlapján használt vonalkódot. A 39-es és a 128-as vonalkódot támogatja a Költségkezelés.               |

### <a name="anti-corruption"></a>Korrupcióellenes

|                 <strong>Mező</strong>                 |                                                                                                                                                                                            <strong>Leírás</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Korrupcióellenes nyilatkozat megjelenítése</strong>  | Válassza ezt a lehetőséget, ha új költségjelentés létrehozásakor meg szeretné jeleníteni a korrupcióellenes szöveget. Ezután engedélyezhetők bizonyos költségkategóriák, amelyek megkövetelik a korrupcióellenes nyilatkozat kiválasztását a költségjelentés alatt. Például egy adott kormányzati tisztviselőkkel kapcsolatos kiadáshoz kapcsolódó ajándékkategória esetében előfordulhat, hogy az alkalmazottnak igazolnia kell, hogy a költség megfelel a kormányzati tisztviselőkhöz kapcsolódó vállalati irányelveknek. |
| <strong>Korrupcióellenes üzenet a beküldő számára</strong> |                                                                                             Írja be az új költségjelentés létrehozásakor az alkalmazottnak megjelenő szöveget. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, kattintson a <strong>Fordítások</strong> gombra.                                                                                             |
| <strong>Korrupcióellenes üzenet a jóváhagyó számára</strong>  |                                                                                             Írja be az új költségjelentés létrehozásakor a jóváhagyónak megjelenő szöveget. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, kattintson a <strong>Fordítások</strong> gombra.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]