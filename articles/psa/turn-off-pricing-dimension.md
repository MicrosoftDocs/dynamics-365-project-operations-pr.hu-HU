---
title: Árazási dimenzió kikapcsolása
description: Ez a témakör bemutatja, hogyan állíthatja be az árazási dimenziókat a Project Service megoldásban.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f308104246efe671d2001e660aa8c0ab9ef44c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581701"
---
# <a name="turn-off-a-pricing-dimension"></a>Árazási dimenzió kikapcsolása

[!include [banner](../includes/psa-now-project-operations.md)]

Előfordulhat, hogy néhány évente felül kell vizsgálnia és frissítenie kell az árképzési stratégiát. A frissítések elvégzéséhez szükség lehet egy meglévő árazási dimenzió kikapcsolására és egy új létrehozására. Például előfordulhat, hogy korábban a **Szerep** árát határozta meg, de most úgy döntött, hogy az **Munkakörnyezet** szerinti árat határozza meg. Ehhez szükség lehet a **Szerep** árképzési dimenzió kikapcsolására, és a **Munkakörnyezet** új árképzési dimenzió létrehozására. 

Árképzési dimenzió kikapcsolása, függetlenül attól, hogy kész vagy egyéni, lehetséges a **Költségre vonatkozó** és **Értékesítésre vonatkozó** mezők **Nem**-re állításával.

Ennek végrehajtásakor azonban a következő hibaüzenet jelenhet meg.

![Üzleti folyamat hiba valószínűsíthető, amikor kikapcsolja az árképzési dimenziót.](media/Business-Process-Error.png)


Ez a hibaüzenet azt jelzi, hogy vannak árrekordok, amelyeket korábban beállítottak a kikapcsolt dimenzióhoz. Az összes **Szerepár** és **Szerep felár** rekordot, amely egy dimenzióra utal, törölni kell, mielőtt a dimenzió alkalmazhatóságát **Nem** értékre lehet állítani. Ez a szabály vonatkozik mind a beépített árképzési dimenziókra, mind az esetlegesen létrehozott egyedi árképzési dimenziókra. Ennek az érvényesítésnek az az oka, hogy a Project Service korlátozza, hogy minden **Szerepár** rekordnak egyedi dimenziókombinációval kell rendelkeznie. Például az **US Cost Rates 2018** nevű árlistán a következő **Szerepár** sorok vannak. 

| Normál cím         | Szerv. egység    |Egység   |Ár  |Pénznem  |
| -----------------------|-------------|-------|-------|----------|
| Rendszermérnök|Contoso USA|Hour| 100|USD|
| Vezető rendszermérnök|Contoso USA|Hour| 150| USD|


Ha kikapcsolja a **Normál cím**-et árképzési dimenzióként, és a Project Service árazási motorja árat keres, akkor csak a **Szerv. egység** értéket a bemeneti környezetből fogja használni. Ha a bemeneti kontextus **szervezeti egysége** a „Contoso US”, az eredmény nem lesz determinisztikus, hiszen mindkét sor egyezik. E forgatókönyv elkerülése érdekében, amikor **Szerepár** rekordokat hoz létre, a Project Service ellenőrzi, hogy a dimenziók kombinációja egyedi-e. Ha a dimenziót a **Szerepár** rekordok létrehozása után kikapcsolják, ez a korlátozás megsérthető. Ezért szükséges, hogy mielőtt kikapcsolna egy dimenziót, törölje az összes **Szerepár** és **Szerep felár** sort, amelyekben a dimenzió értéke kitöltve van.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
