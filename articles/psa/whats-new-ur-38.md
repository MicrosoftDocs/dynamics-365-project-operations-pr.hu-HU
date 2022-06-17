---
title: Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában
description: Ez a cikk a 38-as, V3-as frissítésben Microsoft Dynamics 365 Project Service Automation elérhető funkciókat és javításokat sorolja fel.
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

Ez a cikk a Project Service Automation 38-as, V3-as kiadásának újdonságaival vagy módosításaival kapcsolatos funkciókat és javításokat sorolja fel. Ez a verzió buildszáma V3.10.59.117, és általánosan elérhető egy önfrissítéssel 2021 decemberében.

## <a name="update-release-38"></a>38-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Kivétel akkor fordul elő, ha a jóváhagyási készlet naplóinak hossza meghaladja a 100 000 rekordot.
- A felhasználók nem férhetnek hozzá az Időbevitel **rácshoz az** **Időbevitel** főoldalról.
- Az **Időbevitel importálása** párbeszédpanelen nem jelenik meg szöveg, ha egyetlen elem sem jogosult importálásra.
- A felhasználók jóváhagyási készleteket hozhatnak létre, ahol a **Célállapot** mező Ismeretlen **értékre** van állítva.

**Projektmenedzsment**

- A kontúrok nem jelennek meg megfelelően az UTC(+09:30) és az UTC(+10:00) erőforrás-hozzárendeléseiben, amikor a nyári időszámítás megkezdődik.
- A **munkalebontási struktúrák További oszlop** mezője egyes területi beállításokban el van rejtve.
- A Projekttevékenység **rács naptárvezérlőjének** dátumválasztója nincs megfelelően honosítva a kínai nyelvhez.

**Értékesítés**

- **A szerződésteljesítmény** és **a projekt tényleges költségértékei** nem egyeznek meg, ha a különböző szerződéses egységekkel és pénznemekkel rendelkező foglalható erőforrások időbejegyzéseket küldenek.
- A számlák automatikus megerősítésére szolgáló egyéni munkafolyamat meghiúsul, ha a számlákat felügyelt megoldás ként importálja. A következő üzenet jelenik meg: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Érvénytelen számlaállapot."
- Ha **a Root** van kiválasztva összegzési lehetőségként, és a projekt a tranzakciós osztályok keverékéből (például az idő,a költség és az anyagbecslések kombinációjából) származó becsléseket tartalmaz, a rendszer egyetlen díjsorként összegzi a tranzakciós osztályok között.
- Azokban az esetekben, amikor egy költségsort azelőtt adnak hozzá, hogy egy szerződéssort társítanak egy projekthez, a rendszer nem a megfelelő árképzést adja meg alapértelmezett értékként az **Ár** frissítése mezőben.
- A negatív értékesítési összegek nem engedélyezettek a Projekt **és** a Tevékenység **entitásokon**.
