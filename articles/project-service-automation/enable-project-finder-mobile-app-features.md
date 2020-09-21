---
title: A Project Finder Mobile alkalmazás engedélyezése
description: A Project Finder Mobile alkalmazás funkcióinak engedélyezése a Project Service szolgáltatásban
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752160"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>A Project Finder Mobile alkalmazás funkcióinak engedélyezése (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Erőforrásai a telefonjukon a Project Finder Mobile alkalmazás és a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segítségével találhatják meg az új projekteket, illetve frissíthetik és alakíthatják készségeiket.  
  
 Az alkalmazás elérhető [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefon és [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] készülékekre.  
  
 Be kell állítani néhány opciót szervezeti egysége paraméterbeállításainál, hogy a felhasználók megtekinthessék a projektek erőforráskövetelményeit, és frissíthessék készségeiket.  
  
> [!NOTE]
>  A Project Finder Mobile alkalmazás csak a [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] rendszerrel működik együtt, a helyszíni telepítésekkel nem.  
  
1. Lépjen a **Project Service > Paraméterek** pontba.  
  
2. Kattintson a Project Finder Mobile alkalmazás funkcióinak engedélyezéséhez használni kívánt paraméterbeállításokra.  
  
3. Az **Általános** területen állítsa be az **Erőforrás-követelmények láthatók az erőforrások számára** lehetőségnél az **Igen** beállítást.  
  
4. Állítsa be a **Képességek módosításának engedélyezése az erőforrásoknak** lehetőségnél az **Igen** beállítást.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ez egy globális beállítás. A projektvezetők beállíthatják az egyes projektek esetében, hogy azok láthatók legyenek-e más projektek **Projektcsapat** oldalán.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mail-értesítések  
 A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] az alábbi címzettek és az alábbi időpontokban küld e-maileket erőforrás-kérelmekkel kapcsolatban:  
  
|Címzett|Esemény|  
|---------------|-----------|  
|Projektvezető|-   Amikor egy erőforrás regisztrál egy projektre a Project Finder Mobile alkalmazás segítségével.|  
|Erőforrás|-   Ha egy másik erőforrás már teljesítette a projektmunkát, amelyre az erőforrás regisztrált.<br />-   Ha a készségjóváhagyási kérelmüket elfogadták vagy visszautasították.<br />-   Ha a projektregisztrálási kérelmüket elfogadták vagy visszautasították.|  
  
## <a name="privacy-notice"></a>Adatvédelmi nyilatkozat  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Erőforrások beállítása](../project-service/set-up-resources.md)
