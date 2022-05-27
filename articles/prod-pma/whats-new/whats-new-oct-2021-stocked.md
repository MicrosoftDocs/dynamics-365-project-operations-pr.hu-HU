---
title: Újdonságok vagy változások a Project Operations 2021. októberi projektműveleteiben raktározott/termelésalapú forgatókönyvek esetén
description: Ez a témakör a Project Operations készletezett/termelésalapú forgatókönyvekhez kiadott 2021. októberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 03491ccab855e48819fccf4c9d2b584fd87cb4ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576043"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Újdonságok vagy változások a Project Operations 2021. októberi projektműveleteiben raktározott/termelésalapú forgatókönyvek esetén

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektmenedzsment és számvitel Dynamics 365 Finance környezetben 10.0.22-es verzió
 
## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
|--------------|------------------|----------------|
| Projektvezetés és könyvelés | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | A folyamatban lévő projektmunka és az elhatárolt bevételi összegek nem megfelelően sztornírozódnak vállalatközi vevői számla könyvelésekor. |
| Projektvezetés és könyvelés | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A **Projektbezárás megakadályozása nyitott tranzakciók esetén a** funkció nem működik. |
| Projektvezetés és könyvelés | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A szabadszöveges számlák számlázási besorolása nem tölti ki automatikusan a projektek dimenzióit, ha ez a funkció engedélyezve van. |
| Projektvezetés és könyvelés | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Vállalaton kívüli forgatókönyvekben a befejezetlen termelés és az elhatárolt bevétel összegei nem megfelelően sztornírozódnak a projektszámla könyvelésekor. |
| Projektvezetés és könyvelés | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | A tartozik és a követel érték akkor vált, ha a bővítményt a Microsoft Excel Projekt költségnaplóval használja, és az **Ellenszámla típusa** mező értéke **Project**. |
| Projektvezetés és könyvelés | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | A projekttranzakciókban feladott összeg túlbecsülődik egy olyan projekt beszerzési rendelésen, amely raktározott cikkeket tartalmaz, és amely nem levonható adóösszegekkel rendelkezik a UseTax **megjelölésekor**. |
| Projektvezetés és könyvelés | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | A rendszer felosztja az összeget a projekt eredményjelentései és a projekt folyamatban lévő munka jelentései között. |
| Projektvezetés és könyvelés | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Az aktuális készlet helytelen a részben visszaadott cikkszükséglet helyesbítése után. |
| Projektvezetés és könyvelés | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Az erőforrásnevek ismétlődnek a Project Műveletek programban, amikor a Microsoft Project programban szerkesztik őket. |
| Projektvezetés és könyvelés | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | A vállalatközi költségjelentéseket, amelyekben a kötelezettségek vállalatközi függőben lévő szállítói számlaköltségek szerepelnek, a program először a **Projekt folyamatban lévő munka költségkönyvelési** típusába könyveli. A feldolgozás során azonban a becsült költségekkel kapcsolatos költségeket a program a **projektköltség-feladási** típusba könyveli a várt **vállalatközi költségfeladási** típus helyett. |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A szállítómegtartási eredmények a projektköltség-tranzakciókban nem jelennek meg. |
| Projektvezetés és könyvelés | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A munkaidő-nyilvántartásnak a tranzakció pénznemében lévő tranzakció összegét az összes könyvelési felosztáson és főkönyvi felosztási tételen megadott számú tizedesjegyre kell kerekítenie. |
| Projektvezetés és könyvelés | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | A projektcikk-követelmények mennyisége automatikusan frissül a tervezett rendelések megerősítésekor. |
| Projektvezetés és könyvelés | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | A bizonylatszám, a tranzakciótípus szállítói egyenlege és a számlaszám nem sztornírozható a beszerzési rendelés előlegszámláján. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla megszakad, ha a szállítói számla integrációja be van kapcsolva. |
| Projektvezetés és könyvelés | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projektköltség-napló létrehozásakor a költség összege a Jóváírás **mezőben** jelenik meg. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | A munkaidő-nyilvántartási bizonylatok újra felhasználhatók, ha a számsorozat folyamatosként van beállítva. |
| Projektvezetés és könyvelés | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIAORSZÁG: A **kézi megőrzési összeg** logikája nem felel meg a **Projektszerződés számlajavaslat automatikus megőrzési összeg** logikájának. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | A szállítói megőrzés felszabadításakor a bizonylat feladása helytelen további sorokat tartalmaz. |
| Projektvezetés és könyvelés | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ha a **Számlajavaslat** létrehozása lap Számladátum **mezője** megváltozik, a következő hiba léphet fel: "Az objektumhivatkozás nincs objektumpéldányra állítva." |
| Projektvezetés és könyvelés | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Hiba lép fel, amikor megpróbál jóváhagyni egy munkaidő-nyilvántartást a **TSLine** munkafolyamatból, és szombatra és vasárnapra van egy munkaidő-nyilvántartási szabályzat. |
| Projektvezetés és könyvelés | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | A számlajavaslat számlaösszegének kiszámításakor a program kizárja a kezdő egyenleg projektcikktípusát a Számlajavaslat tranzakció-összefoglalóiból **·**. |
| Projektvezetés és könyvelés | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ha a projekt gyártási rendelésének felhasználási költsége 0 (nulla), a következő hiba lép fel, amikor megpróbálja megbecsülni: "Kísérlet nullával való osztásra." |
| Projektvezetés és könyvelés | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A Project Timesheet Mobile alkalmazás Android nem válaszol. A probléma a TimeEntryDataManager ArgumentNullException függvényhez **kapcsolódik**. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs napló könyveléskor sikertelen, mert a fiókból hiányoznak a dimenziók. Az a számla azonban, amelyből hiányoznak a dimenziók, nem az a számla, amelyre könyvel. |
| Projektvezetés és könyvelés | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | A **Keresések ToDate** szűrője nem törlődik, ha eltávolítja a **Költség** közzététele lap Kijelölés **párbeszédpaneljéről**. |
| Projektvezetés és könyvelés | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Az összes terjesztés** alaphelyzetbe állítása sikertelen, és hibát mutat a csak **idő típusú projekthez** létrehozott munkaidő-nyilvántartások esetében. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető függőben lévő szállítói számlán, ha a beszerzési kategória hozzá van rendelve a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | A navigációs ablak hiányzik, ha nincs bejelentkezve a Project Operations programba Dataverse. |
| Projektvezetés és könyvelés | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Vállalatközi projekthelyesbítési tranzakciók esetén problémák merülnek fel a célvállalatnál. |
| Projektvezetés és könyvelés | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | A projekt lekötött költségei helytelen mennyiséget és önköltségi árat számítanak ki, ha a beszerzési rendelést a Beszerzési rendelés év végi folyamata **dolgozta** fel a főkönyvben. |
| Projektvezetés és könyvelés | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ha egy minőségi rendeléseket tartalmazó projekt gyártási rendelést befejezettként jelent meg, a következő hiba jelenik meg: "Nincs készlettranzakcióval jelölt virtuális tranzakció." |
| Projektvezetés és könyvelés | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projekthez kapcsolódó kötelezettségek számlájának könyvelésekor a következő hiba jelenik meg: "Számozott szöveg Projekt - költség - cikk nem létezik." |
| Projektvezetés és könyvelés | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | A közvetett költségek megduplázódnak, ha manuálisan gyűjt bevételt. |
| Projektvezetés és könyvelés | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Az elhatárolt bevétel és a befejezetlen termelés feladása nem eredményez tranzakciókat. |
| Projektvezetés és könyvelés | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A függőben lévő ár aktiválása sikertelen egy elszámolóárcikk esetében, ha fogadott projekt beszerzési rendelés létezik. |
| Projektvezetés és könyvelés | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | A számlakönyvelés folyamatban lévő munka sztornírozott értéke eltér az idő tétel eredeti könyvelt befejezetlen termelés értékétől. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | A projekt számlázott bevételének feladási kiadása van az alkalmazott megőrző esetekben, amikor a bizonylaton szereplő tranzakciók nem egyensúlyoznak. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A becslés létrehozása a számlajavaslat feladása után blokkolja a korrekciós sorok importálását a Projektműveletek mezőben. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes mértékben számlázott mérföldkőrekord módosítása nem lehetséges. |
| Projektvezetés és könyvelés | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automatikus költségek használata esetén a munkaidő-nyilvántartás vállalatközi vevői számlája nem könyvelhető, és hibaüzenet jelenik meg. |
| Projektvezetés és könyvelés | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Az alprojekt címe nincs megfelelően frissítve. |
| Projektvezetés és könyvelés | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | A cikkszükségletek önköltségi ára frissül a konszolidált beszerzési rendelések beszerzési árával. |
| Projektvezetés és könyvelés | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | A feladott költség nem megfelelő a beszerzési ár frissítése és a Változáskezelés **aktiválása paraméter** engedélyezése után. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden felhasználói költség látható, amikor kategóriát keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciókon és az áfatranzakciókon helytelen összegek feladása egy hitelkártya-tranzakcióból létrehozott költségből történik. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | A költségjelentési lapok frissítésekor irreleváns figyelmeztető üzenet jelenik meg. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | A rendszer nem megfelelő időközi jóváhagyót használ, amikor töröl egy időközi jóváhagyót, majd újra elküldi a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Feladási hiba lép fel, amely a futásteljesítmény beállításához kapcsolódik. |
| Utazás és költség | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A disztribúció nem frissíti a jogi személyt, ha egy nem csatolt tranzakciót újra hozzáad a költségjelentéshez egy vállalatközi költségről. |

### <a name="regulatory-updates"></a>Szabályozási frissítések

A Pénzügyi és üzemeltetési alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalókért tanulmányozza a Szabályozási frissítések című [témakört](/dynamics365/finance/localizations/regulatory-updates). Bejelentkezhet az életciklus-szolgáltatásokba Microsoft Dynamics (LCS), és a Probléma keresőeszközzel megtekintheti a tervezett szabályozási frissítéseket. A problémakeresés lehetővé teszi az ország vagy régió, a funkció típusa és a kiadás szerinti keresést.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
