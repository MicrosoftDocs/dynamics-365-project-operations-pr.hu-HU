---
title: Újdonságok - 2021 wave 2 korai hozzáférés - Project Operations könnyű telepítés
description: Ez a témakör a Project Operations könnyű telepítés 2021 wave 2 korai hozzáférésű kiadásában elérhető funkciókról nyújt tájékoztatást.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323914"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Újdonságok - 2021 wave 2 korai hozzáférés - Project Operations könnyű telepítés

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

  - Project Operations a Dataverse-környezet 4.23.0.4 verzióján

A kiadás csak akkor kerül alkalmazásra, ha egy környezethez [kiválasztottal korai hozzáférésre](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

[Alvállalkozói szerződések kezelése](../subcontracting/subcontracting_EA_scope.md) - Ez a funkció jobb átláthatóságot és ellenőrzést biztosít a projektben végzett munka minden aspektusa felett. Az alvállalkozói szerződések kezelésének előnézete a következő képességeket tartalmazza:

  - A projektmenedzser alvállalkozói szerződést köthet egy szállítóval. Alapértelmezés szerint a szállítói rekordhoz csatolt árlistákat használja a rendszer az alvállalkozóhoz. A szállítói fióknak egy **Szállító** vagy **Beszállító** kapcsolattípusa van.
  - A projektmenedzser az alvállalkozói szerződésben tételesen felsorolhatja az összes beszerzést. Az alvállalkozósorok időre, kiadásokra vagy termékekre vonatkoznak. Az alvállalkozói szerződéssor tranzakciós osztálya határozza meg, hogy mire szolgál a sor.
  - A szállítói account manager és a projektmenedzser meg tud iterálni az alvállalkozói szerződésen. Az árképzés korrigálható a beszerzési árlistákon, amelyek csatolva vannak az alvállalkozói szerződéshez.
  - A folyamat során, ha az alvállalkozói szerződés sora időre szól, a szállítói számlavezető minden egyes alvállalkozói szerződés sorához társíthat szállítói kapcsolatokat. Ez a társítás az alvállalkozóval dolgozó projektmenedzser számára nyújt tájékoztatást. Amikor egy alvállalkozói szerződéssorhoz egy szállítói kapcsolat kapcsolódik, a rendszer automatikusan létrehoz egy foglalható erőforrást a kapcsolatból, ha még nem létezik foglalható erőforrás.
  - Az egyes alvállalkozói szerződéssorok számlázási módszere lehet fix áras vagy idő- és anyagköltséges. A fix áras alvállalkozói szerződéses sorok esetében mérföldkő-alapú számlázási ütemterv kerül felállításra.
