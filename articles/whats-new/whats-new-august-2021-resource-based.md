---
title: Újdonságok - 2021. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez
description: Ez a témakör a Project Operations 2021. augusztusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást az erőforrás/nem készletalapú forgatókönyvek esetében.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323464"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok - 2021. augusztus - Project Operations erőforrás/nem készletalapú forgatókönyvekhez

*Érvényesség: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén*

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

   - Project Operations 4.13.0.152 verziójú Microsoft Dataverse-környezetben.
   - Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.20-es verziójában.

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- **Jóváhagyási készletek**: A jóváhagyási készletek az idő-, költség- vagy anyagfelhasználási jóváhagyási kérelmeket kisebb műveleti alcsoportokba csoportosítják. Ez a csoportosítás lehetővé teszi, hogy a jóváhagyásokat projektenként meghatározott sorrendben dolgozzák fel, és lehetővé teszi az újbóli próbálkozást és a sorrendiséget. A kérelmek csoportosítása javítja a jóváhagyási folyamat megbízhatóságát és nyomon követhetőségét nagy mennyiségű jóváhagyás esetén. További információért lásd: [Jóváhagyási készletek](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations kettős írású térképeinek frissítése

Ebben a kiadásban nincsenek frissítések a Project Operations kettős írási térképekhez. 

A Project Operations kettős írású leképezései aktuális listájának és verzióinak felsorolását lásd: [Project Operations kettős írás leképezési verziói](../environment/resource-dual-write-maps.md).

A Project Operations Dataverse megoldás és a Finance megoldás verziójának frissítése során mindig futtassa a környezetben a leképezés legújabb verzióját, és engedélyezze az összes kapcsolódó táblaleképezést. Előfordulhat, hogy bizonyos funkciók és képességek nem működnek megfelelően, ha a térkép legújabb verziója nincs aktiválva. A térkép aktív verziója **Kettős írás** oldalon látható a **Verzió** oszlopban. Aktiválhatja a leképzés új verzióját a **Táblaleképezés verziója** lehetőség kiválasztásával, majd a legújabb verzió kiválasztásával, majd a kiválasztott verzió mentésével. Ha testreszabta az egyedi táblatérképet, újra kell alkalmaznia a módosításokat. További információért lásd: [Az alkalmazás életciklusának kezelése](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ha probléma merül fel a leképezés indítása során, kövesse a [Hiányzó táblaoszlopokkal kapcsolatos probléma a leképezésekben](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) részt a Kettős írás hibaelhárítási útmutatójában.

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2295625 | A mérföldkő nevét át kell másolni a számlatervből a számla sorának részletezésére. |
| Számlázás és árképzés | 2316323 | Az árengedmény nem szerkeszthető a proforma számlán a Project Operations-ben az erőforrásalapú forgatókönyvek esetében. |
|   Lehetőségkezelés | 2338619 | A **Lehetőség** és az **Ajánlat** üzleti szabályokat csak oldalakon lehet meghívni. |
| Erőforrás-kezelés | 2316523 | A szerepkörrel rendelkező erőforráskövetelményből történő **Kérelem küldése** nem jeleníthet meg hibát. |
| Erőforrás-kezelés | 2326885 | Az erőforrásigény létrehozása egy projekten keresztül nem jeleníthet meg hibát. |
| Idő és költség | 2335584 | Elavult feladatfolyamatok az időbejegyzésben. |
| Idő és költség | 2336884 | A **Hét másolása** időbejegyzés gombnak nem csak az aktuális felhasználó számára kell működnie. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance szolgáltatásban

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Utazás és költség | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Helytelen szállítói tranzakció és forgalmiadó-tranzakció összegek kerülnek könyvelésre, amikor egy hitelkártya-tranzakcióból költséget hoznak létre. |
| Utazás és költség | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | A rossz elszámolás a fizetési napló generálásakor létrehozott sorok. |
| Utazás és költség | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Helytelen forgalmiadó-tranzakcióösszegek kerülnek könyvelésre, amikor egy hitelkártya-tranzakcióból költséget hoznak létre. |
| Utazás és költség | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Egy költségsor törlése hosszú időt vehet igénybe. |
| Projekt könyvelése | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | A rendszer nem támogatja a folyamatos számsorrend beállítását, amikor a KB 4619395 KB alkalmazása után becslést ad fel. |
| Projekt könyvelése | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | A szállítói számla könyvelése a következő hibaüzenettel sikertelen lehet: „Az utalványon szereplő tranzakciók nem állnak egyensúlyban 2021. május 17-én. (számviteli pénznem: 0,00 - jelentési pénznem: 0,01)” |
