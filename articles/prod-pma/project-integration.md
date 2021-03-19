---
title: Microsoft Project Client integráció
description: A projektek ütemezésének tervezése és karbantartása összetett lehet, így a projektmenedzsereknek a feladat kezelését segítő eszközöket kell használniuk. A Microsoft Project Client programmal történő integráció segítséget nyújt a projekt munkalebontási struktúrájának megnyitásához és kezeléséhez.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289327"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client integráció

[!include [banner](../includes/banner.md)]

A projektek ütemezésének tervezése és karbantartása összetett lehet, így a projektmenedzsereknek a feladat kezelését segítő eszközöket kell használniuk. A Microsoft Project Client programmal történő integráció segítséget nyújt a projekt munkalebontási struktúrájának megnyitásához és kezeléséhez. A projektmenedzser bármilyen változást közzétehet a Dynamics 365 Finance projekt munkalebontási szerkezetében.

> [!NOTE]
> A júliusi frissítés (10.0.4 verzió) használata esetén a KB 4054797 és 4055884 telepítése szükséges.

## <a name="configure-the-microsoft-project-client-add-in"></a>A Microsoft Project Client bővítmény konfigurálása
A Microsoft Project Client programmal való integráció engedélyezéséhez egy Microsoft Dynamics 365-bővítményt kell telepíteni a felhasználó kliensének Microsoft Project alkalmazásba. Ezt a **Projektmenedzsment-munkaterület** megnyitásával teheti meg.

•   Kattintson a **Projektkliens-bővítmény konfigurálása** lehetőségre a **Hivatkozások** > **Beállítás** szakaszban a munkaterületen.

•   Kattintson a **Megnyitás** lehetőségre, majd kattintson a **Futtatás** lehetőségre, amikor a rendszer rákérdez.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>A meglévő vázlat munkalebontási struktúra megnyitása és módosítása a Microsoft Project Client alkalmazásban
Ha egy Dynamics 365 Finance projekthez már létrehoztak egy munkalebontási struktúrát, akkor a munkalebontási struktúra megnyitható a Microsoft Project Client alkalmazásban, ha a munkalebontási struktúra vázlat állapotú. A **Projekt** oldalról való megnyitáshoz kattintson a **Megnyitás Microsoft Project alkalmazásban** hivatkozásra a **Terv** lapról. Ez az oldal megnyitható a Microsoft Project Client alkalmazásból is a **Megnyitás** lehetőségre kattintva a **Microsoft Dynamics 365** lapon. Válassza a **Jogi entitás** és a **Projekt** elemet a listáról.

> [!NOTE]
> Ha Internet Explorer böngészőt használ, kattintson a **Mentés** gombra, hogy a fájl letöltési helyéről manuálisan meg tudja nyitni a fájlt. Másik lehetőségként a **Mentés és megnyitás** gombra kattintva nyissa meg a fájlt a Microsoft Project Client programban. Mentéskor ne nevezze át a fájlt.

Mielőtt a Microsoft Project Client program segítségével szerkeszti a fájlt, ki kell vennie azt. Kattintson **Kivétel** lehetőségre a **Microsoft Dynamics 365** lapon. Ezzel megakadályozhatja, hogy több felhasználó egyidejűleg szerkessze a munkalebontási struktúrát a Finance rendszerből. Ha bármilyen módosítás befejezése után közzé szeretné tenni a munkalebontási struktúrát, akkor kattintson a **Beadás** lehetőségre a **Microsoft Dynamics 365** lapon.

Ha egy projektcsapat már hozzá van adva a projekthez a Finance rendszerben, akkor a program a csoport tagjaival tölti fel az erőforráslistát. Ha egy projektcsapat még nincs hozzáadva a projekthez, akkor kiválaszthat erőforrásokat, és összeállíthatja a csapatot a Microsoft Project Client alkalmazásban az **Erőforrások** gombra kattintva a **Microsoft Dynamics 365** lapon. 

A bejelentkezési folyamat részeként a következő adatok kerülnek visszaszinkronizálásba a Finance alkalmazásba:

•   Feladat neve

•   Kezdő dátum

•   Befejezési dátum

•   Megelőző tevékenységek

•   Erőforrásnevek

•   Kategória

•   Erőforrás-kategória

•   Munkaórák

•   Megjegyzések

•   Prioritás

> [!NOTE]
> Ha további oszlopokat ad hozzá a Microsoft Project Client fájlhoz, akkor a program ezeket a fájlokat nem menti a fájlba, és a fájl ismételt megnyitásakor nem fog megjelenni.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Meglévő projekt munkalebontási struktúrájának létrehozása a Microsoft Project Client használatával
Új munkalebontási struktúra létrehozásához a Microsoft Project Client használatával, tegye a következőket:


1.  Nyissa meg a Microsoft Project Client alkalmazást.

2.  A **Microsoft Dynamics 365** lapon kattintson a **Megnyitás** lehetőségre.

3.  Válassza ki a projekt **Jogi entitását**.

4.  Válassza ki a **Projekt** lehetőséget.

5.  Kattintson a **Kivétel** lehetőségre a **Microsoft Dynamics 365** lapon.

6.  Ha készen áll a közzétételre a Finance rendszerbe, akkor kattintson **Beadás** lehetőségre a **Microsoft Dynamics 365** lapon.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Meglévő projekt meglévő munkalebontási struktúrájának cseréje a Microsoft Project Client használatával
Ha új munkalebontási struktúrát szeretne létrehozni a Microsoft Project Client segítségével, és lecserélni egy meglévő projekt meglévő munkalebontási struktúráját, hajtsa végre a következő lépéseket:

1.  Nyissa meg a Microsoft Project Client alkalmazást.

2.  Hozzon létre egy ütemezést a Microsoft Project Client alkalmazásban.

3.  A **Microsoft Dynamics 365** lapon kattintson a **Változtatások mentése** > **Meglévő projekt cseréje** lehetőségre.

4.  Válassza ki a projekt **Jogi entitását**.

5.  Válassza ki a **Projekt** lehetőséget.

6.  Kattintson az **OK** gombra.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Új projekt létrehozása a Microsoft Project Client alkalmazásból


1.  Nyissa meg a Microsoft Project Client alkalmazást.

2.  Hozzon létre egy ütemezést a Microsoft Project Client alkalmazásban.

3.  A **Microsoft Dynamics 365** lapon kattintson a **Változtatások mentése** > **Mentés új projektbe** lehetőségre.

4.  Válassza ki a projekt **Jogi entitását**.

5.  Szükség esetén adja meg a **Projektazonosító** elemet.

6.  Adja meg a **Projektnév** elemet.

7.  Válassza ki a **Projekttípus**, a **Projektcsoport** és a **Projektszerződés azonosítója** elemeket. Másik lehetőségként új projektszerződés is létrehozható az **Új** elemre kattintva.

8.  Válassza ki az erőforrás biztosításához használt **Naptár** elemet.

11. Kattintson az **OK** gombra.


[!INCLUDE[footer-include](../includes/footer-banner.md)]