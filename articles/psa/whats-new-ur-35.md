---
title: Újdonságok vagy változások a Project Service Automation 35-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 35, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574031"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Újdonságok vagy változások a Project Service Automation 35-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 35-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.56.110, és 2021 szeptemberében egy önfrissítéssel válik általánosan elérhetővé.

## <a name="update-release-35"></a>35-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Idő és költség**

- A projekt jóváhagyója olvasási jogosultsági hibát kap, amikor **Projekt jóváhagyó** szerepkörrel hagyja jóvá a költségbejegyzéseket.
- A projekt jóváhagyója írási jogosultsági hibát kap az **msdyn_projectapproval** fájlban, amikor törli a jóváhagyott időbejegyzést **Projekt jóváhagyó** szerepkörrel.
- Amikor a Dynamics 365 for phone - Project Resource Hub alkalmazásmodulban egy időbejegyzésben a **Hét másolása** opciót választja, a következő hiba lép fel: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Az **Újra megpróbálás** házirend automatikusan jóváhagyja a korábban elutasított bejegyzéseket.
- A **Jóváhagyási készletek** alrács a nem alkalmazható szalagműveleteket mutatja.
- A **Projektfeladat** és az **Erőforrás szerepkör** ikonjai hiányoznak az **Időbejegyzés** egységen.
- Az erőforrás-kijelölések importálásakor az importált időbejegyzések nem a megfelelő időtartamúak a kézi üzemmódú feladatokkal létrehozott megbízások esetében.
- A **Törlés** hiányzik a **Munkaidő-bevételi rekordok speciális keresése** lapról.
- A **Mentés** hiányzik az **Időbejegyzés információs** oldalról. Ez a probléma megakadályozza a módosítások mentését az oldal bezárásakor.

**Projekt tervezése**

- Az **Erőforrás hozzárendelés** és az **Erőforrás egyeztetés** rácsok nem rendezik a csoportosított attribútumokat ábécé szerint.
- Nem lehet feladatokat létrehozni, ha a dátum viselkedése **Csak dátumra** van beállítva.

**Erőforrás-kezelés**

- Ha a Dynamics 365 Field Service és a Project Service Automation is telepítve van, átfedési problémák lépnek fel, amikor az **Erőforrás-szükséglethez kapcsolódó nézet** egy főoldalhoz kapcsolódik.
- Ha a **Csoporttag gyors létrehozása** párbeszédpanelen duplán kattint a **Mentés** gombra, az erőforrásigény nem jön létre.

**Értékesítés**

- A rendszer kivételt dob, ha olyan feladatot töröl, amely olyan árajánlathoz kapcsolódik, amelynek állapota **Elnyert**.
