---
title: Project Operations készleten vagy gyártáson alapuló forgatókönyvek esetén – telepítési útmutató
description: Ez a témakör a telepítés típusával, a készletezett/előállítási forgatókönyvekkel kapcsolatos Project Operations kapcsolatos információkat tartalmaz.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b2a606bc587b99c16d45b19689ba90b422c3c62
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999404"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="6b9df-103">Project Operations készleten vagy gyártáson alapuló forgatókönyvek esetén – telepítési útmutató</span><span class="sxs-lookup"><span data-stu-id="6b9df-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="6b9df-104">_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_</span><span class="sxs-lookup"><span data-stu-id="6b9df-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="6b9df-105">Ez a telepítési típus a következő lehetőségeket nyújtja a Projektalapú cégek számára:</span><span class="sxs-lookup"><span data-stu-id="6b9df-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="6b9df-106">Projekttervezés a [munkalebontási struktúrák](work-breakdown-structures.md) használatával</span><span class="sxs-lookup"><span data-stu-id="6b9df-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="6b9df-107">A készletezett készletek beszerzése és felhasználása projektekhez</span><span class="sxs-lookup"><span data-stu-id="6b9df-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="6b9df-108">A projektalapú értékesítések kezelése a Dynamics 365 Finance and Operations alkalmazások **Értékesítés és marketing** moduljának használatával</span><span class="sxs-lookup"><span data-stu-id="6b9df-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="6b9df-109">A projektek árazása és költségszámítása a Finance and Operations alkalmazások költségarány- és számlázásiarány-konfigurációi használatával</span><span class="sxs-lookup"><span data-stu-id="6b9df-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="6b9df-110">Erőforrás-kezelés a Finance and Operations alkalmazások projektjeihez</span><span class="sxs-lookup"><span data-stu-id="6b9df-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="6b9df-111">A projektek előrehaladása és az idő nyomon követése a Finance and Operations alkalmazásokban</span><span class="sxs-lookup"><span data-stu-id="6b9df-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="6b9df-112">A projektek és a projekten kívüli kiadások költségkezelési tapasztalatai az OCR-funkció segítségével végzett nyugtarögzítéssel</span><span class="sxs-lookup"><span data-stu-id="6b9df-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="6b9df-113">Számlázás nagyvállalati szintű áfa és dátum szerint átváltási árfolyamok rendszer használatával</span><span class="sxs-lookup"><span data-stu-id="6b9df-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="6b9df-114">Konfigurálható projektcsoportok a befejezetlen termelés könyveléséhez és az elhatárolásokhoz</span><span class="sxs-lookup"><span data-stu-id="6b9df-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="6b9df-115">Projektbevétel elszámolása</span><span class="sxs-lookup"><span data-stu-id="6b9df-115">Project revenue recognition</span></span>

<span data-ttu-id="6b9df-116">Ez a telepítési típus bővítmény biztosít a Dynamics 365 Finance és a Dynamics 365 Supply Chain Management alkalmazások által biztosított funkciókhoz.</span><span class="sxs-lookup"><span data-stu-id="6b9df-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="6b9df-117">Válassza ezt a telepítési típust, hogy a Dynamics 365 Project Operations szolgáltatást használja a teljes projektéletciklus során, beleértve a következő alapvető követelményeket:</span><span class="sxs-lookup"><span data-stu-id="6b9df-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="6b9df-118">Átfogó projektmenedzsment-rendszer, amely kezeli a készletezett cikkeket és a feladat/gyártási rendelés költségszámítását a belső és a számlázható projektek számára az ütemezés és a pénzügy szempontjából.</span><span class="sxs-lookup"><span data-stu-id="6b9df-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="6b9df-119">A szervezet már rendelkezik a Dynamics 365 Finance vagy a Dynamics 365 Supply Chain és Manufacturing alkalmazásokkal és a Projektalapú tranzakciók integrálásával egyszerűsíti az adatelérési és jelentéskészítési igényeket.</span><span class="sxs-lookup"><span data-stu-id="6b9df-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="6b9df-120">Teljes körűen működőképes költségkezelési rendszer, amely a projekthez tartozó és a projekten kívüli költségekre vonatkozó házirend-kikényszerítést és visszatérítéseket is lehetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="6b9df-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="6b9df-121">Nagyvállalati szintű áfa- és átváltásiárfolyam-kezelő rendszer, amely a projektekre vonatkozóan ügyfeleknek kiállított számlákat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b9df-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="6b9df-122">Egy Nemzetközi Pénzügyi Beszámolási Standardoknak (IFRS) megfelelő projektkönyvelési és bevételelszámolási rendszer.</span><span class="sxs-lookup"><span data-stu-id="6b9df-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]