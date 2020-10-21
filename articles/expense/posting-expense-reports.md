---
title: Költségjelentések közzététele
description: Ez a témakör ismerteti a költségjelentések elküldésének módját.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907411"
---
# <a name="post-expense-reports"></a>Költségjelentések közzététele

A költségjelentés jóváhagyása és a főkönyvi naplóba történő átadása után elküldhető. A költségjelentés elküldésekor a rendszer azonosítja az áfa visszaigénylésére jogosult kiadásokat. Az ÁFA-kifizetések ellenőrzésének és visszaigénylésének feladata a költségjelentés ellenőrzéséért felelős alkalmazotthoz van hozzárendelve.

Ha egy költségjelentés költségeit az alkalmazottat foglalkoztató vállalattól eltérő vállalatnak számítják felé, akkor ellenőriznie kell mind a vállalatot, amelynek a kiadásokkal tartoznak, ás a vállalatot, amely a kiadásokkal tartozik. Például a költségjelentést elküldő alkalmazott a DAT vállalatnál dolgozik, de a DIR vállalatnak számított fel egy kiadást. Ebben az esetben a DAT az a vállalat, amely a költséggel tartozik, és a DIR az a vállalat, amelynek a költséggel tartoznak. A naplósorok ellenőrzése után a költségsorokat a főkönyvbe könyvelheti.

A költségjelentés elküldéséhez a **Jóváhagyott költségjelentések** oldalon válassza ki a költségjelentést, majd a Művelet panelen válassza a **Küldés** lehetőséget.

Az összes költségjelentés egyszerre is elküldhető a listából. Jelölje ki az összes költségjelentést, majd válassza a **Küldés** lehetőséget.
