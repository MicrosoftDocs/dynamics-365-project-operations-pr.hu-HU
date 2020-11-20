---
title: Újdonságok vagy változások a Project Service Automation 23-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 23-os frissítési kiadásában.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131121"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation 23-es frissítési kiadás, V3

Örömmel jelentjük be a Project Service Automation alkalmazásának legújabb frissítését a Dynamics 365-höz. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Ez a kiadás a Dynamics 365 9.x verzióval kompatibilis. A frissítéshez erre a kiadásra látogasson el a Dynamics 365 online Felügyeleti központjába, és a frissítés telepítéséhez menjen a megoldások oldalra. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 23-es frissítési kiadásában. Ennek a verziónak a buildszáma V3.10.34.30, és általánosan elérhető egy önálló frissítésben 2020 augusztusában.

## <a name="update-release-23"></a>23-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:
- Az Edge-eset kezelése a **Projektcsoporttag törlése** opcióban, hogy értelmes kivételt adjon.
- A hozzárendelés importálásának eredményei üres eltávolítási képernyőn.

**Erőforráskezelés**

A következő problémák kerültek kijavításra:

- Az **Erőforrás-kihasználtsági rács erőforráskártya** nem megfelelő adatot jelenít meg, ha az időintervallum öt napnál nagyobb.
- Ha az ügyfelek lefoglalható erőforrást hoznak létre, a beépülő modul időnként nem adja hozzá automatikusan az erőforrást egy Microsoft Office 365 csoporthoz.
- Az **Egyeztetés** nézet a **Heti** vagy a **Havi** nézetben hibásan jeleníti meg a manuális körvonalakat.

**Projektmenedzsment**

A következő problémák kerültek kijavításra:

- A **RetrieveMultiple for usersettings** entitások túlságosan nagy száma leromlott teljesítményt okoz a projektek jóváhagyása és az egyéb műveletek esetében.
- A **Projekttervezés** rács erőforrás-keresése a projektcsapat csak öt tagjának megjelenítésére korlátozódik. 
- A **Projekttervezés** rács erőforrás-keresés funkciója nem szűri az inaktív erőforrásokat.
- A manuális mód nem a várt módon működik a projekttervezési munkalebontási struktúrában.
- A **Projekttervezés** rács **Inaktív tranzakciós kategóriák** mezőt is megjelenít.
- Az **Erőforrás-hozzárendelés** rács hibásan kerekíti az értékeket, ha egy feladathoz több hozzárendelés tartozik.
- A kerekítési értékek eltérést mutatnak a tervezett költség és a tényleges költség között egy adott feladat esetében.

**Sales**

A következő problémák kerültek kijavításra:

- Az **Összes tranzakciós kategória beolvasása** opcióra való dupla kattintás több sort hoz létre.
