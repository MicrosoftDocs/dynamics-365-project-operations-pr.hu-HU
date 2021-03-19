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
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273696"
---
# <a name="cost-product-based-contract-lines---lite"></a>Termékalapú szerződéssorok költségszámítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A Dynamics 365 Project Operations-ben lévő termékalapú szerződéssorok tartalmazzák az **Önköltségi ár** mezőt, amely a termék önköltségi árát tárolja a későbbi jövedelmezőségi számításokhoz.

Ha egy katalógustermékhez termékalapú szerződéssort hoz létre, a sor költsége alapértelmezés szerint a termékkatalógus **Standard költség** mezőjéből kerül ki. A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik. Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Termékalapú szerződéssor egységára

A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez. Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek. Gondolja át a következő példát:

A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain. A Fabrikam telepítési szolgáltatásokat nyújt, de a robotkarok a Trey Research vállalattól származnak. Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára. Ebben az esetben a Fabrikam termékalapú szerződéssort hoz létre a robotkarokhoz. A szerződésben kiszerelési költséget kell megadni. A költség eltér a Trey Research robotkarjainak költségétől.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]