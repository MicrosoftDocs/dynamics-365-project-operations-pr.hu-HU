---
title: A Project Finder Mobile alkalmazás engedélyezése
description: A Project Finder Mobile alkalmazás funkcióinak engedélyezése a Project Service szolgáltatásban
author: JohnPBurrows
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 3f8f23c1f32d94a514de9ae40bd07b3d8063824c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593688"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>A Project Finder Mobile alkalmazás funkcióinak engedélyezése (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Erőforrásai a telefonjukon a Project Finder Mobile alkalmazás és a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segítségével találhatják meg az új projekteket, illetve frissíthetik és alakíthatják készségeiket.  
  
 Az alkalmazás elérhető [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefon és [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] készülékekre.  
    
 Ahhoz, hogy a felhasználók megtekinthessék a projekt erőforráskövetelményeit, és frissíthessék készségeiket, be kell állítani néhány lehetőséget szervezeti egysége paraméterbeállításainál.
  
> [!NOTE]
>  A Project Finder Mobile alkalmazás csak a [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] rendszerrel működik együtt, a helyszíni telepítésekkel nem.  
  
1. Lépjen a **Project Service > Paraméterek** pontba.  
  
2. Kattintson a Project Finder Mobile alkalmazás funkcióinak engedélyezéséhez használni kívánt paraméterbeállításokra.  
  
3. Az **Általános** területen állítsa be az **Erőforrás-követelmények láthatók az erőforrások számára** lehetőségnél az **Igen** beállítást.  
  
4. Állítsa be a **Képességek módosításának engedélyezése az erőforrásoknak** lehetőségnél az **Igen** beállítást.  
  
   ![ProjectService&#95; ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ez egy globális beállítás. A projektvezetők beállíthatják az egyes projektek esetében, hogy azok láthatók legyenek-e más projektek **Projektcsapat** oldalán.  
  
   ![ProjectService&#95; ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mail-értesítések  
 A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] az alábbi címzettek és az alábbi időpontokban küld e-maileket erőforrás-kérelmekkel kapcsolatban:  
  
|Címzett|Esemény|  
|---------------|-----------|  
|Projektvezető|- Egy erőforrás feliratkozik egy projektre a Project Finder Mobile alkalmazás segítségével.|  
|Erőforrás|- Egy másik erőforrás már teljesítette a projektmunkát, amelyre az erőforrás feliratkozott.<br />- A készségjóváhagyási kérelmüket elfogadták vagy visszautasították.<br />- A projektfeliratkozási kérelmüket elfogadták vagy visszautasították.|  
  
## <a name="privacy-notice"></a>Adatvédelmi nyilatkozat  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Erőforrások beállítása](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
