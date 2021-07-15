---
title: Újdonságok és változások 2021. júliusában – Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez
description: A témakör a Project Operations 2021. júliusi kiadásában készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez elérhető minőségi frissítésekkel kapcsolatban nyújt tájékoztatást.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: fb1814330b5e474ccbda0ab85dd67758a6f270a9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334552"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Újdonságok és változások 2021. júliusában – Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.20-es verziójában
 
### <a name="quality-updates"></a>Minőségi frissítések
                                                                                                                                                                                  
| Funkcióterület                      | Hivatkozási szám| Minőségi frissítés                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektvezetés és könyvelés | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | A beszerzési igénylésből származó költségvállalási rekordok akkor törlődnek, amikor a megrendelés fel van oldva a beszerzési igénylési problémájából.                                                                           |
| Projektvezetés és könyvelés | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | A költségvetés ellenőrzése beszerzési igénylés esetén kétszer történik meg. Ez a duplikálás azt jelenti, hogy nem lehet lezárni az igénylést, és nem jön létre a megfelelő beszerzési rendelés.                                                                                                                        |
| Projektvezetés és könyvelés | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Kerekítési probléma miatt nem lehet végrehajtani a **Számlázás ezen százalék elérésekor** számlázási szabályt.                                                                              |
| Projektvezetés és könyvelés | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Ha korrigálja a tranzakciót, és a százalékértékben tizedesjegyek vannak, a költség és az értékesítési ár nem megfelelően lesz korrigálva.                                      |
| Projektvezetés és könyvelés | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | A könyvelési forráskezelő megjeleníti egyetlen idővonalsor óráját jeleníti meg a különböző tevékenységekkel rendelkező több időnyilvántartás-sorhoz.                                      |
| Projektvezetés és könyvelés | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | A mentett nézetek és az időnyilvántartás-sor részleteinek személyre szabása hatására a rendszer mindig az első időnyilvántartás részleteit nyitja meg, amikor megpróbál megnyitni egy időnyilvántartást.  |
| Projektvezetés és könyvelés | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Az importálást követően a projekt gyökércsomópontja eltűnik és a munkalebontási struktúra rekordjai törölve lesznek.                                                                                             |
| Projektvezetés és könyvelés | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Ha a tételeket részben az cikk-követelményéből kapják meg és adják ki, akkor a rendszer nem a megfelelő költségfogyasztási egyenleget frissíti. |
| Projektvezetés és könyvelés | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | A projekt visszatartott megrendelései nem megfelelően mutatják az összesítéseket az **Összegek** ablaktáblában vagy a **Függőben lévő számla** rácson.                                                                  |
| Projektvezetés és könyvelés | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | A készlet lezárásakor a projektcikk költségkorrekciói az egyenlegszámlán vannak közzétéve az nyereség- és veszteségszámla helyett.                                                            |
| Projektvezetés és könyvelés | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | A projekthez feladott tranzakciós bizonylat és a becslési bizonylat amerikai dollárt (USD) használ könyvelési pénznemként, de az összeg azt tükrözi, amennyi ez CAD-ben lenne.              |
| Projektvezetés és könyvelés | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | A vállalt költségek cikk-követelménnyel és megrendelővel hibásak a megrendelés számlafolyamatában részleges terméknyugtával és részleges számlázással.       |
| Projektvezetés és könyvelés | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | A projektkiigazítás nem frissíti helyesen az értékesítés összegét a közvetett költségekkel.                                                                                    |
| Projektvezetés és könyvelés | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Hiányzik egy, az **Időnyilvántartás** táblából egy definiált kapcsolat a **Dolgozó/erőforrás** nézethez.                                                                                   |
| Projektvezetés és könyvelés | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nem lehet feltölteni a **Tevékenység száma** mezőt, amikor a legördülő menüből kiválasztja a vállalatközi időnyilvántartást.                                                                 |
| Projektvezetés és könyvelés | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | A következő oldalakhoz nem adhat hozzá személyre szabott **Cél** vagy **Tevékenységleírás** mezőt: **Projekthez feladott tranzakció**, **Számlajavaslat létrehozása** vagy **Számlajavaslat**.  |
| Projektvezetés és könyvelés | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Nem megfelelő kézbesítési dátum vezérlő van biztosítva, ha cikk-követelményeket hoz létre adatkezeléssel (**ProjSalesItemRequirementEntity**).                                              |
| Projektvezetés és könyvelés | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Amikor kiválaszt egy projektszerződés-azonosítót a Finaince-ban, a Project Operations integrált környezet megnyitja az oldalt egy rekord léterhozásához, ahelyett hogy megnyitná a meglévő projektszerződést.                                                                                                                 |
| Projektvezetés és könyvelés | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  A„@SYS4083080” címke („Nem található egy egyedi dolgozó rekord a megadott értékekkel”) nincs lefordítva dán nyelvre.                                |
| Projektvezetés és könyvelés | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | A **Cikkáfacsoport** mező nem szerkeszthető a számlajavaslaton.                                                                               |
| Projektvezetés és könyvelés | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | A vállalt költséget a rendszer túlbecsüli a levonható adóösszegekkel.                                                                                                    |
| Projektvezetés és könyvelés | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Egy több projekttel és különböző pénzügyi dimenziókkal rendelkező vállalatközi időnyilvántartás váratlan értékeket generál a főkönyvben.                             |
| Projektvezetés és könyvelés | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | A számlajavaslatok sorai duplikáltak, mivel az **Importálás előkészítésből** időszakos folyamat több példánya fut egyszerre.                                      |
| Projektvezetés és könyvelés | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Hiba történik a jóváírási számlaajánlat közzététele során, így a bizonylat tranzakciói nem egyenlítik ki egymást.    |
| Projektvezetés és könyvelés | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | A projektben vállalt költségek helytelenné válnak a váarkoztatott függőben lévő számlák feloldását követően.                                                                             |
| Projektvezetés és könyvelés | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nem lehet jóváírást létrehozni a projekt értékesítési megrendeléséhez, ha az adó nem a vállalat pénznemében van.                                      |
| Projektvezetés és könyvelés | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Egy szerződés törlésekor az ügyfélhez tartozó cím is törölve lesz.                                                                                     |
| Projektvezetés és könyvelés | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Negatív időtranzakció-helyesbítésből származó számlajavaslat nem tehető közzé.                                                                    |
| Utazás és költség                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Az adót a költségjelentések másképpen számítják.                                                                                                                  |
| Utazás és költség                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | A **DB72_Expense.updateTrvExpTransProjTransId()** kiadásfrissítés nem engedi meg a **trvExpTrans.ReferenceDataAreaId** számára új számsorozat létrehozását.                    |
| Utazás és költség                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | A kötelező mezőben nem látható a kitöltött összeg.                                                                                                             |
| Utazás és költség                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | A költség költségjelentéshez csatolása teljesítményének javítása a Költség újragondolva felhasználói felület segítségével.                                                            |
| Utazás és költség                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | A közzétett költségjelentések törölhetők.                                                                                           |
| Utazás és költség                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | A Költségszabályzat üzenete többször jelenik meg.                                                                                                       |
| Utazás és költség                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | A **Fizetési mód** mező az **Új költség** mezőben található.                                                                                                      |
| Utazás és költség                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Ha a munkafolyamat nem található, akkor a **Költségdokeumentum állapotának visszaállítása** eszköz vissza kell állítsa a költségjelentést **Vázlat** állapotra. 

### <a name="regulatory-updates"></a>Szabályozási frissítések
A Finance and Operations alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. A Lifecycle Services (LCS) szolgáltatásba is bejelentkezhet, és megtekintheti a tervezett szabályozói frissítéseket a Problémakeresés eszköz segítségével. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
