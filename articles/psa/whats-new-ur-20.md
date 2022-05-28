---
title: Újdonságok vagy változások a Project Service Automation 20-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 20-os frissítési kiadásában
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 4b1a8b5b65f0dfeeff74db363c918206c64e81f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588831"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation 20-as frissítési kiadás, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 20-es frissítési kiadásában. A verzió build száma V 3.10.31.37, és általánosan elérhető lesz önálló frissítésként 2020 júniusában.

## <a name="update-release-20"></a>20-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- Ha a projektcsapat tagjait olyan felosztási módszerrel importálja, amelyhez órák szükségek, nem egyérlemű hibaüzenetet eredményezhet, ha a megadott órák értéke nulla.
- A felhasználók helytelen hibaüzenetet kapnak, amikor a karakterek maximális számát megadták egy projektfeladat **Leírás** mezőjébe.
- A **Microsoft Dynamics 365 Project Service Automation bővítmény letöltése** oldalt a rendszer átirányítja az angol letöltési oldalra, ha a felhasználó nyelvi beállításai japánra vannak állítva.
- Kiszolgálóhiba esetén a **Projektek űrlap** **Ütemezés** lapján a szinkronizálási címke időnként megmarad.
- Egy feladat módosításakor a rendszer elküldi a redundáns feladatok frissítéseit a kiszolgálónak.

**Sales**

A következő problémák kerültek kijavításra:

- A **Szerződés** űrlapon a dupla kattintás a **számla létrehozása** lehetőségre egyetlen tényleges rekordhoz két számlát hoz létre.
- Internet Explorer 11-ben a felhasználók nem tudnak Költségjelentés-bejegyzéseket létrehozni.
- A költségek sztornírozása és a nem számlázott értékesítések sztornírozása nem kapcsolódik össze.
- A **Tényadatok frissítése** gomb a **Projekt** űrlapon nem frissíti a **Feladat tényleges órái** mezőt.
- A **PreValidateProjectTeamMemberCreate** bővítmény ismétlődő általános foglalható erőforrásokat hozhat létre, ha a **msdyn_isgenericresourceprojectscoped** attribútum **Hamis** értékre van állítva.
- Az **Újraszámítás** törli a termékalapú árajánlati sor és szerződéssor adatainak számlázható költségeit.
- Bizonyos helyzetekben a **PostEstimateLineUpdate** beépülő modul Null hivatkozási kivételi hibát jelenít meg.
- Az időfázis időtartama a **Jövedelmezőségi elemzés diagramjában** nem egyezik meg az ajánlatban szereplő rögzített árú árajánlat sor részletek költségeinek időtartamával.
- Az egység és az egységcsoport értékei nem megfelelőek a költségkategóriákhoz a **szerződéssor részletei** és az **ajánlati sor részletei** űrlapon.
- **A szervezeti egység önköltségi ára** lista engedélyezi az átfedéseket az érvényességi dátumokban.
- A felhasználók nem módosíthatják a **OrgUnit** értékét, ha a megrendelés típusa nem munkaalapú, mert az egy NULL referenciakivételi hibát eredményez.
- Amikor az **ajánlati sor részletei** űrlapról próbál meg navigálni vissza az **árajánlat** lapra, az űrlap frissül, és megjeleníti az **Összesítés** lapot.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
