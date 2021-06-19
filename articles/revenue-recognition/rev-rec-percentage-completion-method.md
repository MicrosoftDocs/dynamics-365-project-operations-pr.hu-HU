---
title: Rögzített árú bevétel becslési projektjei
description: Ez a témakör információkat nyújt rögzített áru bevételekről a projektekben.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013804"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="1ae78-103">Rögzített árú bevétel becslési projektjei</span><span class="sxs-lookup"><span data-stu-id="1ae78-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="1ae78-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="1ae78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1ae78-105">Amikor létrehoz egy projektszerződés-sort a következő attribútumokkal a Dynamics 365 Project Operations alkalmazásban a Microsoft Dataverse alatt, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet.</span><span class="sxs-lookup"><span data-stu-id="1ae78-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="1ae78-106">A projektben szereplő információk a következőkön alapulnak:</span><span class="sxs-lookup"><span data-stu-id="1ae78-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="1ae78-107">Rögzített árú számlázási módszer.</span><span class="sxs-lookup"><span data-stu-id="1ae78-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="1ae78-108">Egy társított projekt.</span><span class="sxs-lookup"><span data-stu-id="1ae78-108">An associated project.</span></span>
  - <span data-ttu-id="1ae78-109">Legalább egy definiált mérföldkő a **Projekt-szerződéssor** lap **Számla ütemezés** lapján.</span><span class="sxs-lookup"><span data-stu-id="1ae78-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="1ae78-110">Rögzített árú bevétel becslési projektek ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1ae78-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="1ae78-111">A rögzített árú bevételbecslési projektek áttekintéséhez hajtsa végre a következő lépéseket:</span><span class="sxs-lookup"><span data-stu-id="1ae78-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="1ae78-112">A Dynamics 365 Finance környezetben nyissa meg a **Projektvezetés és könyvelés** > **Projektek** > **Rögzített árú bevételbecslési projektek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1ae78-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="1ae78-113">Jelölje ki a megtekinteni kívánt projektet, és kattintson duplán a **Projektbecslés azonosítójára** a bejegyzés megnyitásához, és tekintse át a projekt részleteit.</span><span class="sxs-lookup"><span data-stu-id="1ae78-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="1ae78-114">Bontsa ki a **Projekt** lapot. A **Kijelölt projektek** rácsán egy projekt jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="1ae78-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="1ae78-115">A rendszer ezt használja alapértelmezett projektként, mert a projekt szerződéssorához társított projekt.</span><span class="sxs-lookup"><span data-stu-id="1ae78-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="1ae78-116">A társítás módosításához válasszon ki további projekteket, és vegye fel őket a **Kijelölt projektek** rácsára.</span><span class="sxs-lookup"><span data-stu-id="1ae78-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="1ae78-117">Ha ebben a táblázatban több projektet is kijelöl, a projekt százalékos készültségi szintjét és a bevételi becsléseket a program az összes kijelölt projekthez együttesen számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1ae78-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="1ae78-118">A projekt költségét, a bevételi profilt, a költségsablont és az időszak kódját manuálisan is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="1ae78-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="1ae78-119">Ha nem állítanak be manuálisan beállítást, akkor az értékek alapértelmezésre állnak a projekt első becslési számításaiban a projekt költség-és bevételi profiljaihoz beállított szabályok szerint.</span><span class="sxs-lookup"><span data-stu-id="1ae78-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]