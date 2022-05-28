---
title: Újdonságok vagy változások a Project Service Automation 17-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 17-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 70749646f5b67db3cf868a6d9a83c14dc490793a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585094"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation 17-es frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.  Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 17-ös frissítési kiadásában. Ennek a verziónak a build száma V 3.10.5.28, és általánosan elérhető egy önálló frissítésben 2020 márciusában.


## <a name="update-release-17"></a>17-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Általános**

- Javítva: A Project Service Automation frissítése a csapattagok licencek kényszerítésére (a Project Resource Hub tartalmazza a Team Member Service terv metaadatait 3.x)
 
**Idő és költség**

- Javítva: Nem lehetséges egy költségbecslés nem lehetséges nem nulla árról nulla (0) árra. A módosítás mellőzve lett.

**Projektmenedzsment**

- Javítva: A nulla értékek ellenőrzése hozzá lett adva a csapattag beosztásának nevéhez.
- Javítva: az **msdyn_userresourceid** mező a **msdyn_resourceassignment** entitásban elavult.
- Javítva: A frissítés 2.x verzióról 3.x verzióra immár kezeli az üres ráfordításelosztásokat a feladat-hozzárendelésekhez.

**Sales**

- Javítva: az **Invoice.PreValidateInvoiceUpdate** most már kezeli a bejegyzések megfelelő ismételt hozzárendelésének forgatókönyvét.
- Javítva: Amikor a tranzakció osztálya **Idő**, a **UnitGroup** nem szerkeszthető minden entitásnál, beleértve a, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** és **ContractLineDetails** entitásokat. Azonban az **Egység** csak a **JournalLine** és a **InvoiceLineDetails** entitásokhoz nem szerkeszthető.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
