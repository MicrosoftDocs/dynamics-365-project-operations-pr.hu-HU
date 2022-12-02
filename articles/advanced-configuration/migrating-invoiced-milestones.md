---
title: Teljesen számlázott számlázási mérföldkövek áttelepítése az átállás során
description: Ez a cikk ismerteti, hogyan lehet áttelepíteni a rögzített árú számlázási mérföldköveket, amelyek számlázva lettek az ügyfélnek a megnyitott projektszerződésekhez az élesítési dátum előtt.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028705"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Teljesen számlázott számlázási mérföldkövek áttelepítése az átállás során

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="scenario"></a>Forgatókönyv

A Contoso éles üzemre vált a vissza a Microsoft Dynamics 365 Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekkel. Az átállási tevékenységek részeként a megvalósítási csoportnak át kell telepítenie a régi rendszerből a nyitott projektszerződéseket. Egyes projektszerződéseknek vannak olyan szerződéssorai, amelyek a rögzített árú számlázási módot használják, és már részben ki lettek számlázva a végfelhasználónak. A megvalósítási csoportnak tehát át kell telepítenie ezeket a számlázási mérföldköveket **Közzétett ügyfélszámla** státusszal, mert ezeknek szerepelnie kell teljes szerződésértékben bevétel felismerési célokból. Azonban ez nem érintheti a Követelések és az Általános főkönyv ügyfélegyenlegeit.

## <a name="solution"></a>Megoldás

### <a name="prerequisites"></a>Előfeltételek

- A Dynamics 365 Finance 10.0.24-es vagy újabb verzióját kell telepíteni.
- A környezetnek, ahol az áttelepítési lépéseket végre kell végrehajtani, karbantartás módban kell lennie. A mérföldkövek áttelepítése közben nem szabad egyéb tevékenységeket végrehajtani.
- Az áttelepítési lépéseket pontosan az itt leírtak szerint követni kell , és csak az átállási tevékenységhez használható. A Microsoft a képesség semmilyen más felhasználását nem támogatja.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Átállási verzió létrehozása Project Operations integráció szerződéssor-mérföldkövek kettős írású leképezéséből 

1. Ügyeljen arra, hogy a **Project Operations integráció szerződéssor mérföldkövek** entitásának célleképezése naprakész legyen. 

    1. A Pénzügyben menjen az **Adatkezelés** \> **Adatentitások** szakaszhoz, és válassza ki a **Project Operations integráció szerződéssor mérföldkövek** entitását. 
    2. Válassza a **Célleképezések módosítása** lehetőséget. 
    3. A **Előkészítés hozzárendelése célhoz** oldalon válassza a **Leképezés generálása** lehetőséget, majd erősítse meg, hogy szeretné legenerálni a leképezést.

2. Állítsa le, és frissítse a **Project Operations integráció szerződéssor-mérföldkövei** (**msdyn\_contractlinesscheduleofvalues**) kettős írású leképezést. 

    1. Nyissa meg az **Adatkezelés** \> **Kettős írás** menüpontot, válassza ki a leképezést, és nyissa meg a részleteit. 
    2. Válassza a **Leállítás** lehetőséget, és várja meg, amíg a rendszer leállítja a leképezést. 
    3. Válassza a **Táblák frissítése** lehetőséget.

3. Adjon leképezést a tranzakcióállapothoz.

    1. Válassza ki a **Leképezés hozzáadása** lehetőséget.
    2. Az új sorban a **Pénzügyi és műveleti alkalmazások** oszlopban jelölje ki a **TRANSSTATUS \[TRANSSTATUS\]** mezőt.
    3. Válassza a **Microsoft Dataverse** oszlopban az **msdyn\_invoicestatus \[Invoice status\]** elemet.
    4. A **Leképezés típusa** oszlopban válassza a jobb nyíl (**\>**) elemet.
    5. A megjelenő párbeszédpanel **Szinkronizálás iránya** mezőjében válassza a **Dataverse – Pénzügyi és műveleti alkalmazások** lehetőséget.
    6. Válassza az **Átalakítása hozzádása** lehetőséget.
    7. Az **Átalakítás típusa** mezőben válassza a **ValueMap** lehetőséget.
    8. Válassza az **Értékleképezés hozzáadása** lehetőséget.
    9. A bal oldali mezőbe írja be: **4**. Az jobb oldali mezőbe írja be: **192350001**. 
    10. Válassza a **Mentés** gombot, majd zárja be a párbeszédpanelt.

