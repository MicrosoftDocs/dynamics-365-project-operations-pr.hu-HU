---
title: Újdonságok – 2021. január – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2021 januári kiadásában váltak elérhetővé.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958919"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. január – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

  - Project Operations a Dataverse-környezet 4.6.0.154 verzióján
  - Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.16-es verziójában

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| **Központi telepítés és konfiguráció** | 2106818 | Kijavította a webes erőforrás átnevezése, ami problémákat okozott egy oldal testreszabásával kapcsolatban. |
| **Számlázás és árképzés** | 2091908 | Kijavította az **Árképzés zárolása** és az **Aktuális árképzési használata** lehetőségeket a **Számla** lapon, ha a Project Operations a Dynamics 365 Field Service szolgáltatással együtt lett telepítve. |
| **Számlázás és árképzés** | 2103058 | Frissítette a **Projekt végösszegei** lehetőséget, hogy a feladat tényleges költségének null értékei kezelhetőek legyenek. |
| **Számlázás és árképzés** | 2116100 | Továbbfejlesztette a hibaüzeneteket, amelyek a **Tényadatok helyes bejegyzései** funkcióban jelennek meg. |
| **Számlázás és árképzés** | 2116129 | Továbbfejlesztette a költségbecslések láthatóságát a **Projektek** oldal **Becslések** fület. |
| **Számlázás és árképzés** | 2119112 | Kijavította a tényleges értékesítések és a tényleges költségek összesítését, amikor különböző árfolyamokkal vannak használva. |
| **Számlázás és árképzés** | 2134705 | Kijavította a **Számla** lap megnyitásakor és a Field Service telepítésekor a „Nem lehet beolvasni a meghatározatlan **getResourceString** tulajdonságát”. |
| **Lehetőségkezelés** | 2022195 | A **Projekt** oldal feladatalapú számlázási rácsa egy ikont tartalmaz, amely jelzi, hogy az adott feladathoz szerződés- vagy árajánlatsor kapcsolódik. |
| **Lehetőségkezelés** | 2029135 | Kijavította az üzleti folyamat hibát, amely akkor fordul elő, amikor a felhasználó olyan számlasort próbál megnyitni egy visszaigazolt számlán, amelyhez kiszámlázott előlegösszeg tartozik. |
| **Lehetőségkezelés** | 2040713 | Kijavította a szerződésből és a Field Service szolgáltatásból származó számla létrehozásakor jelentkező parancsfájlhibát. |
| **Projekttervezés és nyomon követés** | 2090202 | **Elavult** jelzéssel látta el a már nem használt üzleti szabályokat. |
| **Idő és költség** | 2091249 | Szigorított a vezérlőkön, hogy a felhasználók ne módosíthassák a feladatot egy elküldött vagy jóváhagyott időbejegyzésen. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance szolgáltatásban

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| **Projektvezetés és könyvelés** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Helytelen szerződésösszeg egy több forrásból álló rögzített árú projekt **Résszámlázás** lapján. |
| **Projektvezetés és könyvelés** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Az **Invoiceproposal.PSAnfRefProjId** helyőrzője nem jeleníti meg a munkafolyamathoz a Projektazonosítót, **Tekintse át a projekt számlajavaslatait**. |
| **Projektvezetés és könyvelés** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Nem a megfelelő készpénz-árengedmény dátumot használja a projektszámlák ajánlatainak közzétételekor. |
| **Projektvezetés és könyvelés** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | A Project Operations-ben lévő erőforrás-hozzárendelések eltávolítása és olvasása megduplázza a projekt előrejelzési tételeit a Finance szolgáltatásban. |
| **Projektvezetés és könyvelés** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | A Project Operations lehetőségben nem lehet projektbecsléseket létrehozni a Dataverse-ben anélkül, hogy a projekten szerződéssor ne lenne. |
| **Projektvezetés és könyvelés** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | A projektköltség-tranzakció pénzügyi dimenziója nincs szinkronizálva a kapcsolódó bizonylattal és a költségjelentés könyvelési felosztásával, amikor a költségeket közzéteszik az Egyenlegen. |
| **Projektvezetés és könyvelés** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | A **Számla állapota** szűrő a feladott projekttranzakciókhoz a rögzített árú projektek esetében nem működik. |
| **Projektvezetés és könyvelés** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A becsült érték sztornírozása nem működik a **Periódikus** szakaszban. |
| **Projektvezetés és könyvelés** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | A számlaajánlat-sorok rörölhetők a Project Operations szolgáltatásból, ha Dataverse lehetőséggel integrálta. |
| **Projektvezetés és könyvelés** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | A több szerződéssor funkció bekapcsolásának megakadályozása, ha nincs Dataverse-integráció. |
| **Projektvezetés és könyvelés** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Ha a számlázható számlázás egyenlő a nyereséggel és veszteséggel, akkor a számlázott bevétel nulla értékként szerepel a Becslések lapon. |
| **Projektvezetés és könyvelés** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | A számlakorrekciók nem működnek integrált környezetekben. |
| **Projektvezetés és könyvelés** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Folyamatban lévő munka értékesítési értékek közzétételekor a vállalatközi projektszámlázásban a rossz számlát választotta ki. |
| **Projektvezetés és könyvelés** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | A Project Operations lehetőség Dataverse becsült feladataiban lévő függőségek nem frissíthetők. |
| **Projektvezetés és könyvelés** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | A Project Operations integrációs naplóinak ismételt törlése a Finance lehetőségben adatvesztéshez vezet. |
| **Projektvezetés és könyvelés** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | A következő hibaüzenet jelenik meg a projekt számlajavaslat közzétételekor: „A tranzakció nincs egyensúlyban a jelentési pénznemmel, amikor a levont előleg számlát hozzáadják”. |
| **Projektvezetés és könyvelés** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Nem a megfelelő projektazonosító szerepel a levonásokon a Project Operations alapértelmezett projektszerződésének frissítése után. |
| **Projektvezetés és könyvelés** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | A becsült érték és a bevétel felismerése nem hajtható végre, ha a Project Operations engedélyezve van. |
| **Projektvezetés és könyvelés** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | A Project Operations lehetőségben a projekt szerződésből való eltávolítása nem állítja alaphelyzetbe a szerződés alapértelmezett projektjét. |
| **Projektvezetés és könyvelés** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | A Project Operations lehetőségben a vállalatközi számlán a nem megfelelő költségsorok jelennek meg a **Sor hozzáadása** listában. |
| **Utazás és költség** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | A költségsorokat nem lehet közzétenni, mert hiányzik az óra beállítása a szerződéssorból. |
| **Utazás és költség** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Ha kötelező a projekt/kategória ellenőrzése, a költségjelentésben nem láthatók a projekthez társított költségkategóriák. |
| **Utazás és költség** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | A készpénzfizetési előleg egyenleg nem frissül, ha egy költségjelentést soronként tesznek közzé. |
| **Utazás és költség** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | A **Fizetési információk frissítése** feladat nem sikerül, miután sztornírozzák a számla két vagy több fizetési tranzakcióját. |
| **Utazás és költség** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Probléma merült fel az utolsó napi étkezés csökkentésének számításával kapcsolatban a napidíjhoz tartozó költségkategória esetében. |
| **Utazás és költség** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Ha a felhasználó első kapcsolata az es-MX nyelvben volt, akkor az **Alkalmazottonkénti költségtípus** nem mutatja a tételekhez kapcsolódó költségeket. |
| **Utazás és költség** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Egy költségjelentési számla szállítói fizetése nem a megfelelő összegző számlát használja a kiegyenlítés közzétételéhez. |
| **Utazás és költség** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Ha egy költségjelentést közzétesznek a **Tranzakciók csoportosításának engedélyezése a halasztott fizetési számlán** és **Számlázási dátum javítása a feladáskor** funkciók engedélyezésével, akkor a könyvelési dátumokat úgy jelenítik meg, hogy azok nincsenek csoportosítva a **Könyvelési felosztás** táblában, és befolyásolja az áfarekordokat. |
| **Utazás és költség** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | A költség alkategóriák leképezése törlődik, ha a Felhasználás költségben jelölőnégyzet jelölése ki van törölve, majd újra be van jelölve. |
| **Utazás és költség** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Vállalatközi költségjelentés nem hozható létre, ha a projekt azonosítóját a fejléc szintjén adják hozzá. |
| **Utazás és költség** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Probléma merül fel a költségek kifizetésekor, ha a ráfordítás összege nagyobb, mint a készpénzelőleg összege. |
| **Utazás és költség** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | A vállalatközi költség jelentésen lévő **Projektazonosító** mező üres, ha a felhasználó szerepköre egy adott szervezethez van rendelve. |
| **Utazás és költség** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | A költségkategória zárolva van, amikor új költségsort ad hozzá. |
| **Utazás és költség** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | A már felosztott költségjelentési sorok tételesítési eredménye egy befejezetlen, közzé nem tett Kötelezettségek\Főkönyvi bizonylat lesz. A **TRVEXPTRANS.SOURCEDOCUMENTLINE** duplikációja miatt az Accounting Source Explorer is megszakad. |
| **Utazás és költség** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | A **TRVREQUISITIONLINE** táblához adott index miatt, amelyhez az ügyfél duplikált elemekkel rendelkezik, a frissítés során hiba lép fel. |
| **Utazás és költség** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | A Project Operations esetén nem lehet létrehozni vagy jóváhagyni a Dataverse-ben lévő vállalatközi feladatokkal kapcsolatos időt. |

## <a name="regulatory-updates"></a>Szabályozási frissítések

A Finance and Operations alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [szabályozási frissítések](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. Bejelentkezhet az LCS-be, és megtekintheti a tervezett szabályozási frissítéseket a Problémakereső eszközzel. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]