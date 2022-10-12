---
title: 2022. szeptemberi újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations Lite központi telepítésének 2022. szeptemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621358"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022. szeptemberi újdonságok – A Project Operations Lite telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.46.0.60

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

| Funkcióterület | Funkció neve | További információ |
| --- | --- | --- |
| Lehetőségkezelés | **Idézetek felülvizsgálata és aktiválása**<br>A Project Operations az értékesítési folyamat teljes támogatását biztosítja. A projekt idézetek aktiválhatók, hogy egy olyan állapotot képviseljenek, ahol az idézet csak olvasható és felülvizsgálat alatt áll. Az aktivált idézetek módosíthatók, hogy új idézeteket hozzanak létre, amelyek megnövelt verziószámmal rendelkeznek. Az aktivált projektjegyzések vagy árajánlat-változatok megnyertként vagy elveszettként zárhatók le. | [Projektárajánlat aktiválása és felülvizsgálata](/dynamics365/project-operations/sales/activation-and-revision) |
| Számlázás és árképzés | **Az időzónafüggetlen ár alapértelmezett**<br>A Project Operations bevezette az időzóna-agnosztikus dátum koncepcióját a projekt összes tényleges elemére. Egy új mező, **a Tranzakció dátuma** mostantól elérhető a naplósorokban és a tényleges adatokban, és a tranzakció dátumának tárolására szolgál, de anélkül, hogy ezt a dátumot koordinált világidőre konvertálná. Ezt a dátumot fogjuk használni az olyan downstream folyamatokhoz, mint az ár alapértelmezett beállítása és a számla létrehozása. | <p>[Költséghányadok meghatározása projektalapú becslésekhez és tényleges adatokhoz](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Határozza meg az értékesítési árakat a projektalapú becslésekhez és tényleges adatokhoz](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Számlázás és árképzés | **Hatálybalépési árfelülírások a Project Operationsben**<br>Az érvényes dátum szerinti árfelülírások lehetővé teszik az árlistában szereplő konkrét árak felülbírálását vagy módosítását. | [Hatálybalépéskori árfelülírások](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Idő és költség | **Globális jóváhagyó**<br>Ez a funkció lehetővé teszi a független szoftverszállító (ISV) és a központosított jóváhagyást, függetlenül a projektben szereplő projekt vagy csapattag állapotától. | [Biztonság és jóváhagyások](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2754422. | Az anyag- és költségbecslések nem áramlanak Dynamics 365 Finance, amikor a projekteket bemásolják Dataverse. |
| Idő és költség | 2787409. | A nem érvényes jóváhagyók jóváhagyhatják a nem projektidő-bejegyzést. |
| Lehetőségkezelés | 2788907. | Frissített hibaüzenet a jelzőket tartalmazó rendeléssorok egyediségének érvényesítéséről. |
| Idő és költség | 2842253. | Null kivételkezelés az időjóváhagyáshoz. |
| Számlázás és árképzés | 2844181. | A korrelációs azonosító lekérésének elmulasztása blokkolja a számla létrehozását. |
| Számlázás és árképzés | 2876628. | QLD, CLD – Az árlista felbontásának becslése az árlista örökölt dátumtartomány-mezőit kell használnia. |
| Alvállalkozói | 2893222. | Ha egy alvállalkozói sorhoz nincs megadva szerepkör, lehetővé kell tenni, hogy ezt a sort egy csapattagon bármely szerepkörhöz kiválassza. |
