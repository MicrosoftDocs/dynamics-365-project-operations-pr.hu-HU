---
title: Beépülő modul attribútumainak frissítése új árképzési dimenziókkal
description: Ez a cikk a bővítményattribútumok díjszabási dimenziókhoz való frissítésével kapcsolatos információkat tartalmaz.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920017"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Beépülő modul attribútumainak frissítése új árképzési dimenziókkal

Ez a cikk a bővítményattribútumok díjszabási dimenziókhoz való frissítésével kapcsolatos információkat tartalmaz.

> [!NOTE]
> Ez a cikk csak a Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Előfeltételek
A cikkben található lépések végrehajtása előtt el kell végeznie a következő cikkekben található eljárásokat:

  - [Egyéni mezők és entitások létrehozása](create-custom-fields-entities-pricing-dimensions.md) 
  - [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz ](add-custom-fields-price-setup-transactional-entities.md)
  - [Egyéni mezők beállítása árazási dimenziókként](set-up-custom-fields-pricing-dimensions.md). 
  
Ha még nem fejezte be ezeket az eljárásokat, fejezze ki őket, majd térjen vissza ehhez a cikkhez.

## <a name="register-a-plug-in"></a>Beépülő modul regisztrációja
Ha egy projektajánlatsora jön létre az **Ajánlati sor** lapon a projekt ajánlati sora esetében, a rendszer két becslési sort hoz létre. Az egyik sor a becslés költségoldalán van, a másik sor pedig az értékesítés oldalon. Ugyanez vonatkozik a projektszerződésekre.

Amikor módosít egy mennyiséget vagy egy mezőt a költségoldalon, akkor ez a változás az értékesítési oldalra terjed. Ez azért lehetséges, mert a PreOperation beépülő modul a Quotelinedetail és a contractline részletező entitásokon kapcsolnak bizonyos attribútumokat a tranzakció költségoldaláról az értékesítési oldalára. Ha az értékesítési oldalon a költség oldalon is meg kell változtatnia az árképzési dimenzió értékeit, akkor az árképzési dimenzió módosítása után a következő beépülő modulokat újra regisztrálni kell.

Ezek a beépülő modulok a frissítéshez és az ismételt regisztráláshoz:

- PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction frissítése**
- PreOperationQuoteLineDetailUpdate - **Az msdyn_quotelinetransaction modult frissíti**

Hajtsa végre a következő lépéseket a beépülő modulok frissítéséhez és regisztrálásához.

1. Nyissa meg a **PluginRegistrationTool** eszközt, és kapcsolódjon a Project Operations Dataverse-környezethez.
2. Válassza a **Keresés** lehetőséget, és írja be a frissítendő beépülő modul első néhány betűjét.
3. Miután megtalálta a beépülő modult, válassza ki azt, majd válassza a **Kiválasztás a fő űrlapon** lehetőséget.
4. Válassza ki a **Update msdyn_orderlinetransaction** lépést, kattintson a jobb gombbal, majd válassza a **Frissítés** lehetőséget.
5. A **Frissítés** párbeszédpanelen ablakban kattintson a három pontra (**...**) a szűrési attribútumokban.
6. Megnyílik a szűrési attribútumok ablak, amely felsorolja az entitás összes attribútumát és az árképzési dimenziókat. Jelölje be az árképzési dimenzió attribútumaihoz tartozó jelölőnégyzeteket.
7. Válassza az **OK** gombot, hogy bezárja az oldalt, majd válassza a **Lépés frissítése** elemet.
8. Ismételje meg az 2–7. lépéseket a második **PreOperationQuoteLineDetail** beépülő modulhoz. Ehhez a beépülő modulhoz frissítse az **msdyn_quotelinetransaction frissítése** lépést.
9. Zárja be a **PluginRegistrationTool** eszközt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]