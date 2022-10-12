---
title: 2022. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást erőforrás-/nem készletalapú forgatókönyvekhez.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621343"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.46.0.60
- Projektmenedzsment és könyvelés Dynamics 365 Finance környezetben 10.0.29-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Idézetek felülvizsgálata és aktiválása**<br>A Project Operations az értékesítési folyamat teljes támogatását biztosítja. A projekt idézetek aktiválhatók, hogy egy olyan állapotot képviseljenek, ahol az idézet csak olvasható és felülvizsgálat alatt áll. Az aktivált idézetek módosíthatók, hogy új idézeteket hozzanak létre, amelyek megnövelt verziószámmal rendelkeznek. Az aktivált projektjegyzések vagy árajánlat-változatok megnyertként vagy elveszettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Az időzónafüggetlen ár alapértelmezett**<br>A Project Operations bevezette az időzóna-agnosztikus dátum koncepcióját a projekt összes tényleges elemére. Egy új mező, **a Tranzakció dátuma** mostantól elérhető a naplósorokban és a tényleges adatokban, és a tranzakció dátumának tárolására szolgál, de anélkül, hogy ezt a dátumot koordinált világidőre konvertálná. Ezt a dátumot fogjuk használni az olyan downstream folyamatokhoz, mint az ár alapértelmezett beállítása és a számla létrehozása. | <p>[Költséghányadok meghatározása projektalapú becslésekhez és tényleges adatokhoz](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Határozza meg az értékesítési árakat a projektalapú becslésekhez és tényleges adatokhoz](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Számlázás és árképzés | **Hatálybalépési árfelülírások a Project Operationsben**<br>Az érvényes dátum szerinti árfelülírások lehetővé teszik az árlistában szereplő konkrét árak felülbírálását vagy módosítását. | [Hatálybalépéskori árfelülírások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Alvállalkozói | **Alvállalkozásba adás és szállítói számla egyeztetése**<br>Ez a funkció lehetővé teszi az ügyfelek számára, hogy alvállalkozói szerződést hozzanak létre az erőforrás-idő, a költségkategóriák és a projektmunkához használt anyagok megvásárlásához. Azt is lehetővé teszi az ügyfelek számára, hogy pénzügyi és üzemeltetési alkalmazásokban rögzítsék a szállítói számlákat, amelyek a projektmenedzserek Dataverse számára elérhetők lesznek ellenőrzésre. | <p>[Alvállalkozói szerződések kezelése](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Szállítói számlák létrehozása](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállító (ISV) és a központosított jóváhagyást, függetlenül a projekt vagy a csapattagok állapotától. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |
| Költségkezelés | **Költségkötelezettség feladásának lehetősége a szállító pénznemében**<br>Ez a funkció lehetővé teszi a költségjelentések feladását a szállító pénznemében a készpénzes fizetési módhoz. | [Költségkötelezettség feladásának lehetősége a szállító pénznemében](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektbeszerzés | **Fizetés a szállítói kifizetések kifizetése esetén**<br>Ez a funkció lehetővé teszi a Fizetés fizetés fizetéskor (PWP) funkció használatát a Project Operations nem készletkörnyezetekben. Lehetővé teszi a szállítói kifizetések zárolását/visszatartását a visszatartási feltételek alapján, amíg a kifizetés meg nem érkezik a vevőtől. | [Fizetés a szállítói kifizetések kifizetése esetén](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektbeszerzés | **Projektbeszerzési igénylések**<br>Ez a funkció lehetővé teszi a felhasználók számára, hogy projekthez kapcsolódó beszerzési rendeléseket hozzanak létre olyan jogi személyekben, ahol a Project Operations on Dynamics 365 Customer Engagement integráció engedélyezve van. A projektvásárlási rendelések felhasználhatók a projekthez kapcsolódó nem készletezett anyagbeszerzések rögzítésére beszerzési osztály személyisége alapján. A projektvásárlási rendelések nem lesznek szinkronizálva a következővel Dataverse: . Virtuális entitással azonban megjelenítheti a Project beszerzésirendelés-sorait a Dataverse projektmenedzseri adatokhoz. A projekthez kapcsolódó szállítói számla költsége integrálva van a Projekt tényleges adatai entitással a Dataverse. A projektköltséget a projekt analitikus fájlban rögzíti a Project Operations integrációs naplója segítségével. | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat a Project Operations 2022. szeptemberi kiadásában módosított vagy hozzáadott kettős írású térképeket mutatja be.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Project Operations integrációjának tényleges adatai (msdyn_actuals) | 1.0.0.15. | Ez a térkép támogatja az alvállalkozói adatok feldolgozását a Project Operations segítségével erőforrás-alapú forgatókönyvek esetén. |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.2 | Ez a térkép támogatja az alvállalkozói adatok feldolgozását a Project Operations segítségével erőforrás-alapú forgatókönyvek esetén. |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ez a térkép támogatja az alvállalkozói adatok feldolgozását a Project Operations segítségével erőforrás-alapú forgatókönyvek esetén. |

Mindig futtassa a térkép legújabb verzióját a környezetében, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése közben. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblázattérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha a térkép indításakor problémába ütközik, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszának utasításait](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | Az anyag- és költségbecslések nem áramlanak a Finance-be, amikor a projekteket bemásolják Dataverse. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyók jóváhagyhatják a nem projektidő-bejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet a jelzőket tartalmazó rendeléssorok egyediségének érvényesítéséről. |
| Idő és költség | 2842253. | Null kivételkezelés az időjóváhagyáshoz. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosító lekérésének elmulasztása blokkolja a számla létrehozását. |
| Számlázás és árképzés | 2876628. | QLD, CLD – Az árlista felbontásának becslése az árlista örökölt dátumtartomány-mezőit kell használnia. |
| Alvállalkozói | 2893222. | Ha egy alvállalkozói sorhoz nincs megadva szerepkör, lehetővé kell tenni, hogy ezt a sort egy csapattagon bármely szerepkörhöz kiválassza. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és számvitel a pénzügyekben

A frissítésben található hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services szolgáltatásba Microsoft Dynamics, és tekintse meg a [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Alapértelmezés szerint be van kapcsolva funkciók a közelgő kiadásban

Az alábbi táblázat azokat a szolgáltatásokat sorolja fel, amelyek alapértelmezés szerint be vannak kapcsolva a 10.0.30-as verzióban. A legtöbb automatikusan bekapcsolt funkció kikapcsolható a [Funkciókezelésben](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). A jövőben előfordulhat, hogy egyes, automatikusan bekapcsolt funkciók eltávolításra kerülnek a funkciókezelésből, és kötelezővé válnak. Ez a módosítás biztosítja, hogy az ügyfelek a jelenlegi funkciókat használják, így a fejlesztések a hozzáadáskor a jelenlegi funkciókra építhetnek. A funkciók soha nem lesznek automatikusan engedélyezve egy évnél rövidebb idő alatt, kivéve, ha elengedhetetlennek minősülnek.

| Funkció neve | Dátum engedélyezése | Hozzáadott funkció | Funkció állapota | Modul |
| --- | --- | --- |--- |--- |
| Engedélyezze az aszinkron műveletet, ha a felhasználónak váltania kell a szinkronizálási és az aszinkron műveletek között | 2022. október 21. | 2021. április 9. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A szükséges bevételek költségpolitikai értékelése | 2022. október 21. | 2021. december 20. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A dolgozók delegálásával létrehozott költségjelentések listanézete | 2022. október 21. | 2020. február 19. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A futásteljesítmény-összteljesítmény kiszámítása pénzügyi év szerint | 2022. október 21. | 2022. május 10. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
