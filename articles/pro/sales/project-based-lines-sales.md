---
title: Projektalapú lehetőségsorok (Pro)
description: Ez a témakör a projektalapú lehetőségsorokat ismerteti. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896374"
---
# <a name="project-based-opportunity-lines-pro"></a>Projektalapú lehetőségsorok (Pro)

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektalapú lehetőségsorok csak a projektalapú lehetőségekben érhetők el. A projektalapú lehetőségrekordok **Típus** mezője **Munkaalapú** értékre van beállítva.

A projektalapú lehetőségsorok azok a sorelemek, amelyek az ügyfélnek a projekt segítségével szállításra kerülnek. A projektek azonban nem köthetők projektalapú lehetőségsorokhoz. A projektek az **Árajánlat** fázisban és azután lévő sorelemekhez köthetők, mert jellemzően a lehetőség egy üzlet életciklusának korai fázisában merül fel. Annak meghatározása, hogy hány projekt kerül felhasználásra a munka ügyfélnek történő szállításához, egy olyan döntés, amit az értékesítés későbbi fázisában kell meghozni. A lehetőség fázis segítségével azonosíthatja az ügyfél egyedi szállítási összetevőit. Az ilyen összetevők szállításához használt projektek tényleges számát körülvevő döntések csak akkor hozhatók meg, ha a munkáról már több információ áll rendelkezésre.

Az alábbiakban láthatók a projektalapú lehetőségsorok mezői:

| **Mező** | **Hely** | **Relevancia, cél és útmutatás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Terméktípus | Általános lap (rejtett) | Választhat egyet az alábbi lehetőségek közül:</br>- Projektalapú szolgáltatás (akkor érhető el, ha telepítve van a Dynamics 365 Operations)</br>- Termék (csak akkor érhető el, ha a Project Operations és a Dynamics 365 Sales telepítve van) | Ennek a mezőnek az értékét **Projektalapú szolgáltatás** értékre állítja a program, amikor a lehetőséghez tartozó projektalapú sorok rácsából hozza létre a projektalapú lehetőségsort. <br> Ha módosítja vagy felülbírálja ezt az értéket, a projekt funkció nem lesz engedélyezve a projektalapú sorelemeiben. |
| Lehetőség | Általános lap | Ez a mező csak olvasható, és hivatkozik arra a fölérendelt lehetőségrekordra, amelyhez ez a sorelem tartozik. | Ennek a mezőnek nincs későbbi hatása. |
| Adatfolyam neve | Általános lap | Ez egy szerkeszthető szöveges mező, amellyel rövid azonosítás adható meg ehhez a sorelemhez. | Ezt az értéket a rendszer átviszi az árajánlat sorába, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Ügyfél költségvetése | Általános lap | Ez a szerkeszthető pénznem mező segít nyomon követni az összeget, amelyet az ügyfél hajlandó költeni erre a sorelemre. | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Számlázási mód | Általános lap | Ez a szerkeszthető mező az alábbi értékekkel rendelkezik:</br>- Idő és anyag</br>- Rögzített ár | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. Az árajánlati sor létrehozása után a mező zárolva van, és nem módosítható. A mező értékét a lehető legpontosabban rendelje hozzá. Ha meg kell változtatnia ennek a mezőnek az értékét az árajánlatsorban, törölje, majd hozza létre újra az árajánlatsort. |
