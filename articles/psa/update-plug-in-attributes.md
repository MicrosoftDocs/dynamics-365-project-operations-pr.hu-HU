---
title: Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez
description: Ez a témakör az árazási dimenziókhoz tartozó bővítményattribútumok frissítéséről nyújt információt.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988789"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ha nem a Project Service Automation (PSA) ajánlati és szerződéses szolgáltatásokat használja, kihagyhatja ezt a témát.

Ez a témakör feltételezi, hogy először elvégezte a következő eljárásokat: [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md), [Egyéni mezők hozzáadása az ár a telepítést és tranzakciós szervezetek](field-references.md) és [Egyéni mezők beállítása árképzési dimenziókként](set-up-pricing-dimensions.md). Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához.

Amikor egy **Árajánlatsor** oldalon elkészül egy árajánlati sor egy projekt árajánlatsorához, a rendszer két becslési sort hoz létre a háttérben - egy sort a becslés költségoldalához, egy pedig az értékesítés oldalához. Ugyanez vonatkozik a projektszerződésekre.

Amikor módosít egy mennyiséget vagy egy mezőt a költségoldalon, akkor ez a változás az értékesítési oldalra terjed. Ez azért lehetséges, mert a következő beépülő modulokra van szükség, hogy újra kell regisztrálni az árképzési méretek megváltoztatása után.

- PreOperationContractLineDetailUpdate - Frissítések **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Frissítések **msdyn_quotelinetransaction**.

A következő lépések végigvezetik a beépülő modulok regisztrálásának folyamatát.

1. Nyissa meg a **PluginRegistrationTool** elemet, és csatlakozzon az online példányhoz.
2. Kattintson a **Keresés** elemre, és keresse meg a frissíteni kívánt bővítményt.

 ![A keresési fa képernyőképe.](media/PRT-1.png)

3. Miután megtalálta a beépülő modult, válassza ki azt, majd kattintson a **Kiválasztás a fő űrlapon** elemre.

4. Válassza ki a frissíteni kívánt bővítmény lépését, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.

 ![A frissítendő plug-in képernyőképe.](media/PRT-2.png)
 
5. A frissítési ablakban kattintson a ellipszisre (**...**) a szűrési attribútumokban.

 ![A létező lépéskonfigurációs információk frissítése képernyőképe.](media/PRT-3.png)
 
6. Jelölje be az árazási attribútum jelölőnégyzeteket.

 ![Képernyőkép, amely jelöli a jelölőnégyzet kiválasztását az árazási attribútumokhoz.](media/PRT-4.png)

7. Kattintson az **OK**-ra, hogy zárja be az oldalt, majd válassza a **Lépés frissítése** elemet.

 ![A képernyő frissítése, amelyen megjelenik az „Update Step” gomb.](media/PRT-5.png)
 
8. Ismételje meg ezt a folyamatot a második plug-in számára, **PreOperationQuoteLineDetail - az msdyn_quotelinetransaction frissítése**.

9. Zárja be a plug-in regisztrációs eszközt.



[!INCLUDE[footer-include](../includes/footer-banner.md)]