---
title: Pénznem
description: Ez a témakör a pénznemtípusok Project Operations rendszerben történő hozzáadásáról és eltávolításáról tartalmaz tájékoztatást.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078124"
---
# <a name="currency"></a>Pénznem

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A pénznemek meghatározzák a termékkatalógusban szereplő termékek árát, valamint a tranzakciók, például a salesmegrendelések költségét. Ha az ügyfelek különböző területen helyezkednek el, adja hozzá a pénznemüket a tranzakciók kezeléséhez. Adja hozzá a jelenlegi és jövőbeli üzleti igényeinek leginkább megfelelő pénznemet.  

> [!NOTE]
> Ha Common Data Service-környezetet használ, a Power Platform felügyeleti központban van és a **Pénznemek** oldalra ( **Környezetek** > [környezet kijelölése] > **Beállítások** > **Üzlet** > **Pénznemek** ) lép, akkor az oldal üres lesz. Ennek oka az, hogy a Common Data Service környezetben nem támogatott a pénznem beállítása.

## <a name="add-a-currency"></a>Pénznem hozzáadása  
Az eljárás megkezdése előtt ellenőrizze, hogy a biztonsági szerepkör tartalmazza-e a rendszergazdai engedélyeket. 

1. A Power Platform felügyeleti központban válasszon ki egy környezetet. 
2. Válassza a **Beállítások** > **Vállalat** lehetőséget.
3. Válassza a **Pénznemek** lehetőséget.  
4. Válassza az **Új** lehetőséget.  
5. Töltse ki a szükséges adatokat.  


   |          Mező          |                                                                                                                                                                                                                                                                                                                                                                            Leírás                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Pénznemtípus**    | - **Rendszer** – Jelölje be ezt a beállítást, ha a Dynamics 365 modellvezérelt alkamazásaiban elérhető pénznemet kívánja használni. Pénznem kereséséhez válassza a **Keresés** lehetőséget. Ha kiválasztotta a pénznemkódot, a **Pénznem neve** és a **Pénznemszimbólum** lehetőséget automatikusan hozzáadja a rendszer a kiválasztott pénznemhez.<br />- **Egyéni** – Jelölje be ezt a beállítást, ha a Dynamics 365 modellvezérelt alkamazásaiban nem elérhető pénznemet kívánja használni. Ebben az esetben kézzel kell megadnia a **Pénznemkód** , **Pénznem pontossága** , **Pénznem neve** , **Pénznemszimbólum** , és **Pénznemátváltás** értékeit. |
   |    **Pénznem kódja**    |                                                                                                                                                                                                                                                                                                                                            A pénznem rövid űrlapja. Például, az USA dollár esetében **USD**.                                                                                                                                                                                                                                                                                                                                            |
   | **Pénznem pontossága**  |                                                                                                                                                                                  Írja be azon tizedesjegyek számát, amelyet használni kíván a pénznemhez.  0 és 4 között bármilyen értéket megadhat. **Megjegyzés:** Ha pontos értéket állított be a **Rendszerbeállítások** párbezsédpanelben, az az érték jelenik meg itt.                                                                                                                                                                                  |
   |    **Pénznem neve**    |                                                                                                                                                                                                                                         Ha a Dynamics 365 modellvezérelt alkalmazásaiban elérhető pénznemek listájából kiválasztott egy pénznemkódot, a kiválasztott kód pénznem neve jelenik meg itt. Ha az **Egyéni** lehetőséget választja ki a pénznem típusaként, adja meg a pénznem nevét.                                                                                                                                                                                                                                          |
   |   **Pénznem jele**   |                                                                                                                                                                                                                                                                      Ha az elérhető pénznemek listájából kiválasztott egy pénznemkódot, a kiválasztott pénznem szimbóluma jelenik meg itt. Ha az **Egyéni** lehetőséget választja ki a pénznem típusaként, adja meg az új pénznem szimbólumát.                                                                                                                                                                                                                                                                       |
   | **Pénznemátváltás** |                                                                                                                                                                                                                                     Írja be a kiválasztott pénznem értékét egy USA-dollár értéke alapján. Ez az az összeg, amelyet a kiválasztott pénznem alappénznemmé alakít. **Fontos:** Ellenőrizze, hogy olyan gyakran frissíti ezt az értéket, amennyire szükséges a tranzakciók pontatlan számításainak elkerülése érdekében.                                                                                                                                                                                                                                      |


6. Ha elkészült, a parancssávon válassza a **Mentés** vagy a **Mentés és bezárás** lehetőséget.  

   > [!TIP]
   >  A pénznem szerkesztéséhez válassza a pénznem lehetőséget, és írja be vagy jelölje be az új értékeket.  

## <a name="delete-a-currency"></a>Pénznem törlése  

1. A Power Platform felügyeleti központban válasszon ki egy környezetet. 
2. Válassza a **Beállítások** > **Vállalat** lehetőséget.
3. Válassza a **Pénznemek** lehetőséget.  
4. A pénznemek megjelenő listájából válassza ki a törölni kívánt pénznemet.  
5. Válassza a **Törlés** lehetőséget.  
6. Törlés jóváhagyása.  

> [!IMPORTANT]
>  A más bejegyzések által használt pénznemek nem törölhetők, csak deaktiválhatók. A pénznembejegyzések inaktiválása nem távolítja el a létező bejegyzésekben (például lehetőségekben és megrendelésekben) tárolt pénznemadatokat. Azonban nem lehet új tranzakciókhoz deaktivált pénznemet választani.  
