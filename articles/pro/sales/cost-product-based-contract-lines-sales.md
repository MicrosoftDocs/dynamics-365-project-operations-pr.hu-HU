---
title: Termékalapú szerződéssorok költségszámítása – Lite
description: Ez a cikk a létrehozásról nyújt információkat
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922915"
---
# <a name="cost-product-based-contract-lines---lite"></a>Termékalapú szerződéssorok költségszámítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A Dynamics 365 Project Operations-ben lévő termékalapú szerződéssorok tartalmazzák az **Önköltségi ár** mezőt, amely a termék önköltségi árát tárolja a későbbi jövedelmezőségi számításokhoz.

Ha egy katalógustermékhez termékalapú szerződéssort hoz létre, a sor költsége alapértelmezés szerint a termékkatalógus **Standard költség** mezőjéből kerül ki. A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik. Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Termékalapú szerződéssor egységára

A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez. Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek. Gondolja át a következő példát:

A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain. A Fabrikam telepítési szolgáltatásokat nyújt, de a robotkarok a Trey Research vállalattól származnak. Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára. Ebben az esetben a Fabrikam termékalapú szerződéssort hoz létre a robotkarokhoz. A szerződésben kiszerelési költséget kell megadni. A költség eltér a Trey Research robotkarjainak költségétől.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]