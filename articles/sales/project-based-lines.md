---
title: Projektalapú lehetőségsorok
description: Ez a témakör a projektalapú lehetőségsorok használatát ismerteti.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cceb175210f7b597d682e9e4e910c79280211293
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600929"
---
# <a name="project-based-opportunity-lines"></a>Projektalapú lehetőségsorok

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


A projektalapú lehetőségsorok csak a projektalapú lehetőségekben érhetők el. A projektalapú lehetőségrekordok **Típus** mezője **Munkaalapú** értékre van beállítva.

A projektalapú lehetőségsorok azok a sorelemek, amelyek az ügyfélnek a projekt segítségével szállításra kerülnek. A projektek azonban nem köthetők projektalapú lehetőségsorokhoz. A projektek az **Árajánlat** fázisban és azután lévő sorelemekhez köthetők, mert jellemzően a lehetőség egy üzlet korai fázisában merül fel. Annak meghatározása, hogy hány projekt kerül felhasználásra a munka ügyfélnek történő szállításához, egy olyan döntés, amit az értékesítés későbbi fázisában kell meghozni. A lehetőség fázis segítségével azonosíthatja az ügyfél egyedi szállítási összetevőit. Az ilyen összetevők szállításához használt projektek tényleges számát körülvevő döntések csak akkor hozhatók meg, ha a munkáról már több információ áll rendelkezésre.

Az alábbiakban láthatók a projektalapú lehetőségsorok mezői:

| **Mező** | **Hely** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Terméktípus | Általános lap (rejtett) | Ez egy értékkészletmező. Ha telepítve van a Dynamics 365 Operations, az egyik rendelkezésre álló lehetőség a **Projektalapú szolgáltatás**.  | Ennek a mezőnek az értékét **Projektalapú szolgáltatás** értékre állítja a program, amikor a lehetőséghez tartozó projektalapú sorok rácsából hozza létre a projektalapú lehetőségsort. <br> Ha módosítja vagy felülbírálja ezt az értéket, a projekt funkció nem lesz engedélyezve a projektalapú sorelemeiben. |
| Lehetőség | Általános lap | Ez a mező csak olvasható, és hivatkozik arra a fölérendelt lehetőségrekordra, amelyhez ez a sorelem tartozik. | Ennek a mezőnek nincs későbbi hatása. |
| Adatfolyam neve | Általános lap | Ez egy szerkeszthető szöveges mező, amellyel rövid azonosítás adható meg ehhez a sorelemhez. | Ezt az értéket a rendszer átviszi az árajánlat sorába, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Ügyfél költségvetése | Általános lap | Ez a szerkeszthető pénznem mező segít nyomon követni az összeget, amelyet az ügyfél hajlandó költeni erre a sorelemre. | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Számlázási mód | Általános lap | Ez a szerkeszthető mező az alábbi értékekkel rendelkezik:</br>- Idő és anyag</br>- Rögzített ár | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. Az árajánlati sor létrehozása után a mező zárolva van, és nem módosítható. A mező értékét a lehető legpontosabban rendelje hozzá. Ha meg kell változtatnia ennek a mezőnek az értékét az árajánlatsorban, törölje, majd hozza létre újra az árajánlatsort. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]