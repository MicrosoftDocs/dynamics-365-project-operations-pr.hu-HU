---
title: Termékalapú szerződéssorok költségszámítása
description: Ez a témakör a létrehozásról nyújt információkat
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/20/2020
ms.locfileid: "4078323"
---
# <a name="costing-product-based-contract-lines"></a>Termékalapú szerződéssorok költségszámítása

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


Termék alapú szerződéssorok a Dynamics 365 Project Operations alkalmazásban tartalmazzák az **Önköltségi ár** mezőt, amely tárolja a termék önköltségi árát a későbbi jövedelmezőségi számításokhoz.

Ha egy termékalapú szerződéssor jön létre egy termékkatalógushoz, akkor a termékalapú szerződéssor költségét a rendszer alapértelmezés szerint a termékkatalógus **Általános költség** mezőjéből számítja ki. A termékkatalógus **Általános költség** mezőjének beállítása a szervezet alappénznemében történik. Amikor az egységköltség alapértelmezésben a szerződés sorában szerepel, akkor a rendszer a szerződésben szereplő értékesítési pénznemre váltja át.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Termékalapú szerződéssor egységára

A termékalapú szerződéssor egységköltségének a célja, hogy lehetővé tegye a különböző termékköltségeket az egyes értékesítési egységekhez. Bár nem minden esetben szükségesek, vannak olyan helyzetek, hogy a termék költségét engedményesen adja a szállító az ügyfélnek. Gondolja át a következő példát:

A Fabrikam Robotics a robotkarok telepítését végzi el az Adatum Corporation gyártósorain. A fabrikam üzembe helyezési szolgáltatásokat biztosít, de a robotkarokat a Trey Researchtől szerzi be. Ha a robotkarok telepítése az Adatum Corporation helyszínén új ipari vertikumot nyit a Trey Research robotkarjai számára, akkor a ők speciális engedményt adhatnak ehhez az üzlethez a Fabrikam számára. Ebben az esetben a Fabrikam egy termék-alapú szerződéssort hoz létre a Robotic Arms számára, és egy olyan egységenként költséget ad meg ehhez a szerződéshez, amely eltér a Trey Research robotkarjainak szokásos költségétől.
