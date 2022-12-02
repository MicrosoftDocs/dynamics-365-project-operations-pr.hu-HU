---
title: Projekt állapotának szinkronizálása a lezárt projektekkel szembeni bejegyzések megakadályozásához
description: Ez a cikk ismerteti, hogyan szinkronizálható a Projekt állapota, hogy megakadályozza az inaktív és lezárt projektekhez bejegyzések hozzáadását.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348115"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projekt állapotának szinkronizálása a lezárt projektekkel szembeni bejegyzések megakadályozásához

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="scenario"></a>Forgatókönyv

A Contoso éles üzemre vált a Microsoft Dynamics 365 Project Operations erőforrás-alapú vagy nem készletalapú forgatókönyvekkel. A szokásos üzleti tevékenységek részeként projekteket végre lehet végrehajtani vagy várakoztatni lehet. Egy projekt inaktiválható, így biztosítható, hogy ne legyen semmilyen költség vagy számla generálva.

## <a name="solution"></a>Megoldás

### <a name="prerequisites"></a>Előfeltételek

-   A Microsoft Dynamics 365 Finance 10.0.29-es vagy újabb verzióját kell telepíteni.
-   A kettős írási leképezés 1.0.0.3 a Projektekhez V2 (msdyn\_projects) telepítése vagy manuális konfigurálása szükséges az alábbiakban leírtak szerint.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>A Project Operations integrációs projektek V2 kettős írási leképezés frissített verziójának létrehozása

A Project Operations Projektek V2 kettős írású leképezésének frissítéséhez:

1. Menjen az **Adatkezelés** munkaterületre, válassza a **Kettős írás** lehetőséget.
2. Válassza a **Kettős írás** csempét.
3. T **Táblaleképezés** oszlopban keresse meg és jelölje ki a **Project V2 (msdyn\_projects)** elemet, majd válassza a Leállítás lehetőséget.
4. Válassza ki a leképezés nevét a leképezés megnyitásához, majd válassza a **[Nincs]** lehetőséget.
5. Az Oszlop kijelölése párbeszédpanelen válassza a **statecode \[Projekt állapota\]** lehetőséget, majd válassza az OK lehetőséget. A lista szűkítéséhez beírhatja az **állapot** kifejezést a szűrőértékbe.
6.  Az átalakítás szerkesztéséhez válassza a **leképezés típusa** oszlop **Átalakítás hozzáadása vagy szerkesztése** parancsát.
7.  Az **Átalakítás típusa** helyen válassza a **ValueMap** lehetőséget.
8.  Válassza az **Értékleképezés hozzáadása** lehetőséget, majd adja hozzá a következő **Kulcsokat** és **Értékeket**:

   Key       | Érték 
   ----------|-------
   InProcess | 0     
   kész | 0     

![A kettős írási leképezést bemutató képernyőkép](media/projectstage-dw-mapping.png)

9. Válassza a **Mentés** parancsot.
10. A **Kettős írás > Projektek V2 (msdyn_projects)** oldal tetején válassza a **Mentés másként** lehetőséget.
11. A **Tábla hozzáadása** panel **Közzétevő** mezőjében válassza az **CDS alapértelmezett közzétevő** lehetőséget.
12. A **Verzió** mezőt állítsa 1.0.0.3 értékre.
13. Írjon be egy **Leírást**, majd válassza a **Mentés** lehetőséget.
14. A **Kettős írás > Projects V2 (msdyn_projects)** oldal tetején válassza a **Futtatás** lehetőséget a leképezés indításához, majd ha meg kell erősítenie a futtatás előtt, válassza az **Igen** lehetőséget. 

### <a name="close-a-newly-completed-project"></a>Újonnan befejezett projekt bezárása

A Dynamics 365 Finance a **projekt fázis** mezőt használja a **folyamatban lévő** vagy **befejezett** projektek megkülönböztetéséhez. A **Befejezett** projektekhez nem rendelhető költség, illetve nem számlázhatóak az ügyfeleknek.

1. Nyisson meg egy inaktiválandó projektet.
2. A menüszalagon válassza az **Inaktiválás** lehetőséget.

> [!NOTE]
> A projekt inaktiválható vagy lezárható, mivel mindkettő ugyanúgy viselkedik a Finance környezetében.

3. Nyissa meg a Finace-ben az **Összes projekt listája** oldalt.
4. Erősítse meg, hogy az inaktivált projekt nem jelenik meg a listában.
5. A lista fölötti **projektek megjelenítése** szűrőben módosítsa vissza az értéket **Aktívról** **Mindre**
6. Most már látható az inaktivált projekt.

Ha megpróbál időt vagy költséget naplózni a projekthez a Finance-ban, akkor nem látja a projektek kiválasztásra. Ha manuálisan adja meg a projektszámot egy költéségen, megjelenik egy üzenet, amely szerint "A befejezett projekt fázis nem teszi lehetővé a rögzítést a projektbe". A számlázási és egyéb számlázási funkciókat le kell tiltani, mivel egy lezárt projekt környezetében lesznek.

