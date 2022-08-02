---
title: A teljes számlázású számlázási mérföldkövek áttelepítése átálláskor
description: Ez a cikk azt ismerteti, hogyan migrálhatja azokat a rögzített árú számlázási mérföldköveket, amelyeket az élő adás dátuma előtt számláztak ki a vevőnek a nyitott projektszerződésekért.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>A teljes számlázású számlázási mérföldkövek áttelepítése átálláskor

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="scenario"></a>Forgatókönyv

Contoso a Microsofttal Dynamics 365 Project Operations együtt fog élesedni erőforrás-/nem készletezett forgatókönyvekhez. Az átállási tevékenységek részeként a végrehajtó csapatnak át kell telepítenie a nyitott projektszerződéseket a régi rendszerből. A projektszerződések egy része olyan szerződéssorokat tartalmaz, amelyek rögzített árú számlázási módszert használnak, és már részben ki lettek számlázva a végfelhasználónak. A megvalósítási csapatnak át kell telepítenie ezeket a számlázási mérföldköveket a vevői számla **feladásakor**, mert bevétel-felismerési célokból szerepelniük kell a szerződés teljes értékében. A Kinnlevőségekben és a Főkönyvben fennálló vevői egyenlegeket azonban ez nem érintheti.

## <a name="solution"></a>Megoldás

### <a name="prerequisites"></a>Előfeltételek

- Dynamics 365 Finance 10.0.24-es vagy újabb verzióját kell telepíteni.
- A környezetnek, ahol az áttelepítési lépések befejeződnek, karbantartási módban kell lennie. A mérföldkövek áttelepítése során nem szabad más tevékenységeket végezni.
- Az áttelepítési lépéseket pontosan az itt leírtak szerint kell követni, és csak átállási tevékenységhez használhatók. A Microsoft nem támogatja ennek a képességnek a más módon történő használatát.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>A Project Operations integrációs szerződés sor mérföldköveinek kétírásos térképének átvezető verziójának létrehozása 

1. Győződjön meg arról, hogy a **Project Operations integrációs szerződés sorának mérföldkövei entitás célleképezése** naprakész. 

    1. A Pénzügyek területen válassza az **Adatkezelési** \> **adatentitások lehetőséget**, és válassza ki a **Project Operations integrációs szerződéssor mérföldkövek entitást.** 
    2. Válassza a Célleképezések **módosítása lehetőséget**. 
    3. Az Átmeneti leképezés a céloldalra **lapon válassza a** Leképezés **létrehozása lehetőséget**, majd ellenőrizze, hogy létre szeretné-e hozni a leképezést.

2. Állítsa le és frissítse a **Project Operations integrációs szerződés sorának mérföldköveit** (**msdyn\_ contractlinescheduleofvalues**) a kettős írású térképen. 

    1. Lépjen az **Adatkezelés**\> kettős írása **elemre**, válassza ki a térképet, és nyissa meg a részleteit. 
    2. Válassza a Leállítás **lehetőséget**, és várja meg, amíg a rendszer leállítja a térképet. 
    3. Válassza a Táblák **frissítése lehetőséget**.

3. Adjon hozzá egy leképezést a tranzakciós állapothoz.

    1. Válassza a Leképezés **hozzáadása lehetőséget**.
    2. Az új sorban, a **Finance and operations alkalmazások** oszlopban válassza ki a **TRANSSTATUS TRANSSTATUS \[\]** mezőt.
    3. Az oszlopban válassza az **Microsoft Dataverse** msdyn invoicestatus Invoice status (msdyn **invoicestatus \_ Invoice status) lehetőséget\[.\]**
    4. **A Térkép típusa** oszlopban válassza a jobbra mutató nyilat (**\>**).
    5. A megjelenő párbeszédpanelen a Szinkronizálás iránya **mezőben válassza** a **Dataverse Finance and Operations alkalmazások lehetőséget**.
    6. Válassza az Átalakítás **hozzáadása lehetőséget**.
    7. Az Átalakítás típusa **mezőben válassza a** ValueMap **lehetőséget**.
    8. Válassza az Értékleképezés **hozzáadása lehetőséget**.
    9. A bal oldali mezőbe írja be **a 4 értéket**. A jobb oldali mezőbe írja be **a 192350001**. 
    10. Válassza a Mentés **lehetőséget**, majd zárja be a párbeszédpanelt.

