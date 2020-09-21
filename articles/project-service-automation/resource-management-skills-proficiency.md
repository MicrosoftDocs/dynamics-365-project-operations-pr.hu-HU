---
title: Készség- és jártassági modellek
description: Ez a témakör a készségek és a jártassági modellek használatáról nyújt információkat.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752302"
---
# <a name="skills-and-proficiency-models"></a>Készség- és jártassági modellek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A készségek olyan erőforrás-jellemzők, amelyek jelen vannak a Dynamics 365 Project Service Automation és ha van, a Dynamics 365 Field Service rendszerben is. 

A Project Service Automation készségeinek tárolásához menjen az **Erőforrások** \> **Erőforrás-készségek** oldalra. 

> ![Erőforrás képességei](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Használjon jártassági modelleket az erőforrások értékeléséhez

Az erőforrás-készségeket a jártassági modellek osztályozzák. Az egyes értékelések jártassági modellben vannak. 

1. Jártassági modell létrehozásához lépjen a **Erőforrások** \> **Jóléti modellek** elemre , majd válassza az **Új** lehetőséget.
2. Az új besorolási modellben adja meg a minimális besorolási értéket, a maximális besorolási értéket és az osztályozandó entitást.
3. Az **Értékelési értékek** alhálózatban meghatározhatja a különböző minősítési értékeket, a minimumtól a maximumig.

> ![Meghatározott minimális és maximális besorolás](media/Resource-Management-image85.png)

Ezek a minősítési értékek megjelennek az **Erőforrásigény**, **Ütemezési tábla** és **Ütemezési asszisztens** szűrőkön.
