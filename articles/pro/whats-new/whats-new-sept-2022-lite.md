---
title: 2022. szeptemberi újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations lite központi telepítésének 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
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

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations környezeti Dataverse verzióban 4.46.0.60

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Árajánlatok felülvizsgálata és aktiválása**<br>A Project Operations teljes mértékben támogatja az értékesítési folyamatot. A projektajánlatok aktiválhatók egy olyan állapot ábrázolására, ahol az árajánlat írásvédett és felülvizsgálat alatt áll. Az aktivált árajánlatok felülvizsgálhatók olyan új árajánlatok létrehozásához, amelyek bővített verziószámmal rendelkeznek. Az aktivált projektajánlatok vagy árajánlat-módosítások megnyertként vagy elveszettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Időzónafüggetlen ár-nemteljesítés**<br>A Project Operations bevezette az időzónafüggetlen dátum fogalmát a projekt összes tényadatán. Egy új mező, a Tranzakció dátuma **mostantól elérhető a naplósorokban és a tényadatokban, és a tranzakció dátumának tárolására lesz használva, anélkül azonban,** hogy ezt a dátumot egyezményes világidőre konvertálná. Ezt a dátumot fogjuk használni az olyan lefelé irányuló folyamatokhoz, mint az ár nemteljesítése és a számla létrehozása. | <p>[Költségarányok meghatározása projektalapú becslésekhez és tényadatokhoz](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Értékesítési árak meghatározása projektalapú becslésekhez és tényadatokhoz](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Számlázás és árképzés | **Dátum-hatályos árfelülírások a Project Operations rendszerben**<br>A dátum szerinti érvényben lévő árfelülbírálások lehetőséget nyújtanak az árlistában szereplő konkrét árak felülbírálására vagy módosítására. | [Dátum szerinti árfelülírások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállítót (ISV) és a központi jóváhagyást, függetlenül a projekt vagy a csapattag állapotától a projektben. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |
|Projekttervezés és nyomon követés|**Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal** </br> </br>Az erőforrás-hozzárendelési kontúrszerkesztési API lehetővé teszi a fejlesztők számára, hogy programozott módon adják meg a feladathozzárendelő erőfeszítéseit bármely támogatott dátumtartományban a részletesebb időfázisos munkamennyiség-tervezés érdekében.|[Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | Az anyag- és költségbecslések nem áramlanak Dynamics 365 Finance, amikor a projekteket a Dataverse. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyó jóváhagyhat egy nem projektidő-bejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet a jelzőket tartalmazó rendeléssorok egyediségének ellenőrzéséről. |
| Idő és költség | 2842253. | Null kivétel kezelése az idő jóváhagyásához. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosító lekérésének elmulasztása blokkolja a számla létrehozását. |
| Számlázás és árképzés | 2876628. | QLD, CLD – Az árlista felbontásának becsléséhez az árlista örökölt dátumtartomány-mezőit kell használnia. |
| Alvállalkozói | 2893222. | Ha egy alvállalkozói sorhoz nincs megadva szerepkör, akkor lehetővé kell tenni, hogy ezt a sort egy csapattagon bármely szerepkörhöz kiválassza. |
