---
title: Projektlehetőségek másolása
description: Ez a cikk a projektalapú lehetőségek a Project Operationsben való másolásának módjáról nyújt tájékoztatást.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0fe29918e14a944de7277639f752ad53513a7589
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826131"
---
# <a name="copy-project-opportunities"></a>Projektlehetőségek másolása

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
