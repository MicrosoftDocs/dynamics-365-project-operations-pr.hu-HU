---
title: Nem készletezett anyagok rendelése projekthez a projekt beszerzési rendeléseivel
description: Ez a témakör ismerteti a nem készletezett anyagok rendelését egy projekthez a projekt beszerzési rendeléseivel.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612706"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Beszerzési kategóriák vagy nem raktározott anyagok rendelése projekt beszerzési rendelések használatával

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezet Beszerzési részlege a termékek és szolgáltatások megrendelésének nyomon követésére [megrendelőket](/dynamics365/supply-chain/procurement/purchase-order-overview) használhat. A beszerzési kategóriákra vagy nem raktáron lévő anyagokra vonatkozó beszerzési rendelések egy projekthez rendelhetők. Ezeknek a megrendeléseknek a számlázása rögzíti a költséget a projekttel szemben.

## <a name="prerequisites"></a>Előfeltételek
A következő lépésekkel engedélyezheti a projektmegrendelők funkciót.

1. A Dynamics 365 Finance nyissa meg a **Szolgáltatáskezelés** munkaterületet.
2. Keresse meg és jelölje ki a **Projektmegrendelők engedélyezése a Project Operationsben erőforrásalapú / nem készletezett forgatókönyveknél**.
3. Válassza ki az **Engedélyezés** lehetőséget.
4. Állítsa be a nem készletezett anyagokat és a függőben lévő szállítói számlákat a [Nem készletezett anyagok és a függőben lévő szállítói számlák konfigurálása](configure-materials-nonstocked.md) részben leírtak szerint.
5. Beszerzési kategóriák konfigurálása a Beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal című témakörben [leírtak szerint](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Projektmegrendelő létrehozása a projektmegrendelők listájából

1. A Finance-ben válassza ki a **Projektvezetés és könyvelés** > **Projektek** > **Minden projekt** lehetőséget, és válasszon ki egy projektet.
2. A Műveleti panelen, a **Kezelés** lapon az **Új** csoportban válassza a **Cikkfeladat** > **Megrendelő** lehetőséget.
3. A **Megrendelés létrehozása** lapon jelölje ki azt a szállítót, akihez a megrendelést les szeretné adni, adja meg a szükséges egyéb adatokat, majd kattintson az **OK** gombra.
4. A **Beszerzési rendelés** lapon a **Megrendelő sorok** rácsban válassza a **Sor hozzáadása** lehetőséget.
5. Adjon meg egy cikkszámot vagy beszerzési kategóriát, mennyiséget, egységet, egységárat és egyéb információkat, adott esetben.

    > [!NOTE]
    > Csak beszerzési kategóriák, nem raktározott cikkek és szolgáltatások használhatók projekt beszerzési rendelésekkel. A raktározott elemek nem támogatottak.

6. Szükség szerint továbbra is hozzáadhat cikkeket vagy beszerzési kategóriákat, és erősítse meg a beszerzési rendelést.

    Az áruk és szolgáltatások visszaigazolása a termék átvételi elismervényének létrehozásával és közzétételével rögzíthető.

    > [!NOTE]
    > A rendszer nem rögzíti a termékelismervényeket a projekt tényadatai között a Microsoft Dataverse-ben, és nem befolyásolják a projekt analitikusnaplóját.

    Miután egy szállító elküldi a megrendelésen szereplő tételekhez és szolgáltatásokhoz tartozó számlát, a részleg le tudja generálni a megrendelés számláját a **Számla** > **Generálás** > **Számla** menüben a műveleti panelen. A függőben lévő szállítói számlákról további tudnivalókat a [Nem készletezett anyagok vásárlása függőben lévő szállítói számla használatával](pending-vendor-invoices.md) oldalon talál.
