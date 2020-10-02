---
title: Árképzési dimenzió kikapcsolása
description: Ez a témakör az árképzési dimenziók kikapcsolásáról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896509"
---
# <a name="turning-off-a-pricing-dimension"></a>Árképzési dimenzió kikapcsolása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát. A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására. Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg. Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására és a **Munkakörnyezet** új árképzési dimenzió létrehozására. 

Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.

Ekkor azonban a hibaüzenet jelenhet meg: **Az árképzési dimenzió nem frissíthető és nem törölhető, ha vannak társított árképzési rekordok vannak.**

Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz. Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani. Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra. Erre az ellenőrzésre azért van szükség, mert minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie. Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak. 

| Normál cím         | Szerv. egység    |Egység   |Ár  |Pénznem  |
| -----------------------|-------------|-------|-------|----------|
| Rendszermérnök|Contoso USA|Hour| 100|USD|
| Vezető rendszermérnök|Contoso USA|Hour| 150| USD|


Ha kikapcsolja a **Normál cím** árképzési dimenziót, és az árképzési motor árat keres, akkor a bemeneti környezetből csak a **Szerv. egység** értéket fogja használni. Ha a bemeneti kontextus **szervezeti egysége** a „Contoso US”, az eredmény nem lesz determinisztikus, hiszen mindkét sor egyezik. Ennek elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a rendszer ellenőrzi, hogy a dimenziók kombinációja egyedi-e. Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető. Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.