4. A kettős írású leképezés verziójának mentéshez válassza a **Mentés másként** lehetőséget. 
5. A **Tábla hozzáadása** panel **Közzétevő** mezőjében válassza az **Alapértelmezett közzétevő** lehetőséget.
6. A **Verzió** mezőben adja meg a verziót.
7. A **Leírás** mezőben írjon be egy megjegyzést a leképezés ezen átállási verziójáról. 
8. Válassza a **Mentés** parancsot.
9. Indítsa el a leképezést.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Számlázott mérföldkövek áttelepítése a Dataverse-környezetbe

1. A Project Operations Dataverse-környezetben hozzon létre olyan mérföldköveket amelyek számlázási állapota **Számlázásra kész**. Ezen a ponton ne telepítsen át ki nem számlázott mérföldköveket.

    > [!NOTE]
    > A számlázási mérföldkövek áttelepítése előtt ellenőrizze, hogy a projektszerződéssorhoz kapcsolódó pénzügyi dimenziók a várt módon vannak-e beállítva. A pénzügyi dimenziók nem szerkeszthetők az áttelepítés befejezése után.

2. Az összes mérföldkő áttelepítése után állítsa le a következő kettős írási leképezéseket:

    - Project Operations integráció szerződéssor mérföldkövek (msdyn\_contractlinescheduleofvalues)
    - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
    - Projektszámla-ajánlat V2 (számlák)

    Az leképezések leállításához kövesse ezeket a lépéseket:

    1. A Finance-ben nyissa meg az **Adatkezelés** \> **Kettős írás** menüpontot, válasszon ki egy leképezést, és nyissa meg a részleteit.
    2. Válassza a **Leállítás** lehetőséget, és várja meg, amíg a rendszer leállítja a leképezést.

3. A Project Operations Dataverse-környezetben hozza létre és erősítse meg a számlázási mérföldkövek számláit. 

    1. Az oldaltérképen menjen a projektszerződésekhez, jelölje ki a szerződéseket, majd válassza a **Számlák létrehozása** lehetőséget.
    2. A számlák létrehozása után nyissa meg őket az oldaltérkép **Számlák** menüjében, majd válassza a **Megerősítés** lehetőséget.

    Ez a lépés hozza létre a Dataverse-környezetben a szükséges rekordokat. Ez azonban nem érinti a pénzügyeket és a követeléseket, mivel a korábban felsorolt kettős írási leképezések le lettek állítva.

4. Miután az összes pro-számla megerősítést nyert, állítsa vissza a kettős írású leképezések mindegyikét a kezdeti állapotukba.

    1. Állítsa le, és frissítse a **Project Operations integráció szerződéssor-mérföldkövei** (**msdyn\_contractlinesscheduleofvalues**) kettős írású leképezést verzióját az eredetire. 
    2. Jelölje ki a leképezéslistában a kettős írású leképezéseket, válassza az **Táblaleképezés verziót**, majd válassza ki a táblaleképezés eredeti verzióját.
    3. Válassza a **Mentés** parancsot.
    4. Indítsa újra az alábbi kettős írású leképezéseket:

        - Project Operations integráció szerződéssor mérföldkövek (msdyn\_contractlinescheduleofvalues)
        - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
        - Projektszámla-ajánlat V2 (számlák)

A mérföldkövek áttelepítése megtörtént, és a rendszer készen áll az átállási tevékenység következő lépéseire.
