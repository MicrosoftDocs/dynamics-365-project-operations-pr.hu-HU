---
title: 2022. szeptemberi újdonságok – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a cikk a Project Operations 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást a Microsoft Dynamics 365 Project Operations erőforrás/nem készletalapú forgatókönyvek esetében.
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

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.46.0.60 verziójú Dataverse-környezetben
- Projektmenedzsment és könyvelés a Dynamics 365 Finance 10.0.29-es verziójú környezetekben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Árajánlatok aktiválása és ellenőrzése**<br>A Project Operations az értékesítési folyamat teljes körű támogatását biztosítja. A projektárajánlatok aktiválhatóak annak az állapotnak a megjelenítésére, ahol az ajánlat csak olvasható, és ellenőrzés alatt áll. Az aktivált árajánlatok átdolgozhatóak olyan új ajánlatok létrehozásához, amelyekhez növekményesített verziószáma van. Az aktivált projektárajánlatok megnyertként vagy elvesztettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Időzóna-agnosztikus ár alaphelyzetbe állítások**<br>A Project Operations bevezette az időzóna-agnosztikus dátumfogalmat minden projekttényadathoz. Az új mező, a **Tranzakció dátuma** már elérhető a naplósorokban és a tényadatok között, és a rendszer a tranzakció bekövetkezésének dátumát tárolja benne, de nem alakítja át ezt a dátumot egyezményes világidőre. Ez a dátum a későbbi folyamatokban használatos, például az árak alapértelmezésének beállítására és a számlák létrehozására. | <p>[Az önköltéségi árak meghatározása a projekt alapú becslésekhez és a tényekhez](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Az értékesítési árak meghatározása projektalapú a becslésekhez és a tényekhez](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Számlázás és árképzés | **Érvényességi dátummal rendelkező árfelülbírálások a Project Operations alkalmazásban**<br>A Hatályossági dátummal rendelkező árfelülbírálások segítségével felülbírálhat vagy módosíthat adott árakat az árlistában. | [Hatályossági dátummal rendelkező árfelülbírálások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Alvállalkozásba adás | **Alvállalkozásba adás és szállítói számlák egyeztetése**<br>Ez a funkció lehetővé teszi, hogy az ügyfelek alvállalkozói szerződésket hozzanak létre az erőforrás-idő, a költségkategóriák és a projekt munkához használt anyagok beszerzéséhez. Emellett lehetővé teszi az ügyfelek számára, hogy a pénzügyi és műveleti alkalmazásokban olyan szállítói számlákat rögzítsenek, amelyek Dataverse-ellenőrzésre elérhetők lesznek a projektvezetők számára. | <p>[Alvállalkozók kezelése](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Szállítói számlák létrehozása](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállítókat (ISV) és a központi jóváhagyást, függetlenül a projekt vagy a csoporttagok állapotától. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |
| Költségkezelés | **A költségfelelőség közzététítésének lehetősége a szállító pénznemében**<br>Ez a funkció lehetővé teszi költségjelentések feladását a szállítói pénznemben készpénzes fizetési módhoz. | [A költségfelelőség közzétételének lehetősége a szállító pénznemében](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektbeszerzés | **Fizetéskor fizetett szállítói kifizetések**<br>Ez a funkció lehetővé teszi, hogy a fizetés fizetéskor (PWP) szolgáltatást a Project Operations alkalmazásban használja nem raktározási környezetekben. Lehetővé teszi az szállítói fizetések letiltását/megtartását a megtartási feltételek alapján mindaddig, amíg a fizetés nem érkezik meg az ügyféltől. | [Fizetéskor fizetett szállítói kifizetések](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektbeszerzés | **Projekt beszerzési igénylései**<br>Ez a funkció teszi lehetővé a felhasználók számára, hogy projekthez kapcsolódó megrendeléseket hozzanak létre olyan jogi személyeknél, ahol engedélyezve van a Project Operations a Dynamics 365 Customer Engagement alkalmazásban integrációja. A projektek beszerzési rendelései, nem készleten lévő anyagok beszerzésére használhatók a projekttel szemben egy Beszerzésiosztályhoz tartozó személy által. A projektmegrendeléseket nem szinkronizálja a rendszer Dataverse-szel. A projektmenedzser tájékoztatására azonban virtuális entitás is a Dataverse-ben a projektmegrendelések sorainak megjelenítésére. A projekthez kapcsolódó szállítói számlaköltség integrálva van a Projekt tényadatai entitással a Dataverse-ben. A projektköltség rögzítve van a projekt alszámláján a Project Operations integrációs naplója segítségével. | |
|Projekttervezés és nyomon követés|**Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal** </br> </br>Az erőforráshozzárendelési-kontúr API segítségével a fejlesztők programozott módon határozhatják meg a feladat hozzárendeltjének erőfeszítését bármely támogatott dátumtartományra vonatkozóan a részletesebb erőfeszítésalapú tervezés érdekében.|[Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Az alábbi tábla a Project Operations 2022. szeptemberi kiadásában módosított vagy hozzáadott kettős írású térképeket tartalmazza.

| Entitásleképezés | Frissített verzió | Hozzászólások |
| -------------- | ------------------- | ------------|
| Project Operations integrációjának tényleges adatai (msdyn_actuals) | 1.0.0.15. | Ez a leképezés erőforrásalapú forgatókönyvek esetén támogatja a sz alvállalkozói tényadatfeldolgozást a Project Operations segítségével. |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.2 | Ez a leképezés erőforrásalapú forgatókönyvek esetén támogatja a sz alvállalkozói tényadatfeldolgozást a Project Operations segítségével. |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ez a leképezés erőforrásalapú forgatókönyvek esetén támogatja a sz alvállalkozói tényadatfeldolgozást a Project Operations segítségével. |

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a leképezés legújabb verziója nincs aktiválva. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verziójának aktiválásához válassza **Táblatérkép verziói** pontot, ott pedig az legújabb verziót válassza ki, majd a kijelölt verziót mentse. Ha testreszabott egy gyári táblaleképezést, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha problémát tapasztal a leképezés elindításával kapcsolatban, kövesse a [Kettős írás hibaelhárítási útmutató térkép szakaszának Hiányzó táblaoszlopok című](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részében található utasításokat.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | A projektek Dataverse-be másolása esetén az anyag- és költségbecslések nem áramlanak át a Finance-be. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyó jóváhagyhat egy nem projekt időbejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet az egyediség ellenőrzésével a jelölőket tartalmazó megrendeléssorokhoz. |
| Idő és költség | 2842253. | Null kivételkezelés idő jóváhagyásához. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosítót nem lehet lekérni, és ez akadályozza a számlalétrehozást. |
| Számlázás és árképzés | 2876628. | QLD, CLD – A becsült árlista felbontásának az árlista korábbi dátumtartomány-mezőit kell használnia. |
| Alvállalkozásba adás | 2893222. | Ha az alvállalkozói sorhoz nincs megadva szerepkör, akkor bármelyik szerepkörhöz ki lehet választani az adott sort a csoporttagok közül. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmenedzsment és könyvelés a Finance-ban

Ha további tájékoztatást szeretne kapni a frissítésben található hibajavításokról, lépjen be a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásokba, és tekintse meg a [Tudásbázis cikket](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Az érkező kiadásban alapértelmezetten bekapcsolt funkciók

Ez a kiadás a 10.0.30 verzióban alapértelmezetten bekapcsolt funkciókat tartalmazza. A legtöbb olyan funkció, amely automatikusan be lett kapcsolva, a [Funkciókezelésben](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) kikapcsolható. A jövőben előfordulhat, hogy egyes funkciók, amelyek automatikusan be vannak kapcsolva, eltávolításra kerülnek a Szolgáltatáskezelésből, és kötelezővé válnak. A változás biztosítja, hogy az ügyfelek a naprakész funkciókat használják, így a fejlesztések a hozzáadásuk során a jelenlegi funkciókra épülhessenek. A szolgáltatások egy évnél rövidebb idő alatt soha nem lesznek automatikusan engedélyezve, kivéve ha ez alapvető fontosságú.

| Funkció neve | Dátum engedélyezése | Funkció hozzáadva | Funkció állapota | Modul |
| --- | --- | --- |--- |--- |
| Aszinkron művelet engedélyezése, ha a felhasználónak váltania kell a szinkronizálást és az aszinkron műveletek között | 2022. október 21. | 2021. április 9. | Alapértelmezés szerint be | Költségkezelés |
| Költségjelentések értékelése a szükséges nyugtákhoz | 2022. október 21. | 2021. december 20. | Alapértelmezés szerint be | Költségkezelés |
| A munkatársak delegálásával létrehozott költségjelentések listanézete | 2022. október 21. | 2020. február 19. | Alapértelmezés szerint be | Költségkezelés |
| Futásteljesítmény-végösszegek számítása pénzügyi év alapján | 2022. október 21. | 2022. május 10. | Alapértelmezés szerint be | Költségkezelés |
