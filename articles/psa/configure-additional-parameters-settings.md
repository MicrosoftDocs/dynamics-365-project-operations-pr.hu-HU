---
title: Kiegészítő paraméter beállításainak konfigurálása
description: További paraméterbeállítások testreszabása a Project Service szolgáltatásban
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151571"
---
# <a name="configure-additional-parameter-settings-project-service"></a>További paraméterbeállítások testreszabása (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ha az elemeket már korábbi témaköröknél konfigurálta, további projektparamétereket kell beállítania a projektek használatához. Amikor először telepítette a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programot, létrehozott egy paraméterbeállítást, amely elsőként minden rekordot a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] munkára hoz létre. Most itt az ideje, hogy visszamenjen és elvégezze a további mezők testreszabását ezekhez a beállításokhoz.  
  
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