---
title: Erőforrás-kihasználtság áttekintése
description: Ez a témakör információkat nyújt az erőforrás-kihasználtságról a Project Operations alkalmazásban.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000799"
---
# <a name="resource-utilization-overview"></a>Erőforrás-kihasználtság áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az erőforrások megcélozhatók számlázható felhasználással. Ezt a célfelhasználást a rendszer egy erőforrás alapértelmezett szerepének attribútumaként határozza meg, vagy beállítja az egyes foglalható erőforrások rekordjában. A hasznosítási számítások azon tényleges órákon alapulnak, amelyeket az erőforrások jóváhagyott időbejegyzésekkel jelentettek.

A felhasználás kiszámításához a következő képleteket kell használni:

  - Számlázható felhasználás = Számlázható tényleges óra ÷ Erőforrás-kapacitás
  - Nem számlázható felhasználás = Tényleges idő számlaszám-azonosítóval = Nem terhelhető, kiegészítő vagy nem elérhető ÷ Erőforrás-kapacitás
  - Belső = Valós idő eladási szerződés nélkül ÷ Erőforrás-kapacitás
  - Erőforrás-kapacitás = Erőforrás-munkaidő - Irodán kívüli - Nem munkanapok

Az **Erőforrás-hasznosítás** nézetet az **Erőforrások** ablaktáblában találhatja meg.

A rács minden cellája képviseli az erőforrás számlázható felhasználási százalékát egy időszakban, például egy nap, hét vagy hónap. A cellák színezésére a következő képleteket használják:

  - **Zöld**: Számlázható kihasználtság >= Erőforrás cél kihasználtsága
  - **Sárga**: Cél kihasználtság – 20 <= Számlázható kihasználtság < Célkihasználtság
  - **Piros**: Számlázható kihasználtság < Célkihasználtság – 20

Mivel az **Erőforrás-hasznosítás** nézet az Ütemezési táblán alapul, az Ütemezési tábla szűrési képességeit használhatja az eredmények szűrésére.

A rács megköveteli, hogy állítson be egy célfelhasználást a szerepre vagy az egyes erőforrásokra. A beállítás elvégzéséhez ugorjon az **Erőforrások** > **Erőforrásszerepek** elemre.

Ezenkívül minden foglalható erőforráshoz alapértelmezett szerepet kell hozzárendelni. Lépjen az **Erőforrások** > **Erőforrások** oldalra. A **Project Service** lapon ellenőrizze, hogy az erőforrás szerepe van meghatározva, és hogy a **Alapértelmezett** mező **Igen** értékre van állítva. További szerepeket adhat hozzá, ahol **Alapértelmezett** = **Nem**. A szerep, ahol az **Alapértelmezett** = **Igen**, az erőforrás felhasználásának értékelésére szolgál annak a célnak a függvényében.

A **Project Service** lapon az erőforrás egyedi célhasználatát is beállíthatja. A hasznosítási számítás ezt követően a célfelhasználást használja az erőforrás céljának értékelésére, az erőforrás alapértelmezett szerepének célpontja helyett.

Az erőforrás felhasználása csak akkor jelenik meg, ha az erőforrás jóváhagyott, díjköteles időt mutat a rácson megjelenített időszakban.


[!INCLUDE[footer-include](../includes/footer-banner.md)]