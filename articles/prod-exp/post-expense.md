---
title: Költségjelentés közzététele
description: Ez a témakör ismerteti, hogyan lehet költségjelentést könyvelni a főkönyvbe.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36be76c0c9f25cb93921acee36a820e276cad625
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271311"
---
# <a name="post-an-expense-report"></a>Költségjelentés közzététele

A költségjelentés jóváhagyása és a főkönyvi naplóba történő átadása után elküldhető a főkönyvbe. A költségjelentés elküldésekor a rendszer azonosítja az áfa visszaigénylésére jogosult kiadásokat. Az ÁFA-kifizetések ellenőrzésének és visszaigénylésének feladata a költségjelentés ellenőrzéséért felelős alkalmazotthoz van hozzárendelve.

Ha egy költségjelentés költségeit az alkalmazottat foglalkoztató vállalattól eltérő vállalatnak számítják felé, akkor ellenőriznie kell mind a vállalatot, amelynek a kiadásokkal tartoznak, és a vállalatot, amely a kiadásokkal tartozik. Például a költségjelentést elküldő alkalmazott a DAT vállalatnál dolgozik, de a DIR vállalatnak számított fel egy kiadást. Ebben az esetben a DAT az a vállalat, amely a költséggel tartozik, és a DIR az a vállalat, amelynek a költséggel tartoznak. A naplósorok ellenőrzése után a költségsorokat a főkönyvbe könyvelheti.

A költségjelentés elküldéséhez a **Jóváhagyott költségjelentések** oldalon válassza ki a költségjelentést, majd a Művelet panelen válassza a **Küldés** lehetőséget.

Az összes költségjelentés egyszerre is elküldhető a listából. Jelölje ki az összes költségjelentést, majd válassza a **Küldés** lehetőséget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]