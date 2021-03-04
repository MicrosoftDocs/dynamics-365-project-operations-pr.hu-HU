---
title: Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez
description: Ez a témakör az árazási dimenziókhoz tartozó bővítményattribútumok frissítéséről nyújt információt.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147071"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="ab3ff-103">Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez</span><span class="sxs-lookup"><span data-stu-id="ab3ff-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="ab3ff-104">Ha nem a Project Service Automation (PSA) ajánlati és szerződéses szolgáltatásokat használja, kihagyhatja ezt a témát.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="ab3ff-105">Ez a témakör feltételezi, hogy először elvégezte a következő eljárásokat: [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md), [Egyéni mezők hozzáadása az ár a telepítést és tranzakciós szervezetek](field-references.md) és [Egyéni mezők beállítása árképzési dimenziókként](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ff-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="ab3ff-106">Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="ab3ff-107">Amikor egy **Árajánlatsor** oldalon elkészül egy árajánlati sor egy projekt árajánlatsorához, a rendszer két becslési sort hoz létre a háttérben - egy sort a becslés költségoldalához, egy pedig az értékesítés oldalához.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="ab3ff-108">Ugyanez vonatkozik a projektszerződésekre.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="ab3ff-109">Amikor módosít egy mennyiséget vagy egy mezőt a költségoldalon, akkor ez a változás az értékesítési oldalra terjed.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="ab3ff-110">Ez azért lehetséges, mert a következő beépülő modulokra van szükség, hogy újra kell regisztrálni az árképzési méretek megváltoztatása után.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="ab3ff-111">PreOperationContractLineDetailUpdate - Frissítések **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="ab3ff-112">PreOperationQuoteLineDetailUpdate - Frissítések **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="ab3ff-113">A következő lépések végigvezetik a beépülő modulok regisztrálásának folyamatát.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="ab3ff-114">Nyissa meg a **PluginRegistrationTool** elemet, és csatlakozzon az online példányhoz.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="ab3ff-115">Kattintson a **Keresés** elemre, és keresse meg a frissíteni kívánt bővítményt.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![A keresési fa képernyőképe](media/PRT-1.png)

3. <span data-ttu-id="ab3ff-117">Miután megtalálta a beépülő modult, válassza ki azt, majd kattintson a **Kiválasztás a fő űrlapon** elemre.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="ab3ff-118">Válassza ki a frissíteni kívánt bővítmény lépését, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![A frissítendő plug-in képernyőképe](media/PRT-2.png)
 
5. <span data-ttu-id="ab3ff-120">A frissítési ablakban kattintson a ellipszisre (**...**) a szűrési attribútumokban.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![A létező lépéskonfigurációs információk frissítése képernyőképe](media/PRT-3.png)
 
6. <span data-ttu-id="ab3ff-122">Jelölje be az árazási attribútum jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-122">Select the pricing attribute check boxes.</span></span>

 ![Képernyőkép, amely jelöli a jelölőnégyzet kiválasztását az árazási attribútumokhoz](media/PRT-4.png)

7. <span data-ttu-id="ab3ff-124">Kattintson az **OK**-ra, hogy zárja be az oldalt, majd válassza a **Lépés frissítése** elemet.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![A képernyő frissítése, amelyen megjelenik az „Update Step” gomb](media/PRT-5.png)
 
8. <span data-ttu-id="ab3ff-126">Ismételje meg ezt a folyamatot a második plug-in számára, **PreOperationQuoteLineDetail - az msdyn_quotelinetransaction frissítése**.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="ab3ff-127">Zárja be a plug-in regisztrációs eszközt.</span><span class="sxs-lookup"><span data-stu-id="ab3ff-127">Close the plug-in registration tool.</span></span>

