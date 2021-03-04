---
title: Termékalapú szerződéssorok költségszámítása – Lite
description: Ez a témakör a létrehozásról nyújt információkat
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764462"
---
# <a name="cost-product-based-contract-lines---lite"></a>Termékalapú szerződéssorok költségszámítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A Dynamics 365 Project Operations-ben lévő termékalapú szerződéssorok tartalmazzák az **Önköltségi ár** mezőt, amely a termék önköltségi árát tárolja a későbbi jövedelmezőségi számításokhoz.

Ha egy katalógustermékhez termékalapú szerződéssort hoz létre, a sor költsége alapértelmezés szerint a termékkatalógus **Standard költség** mezőjéből kerül ki. A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik. Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Termékalapú szerződéssor egységára

A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez. Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek. Gondolja át a következő példát:

A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain. A Fabrikam telepítési szolgáltatásokat nyújt, de a robotkarok a Trey Research vállalattól származnak. Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára. Ebben az esetben a Fabrikam termékalapú szerződéssort hoz létre a robotkarokhoz. A szerződésben kiszerelési költséget kell megadni. A költség eltér a Trey Research robotkarjainak költségétől.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]