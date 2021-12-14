---
title: A Projektműveletek újdonságai vagy módosítása, 2021. október a készletezett/termelésalapú forgatókönyvek esetében
description: Ez a témakör tájékoztatást nyújt a raktározott/termelésalapú forgatókönyvek projektműveleteinek 2021. októberi kiadásában elérhető minőségi frissítésekről.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818320"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>A Projektműveletek újdonságai vagy módosítása, 2021. október a készletezett/termelésalapú forgatókönyvek esetében

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektmenedzsment és számvitel Dynamics 365 Finance környezetben verzió 10.0.22
 
## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
|--------------|------------------|----------------|
| Projektvezetés és könyvelés | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | A folyamatban lévő projektmunka (folyamatban lévő munka) és az elhatárolt bevételösszegek nem megfelelően lesznek visszafordítva a vállalatközi vevői számla könyvelésekor. |
| Projektvezetés és könyvelés | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A **Projekt lezárásának megakadályozása nyitott tranzakciók esetén** funkció nem működik. |
| Projektvezetés és könyvelés | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A szabadszöveges számlák számlázási besorolása nem tölti ki automatikusan a projektek méreteit, ha ez a funkció engedélyezve van. |
| Projektvezetés és könyvelés | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Nem vállalatközi esetekben a folyamatban lévő munka és az elhatárolt bevételi összegek nem megfelelően lesznek visszamenetben a projektszámlák könyvelésekor. |
| Projektvezetés és könyvelés | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | A terhelési és hitelértékek akkor váltanak, ha a Microsoft Excel bővítményt a Projekt költségnaplóval, az **Eltolás számlatípus mezőt pedig** Projekt értékre **állíthatja.** |
| Projektvezetés és könyvelés | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | A projekttranzakciókban feladott összeg túlértékelhető egy olyan projektvásárlási rendelésen, amely raktározott cikkeket tartalmaz, és amely a **UseTax jelölésekor nem levonható adóösszegekkel** rendelkezik. |
| Projektvezetés és könyvelés | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | A rendszer felosztja az összeget a projekt eredményjelentései és a projekt folyamatban lévő munkajelentései között. |
| Projektvezetés és könyvelés | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Az aktuális készlet helytelen a részlegesen visszaadott cikkszükséglet módosítása után. |
| Projektvezetés és könyvelés | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Az erőforrásnevek a Microsoft Projectben való szerkesztéskor duplikálódnak a Project Operations programban. |
| Projektvezetés és könyvelés | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | A vállalatközi költségjelentések, amelyeken a kötelezettségeket függő szállítói számlaköltségek teszik ki, először a **projekt befejezetlen** költségkönyvelési típusába kerülnek. A feldolgozás során azonban a becsült költségek a **várt** vállalatközi költségkönyvelési típus helyett a projektköltség-könyvelés **típusba** kerülnek. |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A szállító megtartja a projektköltség-tranzakciók eredményeit, és nem jelennek meg. |
| Projektvezetés és könyvelés | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A munkaidő-nyilvántartásnak a tranzakció pénznemében szereplő tranzakció összegét az összes könyvelési eloszlás és a főkönyvi napló felosztási tételének meghatározott számú tizedesjegyére kell kerekítenie. |
| Projektvezetés és könyvelés | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | A projektcikk-követelmények mennyisége automatikusan frissül a tervezett rendelések firm firmakorásakor. |
| Projektvezetés és könyvelés | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | A bizonylatszám, a tranzakciótípus szállítói egyenlege és a számlaszám nem vonható vissza a beszerzési rendelés előrefizetési számláján. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számlaintegráció be van kapcsolva. |
| Projektvezetés és könyvelés | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projekt költségnapló létrehozásakor a költségösszeg a Hitel mezőben jelenik **meg**. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | A munkaidő-nyilvántartási bizonylatok újra felhasználhatók, ha a számsorozat folyamatosként van beállítva. |
| Projektvezetés és könyvelés | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIAORSZÁG: A **kézi megőrzési összeg** logikája nem felel meg a **Projektszerződés számlajavaslat automatikus megőrzési összeg** logikájának. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói megőrzés felszabadításakor a bizonylat könyvelése helytelen további sorokat mutat be. |
| Projektvezetés és könyvelés | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | A **·** **Számlajavaslat létrehozása lap Számladátum** mezőjének módosításakor a következő hiba léphet fel: "Az objektumhivatkozás nincs egy objektum példányára állítva." |
| Projektvezetés és könyvelés | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Hiba történik, amikor megpróbál jóváhagyni egy munkaidő-nyilvántartást a **TSLine** munkafolyamatból, és van egy munkaidő-nyilvántartási szabályzat szombatra és vasárnapra. |
| Projektvezetés és könyvelés | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | A számlajavaslat számlaösszegének kiszámításakor a kezdő egyenleg projekt cikktípusa ki van zárva **a Számlajavaslat tranzakciós** összegzéseiből. |
| Projektvezetés és könyvelés | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ha egy projekt gyártási rendelésének fogyasztási költsége 0 (nulla), a következő hiba lép fel, amikor megpróbálja megbecsülni: "Megpróbálva nullával megosztani." |
| Projektvezetés és könyvelés | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A Project Timesheet Mobile alkalmazás Android nem válaszol. A probléma a **TimeEntryDataManager ArgumentNullException-hez kapcsolódik**. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Projektműveletek integrációs naplója sikertelen a könyveléskor, mert egy fiókból hiányoznak a dimenziók. A dimenziókból hiányzó fiók azonban nem az a fiók, amelyre felad. |
| Projektvezetés és könyvelés | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | A **keresések ToDate** szűrője nincs törölve, amikor eltávolítják a **Költség közzététele lap Kijelölés** **párbeszédpaneléről**. |
| Projektvezetés és könyvelés | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Az összes disztribúció alaphelyzetbe állítása** sikertelen, és hibát mutat a csak idő típusú projekthez létrehozott munkaidő-nyilvántartásokban. **·** |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt lap nem** szerkeszthető függőben lévő szállítói számlán, amikor a beszerzési kategóriát a cikkhez rendeli. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations Dataverse. |
| Projektvezetés és könyvelés | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | A vállalatközi projektkorrekciós tranzakciók esetében problémák merülnek fel a célvállalatban. |
| Projektvezetés és könyvelés | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | A projekt lekötött költségei rossz mennyiséget és önköltségi árat számítják ki, ha a beszerzési rendelést a Beszerzési rendelés év végi folyamata feldolgozta **a** Főkönyvben. |
| Projektvezetés és könyvelés | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ha egy minőségi rendeléseket mutató projekt gyártási rendelést készként jelent be, a következő hiba lép fel: "Nincs készlettranzakcióval megjelölt virtuális tranzakció." |
| Projektvezetés és könyvelés | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projekttel kapcsolatos kötelezettségek feladásakor a következő hiba lép fel: "Felsorolt szöveg Project - költség - cikk nem létezik." |
| Projektvezetés és könyvelés | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | A közvetett költségek megduplázódnak, ha manuálisan gyűjti a bevételeket. |
| Projektvezetés és könyvelés | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Az elhatárolt bevételek és a folyamatban lévő munka feladása nem eredményez tranzakciókat. |
| Projektvezetés és könyvelés | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A függőben lévő ár aktiválása sikertelen egy elszámolóár-cikk esetében, ha fogadott projektvásárlási rendelés létezik. |
| Projektvezetés és könyvelés | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | A folyamatban lévő munka által fordított érték a számlakönyvelésből eltér az eredeti könyvelt folyamatban lévő munka értékétől egy időtételtől. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | A projekt számlázott bevételeinek feladási problémája az alkalmazott rögzítő esetekben, amikor az utalvány tranzakciói nem egyenleggel. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A számlajavaslat feladása utáni becslés létrehozása blokkolja a korrekciós sorok importálását a Projektműveletekben. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes számlázott mérföldkőrekord módosítása nem lehetséges. |
| Projektvezetés és könyvelés | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automatikus díjak használata esetén a munkaidő-nyilvántartás vállalatközi vevői számlája nem könyvelhető, és hibaüzenet jelenik meg. |
| Projektvezetés és könyvelés | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Az alprojekt címe nincs megfelelően frissítve. |
| Projektvezetés és könyvelés | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | A cikkkövetelmények önköltségi ára frissül a konszolidált beszerzési rendelések beszerzési árával. |
| Projektvezetés és könyvelés | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | A könyvelt költség nem helyes a beszerzési ár frissítése és a **Változáskezelés aktiválása paraméter** engedélyezése után. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Az összes felhasználói költség látható, ha kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciók és az áfatranzakciók helytelen összegeit a hitelkártya-tranzakcióból létrehozott költségből könyveli a termék. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | A költségjelentési lapok frissítésekor irreleváns figyelmeztető üzenet jelenik meg. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A program rossz időközi jóváhagyót használ, amikor töröl egy időközi jóváhagyót, majd újra benyújtja a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításához kapcsolódó feladási hiba lép fel. |
| Utazás és költség | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A felosztás nem frissíti a jogi személyt, ha egy független tranzakciót újra hozzáadnak a vállalatközi költségek költségjelentéséhez. |

### <a name="regulatory-updates"></a>Szabályozási frissítések

A Pénzügyi és műveleti alkalmazások szabályozási frissítéseiről a Szabályozási frissítések című témakörben talál további [információt](/dynamics365/finance/localizations/regulatory-updates). Bejelentkezhet Microsoft Dynamics életciklus-szolgáltatásokba (LCS), és a Probléma kereső eszközzel megtekintheti a tervezett szabályozási frissítéseket. A problémakeresés lehetővé teszi a keresést ország vagy régió, a szolgáltatás típusa és a kiadás szerint.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
