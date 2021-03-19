---
title: Projektalapú lehetőségek másolása
description: Ez a témakör a projektalapú lehetőségek a Project Operationsben való másolásának módjáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1808469a34e05eb926f13c62ec634e8273b0e33c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278556"
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