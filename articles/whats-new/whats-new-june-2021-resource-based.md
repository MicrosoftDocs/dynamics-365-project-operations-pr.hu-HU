---
title: Újdonságok 2021. júniusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
description: Ez a cikk a Project Operations 2021. júniusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028249"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok 2021. júniusában – Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.11.0.156 vagy 4.11.0.164 verziójú Dynamics 365 Dataverse-környezetben.
- Projektmenedzsment és könyvelés a pénzügyi és üzemeltetési alkalmazások környezetében 10.0.19-es verzió.

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- Lehetőség a [Projektszámla-javaslat sorok korrekciós esetekre](../invoicing/correct-project-invoice-proposals.md).
- Az elemi költségsorok az alkategóriák neveit tükrözik a költségjelentésben [Újragondolt és új szolgáltatások a költségjelentésekben](../expense/expense-reports-reimagined.md#new-features).
- Új költség létrehozásakor a fizetési mód az új költségmezőn elérhető.
- A projekt ütemezési API-k általános elérhetősége. Ez az új funkció lehetővé teszi, hogy az ügyfelek programon keresztül létrehozzanak, frissítsenek vagy töröljenek műveleteket a projektfeladatokkal, erőforrás-hozzárendelésekkel, feladat függőségekkel és projektcsoporttag-bejegyzésekkel. További tudnivalók: [A Projektütemezési API-k használata műveletek végrehajtásához az entitások ütemezésével](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írású leképezéseihez. 

A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations-megoldás Dataverse, valamint a pénzügyi és üzemeltetési alkalmazások megoldásverziójának frissítése során. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verziója **Kettős írás** oldalon látható a **Verzió** oszlopban. Aktiválhatja a leképzés új verzióját a **Táblaleképezés verziója** lehetőség kiválasztásával, majd a legújabb verzió kiválasztásával, majd a kiválasztott verzió mentésével. Ha testreszabta az egyedi táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha probléma merül fel a leképezés indítása során, kövesse a [Hiányzó táblaoszlopokkal kapcsolatos probléma a leképezésekben](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részt a Kettős írás hibaelhárítási útmutatójában.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2281417 | Javítottuk a számla ütemezése során az automatikus számlakészítési művelet meghiúsulásával kapcsolatos problémát. |
| Számlázás és árképzés | 2287835 | Továbbfejlesztett számla-visszaigazolási teljesítmény. |
| Lehetőségkezelés | 2222555 | Az anyagbecslések felszámíthatóságát helyesen be kell másolni az árajánlatsorok részleteibe az **Importálás projektbecslésből** segítségével. |
| Lehetőségkezelés | 2223427 | Mostantól engedélyezve vannak a testreszabások a **GenerateRetainersFromRetainerScheduleOptions** művelethez. |
| Lehetőségkezelés | 2277528 | Több ügyfélből álló projektszerződéssorok számlázási mérföldkövekérték-számításának javítása. |
| Projekttervezés és nyomon követés | 2226110 | Kijavítottuk a **Követelmény létrehozása** funkció időszakos problémáját a **Projektcsapat** rácsban. |
| Projekttervezés és nyomon követés | 2208109 | A felhasználók nem hozhatnak létre projekteket egy pénznemben, ha kapcsolódó feladatok másik pénznemben vannak. |
| Projekttervezés és nyomon követés | 2258228 | Frissítve lettek azok a mezők, amelyek módosíthatók az **Ütemezés** entitásokkal az Ütemezés API-jal. |
| Projekttervezés és nyomon követés | 2293989 | A megfelelő nyelvi és területi beállításokat kell átadni a **Projektfeladatok** rács számára. |
| Erőforráskezelés | 2220493 | A **Feladat** rácson javítva lett a felhasználói élmény, amikor egy erőforrás-kérést gyorsan befejezettként jelölnek meg. |
| Erőforráskezelés | 2330496 | Javítva lett az **Ütemezési tábla** betöltési problémája. (A minőség frissítés a 4.11.0.164 verzióban érhető el) |
| Idő és költség | 2194431 | Az **Időbejegyzés** rácsnak tiszteletben kell tartania a hét kezdetét a **Rendszerbeállítások** között megadottak szerint. |
| Idő és költség | 2277311 | Miután törölte az értéket egy cellában az **Időbejegyzés** rácsban, a kurzor a rácsban marad. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Projektvezetés és könyvelés | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Az **Űrlapmegjegyzések** és az **Űrlapbeállítás** nem látható a **Projektvezetési beállítások** alatt a Finance jogi személyeinél, ha integrálva vannak a Project Operations alkalmazással. |
| Projektvezetés és könyvelés | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Az alapértelmezett leírás üres az áfához, ha a **Közzététel típusa** = **a projektszámlák bizonylatainak áfájával**. |
| Projektvezetés és könyvelés | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dupla tranzakciók vannak közzé téve, ha a feladatalapú számlázást használják a Dataverse-szolgáltatásban a Project Operations integrációval. |
| Projektvezetés és könyvelés | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | A Project Operations integrációhoz a bevételelszámolásra vonatkozó készültségi százalékérték helytelen. |
| Projektvezetés és könyvelés | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | A bevételek elhatárolása duplázva lesz függőben lévő szállítói számlákhoz a Project Operations egy integrált forgatókönyvben. |
| Projektvezetés és könyvelés | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nem lehet közzétenni az integrációs naplót, ha a bevételi profilra vonatkozó szabály beállítása **Csoport** beállítás. |
| Projektvezetés és könyvelés | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nem lehet olyan projektmegrendelőkhöz beszerzési számlát közzétenni, amely több mértékegységgel is tartalmaz sort. |
| Projektvezetés és könyvelés | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | A projekt alapértelmezett pénzügyi dimenziója nem frissíthető a Projektek **V2** adatentitás használatával. |
| Projektvezetés és könyvelés | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | A projektbecslés létrehozásának kötegfolyamata túl sok időt vesz igénybe. |
| Projektvezetés és könyvelés | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Egy szerződés törlésekor az ügyfélhez tartozó cím is törölve lesz. |
| Utazás és költség | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | A költségjelentés-jóváhagyás munkafolyamat-feltétele nincs megfelelően kiértékelve. |
| Utazás és költség | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | A költségjelentési irányelv nem megfelelően értékeli a projektazonosítót. |
| Utazás és költség | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | A **Felosztás személyesre a vállalatközi költségtranzakciókhoz** nem működik megfelelően. |
| Utazás és költség | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Ha törlik az utazási igényléseket az bizonyos költségjelentés sorának egyes igényléseit véletlenül törli. Ez akkor fordul elő, ha a költségjelentés és az utazási igénylés recID azonosítója megegyezik. |
| Utazás és költség | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Probléma van a Költség mobilalkalmazásban, ha a költségjelentési szabályzatok megkövetelik a **Projektazonosító** mezőt. |
| Utazás és költség | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | A projekthez kapcsolódó vállalatközi költségek nem módosíthatók. Ehelyett a következő hibaüzenet jelenik meg: „Az objektumhivatkozás nincs beállítva egy objektumpéldányra”. |
| Utazás és költség | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | A költségjelentés feladása után nem a megfelelő pénznem és összeg szerepel a banki alszámlán. |
| Utazás és költség | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Továbbfejlesztettük a *Hitelkártya-tranzakciók törlése* funkciót.  |
| Utazás és költség | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | A költségjelentésben szereplő áfa nem számítható ki következetesen, ha másik jelentés pénznem van megadva egy jogi személyben. |
| Utazás és költség | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | A teljesítményre hatással van egy új készpénzes utazási költség hozzáadása. |
| Utazás és költség | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | A költségszabályzat szabályai nem aktiválódnak a költségjelentésen. |
| Utazás és költség | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Ha az adatkezelési keretrendszer használatával feltölt egy új megosztott kategóriát, azzal az összes megosztott kategória minden alkategóriáját eltávolítja. |
| Utazás és költség | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Amikor létrehoz egy költségsort, és kiválaszt egy kategóriát, akkor a következő hibaüzenet jelenik meg: „A DOM áfacsoport és az STD áfacsoport nem érvényes.” |
| Utazás és költség | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Szinkronizálási problémák vannak a Költség mobilalkalmazással. |
