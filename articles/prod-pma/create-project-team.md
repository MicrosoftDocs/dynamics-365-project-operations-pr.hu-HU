---
title: Projektcsoport létrehozása
description: Ez a cikk a projektcsoportok létrehozásával és kezelésével kapcsolatban tartalmaz tájékoztatást.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927331"
---
# <a name="create-a-project-team"></a>Projektcsapat létrehozása

[!include [banner](../includes/banner.md)]

Ahhoz, hogy a projektben korábban beállított szerepköröket használni lehessen, a projektmenedzsernek hozzá kell rendelnie a szerepköröket a projekthez. A projektekhez több szerepkör is hozzárendelhető. A félreértések elkerülése érdekében ezeket a szerepköröket a rendszer automatikusan címkézi a foglalás során. Ha például a projektvezető három szoftvermérnököt igényel, akkor három szoftvermérnök szerepkör jön létre automatikusan az **1. szoftvermérnök**, **2. szoftvermérnök** és **3. szoftvermérnök** címkével. Ha előzőleg beállította a szerepkörhöz tartozó szerepkörjellemzőket, akkor az erőforrás keresései során szűrőként lesznek alkalmazva. A keresés további finomítása érdekében szükség esetén további jellemzők adhatók hozzá.

A nézet beállításai is testreszabhatók, így könnyebben áttekinthető az erőforrások elérhetősége is. Vannak olyan lehetőségek is, amelyek óránkénti, napi, heti, havi, negyedéves és éves bontásban mutatják a rendelkezésre állást. Lehetőség van az erőforrások rendelkezésre álló és fennmaradó kapacitásának megjelenítésére is. Ez a beállítás időgazdálkodásra is hasznos, ha a tevékenységek vagy az erőforrások elérhetőségének rendelkezésre álló idejét becsüli meg.

A projektmenedzser kiválaszthat egy szerepkört az oldalon, majd ha rendelkezésre áll egy, a követelménynek megfelelő erőforrás, akkor válassza a lehetőséget a szerepkör betöltéséhez szükséges erőforrás lefoglalásához. Ne feledje, hogy az erőforrásokat nem kell ezen a ponton a tervezési fázisban lefoglalni. Ha WBS-t hoz létre, a szerepköröket a projekthez tartozó munkatársakkal ellátott erőforrásokkal helyettesítheti. Ha a szerepeket munkatársakkal ellátott erőforrásokra cseréli le a WBS-ben, az erőforrás-beállítás automatikusan frissíti a projektcsapat felsorolását és ütemezését.

[![Projektcsoport felsorolása, amely a szerepköröket és a tényleges erőforrásokat egyaránt tartalmazza.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

A projektmenedzser többféle lehetőséget kínál a projektek erőforrás-foglalására, például a **Hátralévő kapacitás**, a **Teljes kapacitás**, a **Kapacitás százalékos értéke**, valamint az **Órák megadása**. Ezek a foglalási lehetőségek bármikor visszavonhatók, ha az erőforrás-hozzárendelések megváltoznak. A foglalás két típusa támogatott:

- **Végleges foglalás** – Az erőforrás-foglalás jóváhagyása megtörtént, és megerősítésre került, hogy a megadott időtartamra az aktivitáson dolgozik.
- **Ideiglenes foglalás** – Az erőforrás-foglalások feltételesen beállításra kerültek az aktivitáson a megadott időtartamig végzett munkára.

Az alábbi eljárás bemutatja, hogyan hozhat létre egy projektcsapatot:

## <a name="create-a-project-team"></a>Projektcsapat létrehozása

1. A **Minden projekt** listaoldalon jelöljön ki egy projektet, majd válassza a **Szerkesztés** lehetőséget.
2. A **Projektcsapat és ütemezés** lap **Ütemezés záró dátuma** mezőjében adja meg az ütemezés kezdő dátumát és egy hónapot. Ha például az ütemezés kezdő dátuma 2017. június 24. (24/06/2017), írja be a **24/07/2017** értéket.
3. Válassza a **Hozzáadás** lehetőséget.
4. A **Szerepkörök hozzáadása a projekthez** panel **Szerepkör** mezőjében válassza a **Senior projektmenedzser** lehetőséget.
5. Válassza ki a **Szükséges kompetenciák** lehetőséget.
6. A **Jellemzők kiválasztása** lapon a Senior projektmenedzser szerepkörhöz előzőleg beállított jellemzők alapértelmezés szerint be vannak jelölve. Kattintson az **OK** gombra.
7. A **Szerepkör hozzáadása a projekthez** oldal **Erőforrások száma** mezőjében adja meg az **1** értéket.
8. Az **Erőforrás** mezőben a keresés megjeleníti az összes olyan erőforrást, amely rendelkezik a szükséges kompetenciákkal. Válassza a **Kovács Dániel** lehetőséget, majd kattintson a **Létrehozás** gombra.
9. A **Projekt** oldalon válassza a **Hozzáadás** lehetőséget.
10. A **Szerepkörök hozzáadása a projekthez** panel **Szerepkör** mezőjében válassza a **Csapattag** lehetőséget. Az **Erőforrások száma** mezőben adja meg az **5** értéket.
11. Válassza a **Létrehozás** parancsot.
12. A **Projektek** lapon válassza az **Erőforrás teljesítése** lehetőséget.

## <a name="monitor-project-teams"></a>Projektcsoportok figyelése
1. A **Minden projekt** oldalon jelölje ki az **XYZ frissítés 2. fázis** projekt **Projektazonosító** hivatkozását.
2. A **Projektcsapat és ütemezés** gyorslapon ellenőrizze, hogy helyesek-e a listában szereplő projekterőforrások.


[!INCLUDE[footer-include](../includes/footer-banner.md)]