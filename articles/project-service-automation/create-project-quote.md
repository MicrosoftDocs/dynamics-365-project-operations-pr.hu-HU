---
title: Projekt árajánlat létrehozása
description: Projektárajánlat létrehozása a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 08ad2d2d-cc4b-4598-93c0-426c7ce1aa8f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: efe4ca78641518058b2ee30f3aa69796709eca83
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752173"
---
# <a name="create-a-project-quote-project-service"></a>Projektárajánlat létrehozása (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Az árajánlatok hasonlóképpen hozhatók létre mint a lehetőségek. A lehetőségek belső felhasználásra szánt információk, az árajánlatokat pedig a lehetséges ügyfelek kapják meg. Egy vagy több árajánlatot is létrehozhat az egyes lehetőségekhez. Amikor árajánlatot készít egy lehetséges ügyfél számára, akkor a projekt **Ajánlattétel** fázisában tart.  
  
1. Ha árajánlatot szeretne létrehozni egy lehetőségből, lépjen a **Project Service > Lehetőségek** pontba, majd kattintson a lehetőségre, amelyhez árajánlatot kíván létrehozni.  
  
2. Kattintson a **Következő fázis** lehetőségre a folyamatsáv jobb oldalán, majd válasszon egy már meglévő árajánlatot, vagy kattintson a **Létrehozás** gombra új árajánlat létrehozásához.  
  
3. Az **Összegzés** területen módosítsa az információkat szükség szerint.  
  
4. Kattintson a **Mentés** gombra az árajánlat létrehozásához, hogy folytathassa a szerkesztést.  
  
5. Egy terméket úgy adhat hozzá egy árajánlathoz, hogy az **Új** lehetőségre kattint a **Termékalapú sorok** részben az **Árajánlatsorok** területen. Jelöljön ki egy elemet a **Termék neve** részben, majd adja meg a mennyiséget, az értékesítési árat és a megajánlott összeget.  
  
6. Egy projektbecslést úgy adhat hozzá egy árajánlathoz, hogy a **+** lehetőségre kattint a **Projektalapú sorok** alatt az **Árajánlatsorok** területen. Adja meg a nevet, a költségvetés összegét és a projektet, ha rendelkezésre állnak. Ha munkalebontási struktúrával rendelkező projektet kell létrehoznia egy becslés előállításához, itt talál segítséget: [Projekt létrehozása](../project-service/create-project.md).  
  
7. Amikor végzett a szerkesztéssel, kattintson a **Mentés** gombra a képernyő jobb alsó részén.  
  
8. Ha készen áll arra, hogy elküldje az árajánlatot az ügyfélnek, kattintson az **Egyebek** (...), **Jelentés futtatása**, majd az **Árajánlat** lehetőségre. Mentse a jelentést [!INCLUDE[pn_ms_Word_short](../includes/pn-ms-word-short.md)]-dokumentumként, végezze el az esetlegesen szükséges szerkesztést, és küldje el az árajánlatot az ügyfélnek.  
  
9. Ha az ügyfél elfogadja az árajánlatot, kattintson a **Lezárás megnyertként** lehetőségre az **Árajánlat** képernyő felső részén. Amennyiben az ügyfél szeretné, ha módosítana néhány elemet, akkor végezze el ismét ezt az egész folyamatot egy új árajánlat létrehozásához. Ha az ügyfél úgy dönt, hogy ez alkalommal nem kívánja igénybe venni az Ön szolgáltatásait, kattintson a **Lezárás elveszítettként** lehetőségre az **Árajánlat** képernyő felső részén.  
  
   Amikor megnyertként zár le egy árajánlatot, a projekt átkerül a **szerződés** fázisba, és a **Projektszerződés** képernyő felkéri, hogy hozzon létre egy szerződést ehhez a projekthez.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Partnerkezelői útmutató](../project-service/account-manager-guide.md)
