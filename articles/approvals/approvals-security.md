---
title: Biztonság és jóváhagyások
description: Ez a cikk a Microsoftban a jóváhagyásokkal való munka biztonsági beállításáról nyújt tájékoztatást Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525405"
---
# <a name="security-and-approvals"></a>Biztonság és jóváhagyások

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations két biztonsági szerepkört használ az idő-, költség- és anyagbejegyzések jóváhagyásának lehetővé tételéhez:

- Projekt jóváhagyója
- Projektjóváhagyó rendszergazda

## <a name="project-approver"></a>Projekt jóváhagyója

A projektidő, a költség és az anyagbejegyzések jóváhagyásához rendelkeznie kell a **Projektjóváhagyó** biztonsági szerepkör. Hozzáféréssel kell rendelkeznie a megfelelő kapcsolódó entitásokhoz is, például **a Projecthez**. Ezt a hozzáférést a Projektmenedzseri szerepkörrel rendelkező **személy rendelheti** hozzá. Ezenkívül a projekt csapattagjának kell lennie, és jóváhagyóként kell megjelölnie.

A nem projektbejegyzések jóváhagyásához a beküldő vezetőjének kell lennie.

## <a name="project-approver-admin"></a>Projektjóváhagyó rendszergazda

> [!NOTE]
> A [Jóváhagyás készletek](approval-sets.md) funkciót engedélyezni kell a Projektjóváhagyó rendszergazda funkció használata előtt.

A **Projektjóváhagyó rendszergazdai** biztonsági szerepkör lehetővé teszi a felhasználók számára, hogy megkerüljék a szabályzatokat, és lehetővé teszi a bejegyzések jóváhagyását az összes projektben. Ennek a szerepkörnek a hozzárendelése megkerüli azt az érvényesítési logikát, amely csapattagságot és jóváhagyóként való megjelölést igényel. Hozzáféréssel kell rendelkeznie a megfelelő kapcsolódó entitásokhoz, például **a Projecthez**. Ezt a hozzáférést a Projektmenedzseri szerepkörrel rendelkező **személy rendelheti** hozzá.

A RENDSZER felhasználói környezete ugyanúgy megkerüli az ellenőrzéseket, mint a Projektjóváhagyó rendszergazda biztonsági szerepkör.
