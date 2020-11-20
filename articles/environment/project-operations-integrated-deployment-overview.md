---
title: Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén – telepítési útmutató
description: Ez a témakör a telepítés típusával, az erőforrás-/nem készletalapú forgatókönyvekkel kapcsolatos Project Operations kapcsolatos információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365503"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="d6b9d-103">Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén – telepítési útmutató</span><span class="sxs-lookup"><span data-stu-id="d6b9d-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="d6b9d-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="d6b9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d6b9d-105">A telepítés típusa, a Dynamics 365 Project Operations az erőforrás-/nem készletalapú esetekhez a következő lehetőségeket nyújtja a projektalapú cégek számára:</span><span class="sxs-lookup"><span data-stu-id="d6b9d-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="d6b9d-106">Projekttervezés a Microsoft Webes projekt segítségével</span><span class="sxs-lookup"><span data-stu-id="d6b9d-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d6b9d-107">Többdimenziós árazás és költségszámítás a munkaerő-erőforrások számára</span><span class="sxs-lookup"><span data-stu-id="d6b9d-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="d6b9d-108">Kategória alapú árazás a kiadáskategóriákhoz</span><span class="sxs-lookup"><span data-stu-id="d6b9d-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="d6b9d-109">Projektalapú értékesítések kezelése a Dynamics 365 Sales lehetőségeivel</span><span class="sxs-lookup"><span data-stu-id="d6b9d-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="d6b9d-110">Universal Resource Scheduling, amely a többi alkalmazással integrálható, pl. Dynamics 365 Field Service ás Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="d6b9d-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="d6b9d-111">A projektek előrehaladása és az idő nyomon követése</span><span class="sxs-lookup"><span data-stu-id="d6b9d-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="d6b9d-112">A projektek és a projekten kívüli kiadások alapvető és teljes körű költségkezelési tapasztalatai az OCR-funkció segítségével végzett nyugtarögzítéssel együtt</span><span class="sxs-lookup"><span data-stu-id="d6b9d-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="d6b9d-113">Proformától az ügyfélnek kiállított számláig terjedő számlázás, amelyet nagyvállalati szintű áfa- és érvényességi dátumon alapuló árfolyamrendszer támogat.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="d6b9d-114">Konfigurálható projektköltség, bevételprofilok és termelésben lévő munka (WIP) könyvelésére és elhatárolására vonatkozó szabályok</span><span class="sxs-lookup"><span data-stu-id="d6b9d-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="d6b9d-115">Projektbevétel elszámolása</span><span class="sxs-lookup"><span data-stu-id="d6b9d-115">Project revenue recognition</span></span>
- <span data-ttu-id="d6b9d-116">Bővíthetőség a Power Platform segítségével</span><span class="sxs-lookup"><span data-stu-id="d6b9d-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="d6b9d-117">Ez a telepítési típus bővítmény biztosít a Dynamics 365 Finance és a Dynamics 365 Supply Chain Management alkalmazások által biztosított funkciókhoz.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="d6b9d-118">Ezt a telepítést úgy kell megválasztani, hogy a Project Operations várhatóan a teljes projekt életciklusát használják, amely a következő követelményeket tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="d6b9d-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="d6b9d-119">A projekten alapuló értékesítések más típusú értékesítéssel való kezelésének lehetősége a Sales alkalmazásban szereplő lehetőségek segítségével.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="d6b9d-120">Integrált projektmenedzsment-rendszer, amely a belső és a számlázható projekteket kezeli a projekt értékesítéstől a könyvelésig történő ütemezése és pénzügyei szempontjából.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="d6b9d-121">Költségkezelési rendszer, amely a projekthez tartozó és a projekten kívüli költségekre vonatkozó házirend-kikényszerítést és visszatérítéseket is lehetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="d6b9d-122">Adatokban gazdag, nagyvállalati szintű áfa- és átváltásiárfolyam-kezelő rendszerre van hozzá szükség, amely a projektekre vonatkozóan ügyfeleknek kiállított számlákat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="d6b9d-123">Egy Nemzetközi Pénzügyi Beszámolási Standardoknak (IFRS) megfelelő projektkönyvelési és bevételelszámolási rendszer.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="d6b9d-124">Pénzügyi vagy ellátásilánc-kezelési alkalmazások és a projektalapú tranzakciók integrációja.</span><span class="sxs-lookup"><span data-stu-id="d6b9d-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
