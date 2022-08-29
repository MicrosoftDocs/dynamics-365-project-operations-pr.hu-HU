---
title: Projektállapot szinkronizálása a bezárt projektekbe való belépés megakadályozásához
description: Ez a cikk azt ismerteti, hogyan szinkronizálhatja a Projekt állapotát az inaktív vagy lezárt projektekre való belépés megakadályozása érdekében.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348115"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projektállapot szinkronizálása a bezárt projektekbe való belépés megakadályozásához

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="scenario"></a>Forgatókönyv

Contoso a Microsofttal Dynamics 365 Project Operations együtt él erőforrás-/nem készletezett forgatókönyvekhez. A szokásos üzleti tevékenységek részeként a projektek befejezhetők vagy felfüggeszthetők. Inaktiválhatja a projektet, hogy ne keletkezzen költség vagy számla.

## <a name="solution"></a>Megoldás

### <a name="prerequisites"></a>Előfeltételek

-   Microsoft Dynamics A 365 Finance 10.0.29-es vagy újabb verzióját telepíteni kell.
-   A V2 projektekhez (msdyn\_ projektekhez) tartozó kettős írási térképet 1.0.0.3 az alábbiak szerint kell telepíteni vagy manuálisan konfigurálni.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>A Project Operations integrációs projektek V2 kettős írású térképének frissített verziójának létrehozása

A Project Operations Projects V2 kettős írású térképének frissítése:

1. Lépjen az Adatkezelés **munkaterületre, és válassza a** Kettős írás **lehetőséget**.
2. Válassza a **Kettős írás** csempét.
3. A T **Tábla térkép** oszlopban keresse meg és válassza ki **a Project V2 (msdyn\_ projektek) lehetőséget**, majd válassza a Leállítás lehetőséget.
4. Válassza ki a térkép nevét a térkép megnyitásához, majd válassza a [Nincs] lehetőséget **·**.
5. Az Oszlop kiválasztása párbeszédpanelen válassza **a project statuscode Project Status (Állapot) statecode (Állapotkód) \[lehetőséget\]**, majd kattintson az OK gombra. A lista szűkítéséhez beírhatja **az állapotot** a szűrőértékbe.
6.  Válassza az Átalakítás **hozzáadása vagy szerkesztése lehetőséget** a **térképtípus** oszlopban az átalakítás szerkesztéséhez.
7.  Az **Átalakítás típusa mezőben** válassza a ValueMap **lehetőséget**.
8.  Válassza az Értékleképezés **hozzáadása lehetőséget**, majd adja hozzá a következő **kulcsokat** és **értékeket**:

   Key       | Érték 
   ----------|-------
   InProcess | 0     
   kész | 0     

![Képernyőkép a kettős írású leképezésről](media/projectstage-dw-mapping.png)

9. Válassza a **Mentés** parancsot.
10. A Dual-write > Projects V2 (msdyn_projects) **oldal tetején** válassza a Mentés másként **lehetőséget**.
11. A **Publisher mező Tábla** hozzáadása mezőjében válassza a **CDS Alapértelmezett közzétevő** lehetőséget **.**
12. Állítsa a **Verzió** mezőt 1.0.0.3 értékre.
13. Írjon be egy **Leírást**, majd válassza a Mentés **lehetőséget**.
14. A Dual-write > Projects V2 (msdyn_projects) **oldal tetején válassza a** Futtatás **lehetőséget** a térkép elindításához, majd a **futtatás előtt erősítse meg az Igen** értéket. 

### <a name="close-a-newly-completed-project"></a>Újonnan befejezett projekt bezárása

Dynamics 365 Finance a **projektszakasz** mező segítségével tesz különbséget a folyamatban **lévő vagy** befejezett **projektek** között. **A kész** projektek nem merülhetnek fel költségek, és nem számlázhatók ki az ügyfeleknek.

1. Nyisson meg egy projektet a deaktiváláshoz.
2. A menüszalagon válassza az Inaktiválás **lehetőséget**.

> [!NOTE]
> A projektet inaktiválhatja vagy bezárhatja, mivel mindkettő ugyanúgy fog viselkedni a Finance kontextusában.

3. A Finance (Pénzügyek) területen nyissa meg a **Minden projekt listaoldalt**.
4. Győződjön meg arról, hogy a deaktivált projekt nem jelenik meg a listában.
5. **A lista feletti projektek** megjelenítése szűrőben módosítsa az értéket Aktívról **Mind** értékre **·**.
6. Most látni fogja a deaktivált projektet.

Ha megpróbál időt vagy költséget naplózni ezzel a projekttel kapcsolatban a Finance alkalmazásban, ne tekintse meg a projektet kiválasztásra. Ha manuálisan adja meg a projekt számát egy költséggel kapcsolatban, a következő üzenet jelenik meg: "A projektszakasz befejezve nem teszi lehetővé a felvételt a projektben". A számlázást és az egyéb számlázási funkciókat le kell tiltani, mivel azok egy lezárt projekttel összefüggésben lesznek.

