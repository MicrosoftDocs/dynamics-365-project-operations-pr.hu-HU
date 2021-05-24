---
title: Újdonságok vagy módosítások 2021 áprilisában a Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez
description: Ez témakör a Project Operations 2021 áprilisi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a készleten/gyártáson alapuló forgatókönyvek esetében.
author: andchoi
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 2e2e3c1c717b5296964e0921aeec4999dd2f6e29
ms.sourcegitcommit: 69fadd3ce475d6aed2e1ed81a15becb28f020eb9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935567"
---
# <a name="whats-new-or-changed-in-project-operations-april-2021-for-stockedproduction-based-scenarios"></a>Újdonságok vagy módosítások 2021 áprilisában a Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.18-es verziójában
 
### <a name="quality-updates"></a>Minőségi frissítések
                                                                                                                                                                                  
| Funkcióterület                      | Hivatkozási szám| Minőségi frissítés                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektvezetés és könyvelés | [534393](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534393) | Hiba lép fel a **Projekt rendezési** rácsán.                                                                                                                                                      |
| Projektvezetés és könyvelés | [542850](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542850) | A lekötött összeg túlértékelt, miután az egységárat és a mennyiséget a projekt beszerzési megbízásában kijavították.                                                                                    |
| Projektvezetés és könyvelés | [543645](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543645) | A **ProjParameters** változó deklarálva van, de soha nem rendelt rekordpuffert a használat előtt.                                                                                     |
| Projektvezetés és könyvelés | [543674](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543674) | A **ResRollup**-táblák törlődnek, amikor a **Projekt erőforrásainak feltöltése az összes vállalathoz** kötegelt feladatában végrehajtásra kerül.                                                                          |
| Projektvezetés és könyvelés | [544417](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544417) | Probléma merült fel a **Projekt értékesítési ára** mező frissítésekor egy megrendelésen a **Beszerzési sorok V2** entitással.                                                                           |
| Projektvezetés és könyvelés | [547652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547652) | Az azonosítószámoktól függően alprojektek nem hozhatnak létre.   A következő hiba lép fel: "Function Global ::int642int helytelenül hívták."                                         |
| Projektvezetés és könyvelés | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | Az ügyfél rossz számlákat kap, amikor egy beszerzési kategóriával és tétellel rendelkező beszerzési rendelést számláz ki ugyanazon a számlán.                                                                      |
| Projektvezetés és könyvelés | [509920](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509920) | A projekttranzakció beállítása a közvetett költségekkel a számlázhatótól a nem számlázhatóig és vissza a számlázhatóig nem helyesen törli a WIP-t.                                       |
| Projektvezetés és könyvelés | [511274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511274) | A számlaösszegek helytelenek, amikor az értékesítési rendelésben a megőrzést és a teljes engedményt használják.                                                                                          |
| Projektvezetés és könyvelés | [511315](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511315) | A soradatokon lévő címnév akkor sem változik, ha egy másik tranzakciótípus van kiválasztva.                                                                           |
| Projektvezetés és könyvelés | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | A tételigényléssel és megrendeléssel lekötött költségek hibásak a megrendelés számlázási folyamatában a résztermék beérkezése és részszámlázás esetén.                       |
| Projektvezetés és könyvelés | [524226](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524226) | Amikor egy projekt pénzügyi dimenziói megváltoznak, a beszerzési rendelés fejléce nem tükrözi a változásokat.                                                                                                  |
| Projektvezetés és könyvelés | [524979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524979) | A generált **fix áras projekt** jelentés üres.                                                                                                         |
| Projektvezetés és könyvelés | [529445](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529445) | A számla nem választja ki a projekt azonosító hivatkozást a szállítói számlák áttekintésekor a **Fizetéskor fizetni** oldalon.                                                                          |
| Projektvezetés és könyvelés | [529982](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529982) | A munkaidő-nyilvántartás bejegyzése helytelen egy olyan felhasználó számára, aki korlátozott hozzáféréssel rendelkezik egy jogi személy számára a **HR-menedzser** szerepkörben, mivel a kategória nem hibásan működik.                                         |
| Projektvezetés és könyvelés | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | A projekt eredeti dátumát nem veszi figyelembe a módosítás, ami hibát okoz, ha **A módosítás dátumát új projektdátumként használja** mező **Nem** értékre van állítva.                                             |
| Projektvezetés és könyvelés | [530788](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530788) | Ha a projektbecsléseket köteg segítségével számítják ki, az eredmények helytelenek.                                                                                                         |
| Projektvezetés és könyvelés | [530834](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530834) | A projektszerződésre fordított összeg nem igazodik a projektre vonatkozó részösszeghez.                                                                             |
| Projektvezetés és könyvelés | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | A projektkönyvelő és a projektmenedzser szerepkörök nem tudnak jóváhagyási csoportbeállítással rendelkező óranaplót létrehozni.                                                                                 |
| Projektvezetés és könyvelés | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Nem tehet közzé Microsoft Excel importált Költségnaplót.                                                                                                                                       |
| Projektvezetés és könyvelés | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | A szállítói tranzakciók vállalatközi forgatókönyvekből való megfordítása megengedett, beleértve a szállítói számlákat és a költségjelentéseket is.                                                                     |
| Projektvezetés és könyvelés | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | A projektkiigazítás nem frissíti helyesen az értékesítés összegét a közvetett költségekkel.                                                                                                    |
| Projektvezetés és könyvelés | [534869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534869) | Ha egy fix áras projektszámlához jóváírást hoz létre, és az a szállítási számlázási szabályt használja, a kiadott egységek nem érhetők el újraszámlázásra. |
| Projektvezetés és könyvelés | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | Egy eltérő pénznemű projektszerződés nem számítja ki helyesen a számviteli pénznemet a tételnaplóban vagy a számlajavaslatban.                                                   |
| Projektvezetés és könyvelés | [537158](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537158) | Módosítsa a projektet a beszerzési rendelési sorban egy cikkkövetelmény átviteléhez.                                                                                                                          |
| Projektvezetés és könyvelés | [540603](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540603) | Az előrejelzésből a projekt költségvetésbe való importálás helytelen összegeket eredményez.                                                                                                                    |
| Projektvezetés és könyvelés | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5406222) | A főkönyvi tételek nem jönnek létre, amikor egy tranzakciót számlázhatóról nem számlázhatóra módosítanak.                                                                                            |
| Projektvezetés és könyvelés | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | A projekt tranzakciók nem jönnek létre pay-when-paid funkcióval, ha a **Költségösszeg-számítási funkció engedélyezése a projekt szállítói számlák visszatartási határideje esetében** funkció bekapcsolt állapotban van.                  |
| Projektvezetés és könyvelés | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | Több probléma a **Számlaajánlat készítése** oldalon.                                                                                                                             |
| Projektvezetés és könyvelés | [543390](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543390) | Az **Összes projekt** oldal nem mutatja a listát az új nyelvi kóddal.                                                                                                            |
| Projektvezetés és könyvelés | [543803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543803) | A projekt költségvetési egyenlegében a nem jóváhagyott költségvetési összeg helytelen, ha a költségvetést több mint kétszeresen módosítják.                                                                |
| Projektvezetés és könyvelés | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | A **Vásárlási megállapodás** lap nem látható azoknál a pénzügyi jogi személyeknél, amelyek integrálva vannak a Project Operations szolgáltatással.                                                                               |
| Projektvezetés és könyvelés | [545456](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545456) | A helyes bizonylatdátum nem töltődik fel a Projektórák napló soraiba.                                                                                                            |
| Projektvezetés és könyvelés | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Az erőforrás-alapú forgatókönyvek esetén a Project Operations alkalmazásban integrációs hiba miatt nem tud egy árajánlatot nyertre állítani.                                                                      |
| Projektvezetés és könyvelés | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | A Project Operations szolgáltatásban hibaüzenetet kap, amikor megpróbál asszociációt létrehozni egy szerződéssor és egy projektazonosító között, mert a szerződéssorok és tranzakciótípusok átfedéseinek ellenőrzése miatt.                        |
| Projektvezetés és könyvelés | [546949](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546949) | A **Forrás/projekt érvényesítési csoportok** oldal teljesítményproblémákkal küzd, ha a **ProjValEmplProjSetup** táblázatban több mint 14 000 rekord van.                                                                     |
| Projektvezetés és könyvelés | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | A **ProjCDSProjectContractEntity** beállíthatja a finanszírozási forrás számlacímét egy másik ügyfélből.                                                                                   |
| Projektvezetés és könyvelés | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | A 10.0.15-ös frissítés után nem érhető el az erőforrás szokásos keresése az oldalakon.                                                                                          |
| Projektvezetés és könyvelés | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | A megrendelési számla bizonylat főkönyvi számlája és feladási típusa nem egyezik meg a szolgáltatási tételnél. A projektcsoport **Egyenleg** értékre van beállítva, és a főkönyvi számla helytelen.                   |
| Projektvezetés és könyvelés | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | A tevékenységszám nem jelenik meg függőben lévő szállítói számlán, még akkor sem, ha a **Szülőtevékenység kiválasztásának blokkolása** **Nem** értékre van beállítva.                                            |
| Projektvezetés és könyvelés | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Ha a **Projekt** > **Költségvetés** > **Revíziók** > **Új** > **Importálás** navigációs útvonalat használja, a rendszer minden projekthez létrehozza a projektköltségvetés felülvizsgálatát.                                                            |
| Projektvezetés és könyvelés | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) | A helytelen könyvelési és főkönyvi tételek a különböző tranzakciós és könyvelési pénznemekkel rendelkező tranzakciók módosításakor fordulnak elő.                                                                        |
| Projektvezetés és könyvelés | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | A tranzakció feladási számlájának létrehozásakor nem szerepelnek méretek.                                                                                                   |
| Projektvezetés és könyvelés | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | A **PurchTotals.purchNewTotalAmount()** módszert függőben lévő szállítói számla létrehozásakor hívják, amely nem kapcsolódik semmilyen olyan megrendeléshez, amely teljesítménykibocsátást okoz.                    |
| Utazás és költség                | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | A futásteljesítmény beállításával kapcsolatban könyvelési hiba van.                                                                                                                                          |
| Utazás és költség                | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **A személyek szerinti osztás** a devizás költségtranzakciók esetében nem működik.                                                                                                         |
| Utazás és költség                | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | A költségkategória legördülő menüje helytelen kategóriákat mutat, függetlenül attól, hogy a **Meghatalmazottak** erőforrásként van-e beállítva.                                         |
| Utazás és költség                | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Erőforrás/kategória érvényesítési hiba miatt nem menthet vállalatközi költségjelentést.                                                                                             |
| Utazás és költség                | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | A költségjelentés feladásában a rossz futásteljesítmény-arány kiszámítása osztott vonalakat.                                                                                                        |
| Utazás és költség                | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Nem tehet közzé vállalatközi költségjelentést, ha az forgalmi adót tartalmazza, és a fizetési mód eltolási számlatípusa a **Munkavállaló**.                                                   |
| Utazás és költség                | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Visszaállítottuk a **TrvRequisitionLine** adatentitást és a hozzá tartozó egyedi, entitáshoz társított indexet.                                                                                            |
| Utazás és költség                | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | A költségjelentés egyes pontjain hozzáadott naplózás a forrásdokumentum-sorok létrehozásának és frissítésének támogatása érdekében.                                                                                           |
| Utazás és költség                | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | A helytelen alfőkönyvi napló jelenik meg vállalatközi forgatókönyv esetén, ha az áfa közzé van téve a Cél jogi entitásnak.                                              |
| Utazás és költség                | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | A Project Operations szolgáltatásban a költségbecslések nem törlődnek a Finance-ből, amikor törlik őket a Dataverse-ből.                                                                                         |
| Utazás és költség                | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ha egy költségkategória nem projektkategória, a **Költségek** lapon kiválasztott pénzügyi dimenziók nem lesznek átmásolva a költségjelentésbe.                                          |

### <a name="regulatory-updates"></a>Szabályozási frissítések
A Finance and Operations alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. Bejelentkezhet az LCS-be, és megtekintheti a tervezett szabályozási frissítéseket a Problémakereső eszközzel. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]