---
title: Nem készletezett anyagok rendelése projekthez a projekt beszerzési rendeléseivel
description: Ez a témakör ismerteti a nem készletezett anyagok rendelését egy projekthez a projekt beszerzési rendeléseivel.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563025"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Nem készletezett anyagok rendelése projekthez a projekt beszerzési rendeléseivel

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezet Beszerzési részlege a termékek és szolgáltatások megrendelésének nyomon követésére [megrendelőket](/dynamics365/supply-chain/procurement/purchase-order-overview) használhat. Megrendelők nem készletezett anyagokhoz hozzárendelhetők egy projekthez. Ezeknek a megrendeléseknek a számlázása rögzíti a költséget a projekttel szemben.

## <a name="prerequisites"></a>Előfeltételek
A következő lépésekkel engedélyezheti a projektmegrendelők funkciót.

1. A Dynamics 365 Finance-ben nyissa meg a **Funkciókezelés** munkaterületet.
2. Keresse meg és jelölje ki a **Projektmegrendelők engedélyezése a Project Operationsben erőforrásalapú / nem készletezett forgatókönyveknél**.
3. Válassza ki az **Engedélyezés** lehetőséget.
4. Állítsa be a nem készletezett anyagokat és a függőben lévő szállítói számlákat a [Nem készletezett anyagok és a függőben lévő szállítói számlák konfigurálása](configure-materials-nonstocked.md) részben leírtak szerint.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projektmegrendelő létrehozása a projektmegrendelők listájából

1. A Finance-ben válassza ki a **Projektvezetés és könyvelés** > **Projektek** > **Minden projekt** lehetőséget, és válasszon ki egy projektet.
2. A Műveleti panelen, a **Kezelés** lapon az **Új** csoportban válassza a **Cikkfeladat** > **Megrendelő** lehetőséget.
3. A **Megrendelés létrehozása** lapon jelölje ki azt a szállítót, akihez a megrendelést les szeretné adni, adja meg a szükséges egyéb adatokat, majd kattintson az **OK** gombra.
4. A **Beszerzési rendelés** lapon a **Megrendelő sorok** rácsban válassza a **Sor hozzáadása** lehetőséget.
5. Adja meg a cikkszámot, mennyiséget, egységet, egységárat és egyéb adatokat igény szerint.

    > [!NOTE]
    > Projektmegrendelőkkel csak a nem készletezett cikkek és szolgáltatások használhatók. A rendszer nem támogatja a készletezett cikkeket és beszerzési kategóriákat.

6. Adja hozzá a további szükséges elemeket, és erősítse meg a megrendelést.

    Az áruk és szolgáltatások visszaigazolása a termék átvételi elismervényének létrehozásával és közzétételével rögzíthető.

    > [!NOTE]
    > A rendszer nem rögzíti a termékelismervényeket a projekt tényadatai között a Microsoft Dataverse-ben, és nem befolyásolják a projekt analitikusnaplóját.

    Miután egy szállító elküldi a megrendelésen szereplő tételekhez és szolgáltatásokhoz tartozó számlát, a részleg le tudja generálni a megrendelés számláját a **Számla** > **Generálás** > **Számla** menüben a műveleti panelen. A függőben lévő szállítói számlákról további tudnivalókat a [Nem készletezett anyagok vásárlása függőben lévő szállítói számla használatával](pending-vendor-invoices.md) oldalon talál.
