---
title: Újdonságok vagy változások a Project Service Automation 20-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 20-os frissítési kiadásában
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078041"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="356e2-103">Project Service Automation 20-as frissítési kiadás, V3</span><span class="sxs-lookup"><span data-stu-id="356e2-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="356e2-104">Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz.</span><span class="sxs-lookup"><span data-stu-id="356e2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="356e2-105">Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="356e2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="356e2-106">Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis.</span><span class="sxs-lookup"><span data-stu-id="356e2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="356e2-107">A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra.</span><span class="sxs-lookup"><span data-stu-id="356e2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="356e2-108">További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="356e2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="356e2-109">Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 20-es frissítési kiadásában.</span><span class="sxs-lookup"><span data-stu-id="356e2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="356e2-110">A verzió build száma V 3.10.31.37, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.</span><span class="sxs-lookup"><span data-stu-id="356e2-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="356e2-111">20-ös frissítési kiadás</span><span class="sxs-lookup"><span data-stu-id="356e2-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="356e2-112">Hibajavítások</span><span class="sxs-lookup"><span data-stu-id="356e2-112">Bug fixes</span></span>

<span data-ttu-id="356e2-113">**Projektmenedzsment**</span><span class="sxs-lookup"><span data-stu-id="356e2-113">**Project Management**</span></span>

<span data-ttu-id="356e2-114">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="356e2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="356e2-115">Ha a projektcsapat tagjait olyan felosztási módszerrel importálja, amelyhez órák szükségek, nem egyérlemű hibaüzenetet eredményezhet, ha a megadott órák értéke nulla.</span><span class="sxs-lookup"><span data-stu-id="356e2-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="356e2-116">A felhasználók helytelen hibaüzenetet kapnak, amikor a karakterek maximális számát megadták egy projektfeladat **Leírás** mezőjébe.</span><span class="sxs-lookup"><span data-stu-id="356e2-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="356e2-117">A **Microsoft Dynamics 365 Project Service Automation bővítmény letöltése** oldal átirányít az angol letöltési oldalra, ha a felhasználó nyelvi beállításainak értéke japán.</span><span class="sxs-lookup"><span data-stu-id="356e2-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="356e2-118">Kiszolgálóhiba esetén a **Projektek űrlap** **Ütemezés** lapján a szinkronizálási címke időnként megmarad.</span><span class="sxs-lookup"><span data-stu-id="356e2-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="356e2-119">Egy feladat módosításakor a rendszer elküldi a redundáns feladatok frissítéseit a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="356e2-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="356e2-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="356e2-120">**Sales**</span></span>

<span data-ttu-id="356e2-121">A következő problémák kerültek kijavításra:</span><span class="sxs-lookup"><span data-stu-id="356e2-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="356e2-122">A **Szerződés** űrlapon a dupla kattintás a **számla létrehozása** lehetőségre egyetlen tényleges rekordhoz két számlát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="356e2-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="356e2-123">Internet Explorer 11-ben a felhasználók nem tudnak Költségjelentés-bejegyzéseket létrehozni.</span><span class="sxs-lookup"><span data-stu-id="356e2-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="356e2-124">A költségek sztornírozása és a nem számlázott értékesítések sztornírozása nem kapcsolódik össze.</span><span class="sxs-lookup"><span data-stu-id="356e2-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="356e2-125">A **Tényadatok frissítése** gomb a **Projekt** űrlapon nem frissíti a **Feladat tényleges órái** mezőt.</span><span class="sxs-lookup"><span data-stu-id="356e2-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="356e2-126">A **PreValidateProjectTeamMemberCreate** bővítmény ismétlődő általános foglalható erőforrásokat hozhat létre, ha a **msdyn_isgenericresourceprojectscoped** attribútum **Hamis** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="356e2-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="356e2-127">Az **Újraszámítás** törli a termékalapú árajánlati sor és szerződéssor adatainak számlázható költségeit.</span><span class="sxs-lookup"><span data-stu-id="356e2-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="356e2-128">Bizonyos helyzetekben a **PostEstimateLineUpdate** beépülő modul Null hivatkozási kivételi hibát jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="356e2-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="356e2-129">Az időfázis időtartama a **Jövedelmezőségi elemzés diagramjában** nem egyezik meg az ajánlatban szereplő rögzített árú árajánlat sor részletek költségeinek időtartamával.</span><span class="sxs-lookup"><span data-stu-id="356e2-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="356e2-130">Az egység és az egységcsoport értékei nem megfelelőek a költségkategóriákhoz a **szerződéssor részletei** és az **ajánlati sor részletei** űrlapon.</span><span class="sxs-lookup"><span data-stu-id="356e2-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="356e2-131">**A szervezeti egység önköltségi ára** lista engedélyezi az átfedéseket az érvényességi dátumokban.</span><span class="sxs-lookup"><span data-stu-id="356e2-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="356e2-132">A felhasználók nem módosíthatják a **OrgUnit** értékét, ha a megrendelés típusa nem munkaalapú, mert az egy NULL referenciakivételi hibát eredményez.</span><span class="sxs-lookup"><span data-stu-id="356e2-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="356e2-133">Amikor az **ajánlati sor részletei** űrlapról próbál meg navigálni vissza az **árajánlat** lapra, az űrlap frissül, és megjeleníti az **Összesítés** lapot.</span><span class="sxs-lookup"><span data-stu-id="356e2-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