4. Válassza a Mentés másként **lehetőséget** a kettős írású térkép verziójának mentéséhez. 
5. **A Tábla** hozzáadása panel Közzétevő **mezőjében válassza az** Alapértelmezett közzétevő lehetőséget.**·**
6. **A Verzió** mezőbe írja be a verziót.
7. **A Leírás** mezőbe írjon be egy megjegyzést a térkép ezen átállásos verziójáról. 
8. Válassza a **Mentés** parancsot.
9. Indítsa el a térképet.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Számlázott mérföldkövek áttelepítése a Dataverse környezetbe

1. A Project Operations Dataverse környezetben hozzon létre olyan mérföldköveket, amelyek számlaállapota **Készen áll a számlázásra**. Ezen a ponton ne telepítsen át olyan mérföldköveket, amelyek nem lettek kiszámlázva.

    > [!NOTE]
    > A számlázási mérföldkövek áttelepítése előtt győződjön meg arról, hogy a projektszerződés-sorhoz kapcsolódó pénzügyi dimenziók a várt módon vannak beállítva. A pénzügyi dimenziók nem szerkeszthetők az áttelepítés befejezése után.

2. Az összes mérföldkő áttelepítése után állítsa le a következő kettős írású térképeket:

    - Project Operations integrációs szerződés sorának mérföldkövei (msdyn\_ contractlinescheduleuleofvalues)
    - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
    - Projektszámla-ajánlat V2 (számlák)

    A térképek leállításához kövesse az alábbi lépéseket:

    1. A Finance (Pénzügyek) területen lépjen az **Adatkezelés**\> kettős írása **elemre**, válasszon ki egy térképet, és nyissa meg annak részleteit.
    2. Válassza a Leállítás **lehetőséget**, és várja meg, amíg a rendszer leállítja a térképet.

3. A Project Operations Dataverse környezetben hozzon létre és erősítsen meg pro-forma számlákat a számlázási mérföldkövekhez. 

    1. Az oldaltérképen nyissa meg a projektszerződéseket, válassza ki a szerződéseket, majd válassza a Számlák **létrehozása lehetőséget**.
    2. A számlák létrehozása után nyissa meg őket az **oldaltérkép Számlák** menüjéből, majd válassza a Megerősítés **lehetőséget**.

    Ez a lépés létrehozza a szükséges rekordokat a Dataverse környezetben. Ez azonban nem érinti a pénzügyeket és a követeléseket, mert a korábban felsorolt kettős írású térképeket leállították.

4. Miután az összes pro-forma számlát megerősítette, az összes kettős írású térképet vissza kell állítania a kezdeti állapotába.

    1. Frissítse a Project Operations integrációs szerződés sorának mérföldköveinek **(** msdyn **contractlinescheduleofvalues\_) kettős írású leképezésének** verzióját az eredetire. 
    2. Válassza ki a kettős írású térképet a térképlistában, válassza a Táblatérkép verziója **lehetőséget**, majd válassza ki a táblatérkép eredeti verzióját.
    3. Válassza a **Mentés** parancsot.
    4. Indítsa újra a következő kettős írású leképezéseket:

        - Project Operations integrációs szerződés sorának mérföldkövei (msdyn\_ contractlinescheduleuleofvalues)
        - Project Operations integrációjának tényleges adatai (msdyn\_actuals)
        - Projektszámla-ajánlat V2 (számlák)

A mérföldkövek most migrálva vannak, és a rendszer készen áll az átállási tevékenység következő lépéseire.
