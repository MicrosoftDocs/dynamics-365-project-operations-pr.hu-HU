---
title: Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában
description: Ez a cikk a Microsoft Dynamics 365 Project Service Automation Update Release 38, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915188"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a cikk felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 38-os frissítési kiadásában. Ennek a verziónak a buildszáma V3.10.59.117, és általában 2021 decemberében önfrissítéssel érhető el.

## <a name="update-release-38"></a>38-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Kivétel történik, amikor jóváhagyási készlet naplóinak hossza meghaladja a 100 000-et.
- A felhasználók nem férhetnek hozzá az **Időbevitel** rácshoz az **Időbevitel** főoldalán.
- Az **Időbevitel importálása** párbeszédpanelen nem jelenik meg szöveg, ha egyetlen elem sem jogosult az importálásra.
- A felhasználók létrehozhatnak jóváhagyási csoportokat, ahol a **Célállapot** mező állapota **Ismeretlen**.

**Projektmenedzsment**

- A téli időszámítás kezdetekor nem jelennek meg megfelelően a kontúrok az erőforrás-hozzárendelésekhez UTC (+09:30) és UTC (+10:00) hozzárendelésében.
- A munkalebontási struktúrákhoz szükséges **További oszlop** mező néhány területi változatban rejtett.
- A **Projektfeladat** rácsban a naptárvezérlő dátumválasztója nincs megfelelően honosítva kínai nyelvre.

**Értékesítés**

- A **Szerződési teljesítmény** és a **Projekt tényleges költsége** értékei nem egyeznek meg, ha a különböző szerződő egységekkel és pénznemekkel rendelkező foglalható erőforrások időbejegyzéseket küldenek be.
- A számlák automatikus megerősítése egyéni munkafolyamat meghiúsul, amikor a számlák importálása felügyelt megoldásként történik. A következő üzenet jelenik meg: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Érvénytelen számlaállapot.”
- Ha a **Gyökér** van kiválasztva az összesítési lehetőségként, és a projekt a tranzakciókatosztályok keverékéből (például idő, költség és anyagbecslések kombinációjából) származó becslésekkel rendelkezik, a rendszer egyetlen díjsorként összesít a tranzakcióosztályokat.
- Olyan helyzetekben, amikor még a szerződéssor projekthez való társítása előtt hozzáadnak egy költségsort, az **Ár frissítése** mezőben nincs megadva alapértelmezett értékként a helyes árképzést.
- Negatív értékesítési összegek nem engedélyezettek a **Projekt** és a **Feladat** entitáson.
