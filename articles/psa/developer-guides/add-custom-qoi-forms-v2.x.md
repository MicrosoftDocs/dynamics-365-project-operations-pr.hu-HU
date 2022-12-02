---
title: Új egyéni entitás-űrlapok hozzáadása (Project Service Automation 2.x)
description: Ez a cikk a lehetőségekhez, ajánlatokhoz, megrendelésekhez és számlákhoz tartozó egyéni entitás-űrlapok hozzáadásával kapcsolatban tartalmaz tájékoztatást a Dynamics 365 Project Service Automation 2.x alkalmazásban.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922731"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Új egyéni entitás-űrlapok hozzáadása (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Mező típusa 

Dynamics 365 Project Service Automation a **Típus** (**msdyn\_ordertype**) mezőn és a Lehetőségek, Árajánlatok, Megrendelések és Számlák típusú entitások mezője alapján különbözteti meg ezeknek a **munkaalapú** az entitásoknak a verzióit az **elemalapú** és a **szolgáltatásalapú** verzióktól. Az entitások munkaalapú változatát a PSA kezeli. Az ügyfél oldalán és a kiszolgáló oldalán számos üzleti logika megoldása a **Típus** mezőtől függ. Ezért fontos, hogy az entitások létrehozásakor a program a megfelelő értékkel inicializálja a mezőt. A helytelen értékek helytelen viselkedést okozhatnak, és előfordulhat, hogy bizonyos üzleti logika nem működik megfelelően.

## <a name="automatic-form-switching"></a>Automatikus űrlapváltás

Ha el szeretné kerülni az esetleges adatsérüléseket és a váratlan viselkedéseket, amelyeket az értékesítési entitások bejegyzéseinek helytelen inicializálása és módosítása okoz, a PSA az űrlapon kívüli űrlapokon történő automatikus átváltáshoz tartalmaz logikai adatokat. Ez a logika a megfelelő űrlapra viszi a felhasználókat a munkaalapú verzió vagy bármely más típusú Lehetőség, Árajánlat, Megrendelés, vagy Számla entitás használata során. Amikor a felhasználó megnyitja a Lehetőség, Árajánlat, Megrendelés, vagy Számla entitás munkaalapú változatát, az űrlap a következőre vált: **Projektinformációk**.

Az automatikus űrlapátváltás logikája **a formId** és a **msdyn\_ordertype** mező közötti leképezésen alapul. A leképezéshez az összes nem beépített űrlap hozzá van adva. Az egyéni űrlapokat azonban kézzel kell hozzáadni ahhoz, hogy meg lehesesn adni, a kezelni kívánt entitás melyik verzióját kívánja használni. Ez a **msdyn\_ordertype** mezőn alapul. Ha a leképezésből hiányzik az űrlap, akkor a logika a kifogyott űrlapra vált, az entitás **msdyn\_ordertype** mezőjében elmentett érték alapján.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Egyéni űrlapok hozzáadása és az űrlapátváltás logikájának bekapcsolása

A következő példa azt mutatja be, hogyan vehetők fel egyéni űrlapok, **Saját projektinformációk**, úgy, hogy munka-alapú lehetőségekkel működjön. Ugyanez a folyamat használható az egyéni űrlapok hozzáadására, hogy az ajánlatokat, megrendeléseket és számlákat használják.

A következő lépések végrehajtásával hozhatja létre a **Projektinformációk** űrlap egyéni verzióját.

1. A lehetőség entitásban nyissa meg a **Projektinformációk** űrlapot, és mentse el a **Saját projektinformációk** név alatt található másolatot.
2. Nyissa meg az új űrlapot, és a tulajdonságok részen ellenőrizze, hogy az űrlap inicializációs parancsfájljai szerepelnek-e a **Projektinformációk** űrlapon. 

    > [!IMPORTANT]
    > Ne távolítsa el a parancsfájlokat. Ellenkező esetben előfordulhat, hogy egyes adatok hibásan lesznek inicializálva.

3. Ellenőrizze, hogy a **Típus** (**msdyn\_ordertype**) mező szerepel-e az űrlapon. 

    > [!IMPORTANT]
    > Ne távolítsa el ezt a mezőt. Ellenkező esetben az inicializációs parancsfájlok sikertelenek lesznek.

4. Keresse meg az új űrlap **formId** értékét. Ezt kétféleképpen teheti meg:

    - Exportálja a **Saját projektinformációk** űrlapját egy nem felügyelt megoldás részeként, majd keresse meg a **formId** értékét az exportált megoldás customization.xml fájljában.
    - Nyissa meg a **Saját projektinformációk** űrlapot a űrlapszerkesztőbben, majd keresse meg az URL-címben a **fromId** paraméter melletti globálisan egyedi azonosítót (GUID), amint az a következő ábrán látható.

    ![Az új űrlap formId értéke az URL-ben.](media/how-to-add-custom-forms-in-v2.0.png)

5. Hozzon létre egy **msdyn\_ordertype** leképezést a **formId** értékhez az msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js weberőforrás módosításával. Távolítsa el a kódot az erőforrásból, és cserélje le az alábbi kódra.

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

6. Mentse el, majd tegye közzé a testreszabásokat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
