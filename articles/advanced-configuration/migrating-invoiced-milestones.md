---
title: Teljesen számlázott számlázási mérföldkövek áttelepítése a cutoverkor
description: Ez a témakör bemutatja, hogyan lehet áttelepíteni azokat a rögzített árú számlázási mérföldköveket, amelyeket az élő adás dátuma előtt számláztak ki a vevőnek a nyitott projektszerződésekért.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576273"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Teljesen számlázott számlázási mérföldkövek áttelepítése a cutoverkor

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="scenario"></a>Forgatókönyv

Contoso élesedik a Microsofttal Dynamics 365 Project Operations az erőforrásokkal/nem feltöltött forgatókönyvekkel kapcsolatban. Az átállási tevékenységek részeként a végrehajtó csapatnak át kell telepítenie a nyitott projektszerződéseket a régi rendszerből. Egyes projektszerződések olyan szerződéssorokat tartalmaznak, amelyek rögzített árú számlázási módszert használnak, és amelyeket már részben kiszámláztak a végfelhasználónak. A végrehajtó csapatnak át kell migrálnia ezeket a számlázási mérföldköveket vevőszámla **feladásaként**, mert bevételelszámolási célokból szerepelniük kell a teljes szerződésértékben. A Kinnlevőségek és a Főkönyv vevői egyenlegeit azonban ez nem érintheti.

## <a name="solution"></a>Megoldás

### <a name="prerequisites"></a>Előfeltételek

- Dynamics 365 Finance 10.0.24-es vagy újabb verzióját kell telepíteni.
- Annak a környezetnek, ahol az áttelepítési lépéseket végre kell hajtani, karbantartási módban kell lennie. A mérföldkövek áttelepítése közben nem szabad más tevékenységeket végezni.
- Az áttelepítési lépéseket pontosan az itt leírtak szerint kell követni, és csak az átállási tevékenységhez használhatók. A Microsoft nem támogatja ennek a funkciónak a más használatát.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>A Project Operations integrációs szerződéssor mérföldköveinek átírási verziójának létrehozása kettős írási térkép 

1. Győződjön meg arról, hogy a **Projektműveletek integrációs szerződéssor mérföldkövei entitás célleképezése** naprakész. 

    1. A Pénzügy területen keresse fel az **Adatkezelési** \> **adatok entitásokat**, és válassza ki a **Project Operations integrációs szerződéssor mérföldkövei entitást.** 
    2. Válassza **a Célleképezések** módosítása lehetőséget. 
    3. A Térkép átmeneti sorrendje a céllapra **lapon válassza a** Hozzárendelés **létrehozása lehetőséget**, majd ellenőrizze, hogy létre kívánja-e hozni a hozzárendelést.

2. Állítsa le és frissítse a **Project Operations integrációs szerződéssor mérföldköveit** (**msdyn\_ contractlinescheduleofvalues**) kettős írási térképet. 

    1. Nyissa meg az **Adatkezelés** \> **kettős írás lehetőséget**, válassza ki a térképet, és nyissa meg annak részleteit. 
    2. Válassza a Leállítás **lehetőséget**, és várja meg, amíg a rendszer leállítja a térképet. 
    3. Válassza a Táblázatok frissítése **lehetőséget**.

3. Adjon hozzá hozzárendelést a tranzakció állapotához.

    1. Válassza a Hozzárendelés hozzáadása **lehetőséget**.
    2. Az új sorban a **Pénzügy és műveletek alkalmazások** oszlopban válassza ki a **TRANSSTATUS \[TRANSSTATUS\]** mezőt.
    3. Az oszlopban válassza az **Microsoft Dataverse** msdyn **invoicestatus \_ Számla állapotát\[\]**.
    4. **A Térkép típusa** oszlopban jelölje ki a jobb oldali nyilat (**\>**).
    5. A megjelenő párbeszédpanel Irány szinkronizálása **mezőjében válassza** a **Dataverse Pénzügy és műveletek alkalmazás lehetőséget**.
    6. Válassza az Átalakítás hozzáadása **lehetőséget**.
    7. Az Átalakítás típusa mezőben válassza az **Értéktérkép lehetőséget** **.**
    8. Válassza az Értékleképezés hozzáadása **lehetőséget**.
    9. A bal oldali mezőbe írja be **a 4 értéket**. A jobb oldali mezőbe írja be **a 192350001**. 
    10. Válassza **a Mentés** lehetőséget, majd zárja be a párbeszédpanelt.

