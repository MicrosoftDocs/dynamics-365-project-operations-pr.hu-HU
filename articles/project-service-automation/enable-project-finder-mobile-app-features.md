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
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="764c3-103">A Project Finder Mobile alkalmazás funkcióinak engedélyezése (Project Service)</span><span class="sxs-lookup"><span data-stu-id="764c3-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="764c3-104">Erőforrásai a telefonjukon a Project Finder Mobile alkalmazás és a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] segítségével találhatják meg az új projekteket, illetve frissíthetik és alakíthatják készségeiket.</span><span class="sxs-lookup"><span data-stu-id="764c3-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="764c3-105">Az alkalmazás elérhető [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefon és [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] készülékekre.</span><span class="sxs-lookup"><span data-stu-id="764c3-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="764c3-106">Be kell állítani néhány opciót szervezeti egysége paraméterbeállításainál, hogy a felhasználók megtekinthessék a projektek erőforráskövetelményeit, és frissíthessék készségeiket.</span><span class="sxs-lookup"><span data-stu-id="764c3-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="764c3-107">A Project Finder Mobile alkalmazás csak a [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] rendszerrel működik együtt, a helyszíni telepítésekkel nem.</span><span class="sxs-lookup"><span data-stu-id="764c3-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="764c3-108">Lépjen a **Project Service > Paraméterek** pontba.</span><span class="sxs-lookup"><span data-stu-id="764c3-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="764c3-109">Kattintson a Project Finder Mobile alkalmazás funkcióinak engedélyezéséhez használni kívánt paraméterbeállításokra.</span><span class="sxs-lookup"><span data-stu-id="764c3-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="764c3-110">Az **Általános** területen állítsa be az **Erőforrás-követelmények láthatók az erőforrások számára** lehetőségnél az **Igen** beállítást.</span><span class="sxs-lookup"><span data-stu-id="764c3-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="764c3-111">Állítsa be a **Képességek módosításának engedélyezése az erőforrásoknak** lehetőségnél az **Igen** beállítást.</span><span class="sxs-lookup"><span data-stu-id="764c3-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="764c3-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="764c3-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="764c3-113">Ez egy globális beállítás.</span><span class="sxs-lookup"><span data-stu-id="764c3-113">This is a global setting.</span></span> <span data-ttu-id="764c3-114">A projektvezetők beállíthatják az egyes projektek esetében, hogy azok láthatók legyenek-e más projektek **Projektcsapat** oldalán.</span><span class="sxs-lookup"><span data-stu-id="764c3-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="764c3-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="764c3-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="764c3-116">E-mail-értesítések</span><span class="sxs-lookup"><span data-stu-id="764c3-116">Email notifications</span></span>  
 <span data-ttu-id="764c3-117">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] az alábbi címzettek és az alábbi időpontokban küld e-maileket erőforrás-kérelmekkel kapcsolatban:</span><span class="sxs-lookup"><span data-stu-id="764c3-117">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="764c3-118">Címzett</span><span class="sxs-lookup"><span data-stu-id="764c3-118">Recipient</span></span>|<span data-ttu-id="764c3-119">Esemény</span><span class="sxs-lookup"><span data-stu-id="764c3-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="764c3-120">Projektvezető</span><span class="sxs-lookup"><span data-stu-id="764c3-120">Project manager</span></span>|<span data-ttu-id="764c3-121">-   Amikor egy erőforrás regisztrál egy projektre a Project Finder Mobile alkalmazás segítségével.</span><span class="sxs-lookup"><span data-stu-id="764c3-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="764c3-122">Erőforrás</span><span class="sxs-lookup"><span data-stu-id="764c3-122">Resource</span></span>|<span data-ttu-id="764c3-123">-   Ha egy másik erőforrás már teljesítette a projektmunkát, amelyre az erőforrás regisztrált.</span><span class="sxs-lookup"><span data-stu-id="764c3-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="764c3-124">-   Ha a készségjóváhagyási kérelmüket elfogadták vagy visszautasították.</span><span class="sxs-lookup"><span data-stu-id="764c3-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="764c3-125">-   Ha a projektregisztrálási kérelmüket elfogadták vagy visszautasították.</span><span class="sxs-lookup"><span data-stu-id="764c3-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="764c3-126">Adatvédelmi nyilatkozat</span><span class="sxs-lookup"><span data-stu-id="764c3-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="764c3-127">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="764c3-127">See Also</span></span>  
 [<span data-ttu-id="764c3-128">Erőforrások beállítása</span><span class="sxs-lookup"><span data-stu-id="764c3-128">Set up resources</span></span>](../project-service/set-up-resources.md)
