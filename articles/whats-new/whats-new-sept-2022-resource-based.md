---
title: 2022. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Microsoft Dynamics 365 Project Operations 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrás-/nem készletalapú forgatókönyvekhez.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634808"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations környezeti Dataverse verzióban 4.46.0.60
- Projektvezetés és könyvelés Dynamics 365 Finance környezetben 10.0.29-es verzió

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Árajánlatok felülvizsgálata és aktiválása**<br>A Project Operations teljes mértékben támogatja az értékesítési folyamatot. A projektajánlatok aktiválhatók egy olyan állapot ábrázolására, ahol az árajánlat írásvédett és felülvizsgálat alatt áll. Az aktivált árajánlatok felülvizsgálhatók olyan új árajánlatok létrehozásához, amelyek bővített verziószámmal rendelkeznek. Az aktivált projektajánlatok vagy árajánlat-módosítások megnyertként vagy elveszettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Időzónafüggetlen ár-nemteljesítés**<br>A Project Operations bevezette az időzónafüggetlen dátum fogalmát a projekt összes tényadatán. Egy új mező, a Tranzakció dátuma **mostantól elérhető a naplósorokban és a tényadatokban, és a tranzakció dátumának tárolására lesz használva, anélkül azonban,** hogy ezt a dátumot egyezményes világidőre konvertálná. Ezt a dátumot fogjuk használni az olyan lefelé irányuló folyamatokhoz, mint az ár nemteljesítése és a számla létrehozása. | <p>[Költségarányok meghatározása projektalapú becslésekhez és tényadatokhoz](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Értékesítési árak meghatározása projektalapú becslésekhez és tényadatokhoz](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Számlázás és árképzés | **Dátum-hatályos árfelülírások a Project Operations rendszerben**<br>A dátum szerinti érvényben lévő árfelülbírálások lehetőséget nyújtanak az árlistában szereplő konkrét árak felülbírálására vagy módosítására. | [Dátum szerinti árfelülírások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Alvállalkozói | **Alvállalkozók és szállítói számlák egyeztetése**<br>Ez a funkció lehetővé teszi az ügyfelek számára, hogy alvállalkozókat hozzanak létre az erőforrás-idő, a költségkategóriák és a projektmunkához használt anyagok megvásárlásához. Azt is lehetővé teszi az ügyfelek számára, hogy a pénzügyi és üzemeltetési alkalmazásokban rögzítsék a szállítói számlákat, amelyek a projektmenedzserek Dataverse számára elérhetők lesznek ellenőrzés céljából. | <p>[Alvállalkozói szerződések kezelése](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Szállítói számlák létrehozása](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállítót (ISV) és a központi jóváhagyást, függetlenül a projekt vagy a csapattag állapotától a projektben. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |
| Költségkezelés | **Költségkötelezettség feladásának lehetősége a szállító pénznemében**<br>Ez a funkció lehetővé teszi, hogy a költségjelentéseket a készpénzes fizetési módhoz tartozó szállítói pénznemben adják fel. | [Költségkötelezettség feladásának lehetősége a szállító pénznemében](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekt beszerzés | **Fizetés szállítói kifizetésekkor**<br>Ez a funkció lehetővé teszi a Fizetés fizetéskor (PWP) funkció használatát a Project Operations nem készletkörnyezetekkel. Lehetővé teszi a szállítói kifizetések zárolását/visszatartását a visszatartási feltételek alapján, amíg a kifizetés meg nem érkezik a vevőtől. | [Fizetés szállítói kifizetésekkor](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekt beszerzés | **Projektbeszerzési igénylések**<br>Ez a funkció lehetővé teszi a felhasználók számára, hogy projekthez kapcsolódó beszerzési rendeléseket hozzanak létre olyan jogi személyekben, ahol a Project Operations Dynamics 365 Customer Engagement integrációja engedélyezve van. A projekt beszerzési rendelései felhasználhatók a nem készletezett anyagbeszerzések rögzítésére a projekttel szemben a beszerzési osztály személye szerint. A projekt beszerzési rendelései nem lesznek szinkronizálva a következővel:Dataverse. Virtuális entitás használatával azonban megjelenítheti a projekt beszerzési rendelési sorait Dataverse a projektmenedzser adataihoz. A projekthez kapcsolódó szállítói számla költsége integrálva van a Projekt tényleges adatai entitással a Dataverse. A projektköltség rögzítésre kerül a Project Subledgerben a Project Operations integrációs naplójának használatával. | |
|Projekttervezés és nyomon követés|**Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal** </br> </br>Az erőforrás-hozzárendelési kontúrszerkesztési API lehetővé teszi a fejlesztők számára, hogy programozott módon adják meg a feladathozzárendelő erőfeszítéseit bármely támogatott dátumtartományban a részletesebb időfázisos munkamennyiség-tervezés érdekében.|[Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi táblázat azokat a kettős írású leképezéseket mutatja be, amelyeket a Project Operations 2022. szeptemberi kiadásában módosítottak vagy adtak hozzá.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Project Operations integrációjának tényleges adatai (msdyn_actuals) | 1.0.0.15. | Ez a térkép támogatja az alvállalkozói tényadatok Project Operations alkalmazással történő feldolgozását erőforrás-alapú forgatókönyvekhez. |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.2 | Ez a térkép támogatja az alvállalkozói tényadatok Project Operations alkalmazással történő feldolgozását erőforrás-alapú forgatókönyvekhez. |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ez a térkép támogatja az alvállalkozói tényadatok Project Operations alkalmazással történő feldolgozását erőforrás-alapú forgatókönyvekhez. |

Mindig a térkép legújabb verzióját futtassa a környezetben, és engedélyezze az összes kapcsolódó táblaleképezést a Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítésekor. Előfordulhat, hogy egyes funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy beépített táblatérképet, alkalmazza újra a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémába ütközik a térkép indításakor, kövesse a Kettős írás hibaelhárítási útmutató Hiányzó táblaoszlopok probléma a térképeken [című szakaszában található](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | Az anyag- és költségbecslések nem áramlanak a Finance-be, amikor a projekteket a Dataverse. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyó jóváhagyhat egy nem projektidő-bejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet a jelzőket tartalmazó rendeléssorok egyediségének ellenőrzéséről. |
| Idő és költség | 2842253. | Null kivétel kezelése az idő jóváhagyásához. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosító lekérésének elmulasztása blokkolja a számla létrehozását. |
| Számlázás és árképzés | 2876628. | QLD, CLD – Az árlista felbontásának becsléséhez az árlista örökölt dátumtartomány-mezőit kell használnia. |
| Alvállalkozói | 2893222. | Ha egy alvállalkozói sorhoz nincs megadva szerepkör, akkor lehetővé kell tenni, hogy ezt a sort egy csapattagon bármely szerepkörhöz kiválassza. |

### <a name="project-management-and-accounting-in-finance"></a>Projektvezetés és könyvelés a Finance-ben

A frissítésben szereplő hibajavításokkal kapcsolatos információkért jelentkezzen be a Lifecycle Services szolgáltatásba, és tekintse meg a Microsoft Dynamics [tudásbáziscikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>A közelgő kiadásban alapértelmezés szerint bekapcsolt funkciók

Az alábbi táblázat a 10.0.30-as verzióban alapértelmezés szerint bekapcsolt szolgáltatásokat sorolja fel. A legtöbb automatikusan bekapcsolt funkció kikapcsolható a [Funkciókezelésben](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). A jövőben előfordulhat, hogy egyes automatikusan bekapcsolt funkciók törlődnek a funkciókezelésből, és kötelezővé válnak. Ez a módosítás biztosítja, hogy az ügyfelek az aktuális funkciókat használják, így a fejlesztések a hozzáadáskor az aktuális funkciókra épülhetnek. A funkciók soha nem lesznek automatikusan engedélyezve kevesebb mint egy év alatt, kivéve, ha úgy ítélik meg, hogy elengedhetetlenek.

| Funkció neve | Engedélyezés dátuma | Funkció hozzáadva | Funkció állapota | Modul |
| --- | --- | --- |--- |--- |
| Aszinkron művelet engedélyezése, ha a felhasználónak váltania kell a szinkronizálási és az aszinkron műveletek között | 2022. október 21. | 2021. április 9. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A szükséges bevételek költségpolitikájának értékelése | 2022. október 21. | 2021. december 20. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A dolgozók delegálásával létrehozott költségjelentések listanézete | 2022. október 21. | 2020. február 19. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
| A futásteljesítmény teljes kiszámítása pénzügyi év szerint | 2022. október 21. | 2022. május 10. | Alapértelmezés szerint be van kapcsolva | Költségkezelés |
