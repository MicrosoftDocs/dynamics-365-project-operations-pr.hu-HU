---
title: Project Service Automation a Project Operations projektütemezési átalakítási folyamatához
description: Ez a cikk áttekintést nyújt a funkcióváltozásról Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation a Project Operations projektütemezési átalakítási folyamatához

Miután egy projektet sikeresen frissített a 3.X-ről Microsoft Dynamics 365 Project Service Automation a Lite-ra Dynamics 365 Project Operations, a projekttevékenységek szerkesztése a tevékenységrács munkalebontási struktúrájában (WBS) nem lehetséges. Az ügyfelek áttekinthetik a WBS-eket a nyomkövetési rácsban, ahol új mezőket adtak hozzá, hogy megadják a feladathoz kapcsolódó összes részletet. Azoknál a projekteknél, ahol a munkalebontási struktúrát kell szerkeszteni, a támogatható projekteket szelektíven konvertálhatja az új projektbe a webes ütemezési élmény érdekében.

## <a name="project-conversion-process"></a>Projekt átalakítási folyamat

Projekt konvertálásához kövesse az alábbi lépéseket.

1. Nyissa meg a projekt főoldalát, és válassza a Konvertálás **lehetőséget** a műveleti ablaktáblán.
1. A megerősítő üzenetmezőben kattintson az OK gombra **a** projekt átalakításának megkezdéséhez. A következő műveletek történnek:

    1. A projekt főoldalán megjelenő üzenetsávon ez áll: "A projekt ütemezése átalakítás alatt áll. Nem módosíthatja a projektet, amíg az átalakítás be nem fejeződik."
    1. A rendszer átirányítja a projektlistára.

    A projekt átalakításának befejezése után a következő műveletek történnek:

    1. A kijelölt projektmenedzser értesítést kap az alkalmazás jobb oldalán.
    1. A rendszer eltávolítja azt az üzenetsávot, amely azt jelzi, hogy az átalakítás folyamatban van.
    1. Az **Ütemezés** lapon látható a webes Project új ütemezési élménye. A megfelelő licencekkel és biztonsági szerepkörökkel rendelkező felhasználók szerkeszthetik a munkalebontási struktúrát.
    1. Az **Ütemezési motor** mező a Webes **Projekt értékre** frissül.
    1. A **Konvertálás** gomb el lesz távolítva a műveleti ablaktábláról.

> [!IMPORTANT]
> A projektek tömeges átalakítása nem engedélyezett. Minden olyan kísérlet, amely nagy mennyiségű projekt egyidejű frissítésére irányul, a rendszer szabályozni fogja. Ez a korlátozás segít nagy teljesítményt biztosítani minden ügyfél számára.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuális feladatok vs. automatikus feladatok

Amikor egy környezetet Project Service Automationről Project Operations rendszerre frissítenek, a munkalebontási struktúrában lévő összes tevékenység automatikusan ütemezettnek minősül. A manuálisan ütemezett tevékenységek fogalma nem érhető el a Webes Projectben. Az új projektek létrehozásakor azonban meghatározhatja a projektek előnyben részesített ütemezési viselkedését az [ütemezési mód](/project-management/scheduling-modes.md) beállításával.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Az átalakítást megelőző projektek korlátozott műveletei

Ez a szakasz azokat a funkcionális különbségeket ismerteti, amelyekre akkor számíthat, ha a projekteket még nem konvertálták.

### <a name="copy-project"></a>Projekt másolása

A **Másolás** művelet csak konvertált projekteken támogatott. A frissített projektek nem másolhatók az átalakítás előtt.

### <a name="move-project"></a>Projekt áthelyezése

A projekt kezdési dátumának módosítása csak akkor helyezi át arányosan a tevékenységek kezdetét, ha a projektet átalakították.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mi a különbség a konvertált projektek és a frissítés befejezése után létrehozott új projektek között?

A környezet frissítése után konvertált projektek esetében egy jelző lesz beállítva, amely arra utasítja az ütemezést, hogy csak a projektnaptárat tartsa tiszteletben. Ez a viselkedés megegyezik a Project Service Automation viselkedésével. A jelző azonban nem lesz beállítva a frissítés után létrehozott új projektekhez. Ezért az ütemezés tiszteletben tartja az erőforrások munkaidejét, amikor egy tevékenységhez vannak rendelve.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mit tegyek, ha a projektem nem konvertálódik?

Ha a projekt konvertálása sikertelen, az első lépés a hibanaplók áttekintése a munkalebontási struktúrával kapcsolatos gyakori problémák azonosítása érdekében. Ha a naplók nem jeleznek olyan konkrét hibát, amellyel kapcsolatban intézkedhet, vegye fel a kapcsolatot az ügyfélszolgálattal, hogy az esetet tovább lehessen vizsgálni.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hogyan kezelik a vállalkozások bezárását a Webes Projectben?

A webes Project nem tartja tiszteletben a vállalat által szervezeti szinten meghatározott üzleti bezárásokat. Ez azonban tiszteletben tartja az adott munkaidő-sablonban meghatározott egyéb típusú szabadnapokat.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Milyen korlátozások vonatkoznak a webes Projectre?

Lásd [: Munkalebontási struktúra létrehozása: A projekt korlátozásai](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Számíthatok változásokra a költség- és értékesítési becsléseimben?

Ritka esetekben, amikor az erőforrás-hozzárendelési kontúrok újraszámítása megtörténik, vagy ha a forrásprojekttől eltérő dátumhatárra esnek, különbségeket tapasztalhat az értékesítésben és a költségbecslésekben. A frissítési folyamat részeként az ügyfeleknek tesztelniük kell a projektek reprezentatív mintakészletét, hogy megértsék az esetleges ütemezési változásokat.
