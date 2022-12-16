---
title: Biztonság és jóváhagyások
description: Ez a cikk a Microsoft Dynamics 365 Project Operations jóváhagyások használatával kapcsolatos biztonsági beállítását mutatja be.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841926"
---
# <a name="security-and-approvals"></a>Biztonság és jóváhagyások

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations két biztonsági szerepkör segítségével teszi lehetővé az idő-, költség- és anyagbevitelek jóváhagyását:

- Projekt jóváhagyója
- Projekt jóváhagyó adminisztrátor

## <a name="project-approver"></a>Projekt jóváhagyója

A projektidővel, költséggel és anyagbevitelek jóváhagyásához a **Projektjóváhagyó** biztonsági szerepkörrel kell rendelkeznie. Emellett hozzáféréssel kell lennie a kapcsolódó entitásokhoz, például a **Projekt** entitáshoz. Ezt a hozzáférést olyan felhasználó hozzárendelheti Önhöz, aki **Projektmenedzser** szerepkörrel rendelkezik. Emellett a projekt csoporttagnak kell lennie, és jóváhagyóként kell megjelölve lennie.

A projekten kívüli bejegyzések jóváhagyásához Önnek kell a beküldő vezetőjének kell lennie.

## <a name="project-approver-admin"></a>Projekt jóváhagyó adminisztrátor

> [!NOTE]
> A [Jóváhagyási készletek](approval-sets.md) szolgáltatást engedélyezni kell, mielőtt használhatná a Projektjóváhagyó rendszergazda funkciót.

A **Projekt jóváhagyó rendszergazda** biztonsági szerepkör lehetővé teszi, hogy a felhasználók megkerüljék a szabályzatokat, és lehetővé teszi a bejegyzések jóváhagyását minden projektben. Ennek a szerepkörnek a hozzárendelése mellőzi az ellenőrzési logikát, amely csoporttagságot és jóváhagyóként való megjelölést igényel. Az Önhöz rendelt biztonsági szerepkörök segítségével hozzáféréssel kell rendelkeznie a megfelelő kapcsolódó táblákhoz, például a **Projekt** táblához.

A SYSTEM felhasználói környezet ugyanúgy mellőzi az biztonsági szerepkörök ellenőrzését, mint a Projektjóváhagyó rendszergazda biztonsági szerepkör.
