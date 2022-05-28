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
ms.reviewer: johnmichalak
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598721"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Újdonságok vagy változások a Project Service Automation 38-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 38-os frissítési kiadásában. Ez a verzió buildszámú V3.10.59.117 rendelkezik, és általában 2021 decemberében önfrissítéssel érhető el.

## <a name="update-release-38"></a>38-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- Kivételt képez, ha a jóváhagyási készletnaplók hossza meghaladja a 100 000 rekordot.
- A felhasználók nem férhetnek hozzá az Időbejegyzés **rácshoz az** **Időbejegyzés** főoldaláról.
- Az **Időbejegyzés importálása** párbeszédpanelen nem jelenik meg szöveg, ha egyetlen elem sem jogosult importálásra.
- A felhasználók olyan jóváhagyási készleteket hozhatnak létre, amelyekben **a** Célállapot **mező értéke Ismeretlen**.

**Projektmenedzsment**

- A kontúrok nem jelennek meg megfelelően az UTC (+09:30) és az UTC(+10:00) erőforrás-hozzárendeléseiben a nyári időszámítás kezdetekor.
- A **munkabontási struktúrák További oszlop** mezője néhány területi beállításban el van rejtve.
- A Projektfeladat **rács naptárvezérlőjének** dátumválasztója nincs megfelelően honosítva a kínai nyelvhez.

**Értékesítés**

- **A Szerződés teljesítménye** és **a Projekt tényleges költség** értékei nem egyeznek meg, ha a különböző szerződési egységgel és pénznemekkel rendelkező könyvelhető erőforrások időtételeket küldenek.
- A számlák automatikus megerősítését célzó egyéni munkafolyamat sikertelen, ha a számlákat felügyelt megoldás importálja. A következő üzenet jelenik meg: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice status."
- Ha **a Gyökér** van kiválasztva összegzési lehetőségként, és a projekt a tranzakcióosztályok keverékéből származó becsléseket tartalmaz (például idő-, költség- és anyagbecslések kombinációjából), a rendszer egyetlen díjsorként foglalja össze a tranzakcióosztályokat.
- Azokban az esetekben, amikor egy költségsor hozzáadódik, mielőtt egy szerződéssort társítanának egy projekthez, a program nem a megfelelő árképzést adja meg alapértelmezett értékként az **Ár** frissítése mezőben.
- A negatív értékesítési összegek nem engedélyezettek a Projekt- és **tevékenységtűrtökön** **.**
