---
title: Újdonságok vagy változások a Project Service Automation 33-es frissítési kiadásának V3 változatában
description: Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek elérhetők a Project Service Automation V3. 33-os frissítési kiadásában.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601481"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Újdonságok vagy változások a Project Service Automation 33-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3. 33-es frissítési kiadásában. Ennek a verziónak a buldszáma V3.10.54.98, és általánosan elérhető 2021. júliusában önálló frissítésen keresztül.

## <a name="update-release-33"></a>33-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

**Idő és költség**

A következő problémák kerültek kijavításra:

- Két zárolt mező, az **msdyn_description** és az **msdyn_externaldescription** szerkeszthető az elküldés után.
- Hibaüzenet jelenik meg, ha olyan költség jön létre, amely nem kapcsolódik projekthez.
- Időbejegyzés létrehozásakor az erőforrás szerepköre alapértelmezetten egy inaktív szerepkörre vált.
- A rendszer nem távolítja el a visszahívott és nem törölt kiadásokhoz társított naplósorokat.
- Az **Időbeviteli gyorslétrehozási űrlapon** módosítsa a **Projektfeladat-lista** nézetét, hogy az alapértelmezetten megjelenített dátumot a feladat kezdő dátumára váltsa.
- Ha a foglalható erőforrás **Kapcsolódó** lapján hoz létre időbejegyzést, a fölérendelt foglalható erőforrás helyett helytelenül a bejelentkezett felhasználóhoz jön létre az időbejegyzés.
- Az új mezőket a rendszer hozzáadja a **Tömeges jóváhagyású MDD** párbeszédpanelhez.

**Projekt tervezése**

A következő problémák kerültek kijavításra:
- Lassítja a projektek létrehozását, ha összetett naptárakat alkalmaz a projekt munkaóra-sablonokhoz.
- Ha a kezdő dátum nagyobb a záró dátumnál, a mezők időösszetevői közötti különbség miatt hiba jelenik meg a projektsablon másolásakor.

**Erőforrás-kezelés**

A következő problémák kerültek kijavításra:
- Az erőforrás-felhasználás lekérdezésben helytelen paraméter van használva, és az XML helytelen szűrési eredményekhez vezet az **Erőforrás-felhasználás** rácsban.
- A **Foglalások meghosszabbítása** jóváhagyás helytelen záró dátumot jelenít meg a foglalásokhoz.

**Értékesítés**

A következő problémák kerültek kijavításra:
- Hibaüzenet jelenik meh, ha egy kategóriaárat hiányzó értékekkel hoznak létre.
- Hibaüzenet jelenik meg, ha a szerződéssor mérföldkövét megrendeléssor nélkül hozzák létre.
