---
title: Project Operations kettős írás leképezési verziói
description: Ez a témakör a(z) Dynamics 365 Project Operations-hez szükséges kettős írású térképek listáját tartalmazza.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 452f9f16bfbae2d547afb9fcf4fc51595ea49890
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547112"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations kettős írás leképezési verziói

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az Dynamics 365 Project Operations erőforrásokkal/nem raktározott forgatókönyvekkel kapcsolatos használathoz kettős írású térképeknek kell futniuk a környezetben. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Előfeltételként meghatározott térképek: Kettős írású vezénylőmegoldás

A Project Operations megoldáshoz a következő térképek szükségesek. Győződjön meg róla, hogy a következő táblázatban felsorolt térképeket és a környezetében található kapcsolódó táblázattérképeket futtatja.

| Táblaleképezés | Kezdeti szinkronizálás |
| --- | --- |
| Főkönyv (msdyn_ledgers) | A táblázattérképhez és az összes előfeltételhez kezdeti szinkronizálásra van szükség. Kezdeti szinkronizálás fő eleme Finance and Operations alkalmazások. |
| Jogi entitások (cdm_companies) | Nem kötelező. A rendszer automatikusan feltölti ezt az entitást, ha a környezeteket kettős írással kapcsolják össze. |
| Ügyfelek V3 (fiókok) | Nem szükséges a kiépítéshez. |
| Szállítók V2 (msdyn_vendors) | Nem szükséges a kiépítéshez. |

1. A leképezések listájában válassza ki a Főkönyvi **(msdyn\_ledgers)** térkép minden előfeltételét, majd jelölje ki a **Kezdeti szinkronizálás** jelölőnégyzetet. A **Kezdeti szinkronizálási főelem** mezőjében válassza ki az **Finance and Operations alkalmazásokat** mind a főkönyvi térképhez, mind az összes előfeltétel térképhez. Válassza a **Futtatás** lehetőséget.

![Főkönyvi leképezés szinkronizálása.](media/DW6.png)

2. Kövesse ugyanazokat a lépéseket a fenti táblázatban felsorolt összes többi táblázattérképhez. A térképek futtatásakor ne jelölje be a **Kezdeti szinkronizálás** jelölőnégyzetet.

## <a name="project-operations-dual-write-maps"></a>Project Operations kettős írású térképei

A Project Operations megoldáshoz a következő térképek szükségesek. A kettős írású leképezés verziók a Project Operations 2021 májusi frissítésétől kezdve, 4.10.0.186 verzió.

| **Entitásleképezés** | **Legutóbbi verzió** | **Kezdeti szinkronizálás** |
| --- | --- | --- |
| A projekt tranzakciókapcsolatainak integrációs entitása (msdyn\_transactionconnections) | 1.0.0.0 | Nem szükséges a kiépítéshez. |
| Projektszerződés fejlécei (értékesítési megbízások) | 1.0.0.1 | Nem szükséges a kiépítéshez. |
| Projektszerződéssorok (salesorderdetails) | 1.0.0.0 | Nem szükséges a kiépítéshez. |
| Projektfinanszírozási forrás (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Nem szükséges a kiépítéshez. |
| Project Operations integrációs táblázat az anyagbecslésekhez (msdyn\_estimatelines) | 1.0.0.0 | Nem szükséges a kiépítéshez. |
| Projektszámla-ajánlatok V2 (számlák) | 1.0.0.3 | Nem szükséges a kiépítéshez. |
| Project Operations integrációjának tényleges adatai (msdyn_actuals) | 1.0.0.14 | Nem szükséges a kiépítéshez. |
| Project Operations integráció szerződéssor mérföldkövek (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Nem szükséges a kiépítéshez. |
| A Project Operations integráció entitása költségbecslésekhez (msdyn_estimatelines) | 1.0.0.2 | Nem szükséges a kiépítéshez. |
| A Project Operations integrációs entitása órabecslésekhez (msdyn_resourceassignments) | 1.0.0.5 | Nem szükséges a kiépítéshez. |
| Project Operations integráció projektköltség-kategóriák exportálási entitása (msdyn_expensecategories) | 1.0.0.1 | Nem szükséges a kiépítéshez. |
| Project Operations integráció projektkiadások exportálási entitása (msdyn_expenses) | 1.0.0.2 | Nem szükséges a kiépítéshez. |
| Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices) | 1.0.0.0 | Nem szükséges a kiépítéshez. |
| Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Nem szükséges a kiépítéshez. |
| Az összes vállalat projekterőforrás-szerepkörei (bookableresourcecategories) | 1.0.0.1 | A kiépítés során a Dynamics 365 Dataverse környezetben tartott projektmenedzseri és csapattagi erőforrás-szerepkörök szinkronizálásához a táblatérkép kezdeti szinkronizálása szükséges. Dataverse a kezdeti szinkronizálás fő forrása. |
| Projektfeladatok (msdyn_projecttasks) | 1.0.0.4 | Nem szükséges a kiépítéshez. |
| Projekttranzakciós kategóriák (msdyn_transactioncategories) | 1.0.0.0 | Nem szükséges a kiépítéshez. |
| V2 projektek (msdyn_projects) | 1.0.0.2 | Nem szükséges a kiépítéshez. |

Végezze el a következő lépéseket a felsorolt térképek futtatásához.

1. Engedélyezze a Projekt erőforrás-szerepköreit az **összes vállalat (bookableresourcecategories)** táblatérkép számára, mivel ez a térkép megköveteli a kezdeti szinkronizálást. A **Kezdeti szinkronizálás fő eleme** mezőjében válassza a **Common data service** lehetőséget. 

 ![Erőforrás-szerepkör-táblázat térképének szinkronizálása.](media/6ResourceInitialSync.jpg)

 Várjon, amíg a térkép állapota **fut**, mielőtt a következő lépésre lép.

2. Jelölje ki az összes többi szükséges térképet. A kettős írású térképlistában a jobb felső sarokban található **Projekt** kulcsszóval szűrheti őket. Az összes térképet egyszerre is kijelölheti, majd futtathatja. További tudnivalókért lásd: [Több táblatérkép kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Győződjön meg arról, hogy engedélyezi és futtatja a kapcsolódó entitástérképeket is.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations kettős írás leképezési verziói

Mindig futtassa a térkép legújabb verzióját a környezetében. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha az alábbi feltételek bármelyike fennáll:

- A térkép nincs aktiválva.
- A térkép legújabb verziója nincs aktiválva. 
- A kapcsolódó táblatérképek nincsenek aktiválva.

A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon tekintheti meg. A térkép új verzióját aktiválhatja a **Táblatérkép verziói** pontban, ott pedig az legújabb verzió kiválasztásával, majd a kijelölt verzió mentésével. Ha testreszabta a dobozon kívüli táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
