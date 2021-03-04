---
title: Költségkezelési paraméterek konfigurálása
description: Ez a témakör ismerteti azokat a paramétereket, amelyek a Költségkezelés általános működését szabályozzák.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 09da0f4e0c6aec97c93c10eb686513e782189f77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121041"
---
# <a name="configure-expense-management-parameters"></a>Költségkezelési paraméterek konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör ismerteti azokat a paramétereket, amelyek a Költségkezelés általános működését szabályozzák.

## <a name="general"></a>Általános

| Mező                                                    | Adatfolyam leírása |
|----------------------------------------------------------|-------------|
| Standard útiköltségtérítés                                 | Adja meg a útiköltség-kiadások megtérítési arányát. Ezt az arányt szorozza meg a rendszer a költséghez megadott útiköltséggel, hogy kiszámítsa az utazási költségre visszatérített összeget. |
| Költség céljának ellenőrzése                                 | Kapcsolja be ezt a beállítást, ha a felhasználóit a **Kiadás céljának jelentése** mezőben megadott meglévő értékek használatára szeretné korlátozni, amikor létrehozzák a költségjelentéseket. |
| Személyes kiadások kifizetője                                | Válassza ki, hogy ki felel a személyesként kategorizált hitelkártya-tranzakciók összegének megfizetéséért. |
| Teljes költségjelentés megjelenítése visszakövetés esetén               | Jelölje be ezt a jelölőnégyzetet, ha egy költségjelentés összes költségét meg szeretné jeleníteni, amikor az eredeti dokumentum adatait egy adott bizonylatra vonatkozóan tekinti meg, amely a költségjelentés könyvelésekor jött létre. |
| Az utazás előzetes engedélyezése kötelező                 | Jelölje be ezt a jelölőnégyzetet, ha azt szeretné, hogy utazási igénylést kelljen benyújtani és jóváhagyni ahhoz, hogy egy alkalmazott költségjelentést küldhessen be. |
| Elosztások szerkesztésének engedélyezése a feladás előtt            | Adja meg, hogy a költségjelentés felosztásai a feladás előtt szerkeszthetők-e. |
| Költséggazdálkodási alapszabályok kiértékelése                     | Adja meg, hogy a költségek értékelése esetén megsértésre került-e egy költségszabály. A kiadások kiértékelhetők a kiadási bejegyzés bevitelekor és mentésekor, illetve a kiadás jóváhagyás céljából történő elküldésekor. A program a kiadási sor mentésekor kiértékeli a bizonylatok szükséges irányelvszabályait. |
| Vállalatközi kiadási sorok engedélyezése                         | Válassza ki, hogy megadhatók-e más jogi entitások kiadásai egy költségjelentésben. |
| A hitelkártya-kiadásokra vonatkozó átváltási árfolyam módosításának engedélyezése | Jelölje be ezt a beállítást, ha engedélyezni szeretné, hogy a felhasználó módosíthassa az importált hitelkártya-kiadások átváltási árfolyamát. |
| Megjelenítendő többszintű hierarchiamezők                  | Adja meg, hogy mely jóváhagyói mezők jelenjenek meg, ha a munkafolyamat-hozzárendelés típusa hierarchia, és a **Hierarchia** kiválasztása a jóváhagyási hierarchia, költség többszintű jóváhagyása értékre van beállítva. A többszintű jóváhagyási hierarchia munkafolyamathoz való használatakor a kijelölt mezők megjelennek a költségjelentésben, és módosíthatók. |
| Az alkalmazotti hitelkártya számának megadása                        | Adja meg, hogy egy 15 karakterből vagy 16 karakterből álló szám adható-e meg, és menthető-e el az alkalmazotthoz tartozó **Hitelkártyák** oldal **Kártyaazonosító** mezőjében. |
| Utazási igénylés céljának érvényesítése                      | Kapcsolja be ezt a beállítást, ha a felhasználóit a **Kiadás céljának jelentése** mezőben megadott meglévő értékek használatára szeretné korlátozni, amikor létrehozzák az utazási igénylést. |

## <a name="financial"></a>Pénzügyi szolgáltató

