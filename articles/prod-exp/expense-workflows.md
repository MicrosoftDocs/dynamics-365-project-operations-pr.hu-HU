---
title: Költségkezelési munkafolyamatok beállítása
description: Beállíthat munkafolyamatot az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271626"
---
# <a name="set-up-expense-management-workflows"></a>Költségkezelési munkafolyamatok beállítása

Beállíthat olyan munkafolyamatot, amely az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására szolgál. A dokumentumok, amelyekhez definiálhatók munkafolyamatok a költségjelentések, az utazási igénylések és a készpénzelőleg igénylések.

A munkafolyamatok egy üzleti folyamatnak felelnek meg. Meghatározza, hogyan halad a dokumentum a rendszeren keresztül, és jelzi, hogy kinek kell elvégeznie a feladatot, vagy jóváhagynia a dokumentumot. A munkafolyamatok használata több okból is hasznos a szervezetek számára:

-   **Egységes eljárások** – Meghatározható bizonyos dokumentumok (például a beszerzési igénylések vagy a költségelszámolások) jóváhagyási folyamata. A munkafolyamatokkal biztosítható, hogy a dokumentumok feldolgozása és jóváhagyása egységes és hatékony legyen.

-   Folyamat láthatósága – Nyomon követheti egy adott munkafolyamat-példány állapotát, előzményeit és teljesítménymutatóit. Így meghatározhatja, hogy szükség van-e a munkafolyamat hatékonyabbá tételére.

-   Központosított munkavégzési lista – A felhasználók megtekinthetik a központosított munkavégzési listákat, és láthatják a hozzájuk rendelt munkafolyamat-feladatokat és jóváhagyásokat. 

**A létrehozható munkafolyamatok**

Az alábbi táblázat a **Költség** részen létrehozható munkafolyamatok típusait ismerteti.


|              <strong>Típus</strong>              |                   <strong>A típus használata</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Költségjelentés</strong>         |            Jóváhagyási munkafolyamatok létrehozása költségjelentésekhez.             |
|  <strong>Költségjelentés automatikus közzététele</strong>   |        Automatikus közzétételi munkafolyamatok létrehozása költségjelentésekhez.        |
|       <strong>Költségsorelem</strong>        |     Jóváhagyási munkafolyamatok létrehozása a költségjelentések sorelemeihez.      |
| <strong>Költségsorelem automatikus közzététele</strong> | Automatikus közzétételi munkafolyamatok létrehozása a költségjelentések sorelemeihez. |
|       <strong>Utazási kérelem</strong>       |          Jóváhagyási munkafolyamatok létrehozása utazási kérelmekhez.           |
|      <strong>Készpénzelőleg kérése</strong>      |         Jóváhagyási munkafolyamatok létrehozása készpénzelőleg kéréséhez.          |
|        <strong>ÁFA-visszaigénylés</strong>        | Jóváhagyási munkafolyamatok létrehozása ÁFA visszaigényléséhez.  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]