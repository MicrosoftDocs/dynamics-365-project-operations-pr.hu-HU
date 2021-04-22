---
title: Újdonságok 2021. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez témakör a Project Operations 2021 áprilisi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrásalapú/nem készletalapú forgatókönyvekhez.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867996"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2021. áprilisban – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations a Dataverse-környezet 4.9.0.221 verzióján
- Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.17-es verziójában

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- Nem készletezett anyagok projektekhez. A legfontosabb képességek a következők:
  - Nem készletezett anyagok becslése és árképzése a projekt értékesítési ciklusa alatt. További információért lásd a [Költség- és értékesítési árak beállítása a katalógustermékekhez – Lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md) részt.
  - A nem készletezett anyagok használatának követése a projekt teljesítése során. További információért lásd az [Anyaghasználat rögzítése projekteknél és projektfeladatoknál](../material/material-usage-log.md) részt.
  - A felhasznált nem készletezett anyagköltségek számlázása. További információért lásd a [Számlázási elmaradás kezelése](../proforma-invoicing/manage-billing-backlog.md) részt.
- Feladatalapú számlázás: Lehetővé tette a projektfeladatok projektszerződés-sorokkal való társítását, ezáltal ugyanaz a számlázási módszer, számlagyakoriság és vevők vonatkoznak rá, mint a szerződéssoron szereplőkre. Ez a társítás biztosítja a pontos számlázást, könyvelést, bevételbecslést és felismerést, hogy a projektfeladatokon ennek a beállításnak megfelelően működjön.
- A Dynamics 365 Dataverse-ben lévő új API-k lehetővé teszik az **Ütemezési entitásokkal** végzett műveletek létrehozását, frissítését és törlését. További információt az [Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations a Dynamics 365 Dataverse-ben

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2124532 | A **Számla helyesbítése** gomb akkor jelenik meg egy proforma számlán, ha a foglalóösszeg vagy az alkalmazott foglalóösszeg jelen van az eredeti számlán. A gomb csak a Finance 10.0.19-es vagy újabb verzióján jelenik meg. |
| Számlázás és árképzés | 2224568 | Hozzáadott logika a számlameghívó beépülő modult megerősítő testreszabások engedélyezéséhez. |
| Számlázás és árképzés | 2101098 | Az alapértelmezett mezők logikáját proforma számlára javította: a **Számlázási cím**, a **Számlázási név** és a **Fizetési feltételek** mostantól alapértelmezetten a megfelelő projektszerződés ügyfélrekordból kerülnek beírásra. |
| Számlázás és árképzés | 2021413 | Frissítette a **Tényleges költség** és **Értékesítés** mezőket a **Feladat** entitáson, hogy tartalmazza a feladatokon a számlázatlan és számlázott kiadások értékesítési értékeit. |
| Számlázás és árképzés | 2182110 | Projektszerződés másolásakor a szerződéssor azonosítója újra lesz generálva a célprojekt-szerződésben, hogy biztosítsák egyediségét. |
| Lehetőségkezelés | 2186741 | Hozzáadott ellenőrzések annak biztosítására, hogy az **Eredet** mező és a **Tranzakciótípus** ne legyen frissíthető a meglévő árajánlatsor részleteivel kapcsolatban. |
| Lehetőségkezelés | 2191353 | Mérföldköveket nem szabad idő- és anyagszerződési sorokban létrehozni. |
| Lehetőségkezelés | 2216956 | Kijavítottuk az **Árak frissítésével** kapcsolatos problémákat. |
| Tervezés és nyomon követés | 2182979 | A projektmásolási funkció tovább lett fejlesztve annak biztosítására, hogy a költségbecslési sorok át legyenek másolva az eredeti projektből. |
| Tervezés és nyomon követés | 2184144 | A projektmásolási funkció tovább lett fejlesztve annak biztosítására, hogy az erőforráspozíció neve át legyen másolva az eredeti projektből. |
| Tervezés és nyomon követés | 2184799 | Projektmásolás: Szigorított vezérlés annak biztosítására, hogy a becsült kezdési dátum ne legyen módosítható a másolás közben. |
| Tervezés és nyomon követés | 2185134 | Projektmásolás: A célprojekt becsült kezdési dátuma a mai dátumra van állítva. |
| Tervezés és nyomon követés | 2196373 | Projektmásolás: Győződjön meg arról, hogy a projektmenedzser és a csoporttag rekordjai nem ismétlődnek meg a projektcsoportban. |
| Tervezés és nyomon követés | 2211833 | Projektmásolás: Az erőforrás-hozzárendelések a forrásprojekt-feladatból a célprojektbe másolhatók. |
| Tervezés és nyomon követés | 2186541 | A **Becslések** rácsban, az erőforrás szerinti csoportosításkor felmerült problémák kijavítva. |
| Tervezés és nyomon követés | 2166906 | A feladat tranzakciókategóriáit át kell másolni az **Erőforrás-hozzárendelés** entitásba. |
| Erőforráskezelés | 2125362 | Az általános csoporttag óraalapú felosztási módszerrel történő létrehozással kapcsolatos problémák kijavítva. |
| Idő és költség | 2113603 | Az attribútumok **Időbejegyzés** lapról való eltávolításával, a testreszabással kapcsolatos probléma kijavítva. A rendszer most ellenőrzi, hogy az attribútum létezik-e a lapon, mielőtt parancsfájl használatával hozzájuk férne. |
| Idő és költség | 2204377 | A másolt munkaidő-nyilvántartásoknak automatikusan meg kell jelenniük, amikor az időbejegyzés során a **Hét másolása** lehetőséget választja. |
| Idő és költség | 2209059 | Az **Állapot** mező szerkeszthető a Dynamics 365 Field Service időbejegyzésekhez. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance szolgáltatásban

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Projektvezetés és könyvelés | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A fordított becslés megszüntetése nem működik **Időszakos** beállításban.  |
| Projektvezetés és könyvelés | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | A **Könyveléshelyesbítés** funkció problémát hoz létre azoknál a főkönyvi számláknál, amelyeknél a **Nincs engedélyezve manuális bevitel** van kiválasztva. |
| Projektvezetés és könyvelés | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Hozzáadott üzleti logika a javítási számlák feldolgozásához, beleértve a foglalóösszeget vagy az alkalmazott foglalóösszeget. |
| Projektvezetés és könyvelés | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Folyamatban lévő munka értékesítési érték feladása a vállalatközi projektszámlázásban egy nem várt számlát választ ki. |
| Projektvezetés és könyvelés | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Ha a Project Operationsben foglalókkal dolgozik, az előlegek számlázása után a szerződés alapértelmezett projektjének módosítása problémákat okoz a bejövő levonásoknál. |
| Projektvezetés és könyvelés | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | A Project Operations szolgáltatásban a projekt szerződésből való eltávolításához szükség esetén alaphelyzetbe kell állítani a szerződés alapértelmezett projektjét. |
| Projektvezetés és könyvelés | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | A Project Operations szolgáltatásban a **Sor hozzáadása** elemnél helytelen költségsorok jelennek meg a vállalatközi számlán. |
| Projektvezetés és könyvelés | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | A Project Operations szolgáltatásban a **Vásárlási megállapodás** lap nem látható azoknál a pénzügyi jogi személyeknél, amelyek integrálva vannak a Project Operations szolgáltatással. |
| Projektvezetés és könyvelés | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | A Dataverse integrációs hibája miatt nem konvertálhat árajánlatot elnyertre a Project Operations szolgáltatásban. |
| Projektvezetés és könyvelés | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | A **ProjCDSProjectContractEntity** beállíthatja a finanszírozási forrás számlacímét egy másik ügyfélből.  |
| Projektvezetés és könyvelés | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | A Project Operations szolgáltatásban a tranzakció közzétételi számlájának létrehozásakor nem lesz kiválasztva dimenzió. |
| Utazás és költség | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | A készpénzelőleg egyenlege nem frissül a költségjelentéshez, ha azt sorról sorra jóváhagyják és könyvelik. |
| Utazás és költség | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | A tételes vállalatközi költségjelentések adóit a program nem számítja ki megfelelően. |
| Utazás és költség | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | A projektekhez kapcsolódó további mezők az újragondolt **Vállalatközi költségjelentések** lapon jelennek meg. |
| Utazás és költség | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Helytelen hibaüzenet jelenik meg a költségjelentések fejlécnyugtákon. |
| Utazás és költség | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | A költségjelentés helytelenül van feladva vállalatközi forgatókönyv esetén, ha az áfa közzé van téve a cél jogi entitásnak. |
| Utazás és költség | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | A jelentésküldési dátumok nincsenek kinyomtatva a jóváhagyott költségjelentéseken. |
| Utazás és költség | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | A **Jóváhagyott dátum** és az **Elutasított dátum** mezői nincsenek megadva a költség jóváhagyása után. |
| Utazás és költség | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Az egyik dolgozó számára létrehozott utazási igénylés egy másik dolgozó költségjelentésére használható. |
| Utazás és költség | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | A költségkategóriák zárolva vannak az új költségsor hozzáadásakor. |
| Utazás és költség | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | A már felosztott költségjelentési sorok tételesítése a Kötelezettségek\Általános főkönyvi bizonylat hiányos könyvelését eredményezi, és megszakítja a Könyvelési erőforráskezelőt a **TRVEXPTRANS.SOURCEDOCUMENTLINE** megduplázódása miatt. |
| Utazás és költség | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Az utazási kérelem szabályzat nem a várt módon működik. |
| Utazás és költség | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | A szállítói számla neve nem jelenik meg a költségjelentések közzétett projekttranzakcióin. |
| Utazás és költség | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | A Project Operations szolgáltatásban nem hagyhat jóvá időt egy vállalatközi projekt feladatával. |
| Utazás és költség | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | A készpénzelőleg-visszatérítési kategória nem frissíti a készpénzelőleg-egyenlegeket, ha azok közzé vannak téve. |
| Utazás és költség | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Az értékesítési ár kiszámítása helytelenül történik az olyan költségjelentéseken, amelyeket külföldi pénznemben hoztak létre importált hitelkártya-tranzakciókkal, illetve amelyek hozzá vannak társítva egy projekthez. |
| Utazás és költség | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Visszaállítottuk a **TrvRequisitionLine** adatentitást és a hozzá tartozó egyedi indexet. |
| Utazás és költség | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Eszközt adtunk hozzá a **SOURCEDOCUMENTLINE** generálásához. |
| Utazás és költség | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | A helytelen alfőkönyvi napló jelenik meg vállalatközi forgatókönyv esetén, ha az áfa közzé van téve a cél jogi entitásnak. |
| Utazás és költség | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | A Project Operations szolgáltatásban a költségbecslések nem törlődnek a Finance-ből, amikor törlik őket a Dataverse-ből. |
| Utazás és költség | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ha egy költségkategória nem projektkategória, a **Költség** lapon kiválasztott pénzügyi dimenziók nem lesznek átmásolva a költségjelentésbe. |
