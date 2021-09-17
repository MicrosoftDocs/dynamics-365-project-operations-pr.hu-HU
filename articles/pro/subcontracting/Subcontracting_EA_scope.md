---
title: Alvállalkozásba adás a 2021 októberi Early Access kiadásban
description: Ez a témakör áttekintést nyújt a Project Operations alvállalkozói képességekről, amelyek a 2021. októberi korai hozzáférésű kiadás részét képezik.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383698"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Alvállalkozásba adás a 2021 októberi Early Access kiadásban

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Dynamics 365 Project Operations alvállalkozói képességekről nyújt áttekintést, amelyek a 2021. októberi korai hozzáférésű kiadás részét képezik. Ez a funkciókészlet még nem áll készen a gyártásra vagy éles környezetekre, ezért ezek a funkciók korai hozzáférésű kiadásban maradnak, amíg a teljes funkciókészlet ki nem kerül. Határozottan javasoljuk, hogy ne használja az alvállalkozói funkciókészletet éles termelési forgatókönyvekhez, amíg az előnézeti banner nem kerül eltávolításra. 

Az alábbi lista áttekintést nyújt arról, hogy jelenleg mi érhető el a 2021. októberi Early Access kiadásban:

1. A projektvezető alvállalkozói szerződést hoz létre egy alvállalkozóval. Alapértelmezés szerint a szállítói rekordhoz csatolt árlistákat használja a rendszer az alvállalkozóhoz. A szállítói fióknak egy **Szállító** vagy **Beszállító** kapcsolattípusa van.

2. A projektmenedzser az alvállalkozónál minden vásárlást sorelemként felszámíthat. Az alvállalkozósorok időre, kiadásokra vagy termékekre vonatkoznak. Az alvállalkozói szerződéssor tranzakciós osztálya határozza meg, hogy mire szolgál a sor.

3. A szállítói account manager és a projektmenedzser meg tud iterálni az alvállalkozói szerződésen. Az árképzés korrigálható a beszerzési árlistákon, amelyek csatolva vannak az alvállalkozói szerződéshez.

4. Ezen a ponton vagy a folyamat későbbi szakaszában, ha az alvállalkozói szerződéssor időre szól, a szállítói számlavezető minden egyes alvállalkozói szerződéssorhoz hozzárendeli a szállítói kapcsolatokat. Ez a társítás az alvállalkozóval dolgozó projektmenedzser számára nyújt tájékoztatást. Amikor egy alvállalkozói szerződéssorhoz egy szállítói kapcsolat kapcsolódik, a rendszer automatikusan létrehoz egy foglalható erőforrást a kapcsolatból, ha még nem létezik foglalható erőforrás.

5. Az egyes alvállalkozói sorok számlázási módja lehet **Rögzített árú vagy** **Idő és anyag**. A fix áras alvállalkozói szerződéses sorok esetében mérföldkő-alapú számlázási ütemterv kerül felállításra.

Az alvállalkozói szerződéskötés üzleti folyamatának az áttekintésben felvázolt többi lépése jelenleg nem áll rendelkezésre. Amint új funkciókkal bővül, ez a téma frissülni fog. 

Az alábbi ábra az alvállalkozói korai hozzáférésű kiadást szemlélteti a végponttól végpontig tartó üzleti folyamattal szemben.

![Alvállalkozói folyamat](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Mennyiségalapú és munkaalapú alvállalkozói szerződéssorok korai hozzáférési felszabadítása
A 2021. októberi korai hozzáférésű kiadásban csak a mennyiségi alvállalkozói szerződéssorok támogatottak. Ez azt jelenti, hogy egy alvállalkozói szerződéssor felhasználható idő, költségek vagy anyagok beszerzésére egy szállítótól, de nem egy teljes munkacsoportra. Ez azt is jelenti, hogy az alvállalkozói soron vásárolt mennyiség (időegység, költség vagy anyagmennyiség) a rendszer bármelyik projektjénél felhasználható.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
