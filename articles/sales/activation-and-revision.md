---
title: Projektajánlat aktiválása és módosítása
description: Ez a cikk az idézetek aktiválásáról és felülvizsgálatáról nyújt tájékoztatást a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410383"
---
# <a name="activate-and-revise-a-project-quote"></a>Projektajánlat aktiválása és módosítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az aktiválási és módosítási képességek segítségével nyomon követheti a projektalapú árajánlatok verziószámozását a becslési és egyeztetési fázisban. Ha egy idézet vázlata aktiválódik, az írásvédetté válik.

Az aktiválási és módosítási képességek lehetővé teszik a következő feladatok elvégzését:

- Csak az aktiválás után nyerjen vagy veszítsen el árajánlatokat.
- Tekintse át az árajánlatot, hogy módosítsa a meglévő árajánlatot, vagy hozzon létre egy új verziót.

> [!NOTE]
> Miután engedélyezte az idézőjelek aktiválására és felülvizsgálatára szolgáló funkciót, az nem tiltható le.

A projektalapú árajánlatok aktiválásának és felülvizsgálatának bekapcsolásához kövesse az alábbi lépéseket.

1. Lépjen a **Beállítások** \> **paramétereihez**.
1. Nyissa meg a **Parameters** rekordot.
1. A Műveleti ablaktábla Funkcióvezérlő **lapján válassza az** Idézetek **aktiválásának és felülvizsgálatának engedélyezése lehetőséget**.
1. A jóváhagyást kérő párbeszédpanelen válassza az **OK** lehetőséget.
1. Néhány pillanat múlva frissítse a böngészőt. Az aktiválási és felülvizsgálati képességeknek mostantól elérhetőnek kell lenniük. Tudni fogja, hogy ezek a képességek engedélyezve vannak, ha az **Idézetek** aktiválásának és változatának engedélyezése gomb már nem jelenik meg a műveleti ablaktáblán.

## <a name="activating-a-quote"></a>Árajánlat aktiválása

Miután engedélyezte az idézetek aktiválására és felülvizsgálatára szolgáló funkciót, az **Idézet bezárása megnyertként** és **Az idézet bezárása elveszettként** gombok a műveleti ablaktáblán nem érhetők el a projektajánlat-tervezetekhez. Csak az árajánlat aktiválása után érhetők el.

Az aktiválás az árajánlati folyamat azon szakaszát jelöli, amikor meg szeretné akadályozni az árajánlat további módosítását. Ebben a szakaszban az árajánlatot belső felülvizsgálatra vagy az ügyfélnek küldik el.

Az Idézet bezárása megnyertként **és** az **Idézet bezárása elveszettként** gombok a műveleti ablaktáblán az aktivált árajánlatokhoz érhetők el. A belső vagy ügyfél-ellenőrzés eredményétől függően ezen gombok egyikével bezárhat egy aktivált árajánlatot. Az aktivált árajánlatok egyeztetését és módosítását az Idézet **felülvizsgálata lehetőség kiválasztásával** végezheti el.

## <a name="revising-a-quote"></a>Idézet felülvizsgálata

Ha módosítania kell egy aktivált árajánlatot, válassza az Idézet **módosítása lehetőséget**. Az idézet be van zárva, és a **felülvizsgált** okkódot használja. Ezután létrejön egy új idézet, amely ugyanazzal az azonosítóval és egy megnövelt verziószámmal rendelkezik. Az eredeti idézet minden részletét átmásolja az új idézetbe. Az új árajánlat piszkozat státuszban van, és szükség szerint szerkeszthető.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
