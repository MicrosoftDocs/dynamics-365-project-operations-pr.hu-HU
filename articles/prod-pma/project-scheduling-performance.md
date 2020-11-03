---
title: Projekterőforrás ütemezési teljesítménye
description: Ez a témakör a nagy számú projektre vonatkozó erőforrás-ütemezési teljesítmény javításával kapcsolatban tartalmaz tájékoztatást.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078075"
---
# <a name="project-resource-scheduling-performance"></a>Projekterőforrás ütemezési teljesítménye

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Az erőforrás-ütemezéssel kapcsolatos teljesítményproblémák akkor fordulnak elő, ha a projektek száma eléri a több ezres értéket. Az erőforrás-ütemezési teljesítmény javításához egy funkció érhető el, amely lehetővé teszi, hogy a felhasználók csökkentsék az erőforrás elérhetőségi űrlapjának indításához szükséges időt. Ezzel eltávolítja az erőforrás-kapacitás összesítés-szinkronizálási folyamatát, és a **ResProjectResource** tábla használatával felgyorsítja az erőforrások keresését. Ne feledje, hogy a **ResRollup** táblát a továbbiakban nem használja a rendszer.

> [!IMPORTANT]
> Ha az erőforrás-kapacitás összesítés-szinkronizálási folyamata vagy a **ResProjectResource** tábla függősége fennáll, ne használja ezt a szolgáltatást.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Erőforrás-ütemezési teljesítmény fokozásának engedélyezése
Az erőforrás-ütemezés teljesítménynövelésének engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. Lépjen a **Funkciókezelés** > **Összes** pontra, és a funkciók listájában keresse meg a **Projekterőforrás ütemezésiteljesítmény-növelési funkciójának engedélyezése** elemet.
2. Válassza ki az **Engedélyezés most** lehetőséget.

> [!NOTE]
> Ha nem találja a funkciót a listájában, akkor a lista frissítéséhez jelölje be a **Frissítések keresése** jelölőnégyzetet.

3. Frissítse a böngészőt, majd nyissa meg a **projektmenedzsment és a könyvelés** > **időszakos** > **Projekterőforrások** > **Erőforrásnaptárak kapacitásának szinkronizálása az összes vállalatban**.
4. Állítsa a **Meglévő kapacitásrekordok eltávolítása** beállítást **Igen** értékre a korábbi adatok eltávolításához. Ha növekményes adatokat szeretne létrehozni, akkor állítsa **Nem** értékre.
5. Az **Időszak kódja** mezőben válassza ki, hogy milyen időszakra kell létrehozni az adatot. Ha kiválaszt egy időszakkódot, a kezdő és befejező dátumot nem kell meghatározni.
6. Ha üresen hagyja az **Időszak kódja** mezőt, akkor az adatok generálásához válassza ki a kezdési és a befejezési dátumot.
7. Kattintson az **OK** gombra.

 > [!NOTE]
 > Ezzel az általános adatokat szétotsztja a **ResCalendarCapacity** táblába a környezet minden vállalatában, így a kötegelt feldolgozást csak egy jogi személyben kell futtatni. Az ebben a kötegelt feldolgozásban szereplő adatok szükségesek az erőforrás-kapacitásnak a hozzárendelt naptáron keresztüli kiszámításához.

8. Nyissa meg a **projektmenedzsment és a könyvelés** > **időszakos** > **Projekterőforrások** > **Projekterőforrások kitöltése az összes vállalatban** , majd válassza az **OK** elemet. Ez az adatfrissítési parancsfájl a **ResProjectResource** , a **ResCalendarDateTimeRange** és a **ResEffectiveDateTimeRange** tábláiban lévő általános adatokhoz. A **PSAPRojSchedRole.RootActivity** mező értékeit is frissíti a rendszer. Ha ez nem történik meg, akkor figyelmeztetés jelenik meg, amikor megpróbálja végrehajtani az erőforrás-ütemezési műveleteket.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Erőforrás-ütemezési teljesítmény fokozásának kikapcsolása

1. Lépjen a **Funkciókezelés** > **Összes** pontra, és keresse meg a **Projekterőforrás ütemezésiteljesítmény-növelési funkciójának engedélyezése** elemet.
2. Jelölje ki a funkciót, majd válassza a **Letiltás** gombot.
3. Frissítse a böngészőjét.
4. Nyissa meg a **Projektmenedzsment és könyvelés** > **Időszakos** > **Kapacitás szinkronizálása** > **Erőforráskapacitás-összesítések szinkronizálása** lehetőséget.
5. A **kapacitás-összesítés szinkronizálása** lapon állítsa a **meglévő kapacitásrekordok eltávolítása** beállítást **Igen** értékre a korábbi adatok eltávolításához. Ha növekményes adatokat szeretne létrehozni, akkor állítsa **Nem** értékre.
6. Az **Időszak kódja** mezőben válassza ki, hogy milyen időszakra kell létrehozni az adatot. Ha kiválaszt egy időszakkódot, a kezdő és befejező dátumot nem kell meghatározni.
7. Ha üresen hagyja az **Időszak kódja** mezőt, akkor az adatok generálásához válassza ki a kezdési és a befejezési dátumot.
8. Kattintson az **OK** gombra.

> [!NOTE]
> Ezzel az általános adatokat szétotsztja a **ResRollup** táblába a környezet minden vállalatában, így a kötegelt feldolgozást csak egy jogi személyben kell futtatni. Ez a kötegelt feldolgozás az összes **erőforrás-elérhetőségi** nézet esetében szükséges. Ha a kötegelt feldolgozást nem futtatják le, akkor a **ResRollup** -adatok menet közben jönnek létre, ami időt vesz igénybe.
