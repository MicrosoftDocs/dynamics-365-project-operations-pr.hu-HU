---
title: Kijavított számlák
description: Ez a témakör a kijavított számlákról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287826"
---
# <a name="corrected-invoices"></a>Kijavított számlák

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A megerősített számlák szerkeszthetők. Egy megerősített számla szerkesztésekor a kijavított számla piszkozata jön létre. Mivel a feltételezés az, hogy meg akarja fordítani az eredeti számla összes tranzakcióját és mennyiségét, ez a kijavított számla tartalmazza az eredeti számla összes tranzakcióját, és a rajta lévő teljes mennyiség 0 (nulla).

Ha bármely tranzakció nem igényel javítást, akkor eltávolíthatja azt a korrekciós számlavázlatból. Ha csak részleges mennyiséget kíván megfordítani, vagy visszatéríteni, az adatsor részleteit a Mennyiség mezőben szerkesztheti. Ha kinyitja a számlasor részleteit, láthatja az eredeti számlamennyiséget. Ezután módosíthatja az aktuális számlamennyiséget oly módon, hogy az kevesebb vagy több legyen, mint az eredeti számlamennyiség.

A korrekciós számla megerősítésekor az eredetileg számlázott tényleges értékesítés megfordul, és létrejön egy újonnan számlázott tényleges értékesítés. Ha a mennyiséget csökkentették, a különbség egy új, nem számlázott értékesítés létrehozását is eredményezi. Ha például az eredeti számlázott értékesítés nyolc órán keresztül történt, és a javított számla sorában lévő részlet hat óra, a rendszer megfordítja az eredeti számlázott értékesítési sort, és két új aktuális értéket hoz létre:

- Hat órás tényleges számlázott értékesítés.
- Nem számlázott tényleges értékesítés a fennmaradó két órára. Ezt a tranzakciót később számlázhatják, vagy pedig díjmentesnek jelölhetik, az ügyféllel folytatott tárgyalásoktól függően.


[!INCLUDE[footer-include](../includes/footer-banner.md)]