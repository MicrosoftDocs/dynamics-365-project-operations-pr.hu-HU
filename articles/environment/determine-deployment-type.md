---
title: A telepítés típusának meghatározása
description: Ez a cikk a Project Operations az Ön vállalatának megfelelő telepítéstípusának megállapításában segítő információkat tartalmaz.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912197"
---
# <a name="determine-your-deployment-type"></a>A telepítés típusának meghatározása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

> [!IMPORTANT]
> A licenc vásárlása után kezdje el itt meghatározni a Dynamics 365 Project Operations központi telepítési modelljét az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.
> Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez. A telepítés befejezéséhez tekintse meg a telepítés részleteit.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei
A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza. A frissítés elérési úta 2021-es 1 kiadási hullámban jelennek meg az ügyfelek számára.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei 

A projektmenedzsment és-számlázási funkciót használó meglévő Finance ügyfelek továbbra is használhatják azt. Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).


## <a name="deployment-regions"></a>Központi telepítési régiók
Annak meghatározásához, hogy mely régiók támogatják a Project Operations központi telepítlését, lásd: [Földrajzi elérhetőség a Dynamics 365 és a Power Platform jelentés esetében](https://dynamics.microsoft.com/en-us/geographic-availability/). Válassza a **Jelentés megtekintése** lehetőséget, majd a támogatott régiók megtekintéséhez bontsa ki a **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** alkalmazást.

## <a name="deployment-types"></a>A központi telepítés típusai
A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek. Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.

A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában. Az eredmények a következő telepítési típusok egyike felé irányítják:

- [Egyszerű telepítés – proforma számlázás](#lite)
- [Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez](#integrated)
- [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma)

A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül. A Contoso például az Egyesült államokbeli gyártási létesítményben a készletezett/termelési rendelés funkcióit használhatja (Jogi személy = Contoso Manufacturing United States). A Contoso a nem készletezett/erőforrás alapú lehetőségeket használhatja a Contoso Robotics Arms karbantartási létesítményében az Egyesült Királyságban (a jogi személy = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Egyszerű telepítés – proforma számlázás

A Lite telepítés a következő lehetőségeket tartalmazza:

- A Dynamics 365 Sales alkalmazás tapasztalatait kibővítő projektek Értékesítési folyamata
- Projekttervezés a Microsoft Webes projekt segítségével
- Többdimenziós árképzés
- Egyesített erőforrás-kezelés
- Időkövetés
- Alapvető költség
- Proforma számlázás a Projektmenedzser általi ellenőrzéshez és szerkesztésekhez 

#### <a name="deployment-steps"></a>Központi telepítési lépések
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:
 
- A Dynamics 365 Sales alkalmazást kibővítő projektek Értékesítési folyamata
- Projekttervezés a Microsoft Webes projekt segítségével
- Többdimenziós árképzés
- Egyesített erőforrás-kezelés
- Időkövetés
- Alapvető költség
- Teljes költség
- Bizonylat OCR
- Proforma és az ügyfél felé irányuló számlázás 
- Bevétel elszámolása projektekhez

#### <a name="deployment-steps"></a>Központi telepítési lépések
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez

- Projekt tervezése WBS használatával
- Erőforrás-kezelés
- Időkövetés
- Teljes költség
- Bizonylat OCR
- Teljes számlázás
- Bevételelszámolás
- Termelési rendelések
- Készletezett anyagok támogatása készlettel

#### <a name="deployment-steps"></a>Központi telepítési lépések
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) és az [Új környezet kiépítése](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]