| Mező                                                                                    | Adatfolyam leírása |
|------------------------------------------------------------------------------------------|-------------|
| Főkönyvi napi napló neve                                                                | Válassza ki annak a főkönyvi naplónak a nevét, amelyhez a jóváhagyott költségjelentéseket könyveli a rendszer. |
| Költségadó-visszaigénylés engedélyezése                                                        | Válassza ezt a lehetőséget, ha engedélyezni szeretné a költségadó-visszaigénylést az arra jogosult kiadások esetében. Ez a beállítás nem választható ki, ha az USA áfa- és importadó-szabályok engedélyezve vannak. |
| Készpénzes előlegek azonnali feladása                                                           | Válassza ezt a lehetőséget, ha a fizetési és átadási folyamat befejezése után feladásra kerüljön egy jóváhagyott készpénzelőleg. Ha ez a beállítás nincs bejelölve, akkor a fizetési és átadási folyamat egy könyveletlen főkönyvi naplót hoz létre. |
| Helyes könyvelési dátum feladás közben                                                   | Jelölje be ezt a beállítást, ha frissíteni szeretné a könyvelési dátumot a kiadások könyvelésekor, ha az aktuális időszak függőben vagy lezárva van. A rendszer a következő nyitott időszakra állítja a könyvelési dátumot. |
| Tranzakciók csoportosításának engedélyezése a fizetési módban megadott ellenszámla alapján       | Jelölje be ezt a jelölőnégyzetet, ha szeretné összesíteni a költségjelentés költségtranzakcióit a kiadások fizetési módjában megadott ellenszámla alapján. |
| Adóval együtt                                                                             | Válassza ezt a beállítást, ha a kiadás összegében alapértelmezés szerint szerepeltetni szeretné az áfát. |
| Kötelezettségvállalások felszabadítása utazásigénylések lezárásakor                                      | Válassza ezt a lehetőséget, ha a jóváhagyott utazási igénylés lezárásakor fel szeretné szabadítani a terhelt forrásokat. |
| Utazásigénylés benyújtásának engedélyezése a költségvetés túllépésekor a költségvetésjegyzék és a projektköltségvetés számára | Válassza ezt a lehetőséget, ha lehetővé teszi, hogy az alkalmazottak utazási igényléseket nyújtsanak be jóváhagyásra, még akkor is, ha túllépik a költségvetés-jegyzékben beállított engedélyezett költségvetést vagy a projekt engedélyezett költségvetését. |
| Költségjelentés benyújtásának engedélyezése a költségvetés túllépésekor a költségvetésjegyzék és a projektköltségvetés számára     | Válassza ezt a lehetőséget, ha lehetővé teszi, hogy az alkalmazottak költségjelentéseket nyújtsanak be jóváhagyásra, még akkor is, ha túllépik a költségvetés-jegyzékben beállított engedélyezett költségvetést vagy a projekt engedélyezett költségvetését. |
| Költségjelentés jóváhagyásának engedélyezése a költségvetés túllépésekor kizárólag a költségvetésjegyzék számára                 | Válassza ezt a lehetőséget, ha engedélyezni szeretné, hogy a jóváhagyók jóváhagyják a költségvetési tételjegyzékben beállított, engedélyezett költségvetést meghaladó költségjelentéseket. |

## <a name="per-diem"></a>Napidíj

