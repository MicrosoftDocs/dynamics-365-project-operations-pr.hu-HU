---
title: A Project Service Automation szolgáltatásának projektműveletekre való módosítása
description: Ez a cikk áttekintést nyújt a funkcióváltozásokról Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621342"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>A Project Service Automation szolgáltatásának projektműveletekre való módosítása

Miután egy projektet sikeresen frissítettek 3.X-ről Microsoft Dynamics 365 Project Service Automation Lite-ra Dynamics 365 Project Operations, a projekttevékenységek nem szerkeszthetők a tevékenységrács munkalebontási struktúrájában (WBS). Az ügyfelek áttekinthetik a WBS-eket abban a nyomon követési rácsban, ahol új mezőket adtak hozzá, hogy megadják a feladathoz kapcsolódó összes részletet. Azoknál a projekteknél, amelyeknél a munkalebontási struktúrán végzett szerkesztésre van szükség, a jogosult projekteket szelektíven konvertálhatja az új Project for the webütemezési élménybe.

## <a name="project-conversion-process"></a>Projektátalakítási folyamat

Projekt konvertálásához kövesse az alábbi lépéseket.

1. Nyissa meg a projekt főoldalát, és válassza a Konvertálás **lehetőséget** a műveleti ablaktáblán.
1. A megerősítő üzenet mezőben kattintson **az OK gombra** a projektkonverzió elindításához. A következő műveletek történnek:

    1. A projekt főoldalán megjelenő üzenetsávon ez áll: "A projekt ütemezése átalakításra kerül. A projekten addig nem módosíthatja, amíg az átalakítás be nem fejeződik."
    1. A rendszer átirányítja a projektlistára.

    A projektkonverzió befejezése után a következő műveletek történnek:

    1. A kijelölt projektmenedzser értesítést kap az alkalmazás jobb oldalán.
    1. A rendszer eltávolítja az üzenetsávot, amely jelzi, hogy az átalakítás folyamatban van.
    1. Az **Ütemezés** lapon látható a Webes Projekt új ütemezési élménye. Bármely felhasználó, aki rendelkezik a megfelelő licencekkel és biztonsági szerepkörökkel, szerkesztheti a munkalebontási struktúrát.
    1. Az **Ütemezési motor** mező frissítve lesz a Webes **Projektre**.
    1. A **Konvertálás** gomb el lesz távolítva a Műveleti ablaktáblából.

> [!IMPORTANT]
> A projektek tömeges átalakítása nem engedélyezett. Minden olyan kísérlet, amely egyszerre nagy mennyiségű projekt frissítésére irányul, a rendszer korlátozza. Ez a korlátozás segít biztosítani a nagy teljesítményt minden ügyfél számára.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuális feladatok és automatikus feladatok

Amikor egy környezetet a Project Service Automationről a Project Operations szolgáltatásra frissítenek, a munkalebontási struktúrában lévő összes feladat automatikusan ütemezettnek minősül. A manuálisan ütemezett tevékenységek fogalma nem érhető el a webes Projectben. Az ütemezési mód beállításával azonban meghatározhatja a projektek előnyben részesített ütemezési viselkedését az [ütemezési mód](/project-management/scheduling-modes.md) beállításával új projektek létrehozásakor.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Korlátozott műveletek az átalakítás előtti projektekhez

Ez a szakasz azokat a funkcionális különbségeket vázolja fel, amelyekre számíthat, ha a projekteket nem konvertálták.

### <a name="copy-project"></a>Projekt másolása

A **Másolás** művelet csak konvertált projekteken támogatott. A frissített projektek nem másolhatók az átalakítás előtt.

### <a name="move-project"></a>Projekt áthelyezése

A projekt kezdési dátumának módosítása csak akkor mozgatja arányosan a tevékenységek kezdetét, ha a projektet átalakították.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Mi a különbség az átalakított projektek és a frissítés befejezése után létrehozott új projektek között?

A környezet frissítése után átalakított projektek esetében egy jelző lesz beállítva, amely arra utasítja az ütemezést, hogy csak a projektnaptárat tartsa be. Ez a viselkedés megegyezik a Project Service Automation viselkedésével. A jelző azonban nem lesz beállítva a frissítés után létrehozott új projektekhez. Ezért az ütemezés tiszteletben tartja az erőforrások munkaidejét, amikor azok egy tevékenységhez vannak rendelve.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Mit tegyek, ha a projektem nem konvertálódik?

Ha a projekt konvertálása sikertelen, az első lépés a hibanaplók áttekintése a munkalebontási struktúrához kapcsolódó gyakori problémák azonosítása érdekében. Ha a naplók nem jeleznek olyan konkrét hibát, amellyel kapcsolatban lépéseket tehet, vegye fel a kapcsolatot az ügyfélszolgálattal, hogy az esetet tovább lehessen vizsgálni.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hogyan kezelik a vállalkozások bezárását a Webes Projektben?

A Webes projekt nem tartja tiszteletben a vállalat által a szervezet szintjén meghatározott üzleti bezárásokat. Ez azonban tiszteletben tartja az adott munkaidő-sablonban meghatározott egyéb típusú szabadnapokat.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Milyen korlátozások vonatkoznak a Project for the webre?

Lásd: [Munkalebontási struktúra létrehozása: Projektkorlátozások](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Számíthatok a költség- és értékesítési becsléseim változásaira?

Ritka esetekben, amikor az erőforrás-hozzárendelési kontúrok újraszámításra kerülnek, vagy ha a forrásprojekttől eltérő dátumhatárra esnek, különbségeket tapasztalhat az értékesítésben és a költségbecslésekben. A frissítési folyamat részeként az ügyfelektől elvárjuk, hogy teszteljenek egy reprezentatív mintaprojekt-készletet, hogy megértsék az esetleges ütemezési változásokat.
