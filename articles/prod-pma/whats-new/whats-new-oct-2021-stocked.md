---
title: Újdonságok vagy változások a Project Operationsben, 2021. október a készletezett/éles környezetben tárolt forgatókönyvek esetén
description: Ez a cikk a Project Operations 2021. októberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a készletezett/éles környezetben használt forgatókönyvekhez.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029946"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Újdonságok vagy változások a Project Operationsben, 2021. október a készletezett/éles környezetben tárolt forgatókönyvek esetén

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.22-es verzió
 
## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
|--------------|------------------|----------------|
| Projektvezetés és könyvelés | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | A folyamatban lévő projektmunka (WIP) és a felhalmozott bevételi összegek nincsenek megfelelően visszavonva, amikor egy vállalatközi vevői számlát feladnak. |
| Projektvezetés és könyvelés | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A **Projektbezárás megakadályozása, ha vannak nyitott tranzakciók léteznek** funkció, nem működik. |
| Projektvezetés és könyvelés | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A szabadszöveges számlák számlázási besorolása nem tölti ki automatikusan a projektek dimenzióit, ha az adott funkció engedélyezve van. |
| Projektvezetés és könyvelés | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Nem vállalatközi forgatókönyvekben a wip- és a felhalmozott bevételi összegek nem lesznek megfelelően visszavonva a projektszámla feladásakor. |
| Projektvezetés és könyvelés | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | A terhelési és jóváírási értékek akkor váltanak át, ha a Microsoft Excel bővítményt a Projekt költségnaplójával együtt használják, és az **Ellenszámla típusa** mező Project értékre **van állítva**. |
| Projektvezetés és könyvelés | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | A projekttranzakciókban feladott összeg túlbecsüli egy olyan projektvásárlási rendelést, amely készletezett cikkeket tartalmaz, és amely nem vonható leadóösszegekkel rendelkezik, amikor **a UseTax** meg van jelölve. |
| Projektvezetés és könyvelés | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | A rendszer felosztja az összeget a projekt eredményjelentései és a projekt WIP-jelentései között. |
| Projektvezetés és könyvelés | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Az aktuális készlet helytelen a részben visszaadott cikkszükséglet kiigazítása után. |
| Projektvezetés és könyvelés | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Az erőforrásnevek ismétlődnek a Project Operationsben, amikor a Microsoft Projectben szerkesztik őket. |
| Projektvezetés és könyvelés | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | A vállalatközi költségjelentések, amelyek vállalatközi függőben lévő szállítói számlaköltségekkel rendelkeznek, először a **Projekt WIP költségfelfüggesztési** típusába kerülnek feladásra. A feldolgozás során azonban a becsléssel kapcsolatos költségek a projekt költségfelfüggesztési **típusába kerülnek feladásra** a várt **vállalatközi költségfelfüggesztési** típus helyett. |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A szállítói megtartási eredmények a projekt költségtranzakcióiban nem jelennek meg. |
| Projektvezetés és könyvelés | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A munkaidő-nyilvántartásnak a tranzakció pénznemében lévő tranzakció összegét meghatározott számú tizedesjegyre kell kerekítenie az összes könyvelési felosztás és általános naplófelosztási bejegyzés esetében. |
| Projektvezetés és könyvelés | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | A projektcikk-követelmények mennyisége automatikusan frissül a tervezett rendelések véglegesítésekor. |
| Projektvezetés és könyvelés | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | A bizonylatszám, a tranzakciótípus szállítói egyenlege és a számlaszám nem vonható vissza a beszerzési rendelés előlegszámláján. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számla integrációja be van kapcsolva. |
| Projektvezetés és könyvelés | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projekt költségnapló létrehozásakor a költségösszeg megjelenik a **Jóváírás** mezőben. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Előfordulhat, hogy a munkaidő-nyilvántartási bizonylatokat újra felhasználjuk, ha a számsorozat folyamatosként van beállítva. |
| Projektvezetés és könyvelés | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIAORSZÁG: A **Manuális megőrzési összeg** logika nem egyezik meg a **Projektszerződés számlajavaslatában szereplő Automatikus visszatartási összeg** logikával. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói visszatartás felszabadításakor a bizonylat feladása helytelen további sorokat tartalmaz. |
| Projektvezetés és könyvelés | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ha a **Számlajavaslat** létrehozása lapon a **Számla dátuma** mező megváltozik, a következő hibaüzenet jelenhet meg: "Az objektumhivatkozás nincs beállítva egy objektumpéldányra." |
| Projektvezetés és könyvelés | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Hiba történik, amikor megpróbál jóváhagyni egy munkaidő-nyilvántartást a **TSLine-munkafolyamatból**, és szombatra és vasárnapra van időnyilvántartási szabályzat. |
| Projektvezetés és könyvelés | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | A számlajavaslat tranzakciós összesítéseinek kiszámításakor a kezdő egyenleg projektelemtípus ki lesz zárva a Számlajavaslat tranzakciós **összesítései közül**. |
| Projektvezetés és könyvelés | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ha egy projekt termelési rendelésének felhasználási költsége 0 (nulla), a következő hibaüzenet jelenik meg, amikor megpróbálja megbecsülni: "Megpróbálta nullával osztani." |
| Projektvezetés és könyvelés | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A Project Timesheet Mobile alkalmazás a válaszadás leállításához Android. A probléma a TimeEntryDataManager ArgumentNullExceptionnel **kapcsolatos**. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs naplója sikertelen lesz, amikor feladja, mert egy fiókból hiányoznak a dimenziók. A dimenziókat nem tartalmazó fiók azonban nem az a fiók, amelybe közzétesz. |
| Projektvezetés és könyvelés | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | A **keresésekben a ToDate** szűrő nem törlődik, ha el van távolítva a **Feladási költség** oldal Kijelölés **párbeszédpaneléről**. |
| Projektvezetés és könyvelés | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Az összes terjesztés** alaphelyzetbe állítása sikertelen, és hibát jelez a csak **idő típusú projekthez** létrehozott munkaidő-nyilvántartásoknál. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető függőben lévő szállítói számlán, ha a beszerzési kategória hozzá van rendelve a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations szolgáltatásba Dataverse. |
| Projektvezetés és könyvelés | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | A vállalatközi projektkiigazítási tranzakciók esetében problémák vannak a célvállalatnál. |
| Projektvezetés és könyvelés | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Egy projekt lekötött költségei rossz mennyiséget és önköltségi árat számítanak ki, ha a beszerzési rendelés év végi folyamatával **dolgozták** fel a főkönyvben. |
| Projektvezetés és könyvelés | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ha egy minőségi rendeléseket tartalmazó projekt termelési rendelést befejezettként jelentenek, a következő hibaüzenet jelenik meg: "Nincs készlettranzakcióval megjelölt virtuális tranzakció." |
| Projektvezetés és könyvelés | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projekttel kapcsolatos kötelezettségek számlájának feladásakor a következő hibaüzenet jelenik meg: "Enumerált szöveg Projekt - költség - cikk nem létezik." |
| Projektvezetés és könyvelés | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | A közvetett költségek megduplázódnak, ha manuálisan gyűjti össze a bevételt. |
| Projektvezetés és könyvelés | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Az elhatárolt bevétel és a WIP-feladás nem eredményez tranzakciókat. |
| Projektvezetés és könyvelés | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A függőben lévő ár aktiválása sikertelen egy elszámolóköltség-cikk esetében, ha létezik fogadott projektvásárlási rendelés. |
| Projektvezetés és könyvelés | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | A számlafeladás wip-visszafordított értéke eltér az eredeti közzétett WIP-értéktől az időbeviteltől. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | A projektből kiszámlázott bevételekre vonatkozóan könyvelési probléma áll fenn az alkalmazott megőrző esetekben, amikor az utalványon szereplő tranzakciók nem állnak ki egyenlegen. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A becslés létrehozása a számlajavaslat feladása után blokkolja a korrekciós sorok importálását a Project Operationsben. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes mértékben számlázott mérföldkő-rekord módosítása nem lehetséges. |
| Projektvezetés és könyvelés | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automatikus terhelések használata esetén a munkaidő-nyilvántartáshoz tartozó vállalatközi vevői számla nem adható fel, és hibaüzenet jelenik meg. |
| Projektvezetés és könyvelés | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Az alprojekt címe nincs megfelelően frissítve. |
| Projektvezetés és könyvelés | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | A cikkszükségletek önköltségi ára frissül a konszolidált beszerzési rendelések vételárával. |
| Projektvezetés és könyvelés | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | A közzétett költség nem megfelelő a vételár frissítése és a Változáskezelés **aktiválása paraméter** engedélyezése után. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Az összes felhasználói költség látható, amikor egy kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciók és az áfatranzakciók helytelen összegei egy hitelkártya-tranzakcióból létrehozott költségből kerülnek feladásra. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Irreleváns figyelmeztető üzenet jelenik meg a költségjelentési oldalak frissítésekor. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A rendszer rossz ideiglenes jóváhagyót használ, amikor töröl egy ideiglenes jóváhagyót, majd újra benyújtja a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Feladási hiba lép fel, amely a futásteljesítmény beállításához kapcsolódik. |
| Utazás és költség | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A felosztás nem frissíti a jogi személyt, ha egy nem csatolt tranzakciót újra hozzáadnak egy vállalatközi költség költség költségjelentéséhez. |

### <a name="regulatory-updates"></a>Szabályozási frissítések

További információ a pénzügyi és üzemeltetési alkalmazások szabályozási frissítéseiről: [Szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates). Bejelentkezhet a Lifecycle Services (LCS) szolgáltatásba Microsoft Dynamics is, és a Problémakereső eszközzel megtekintheti a tervezett szabályozási frissítéseket. A problémakeresés lehetővé teszi az ország vagy régió, a funkció típusa és a kiadás szerinti keresést.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
