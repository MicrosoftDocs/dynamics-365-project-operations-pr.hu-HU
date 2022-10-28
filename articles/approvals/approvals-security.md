---
title: Biztonság és jóváhagyások
description: Ez a cikk a Microsoft jóváhagyásainak biztonsági beállításáról nyújt tájékoztatást Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709400"
---
# <a name="security-and-approvals"></a>Biztonság és jóváhagyások

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations két biztonsági szerepkört használ az idő-, költség- és anyagbejegyzések jóváhagyásának engedélyezéséhez:

- Projekt jóváhagyója
- Projekt jóváhagyó rendszergazdája

## <a name="project-approver"></a>Projekt jóváhagyója

A projektidő, a költségek és az anyagbejegyzések jóváhagyásához rendelkeznie kell a **projektjóváhagyó** biztonsági szerepkör. Hozzáféréssel kell rendelkeznie a megfelelő kapcsolódó entitásokhoz is, például **a Projecthez**. Ezt a **hozzáférést olyan személy rendelheti hozzá, aki projektmenedzseri** szerepkörrel rendelkezik. Emellett a projekt csapattagjának kell lennie, és jóváhagyóként kell megjelölnie.

A nem projektbejegyzések jóváhagyásához Önnek kell lennie a beküldő felettesének.

## <a name="project-approver-admin"></a>Projekt jóváhagyó rendszergazdája

> [!NOTE]
> A [Jóváhagyási készletek](approval-sets.md) funkciót engedélyezni kell a Project Approvalrover Admin funkció használata előtt.

A Project Approval Admin **biztonsági szerepkör lehetővé teszi a** felhasználók számára a házirendek megkerülését, és lehetővé teszi a bejegyzések jóváhagyását az összes projektben. Ennek a szerepkörnek a hozzárendelése megkerüli az érvényesítési logikát, amely csapattagságot és jóváhagyóként való megjelölést igényel. Hozzáféréssel kell rendelkeznie a megfelelő kapcsolódó táblákhoz, például **a Projecthez** az Önhöz rendelt biztonsági szerepkörökön keresztül.

A RENDSZER felhasználói környezet ugyanúgy megkerüli az ellenőrzéseket, mint a projektjóváhagyó rendszergazdai biztonsági szerepkör.
