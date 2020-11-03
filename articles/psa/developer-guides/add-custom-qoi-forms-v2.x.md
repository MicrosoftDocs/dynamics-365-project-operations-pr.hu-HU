---
title: Új egyéni entitás-űrlapok hozzáadása (Project Service Automation 2.x)
description: Ez a témakör a lehetőségekhez, ajánlatokhoz, megrendelésekhez és számlákhoz tartozó egyéni entitás-űrlapok hozzáadásával kapcsolatban tartalmaz tájékoztatást a Dynamics 365 Project Service Automation 2.x alkalmazásban.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078286"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="4d1bd-103">Új egyéni entitás-űrlapok hozzáadása (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="4d1bd-104">Mező típusa</span><span class="sxs-lookup"><span data-stu-id="4d1bd-104">Type field</span></span> 

<span data-ttu-id="4d1bd-105">Dynamics 365 Project Service Automation a **Típus** ( **msdyn\_ordertype** ) mezőn és a Lehetőségek, Árajánlatok, Megrendelések és Számlák típusú entitások mezője alapján különbözteti meg ezeknek a **munkaalapú** az entitásoknak a verzióit az **elemalapú** és a **szolgáltatásalapú** verzióktól.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="4d1bd-106">Az entitások munkaalapú változatát a PSA kezeli.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="4d1bd-107">Az ügyfél oldalán és a kiszolgáló oldalán számos üzleti logika megoldása a **Típus** mezőtől függ.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="4d1bd-108">Ezért fontos, hogy az entitások létrehozásakor a program a megfelelő értékkel inicializálja a mezőt.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="4d1bd-109">A helytelen értékek helytelen viselkedést okozhatnak, és előfordulhat, hogy bizonyos üzleti logika nem működik megfelelően.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="4d1bd-110">Automatikus űrlapváltás</span><span class="sxs-lookup"><span data-stu-id="4d1bd-110">Automatic form switching</span></span>

<span data-ttu-id="4d1bd-111">Ha el szeretné kerülni az esetleges adatsérüléseket és a váratlan viselkedéseket, amelyeket az értékesítési entitások bejegyzéseinek helytelen inicializálása és módosítása okoz, a PSA az űrlapon kívüli űrlapokon történő automatikus átváltáshoz tartalmaz logikai adatokat.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="4d1bd-112">Ez a logika a megfelelő űrlapra viszi a felhasználókat a munkaalapú verzió vagy bármely más típusú Lehetőség, Árajánlat, Megrendelés, vagy Számla entitás használata során.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="4d1bd-113">Amikor a felhasználó megnyitja a Lehetőség, Árajánlat, Megrendelés, vagy Számla entitás munkaalapú változatát, az űrlap a következőre vált: **Projektinformációk**.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="4d1bd-114">Az automatikus űrlapátváltás logikája **a formId** és a **msdyn\_ordertype** mező közötti leképezésen alapul.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="4d1bd-115">A leképezéshez az összes nem beépített űrlap hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="4d1bd-116">Az egyéni űrlapokat azonban kézzel kell hozzáadni ahhoz, hogy meg lehesesn adni, a kezelni kívánt entitás melyik verzióját kívánja használni.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="4d1bd-117">Ez a **msdyn\_ordertype** mezőn alapul.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="4d1bd-118">Ha a leképezésből hiányzik az űrlap, akkor a logika a kifogyott űrlapra vált, az entitás **msdyn\_ordertype** mezőjében elmentett érték alapján.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="4d1bd-119">Egyéni űrlapok hozzáadása és az űrlapátváltás logikájának bekapcsolása</span><span class="sxs-lookup"><span data-stu-id="4d1bd-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="4d1bd-120">A következő példa azt mutatja be, hogyan vehetők fel egyéni űrlapok, **Saját projektinformációk** , úgy, hogy munka-alapú lehetőségekkel működjön.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="4d1bd-121">Ugyanez a folyamat használható az egyéni űrlapok hozzáadására, hogy az ajánlatokat, megrendeléseket és számlákat használják.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="4d1bd-122">A következő lépések végrehajtásával hozhatja létre a **Projektinformációk** űrlap egyéni verzióját.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="4d1bd-123">A lehetőség entitásban nyissa meg a **Projektinformációk** űrlapot, és mentse el a **Saját projektinformációk** név alatt található másolatot.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="4d1bd-124">Nyissa meg az új űrlapot, és a tulajdonságok részen ellenőrizze, hogy az űrlap inicializációs parancsfájljai szerepelnek-e a **Projektinformációk** űrlapon.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="4d1bd-125">Ne távolítsa el a parancsfájlokat.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-125">Don't remove the scripts.</span></span> <span data-ttu-id="4d1bd-126">Ellenkező esetben előfordulhat, hogy egyes adatok hibásan lesznek inicializálva.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="4d1bd-127">Ellenőrizze, hogy a **Típus** ( **msdyn\_ordertype** ) mező szerepel-e az űrlapon.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="4d1bd-128">Ne távolítsa el ezt a mezőt.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-128">Don't remove this field.</span></span> <span data-ttu-id="4d1bd-129">Ellenkező esetben az inicializációs parancsfájlok sikertelenek lesznek.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="4d1bd-130">Keresse meg az új űrlap **formId** értékét.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="4d1bd-131">Ezt kétféleképpen teheti meg:</span><span class="sxs-lookup"><span data-stu-id="4d1bd-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="4d1bd-132">Exportálja a **Saját projektinformációk** űrlapját egy nem felügyelt megoldás részeként, majd keresse meg a **formId** értékét az exportált megoldás customization.xml fájljában.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="4d1bd-133">Nyissa meg a **Saját projektinformációk** űrlapot a űrlapszerkesztőbben, majd keresse meg az URL-címben a **fromId** paraméter melletti globálisan egyedi azonosítót (GUID), amint az a következő ábrán látható.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Az új űrlap formId értéke az URL-ben.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="4d1bd-135">Hozzon létre egy **msdyn\_ordertype** leképezést a **formId** értékhez az msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js weberőforrás módosításával.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="4d1bd-136">Távolítsa el a kódot az erőforrásból, és cserélje le az alábbi kódra.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="4d1bd-137">Mentse el, majd tegye közzé a testreszabásokat.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-137">Save and then publish the customizations.</span></span>
