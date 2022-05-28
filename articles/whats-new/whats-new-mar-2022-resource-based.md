---
title: Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör a Project Operations erőforrás-/nem raktározott forgatókönyvek projektműveleteinek 2022. márciusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600745"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2022. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Projektműveletek környezeti Dataverse verzióban 4.30.0.99
- Projektmenedzsment és -számvitel Dynamics 365 Finance környezetben 10.0.25-ös verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

A napidíjakat most az új és újragondolt modern költség-munkaterület támogatja. Azok a vállalatok, amelyek napidíjat használnak, lehetővé tehetik ezt a funkciót, hogy a felhasználók egyszerűen benyújthassák és megtéríthessék napidíjaikat. További információ: [Per diem költségek](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi lista a Project Operations 2022. márciusi kiadásában módosított vagy hozzáadott kettős írási térképeket mutatja be.

| **Entitásleképezés** | **Frissített verzió** | **Hozzászólások** |
| --- | --- | --- |
| Projektműveletek integráció projekt szállítói számlasor exportálási entitás msdyn\_ projectvendorinvoicelines | 1.0.0.3 | A hozzárendelések frissültek, hogy igazodjanak a szállítói számlasor entitásához a alkalmazásban Dataverse. <br>Ne aktiválja a hozzárendelési verzió 1.0.0.4. A következő havi frissítésben a Pénzügyi környezet 10.0.26-os verziójával együtt használható lesz. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Pénzügy megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémát tapasztal, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblázatoszlopok probléma a térképeken [című részében található utasításokat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Idő és költség | 2388011 | Elutasító megjegyzések megjelenítése az időbejegyzés-beküldők számára a tömeges jóváhagyás során. |
| Projekttervezés és nyomon követés | 2495294 | A projekt részletei nem szerkeszthetők a **Tevékenység részletei** lapon. |
| Számlázás és árképzés | 2499605 | Az ajánlati mérföldkövekből létrehozott szerződési mérföldkövek helytelenül írásvédettként vannak megjelölve. |
| Projekttervezés és nyomon követés | 2506050 | A műveletkészlet egy órán át függőben marad, ha nincs mentendő módosítás. A készlet ezután hamisan sikertelenként **van** megjelölve, míg azonnal be kell fejezni. |
| Számlázás és árképzés | 2507401 | Az alapértelmezett szerződéskötési egységek helytelenül vannak megadva a projektekben a helytelen gyorsítótárazás miatt. |
| Számlázás és árképzés | 2541660 | **Az értékesítési rendelés létrehozásának ellenőrzése** kettős írásban csak projektalapú rendelések esetén történhet meg. |
| Számlázás és árképzés | 2552745 | Az adó nem oszlik meg a megosztott számlázási szabályokat létrehozó ügyfelek között. |
| Számlázás és árképzés | 2558859 | Továbbfejlesztett hibaüzenetek az árképzési dimenziók beállításakor. |
| Számlázás és árképzés | 2558933 | **A Projektbecslésekből** történő importálás sikertelen, ha **az msdyn\_ projekt** árazási dimenzióként van hozzáadva. |
| Számlázás és árképzés | 2559101 | A projektparaméterek törlése nincs blokkolva, és problémákat okoz. |
|   Lehetőségkezelés | 2570390 | A kettős írás beépülő modul arra kényszeríti a fióktípust az ajánlatokra, megrendelésekre és lehetőségekre, hogy ügyfél **legyen**, még akkor is, ha az adott fióktípus nem megfelelő. |
| Számlázás és árképzés | 2586097 | A felosztott számlázott költség tényleges adatai nem sztornírozódnak, ha egy projektet eltávolítanak a projektszerződési sorból. |
| Számlázás és árképzés | 2589619 | A beírt anyag adója a nem számlázott értékesítési tényleges adatokra és a számlára terjed ki. |
|   Lehetőségkezelés | 2594015 | Az ajánlat nem zárható le nyertesként a Net60 **fizetési feltételekkel rendelkező** ügyfelek számára. |
| Projekttervezés és nyomon követés | 2595841 | A Project for the Web programban a felhasználók hibaüzenetet kapnak egy hiányzó **msdyn\_ actualstartról**, amikor új erőforrás-kérelmet hoznak létre. |
| Idő és költség | 2602511 | Az **Időbejegyzések Elutasítva mezőben** a Rendszer **jelenik meg**, nem pedig egy megnevezett felhasználó, mint elutasító. |
| Idő és költség | 2602528 | A projekt jóváhagyó jóváhagyhatja az időt azokon a projekteken, amelyekben nem szerepelnek jóváhagyóként. |
| Számlázás és árképzés | 2608550 | A helyesbítő számla akkor is megerősíthető, ha az eredetiben nincs változás. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | A Kategóriaazonosító **mező megengedett hosszában eltérés van a Pénzügy és a** Projektműveletek között. |
| Projektvezetés és könyvelés | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | A rögzített árú projektek nem szüntethetők meg, ha a **Számlaszámlázás** mező **értéke Nyereség és veszteség**, és a **Kitöltött százalék** elvet használja. |
| Projektvezetés és könyvelés | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | A Projektműveletek integrációs napló költségsoraiban helytelen alapértelmezett áfacsoportot a program helytelen alapértelmezett áfacsoportot ír be. |
| Projektvezetés és könyvelés | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | A projektszámla-javaslat fejdimenziói nem szerkeszthetők integrált üzembe helyezésben a Project Operations szolgáltatással. |
| Projektvezetés és könyvelés | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | A vállalatközi szállítói számlákat nem szabad integrálni a rendszerbe Dataverse. |
| Projektvezetés és könyvelés | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Eltérés van a vevői egyenlegek pénznemében és a jelentés pénznemében. |
| Projektvezetés és könyvelés | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektszámlát akkor is könyvelhet, ha a vevő az összes számlához várakozik. |
| Projektvezetés és könyvelés | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Az **Összes sor** törlése gomb hiányzik a Fejléc **és** sorok **nézettel rendelkező** projektszámla-javaslatokból. |
| Projektvezetés és könyvelés | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Szállítói számla könyvelésekor a következő hiba lép fel: "A számla könyvelési dátumának ugyanabban a könyvelési évben kell lennie, mint a kapcsolódó beszerzési rendelésnek. Futtassa a beszerzési rendelés év végi folyamatát, vagy módosítsa a dátumot az aktuális számviteli évre." |
| Utazás és költség | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | A projekt lekötött költsége nem jelenik meg az utazási igénylés véglegesített költségének felszabadítása után. |
| Utazás és költség | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Költségjelentés benyújtásakor a következő hiba lép fel: "Veremkövetés: A vállalat nem létezik." |
| Utazás és költség | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Ha a projektben be van jelölve a **naplóparaméterhez** szükséges tevékenység megkövetelése jelölőnégyzet, a program nem adja meg az alapértelmezett **projektazonosítót** a költségjelentésekben. |
| Utazás és költség | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | A **Költségek** könyvelése gomb nem működik megfelelően a Projektműveletek programban erőforrás-/nem raktározott forgatókönyvek esetén. |
| Utazás és költség | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Probléma van a mérföldenkénti **díjjal** egy kilométerenkénti költségjelentés esetében, amely magában foglalja az utasokat. |
| Utazás és költség | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Az alkalmazottak költségmunkrózis-arányai nincsenek megfelelően összesítve, ha két különböző járműtípust használnak a **Futásteljesítménydíj-szintek** költségkategóriájában. |
| Utazás és költség | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Az utazási igénylési sorban a **Projekt** mező keresése nem adja vissza a projektek megfelelő listáját. |
| Utazás és költség | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **A vizsgált** futásteljesítmény figyelmeztetést mutat a költségjelentésekre vonatkozóan. |
| Utazás és költség | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | A nyugta optikai karakterfelismerési (OCR) szolgáltatás nem működik a költség OCR szolgáltatás URL-címével kapcsolatos probléma miatt. |
| Utazás és költség | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ha az **ismétlődő költségek gyors** részletezésének képessége funkció engedélyezve van, a költségjelentések cikkezési soraiban szereplő összegek a Cikkméret **lap megnyitásakor minden alkalommal** változnak. |
| Utazás és költség | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Költségjelentés nem törölhető, ha az időközi listán egynél több jóváhagyó van. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations](removed-depreciated-features-project.md) témakör eltávolított vagy elavult szolgáltatásai a következőhöz lettek eltávolított vagy elavult Dynamics 365 Project Operations szolgáltatásokat írják le:

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkció nincs aktív fejlesztés alatt, és egy későbbi frissítésben eltávolíthatók.

Az elavulás bejelentése megjelenik a [Project Operations](removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiban témakör 12 hónappal azelőtt, hogy bármely funkciót eltávolítanának a termékből.

Olyan módosítások megszakítása esetén, amelyek csak a fordítási időt befolyásolják, de binárisan kompatibilisek a sandbox és az éles környezetekkel, az elavulási idő kevesebb, mint 12 hónap lesz. Ezek a módosítások általában funkcionális frissítések, amelyeket a fordítón kell elvégezni.
