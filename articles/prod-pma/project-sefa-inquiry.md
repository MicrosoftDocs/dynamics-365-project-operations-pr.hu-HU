---
title: A szövetségi díjak kiadásaira vonatkozó lekérdezés ütemezése
description: Ez a témakör a szövetségi díjak kiadásával kapcsolatos lekérdezés ütemezésére vonatkozó információkat tartalmaz.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007239"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>A szövetségi díjak kiadásaira vonatkozó lekérdezés ütemezése

[!include [banner](../includes/banner.md)]

Az Igazgatási és Költségvetési Hivatal A-133 körlevele szerint, a szövetségi pénzösszegeket fogadó ügynökségek a könyvvizsgálati követelmények alá tartoznak, amelyeket egyedi auditnak is neveznek. A könyvvizsgálati folyamat rendszeresen beszámol a szövetségi támogatások bevételeinek és kiadásainak jelentéséről. Az egységes könyvvizsgálati jelentés egy része tartalmazza a szövetségi díjakra (SEFA) vonatkozó kiadások ütemezését.

A szövetségi díjak kiadásainak ütemezésével kapcsolatos lekérdezés a katalógus a szövetségi hazai támogatás (CFDA) címét és számát, a támogatás számát, a támogatás évét, a szövetségi ügynökség nevét, amely biztosítja az alapokat, valamint az átadó entitás nevét. A lekérdezés adott időre szól. Ez az időszak általában megegyezik a pénzügyi kimutatás időszakával, amely pénzügyi év.

A lekérdezés olyan támogatásokat is tartalmaz, amelyek leképezési dátumai a kijelölt időtartományban vannak. A **Támogató ügynökség** oszlopa mutatja a támogatási ügyfelet, vagy a továbbadott támogatás esetén a támogató ügynökséget. Továbbadott támogatás esetén az **Átadó ügynökség** oszlop mutatja a támogatott ügyfelet. Ha a támogatás nem továbbadott támogatás, az **Átadó ügynökség** oszlop üres.

## <a name="set-up-the-cfda-clusters"></a>Az CFDA-klaszter beállítása

Be kell állítania azokat a CFDA-klasztereket, amelyek a szövetségi díjak kiadásaival kapcsolatos ütemezés során CFDA-számokhoz társíthatók.

1. Lépjen a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatások \> Szövetségi belföldi támogatás katalógusa** lehetőségre.
2. CDFA-klaszter létrehozásához kattintson az **Új** lehetőségre.
3. Adja meg a klaszter nevét.
4. Válassza a **Mentés** lehetőséget a módosítások mentéséhez.

## <a name="set-up-cfda-numbers"></a>CFDA-számok beállítása

Be kell állítania azokat a CFDA-számokat, amelyek támogatásokhoz adhatók és a szövetségi díjak kiadásaival kapcsolatos ütemezés lekérdezésében szerepelnek.

1. Lépjen a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatások \> Szövetségi belföldi támogatás katalógusának számai** lehetőségre.
2. CDFA-szám létrehozásához kattintson az **Új** lehetőségre.
3. A **Szám** oszlopba írja be a CFDA-számot.
4. Nyomja le a **Tab** billentyűt.
5. A **Leírás** oszlopba írja be a CFDA-címet.
6. Nyomja le a **Tab** billentyűt.
7. Nem kötelező: a **programklaszter** mezőben adja hozzá a megfelelő CFDA-fürtöt.
8. Válassza a **Mentés** lehetőséget a módosítások mentéséhez.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>A szövetségi díjak kiadásának ütemezésére vonatkozó lekérdezés ütemezéséhez a jelentésekre vonatkozó támogatások beállítása

1. Lépjen a **Projektmenedzsment és könyvelés \> Támogatások \> Támogatások** részre és válasszon egy meglévő támogatást.
2. A **Telepítés** gyorslapon, a **Szövetségi belföldi támogatási katalógus** mezőben a CFDA-számot rendelje hozzá. A támogatás CFDA száma határozza meg a jelentéskészítéshez szükséges CFDA-fürtöt.
3. A **kapcsolatfelvételi adatok** gyorslapon adja meg a támogatóra vonatkozó információkat a következő lépések végrehajtásával:

    1. A **támogatott ügyfél** mezőben adja meg a támogatásért felelős ügyfelet. Meglévő támogatás esetén előfordulhat, hogy a rendszer ezeket az adatokat már megadta.
    2. Adja meg, hogy a támogatási ügyfél a finanszírozó-e. Ha a támogatási ügyfél a finanszírozó, akkor hagyja üresen az **átadó** jelölőnégyzetet. Ha egy másik ügyfél a finanszírozó, és a támogatási ügyfél felelős a pénz kiadásáért és nyomon követéséért, jelölje be az **átadó** jelölőnégyzetet.

4. Ha az előző lépésben bejelölte az **átadó** jelölőnégyzetet, akkor a **támogatási Ügynökség** mezőben adja meg azt az ügyfelet, aki a támogatást nyújtotta. A támogatási ügynökség és a támogatási ügyfél nem lehet azonos ügyfél.

Példa az átadói támogatásra:

A szövetségi kormány egy állam számára infrastrukturális projektet finanszírozott. A szövetségi kormány adta a pénzt, amit az állam elkölthet. Ebben az esetben a szövetségi kormány a támogató ügynökség, és az állam a támogatási ügyfél.

> [!NOTE] 
> Amikor először bekapcsolja a szolgáltatást, a rendszer a kezdeti CFDA számokat a támogatásban szereplő meglévő számok használatával adja meg.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Támogatások kizárása a SEFA-jelentésből a támogatás típusa alapján

1. Válassza a **Projektmenedzsment és könyvelés \> Beállítás \> Támogatás \> Támogatási típus** elemet.
2. Az **Alapértelmezett információ** gyorslapon jelölje be a **Szövetségi díjak kiadásainak ütemezéséből való kizárás** jelölőnégyzetet.
3. Válassza a **Mentés** lehetőséget a módosítások mentéséhez.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>A szövetségi díjak kiadásainak ütemezésére vonatkozó lekérdezés futtatása

1. Nyissa meg a **Projektkezelés és könyvelés \> Lekérdezések és jelentések \> Támogatás lekérdezése \> Szövetségi díjak kiadásainak ütemezése** pontot.
2. A **Paraméterek** szakaszban kövesse az alábbi lépéseket:

    1. A **dátumtartomány** mezőben jelölje ki a dátumtartomány kódját. Másik lehetőségként a **kezdő dátum** és a **záró dátum** mezőkben adhatja meg a dátumtartomány értékét.
    2. Nem kötelező: Ha csak a számlázott tranzakciókat kívánja bevételként szerepeltetni a lekérdezésben, akkor állítsa az **csak a számlázott bevétel felvétele** lehetőséget **Igen** értékre.

## <a name="columns"></a>Oszlopok

A szövetségi díjak kiadásainak ütemezésére vonatkozó lekérdezés a következő oszlopokat tartalmazza:

- A Szövetségi belföldi támogatás katalógusának klaszterneve
- Ttámogatási ügynökség
- Átadó ügynökség
- Támogatás neve
- Támogatási azonosító
- Támogatási pályázat azonosítója
- A Szövetségi belföldi támogatás katalógusa
- Nyugták
- Kiadások


[!INCLUDE[footer-include](../includes/footer-banner.md)]