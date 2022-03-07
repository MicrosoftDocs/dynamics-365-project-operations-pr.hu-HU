---
title: Projekt értékesítési árlistáinak felülbírálása
description: Ez a témakör az egyéni értékesítési árlisták létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130851"
---
# <a name="override-project-sales-price-lists"></a>Projekt értékesítési árlistáinak felülbírálása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

## <a name="customer-specific-project-price-lists"></a>Az ügyfélre jellemző projektárlisták

Az ügyfél-specifikus árakra vonatkozó megállapodások projektárlisták formájában állíthatók be a Dynamics 365 Project Operations egy partnerrekordján.

Ha egy ügyfélhez tartozó projektárlistát szeretne létrehozni, akkor nyissa meg a partnerrekordot az **értékesítés** területen.

1. Nyissa meg a **Partnerek** listaoldalt.
2. Keresse meg és kattintson duplán egy ügyfélrekordra a **partner** részletező lap megnyitásához.
3. A **projektárlisták** lapon válassza a **+ új projektárlista^^ lehetőséget.
4. Az **új projektárlista** lapon válasszon ki egy árlistát a legördülő listából. Csak azok az árlisták szerepelnek a rendszerben, amelyek esetében a környezet értéke **értékesítés**, és amelynek pénzneme megegyezik a partner pénznemével.
5. Nevezze el a társítást, majd válassza a **Mentés** lehetőséget. Az ügyfélre jellemző projektárlista létrejön. Ezt az árlistát fogja használni a rendszer az ügyfélhez létrehozott projektárajánlatok vagy szerződések alapértelmezett projektáraihoz, ahol az árajánlat vagy a projektszerződés létrehozott dátuma az árlista érvényességi időszakába esik.

## <a name="custom-pricing-on-project-quotes"></a>Egyéni árazás a projektárajánlatoknál

A projektárajánlatoknál a projekt árazása kiindulhat az ügyféltől származó alapértelmezett standard árlistával, vagy a projektparaméterekből.

Ha egy adott árajánlaton belül egyéni árazásra van szüksége a projekthez kapcsolódó munkára vonatkozóan, akkor a projektárlistákhoz társított entitásból kaphatja meg.

Hajtsa végre az alábbi lépéseket az árajánlat-specifikus projektek árazásának beállításához.

1. Nyissa meg a projektárajánlatot, és válassza ki a **projektárlisták** lapot.
2. Az alrácsban válassza az **Egyéni árképzés létrehozása** lehetőséget.

Az árajánlathoz csatolt összes projektárlistát az program az új árlisták listájába másolja. Az új árlisták neve tükrözi az árajánlat nevét, amely a dátum- és időbélyegzőt tartalmazza az árlisták létrehozásának időpontjával.

Használhatja ezeket az árlistákat, és frissítheti a munka (szerepkörár) és költség (kategória ára) árait. Ezek az árak csak erre a projektárajánlatra vonatkoznak.

## <a name="price-lists-on-a-project-contract"></a>Projektszerződés árlistái

A Projektszerződésekben a projektek árazása mindig alapértelmezés szerint egyéni árlistaként szerepel a szerződés nevével és a létrehozott dátum- és időbélyegzővel, amelyet a rendszer a névhez fűzött. Ez akkor is igaz, ha a szerződés az árajánlat megnyerése után jött létre, vagy ha a szerződés a semmiből jött létre. Ha szükséges, eltávolíthatja ezt a társítást az egyéni árlistához, és ehelyett társíthat egy normál árlistát a projektszerződéshez.

Ha normál árlistát rendel az árajánlathoz vagy a szerződéshez tartozó projektárlistákhoz, akkor az árlista árain végrehajtott változtatások hatással vannak az árlistát használó összes ajánlatra és szerződésre.
