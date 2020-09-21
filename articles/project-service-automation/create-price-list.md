---
title: Árlista létrehozása
description: Árlista létrehozása a Project Service szolgáltatásban
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752315"
---
# <a name="create-a-price-list-project-service"></a>Árlista létrehozása (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Az árlisták egy sablont biztosítanak a partnerkezelők számára, amely segít nekik az árajánlatok és a projektek létrehozásában, illetve egy projekt költségeinek a m,egállapításában. Sorelemlistát biztosítanak szerepkörökhöz, költségekhez, illetve az egyes cikkekért majd felszámítandó árat. Több árlistát is létre tud hozni, így külön árszerkezetet tarthat karban a különböző régiókban amelyekben értékesít és az értékesítési csatornákat is szétválaszthatja. Érdemes legalább egy árlistát létrehozni minden pénznem esetében, amelyen számlázni szeretne az ügyfeleinek.  
  
Ha szeretne az elvégzendő munkához pénzügyi becsléseket létrehozni, győződjön meg arról, hogy minden projektnek biztonsági önköltségi és értékesítési árlistája. Állítson be egy alapértelmezett önköltségi és értékesítési árlistát, amely érvényes minden, a szervezetben létrehozott projektre.  
  
Az árlisták szerepkörökre és költségkategóriákra támaszkodnak, így árlisták létrehozása előtt ellenőrizze, hogy konfigurálta-e már a szerepköröket és kategóriákat, amelyeket használni kíván az árlista létrehozása előtt.  
  
1.  Lépjen a **Project Service > Árlisták** pontba.  
  
2.  Kattintson az **Új** elemre.  
  
3.  A **Környezet** pontban válassza ki, hogy az árlistát mihez hozza létre: **Költség**, **Beszerzés** vagy **Értékesítés**.  
  
4.  A **Név** mezőben adjon egy nevet az árlistának.  
  
5.  A **Pénznem** mezőben válassza ki a pénznemet, amelyet a számlázáshoz vagy költségszámításhoz kíván használni.  
  
6.  Az **Időegység** mezőben adja meg az időszakot, amelyre az ár vonatkozik, például nap vagy óra.  
  
7.  Töltse ki a **Kezdő dátum**, **Befejező dátum** és **Leírás** mezőket szükség szerint.  
  
8.  Kattintson a **Mentés** gombra a bejegyzés létrehozásához, hogy folytathassa a szerkesztést.  
  
9. Szerepkörár árlistához való hozzáadásához kattintson a **+** lehetőségre a **Szerepkörárak** alatt.  
  
10. A **Szerepkörár** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra. Folytassa a szerepkörárak hozzáadását, ameddig szükséges. Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.  
  
11. Költségkategória-ár árlistához való hozzáadásához kattintson a **+** lehetőségre a **Kategóriaárak** alatt.  
  
12. A **Tranzakciókategória-ár** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra. Folytassa a kategóriaárak hozzáadását, ameddig szükséges. Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.  
  
13. Árlistaelemek árlistához való hozzáadásához kattintson a **+** lehetőségre az **Árlistaelemek** alatt.  
  
14. Az **Árlistaelem** panelen adja meg a részleteket, majd kattintson a **Mentés** gombra. Folytassa az árlistaelemek hozzáadását, ameddig szükséges. Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.  
  
15. Területi kapcsolatok árlistához való hozzáadásához kattintson a **+** lehetőségre a **Területi kapcsolatok** alatt.  
  
16. Az **Új kapcsolat** ablakban adja meg a részleteket, majd kattintson a **Mentés** gombra. Folytassa a területi kapcsolatok hozzáadását, ameddig szükséges. Amikor végzett kattintson a **Mentés** gombra a képernyő jobb alsó sarkában.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Project Service Automation konfigurálása](../project-service/configure.md)
