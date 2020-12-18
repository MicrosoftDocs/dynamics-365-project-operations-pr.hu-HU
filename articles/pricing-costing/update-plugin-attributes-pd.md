---
title: Beépülő modul attribútumainak frissítése új árképzési dimenziókkal
description: Ez a témakör az árazási dimenziókhoz tartozó bővítményattribútumok frissítésének módjáról nyújt információt.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643221"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="59ac3-103">Beépülő modul attribútumainak frissítése új árképzési dimenziókkal</span><span class="sxs-lookup"><span data-stu-id="59ac3-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="59ac3-104">Ez a témakör az árazási dimenziókhoz tartozó bővítményattribútumok frissítésének módjáról nyújt információt.</span><span class="sxs-lookup"><span data-stu-id="59ac3-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="59ac3-105">Ez a témakör csak az Dynamics 365 Project Operations ajánlat és a szerződés funkciókra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="59ac3-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59ac3-106">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="59ac3-106">Prerequisites</span></span>
<span data-ttu-id="59ac3-107">A témakör lépéseinek végrehajtása előtt az alábbi témakörökben ismertetett lépéseket kell végrehajtania:</span><span class="sxs-lookup"><span data-stu-id="59ac3-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="59ac3-108">Egyéni mezők és entitások létrehozása</span><span class="sxs-lookup"><span data-stu-id="59ac3-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="59ac3-109">Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz </span><span class="sxs-lookup"><span data-stu-id="59ac3-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="59ac3-110">[Egyéni mezők beállítása árazási dimenziókként](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="59ac3-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="59ac3-111">Ha még nem fejezte be ezeket az eljárásokat, fejezze be őket, majd térjen vissza ehhez a témához.</span><span class="sxs-lookup"><span data-stu-id="59ac3-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="59ac3-112">Beépülő modul regisztrációja</span><span class="sxs-lookup"><span data-stu-id="59ac3-112">Register a plug-in</span></span>
<span data-ttu-id="59ac3-113">Ha egy projektajánlatsora jön létre az **Ajánlati sor** lapon a projekt ajánlati sora esetében, a rendszer két becslési sort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="59ac3-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="59ac3-114">Az egyik sor a becslés költségoldalán van, a másik sor pedig az értékesítés oldalon.</span><span class="sxs-lookup"><span data-stu-id="59ac3-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="59ac3-115">Ugyanez vonatkozik a projektszerződésekre.</span><span class="sxs-lookup"><span data-stu-id="59ac3-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="59ac3-116">Amikor módosít egy mennyiséget vagy egy mezőt a költségoldalon, akkor ez a változás az értékesítési oldalra terjed.</span><span class="sxs-lookup"><span data-stu-id="59ac3-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="59ac3-117">Ez azért lehetséges, mert a PreOperation beépülő modul a Quotelinedetail és a contractline részletező entitásokon kapcsolnak bizonyos attribútumokat a tranzakció költségoldaláról az értékesítési oldalára.</span><span class="sxs-lookup"><span data-stu-id="59ac3-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="59ac3-118">Ha az értékesítési oldalon a költség oldalon is meg kell változtatnia az árképzési dimenzió értékeit, akkor az árképzési dimenzió módosítása után a következő beépülő modulokat újra regisztrálni kell.</span><span class="sxs-lookup"><span data-stu-id="59ac3-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="59ac3-119">Ezek a beépülő modulok a frissítéshez és az ismételt regisztráláshoz:</span><span class="sxs-lookup"><span data-stu-id="59ac3-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="59ac3-120">PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction frissítése**</span><span class="sxs-lookup"><span data-stu-id="59ac3-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="59ac3-121">PreOperationQuoteLineDetailUpdate - **Az msdyn_quotelinetransaction modult frissíti**</span><span class="sxs-lookup"><span data-stu-id="59ac3-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="59ac3-122">Hajtsa végre a következő lépéseket a beépülő modulok frissítéséhez és regisztrálásához.</span><span class="sxs-lookup"><span data-stu-id="59ac3-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="59ac3-123">Nyissa meg a **PluginRegistrationTool** eszközt, és kapcsolódjon a Project Operations Dataverse-környezethez.</span><span class="sxs-lookup"><span data-stu-id="59ac3-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="59ac3-124">Válassza a **Keresés** lehetőséget, és írja be a frissítendő beépülő modul első néhány betűjét.</span><span class="sxs-lookup"><span data-stu-id="59ac3-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="59ac3-125">Miután megtalálta a beépülő modult, válassza ki azt, majd válassza a **Kiválasztás a fő űrlapon** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="59ac3-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="59ac3-126">Válassza ki a **Update msdyn_orderlinetransaction** lépést, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="59ac3-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="59ac3-127">A **Frissítés** párbeszédpanelen ablakban kattintson a három pontra (**...**) a szűrési attribútumokban.</span><span class="sxs-lookup"><span data-stu-id="59ac3-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="59ac3-128">Megnyílik a szűrési attribútumok ablak, amely felsorolja az entitás összes attribútumát és az árképzési dimenziókat.</span><span class="sxs-lookup"><span data-stu-id="59ac3-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="59ac3-129">Jelölje be az árképzési dimenzió attribútumaihoz tartozó jelölőnégyzeteket.</span><span class="sxs-lookup"><span data-stu-id="59ac3-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="59ac3-130">Válassza az **OK** gombot, hogy bezárja az oldalt, majd válassza a **Lépés frissítése** elemet.</span><span class="sxs-lookup"><span data-stu-id="59ac3-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="59ac3-131">Ismételje meg az 2–7. lépéseket a második **PreOperationQuoteLineDetail** beépülő modulhoz.</span><span class="sxs-lookup"><span data-stu-id="59ac3-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="59ac3-132">Ehhez a beépülő modulhoz frissítse az **msdyn_quotelinetransaction frissítése** lépést.</span><span class="sxs-lookup"><span data-stu-id="59ac3-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="59ac3-133">Zárja be a **PluginRegistrationTool** eszközt.</span><span class="sxs-lookup"><span data-stu-id="59ac3-133">Close **PluginRegistrationTool**.</span></span>
