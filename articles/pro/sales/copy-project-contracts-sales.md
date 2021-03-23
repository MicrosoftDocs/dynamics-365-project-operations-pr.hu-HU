---
title: Projektszerződések másolása - Lite
description: Ez a témakör információkat nyújt a projektszerződések másolásáról a Project Operations alkalmazásban.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a0ffb807c8254f4d392c4750fa0b4a60f7fd26b0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273741"
---
# <a name="copy-project-contracts---lite"></a>Projektszerződések másolása - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az új projektszerződések egyszerűen létrehozhatók a meglévő szerződések példányainak kétféle módon történő másolásával: 

  - A **Projektszerződések** listán válassza ki a projektszerződést, majd válassza a **Másolás** lehetőséget.
  - A **Projektszerződés** részletek lapján válassza a **Másolás** lehetőséget.

Ekkor megnyílik egy párbeszédpanel, ahol kiválaszthatja a másolt szerződés paramétereit. Töltse ki a következő mezőket a párbeszédpanelen. A párbeszédpanelen kiválasztott értékektől függően előfordulhat, hogy a másolási folyamat megváltozhat.

| **Mező** | **Leírás** | **Alsóbb rétegbeli hatás** |
| --- | --- | --- |
| Téma | Adja meg a célszerződés témáját. Amikor megnyílik a párbeszédpanel lapja, a rendszer a forrás szerződés nevére állítja be ezt a mezőt a **másolat** karaktersorozatot hozzáfűzve. | Ennek a mezőnek nincs későbbi hatása. |
| Ügyfél | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. Amikor megnyílik a párbeszédpanel, a rendszer beállítja ezt a mezőt a forrásszerződés partnerére. | Ez a mező az szerződésen szereplő elsődleges ügyfél. |
| Szerződő részleg | Az üzlethez kapcsolódó projekt(ek) teljesítéséért felelős Szervezeti egység. Amikor megnyílik a párbeszédpanel lapja, a rendszer beállítja a forrás szerződés szerződő részlegére. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő részleghez tartozik pénznem. A pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
| Pénznem | A pénznem, melyben az üzlet lebonyolításra kerül. Amikor megnyílik a párbeszédpanel lapja, a rendszer beállítja ezt a mezőt a forrásszerződés pénznemére. A pénznem módosítható. Ha van, akkor az **Árképzés másolása** mező értéke mindig **Nem**, mert a forrás szerződésben szereplő árlisták már nem relevánsak. | A pénznem kerül felhasználásra az alapértelmezett árlistákhoz, pénzügyi becslések készítéséhez az szerződéshez, és az üzlet megnyerése után az ügyfélnek történő számlázásra. |
| Kért kézbesítési dátum | Az ügyfél által kért szállítási dátum. | Ez a dátum a számlázási dátumok adott gyakoriság szerinti létrehozásakor záró dátumként használható. |
| Árképzés másolása | Azt jelzi, hogy a szerződésben szereplő árazást át kell-e másolni a forrásszerződésből. | Ha a mező **Igen** értékre van állítva, akkor a program a projektárlista és a termékárlista hivatkozásait átmásolja a forrásszerződésből a célszerződésbe. Ha a **Nem** beállítást választja, a rendszer a partner- vagy a projektparaméterekben található legfrissebb árlisták alapján újra alapértékekre állítja az árlistákat. |

Amikor az **OK** lehetőséget választja, a párbeszédoldalon, a rendszer a párbeszédpanelen kiválasztott paraméterek alapján létrehoz egy másolatot a szerződésről. Megnyílik az új szerződés.

A következő információkat nem másolja a program a **Forrásból** a **Célszerződésbe**:

  - Számlaütemezések
  - Szerződés és szerződéssor ügyfelei
  - Projektre vonatkozó referencia a projekt alapú szerződéssorok alapján
  - Ügyfélköltségvetés adatai

Mivel ez az információ specifikus az egyes szerződésekre, ezeket a mezőket és rekordokat nem másolja a rendszer. A projektek és termékek szerződéssorai, az szerződéssor részleteinek becslései és a nem meghaladandó értékek a szerződés szintjén másolásra kerülnek. Az ár és a költségarány alapértelmezései a **Paraméterek másolása** mezőben kiválasztott **Árképzés másolása** beállítástól függnek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]