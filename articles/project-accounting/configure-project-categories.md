---
title: Projektkategóriák konfigurálása
description: Ez a cikk a projektkategóriák beállításával kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 440fc712750c07e8426d54e3a1f994f506879e3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933587"
---
# <a name="configure-project-categories"></a>Projektkategóriák konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Project Operations megbízható lehetőségeket biztosít a projektek bevételeinek és kiadásainak kategorizálására. A kategóriák lehetőséget nyújtanak a projekttranzakciók jelentésére és elemzésére, valamint a főkönyvbe való beküldésre.

A következő ábra a tranzakciók kategóriái, a megosztott kategóriák és a projektkategóriák közötti korrelációt szemlélteti. 

A tranzakciós kategóriák a projekttranzakciók alapvető csoportosítása. Az adott csoportosításon belül van egy sor megosztott kategória, amelyek az alkalmazások és modulok között megoszthatók. Részletesebben vizsgálva a projektkategóriák a legrészletesebb szintű kategóriák. A projektkategóriák a jogi entitásra, a modulra és az alkalmazásra vonatkoznak.

![A tranzakciók kategóriái, a megosztott kategóriák és a projektkategóriák közötti korreláció.](media/project-categories.png)

## <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciós kategóriák a projekttranzakciók alapvető csoportosítását jelentik, és nem vállalat- vagy tranzakciótípus-specifikusak. A Contoso Robotics például tervezési, utazási, telepítési és szolgáltatási tranzakciós kategóriákat használ a projekttranzakciók csoportosításához.

A tranzakciós kategóriákat a Project Operations modul definiálja. 
1. Az űrlap megnyitásához lépjen a **Beállítások** \> **Tranzakciós kategóriák** menüpontra. 
2. Hozzon létre új tranzakciós kategóriát akár az **Új** lehetőség választásával, vagy az **Importálás az Excelből** kiválasztásával.

## <a name="shared-categories"></a>Megosztott kategóriák

A Dynamics 365 a Megosztott kategóriák koncepciót használja a költségek kategorizálására különböző alkalmazásokban, például Dynamics 365 Finance, Dynamics 365 Ellátási lánc és Dynamics 365 Project Operations. Minden létrehozott tranzakciós kategória esetében a Project Operations automatikusan négy kapcsolódó megosztott kategóriát hoz létre: az órákat, a költségeket, a díjakat és a cikkeket. A megosztott kategóriákat áttekintheti és módosíthatja, ha a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Megosztott kategóriák** menüpontra lép.

## <a name="project-categories"></a>Projektkategóriák

A projektkategóriák a kategória konfigurációjának legrészletesebb szintjét jelentik, és ezeket külön kell konfigurálni mindegyik vállalatnál egy projektkönyvelőnek.

1. Nyissa meg a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Projektkategóriák** menüpontot.
2. Válassza az **Új** lehetőséget.
3. Válassza ki az előző szakaszban létrehozott megosztott kategória **Kategóriaazonosító** elemét. A Project Operations csak azoknak a megosztott kategóriáknak a használatát engedélyezi, amelyek tranzakciós kategóriákhoz vannak társítva.
4. Válasszon kategóriacsoportot.

## <a name="category-groups"></a>Kategóriacsoportok

A kategóriacsoportok segítségével megoszthatók a tulajdonságok, elsősorban a feladási profilok a kapcsolódó projektkategóriák között. Az egyes tranzakciótípusok mindegyikéhez legalább egy kategóriacsoport szükséges, és minden egyes projektkategóriához egy csoport tartozik.

A Project Operationsben szereplő könyvelési előírásokat a projekt költség- és bevételi profiljának szabályai, a projektkategóriák és a kategóriacsoportok határozzák meg. A kategóriacsoportok a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Kategóriák** \> **Kategóriacsoportok** segítségével állíthatók be.


[!INCLUDE[footer-include](../includes/footer-banner.md)]