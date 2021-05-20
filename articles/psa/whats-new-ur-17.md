---
title: Újdonságok vagy változások a Project Service Automation 17-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 17-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949232"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="528e1-103">Project Service Automation 17-es frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="528e1-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="528e1-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="528e1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="528e1-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="528e1-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="528e1-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="528e1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="528e1-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="528e1-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="528e1-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="528e1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="528e1-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 17-ös frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="528e1-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="528e1-110">Ennek a verziónak a build száma V 3.10.5.28, és általánosan elérhető egy önálló frissítésben 2020 márciusában.</span><span class="sxs-lookup"><span data-stu-id="528e1-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="528e1-111">17-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="528e1-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="528e1-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="528e1-112">Bug fixes</span></span>

<span data-ttu-id="528e1-113">**Általános**</span><span class="sxs-lookup"><span data-stu-id="528e1-113">**General**</span></span>

- <span data-ttu-id="528e1-114">Javítva: A Project Service Automation frissítése a csapattagok licencek kényszerítésére (a Project Resource Hub tartalmazza a Team Member Service terv metaadatait 3.x)</span><span class="sxs-lookup"><span data-stu-id="528e1-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="528e1-115">**Idő és költség**</span><span class="sxs-lookup"><span data-stu-id="528e1-115">**Time and Expense**</span></span>

- <span data-ttu-id="528e1-116">Javítva: Nem lehetséges egy költségbecslés nem lehetséges nem nulla árról nulla (0) árra.</span><span class="sxs-lookup"><span data-stu-id="528e1-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="528e1-117">A módosítás mellőzve lett.</span><span class="sxs-lookup"><span data-stu-id="528e1-117">The change is ignored.</span></span>

<span data-ttu-id="528e1-118">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="528e1-118">**Project Management**</span></span>

- <span data-ttu-id="528e1-119">Javítva: A nulla értékek ellenőrzése hozzá lett adva a csapattag beosztásának nevéhez.</span><span class="sxs-lookup"><span data-stu-id="528e1-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="528e1-120">Javítva: az **msdyn_userresourceid** mező a **msdyn_resourceassignment** entitásban elavult.</span><span class="sxs-lookup"><span data-stu-id="528e1-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="528e1-121">Javítva: A frissítés 2.x verzióról 3.x verzióra immár kezeli az üres ráfordításelosztásokat a feladat-hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="528e1-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="528e1-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="528e1-122">**Sales**</span></span>

- <span data-ttu-id="528e1-123">Javítva: az **Invoice.PreValidateInvoiceUpdate** most már kezeli a bejegyzések megfelelő ismételt hozzárendelésének forgatókönyvét.</span><span class="sxs-lookup"><span data-stu-id="528e1-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="528e1-124">Javítva: Amikor a tranzakció osztálya **Idő**, a **UnitGroup** nem szerkeszthető minden entitásnál, beleértve a, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** és **ContractLineDetails** entitásokat.</span><span class="sxs-lookup"><span data-stu-id="528e1-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="528e1-125">Azonban az **Egység** csak a **JournalLine** és a **InvoiceLineDetails** entitásokhoz nem szerkeszthető.</span><span class="sxs-lookup"><span data-stu-id="528e1-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]