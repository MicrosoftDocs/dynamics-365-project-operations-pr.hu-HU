---
title: Kézi proforma számla létrehozása – Lite
description: Ez a témakör a kézi proforma számlák a Project Operations alkalmazásban való létrehozásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764506"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Kézi proforma számla létrehozása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations-ben a proforma számlák szükség szerint manuálisan is létrehozathatóak. A **Projektszerződések** listából vagy a **Projektszerződés** részletei oldalon manuálisan létrehozhatja a proforma számlát.

##  <a name="project-contracts-list-page"></a>Projektszerződések listaoldala

A **Projektszerződések** listaoldalon jelöljön ki egy vagy több projektszerződést, és hozzon létre számlákat az összes kijelölt bejegyzéshez.

A rendszer ellenőrzi, hogy a kijelölt projekttervek közül melyik rendelkezik **Számlázásra kész** elmaradással a mai dátum előtt. Ezekből a szerződésekből a rendszer létrehozza a vázlat proforma számlákat. Ha egy projektszerződés több ügyfelet tartalmaz, akkor egy-egy számla is létrehozható egy ügyfelenként, és a több számla is projektszerződésenként.

Az összes létrehozott projektszámla elérhető a **Számla** oldalon az **Számlázás** szakaszban az **Értékesítés** területen.

## <a name="project-contract-details-page"></a>Projektszerződés részletei oldala

Proforma számla is létrehozható a **Projektszerződés** részletei oldalon. A rendszer jóváhagyja azt a projektet, amely **Számlázásra kész** elmaradással rendelkezik a mai dátum előtt. Ezekből a szerződésekből a rendszer az egyes szerződéssorok ügyfeleinek számától függően létrehoz egy vázlat proforma számlát.

Ha egyetlen proforma számla létre lett hozva, megnyílik a **Számla** lap. Ha az adott projektszerződéshez több számlát is létrehoztak, akkor megnyílik a **Számlák** listaoldal, és megjelenik az összes létrehozott számla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]