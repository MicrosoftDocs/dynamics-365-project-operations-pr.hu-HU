---
title: Újdonságok vagy változások 2021 októberében – Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez
description: Ez a cikk információval szolgál a készletalapú/termelésalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2021 októberi kiadásában váltak elérhetővé.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Újdonságok vagy változások 2021 októberében – Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.22-es verziójú környezetekben
 
## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
|--------------|------------------|----------------|
| Projektvezetés és könyvelés | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | A folyamatban lévő projektmunkához (WIP) és a görgetett bevételi összegekhez tartozó bevételek sztornózása helytelen egy vállalatközi ügyfélszámla feladásakor. |
| Projektvezetés és könyvelés | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A **Projekt lezárásának megakadályozása nyitott tranzakciók esetén** funkció nem működik. |
| Projektvezetés és könyvelés | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Egy szabadszöveges számla számlázási besorolása a funkció engedélyezésekor nem tölti ki automatikusan a projektekből a dimenziókat. |
| Projektvezetés és könyvelés | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Nem vállalatközi forgatókönyvek esetén a WIP és a görgetett bevételi összegekhez tartozó bevételek sztornózása helytelen a projektszámla feladásakor. |
| Projektvezetés és könyvelés | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | A terhelési és jóváírási értékek fel vannak cserélve, amikor a Microsoft Excel bővítményt használják a Projektköltség-naplóhoz és az **Ellenszámla típusa** mező beállítása **Projekt**. |
| Projektvezetés és könyvelés | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | A projekttranzakciókban feladott összeget a program egy olyan projektbeszerzési rendeléseken túlbecsüli, amelyek olyan készleten lévő cikket tartalmaznak, amelyek nem levonható adósszegekkel rendelkeznek, ha az **Importadó** be van jelölve. |
| Projektvezetés és könyvelés | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | A rendszer felosztja az összeget a projekt nyereség- és veszteségjelentései és a projekt folyamatban lévő munkáinak jelentései között. |
| Projektvezetés és könyvelés | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | A részlegesen visszaküldött cikk-követelményének beállítása után nem megfelelő az aktuális készlet. |
| Projektvezetés és könyvelés | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | A Microsoft Projectben szerkesztésekor az erőforrásnevek duplikáltak a Project Operations alkalmazásban. |
| Projektvezetés és könyvelés | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Azok a vállalatközi költségjelentések , amelyeknél a Kötelezettségekhez tartozó vállalatközi szállítói számlaköltségek vannak először a **Projekt WIP-költség** feladási típushoz vannak feladva. Azonban a feldolgozás során a becsléshez kapcsolódó költségeket a program a **Projektköltség** feladási típushoz adja közzé a várt **Vállalatközi költség** feladási típus helyett. |
| Projektvezetés és könyvelés | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | A szállító visszatartási eredményei nem jelennek meg a projektköltség-tranzakciókban. |
| Projektvezetés és könyvelés | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Az munkaidő-nyilvántartásnak a tranzakció pénznemében szereplő összeget megadott számú tizedesjegyre kell kerekítenie az összes könyvelési felosztásban és az általános napló-hozzárendelési bejegyzésekben. |
| Projektvezetés és könyvelés | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | A projektcikk-követelmények mennyiségét a rendszer automatikusan frissíti, amikor a tervezett megrendeléseket megerősítik. |
| Projektvezetés és könyvelés | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | A bizonylatszám, a tranzakció típusú szállítói egyenleg és a számlaszám nem sztornózható egy beszerzési rendelés előlegszámláján. |
| Projektvezetés és könyvelés | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A vállalatközi szállítói számla hibás, amikor a szállítói számlák integrálása be van kapcsolva. |
| Projektvezetés és könyvelés | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Projektköltségnapló létrehozásakor a költség összege a **Jóváírás** mezőben jelenik meg. |
| Projektvezetés és könyvelés | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | A projektszámlák fizetési feltételei nem a várt módon működnek. |
| Projektvezetés és könyvelés | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Az időnyilvántartás-bizonylatok újra felhasználhatók, amikor a számsorozat folyamatosként van beállítva. |
| Projektvezetés és könyvelés | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIAORSZÁG: A **Manuális foglalóösszeg** logikája nem egyezik meg a Projektszerződés számlajavaslatában szereplő **Automatikus foglalóösszeg** logikával. |
| Projektvezetés és könyvelés | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Egy szállítói foglaló kiadásakor a bizonylat feladása további helytelen sorokat tartalmaz. |
| Projektvezetés és könyvelés | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ha módosul a **Számla dátuma** mező a **Számlajavaslat létrehozása** lapon, a következő hiba fordulhat elő: "Az objektumhivatkozás nincs beállítva egy objektumpéldányra.” |
| Projektvezetés és könyvelés | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Hiba történik, ha a **TSLine** munkafolyamatból megpróbál jóváhagyni egy időnyilvántartást, és van egy idővonal-szabályzat a szombatra és vasárnapra. |
| Projektvezetés és könyvelés | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | A kezdő egyenleg projektelemtípus ki van zárva a **Számlajavaslat tranzakcióösszegzéseiből**, amikor a számlajavaslat számlaösszege kiszámításra kerül. |
| Projektvezetés és könyvelés | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ha a projekt gyártási megrendelésének költségköltsége 0 (nulla), akkor a következő hiba történik a becslés során: „Nullával próbált osztani.” |
| Projektvezetés és könyvelés | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Az Android Project Timesheet mobilalkalmazás nem válaszol. A probléma a **TimeEntryDataManager ArgumentNullException** argumentumhoz kapcsolódik. |
| Projektvezetés és könyvelés | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | A Project Operations integrációs naplója hibát ad, amikor megpróbálja feladni mert egy számlából dimenziók hiányoznak. A számla amelyekből hiányoznak a dimenziók azonban nem az a számla, amelyre felad. |
| Projektvezetés és könyvelés | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | A keresésben a **ToDate** szűrő nem törlődik, amikor eltávolításra kerül a **Költség feladása** lapon a **Kijelölés** párbeszédpanelről. |
| Projektvezetés és könyvelés | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Az összeselosztás visszaállítása** sikertelen, és hibaüzenet jelenik meg olyan időnyilvántartásokhoz, amelyek egy **Csak idő** típusú projekthez lettek létrehozva. |
| Projektvezetés és könyvelés | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | A **Projekt** lap nem szerkeszthető egy függőben lévő szállítói számlán, amikor egy beszerzési kategória van társítva a cikkhez. |
| Projektvezetés és könyvelés | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ha nem jelentkezik be a Project Operations Dataverse-be, akkor hiányzik a navigációs ablak. |
| Projektvezetés és könyvelés | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Az vállalatközi projektkorrekciós-tranzakcióknál problémák vannak a célvállalatnál. |
| Projektvezetés és könyvelés | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | A projekthez vállalt költségek nem a megfelelő mennyiséget és költségárat számítják ki, ha a vételi megrendelést a Főkönyv **Vételi megrendelés év végi folyamata** alapján dolgozták fel. |
| Projektvezetés és könyvelés | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Amikor egy olyan projekt gyártási megrendelését, amelyhez minőségi megrendelések vannak, befejezettként jelentenek, a következő hibaüzenet jelenik meg: „Nincs készlettranzakcióval megjelölve virtuális tranzakció.” |
| Projektvezetés és könyvelés | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projekthez kapcsolódó Kötelezettségek számla feladás a során következő hiba történik: "Felsorolásszöveg Projekt – költség – elem nem létezik.” |
| Projektvezetés és könyvelés | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | A bevételek manuális görgetése esetén a közvetett költségek megduplázódnak. |
| Projektvezetés és könyvelés | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | A bevételek görgetése és a folyamatban lévő munka feladása nem hoz létre tranzakciókat. |
| Projektvezetés és könyvelés | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A függőben lévő ár aktiválása sikertelen egy általános költségelem esetén, ha egy beérkezett projekt beszerzési rendelés létezik. |
| Projektvezetés és könyvelés | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | A folyamatban lévő sztornírozott érték a számla feladásából eltér az eredetileg feladott folyamatban lévő értéktől az időbejegyzésből. |
| Projektvezetés és könyvelés | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Feladási probléma tapasztalható a projekthez számlázott bevételhez foglalót alkalmazó esetekhez, ahol a bizonylat tranzakciói nem egyenlítődnek ki. |
| Projektvezetés és könyvelés | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A becslés létrehozása a számlajavaslat közzététele után letiltja a helyesbítő sorok importálását a Project Operations alkalmazásba. |
| Projektvezetés és könyvelés | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A teljes számlázott mérföldkövek rekordjának módosítása nem szabad, hogy lehetséges legyen. |
| Projektvezetés és könyvelés | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Automatikus díjak használata esetén nem lehet közzé tenni az vállalatközi ügyfélszámlát egy időnyilvántartáshoz, és egy hibaüzenet jelenik meg. |
| Projektvezetés és könyvelés | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Az alprojekten a cím frissítése nem megfelelően történik. |
| Projektvezetés és könyvelés | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | A cikkkövetelmények önköltségi árát a rendszer a összesített megrendelésekhez a beszerzési árral frissíti. |
| Projektvezetés és könyvelés | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | A közzétett költség nem helyes a beszerzési ár frissítése és a **Változáskezelés aktiválása** paraméter engedélyezése után. |
| Utazás és költség | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Minden felhasználói költség látható, amikor kategóriára keres a Költség mobilalkalmazásban. |
| Utazás és költség | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | A szállítói tranzakciókkal és áfatranzakciókkal kapcsolatosan helytelen összegek vannak közzétéve egy olyan kiadásból, amelyet egy hitelkártyatranzakcióból hoztak létre. |
| Utazás és költség | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Egy irreleváns figyelmeztető üzenet jelenik meg a költségjelentés oldalainak frissítésekor. |
| Utazás és költség | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nem a megfelelő ideiglenes jóváhagyó van használva, amikor ideiglenes jóváhagyót töröl, majd újra beküld a munkafolyamaton keresztül. |
| Utazás és költség | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | A futásteljesítmény beállításával kapcsolatos feladási hiba történik. |
| Utazás és költség | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A vállalatközi költségsorokon a terjesztés nem frissíti a jogi személyt, ha a egy nem mellékelt tranzakciót újra hozzáadnak a költségjelentéshez. |

### <a name="regulatory-updates"></a>Szabályozási frissítések

A pénzügyi és műveleti alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [Szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. A Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásba is bejelentkezhet, és megtekintheti a tervezett szabályozói frissítéseket a Problémakeresés eszköz segítségével. A Problémakereső segítségével országonként vagy régiónként, a szolgáltatás típusa és a kiadás között kereshet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
