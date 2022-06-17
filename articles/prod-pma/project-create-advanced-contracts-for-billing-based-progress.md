---
title: Speciális szerződések létrehozása folyamatalapú számlázáshoz
description: Ez a cikk bemutatja, hogyan hozhat létre projektszerződéseket, hogy a befejezett munka százalékos aránya alapján számlákat hozhasson létre a vevők számára.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26fe072b8241c7fdc96629f534e33a8fe53d3164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913669"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Speciális szerződések létrehozása folyamatalapú számlázáshoz
[!include [banner](../includes/banner.md)]

Ez a cikk azt ismerteti, hogyan hozhat létre projektszerződéseket, hogy a befejezett munka százalékos aránya alapján számlákat hozhasson létre a vevők számára. A számlaösszegeket a program automatikusan kiszámítja a projekthez beállított, meghatározott költségvetési kategóriákhoz. A számla időzítését akkor adja meg a program, amikor egyezteti a projektszerződést az ügyféllel.

A cikkben ismertetett eljárásokkal beállíthat egy szerződést, egy társított projektet, valamint azokat a számlázási szabályokat, amelyek a projekthez beállított költségvetési munkakategóriákhoz tartozó számlaösszegeket számítják ki.

A szerződés és a projekt létrehozása után beállíthatja a projekt részleteit. Megadhatja például a tevékenységeket, és a projekthez rendelheti a dolgozókat.

## <a name="example"></a>Példa

Szervezete egy szoftverfejlesztő cég. Ön vállalja, hogy kidolgozza a bérszámfejtési csomagot az ügyfél számára a teljes 20 000 USA dolláros (USD) díjért. A szervezete vállalja, hogy a projekt adott százalékának végrehajtásakor számláz az ügyfélnek. A következő projektkategóriákat állíthatja be a munkához, hogy a számlázási folyamatban használhatók legyenek:

- Konzultáció
- Tervezés
- Telepítés

Olyan számlázási szabályokat is kell beállítani, amelyek automatikusan kiszámítják a számlaösszegeket az egyes kategóriákhoz tartozó befejezett projektmunka-mennyiségek százalékos arányai alapján.

A költségvetés-kezelő a projektkategóriák költségvetését hozza létre. A befejezett munkák összegét a rendszer automatikusan kiszámítja a tényleges munkamennyiség százalékában, a tervezett költségvetési összegekkel összehasonlítva.

## <a name="prerequisites"></a>Előfeltételek

A számlázási szabályokat használó projekt létrehozása előtt be kell állítania a számlázási szabályok számsorozatait és a folyamatszámlák elszámlálásához használt díjnaplót.

1. Lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
2. A **Projektmenedzsment és könyvelési paraméterek** oldalon a **Számsorozatok** lapon állítsa be a számlázási szabályok létrehozásakor használni kívánt számsorozatot.
3. Lépjen a **Projektvezetés és könyvelés** \> **Naplók** \> **Díj** elemre.
4. A **Díjnapló** lapon válassza az **Új** lehetőséget, majd írja be a napló nevét.

## <a name="create-a-contract-for-progress-billings"></a>Szerződés létrehozása folyamatban lévő számlázásokhoz

Ezzel az eljárással hozhat létre projektszerződést egy rögzített árú projekthez. A projektszámlát akkor hozza létre, amikor a projekten végrehajtott munkavégzés eléri a megadott százalékértéket.

1. Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Projektszerződések** elemre.
2. A **Projektszerződések** oldalon válassza az **Új** lehetőséget.
3. Az **Új projektszerződés** párbeszédablakon állítsa be a következő mezőket:

    - **Név**
    - **Finanszírozás típusa**
    - **Finanszírozási forrás**
    - **Értékesítési pénznem** – Ez a pénznem alapértelmezés szerint a projekt szerződéshez társított vevői számlákhoz használható. Egy adott vevői számlán azonban megváltoztathatja az értékesítési pénznemet.

4. Kattintson az **OK** gombra. A rendszer átmásolja az információkat a **projektszerződések** oldal fejlécébe.
5. A **projektszerződések** lapon töltse ki a projekthez szükséges összes információt.

## <a name="create-a-project-for-progress-billings"></a>Projekt létrehozása folyamatban lévő számlázásokhoz

A következő lépések végrehajtásával hozhat létre projekteket és a projekt szerződéshez kapcsolódó alprojekteket.

1. Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre.
2. Az **Összes projekt** lapon válassza az **Új** lehetőséget.
3. Az **új projekt** párbeszédpanel **projekttípus** mezőjében válassza az **idő és az anyag** elemet.
4. Válasszon ki egy projektcsoportot. A projektcsoport határozza meg a csoporthoz rendelt projektek feladási információit.
5. Válassza a **Projekt létrehozása** lehetőséget.
6. A projekt létrehozása után állítsa be a projekt fázisát **folyamatban** értékre.

## <a name="create-a-budget-for-a-project"></a>Költségvetés létrehozása projekthez

A költségvetési kategóriák segítségével a rendszer automatikusan kiszámítja a számlaösszegeket az egyes kategóriákhoz tartozó befejezett munkamennyiségek százalékos arányai alapján. A következő lépések végrehajtásával költségvetési kategóriákat hozhat létre a becsült költségekhez.

1. Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** elemre.
2. Az **Összes projekt** lapon jelölje ki a kívánt projektet, és nyissa meg azt.
3. A **projektek** lap művelet ablaktáblájának **tervezés** lapján, a **költségvetés** csoportjában válassza a **projektköltségvetés** elemet.
4. A **projektköltségvetés** lapon adjon meg egy becsült költséget a projekt egyes kategóriáira vonatkozóan.

## <a name="create-billing-rules-for-progress-billings"></a>Számlázási szabályok létrehozása a folyamatban lévő számlázáshoz

1. Lépjen a **Projektvezetés és könyvelés** \> **Projektek** \> **Projektszerződések** elemre.
2. A **Projektszerződések** oldalon válassza ki és nyissa meg a projektszerződést.
3. A projektszerződés oldalon **Számlázási szabályok** gyorslapján válassza a **Hozzáadás** lehetőséget.
4. A **Számlázási szabály** lap **sortípusa** mezőjében válassza a **folyamatjelző** lehetőséget.
5. Adja meg a szerződés teljes értékét a **Számlázási szabály sorának részletei** gyorslapon, a **Szerződés értéke** mezőben.
6. A **Kategória** mezőben válassza ki, hogy milyen kategóriába szeretné könyvelni a díjtranzakciót.
7. A **Projekt** mezőben jelölje ki a számlázási szabályt használó projektet.
8. Nem kötelező: a számlázási szabályt további projektekhez rendelje hozzá. A **Projekt** gyorslapon, a **rendelkezésre álló projektek** szakaszban jelöljön ki egy projektet, majd a jobb nyílra kattintva adja hozzá a projektet a **kijelölt projektek** szakaszhoz.
9. Nem kötelező: a százalékos összeg kiszámítása, amelyet az ügyfél visszatart a számla kifizetéséről. A **fizetési adatok megőrzési feltételei** gyorslapon válassza ki a finanszírozási forrást, majd az **Adatmegőrzési százalék** mezőben adja meg a megőrzési százalékot.
10. Ismételje meg ezeket a lépéseket, ha további számlázási szabályokat szeretne létrehozni a projektszerződéshez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]