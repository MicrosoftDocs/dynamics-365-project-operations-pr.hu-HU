---
title: Alvállalkozói szerződések kezelése Project Operations-ben
description: Ez témakör áttekintést nyújt a Microsoft Dynamics 365 Project Operations teljes alvállalkozó-kezelési folyamatról.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994234"
---
# <a name="subcontract-management-in-project-operations"></a>Alvállalkozói szerződések kezelése Project Operations-ben

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations alvállalkozói szolgáltatása a következő üzleti folyamatokat támogatja.

![Alvállalkozói folyamat](../media/SubcontractingProcessFlow.png)

Itt az alvállalkozói folyamat részletes leírását találja.

1. A projektvezető alvállalkozói szerződést hoz létre egy alvállalkozóval. Alapértelmezés szerint a szállítói rekordhoz csatolt árlistákat használja a rendszer az alvállalkozóhoz. A szállítói fióknak egy **Szállító** vagy **Beszállító** kapcsolattípusa van.
2. A projektmenedzser az alvállalkozónál minden vásárlást sorelemként felszámíthat. Az alvállalkozósorok időre, kiadásokra vagy termékekre vonatkoznak. Az egyes alvállalkozósorok esetén kijelölt tranzakciós osztály határozza meg, hogy mire vonatkozik a sor.
3. A szállítói account manager és a projektmenedzser meg tud iterálni az alvállalkozói szerződésen. Az árképzés korrigálható a beszerzési árlistákon, amelyek csatolva vannak az alvállalkozói szerződéshez.
4. Ekkor vagy a folyamat egy későbbi részében, ha az alvállalkozói sor időt képvisel a szállító partnerkezelője kapcsolattartókat társít minden alvállalkozói sorhoz. Ez a társítás az alvállalkozóval dolgozó projektmenedzser számára nyújt tájékoztatást. Amikor egy kapcsolattartó alvállalkozói sorhoz van társítva, a rendszer automatikusan létrehoz egy lefoglalható erőforrást a kapcsolattartóból, amennyiben még nem létezik foglalható erőforrás.
5. Az egyes alvállalkozói sorok számlázási módja lehet **Rögzített árú vagy** **Idő és anyag**. Rögzített árú alvállalkozósorok számára beállíthat a mérföldkő alapú számlaütemezést.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
