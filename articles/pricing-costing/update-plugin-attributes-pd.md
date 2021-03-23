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
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274686"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Beépülő modul attribútumainak frissítése új árképzési dimenziókkal

Ez a témakör az árazási dimenziókhoz tartozó bővítményattribútumok frissítésének módjáról nyújt információt.

> [!NOTE]
> Ez a témakör csak az Dynamics 365 Project Operations ajánlat és a szerződés funkciókra vonatkozik.

## <a name="prerequisites"></a>Előfeltételek
A témakör lépéseinek végrehajtása előtt az alábbi témakörökben ismertetett lépéseket kell végrehajtania:

  - [Egyéni mezők és entitások létrehozása](create-custom-fields-entities-pricing-dimensions.md) 
  - [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz ](add-custom-fields-price-setup-transactional-entities.md)
  - [Egyéni mezők beállítása árazási dimenziókként](set-up-custom-fields-pricing-dimensions.md). 
  
Ha még nem fejezte be ezeket az eljárásokat, fejezze be őket, majd térjen vissza ehhez a témához.

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