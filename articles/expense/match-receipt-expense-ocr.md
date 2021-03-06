---
title: Nyugta párosítása költséggel OCR használatával
description: Ez a témakör a nyugták optikai karakterfelismeréssel (OCR) való feldolgozásáról nyújt információkat.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897004"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Nyugta párosítása költséggel OCR használatával

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A költségbejegyzést továbbfejlesztettük a nyugták optikai karakterfelismeréssel (OCR) való feldolgozási funkciójának bevezetésével. Ez a funkció egyszerűbbé teszi a költségjelentések létrehozását.

## <a name="key-features"></a>Legfontosabb funkciók

- A rendszer kinyeri a kereskedő nevét, a dátumot, valamint a nyugtákon lévő teljes összeget.
- Ezenkívül megpróbálja megfeleltetni a nem csatolt nyugtákat és a nem csatolt költségtranzakciókat.
- A nyugtákból hozhatók létre manuálisan megadott költségtranzakciók.

## <a name="attach-receipts-to-an-expense-report"></a>Nyugták csatolása költségjelentéshez

Ha a költségjelentések létrehozásakor automatikusan csatolni szeretné az olyan nyugtákat, amelyeken szerepelnek a hitelkártya-tranzakciók, hajtsa végre az alábbi lépéseket.

  1. Nyissa meg a **Költségkezelés** munkaterületet.
  2. A **Nyugták** lapon ellenőrizze, hogy vannak-e nem csatolt nyugták. A nyugtákat a **Nyugták** lapon fel is töltheti.
  3. A **Költségek** lapon ellenőrizze, hogy vannak-e nem csatolt költségek. A költségadminisztrátorok általában a hitelkártya-szolgáltatótól importálják ezeket a költségeket.
  4. Válassza az **Új Költségjelentés** lehetőséget. Vegye figyelembe, hogy már a költségek és a nyugták is megadhatók a költségjelentés létrehozásakor. Ha a költségeket és a nyugtákat egyaránt hozzáadja, a rendszer automatikusan egyezteti a nyugtákat a kiadásokkal.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Nyugták létrehozása és egyeztetése költségjelentéshez
Ha költséget szeretne létrehozni, vagy költséget szeretne egyeztetni egy nyugtáról, hajtsa végre az alábbi lépéseket.

  1. A költségjelentés **Nyugták** lapján csatoljon egy nyugtát a **Nyugták hozzáadása** lehetőséggel.
  2. A nyugta feltöltött képe alapján találja a **Létrehozás** és az **Egyeztetés** elemet.

      - A **Létrehozás** lehetőséggel manuálisan megadott költségtranzakciót hozhat létre, amelyet kitölthet a nyugtáról kinyert értékekkel.
      - Az **Egyeztetés** lehetőség használata esetén a rendszer egy meglévő költséget próbál egyeztetni a nyugtával.

## <a name="installation"></a>Telepítés

A költségek ilyen speciális funkcióinak használatához telepíteni kell a Költségkezelési szolgáltatás bővítményt a Microsoft Dynamics 365 Finance rendszerhez, és be kell kapcsolni a funkciókat a példányban. A bővítményt a projektből, a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból érheti el.

1. Jelentkezzen be az LCS rendszerbe, és nyissa meg a kívánt környezetet.
2. Válassza a **Minden részlet** lehetőséget.
3. Válassza a **Karbantartás** lehetőséget, vagy görgessen le a **Környezeti bővítmények** gyorslaphoz.
4. Válassza az **Új bővítmény telepítése** lehetőséget.
5. Válassza a **Költségkezelési szolgáltatás** lehetőséget.
6. Kövesse a telepítési útmutatót, és fogadja el a használati feltételeket.
7. Válassza a **Telepítés** lehetőséget.

A **Szolgáltatások kezelése** munkaterületen kapcsolja be a következő szolgáltatásokat:

- Költségjelentések újragondolva
- Automatikus egyeztetés és költség létrehozása nyugtából

Amikor bekapcsolja ezeket a funkciókat, a következő műveleteket hajtja végre a rendszer:

- A meglévő **Költségkezelés** munkaterület az új munkaterületre cserélődik.
- A rendszer új, a költség mező láthatóságával kapcsolatos menüelemet vesz fel.
- A korábbi **Költségjelentés** lapot továbbra is megnyithatja a **Költségkezelés > Saját kiadások > Költségjelentések** beállítással.
- A munkafolyamatok és a jóváhagyások továbbra is a meglévő költségjelentési oldalra irányítják át.
- A nyugtákat a rendszer a Microsoft Azure Cognitive Services szolgáltatáson keresztül dolgozza fel; a metaadatokat kinyeri és hozzáadja.
- A rendszer hozzáad egy olyan beállítást, amellyel a megfeleltetett, nem csatolt nyugtákat tartalmazó költségjelentések hozhatók létre.
- A rendszer hozzáad egy olyan beállítást a költségjelentésekhez, amellyel költségsor készíthető egy nyugtából, illetve amellyel megpróbálható a meglévő nyugták és költségsorok egyeztetése.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

**Használja a Microsoft az adataimat a modelljeihez?**

Nem, a Microsoft általános gépi tanulás modellt készített a nyugtákat feldolgozó szolgáltatásához. Ez a modell nem a feltöltött nyugtákon alapul.

**Hol érhető el és hol kerül feldolgozásra a szolgáltatás?**

Jelenleg az Egyesült Államokban támogatott.

**Hová kerülnek a nyugtáim?**

A Finance a Cognitive Services használatával nyeri ki a mezők adatait. A Cognitive Services legfeljebb 24 óráig, a feldolgozáshoz őrzi meg a nyugták másolatát. A feldolgozás befejezése után a Cognitive Services eltávolítja a nyugtát. A Finance továbbra is tárolja majd a nyugtákat.

További információ: [A nyugták Form Recognizer új funkciójával történő felismerésének engedélyezése](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
