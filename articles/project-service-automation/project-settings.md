---
title: A projekt beállításai
description: Ez a témakör információkat nyújt a projektkezelési beállításokról.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752201"
---
# <a name="project-settings"></a>A projekt beállításai

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A következő beállításokkal érheti el a projekttervezési funkciókat.

## <a name="work-template"></a>Munkasablon

A projekt ütemezésének elkészítéséhez létre kell hoznia egy projekt naptársablont, amely meghatározza a napi munkaórák számát és az esetleges szünnapokat. Projekt naptársablon létrehozásához társítson egy munkasablont a projekt **Naptársablon** mezőjéhez. Kövesse az alábbi a lépéseket munkasablon létrehozásához.

1. A PSA-ban a bal oldali navigációs panelen kattintson az **Erőforrások** elemre. 
2. Az **Erőforrások** listaoldalon nyisson meg egy felhasználói rekordot, majd válassza a **Munkaórák megjelenítése** lehetőséget.

  > [!NOTE]
  > Győződjön meg arról, hogy engedélyezte az előugró ablakokat a böngésző oldalán. Ez lehetővé teszi az erőforráshoz beállított munkaórák megtekintését.
  
3. A **Havi nézet** lapon kattintson a **Beállítás** elemre. Megjelenik egy három lehetőséget tartalmazó lista: 

  - Új heti ütemezés
  - Egynapi munkaütemezés
  - Szabadidő

> ![Opciók beállítása](media/project-13.png)

4. Válassza az **Új heti ütemezés** elemet, majd állítsa be az erőforrás ütemezésének opcióit. Beállíthat ismétlődő heti ütemezést, napi óraparamétereket, szünnapokat stb.
5. Állítsa be a dátumtartományt, válassza a **Mentés** lehetőséget, majd kattintson a **Bezár** gombra. 
6. Lépjen vissza az **Erőforrások** listaoldalra, és válassza ki azt az erőforrást, amelyre beállította a munkaórákat. 
7. A munkasablon beállításához válassza a **Naptár beállítása mint** lehetőséget. 
8. A **Munkasablon** párbeszédpanelen adja meg a munkasablon nevét, majd válassza az **Alkalmaz** lehetőséget. 

Most már hozzárendelheti a munkasablont egy projekt naptársablonhoz.

## <a name="resource-roles"></a>Erőforrás-szerepkörök

Az *erőforrás-szerepkör* kifejezés egy sor készséget, kompetenciát és minősítést takar, amelyekre egy személynek szüksége van ahhoz, hogy egy konkrét feladatcsoportot végrehajtson egy projektben. A PSA segítségével kiszámolhatja és kiszámlázhatja az erőforrás idejét az erőforráshoz társított szerepkör alapján. Minden szervezetnek be kell állítania ezeket a szerepköröket a bal oldali navigációs panel segítségével a **Project Service** menüben.

Minden szervezetnek be kell állítania ezeket a szerepköröket az **Aktív erőforráskategóriák** oldalon. Az oldal megnyitásához a bal oldali navigációs panelen válassza a **Erőforrás-szerepkörök** lehetőséget.

## <a name="price-lists"></a>Árlisták

Az árlisták segítségével beállíthatja a költség- és eladási árakat az erőforrás-szerepkörökhöz, a költségkategóriákhoz, a termékekhez és a szervezet más elemeihez. Mielőtt meghatározná a projekthez teljesítendő munkára vonatkozó pénzügyi becsléseket, el kell készítenie egy támogatási költség- és eladási árlistát. A paraméterek szakaszban be kell állítania egy alapértelmezett költség- és eladási árlistát, amely a szervezetben létrehozott projektekre vonatkozik. Az **Aktív projektparaméterek** oldalon ellenőrizze, hogy beállított-e alapértelmezett költség- és eladási árlistát.
