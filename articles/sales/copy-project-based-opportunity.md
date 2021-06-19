---
title: Projektalapú lehetőségek másolása
description: Ez a témakör a projektalapú lehetőségek a Project Operationsben való másolásának módjáról nyújt tájékoztatást.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae724d18e768b838f388b6fd089bfa657c937da1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013444"
---
# <a name="copy-project-based-opportunities"></a>Projektalapú lehetőségek másolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A projektek lehetőségei könnyen átmásolhatók új projektlehetőségek létrehozásához. 

1. Nyissa meg a **Projekt lehetőségei** listát, és jelöljön ki egy lehetőséget a listából. Vagy nyissa meg egy adott lehetőség adatait tartalmazó oldalt. 
2. Bármelyik oldalról válassza a **Másolás** lehetőséget. Megnyílik egy párbeszédpanel, amely a következő mezőadatokat tartalmazza. A párbeszédpanelen kiválasztott értékektől függően előfordulhat, hogy a másolási folyamat más lehet.

    | **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
    | --- | --- | --- |
    | Téma | Adja meg a célszerződés vonatkozó témáját. Amikor megnyílik a párbeszédpanel, a rendszer a forrás lehetőség témakörére állítja be a **-másolat** karaktersorozatot hozzáfűzve. | Ennek a mezőnek nincs későbbi hatása. |
    | Fiók | Hivatkozások az ügyfél vállalati vagy partneri rekordjára. Amikor megnyílik a párbeszédpanel, a rendszer beállítja a forráslehetőség partnerére. | Ez a mező az lehetőségben szereplő elsődleges ügyfél. |
    | Szerződő részleg | Az üzlethez kapcsolódó projekt(ek) teljesítéséért felelős szervezeti egység. Amikor megnyílik a párbeszédpanel, a rendszer beállítja a forráslehetőség szerződő részlegére. | A szerződő részleg a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő egység pénznemmel rendelkezik, és ez a pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
    | Pénznem | A pénznem, melyben az üzlet lebonyolításra kerül. Amikor megnyílik a párbeszédpanel lapja, a rendszer beállítja a forráslehetőség pénznemére. | A pénznem az árlista alapértelmezett árlistához, és pénzügyi becslések készítéséhez szükséges az ajánlaton. Végül a pénznem az ügyfélnek az üzlet megnyerése esetén történő számlázásához is használva lesz. |
    | Árképzés másolása | Igen/nem érték, amely azt jelzi, hogy a lehetőség árazását át kell-e másolni a forráslehetőségből. | Ha az **Igen** jelölőnégyzet be van jelölve, akkor a program az árlistát a forrásból a cél lehetőségbe másolja. Ha a **Nem** beállítást választja, a rendszer a beállított legfrissebb árlisták alapján újra alapértékekre állítja az árlistákat. |

3. Kattintson az **OK** gombra. A rendszer a kijelölt paraméterek és az új projekt lehetőség alapján hozza létre a projektlehetőség egy példányát.


[!INCLUDE[footer-include](../includes/footer-banner.md)]