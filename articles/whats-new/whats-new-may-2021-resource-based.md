---
title: Újdonságok 2021. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez
description: Ez témakör a Project Operations 2021. májusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrásalapú/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723771"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2021. májusában – Project Operations erőforrásalapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations, 4.10.0.186-os verziójú Dynamics 365 Dataverse-környezetben
- Projektmenedzsment és -számvitel a Pénzügyi és Üzemeltetési alkalmazások környezetében 10.0.18-as verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- [Ütemezési módok](../project-management/scheduling-modes.md): A projektmenedzserek definiálják, hogy a projekteket a rögzített időtartam, rögzített munka vagy rögzített egységek ütemezési módjával kell-e kezelni.
- [Futásteljesítmény beállítása futásteljesítmény-szintek használatával](../expense/set-up-mileage.md): Futásteljesítmény-szintek frissítése az alkalmazotti költségjelentésekhez.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi lista a Project Operations 2021. májusi kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| --- | --- | --- |
| Projektfinanszírozási forrás (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Projektszerződés ügyfél fizetési feltételeinek szinkronizálása. |
| Projektszámla-ajánlat V2 (számlák) | 1.0.0.3 | A proforma számla fizetési feltételeinek szinkronizálása. |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Minőségi frissítések |
| Projektek V2 (msdyn\_projects) | 1.0.0.2 | Minőségi frissítések |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance and Operations alkalmazások megoldásverziójának frissítésekor. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon láthatja. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabta az egyedi táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a térkép elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2227635 | Az **Egységcsoport** és az **Egység** mezők értékei az alapértelmezett érték a terméktől az **Anyagbecslések** rácsban. |
| Számlázás és árképzés | 2234127 | A **Feladatazonosító** mező mostantól megfelelően integrálva van a Dataverse projekt tényadatokkal, amikor egy szállító számláját közzéteszik. |
| Számlázás és árképzés | 2235564 | A naplósor mentésével biztosíthatja, hogy a naplósorban megjelenített pénznem a mentést követően a sorhoz megfelelő alapértelmezett pénznemnek feleljen meg. |
| Számlázás és árképzés | 2246671 | Ha a tranzakció számlázás közben nem számítható fel, akkor a rendszer visszavonja az eredeti számlázatlan értékesítési rekordot, és új, nem számlázható értékesítési rekordot hoz létre. |
| Számlázás és árképzés | 2264042 | Az érvényes számlakorrekciót nem szabad letiltani, ha egy számlakorrekció részletei nem érvényesek a környezetben. |
| Számlázás és árképzés | 2146367 | A projekt számlafejlécének kettős írású leképezése ki lett bővítve, hogy a fizetési feltételeket tartalmazza. |
|   Lehetőségkezelés | 2086888 | Ne vegyen fel olyan szerepköröket és kategóriákat, amelyek inaktiválva vannak, mielőtt az ajánlatot számlázható szerepkörökbe és az újonnan másolt ajánlatok kategóriáiba másolja. |
|   Lehetőségkezelés | 2234376 | A csak olvasható mezők az **Anyagbecslések** rácsban ki vannak szürkítve. |
|   Lehetőségkezelés | 2238337 | A kapcsolattartón alapuló ajánlatok akkor is menthetők, ha nincsenek projektárlistához társítva. |
|   Lehetőségkezelés | 2239810 | Ha az ajánlatot elvesztettként lezárja, a kapcsolódó projekt is bezárul, és törli a foglalásokat. |
| Projekttervezés és nyomon követés | 2099559 | A rendszer állapotára további ellenőrzések lettek hozzáadva a **Projektfeladatok** rács megnyitása előtt. |
| Projekttervezés és nyomon követés | 2178987 | Javítottunk egy átmeneti hibát, amely a **Projekt oldal** **Következő fázisának** kiválasztásakor fordul elő. |
| Erőforráskezelés | 2224817 | Az alapértelmezés szerint a foglalások megfelelő állapotra való kibővítését teszi lehetővé ez a funkció. |
| Időbejegyzés | 2202476 | Az **Időbevitel** oldal mostantól reaktív rácsvezérlőt használ, és kijavít az olyan problémákat, mint a rács elcsúszása. |
| Időbejegyzés | 2223377 | Az időbevitel el van rejtve a **Foglalható erőforrás** oldal **Kapcsolódó** szakaszában, hogy elkerülhető legyen a használhatósággal kapcsolatos zavar. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és számvitel Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | A Project Operations erőforrás-alapú forgatókönyvek esetén: Integrációs hiba miatt nem tud egy árajánlatot megnyertre átállítani. |
| Projektvezetés és könyvelés | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | A Project Operations: Egy hibaüzenet jelenik meg, amikor egymást átfedő szerződéssorok és tranzakciótípusok ellenőrzése miatt próbál szerződéssort társítani egy Projektazonosítóhoz. |
| Projektvezetés és könyvelés | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | A **ProjCDSProjectContractEntity** beállítja a finanszírozási forrás számlacímét egy másik ügyfélből. |
| Utazás és költség | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | A futásteljesítmény beállításával kapcsolatban könyvelési hiba merülhet fel. |
| Utazás és költség | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | A **Személyek szerinti osztás** funkció a devizás költségtranzakciók esetében nem működik. |
| Utazás és költség | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | A költségkategória legördülő menüje helytelen kategóriákat mutat, függetlenül attól, hogy a meghatalmazottak erőforrásként van-e beállítva. |
| Utazás és költség | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | **Erőforrás/kategória érvényesítési** hiba miatt nem menthet vállalatközi költségjelentést. |
| Utazás és költség | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | A költségjelentés feladásában a rossz futásteljesítmény-arány kiszámítása osztott vonalakat. |
| Utazás és költség | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Nem tehet közzé vállalatközi költségjelentést, ha az forgalmi adót tartalmazza, és a fizetési mód eltolási számlatípusa a **Munkavállaló**. |
| Utazás és költség | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Visszaállítottuk a **TrvRequisitionLine** adatentitást és a hozzá társított egyedi indexet. |
| Utazás és költség | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | A költségjelentés támogatja a forrásdokumentum-sorok létrehozását és frissítését. |
| Utazás és költség | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Egy helytelen alfőkönyvi napló jelenik meg vállalatközi forgatókönyv esetén, ha az áfa közzé van téve a cél jogi entitásnak. |
| Utazás és költség | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: A költségbecslések nem törlődnek a Finance-ből, amikor törlik őket a Dataverse-ből. |
| Utazás és költség | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ha egy költségkategória nem projektkategória, a **Költségek** lapon kiválasztott pénzügyi dimenziók nem lesznek átmásolva a költségjelentésbe. |
