---
title: Új projekt létrehozása
description: Ez a témakör információt nyújt egy új projekt létrehozásáról.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985954"
---
# <a name="create-a-new-project"></a>Új projekt létrehozása

[!include [banner](../includes/banner.md)]

A következő lépések elvégzésével hozhat létre új projektet.

1. A **Projektmenedzsment** oldalon válassza az **Új projekt** lehetőséget, és adja meg a következő értékeket:

    - **Projekttípus:** Idő és anyag
    - **Projekt neve:** XYZ frissítés 2. fázis
    - **Projektcsoport:** TM\_WIP
    - **Projektszerződés azonosítója:** 00000002

2. Válassza a **Projekt létrehozása** lehetőséget.

## <a name="assign-a-resource-to-a-project"></a>Erőforrás hozzárendelése egy projekthez

1. A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki annak a dolgozónak a rekordját, akihez korábban kompetenciákat hozott létre, és nyissa meg a dolgozó rekordját.
2. A Művelet panelen a **Projekt** lap **Beállítás** csoportjában válassza a **Projektek hozzárendelése** lehetőséget.
3. Az **Erőforrás-ellenőrzés projekt-hozzárendelései** oldal **Projektek** lapjának **Projekt hozzáadása a kijelölt projektekhez** mezőjében szűrjön az **XYZ frissítés 2. fázis** projektre.
4. A **Fennmaradó projektek** panelen válasszon ki egy projektet, majd válassza a nyíl gombot, majd adja hozzá a **Kijelölt projektek** panelhez.

Szükség szerint az erőforrásokhoz is hozzárendelhet kategóriákat. A kategória típusa vagy **Költség** vagy **Bevétel**. A kategória típusát a szervezete határozza meg. Ha egy erőforráshoz egyetlen kategória sincs hozzárendelve, akkor a Pénzügy az alapértelmezett kategóriát keresi ki a költség és a bevétel óránkénti ára esetében.

## <a name="set-up-project-resource-and-role-characteristics"></a>A projekt erőforrás- és szerepkörjellemzőinek beállítása

A projektmenedzser a projekterőforrások biztosításának funkciójával létrehozhatja a projekthez szükséges erőforrásokat. A szerepkörök használhatók, ha a megerősített erőforrások még nem ismertek az erőforrások lefoglalása esetén. A szerepkörök ideiglenesen lefoglalhatók fenntartott erőforrásként, így folytathatja a projektek tervezési fázisait.

[![Példa szerepkörre.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Szituáció:** A Contoso céget egy idő és anyag alapú projekttel bízták meg, amelyhez tartozik egy jóváhagyott projektcharterrel. A junior projektmenedzser még dolgozik a projekt hatókörének befejezésén. Az erőforrás-kezelő jelenleg azonosítja azokat az erőforrásokat, amelyek az új projekt munkájához lefoglalásra kerülnek. A projekt kritikus jellegéből adódóan a projekt szponzora az egyik szerepkörként a Senior projektmenedzsert kérelmezte. Az erőforrás-menedzsernek meg kell szereznie az új erőforrást, és meg kell adnia a szerepkört a rendszerben abban az esetben, ha a junior projektmenedzsernek erőforrásadatokra van szüksége a projekttervezés során.

A következő lépések azt mutatják, hogy az erőforrás-menedzser hogyan állíthatja be a Senior projektmenedzseri szerepkört, és társíthatja hozzá az erőforrás-jellemzőket. Később a szerepkör használható a szükséges erőforrás-kompetenciáknak megfelelő, rendelkezésre álló erőforrások keresésére.

1. A **Szerepek beállítása** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:

    - **Szerepkör-azonosító:** Senior projektmenedzser
    - **Leírás:** Senior projektmenedzser

2. Válassza a **Létrehozás** parancsot.
3. Válassza ki a **Senior projektmenedzser** szerepkört, majd válassza a **Tulajdonságok konfigurálása** lehetőséget.
4. A **Jellemzők típusa** mezőben válassza a **Készség** lehetőséget.
5. A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő készséget.
6. A **Jellemzők típusa** mezőben válassza a **Tanúsítvány** lehetőséget.
7. A **Rendelkezésre álló jellemzők** mezőben adja meg a keresendő tanúsítványtípust.

## <a name="assign-a-project-resource-to-a-project"></a>Projekterőforrás hozzárendelése egy projekthez

1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projektet.
2. A **Projektcsapat és ütemezés** lapon válassza a **Hozzáadás** lehetőséget.
3. A **Szerepkör** mezőben jelölje ki a **Csapattag** elemet.
4. Válassza a **Foglalás a naptárból** lehetőséget.
5. Az **Erőforrás elérhetősége** oldalon válassza a **Nézet beállításai** lehetőséget.
6. A **Nézet beállításainak módosítása** oldalon adja meg a következő értékeket:

    - **Dátumtartomány nézetének formátuma:** Nap
    - **Rendelkezésre állási leírások megjelenítése:** Igen
    - **Hátralévő kapacitás megjelenítése:** Igen

7. Válasszon ki egy erőforrást az erőforrások listájából.
8. Válassza **Végleges foglalás** és a **Teljes kapacitás** lehetőséget.

## <a name="assign-a-resource-to-a-default-role"></a>Rendeljen egy erőforrást az alapértelmezett szerephez

Segítségként a projekt- vagy erőforrás-menedzserek tovább fúrhatnak le az erőforrásokon, amelyek egy projekthez vannak lefoglalva. Az alapértelmezett szerepkör társítható meglévő erőforráshoz vagy újonnan megszerzett erőforráshoz. Amikor például Dániel felvették, megfelelő tapasztalattal és készségekkel rendelkezett az üzleti elemző szerepkör betöltésére. Az erőforrás-menedzser ezt a szerepkört rendelte Dánielhez alapértelmezett szerepkörként. Ezért az erőforrás-menedzser hozzáadta Dánielt a projekteken végzett munkához rendelkezésre álló üzleti elemzők készletéhez.

Az erőforrás-foglalás során a projektmenedzserek szűrhetik a projektek számára elérhető szerepkör-erőforrásokat. Ezeket az információkat felhasználhatják feltételként, amikor a többfeltételű döntési döntéselemzést hajtanak végre az erőforrás-teljesítés során. Emellett más erőforrás-jellemzőket is hozzáadhatnak a szűrőhöz, hogy olyan erőforrásokat keressenek, amelyek meghatározott készségekkel, oktatással és tapasztalattal rendelkeznek egy adott projekthez.

**Forgatókönyv:** Egy jóváhagyott projekt elindult, és a Senior projektmenedzser szerepe a projekt tervezési fázisában tervezett erőforrásként lett lefoglalva. Az erőforrás-menedzser most már megszerezte az erőforrást a Senior projektmenedzseri szerepkör betöltéséhez.

1. Az **Erőforrások listája** oldalon válassza a **Kovács Dániel** lehetőséget.
2. Az **Erőforrás szerepköre** oldalon válassza az **Új** lehetőséget, és adja meg a következő értékeket:

    - **Hatályos:** Adja meg az aktuális dátumot.
    - **Lejárat:** Adja meg a **Soha** értéket.
    - **Szerepkör:** Adja meg a **Senior projektmenedzser** értéket.

3. Válassza a **Mentés** lehetőséget, és zárja be az oldalt.
4. A **Kompetenciák** lapon adja hozzá a **ProjectMgmt** készséget és a **PMP** tanúsítványt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]