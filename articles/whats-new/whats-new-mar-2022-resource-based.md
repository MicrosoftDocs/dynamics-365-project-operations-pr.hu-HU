---
title: Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2022. márciusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910909"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.30.0.99
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.25-ös verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

A napidíjak mostantól támogatottak az új és újragondolt modern költség munkaterületen. Azok a vállalatok, amelyek napidíjat használnak, lehetővé tehetik ezt a funkciót, hogy a felhasználók számára egyszerű módot biztosítsanak a benyújtásra és a napidíj-költségek megtérítésére. További információ: [Napidíjköltségek](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi lista azokat a kettős írású térképeket mutatja be, amelyeket módosítottak vagy hozzáadtak a Project Operations 2022. márciusi kiadásához.

| **Entitásleképezés** | **Frissített verzió** | **Hozzászólások** |
| --- | --- | --- |
| Project Operations integrációs projekt szállítói számla export entitás msdyn\_ projectvendorinvoicelines | 1.0.0.3 | A leképezések frissítve vannak, hogy igazodjanak a szállítói számlasor-entitáshoz Dataverse. <br>Ne aktiválja a leképezési verziót 1.0.0.4. A következő havi frissítésben készen áll a használatra a Finance environment 10.0.26-os verziójával együtt. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Idő és költség | 2388011 | Elutasító megjegyzések megjelenítése az időbejelentőknek a tömeges jóváhagyás során. |
| Projekttervezés és nyomon követés | 2495294 | A projekt részletei nem szerkeszthetők a **Tevékenység részletei** lapon. |
| Számlázás és árképzés | 2499605 | Az árajánlat mérföldkövekből létrehozott szerződéses mérföldkövek helytelenül írásvédettként vannak megjelölve. |
| Projekttervezés és nyomon követés | 2506050 | A műveletkészlet egy órán át függőben marad, ha nincs mentendő módosítás. A készletet ezután tévesen Sikertelenként **jelölik** meg, míg azonnal be kell fejezni. |
| Számlázás és árképzés | 2507401 | Az alapértelmezett szerződéses egységek helytelenül vannak megadva a projektekben a helytelen gyorsítótárazás miatt. |
| Számlázás és árképzés | 2541660 | **Az értékesítési rendelések létrehozásának ellenőrzése** kettős írásban csak projektalapú rendelésekre vonatkozhat. |
| Számlázás és árképzés | 2552745 | Az adó nem oszlik meg azon ügyfelek között, akik megosztott számlázási szabályokat állítottak be. |
| Számlázás és árképzés | 2558859 | Továbbfejlesztett hibaüzenetek a díjszabási dimenziók beállításakor. |
| Számlázás és árképzés | 2558933 | **A Project Estimates-ből** való importálás sikertelen lesz, ha **az msdyn\_ projektet** tarifadimenzióként adja hozzá. |
| Számlázás és árképzés | 2559101 | A projektparaméterek törlése nincs letiltva, és problémákat okoz. |
|   Lehetőségkezelés | 2570390 | A kettős írású beépülő modul arra kényszeríti a fióktípust az árajánlatokra, megrendelésekre és lehetőségekre, hogy Ügyfél **legyen**, még akkor is, ha az adott fióktípus nem megfelelő. |
| Számlázás és árképzés | 2586097 | A felosztott számlázott költség tényleges adatai nem lesznek visszafordítva, amikor egy projektet eltávolítanak egy projektszerződés-sorból. |
| Számlázás és árképzés | 2589619 | A beírt anyagra kivetett adót a számlázatlan értékesítési tényleges adatokra és a számlára terjesztik. |
|   Lehetőségkezelés | 2594015 | Az árajánlat nem zárható le a megnyert módon azoknál az ügyfeleknél, akik net60 **fizetési feltételekkel rendelkeznek**. |
| Projekttervezés és nyomon követés | 2595841 | A Webes Projectben a felhasználók hibaüzenetet kapnak egy hiányzó **msdyn\_ actualstart** értékről, amikor új erőforrás-kérést hoznak létre. |
| Idő és költség | 2602511 | Az **Időbejegyzések Elutasítva mezője** a Rendszer **jelenik meg** a megnevezett felhasználó helyett elutasítóként. |
| Idő és költség | 2602528 | A projektjóváhagyók jóváhagyhatják az olyan projektek idejét, amelyek nem szerepelnek jóváhagyóként. |
| Számlázás és árképzés | 2608550 | A helyesbítő számla akkor is visszaigazolható, ha az eredeti nem változik. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | A Kategóriaazonosító **mező megengedett hosszában eltérés van a Finance és a** Project Operations között. |
| Projektvezetés és könyvelés | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | A rögzített árú projektek nem szüntethetők meg, ha a **Számlaszámlázás** mező értéke **Nyereség és veszteség**, és a **Teljesített százalék** elvét használja. |
| Projektvezetés és könyvelés | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Helytelen alapértelmezett áfacsoport kerül beírásra a projekt beállításából a Project Operations integrációs napló költségsoraiba. |
| Projektvezetés és könyvelés | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | A projektszámla-javaslat fejlécdimenziói nem szerkeszthetők a Project Operations integrált üzemelő példányaiban. |
| Projektvezetés és könyvelés | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | A vállalatközi szállítói számlákat nem szabad integrálni a következővel Dataverse: . |
| Projektvezetés és könyvelés | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Eltérés van az ügyfélegyenleg pénznemében és a jelentési pénznemben. |
| Projektvezetés és könyvelés | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | A projektszámlát akkor is feladhatja, ha a vevő az összes számla esetében várakozik. |
| Projektvezetés és könyvelés | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Az **Összes sor** törlése gomb hiányzik azokból a **projektszámla-javaslatokból, amelyek fejléc** és **sorok** nézettel rendelkeznek. |
| Projektvezetés és könyvelés | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Szállítói számla feladásakor a következő hibaüzenet történik: "A számla könyvelési dátumának ugyanabban a számviteli évben kell lennie, mint a kapcsolódó megvásárolt rendelésnek. Futtassa a beszerzési rendelés év végi folyamatát, vagy módosítsa a dátumot az aktuális számviteli évre." |
| Utazás és költség | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | A projekt lekötött költsége nem szabadul fel az utazási igénylés lekötött költségének felszabadítása után. |
| Utazás és költség | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | A következő hibaüzenet jelenik meg a költségjelentés elküldésekor: "Veremkövetés: A vállalat nem létezik." |
| Utazás és költség | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Az alapértelmezett **projektazonosító** nem kerül be a költségjelentésekbe, ha a Tevékenység megkövetelése naplóhoz **paraméter** be van jelölve a projektben. |
| Utazás és költség | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | A **Költségek** feladása gomb nem működik megfelelően a Project Operationsben erőforrás-/nem készletezett forgatókönyvek esetén. |
| Utazás és költség | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Probléma van a mérföldenkénti **árral** az utasokat tartalmazó kilométerköltség-jelentéshez. |
| Utazás és költség | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Az alkalmazottak költséglehetőségi díjai nincsenek megfelelően összegezve, ha két különböző járműtípust használnak a **kilométerdíj-szintek** költségkategóriájában. |
| Utazás és költség | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Az utazási igénylési sorban lévő **Projekt** mező keresése nem a megfelelő projektlistát adja vissza. |
| Utazás és költség | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **A felülvizsgálat** alatt álló futásteljesítmény figyelmeztetést jelenít meg a költségjelentéseken. |
| Utazás és költség | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | A nyugta optikai karakterfelismerő (OCR) szolgáltatás nem működik, mert probléma van a költség OCR szolgáltatás URL-címével. |
| Utazás és költség | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ha az **Ismétlődő költségek gyors** tételének képessége funkció engedélyezve van, a költségjelentések tételes soraiban lévő összegek minden alkalommal változnak, amikor a **Tételes** oldal megnyílik. |
| Utazás és költség | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Nem törölhet költségjelentést, ha az ideiglenes listának egynél több jóváhagyója van. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiról szóló cikk azokat a funkciókat ismerteti, amelyek eltávolításra vagy elavultak Dynamics 365 Project Operations.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nincsenek aktív fejlesztés alatt, és előfordulhat, hogy egy későbbi frissítés során el lesznek távolítva.

Az elalvasztási bejelentés 12 hónappal azelőtt jelenik meg a [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiban, hogy bármely funkciót eltávolítana a termékből.

Az olyan módosítások megszakítása esetén, amelyek csak a fordítási időt érintik, de binárisan kompatibilisek a tesztkörnyezettel és az éles környezetekkel, az elavulási idő kevesebb, mint 12 hónap. Ezek a módosítások általában funkcionális frissítések, amelyeket a fordítón kell elvégezni.
