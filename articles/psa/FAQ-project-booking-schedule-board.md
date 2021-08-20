---
title: Projektfoglalás létrehozása az Ütemezés tábláról
description: Ez a témakör arról nyújt információt, hogy miként lehet létrehozni egy projektfoglalást az Ütemezés tábláról.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 513f7fe75cfb7b1658b4be71ed0a17da7b64a1023992e1dada9adca8f0dbf21e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987619"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Projektfoglalás létrehozása az Ütemezés tábláról

[!include [banner](../includes/psa-now-project-operations.md)]

Az erőforrásokat egy projektre közvetlenül a projekt **Csapat** lapjáról foglalhatja le, vagy generálhat egy erőforrásigényt egy általános csapattag-hozzárendelésből, majd teljesítheti a létrehozott követelményt egy projekten belüli csapattaggal.

Az erőforrásokat a projektekre közvetlenül az Ütemezés tábláról is lefoglalhatja. Ez három módon oldható meg:

- **Foglalás generált erőforrás-követelményből:** Erőforrás-követelményt generálhat általános erőforrás létrehozása és a projekten belüli feladatok kiosztása után.

- **Foglalás az elsődleges követelményből:** Az elsődleges követelmények megjelennek az Ütemezés tábla **Projekt** lapján. 

- **Foglalás új erőforrás-igénylésből:** Azonnal létrehozhat egy erőforrás-követelményt, és társíthatja azt egy projekthez. Az Ütemezés táblán az erőforrás-követelmény megjelenik az **Nyílt követelmények** fülön.

## <a name="book-from-a-generated-resource-requirement"></a>Foglalás egy létrehozott erőforrás-követelményből

Készíthet általános erőforrást, és egy vagy több feladatot rendelhet hozzá egy projekten belül. Ezután generálhat egy erőforrás-követelményt az általános csapattagtól. 

1.  Az Ütemezés táblán ez az erőforrás megjelenik az **Nyílt követelmények** lapon. Lehet, hogy oszlopszűrőket kell használnia a rácson, ha sok nyílt követelmény van. 

    ![A Követelmények lap megnyitása az Ütemezési táblán.](media/FAQ-Project-Booking-Schedule-Board-1.png "A foglalások és hozzárendelések tábla – képernyőkép")

2. Válassza ki a követelmény. A **Rendelkezésre állás keresése** fül jelenik meg a kiválasztott sor tetején.
 
3. A fül kiválasztásakor megnyílik az Ütemezés tábla Ütemezés-asszisztens módja, majd kiszűri a rendelkezésre álló erőforrásokat, amelyek megfelelnek az erőforrás-követelményeknek. Ezután lefoglalhat egy erőforrást.

4. A kijelölt sort az Ütemezés tábla aljáról a fenti rács erőforráscellájába is húzhatja. Amikor ledobja, megjelenik az **Erőforrás-foglalások létrehozása** panel a jobb oldalon.

    A **Foglalás** kijelölése lefoglaja az erőforrást a projektcsoport számára.

![Erőforrás-foglalási panel létrehozása.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Foglalás az elsődleges követelményből

Egy projekt létrehozása a Project Service megoldásban automatikusan hoz létre egy elsődleges követelmény nevű erőforrás-követelményt. Ez egy olyan üres követelmény, amelyet az erőforrás gyors ütemezéséhez használnak az Ütemezés táblán követelmény generálása vagy a nulláról való létrehozása nélkül. Mivel a követelmény üres, meg kell adnia a dátumokat, valamint a beosztási módszert és az órákat, ha alkalmazható. 

1. Erőforrás foglalásához az elsődleges követelménnyel az Ütemezés táblán válassza a **Projekt** fület. Szükség lehet az oszlopszűrő használatára a **Projekt** oszlopon, ha több projekttel rendelkezik.

   ![Oszlopszűrők az Ütemezési táblán.](media/FAQ-Project-Booking-Schedule-Board-2.png "A foglalások és hozzárendelések tábla – képernyőkép")

2. Válassza ki azt a követelményt, amelynek csak a projekt neve lesz a neve, és időtartama nulla (0).

3. Válassza az **Elérhetőség keresése** lapot, amely a soron jelenik meg. Ez az Ütemezés táblát Ütemezés-asszisztens módra állítja, és megmutatja a rendelkezésre álló erőforrásokat, amelyek lefoglalhatók a projektre.

4. Mivel az **Elsődleges követelmény** nulla (0) időtartammal rendelkező, üres követelmény, az erőforrás kiválasztásakor és lefoglalásakor be kell állítania az időtartamot az **Erőforrás-foglalás létrehozása** panelen.

5. Az Ütemezés tábla alján kiválaszthatja a **Projekt elsődleges követelményét**, és áthelyezheti az erőforrásba, hogy lefoglalja.
 
    Mivel a **Elsődleges követelmény** egy nulla (0) időtartamú, üres követelmény, akkor kell beállítania az időtartamot az **Erőforrás-foglalás létrehozása** panelen, amikor kiválasztja és lefoglalja az erőforrást.
 
    Amikor egy erőforrást az Ütemezés táblán az **Elsődleges követelmény** lehetőségen keresztül foglal le, hozzárendelések nélkül adja hozzá azt a projektcsapathoz.
 
## <a name="book-from-a-new-resource-requirement"></a>Foglalás egy új erőforrás-követelményből
Az új erőforrás-követelményből történő foglaláshoz hajtsa végre a következő lépéseket. 

1. Lépjen az **Erőforráskövetelmény** elemre, majd válassza az **Új** lehetőséget új erőforráskövetelmény létrehozásához.

2. A **Projekt** fülön válasszon ki egy projektet a követelmény társításához.
 
    Az Ütemezés táblán ez az új követelmény **Nyílt követelmény** formájában jelenik meg, amelyet teljesíteni tud.

3. Foglalja le az erőforrást a projektcsapathoz történő hozzáadásához.

4. Miután lefoglalta az erőforrást, kézileg kell hozzárendelnie a feladatokat.



[!INCLUDE[footer-include](../includes/footer-banner.md)]