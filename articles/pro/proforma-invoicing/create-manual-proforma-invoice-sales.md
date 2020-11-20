---
title: Kézi proforma számla létrehozása – Lite
description: Ez a témakör a kézi proforma számlák a Project Operations alkalmazásban való létrehozásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176389"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Kézi proforma számla létrehozása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 a Project Operations alkalmazásban igény szerint manuálisan is létrehozhatók a proforma számlák. A **Projektszerződések** listából vagy a **Projektszerződés** részletei oldalon manuálisan létrehozhatja a proforma számlát.

##  <a name="project-contracts-list-page"></a>Projektszerződések listaoldala

A **Projektszerződések** listaoldalon jelöljön ki egy vagy több projektszerződést, és hozzon létre számlákat az összes kijelölt bejegyzéshez.

A rendszer ellenőrzi, hogy a kijelölt projekttervek közül melyik rendelkezik **Számlázásra kész** elmaradással a mai dátum előtt. Ezekből a szerződésekből a rendszer létrehozza a vázlat proforma számlákat. Ha egy projektszerződés több ügyfelet tartalmaz, akkor egy-egy számla is létrehozható egy ügyfelenként, és a több számla is projektszerződésenként.

Az összes létrehozott projektszámla elérhető a **Számla** oldalon az **Számlázás** szakaszban az **Értékesítés** területen.

## <a name="project-contract-details-page"></a>Projektszerződés részletei oldala

A proforma számla a **Projektszerződés** részletek oldaláról is létrehozható , amely létrehozza a számlát az adott projekt szerződéshez. A rendszer ellenőrzi, hogy a projektszerződés rendelkezik-e **Számlázásra kész** elmaradással a mai dátum előtt. Ezekből a szerződésekből a rendszer az egyes szerződéssorok ügyfeleinek számától függően létrehoz egy vázlat proforma számlát.

Ha egyetlen proforma számla létre lett hozva, megnyílik a **Számla** lap. Ha a projektszerződéshez több számlát hoz létre, a **Számlák** listaoldala nyílik meg, és megjeleníti az összes létrehozott számlát.