4. Válassza a Mentés másként **lehetőséget** a kettős írási térkép verziójának mentéséhez. 
5. **A Tábla** hozzáadása ablaktáblán a Publisher **mezőben válassza az** Alapértelmezett közzétevő **lehetőséget**.
6. **A Verzió** mezőbe írja be a verziót.
7. **A Leírás** mezőbe írjon megjegyzést a térkép ezen átvágási verziójáról. 
8. Válassza a **Mentés** parancsot.
9. Indítsd el a térképet.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Számlázott mérföldkövek áttelepítése a Dataverse környezetbe

1. A Projektműveletek Dataverse környezetben hozzon létre olyan mérföldköveket, amelyek számlaállapota **Számlázásra** kész. Ezen a ponton ne telepítsen át olyan mérföldköveket, amelyeket még nem számláztak ki.

    > [!NOTE]
    > A számlázási mérföldkövek áttelepítése előtt győződjön meg arról, hogy a projektszerződés-sorhoz kapcsolódó pénzügyi dimenziók a várt módon vannak beállítva. A pénzügyi dimenziók nem szerkeszthetők az áttelepítés befejezése után.

2. Az összes mérföldkő áttelepítése után állítsa le a következő kettős írású térképeket:

    - Projektműveletek integrációs szerződéssorának mérföldkövei (msdyn\_ contractlineschedule ofvalues)
    - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
    - Projektszámla-ajánlat V2 (számlák)

    A térképek leállításához hajtsa végre az alábbi lépéseket:

    1. A Pénzügy területen keresse fel az **Adatkezelés** \> **kettős írást**, válasszon ki egy térképet, és nyissa meg annak részleteit.
    2. Válassza a Leállítás **lehetőséget**, és várja meg, amíg a rendszer leállítja a térképet.

3. A Project Operations Dataverse környezetben hozzon létre és erősítse meg a számlázási mérföldkövek pro-forma számláit. 

    1. A helytérképen nyissa meg a projektszerződéseket, jelölje ki a szerződéseket, majd válassza a Számlák **létrehozása lehetőséget**.
    2. A számlák létrehozása után nyissa meg őket a **helytérkép Számlák** menüjéből, majd válassza a Megerősítés **lehetőséget**.

    Ez a lépés létrehozza a szükséges rekordokat a Dataverse környezetben. Ez azonban nem befolyásolja a pénzügyi és számlaköveteléseket, mert a korábban felsorolt kettős írású térképeket leállították.

4. Miután az összes pro-forma számlát megerősítették, állítsa vissza az összes kettős írási térképet a kezdeti állapotukba.

    1. Frissítse a Project Operations integrációs szerződéssor **mérföldköveinek** (**msdyn\_ contractlinescheduleofvalues**) kettős írási térképének verzióját az eredetire. 
    2. Jelölje ki a kettős írási térképet a térképlistában, válassza **a Táblázattérkép verzióját**, majd válassza ki a táblázattérkép eredeti verzióját.
    3. Válassza a **Mentés** parancsot.
    4. Indítsa újra a következő kettős írású térképeket:

        - Projektműveletek integrációs szerződéssorának mérföldkövei (msdyn\_ contractlineschedule ofvalues)
        - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
        - Projektszámla-ajánlat V2 (számlák)

A mérföldkövek áttelepítése most megtörtént, és a rendszer készen áll az átállási tevékenység következő lépéseire.
