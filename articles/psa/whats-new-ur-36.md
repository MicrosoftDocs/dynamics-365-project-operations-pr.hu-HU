---
title: Újdonságok vagy változások a Project Service Automation 36-es frissítési kiadásának V3 változatában
description: Ez a témakör a Microsoft Dynamics 365 Project Service Automation Update Release 36, V3 verzióban elérhető funkciókat és javításokat sorolja fel.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606770"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Újdonságok vagy változások a Project Service Automation 36-es frissítési kiadásának V3 változatában

[!include [banner](../includes/psa-now-project-operations.md)]

Örömünkre szolgál, ha bejelentjük a Microsoft Dynamics 365 Project Service Automation alkalmazás legújabb frissítését. Ez a kiadás a minőséggel, a teljesítménnyel és a használhatósággal kapcsolatos fontos javításokat tartalmaz. Kompatibilis a Dynamics 365 9.x rendszerrel. A kiadásra frissítéshez keresse fel a Dynamics 365 online megoldások felügyeleti központját, és telepítse a frissítést. További információ: [Megoldás telepítése, frissítése vagy eltávolítása](/power-platform/admin/install-remove-preferred-solution).

Ez a témakör felsorolja azokat a funkciókat és javításokat, amelyek újak vagy megváltoztak a Project Service Automation V3 36-os frissítési kiadásában. Ennek a verziónak a build száma V3.10.57.152, és általánosan elérhető egy önálló frissítésben 2021 októberében.

## <a name="update-release-36"></a>36-ös frissítési kiadás

### <a name="bug-fixes"></a>Hibajavítások

A következő problémák kerültek kijavításra.

**Általános**
- Nem megfelelően van lefordítva az **Alapértelmezett munkaidősablon** mezőnév a **Projektparaméterek** oldalon.
- Az aszinkron beépülő modulok nem kezelik megfelelően a **SharedVariableService** szolgáltatáshoz kapcsolódó kivételeket.

**Idő és költség**
- Ha hiányoznak a naplósorok, vagy ha a felhasználónak nincs meg a naplósorok olvasásához szükséges jogosultsága, helytelen hiba történik a projekt-jóváhagyások visszavonásakor.
- A felhasználók nem vonhatnak vissza egy jóváhagyást amennyiben a költség vagy időbejegyzés több projekt-jóváhagyással rendelkezik.
- A **Távollét** és a **Szabadság** helytelenül van fordítva a kínai nyelvre az **Időbejegyzés** gyors létrehozási oldalán egy keresésben.

**Erőforrás-kezelés**
- A felhasználó nem tud erőforrásokat keresni az **Ütemezési segédben**, ha a nézetmód **Nap**, **Hét** vagy **Hónap**.
- Az általános erőforrások számára helytelenül van engedélyezve, hogy üres pozíciónevekkel rendelkezzenek. 
- A szerződés elvesztettként való lezárása nem törli a jövőbeli foglalásokat.

**Értékesítés**
- Ha egy környezetben nagy mennyiségű termék van, akkor a teljesítmény csökken az **Anyagbecslés** rácsban.
- Projekt sablonból való létrehozásakor a projekt pénzneme alapértelmezés szerint a nem az adott Projektmenedzser szerződési egységéhez illeszkedik.
- A tényleges összegek nem mindig egyeznek meg a projekt esedékességén tükröződő értékekkel, vagy az összegek negatívvá válnak bizonyos visszahívási helyzetekben.
- Hiba történik, ha projektsablonból létrehozott projektet szerződéssorhoz társít.
- A felhasználók törölhetik a **Számlázásra kész** és **Számla létrehozva** mérföldkövekkel rendelkező szerződéssorokat. Ezt nem szabad megengedni.
- Ha egy projektből becsléseket importálnak, akkor nem megfelelően van beállítva az ajánlatsor részleteinek számlázhatósága, ha a feladatalapú számlázás engedélyezve van az ajánlatsorhoz.
- Rögzített árú számlázás mérföldkő hozzáadásakor a mérföldkövek nem jelennek meg a mérföldkövek részrácsában, amíg nem frissítik az oldalt.
- Nullhivatkozás kivétel jön létre olyan projektszerződés létrehozásakor, amely null értékű ajánlatnevet tartalmaz.
- Helytelen árbecsléseket eredményeznek az olyan manuális módú feladatok, amelyekben a projekt pénzneme eltér az erőforrás pénznemétől.
- A felhasználók nem tudnak olyan tranzakciót visszahívni, amelyet sikeresen javítottak helyesbítő számlával.
- Az inaktivált tranzakciókategóriák jelennek meg a **Költségbecslések** rácsban.



