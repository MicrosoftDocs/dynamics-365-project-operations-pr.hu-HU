---
title: Project Service Automation konfigurálása
description: Lépések a Project Service testreszabásához
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752209"
---
# <a name="configure-project-service"></a><span data-ttu-id="a4dec-103">A Project Service testreszabása</span><span class="sxs-lookup"><span data-stu-id="a4dec-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a4dec-104">Mielőtt használhatná a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatizálási lehetőséget a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] rendszerben a partnerek, projektek és erőforrások kezeléséhez, el kell végezni néhány konfigurálási lépést, hogy a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] megoldás biztosan illeszkedjen a szervezet igényeihez.</span><span class="sxs-lookup"><span data-stu-id="a4dec-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="a4dec-105">Ezek a lépések a következők:</span><span class="sxs-lookup"><span data-stu-id="a4dec-105">These steps include:</span></span>  
  
-   <span data-ttu-id="a4dec-106">[Időegységek beállítása](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="a4dec-107">Állítsa be a termékkatalógusban a projektek ütemezéséhez és számlázásához használatos időegységeket.</span><span class="sxs-lookup"><span data-stu-id="a4dec-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="a4dec-108">[Pénznemek és árfolyamok beállítása](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="a4dec-109">Állítsa be a projektekhez használatos pénznemeket.</span><span class="sxs-lookup"><span data-stu-id="a4dec-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="a4dec-110">[Szervezeti egységek létrehozása](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="a4dec-111">Állítsa be a vállalat által az üzleti tevékenységek elkülönítésére használt csoportokat, ezek lehetnek földrajzi, üzleti funkció szerinti vagy más logikai bontáson alapuló csoportosítások.</span><span class="sxs-lookup"><span data-stu-id="a4dec-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="a4dec-112">[Számlázási gyakoriságok beállítása](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="a4dec-113">Állítsa be az ügyfelek felé történő számlázáshoz használatos időszakokat.</span><span class="sxs-lookup"><span data-stu-id="a4dec-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="a4dec-114">[Tranzakciókategóriák konfigurálása](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="a4dec-115">Állítson be tranzakciókategóriákat tanácsadói számlázható és nem számlázható kiadásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a4dec-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a4dec-116">[Költségkategóriák konfigurálása](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="a4dec-117">Állítson be kategóriákat tanácsadói számlázható és nem számlázható kiadásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a4dec-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a4dec-118">[Termékkatalógus elemek létrehozása](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="a4dec-119">Adja hozzá a termékkatalógushoz az Ön által értékesített termékeket, például a szoftverlicencek.</span><span class="sxs-lookup"><span data-stu-id="a4dec-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="a4dec-120">[Árlista létrehozása](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="a4dec-121">Állítson be különböző árlistákat, az alapján, hogy mekkora díjazást kíván felszámolni ügyfeleinek a projektjeikhez szükséges egyes szerepkörök után.</span><span class="sxs-lookup"><span data-stu-id="a4dec-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="a4dec-122">[Erőforrások beállítása](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="a4dec-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="a4dec-123">Adja hozzá a projektekhez szükséges képzettségeket, jártasságokat, erőforrás-szerepköröket és más, az erőforrásokra vonatkozó információkat.</span><span class="sxs-lookup"><span data-stu-id="a4dec-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a4dec-124">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="a4dec-124">See Also</span></span>  
 <span data-ttu-id="a4dec-125">[Project Service Automation áttekintése](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="a4dec-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="a4dec-126">[Project Service Automation konfigurálása](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="a4dec-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="a4dec-127">[Partnerkezelői útmutató](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a4dec-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="a4dec-128">[Projektmenedzseri útmutató](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a4dec-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="a4dec-129">[Erőforrás-kezelői útmutató](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a4dec-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="a4dec-130">Idő, Költségek és Együttműködési útmutató</span><span class="sxs-lookup"><span data-stu-id="a4dec-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
