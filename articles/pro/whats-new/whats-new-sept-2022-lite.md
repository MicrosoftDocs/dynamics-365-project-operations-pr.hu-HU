---
title: 2022. szeptemberi újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations könnyű telepítés 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634855"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022. szeptemberi újdonságok – A Project Operations Lite telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.46.0.60 verziójú Dataverse-környezetben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Árajánlatok aktiválása és ellenőrzése**<br>A Project Operations az értékesítési folyamat teljes körű támogatását biztosítja. A projektárajánlatok aktiválhatóak annak az állapotnak a megjelenítésére, ahol az ajánlat csak olvasható, és ellenőrzés alatt áll. Az aktivált árajánlatok átdolgozhatóak olyan új ajánlatok létrehozásához, amelyekhez növekményesített verziószáma van. Az aktivált projektárajánlatok megnyertként vagy elvesztettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Időzóna-agnosztikus ár alaphelyzetbe állítások**<br>A Project Operations bevezette az időzóna-agnosztikus dátumfogalmat minden projekttényadathoz. Az új mező, a **Tranzakció dátuma** már elérhető a naplósorokban és a tényadatok között, és a rendszer a tranzakció bekövetkezésének dátumát tárolja benne, de nem alakítja át ezt a dátumot egyezményes világidőre. Ez a dátum a későbbi folyamatokban használatos, például az árak alapértelmezésének beállítására és a számlák létrehozására. | <p>[Az önköltéségi árak meghatározása a projekt alapú becslésekhez és a tényekhez](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Az értékesítési árak meghatározása projektalapú a becslésekhez és a tényekhez](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Számlázás és árképzés | **Érvényességi dátummal rendelkező árfelülbírálások a Project Operations alkalmazásban**<br>A Hatályossági dátummal rendelkező árfelülbírálások segítségével felülbírálhat vagy módosíthat adott árakat az árlistában. | [Hatályossági dátummal rendelkező árfelülbírálások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállítókat (ISV) és a központi jóváhagyást, függetlenül a projekt vagy a csoporttagok állapotától. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |
|Projekttervezés és nyomon követés|**Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal** </br> </br>Az erőforráshozzárendelési-kontúr API segítségével a fejlesztők programozott módon határozhatják meg a feladat hozzárendeltjének erőfeszítését bármely támogatott dátumtartományra vonatkozóan a részletesebb erőfeszítésalapú tervezés érdekében.|[Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | A projektek Dataverse-be másolása esetén az anyag- és költségbecslések nem áramlanak át a Dynamics 365 Finance-be. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyó jóváhagyhat egy nem projekt időbejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet az egyediség ellenőrzésével a jelölőket tartalmazó megrendeléssorokhoz. |
| Idő és költség | 2842253. | Null kivételkezelés idő jóváhagyásához. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosítót nem lehet lekérni, és ez akadályozza a számlalétrehozást. |
| Számlázás és árképzés | 2876628. | QLD, CLD – A becsült árlista felbontásának az árlista korábbi dátumtartomány-mezőit kell használnia. |
| Alvállalkozásba adás | 2893222. | Ha az alvállalkozói sorhoz nincs megadva szerepkör, akkor bármelyik szerepkörhöz ki lehet választani az adott sort a csoporttagok közül. |
