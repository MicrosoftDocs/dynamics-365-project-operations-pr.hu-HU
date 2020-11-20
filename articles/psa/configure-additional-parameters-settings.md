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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129366"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="73a43-103">További paraméterbeállítások testreszabása (Project Service)</span><span class="sxs-lookup"><span data-stu-id="73a43-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="73a43-104">Ha az elemeket már korábbi témaköröknél konfigurálta, további projektparamétereket kell beállítania a projektek használatához.</span><span class="sxs-lookup"><span data-stu-id="73a43-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="73a43-105">Amikor először telepítette a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] programot, létrehozott egy paraméterbeállítást, amely elsőként minden rekordot a(z) [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] munkára hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73a43-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="73a43-106">Most itt az ideje, hogy visszamenjen és elvégezze a további mezők testreszabását ezekhez a beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="73a43-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="73a43-107">Az alábbi beállításokat kell elvégeznie:</span><span class="sxs-lookup"><span data-stu-id="73a43-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="73a43-108">Szervezeti egység</span><span class="sxs-lookup"><span data-stu-id="73a43-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="73a43-109">Számlázási gyakoriság</span><span class="sxs-lookup"><span data-stu-id="73a43-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="73a43-110">Munkaidősablonok</span><span class="sxs-lookup"><span data-stu-id="73a43-110">Work hours template</span></span>  
  
-   <span data-ttu-id="73a43-111">Árlista</span><span class="sxs-lookup"><span data-stu-id="73a43-111">Price list</span></span>  
 
<span data-ttu-id="73a43-112">Ebben a lépésben adhatja meg, hogy milyen típusú erőforrás-elosztást szeretne:</span><span class="sxs-lookup"><span data-stu-id="73a43-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="73a43-113">**Központi**.</span><span class="sxs-lookup"><span data-stu-id="73a43-113">**Central**.</span></span> <span data-ttu-id="73a43-114">Csak az erőforrás-kezelők tudják kijelölni a projektek erőforrásait.</span><span class="sxs-lookup"><span data-stu-id="73a43-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="73a43-115">**Hibrid**.</span><span class="sxs-lookup"><span data-stu-id="73a43-115">**Hybrid**.</span></span> <span data-ttu-id="73a43-116">Az erőforrás-menedzserek, projektmenedzserek és partnerkezelők oszthatják el az erőforrásokat a projektek között.</span><span class="sxs-lookup"><span data-stu-id="73a43-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="73a43-117">A projektparaméterek beállításához:</span><span class="sxs-lookup"><span data-stu-id="73a43-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="73a43-118">Lépjen a **Project Service > Paraméterek** pontba.</span><span class="sxs-lookup"><span data-stu-id="73a43-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="73a43-119">Kattintson arra a paraméterbeállításra, amelyet konfigurálni akar (amelyet az alábbi program első telepítésekor létrehozott: [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), vagy kattintson az **Új** lehetőségre, új beállítás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="73a43-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="73a43-120">Az **Általános** területen állítsa be a lehetőségeket projektparamétereinek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="73a43-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="73a43-121">Az **Árlista** területen kattintson a **+** lehetőségre árlista hozzáadásához, válasszon egy árlistát a **Projektparaméter árlista** legördülő listából, majd kattintson a **Mentés** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="73a43-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="73a43-122">Kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.</span><span class="sxs-lookup"><span data-stu-id="73a43-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="73a43-123">Ahhoz, hogy a Project Service megfelelően működjön a projekt paraméterrekordját karban kell tartani.</span><span class="sxs-lookup"><span data-stu-id="73a43-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="73a43-124">Ez a bejegyzést nem szabad törölni.</span><span class="sxs-lookup"><span data-stu-id="73a43-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="73a43-125">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="73a43-125">See Also</span></span>  
 [<span data-ttu-id="73a43-126">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="73a43-126">Set up resources</span></span>](../psa/set-up-resources.md)