| Mező                                 | Adatfolyam leírása |
|---------------------------------------|-------------|
| Napidíj minimális órakövetelménye            | Adja meg az alapértelmezett minimális óraszámot, ameddig egy alkalmazottnak napi szinten kell dolgoznia ahhoz, hogy az utazáshoz kapcsolódó kiadások esetében napidíjat kapjon. Ez az érték alapértelmezett értékként csak a napidíjszintek **Minimális óraszám** mezőjében használható. |
| Étkezés százaléka                          | Adja meg a napidíj alapértelmezett étkezésekre vonatkozó százalékát az utazáshoz kapcsolódó költség első és utolsó napjain, amikor az **Étkezési levonás számításának alapja:** mező **Étkezéstípus nap szerint** vagy **Étkezések száma naponta** értékre van beállítva. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg az adott napon eltérhet az általános összegtől. Ha a százalékos érték **0** (nulla), az első és az utolsó napok levonása 0,00 lesz. |
| Szálloda százaléka                         | Adja meg a napidíj alapértelmezett százalékát az utazáshoz kapcsolódó kiadások első és utolsó napjaiban használt szállodáknál. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg az adott napon eltérhet az általános összegtől. Ha a százalékos érték **0** (nulla), az első és az utolsó napok levonása 0,00 lesz. |
| Egyéb százalék                         | Adja meg a napidíj alapértelmezett százalékát az egyéb kiadások esetében az utazáshoz kapcsolódó kiadások első és utolsó napjaiban. Az első és utolsó napokon a munkanap rövidebb lehet, mint a szokásos munkanap. Ezért a napidíjban szereplő összeg az adott napon eltérhet az általános összegtől. Ha a százalékos érték **0** (nulla), az első és az utolsó napok levonása 0,00 lesz. |
| A reggeli miatti levonás százalékban | Adja meg azt az összeget, amellyel a napidíj a reggeli miatt csökken. Ha például egy alkalmazott ingyenes reggelit kap, előfordulhat, hogy 10 százalékkal csökkenteni szeretné a napidíj összegét. |
| Az ebéd miatti levonás százalékban     | Adja meg azt az összeget, amellyel a napidíj az ebéd miatt csökken. Ha például egy alkalmazott ingyenes ebédet kap, előfordulhat, hogy 15 százalékkal csökkenteni szeretné a napidíj összegét. |
| A vacsora miatti levonás százalékban    | Adja meg azt az összeget, amellyel a napidíj a vacsora miatt csökken. Ha például egy alkalmazott ingyenes vacsorát kap, előfordulhat, hogy 25 százalékkal csökkenteni szeretné a napidíj összegét. |
| Étkezési levonás számításának alapja:           | Adja meg, hogy a rendszer hogyan számítsa ki a napidíj étkezés miatti levonását, kiválasztva, hogy a csökkentés az utazásonkénti vagy napi étkezéstípuson vagy az étkezések naponta engedélyezett számán alapul-e. |
| Napidíj kerekítése                     | Válassza ki, hogy milyen típusú kerekítést használ a rendszer a napidíjhoz kapcsolódó kiadásokhoz. Ha a normál kerekítés lehetőséget választja, akkor a 0,50 összegű napidíjat legfeljebb 1,00-ig kerekíti a rendszer, és minden olyan napidíjat, amelynek összege kisebb, mint 0,50, lefelé kerekíti a 0,00 értékre. |
| Napi kalkuláció alapja          | Adja meg, hogy a napidíj összege naptári napon vagy 24 órás időszakon alapuljon-e. |

## <a name="fax-cover-pages"></a>Faxfedőlapok

| Mező                          | Adatfolyam leírása |
|--------------------------------|-------------|
| Útmutatások                   | Adja meg, hogy az alkalmazottak milyen utasításokat kövessenek, amikor létrehoznak egy fedőlapot egy olyan faxhoz, amely a költségjelentéshez kapcsolódó bizonylatok küldéséhez szükséges. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, válassza a **Fordítások** lehetőséget. |
| Felhasználóazonosító (vonalkód-információ) | Válassza ezt a beállítást, ha az alkalmazott egyedi azonosítóját a fax fedőlapján lévő vonalkódban szeretné tárolni. |
| Vonalkód                       | Válassza ki a fax fedőlapján használt vonalkódot. A 39-es és a 128-as vonalkódot támogatja a Költségkezelés. |

## <a name="anti-corruption"></a>Korrupcióellenes

| Mező                                 | Adatfolyam leírása |
|---------------------------------------|-------------|
| Korrupcióellenes nyilatkozat megjelenítése   | Válassza ezt a lehetőséget, ha a költségjelentés létrehozásakor meg szeretné jeleníteni a korrupcióellenes szöveget. Ezután engedélyezhetők bizonyos költségkategóriák, amelyek megkövetelik a korrupcióellenes nyilatkozat kiválasztását a költségjelentés alatt. Például egy adott kormányzati tisztviselőkkel kapcsolatos kiadáshoz kapcsolódó ajándékkategória esetében előfordulhat, hogy az alkalmazottnak igazolnia kell, hogy a költség megfelel a kormányzati tisztviselőkhöz kapcsolódó vállalati irányelveknek. |
| Korrupcióellenes üzenet a beküldő számára | Adja meg azt a szöveget, amelynek a költségjelentés létrehozását végző alkalmazott számára meg kell jelennie. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, válassza a **Fordítások** lehetőséget. |
| Korrupcióellenes üzenet a jóváhagyó számára  | Adja meg azt a szöveget, amelynek a költségjelentés létrehozásakor a jóváhagyó számára meg kell jelennie. Ha nyelvfüggő szöveget szeretne beírni, amely a felhasználói nyelv alapján jelenik meg, válassza a **Fordítások** lehetőséget. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]