---
title: Újdonságok vagy változások a Project Service Automation 29-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 29-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 56cf47d207c7ee518d5d4b53866c3d6ddf1d1fb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587221"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Újdonságok vagy változások a Project Service Automation 29-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 29-es frissítési kiadásában. Ennek a verziónak a build száma V3.10.47.7, és általánosan elérhető egy önálló frissítésben 2021 februárjában.

## <a name="update-release-29"></a>29-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- A felhasználók nem látják a naplózott munkaórákat, amelyek nem munkanapokon vannak rögzítve az időbeviteli táblázatban.
- A jóváhagyott költségbejegyzések a rácson szerkeszthetők.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Hiányzik az ellenőrzési logika, amely biztosítja, hogy az erőforrás-hozzárendelési munkaórák nem lehetnek negatívak.
- Az **AssignResourcesForTask** egyéni művelet a csak a módosított mezők helyett az összes mezőt frissíti.
- Ha olyan környezetben másol projektet, amely **CreateProject** eseményen regisztrált beépülő modulokkal vagy munkafolyamatokkal rendelkezik, a **msdyn_bulkgenerationstatus** attribútum nem frissül, ha a **CopyWBSToProject** nem sikerül.
- A projektnaptár kibontásakor a munkanapok nem növekvő sorrendben vannak rendezve, így egyes projektfeladatok frissítése sikertelen lesz.
- Ha egy meglévő projekten módosítja a Projektkezelőt, akkor a szervezeti egység alapértelmezett logikája megváltozik.

**Értékesítés**

A következő problémák kerültek kijavításra:

- Ha nincsenek szerződéssorok, akkor a **Szerződés** oldal **Szerződés teljesítése** lapja az inicializáció során a háttérben meghiúsul.
