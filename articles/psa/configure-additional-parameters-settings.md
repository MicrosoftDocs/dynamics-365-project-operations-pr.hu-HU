---
title: Kiegészítő paraméter beállításainak konfigurálása
description: További paraméterbeállítások testreszabása a Project Service szolgáltatásban
author: JohnPBurrows
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
ms.openlocfilehash: 75fe0aab8ea8bf41fcb98f4318380c93ac52fef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919235"
---
# <a name="configure-additional-parameter-settings-project-service"></a>További paraméterbeállítások testreszabása (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ha az elemeket már korábbi cikkeknél konfigurálta, további projektparamétereket kell beállítania a projektek használatához. Amikor először telepítette a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programot, létrehozott egy paraméterbeállítást, amely elsőként minden rekordot a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] munkára hoz létre. Most itt az ideje, hogy visszamenjen és elvégezze a további mezők testreszabását ezekhez a beállításokhoz.  
  
 Az alábbi beállításokat kell elvégeznie:  
  
-   Szervezeti egység  
  
-   Számlázási gyakoriság  
  
-   Munkaidősablonok  
  
-   Árlista  
 
Ebben a lépésben adhatja meg, hogy milyen típusú erőforrás-elosztást szeretne:  
  
- **Központi**. Csak az erőforrás-kezelők tudják kijelölni a projektek erőforrásait.  
  
- **Hibrid**. Az erőforrás-menedzserek, projektmenedzserek és partnerkezelők oszthatják el az erőforrásokat a projektek között.  
  
 
A projektparaméterek beállításához:  
  
1. Lépjen a **Project Service > Paraméterek** pontba.  
  
2. Kattintson arra a paraméterbeállításra, amelyet konfigurálni akar (amelyet az alábbi program első telepítésekor létrehozott: [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), vagy kattintson az **Új** lehetőségre, új beállítás létrehozásához.  
  
3. Az **Általános** területen állítsa be a lehetőségeket projektparamétereinek megfelelően.  
  
4. Az **Árlista** területen kattintson a **+** lehetőségre árlista hozzáadásához, válasszon egy árlistát a **Projektparaméter árlista** legördülő listából, majd kattintson a **Mentés** lehetőségre.  
  
5. Kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.  

> [!NOTE]
> Ahhoz, hogy a Project Service megfelelően működjön a projekt paraméterrekordját karban kell tartani. Ez a bejegyzést nem szabad törölni.

### <a name="see-also"></a>Kapcsolódó információk  
 [Erőforrások beállítása](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
