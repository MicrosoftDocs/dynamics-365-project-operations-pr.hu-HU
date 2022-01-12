---
title: Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 38, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901510"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 38-os frissítési kiadásában. Ez a verzió V3.10.59.117 buildszámmal rendelkezik, és 2021 decemberében általánosan elérhető egy önfrissítéssel.

## <a name="update-release-38"></a>38-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Kivételt képez, ha a jóváhagyási készlet naplóinak hossza meghaladja a 100 000 rekordot.
- A felhasználók nem férhetnek hozzá az **Időbevitel** rácshoz az **Időbevitel** főoldaláról.
- Az **Időbevitel importálása** párbeszédpanel nem jelenít meg szöveget, ha egyetlen elem sem importálható.
- A felhasználók olyan jóváhagyási készleteket hozhatnak létre, ahol a **Célállapot** mező Ismeretlenre van **állítva.**

**Projektmenedzsment**

- A kontúrok nem jelennek meg megfelelően az UTC(+09:30) és az UTC(+10:00) erőforrás-hozzárendelésekben a nyári időszámítás kezdetekor.
- A **munkalebontási struktúrák További oszlop** mezője egyes területi helyeken rejtve van.
- A Projektfeladat rács naptárvezérlőjének **dátumválasztója nincs megfelelően** lokalizálva a kínai nyelvhez.

**Értékesítés**

- **A szerződés teljesítménye** és a projekt tényleges **költségértékei** nem egyeznek meg, ha a különböző beszerzési egységekkel és pénznemekkel rendelkező könyvelhető erőforrások időtételeket küldenek be.
- A számlák automatikus megerősítésére irányuló egyéni munkafolyamat meghiúsul, ha a számlákat felügyelt megoldás importálják. A következő üzenet jelenik meg: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice status."
- Ha **a Root van** kiválasztva összegzési lehetőségként, és a projekt tranzakcióosztályok keverékéből (például idő-, költség- és anyagbecslések kombinációjából) származó becsléseket mutat be, a rendszer egyetlen díjsorként foglalja össze a tranzakcióosztályok közötti összegeket.
- Azokban az esetekben, amikor egy költségsort hozzáadnak, mielőtt egy szerződéssort egy projekthez társítanának, a helyes árképzés nem alapértelmezett értékként ik meg a **Frissítési ár** mezőben.
- A projekt- és tevékenység entitásokon nem engedélyezettek negatív **értékesítési** **összegek**.
