---
title: Költségjelentések közzététele
description: Ez a cikk a költségjelentések feladását ismerteti.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524872"
---
# <a name="post-expense-reports"></a>Költségjelentések közzététele

A költségjelentés jóváhagyása és a főkönyvi naplóba történő átadása után elküldhető. A költségjelentés elküldésekor a rendszer azonosítja az áfa visszaigénylésére jogosult kiadásokat. Az ÁFA-kifizetések ellenőrzésének és visszaigénylésének feladata a költségjelentés ellenőrzéséért felelős alkalmazotthoz van hozzárendelve.

Ha egy költségjelentés költségeit az alkalmazottat foglalkoztató vállalattól eltérő vállalatnak számítják felé, akkor ellenőriznie kell mind a vállalatot, amelynek a kiadásokkal tartoznak, ás a vállalatot, amely a kiadásokkal tartozik. Például a költségjelentést elküldő alkalmazott a DAT vállalatnál dolgozik, de a DIR vállalatnak számított fel egy kiadást. Ebben az esetben a DAT az a vállalat, amely a költséggel tartozik, és a DIR az a vállalat, amelynek a költséggel tartoznak. A naplósorok ellenőrzése után a költségsorokat a főkönyvbe könyvelheti.

A költségjelentés elküldéséhez a **Jóváhagyott költségjelentések** oldalon válassza ki a költségjelentést, majd a Művelet panelen válassza a **Küldés** lehetőséget.

Az összes költségjelentés egyszerre is elküldhető a listából. Jelölje ki az összes költségjelentést, majd válassza a **Küldés** lehetőséget.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>A Költségkötelezettség szállítói pénznemben történő feladásának engedélyezése készpénzes fizetési mód esetén funkció engedélyezése

A **Költségkötelezettség szállítói pénznemben történő feladásának lehetősége készpénzfizetési mód** esetén funkció lehetővé teszi a költségjelentések feladását a szállító pénznemében a készpénzes fizetési módhoz.

Jelenleg a készpénzköltségek benyújtásakor a költségjelentések a könyvelési pénznemben kerülnek feladásra. A tranzakció pénzneme, a könyvelési pénznem és a szállító pénzneme közötti összegátváltás miatt a rendszer helytelen összeget fizet ki a szállítóknak, ha a ráfordítás tranzakciós dátuma és a tényleges fizetési dátum eltérő átváltási árfolyammal rendelkezik.

Ez a funkció biztosítja, hogy a szállítói egyenleg a szállító pénznemében legyen rögzítve a költségjelentés feladásakor.

1. Válassza a **Munkaterületek** \> **Szolgáltatáskezelés** lehetőséget.
2. A listában keresse meg és válassza a **Képesség költségkötelezettség feladására szállítói pénznemben a készpénzes fizetési módhoz** lehetőséget, majd válassza az Engedélyezés most **lehetőséget**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
