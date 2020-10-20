---
title: A központi telepítés típusai
description: Ez a témakör a Project Operations az Ön vállalatának megfelelő telepítéstípusának megállapításában segítő információkat tartalmaz.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948908"
---
# <a name="deployment-types"></a>A központi telepítés típusai

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

> [!IMPORTANT]
> Miután megvásárolta a licencet, kezdje itt a Dynamics 365 Project Operations legjobb telepítési modelljének meghatározásával az [Irányított telepítési folyamat](https://aka.ms/provisionprojectoperations) használatával.
> Miután befejezte az Irányított telepítési folyamatot, a rendszer a helyes felügyeleti portálra irányítja a telepítés befejezéséhez. A telepítés befejezéséhez tekintse meg a telepítés alábbi részleteit.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>A Dynamics meglévő Dynamics 365 Project Service Automation rendszert használó ügyfelei
A Project Operations a Project Service Automation szolgáltatással szállított képességeket tartalmazza. A jövőben ezen ügyfelek számára egy frissítési elérési út kerül kiadásra

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>A Dynamics 365 Finance Projektmenedzsment és könyvelés alkalmazást használó meglévő ügyfelei 

A Finance Projektmenedzsment és könyvelés funkciót használó meglévő ügyfelei továbbra is használhatják azt. Lásd: [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma).

A Project Operations több telepítési lehetőséget is támogat, hogy megfeleljen az igényeinek. Akár új, akár meglévő Dynamics 365-ügyfél, a Project Operations képes támogatni az igényeit.

A [telepítési kérdőívünk](https://aka.ms/provisionprojectoperations) segítséget nyújt a megfelelő telepítés meghatározásában. Az eredmények a következő telepítési típusok egyike felé irányítják:

- [Egyszerű telepítés – proforma számlázás](#lite)
- [Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez](#integrated)
- [Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez](#pma)

A Project Operations a készletalapú/gyártási megrendeléseken alapuló forgatókönyveket és a nem készletalapú/erőforrásalapú forgatókönyveket támogatja ugyanazon környezetben, jogientitás-szintű konfigurációkon keresztül. A Contoso például az amerikai gyártói létesítményben (jogi entitás = Contoso Manufacturing United States) készletalapú/gyártási megrendeléseken alapuló képességeket, az Egyesült Királyságban található Contoso Robotics Arms szervizüzemben (jogi entitás = Contoso Robotics United Kingdom) pedig nem készletalapú/erőforrásalapú képességeket használhat.

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Egyszerű telepítés – proforma számlázás
A Lite telepítés a következő lehetőségeket tartalmazza:

- Projekttervezés a Microsoft Webes projekt segítségével
- Többdimenziós árképzés
- Egyesített erőforrás-kezelés
- Időkövetés
- Alapvető költség
- Számlajavaslat

### <a name="deployment-steps"></a>Telepítési lépések:
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](lite-preview-subscription-sign-up.md) és az [Új környezet kiépítése](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Projekt Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez
A Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekhez az alábbi képességeket tartalmazza:
  
- Projekttervezés a Microsoft Webes projekt segítségével
- Többdimenziós árképzés
- Egyesített erőforrás-kezelés
- Időkövetés
- Alapvető költség
- Teljes költség
- Bizonylat OCR
- Teljes számlázás
- Bevételfelismerés

### <a name="deployment-steps"></a>Telepítési lépések:
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](resource-sign-up-preview-subscription.md) és az [Új környezet kiépítése](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Projekt Operations készletalapú vagy gyártási megrendeléseken alapuló forgatókönyvekhez

- Projekt tervezése WBS használatával
- Erőforráskezelés
- Időkövetés
- Teljes költség
- Bizonylat OCR
- Teljes számlázás
- Bevételfelismerés
- Termelési rendelések
- Anyagok támogatása

### <a name="deployment-steps"></a>Telepítési lépések:
Határozza meg a Project Operations legjobb telepítési modelljét a [telepítési kérdőív](https://aka.ms/provisionprojectoperations) használatával.

Ehhez a telepítéshez lásd: [Regisztráció az előzetes verziós előfizetésekre](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) és az [Új környezet kiépítése](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



