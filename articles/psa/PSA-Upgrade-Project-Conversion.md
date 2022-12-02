---
title: Project Service Automation és Project Operations közötti projektütemezés átalakítási folyamata
description: A cikk áttekintést a Microsoft Dynamics 365 Project Service Automation és a Dynamics 365 Project Operations közötti változásokról ad tájékoztatást.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642571"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation és Project Operations közötti projektütemezés átalakítási folyamata

Egy projekt a Microsoft Dynamics 365 Project Service Automation 3.X verzióról Dynamics 365 Project Operations Lite verzióra való sikeres frissítését követően nem lehet szerkeszteni a projektfeladatokat a feladatrács munkalebontási struktúrában (WBS). Az ügyfelek a követési rácsban áttekinthetik a WBS-eket, ahol új mezőket lettek hozzáadva a feladathoz kapcsolódó összes részlet megadásához. Az olyan projektek esetén, ahol szerkesztésekre van szükség a WBS-ben, a jogosult projekteket szelektíven át lehet alakítani az új Project for the Web ütemezési élményre.

## <a name="project-conversion-process"></a>Projektátalakítási folyamat

Egy projekt átalakításához kövesse ezeket a lépéseket.

1. Nyissa meg a projekt főoldalát, és válassza az **Átalakítás** lehetőséget a műveleti panelen.
1. A megjelenő megerősítő üzenetben válassza a **OK** lehetőséget a projektátalakítás megerősítéséhez. A következő műveletek történnek:

    1. A projekt főoldalán megjelenő üzenetsávban a következő látható: „A projekt ütemezésének átalakítása folyamatban van. A projekten nem lehet módosításokat végrehajtani, amíg az átalakítás nem fejeződik be.”
    1. A rendszer átirányítja a projektlistára.

    A projektátalakítás befejezése után a következő műveleteket történnek:

    1. A hozzárendelt projektmenedzser értesítést kap az alkalmazás jobb oldalán.
    1. Az üzentsáv, amely jelzi, hogy az átalakítás folyamatban van, eltávolításra kerül.
    1. Az **Ütemezés** lap megjeleníti az új ütemezési élményt a Project for the Web alkalmazással. A WBS-et bármely felhasználó módosíthatja, aki rendelkezik a megfelelő licencekkel és biztonsági szerepkörökkel.
    1. Az **Ütemezési motor** mezőjét a program a **Project for the Web** értékre frissíti.
    1. A műveletpanelről a Rendszer eltávolítja az **Átalakítás** gombot.

> [!IMPORTANT]
> A projektek tömeges átalakítása nem engedélyezett. A nagy mennyiségű projekt egyszerre való frissítésére tett kísérleteket a rendszer leszabályozza. Ez a korlátozás biztosítja a nagy teljesítményt minden ügyfél számára.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuális feladatok és automatikus feladatok

Ha egy környezetet a Project Service Automation alkalmazásról a Project Operations alkalmazásra frissítenek, a WBS minden feladata automatikusan ütemezettnek lesz tekintve. A manuálisan ütemezett feladatok fogalma nem érhető el a Project for the Web alkalmazásban. Azonban az új projektek létrehozásakor az [ütemezési mód](/project-management/scheduling-modes.md) beállításának használatával meghatározhatja a projektek előnyben részesített ütemezési viselkedését.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Korlátozott műveletek átalakítás előtti projektekhez

Ez a szakasz a projektek átalakításának elmaradásakor várható funkcionális különbségeket ismerteti.

### <a name="copy-project"></a>Projekt másolása

A **Másolás** művelet csak az átalakított projektek esetén támogatott. A frissített projektek nem másolhatók az átalakítás előtt.

### <a name="move-project"></a>Projekt áthelyezése

A projekt kezdő dátumának módosítása nem fogja arányosan eltolni a feladatok kezdetét, hacsak a projekt nem lett átalakítva.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mi a különbség az átalakított projektek és az új, a frissítés után létrehozott projektek között?

A környezet frissítése után átalakított projektek esetén egy jelző lesz beállítva, amely arra utasítja az ütemezést, hogy csak a projekt naptárát vegye figyelembe. Ez a viselkedés egyezik a Project Service Automation viselkedésével. A frissítés után létrehozott új projektekhez azonban nem lesz beállítva ez a jelző. Éppen ezért az ütemezés az erőforrások munkaóráit be fogja tartani, amikor egy feladathoz vannak rendelve.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mit kell tennem, ha a projektem nem alakítása nem sikerül?

Ha a projekt átalakítás nem sikerül, az első lépés a hibanaplók áttekintése, és azonosítja a WBS-hez kapcsolódó, általános problémákat. Ha a naplók nem utalnak konkrét hibára, amely alapján valamilyen lépést tehetne, forduljon az ügyfélszolgálathoz az eset további kivizsgálásáért.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hogyan kezeli a szünnapokat Project for the Web?

A Project for the Web nem tartja be a vállalatnál szervezeti szinten definiált szünnapokat. Figyelembe veszi azonban tartani az egyéb, munkaidősablonokban definiált szabadnapokat.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Mik a Project for the Web korlátozásai?

Lásd [Munkalebontási struktúra: Projekt korlátozásai](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Várhatók a költség- és értékesítési becslésekben változások?

Azon ritka esetekben, amikor az erőforrás-hozzárendelési kontúrok újraszámításra kerülnek, illetve a forrás projekttől eltérő dátumtartományba esnek, különbségeket tapasztalhat az értékesítési és költségbecslésekben. A frissítési folyamat részeként az ügyfelek elvárják, hogy teszteljék a projektek egy mintakészletét, hogy megértsék az esetleges ütemezést érintő módosításokat.
