---
title: Projektárlisták kezelése projektszerződéseken
description: Ez a témakör információt nyújt a projektárlisták a projektszerződéseken való kezeléséről.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010384"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projektárlisták kezelése projektszerződéseken

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations alkalmazásban a projektekszerződések segítségével több dátumon érvényes értékesítési árlistákat lehet támogatni egy szerződéshez. A Project Operations alkalmazásban egy új a **Projektárlisták** nevű új társított entitás is van. Ez az entitás egy-a-többhöz kapcsolatban van egy projektszerződéssel.

A projektárlisták a projekt idő-, anyag- és költségtranzakcióinak árazására használhatók. Ha egy szerződés egy vagy több projektárlistával rendelkezik, akkor ezek az árlisták a szerződéssoron keresztül a szerződéshez társított projektek idő-, anyag-, költségbecslései és tényadatai árazására használhatók.

Ha egy projektszerződésen nincsenek projektárlisták, figyelmeztető üzenet jelenik meg arról, hogy a naplózott projektárlisták, becslések, tényleges projektmunka, anyag és költségek nem kerülnek beárazásra. Az értékesítési értékekhez nem tartozik majd ár.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Projekt-árlista hozzárendelése vagy hozzárendelésének megszüntetése egy projekt-szerződésben

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Adott árlista létrehozása vagy társítása a projektalapú munka, anyag és költségek becsléséhez

1. Nyissa meg a projektszerződést, és válassza ki a **Projektárlisták** lapot.
2. Az alrácsban válassza a **+ új projektárlista hozzáadása** lehetőséget.
3. A **Gyorslétrehozás** csúszkával jelöljön ki egy árlistát. 

  A legördülő listában láthatók az **Értékesítésre** beállított kontextussal rendelkező összes árlista , ahol az árlista pénzneme megegyezik a szerződés pénznemével.
  
4. Adja meg a projekt árlista-hozzárendelésének leírását, válassza a **Mentés** lehetőséget, majd zárja be a **Gyors létrehozás** csúszkát.

   Létrejön egy projektárlista-hozzárendelés.
   
5. Ismételje meg a 1–4. lépéseket, ha egynél több projektárlistát szeretne társítani a projekt szerződéshez. Csak akkor hozzon létre több projekt-árlistát, ha az egyes társított projektárlistákhoz eltérő hatályossági dátum tartozik.

> [!NOTE]
> A Project Operations nem támogatja a projektárlisták hatályossági dátumainak átfedését. Ha egy adott dátummal rendelkező tranzakcióhoz több projekt-árlista is tartozik, akkor a tranzakció ára alapértelmezés szerint nulla lesz.

### <a name="remove-a-project-price-list-association"></a>Projektárlista társításánek eltávolítása

- Jelölje ki a projektárlistát majd válassza az alrácson válassza a **Szerződés projektárlistájának törlése** elemet. 

  A program eltávolítja az árlistát a szerződésből a projekt árlisták listájából. A rendszer nem törli az árlistát. Csak a szerződéshez való társítást törli a rendszer.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>A projektárlisták automatikus alapértelmezésének beállítása a szerződésen

A projekt árlistája beállítható alapértelmezett projektárlistaként. Ez a beállítás biztosítja, hogy a szervezet összes szerződése mindig az adott áridőszakra vonatkozó standard projektárlistával kezdődjön.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>A projektárlisták szervezeti alapértelmezésének beállítása

1. Lépjen a **Beállítások** > **Általános** menüpontra, majd válassza a **Paraméterek** lehetőséget.
2. Az **Aktív paraméterek** listában jelölje ki a bejegyzést, és kattintson rá duplán, a megnyitáshoz. A dupla kattintás során ügyeljen arra, hogy ne kattintson olyan mezőértékre, ami hivatkozás. 
3. Az **Aktív paraméterek** lapon válassza az **Árlista** fület. Egy alrács az alapértelmezett árlisták listáját jeleníti meg. Ez az általános költség-és értékesítési árlisták listája. Ha itt társít egy **Értékesítés** árlistát minden olyan pénznemhez, amelyben értékesít, akkor biztosítható, hogy az értékesítési árlista legyen az alapértelmezett minden olyan szerződésnél, amelyet olyan ügyfelek számára hoz létre, akik ebben a pénznemben kereskednek.

### <a name="set-up-a-customer-specific-project-price-list"></a>Ügyfélspecifikus projektárlista létrehozása

Beállíthat ügyfélspecifikus projektárlistákat is, amikor az ügyfelekkel megkötött egy fő árképzési megállapodást.

1. Válassza az **Értékesítés** > **Ügyfelek** lehetőséget.
2. Válassza ki az aktív partnerek listájából azt az ügyfelet, akihez rendelkezik speciális árlistával.
3. Válassza ki az ügyfélrekordot a megnyitáshoz majd válassza a **Projektárlisták** lapot. Egy alrács az adott ügyfélre vonatkozó projektárlisták listáját jeleníti meg. 
4. Itt hozzon létre egy új árlista-társítást, hogy az adott ügyfélre vonatkozó projektárlista elérhető legyen.

## <a name="custom-pricing-on-a-project-contract"></a>Egyéni árazás egy projektszerződésben

Miután a szervezeti és az ügyfél-specifikus alapértelmezett projektárlistái is vannak, a projekt-szerződések automatikusan létrejönnek ezekkel a projektárlista-hozzárendelésekkel. A projektszerződésben szereplő árlisták azonban mindig a hozzájuk fűzött dátummal és szerződésnévvel vannak másolva. A partner-és projektmenedzserek ezután megkezdhetik az árak szerkesztését ezeken a példányokon. Ezek a módosított árak csak erre a projektszerződésre vonatkoznak.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
