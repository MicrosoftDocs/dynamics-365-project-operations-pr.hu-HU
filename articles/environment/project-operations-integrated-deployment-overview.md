---
title: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén – telepítési útmutató
description: Ez a témakör a telepítés típusával, az erőforrás-/nem készletalapú forgatókönyvekkel kapcsolatos Project Operations kapcsolatos információkat tartalmaz.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 3648bf6c5e00fe701f309392bd09819f84bf574d
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368704"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="150d6-103">Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén – telepítési útmutató</span><span class="sxs-lookup"><span data-stu-id="150d6-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="150d6-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="150d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="150d6-105">A telepítés típusa, a Dynamics 365 Project Operations az erőforrás-/nem készletalapú esetekhez a következő lehetőségeket nyújtja a projektalapú cégek számára:</span><span class="sxs-lookup"><span data-stu-id="150d6-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="150d6-106">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="150d6-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="150d6-107">Többdimenziós árazás és költségszámítás a munkaerő-erőforrások számára</span><span class="sxs-lookup"><span data-stu-id="150d6-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="150d6-108">Kategória alapú árazás a kiadáskategóriákhoz</span><span class="sxs-lookup"><span data-stu-id="150d6-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="150d6-109">Projektalapú értékesítések kezelése a Dynamics 365 Sales lehetőségeivel</span><span class="sxs-lookup"><span data-stu-id="150d6-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="150d6-110">Universal Resource Scheduling, amely a többi alkalmazással integrálható, pl. Dynamics 365 Field Service ás Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="150d6-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="150d6-111">A projektek előrehaladása és az idő nyomon követése</span><span class="sxs-lookup"><span data-stu-id="150d6-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="150d6-112">A projektek és a projekten kívüli kiadások alapvető és teljes körű költségkezelési tapasztalatai az OCR-funkció segítségével végzett nyugtarögzítéssel együtt</span><span class="sxs-lookup"><span data-stu-id="150d6-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="150d6-113">Proformától az ügyfélnek kiállított számláig terjedő számlázás, amelyet nagyvállalati szintű áfa- és érvényességi dátumon alapuló árfolyamrendszer támogat.</span><span class="sxs-lookup"><span data-stu-id="150d6-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="150d6-114">Konfigurálható projektköltség, bevételprofilok és termelésben lévő munka (WIP) könyvelésére és elhatárolására vonatkozó szabályok</span><span class="sxs-lookup"><span data-stu-id="150d6-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="150d6-115">Projektbevétel elszámolása</span><span class="sxs-lookup"><span data-stu-id="150d6-115">Project revenue recognition</span></span>
- <span data-ttu-id="150d6-116">Bővíthetőség a Power Platform segítségével</span><span class="sxs-lookup"><span data-stu-id="150d6-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="150d6-117">Ez a telepítési típus bővítmény biztosít a Dynamics 365 Finance és a Dynamics 365 Supply Chain Management alkalmazások által biztosított funkciókhoz.</span><span class="sxs-lookup"><span data-stu-id="150d6-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="150d6-118">Ezt a telepítést úgy kell megválasztani, hogy a Project Operations várhatóan a teljes projekt életciklusát használják, amely a következő követelményeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="150d6-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="150d6-119">A projekten alapuló értékesítések más típusú értékesítéssel való kezelésének lehetősége a Sales alkalmazásban szereplő lehetőségek segítségével.</span><span class="sxs-lookup"><span data-stu-id="150d6-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="150d6-120">Integrált projektmenedzsment-rendszer, amely a belső és a számlázható projekteket kezeli a projekt értékesítéstől a könyvelésig történő ütemezése és pénzügyei szempontjából.</span><span class="sxs-lookup"><span data-stu-id="150d6-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="150d6-121">Költségkezelési rendszer, amely a projekthez tartozó és a projekten kívüli költségekre vonatkozó házirend-kikényszerítést és visszatérítéseket is lehetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="150d6-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="150d6-122">Adatokban gazdag, nagyvállalati szintű áfa- és átváltásiárfolyam-kezelő rendszerre van hozzá szükség, amely a projektekre vonatkozóan ügyfeleknek kiállított számlákat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="150d6-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="150d6-123">Egy Nemzetközi Pénzügyi Beszámolási Standardoknak (IFRS) megfelelő projektkönyvelési és bevételelszámolási rendszer.</span><span class="sxs-lookup"><span data-stu-id="150d6-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="150d6-124">Pénzügyi vagy ellátásilánc-kezelési alkalmazások és a projektalapú tranzakciók integrációja.</span><span class="sxs-lookup"><span data-stu-id="150d6-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]