---
title: Project Service Automation konfigurálása
description: Lépések a Project Service testreszabásához
author: ruhercul
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002841"
---
# <a name="configure-project-service"></a><span data-ttu-id="efad2-103">A Project Service testreszabása</span><span class="sxs-lookup"><span data-stu-id="efad2-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="efad2-104">Mielőtt használhatná a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatizálási lehetőséget a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] rendszerben a partnerek, projektek és erőforrások kezeléséhez, el kell végezni néhány konfigurálási lépést, hogy a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] megoldás biztosan illeszkedjen a szervezet igényeihez.</span><span class="sxs-lookup"><span data-stu-id="efad2-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="efad2-105">Ezek a lépések a következők:</span><span class="sxs-lookup"><span data-stu-id="efad2-105">These steps include:</span></span>  
  
-   <span data-ttu-id="efad2-106">[Időegységek beállítása](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="efad2-107">Állítsa be a termékkatalógusban a projektek ütemezéséhez és számlázásához használatos időegységeket.</span><span class="sxs-lookup"><span data-stu-id="efad2-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="efad2-108">[Pénznemek és árfolyamok beállítása](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="efad2-109">Állítsa be a projektekhez használatos pénznemeket.</span><span class="sxs-lookup"><span data-stu-id="efad2-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="efad2-110">[Szervezeti egységek létrehozása](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="efad2-111">Állítsa be a vállalat által az üzleti tevékenységek elkülönítésére használt csoportokat, ezek lehetnek földrajzi, üzleti funkció szerinti vagy más logikai bontáson alapuló csoportosítások.</span><span class="sxs-lookup"><span data-stu-id="efad2-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="efad2-112">[Számlázási gyakoriságok beállítása](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="efad2-113">Állítsa be az ügyfelek felé történő számlázáshoz használatos időszakokat.</span><span class="sxs-lookup"><span data-stu-id="efad2-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="efad2-114">[Tranzakciókategóriák konfigurálása](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="efad2-115">Állítson be tranzakciókategóriákat tanácsadói számlázható és nem számlázható kiadásaihoz.</span><span class="sxs-lookup"><span data-stu-id="efad2-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="efad2-116">[Költségkategóriák konfigurálása](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="efad2-117">Állítson be kategóriákat tanácsadói számlázható és nem számlázható kiadásaihoz.</span><span class="sxs-lookup"><span data-stu-id="efad2-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="efad2-118">[Termékkatalógus elemek létrehozása](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="efad2-119">Adja hozzá a termékkatalógushoz az Ön által értékesített termékeket, például a szoftverlicencek.</span><span class="sxs-lookup"><span data-stu-id="efad2-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="efad2-120">[Árlista létrehozása](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="efad2-121">Állítson be különböző árlistákat, az alapján, hogy mekkora díjazást kíván felszámolni ügyfeleinek a projektjeikhez szükséges egyes szerepkörök után.</span><span class="sxs-lookup"><span data-stu-id="efad2-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="efad2-122">[Erőforrások beállítása](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="efad2-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="efad2-123">Adja hozzá a projektekhez szükséges képzettségeket, jártasságokat, erőforrás-szerepköröket és más, az erőforrásokra vonatkozó információkat.</span><span class="sxs-lookup"><span data-stu-id="efad2-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="efad2-124">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="efad2-124">See Also</span></span>  
 <span data-ttu-id="efad2-125">[Project Service Automation áttekintése](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="efad2-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="efad2-126">[Project Service Automation konfigurálása](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="efad2-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="efad2-127">[Partnerkezelői útmutató](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="efad2-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="efad2-128">[Projektmenedzseri útmutató](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="efad2-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="efad2-129">[Erőforrás-kezelői útmutató](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="efad2-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="efad2-130">Idő, Költségek és Együttműködési útmutató</span><span class="sxs-lookup"><span data-stu-id="efad2-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]