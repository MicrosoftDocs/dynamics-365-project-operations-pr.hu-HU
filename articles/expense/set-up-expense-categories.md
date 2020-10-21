---
title: Költségkategóriák beállítása
description: Ez a témakör a költségkategóriák és a megosztott kategóriák költségjelentésekhez való beállításával kapcsolatban tartalmaz tájékoztatást.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896689"
---
# <a name="set-up-expense-categories"></a>Költségkategóriák beállítása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Amikor az alkalmazottak költségjelentéseket készítenek, az általuk rögzített kiadásoknak egy költségkategóriához kell társítva lennie. A költségkategóriák olyan megosztott kategóriákból származnak, amelyek megoszthatók a szervezet jogi entitásai között. A szervezet definiálásának függvényében ezek a költségkategóriák más területeken is megoszthatók. A szervezet definíciója és a megvalósítási csoport útmutatása alapján meg kell határozni, hogy a költségkezelésben használt kategóriákat csak a költségkezelésben -használja a program, vagy más területeken is meg kell osztania.

> [!NOTE]
> Ezek a kategóriák megoszthatók a Projektmenedzsment és könyvelés és a Költségkezelés vagy a Projektmenedzsment és könyvelés és Termelés között. Nem oszthatók meg azonban a Költségkezelés és a Termelés között.

A beállítási folyamat megkezdése előtt a következő döntéseket kell meghozni minden egyes költségkategóriára vonatkozóan:

- Mi a költségkategória? Ilyenek például a repülőjáratok, a szállodák vagy az útiköltségtérítés kategóriái.
- A költségkategória használható a Projektmenedzsment és könyvelés modulban is? Ha igen, akkor a következő döntéseket kell meghoznia:

    - Milyen költségszámlákat fog használni a következő kiadásokhoz?

        - Költség
        - Bérlista-hozzárendelés
        - Folyamatban lévő termelés költségértéke
        - Költségelem
        - Folyamatban lévő termelés költségérték-eleme
        - Elhatárolt veszteség
        - Folyamatban lévő termelés elhatárolt vesztesége

    - Milyen bevételi számlákat fog használni a következő bevételi források esetén?

        - Számlázott bevétel
        - Elhatárolt bevétel – Értékesítési érték
        - Folyamatban lévő termelés – értékesítési érték
        - Elhatárolt bevétel – termelés
        - Folyamatban lévő termelés
        - Elhatárolt bevétel – profit
        - Folyamatban lévő termelés – profit
        - Elhatárolt bevétel – előfizetés
        - Folyamatban lévő termelés – előfizetés

- Mi a költségtípus?
- Mi a költségkategória alapértelmezett fizetési módja?
- A költség kategóriába tartozó költségeket tételezni kell?
- Mi a költségkategória fő alapértelmezett számlája?
- Mi a költségkategória alapértelmezett cikkáfacsoportja?
- Engedélyezve vannak a költségkategóriához további fizetési módok? Ha igen, melyek ezek?
- Vannak alkategóriák ebben a költségkategóriában? Ha vannak alkategóriák, akkor a következő döntéseket kell meghoznia:

    - Van olyan alkategória, amely ki van zárva az adó visszaigényléséből?
    - Mi ezen alkategóriák cikkáfacsoportja?
