---
title: Munkafolyamatok beállítása költségkezeléshez
description: Beállíthat olyan munkafolyamatot, amely az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására szolgál.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001024"
---
# <a name="set-up-workflows-for-expense-management"></a>Munkafolyamatok beállítása költségkezeléshez

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Beállíthat munkafolyamatot az utazásokkal és a költségekkel kapcsolatos dokumentumok ellenőrzésére és jóváhagyására. Megadhat munkafolyamatokat a költségjelentések, az utazási igénylések és a készpénzelőleg igénylései számára.

A munkafolyamat olyan üzleti folyamat, amely meghatározza, hogy egy dokumentum hogy halad át a rendszeren. A munkafolyamat azt is jelzi, hogy kinek kell elvégeznie egy feladatot, vagy jóváhagynia egy dokumentumot. A munkafolyamatok használata több okból is hasznos a szervezetek számára:

- **Egységes eljárások**: Meghatározható bizonyos dokumentumok (például a beszerzési igénylések vagy a költségelszámolások) jóváhagyási folyamata. A munkafolyamatokkal biztosítható, hogy a dokumentumok feldolgozása és jóváhagyása egységes és hatékony legyen.
- **Folyamat láthatósága**: Nyomon követheti egy adott munkafolyamat-példány állapotát, előzményeit és teljesítménymutatóit. Így meghatározhatja, hogy szükség van-e a munkafolyamat hatékonyabbá tételére.
- **Központosított munkavégzési lista**: A felhasználók megtekinthetik a központosított munkavégzési listákat, és láthatják a hozzájuk rendelt munkafolyamat-feladatokat és jóváhagyásokat. 

## <a name="workflow-types"></a>Munkafolyamatok típusai

Az alábbi táblázat a **Költségkezelés** részen létrehozható munkafolyamatok típusait ismerteti.


|              <strong>Típus</strong>              |                   <strong>A típus használata</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Költségjelentés automatikus jóváhagyása</strong> |            Jóváhagyási munkafolyamatok létrehozása költségjelentésekhez.             |
|  <strong>Költségjelentés automatikus közzététele</strong>   |        Automatikus közzétételi munkafolyamatok létrehozása költségjelentésekhez.        |
|       <strong>Költségsorelem</strong>        |     Jóváhagyási munkafolyamatok létrehozása a költségjelentések sorelemeihez.      |
| <strong>Költségsorelem automatikus közzététele</strong> | Automatikus közzétételi munkafolyamatok létrehozása a költségjelentések sorelemeihez. |
|       <strong>Utazási kérelem</strong>       |          Jóváhagyási munkafolyamatok létrehozása utazási kérelmekhez.           |
|      <strong>Készpénzelőleg kérése</strong>      |         Jóváhagyási munkafolyamatok létrehozása készpénzelőleg kéréséhez.          |
|        <strong>ÁFA-visszaigénylés</strong>        | Jóváhagyási munkafolyamatok létrehozása ÁFA visszaigényléséhez.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]