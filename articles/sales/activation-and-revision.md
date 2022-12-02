---
title: Projektárajánlat aktiválása és felülvizsgálata
description: Ez a cikk az ajánlatok aktiválásával és felülvizsgálatával kapcsolatosan ad információkat a Microsoft Dynamics 365 Project Operations alkalmazásban.
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
# <a name="activate-and-revise-a-project-quote"></a>Projektárajánlat aktiválása és felülvizsgálata

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az aktiválási és felülvizsgálati képességek segítségével nyomon követhető a projektalapú árajánlatok verziószáma a becslési és tárgyalási fázisokban. Amikor aktiválnak egy vázlat ajánlatot, az csak olvashatóvá válik.

Az aktiválási és felülvizsgálási lehetőségek a következő feladatok elvégzését teszik lehetővé:

- Az árajánlatokat elnyerése vagy elvesztése az aktiválás után.
- Az ajánlat átdolgozása a meglévő ajánlat módosításához vagy új verzió létrehozásához.

> [!NOTE]
> Azajánlatok felülvizsgálata funkció engedélyezése után az nem tiltható le.

A projektalapú ajánlatok aktiválása és átdolgozása képességének bekapcsolához hajtsa végre a következő lépéseket.

1. Válassza a **Beállítások** \> **Paraméterek** lehetőséget.
1. Nyissa meg a **Paraméterek** rekordot.
1. A Műveletpanel **Funkciókezelése** lapján jelölje be az **Árajánlatok aktiválásának és felülvizsgálatainak engedélyezése** lehetőséget.
1. A jóváhagyást kérő párbeszédpanelen válassza az **OK** lehetőséget.
1. Néhány pillanat után frissítse a böngészőjét. Aktiválási és felülvizsgálási lehetőségek most elérhetőek kell legyenek. Tudni fogja, hogy ezek a lehetőségek engedélyezve vannak, ha az **Árajánlatok aktiválásának és felülvizsgálatainak engedélyezése** gomb a már nem jelenik meg a műveletablakban.

## <a name="activating-a-quote"></a>Árajánlat aktiválása

Az Árajánlatok aktiválásának és felülvizsgálatainak engedélyezése funkció engedélyezése után az **Árajánlat lezárása megnyertként** és az **Árajánlat lezárása elvesztettként** gombok nem érhető el a műveletpanelen a projektajánlat-vázlatok esetén. Ezek csak az ajánlat aktiválása után érhetők el.

Az aktiválás az árajánlat folyamatának azt a fázisát jelenti, amikor meg szeretné akadályozni az ajánlat további módosításait. Ebben a fázisban a rendszer belső ellenőrzésre vagy az ügyfélnek küldi el az ajánlatot.

Az **Árajánlat lezárása megnyertként** és **Árajánlat lezárása elvesztettként** gombok rendelkezésre állnak a műveleti panelen. A belső vagy az ügyfél áttekintése eredményétől függőan a gombok egyikének használatával lezárhatja az aktivált ajánlatot. Az aktivált ajánlatokon a tárgyalásokat és módosításokat az **Árajánlat felülvizsgálata** gombbal érvényesítheti.

## <a name="revising-a-quote"></a>Árajánlat felülvizsgálata

Ha módosítania kell egy aktivált ajánlatot, válassza az **Ajánlat felülvizsgálata** lehetőséget. A rendszer lezárja az ajánlatot, és a **felülvizsgált** okkódot használja. Ekkor létrejön egy új ajánlat, amely ugyanazzal az azonosítóval és növekményesített verziószámmal rendelkezik. A rendszer az eredeti árajánlat minden részletét átmásolja az új árajánlatba. Az új árajánlat vázlat állapotú, és igény szerint szerkeszthető.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
