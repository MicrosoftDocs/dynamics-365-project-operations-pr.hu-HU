---
title: Projektalapú szerződések másolása
description: Ez a cikk információkat nyújt a projektszerződések másolásáról a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410370"
---
# <a name="copy-project-based-contracts"></a>Projektalapú szerződések másolása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az új projektszerződések egyszerűen létrehozhatók a meglévő szerződések példányainak kétféle módon történő másolásával:

- A **Projektszerződések** listán válassza ki a projektszerződést, majd válassza a **Másolás** lehetőséget.
- A **Projektszerződés** részletek lapján válassza a **Másolás** lehetőséget.

Mindkét esetben megjelenik egy párbeszédpanel, ahol beállíthatja a másolt szerződés paramétereit. A párbeszédpanel a következő mezőket tartalmazza. A kiválasztott értékektől függően előfordulhat, hogy a másolási folyamat megváltozhat.

| Mező | Description | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| Témakör | Adja meg a célszerződés témáját. Amikor megnyílik a párbeszédpanel, a rendszer a forrás szerződés nevére állítja be ezt a mezőt a "másolat" szót hozzáfűzve. | Ennek a mezőnek nincs későbbi hatása. |
| Ügyfelünk | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. Amikor megnyílik a párbeszédpanel, a rendszer beállítja ezt a mezőt a forrásszerződés partnerére. | Ez a mező az szerződésen szereplő elsődleges ügyfél. |
| Tulajdonos vállalat | Az üzlethez kapcsolódó projektek teljesítéséért felelős vállalat. Amikor megnyílik a párbeszédpanel, a rendszer beállítja ezt a mezőt a forrásszerződés tulajdonos vállalatára. | A tulajdonos vállalat az a jogi személy, amely az üzlet lezárása után fogja végrehajtani a projektet. A tulajdonos vállalata pénzneme meg kell egyezzen a projektben szereplő szerződő egység pénznemével. |
| Szerződő részleg | Az üzlethez kapcsolódó projektek teljesítéséért felelős szervezeti egység. Amikor megnyílik a párbeszédpanel, a rendszer beállítja ezt a mezőt a forrásszerződés szerződő egységére. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő részleghez tartozik pénznem. A pénznem kerül felhasználásra a projekthez kapcsolódó becsült és ténylegesen felmerült költségek jelentésére. |
| Pénznem | A pénznem, melyben az üzlet lebonyolításra kerül. Amikor megnyílik a párbeszédpanel, a rendszer beállítja ezt a mezőt a forrásszerződés pénznemére. A pénznem módosítható. Ha van, akkor az **Árképzés másolása** mező értéke mindig **Nem**, mert a forrás szerződésben szereplő árlisták már nem relevánsak. | Eza pénznem kerül felhasználásra az alapértelmezett árlistákhoz, pénzügyi becslések generálásához az szerződéshez, és az üzlet megnyerése után az ügyfélnek történő számlázásra. |
| Kért szállítási dátum | Az ügyfél által kért szállítási dátum. | Ez a dátum a számlázási dátumok adott gyakoriság szerinti létrehozásakor záró dátumként használható. |
| Árképzés másolása | Egy érték, amely azt jelzi, hogy a szerződésben szereplő árazást át kell-e másolni a forrásszerződésből. | Ha a mező **Igen** értékre van állítva, akkor a program a projektárlista és a termékárlista hivatkozásait átmásolja a forrásszerződésből a célszerződésbe. Ha a **Nem** beállítást választja, a rendszer a partner- vagy a projektparaméterekben található legfrissebb árlisták alapján újra alapértékekre állítja az árlistákat. |

Amikor az **OK** lehetőséget választja, a párbeszédoldalon, a rendszer a párbeszédpanelen beállított paraméterek alapján létrehoz egy másolatot a szerződésről. Ezután megnyílik az új szerződés.

A következő információkat a rendszer **nem** másolja a forrásszerződésből a célszerződésbe, mert az mindegyik szerződésben egyedi:

- Számlaütemezések
- Szerződés és szerződéssor ügyfelei
- Projektre vonatkozó referencia a projekt alapú szerződéssorok alapján
- Ügyfélköltségvetés adatai

A projektek és termékek szerződéssorai, az szerződéssor részleteinek becslései és a nem meghaladandó értékek a szerződés szintjén másolásra kerülnek. Az alapértelmezett árak és a költségarány bevitele a **Paraméterek másolása** párbeszédpanelen kiválasztott **Árképzés másolása** beállítástól függnek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
