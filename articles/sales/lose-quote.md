---
title: Projektalapú árajánlatok másolása
description: Ez a témakör a projektalapú árajánlatok Project Operationsben való másolásának módjáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e8611f34a23d6d87317cc785148c1a3f9c26dca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588049"
---
# <a name="copy-project-based-quotes"></a>Projektalapú árajánlatok másolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A meglévőket másolva egyszerűen hozhat létre új projektárajánlatot. 

- Projektárajánlat másolásához válassza ki a másolni kívánt projektárajánlatot a **Projektárajánlatok** listaoldalon vagy a **Projektárajánlat** részletek oldalán, majd válassza a **Másolás** lehetőséget.

Ekkor megnyílik egy párbeszédpanel, ahol megadhatja a másolat paramétereit. A következő táblázat a párbeszédpanelen szereplő mezőket sorolja fel. A kiválasztott értékektől függően előfordulhat, hogy a másolási folyamat megváltozhat.

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Téma | Adja meg a cél árajánlat releváns témakörét vagy nevét. Amikor megnyílik a párbeszédpanel, a rendszer a forrás árajánlat témakörére állítja be a **-másolat** karaktersorozatot hozzáfűzve. | |
| Potenciális ügyfél | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. Amikor megnyílik a párbeszédpanel, a rendszer beállítja a forrás árajánlat partnerére. | Ez a mező az árajánlatban szereplő elsődleges ügyfél. |
| Szerződő részleg | Az üzlethez kapcsolódó projekt(ek) teljesítéséért felelős szervezeti egység.
Amikor megnyílik a párbeszédpanel, a rendszer beállítja a forrás árajánlat szerződő részlegére. | A szerződő részleg a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő részleghez tartozik pénznem. Ez a pénznem kerül felhasználásra a projekt végrehajtásához kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
| Pénznem | Ez a pénznem, melyben az üzlet lebonyolításra kerül. Amikor megnyílik a párbeszédpanel, a rendszer beállítja a forrás árajánlat pénznemére. Ez módosítható, és ha módosításra kerül, az **Árképzés másolása** mező értéke mindig **Nem** lesz. Ennek oka az, hogy a forrás árajánlathoz tartozó árlisták már nem relevánsak. | A pénznem kerül felhasználásra az alapértelmezett árlistához, pénzügyi becslés készítéséhez az árajánlaton, és végül az üzlet megnyerése után az ügyfélnek történő számlázásra. |
| Kért kézbesítési dátum | Ez az ügyfél által kért szállítás dátuma. | Ez a számlázási dátumok adott gyakoriság szerinti létrehozásakor záró dátumként használható. |
| Árképzés másolása | Az Igen/Nem érték azt jelzi, hogy az árajánlatban szereplő árazást át kell-e másolni a forrás árajánlatból. | Ha az **Igen** lehetőséget választja, akkor a program a projektárlista és a termékárlista hivatkozásait átmásolja a forrás árajánlatból a cél árajánlatba. Ha a **Nem** beállítást választja, a rendszer a partner- vagy a projektparaméterekben beállított legfrissebb árlisták alapján újra alapértékekre állítja az árlistákat. |

Amikor az **OK** lehetőséget választja, a párbeszédoldalon, a rendszer a párbeszédpanelen kiválasztott paraméterek alapján létrehoz egy másolatot a projektárajánlatról. Megnyílik az új projektárajánlat. 

> [!NOTE]
> A következő információkat nem másolja a program a forrásból a cél árajánlatba:
>
> - Számlaütemezések
> - Árajánlati és árajánlatsori ügyfelek
> - Projekthivatkozás a projektalapú árajánlatsorok Ügyfélköltségvetés-információira
>
>Mivel ez az információ nagyon jellemző az egyes ajánlatokra, ezeket a mezőket és rekordokat nem másolja a rendszer. A projektek és termékek árajánlatsorai, az árajánlatsor-részletek becslései és a nem meghaladandó értékek az árajánlat szintjén másolásra kerülnek. Az ár és a költségarány alapértelmezései a **Paraméterek másolása** párbeszédpanelen kiválasztott **Árképzés másolása** beállítástól függnek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]