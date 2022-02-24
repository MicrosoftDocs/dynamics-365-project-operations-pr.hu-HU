---
title: Újdonságok vagy változások a Project Service Automation 15-es frissítési kiadásának V3 változatában
description: Ez a témakör információkat nyújt arról, hogy milyen újdonságok és változások vannak a Project Service Automation 15-ös frissítési kiadásának V3 verziójában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 0ec6746c0d3a1a03ee56440c73d044df844046f8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143966"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation 15-ös frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Dynamics 365 Project Service Automation (PSA) alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez nyissa meg a megoldások oldalt. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a PSA V3. 15-ös frissítési kiadásában. Ennek a verziónak a build száma V 3.10.5.28, és általánosan elérhető egy önálló frissítésben 2020 januárjában.

## <a name="update-release-15"></a>15-ös frissítési kiadás 

### <a name="enhancements"></a>Fejlesztések

- Projektmenedzsment

### <a name="bug-fixes"></a>Hibajavítások

- Idő és költség

  - Javítva: Bővítmény betöltési hibája az egyeztetési nézetben.
  - Javítva: Projekterőforrás-központ: **Mennyiség** átnevezése a többértelműség elkerüléséhez.
  - Javítva: Az **Időbejegyzés másolásához használt oszlopok** módosítása,hogy a típust is tartalmazza.
  - Javítva: Szerkesztés ideje bejegyzés megadása a rácsnézetben decimális számokkal bizonyos számoknál ismeretlen hibát ad.

- Projektmenedzsment

  - Javítva: A **Használata követési nézetben** legördülő menü kibővül a lehetőségek szélességének megfelelően.
  - Javítva: A +13-as időzónában a projektek kezelésekor a feladatszámítások pontatlan eredményeket jeleníthettek meg.
  - Javítva: **Csoporttag befejezési idő** javítva lett 24-órás naptár használata esetén.
  - Javítva: A **BPF** ismét aktiválva az **msdyn_project** fő űrlapon.
  - Javítva: A hozzárendelések kiszámítása immár nem hagy figyelmen kívül egy napot.
  - Javítva: Egy új értesítési sáv lett hozzáadva a projektűrlaphoz, amikor az időzóna eltér a felhasználó és a projekt között.

- Sales

  - Javítva: A költségbecslés kategória keresése használható az ismétlődések szűrésére.
  - Javítva: A **PluginDomain.ExecuteInTryCatchBlock(..)** kódja a továbbiakban nem rejti el a kivételek eredetét.
  - Javítva: A továbbiakban nem kap hibaüzenetet a **Projektkeresőben** az **Ajánlati sor** űrlapon, ha több mint 1000 projekt van.
  - Javítva: A **Becslések** rács a munka becsléséhez és a költségbecsléséhez immár a helyes pénznemszimbólummal jelenik meg.
  - Javítva: Miután egy szervezet frissítette a PSA-t 14. frissítési kiadásról a 15. frissítési kiadásra, az **Ütemezés** lap már nem üresen jelenik meg a **Projekt** űrlapon.
