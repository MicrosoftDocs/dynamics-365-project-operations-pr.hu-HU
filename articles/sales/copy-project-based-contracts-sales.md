---
title: Projektalapú szerződések másolása
description: Ez a cikk a projektszerződések Microsoftban történő másolásáról nyújt tájékoztatást Dynamics 365 Project Operations.
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

Egyszerűen létrehozhat új projektszerződéseket, ha a meglévő szerződéseket kétféleképpen másolja:

- **A Projektszerződések** listaoldalon válasszon ki egy projektszerződést, majd válassza a Másolás **lehetőséget**.
- A **Projektszerződés** részletek lapján válassza a **Másolás** lehetőséget.

Mindkét esetben megjelenik egy párbeszédpanel, ahol beállíthatja a másolt szerződés paramétereit. A párbeszédpanel a következő mezőket tartalmazza. A kiválasztott értékektől függően a másolási folyamat megváltozhat.

| Mező | Description | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| Témakör | Adja meg a célszerződés témáját. A párbeszédpanel megnyitásakor a rendszer a mezőt a forrásszerződés nevére állítja be, de a "másolás" szó hozzá van fűzve. | Ennek a mezőnek nincs későbbi hatása. |
| Ügyfelünk | Hivatkozás az ügyfél vállalati vagy partneri rekordjára. A párbeszédpanel megnyitásakor a rendszer a mezőt a forrásszerződésben szereplő fiókra állítja be. | Ez a mező az szerződésen szereplő elsődleges ügyfél. |
| Tulajdonos vállalat | Az a vállalat, amely felelős az üzlethez kapcsolódó projektek megvalósításáért. A párbeszédpanel megnyitásakor a rendszer a mezőt a forrásszerződés tulajdonos vállalatára állítja be. | A tulajdonos társaság az a jogi személy, amely az ügylet lezárása után végrehajtja a projektet. A tulajdonos társaság pénznemének meg kell egyeznie a szerződő egység pénznemével. |
| Szerződő részleg | Az a szervezeti egység, amely felelős az üzlethez kapcsolódó projektek megvalósításáért. A párbeszédpanel megnyitásakor a rendszer a mezőt a forrásszerződés szerződő egységére állítja. | A szerződő egység a vállalat azon részlege, amely a projekteket az üzlet lezárását követően végrehajtja. Minden egyes szerződő részleghez tartozik pénznem. Ez a pénznem a projekt során felmerült becsült és tényleges költségek jelentésére szolgál. |
| Pénznem | A pénznem, melyben az üzlet lebonyolításra kerül. A párbeszédpanel megnyitásakor a rendszer a mezőt a forrásszerződés pénznemére állítja. A pénznem módosítható. Ha igen, az **Árképzés** másolása mező mindig Nem **értékre** van állítva, mert a forrásszerződés árlistái már nem relevánsak. | Ez a pénznem az alapértelmezett árlistákhoz, a szerződés pénzügyi becsléseinek létrehozásához, valamint az ügylet megnyerésekor az ügyfélnek történő számlázáshoz használatos. |
| Kért szállítási dátum | Az ügyfél által kért szállítási dátum. | Ez a dátum a záró dátumként használatos, amikor meghatározott gyakorisággal hoz létre számlázási dátumokat. |
| Árképzés másolása | Egy érték, amely jelzi, hogy a szerződés árazását le kell-e másolni a forrásszerződésből. | Ha a mező Igen **értékre** van állítva, a projekt- és termékárlista-hivatkozások átmásolódnak a forrásszerződésből a célszerződésbe. Ha nemre **van** állítva, a rendszer az alapértelmezett árlistákat használja a fiók- vagy projektparaméterek legújabb árlistái alapján. |

Ha a párbeszédpanelen az OK gombot **választja**, a rendszer a beállított paraméterértékek alapján másolatot készít a szerződésről. Ezután megnyílik az új szerződés.

A rendszer nem **másolja a következő információkat** a forrásszerződésből a célszerződésbe, mert azok az egyes szerződésekre jellemzőek:

- Számlaütemezések
- Szerződés és szerződéssor ügyfelei
- Projektre vonatkozó referencia a projekt alapú szerződéssorok alapján
- Ügyfélköltségvetés adatai

A projektekre és termékekre vonatkozó szerződéses sorok, a szerződéssor részleteiben szereplő becslések, valamint a szerződés szintjén nem túllépett értékek másolásra kerülnek. Az alapértelmezett árak és a költségi díjak megadása a Paraméterek **másolása párbeszédpanel Díjszabás** másolása mezőjében **megadott** beállítástól függ.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
