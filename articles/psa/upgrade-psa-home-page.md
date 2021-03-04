---
title: A kezdőlap frissítése
description: Ez a témakör azt mutatja, hogy hol találja a fontos információkat az új és módosult funkciókról a Dynamics 365 Project Service Automation rendszerben, és a folyamatot a legújabb verzióra történő frissítéshez.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e30da3a5ade6d8bafcdc45801b830196841997bf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150086"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="e590d-103">A kezdőlap frissítése</span><span class="sxs-lookup"><span data-stu-id="e590d-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="e590d-104">Frissítés a PSA 2.x vagy 1.x verziójáról a 3.x verzióra</span><span class="sxs-lookup"><span data-stu-id="e590d-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="e590d-105">Új példányok</span><span class="sxs-lookup"><span data-stu-id="e590d-105">New instances</span></span>

<span data-ttu-id="e590d-106">2019. május 17-től, amikor egy új példány létesítésekor a Project Service Automation van kiválasztva, az alapértelmezés szerint a 3.x verzió kerül telepítésre.</span><span class="sxs-lookup"><span data-stu-id="e590d-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="e590d-107">Meglévő példányok</span><span class="sxs-lookup"><span data-stu-id="e590d-107">Existing instances</span></span>

<span data-ttu-id="e590d-108">Korábban azoknak az ügyfeleknek, akiknek PSA 2.x verziója volt, és frissíteniük kellett a 3.x verzióra, amely a PSA Unified Client Interface (UCI) verziója, fel kellett venniük a kapcsolatot a Microsoft ügyfélszolgálattal, és meg kellett adniuk a részleteket a saját példányukról, hogy a támogatás lehetővé tegye a példány frissítését a 3.x verzióra.</span><span class="sxs-lookup"><span data-stu-id="e590d-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="e590d-109">2020. március 1-jétől azoknak az ügyfeleknek, akiknek PSA 2.x példánya van, és frissíteniük kell a 3.x verzióra, a példányaikat közvetlenül az Adminisztrátor portálról frissíthetik példányaikat, és ne kell felvenniük a kapcsolatot a Microsoft ügyfélszolgálattal.</span><span class="sxs-lookup"><span data-stu-id="e590d-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="e590d-110">A PSA 3.x verziója jelentős változtatásokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e590d-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="e590d-111">A továbbfejlesztett felhasználói élmény biztosítása érdekében az egységes interfész keretére épült.</span><span class="sxs-lookup"><span data-stu-id="e590d-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="e590d-112">Az átalakított alkalmazás következetes, egységes felhasználói felületet (UI) biztosít, és reagáló tervezési elveket követ az optimális megtekintéshez bármilyen képernyőméretben vagy eszközön.</span><span class="sxs-lookup"><span data-stu-id="e590d-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="e590d-113">Az alkalmazás egészében más változások is történtek.</span><span class="sxs-lookup"><span data-stu-id="e590d-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="e590d-114">Néhány megváltozott terület magában foglalja az árazást, az erőforrások, az idő, a költségek és a jóváhagyások elrendelését és hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="e590d-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="e590d-115">A frissítési folyamat megkezdése előtt javasoljuk, hogy hajtsa végre a következő feladatokat:</span><span class="sxs-lookup"><span data-stu-id="e590d-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="e590d-116">Ellenőrizze, hogy a Dynamics 365 Field Service és a Project Service Automation telepítve vannak-e az azonosított példányon.</span><span class="sxs-lookup"><span data-stu-id="e590d-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="e590d-117">Ha mindkét megoldás telepítve van, akkor a példa rendszeres használatának folytatása előtt terveznie kell mindkettő frissítését.</span><span class="sxs-lookup"><span data-stu-id="e590d-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="e590d-118">Gondosan olvassa át a következő témákat.</span><span class="sxs-lookup"><span data-stu-id="e590d-118">Carefully review the following topics.</span></span> <span data-ttu-id="e590d-119">A verziók közötti változások ismerete és megértése segít a frissítési folyamatban.</span><span class="sxs-lookup"><span data-stu-id="e590d-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="e590d-120">Ezek a témák információkat tartalmaznak a PSA jelentős változásairól, valamint a 3.x verzióra történő frissítés megfontolásairól és ajánlásairól.</span><span class="sxs-lookup"><span data-stu-id="e590d-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="e590d-121">Újdonságok és változások a Project Service Automation 3. verziójában</span><span class="sxs-lookup"><span data-stu-id="e590d-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="e590d-122">Frissítési szempontok - A Project Service Automation 2.x vagy 1.x verziója a 3. verzióra</span><span class="sxs-lookup"><span data-stu-id="e590d-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="e590d-123">Frissítse a sandbox példányát a megvalósításban bekövetkező változások értékeléséhez, mielőtt frissítené a termelési példányt.</span><span class="sxs-lookup"><span data-stu-id="e590d-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="e590d-124">Miután áttekintette a korábban említett témákat, és készen áll a PSA 3.x vagy UCI-alapú verzióra való frissítésre, kérje a Microsoft támogatását, hogy a frissítést elérhetővé tegye az adminisztrációs központból.</span><span class="sxs-lookup"><span data-stu-id="e590d-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="e590d-125">Kérésében adja meg a példány részleteit.</span><span class="sxs-lookup"><span data-stu-id="e590d-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="e590d-126">A PSA régebbi verziói (PSA 2.x verzió) egy újonnan létrehozott példányban</span><span class="sxs-lookup"><span data-stu-id="e590d-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="e590d-127">2019. május 17-től minden új példányon UCI lesz az alapértelmezett ügyfél.</span><span class="sxs-lookup"><span data-stu-id="e590d-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="e590d-128">A változáshoz való hozzáigazításhoz a PSA 3.x és a Field Service 8.x verziója alapértelmezés szerint lesz biztosítva, mivel ezeket a verziókat úgy tervezték, hogy az UCI klienssel működjenek.</span><span class="sxs-lookup"><span data-stu-id="e590d-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="e590d-129">2020. március 1-jétől a Dynamics PSA ügyfelei a továbbiakban nem hozhatnak létre új környezetet a PSA régebbi verzióival, például a PSA 2.x-es vagy régebbi verzióival.</span><span class="sxs-lookup"><span data-stu-id="e590d-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="e590d-130">Minden új környezet csak a PSA 3.X verziójában hozható létre.</span><span class="sxs-lookup"><span data-stu-id="e590d-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="e590d-131">A legjobb élmény érdekében, ha a Field Service és a PSA alkalmazások régebbi verzióit használja, keresse meg a **Rendszerbeállítások** oldalt és a mezőnél használja a **Csak az új egységes interfész használata (ajánlott)** mezőt, válassza a **Nem** lehetőséget, mivel ezek a verziók nem úgy vannak megtervezve, hogy megfelelően letöltsék az UCI-t.</span><span class="sxs-lookup"><span data-stu-id="e590d-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="e590d-132">Az UCI kikapcsolása után a régi web kliens használatával megnyithatja és futtathatja a Field Service és a PSA ezeket a verzióit.</span><span class="sxs-lookup"><span data-stu-id="e590d-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
