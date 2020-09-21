---
title: Munkabecslések biztosítása egy projekthez az értékesítési folyamat során
description: Munkabecslések biztosítása egy projekthez az értékesítési folyamat során a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752283"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Munkabecslések biztosítása egy projekthez az értékesítési folyamat során (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Az értékesítési folyamat során teljesen új értékesítési becsléseket dolgozhat ki árajánlatsorokkal. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] képességeinek a(z) [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] tudományosabb és determinisztikusabb módon készíthetők értékesítési becslések a munkatételek lebontásával és a projektbecslések szempontjából lényeges attribútumok társításával a munkalebontási struktúrában.  
  
 Az értékesítés elnyerését követően használhatja a társított munkalebontási struktúrát a projekttervben, hogy szükség szerint finomítsa azt a projekt sikeres kivitelezése érdekében.  
  
## <a name="link-a-project-to-a-quote-line"></a>Egy projekt árajánlatsorhoz kapcsolása  
 Egy projektalapú árajánlatsor létrehozásakor létrehozhat új projektet az árajánlatsorból. Ekkor használhat projektsablonokat, amelyek vagy előre konfigurált, a szervezetében gyakori, szabványos projektterv és a pénzügyi becslések vagy egy korábbi projektből származó projektterv és becslések másolata. Egy projekt létrehozásakor a projektsablon kiválasztása biztosít alapot a projektterv, a becslések és a szerepkör-követelmények finomításához. Ha árajánlatból hoz létre projektet, akkor a rendszer automatikusan társítja a projektet az árajánlatsorhoz.  
  
## <a name="project-estimate-components"></a>Projektbecslések összetevői  
 A projekt munkalebontási struktúrája segítségével bontható a munka feladatokra, tartható fent a feladatok hierarchiája, és társítható egy becslés az egyes feladatokhoz az elvégzésükhöz szükséges ráfordításról. Továbbá társíthat szerepköröket is egy feladathoz, így megadva egy becslést az erőforrás-típusra vonatkozóan, amelyre szükség van a feladat és az ütemterv befejezéséhez.  
  
 A munkalebontási struktúra segít meghatározni a munkaráfordítást és ütemezni a becsléseket. Alapértelmezés szerint a projekt korábban meghatározott alapértelmezett árlistákat használja. Az árlistákban meghatározott önköltségi és értékesítési árak segítenek meghatározni a pénzügyi becsléseket a projekt munkalebontásához.  
  
 Ha a projekthez egy árajánlat társul, és az árajánlat az alapértelmezettől eltérő árlistával rendelkezik, akkor az árajánlat árlistáját használja a rendszer a pénzügyi becslésekhez.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Becslések importálása egy projektből egy árajánlatba  
 Ha rendelkezik projektbecslésekkel a projektben, akkor importálhatja ezeket a becsléseket az árajánlatsorba:  
  
-   Az **Árajánlatsor részletei** részben kattintson az **Importálás becslésekből** lehetőségre. 

-   Válassza ki, hogy a projektbecslések importálásakor az összegzés a tranzakciótípus, a szerepkör vagy a munkalebontási struktúra csomópontszintje alapján történjen.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Projektmenedzseri útmutató](../project-service/project-manager-guide.md)
