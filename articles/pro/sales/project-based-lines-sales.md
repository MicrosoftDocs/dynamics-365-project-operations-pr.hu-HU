---
title: Projekt lehetőségsorai
description: Ez a cikk a projektalapú lehetőségsorokat ismerteti. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e4f67bd9b7d51559e2942e9005b8f5f9187b1f78
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824958"
---
# <a name="project-opportunity-lines"></a>Projekt lehetőségsorai 

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projekt lehetőségsorai csak a projektalapú lehetőségekben érhetők el. A projektalapú lehetőségrekordok **Típus** mezője **Munkaalapú** értékre van beállítva.

A projektlehetőségsorok azok a sortételek, amelyeket egy projekt segítségével kézbesítenek a vevőnek. A projektek azonban nem köthetők projektalapú lehetőségsorokhoz. A projektek az **Árajánlat** fázisban és azután lévő sorelemekhez köthetők, mert jellemzően a lehetőség egy üzlet életciklusának korai fázisában merül fel. Annak meghatározása, hogy hány projekt kerül felhasználásra a munka ügyfélnek történő szállításához, egy olyan döntés, amit az értékesítés későbbi fázisában kell meghozni. A lehetőség fázis segítségével azonosíthatja az ügyfél egyedi szállítási összetevőit. Az ilyen összetevők szállításához használt projektek tényleges számát körülvevő döntések csak akkor hozhatók meg, ha a munkáról már több információ áll rendelkezésre.

Az alábbiakban a projektlehetőség sorának mezői láthatók:

| **Mező** | **Location** | **Ismertetés** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- | --- |
| Terméktípus | Általános lap (rejtett) | Választhat egyet az alábbi lehetőségek közül:</br>- Projektalapú szolgáltatás (csak akkor érhető el, ha a Dynamics 365 Project Operations telepítve van)</br>- Termék (csak akkor érhető el, ha a Project Operations és a Dynamics 365 Sales telepítve van) | Ennek a mezőnek az értékét **Projektalapú szolgáltatás** értékre állítja a program, amikor a lehetőséghez tartozó projektalapú sorok rácsából hozza létre a projektalapú lehetőségsort. <br> Ha módosítja vagy felülbírálja ezt az értéket, a projekt funkció nem lesz engedélyezve a projektalapú sorelemeiben. |
| Lehetőség | Általános lap | Ez a mező csak olvasható, és hivatkozik arra a fölérendelt lehetőségrekordra, amelyhez ez a sorelem tartozik. | Ennek a mezőnek nincs későbbi hatása. |
| Adatfolyam neve | Általános lap | Ez egy szerkeszthető szöveges mező, amellyel rövid azonosítás adható meg ehhez a sorelemhez. | Ezt az értéket a rendszer átviszi az árajánlat sorába, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Ügyfél költségvetése | Általános lap | Ez a szerkeszthető pénznem mező segít nyomon követni az összeget, amelyet az ügyfél hajlandó költeni erre a sorelemre. | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. |
| Számlázási mód | Általános lap | Ez a szerkeszthető mező az alábbi értékekkel rendelkezik:</br>- Idő és anyag</br>- Rögzített ár | Ezt az értéket a rendszer átviszi az árajánlat sorának megfelelő mezőjébe, amikor árajánlatot hoz létre ebből a lehetőségből. Az árajánlati sor létrehozása után a mező zárolva van, és nem módosítható. A mező értékét a lehető legpontosabban rendelje hozzá. Ha meg kell változtatnia ennek a mezőnek az értékét az árajánlatsorban, törölje, majd hozza létre újra az árajánlatsort. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
