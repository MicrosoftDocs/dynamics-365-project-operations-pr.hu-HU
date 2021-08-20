---
title: Projektalapú szerződéssorok használata
description: Ez a témakör információkat nyújt a projektalapú szerződéssorokról.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990049"
---
# <a name="work-with-projectbased-contract-lines"></a>Projektalapú szerződéssorok használata

A Dynamics 365 Project Operations szerződéssorai úgy vannak kialakítva, hogy tárolják a becsléseket és számlázási megállapodásokat a projektmunka adott komponenseire egy aktivitásban. A projektalapú szerződéssorok felépítése a projektek becsült és számlázási helyzetére vonatkozóan a következő fogalmakkal bővül:

- Számlázási mód
- Projekt és feladatleképezés
- Szerepeltetett tranzakciós osztályok
- Nem meghaladandó korlát
- Felszámíthatósági beállítás
- Becslések a szerződéssorok részleteinek használatával
- Szerződéssor ügyfelei

A következő mezők a projektalapú szerződéssorok **Általános** lapján találhatók. Ezek a mezők elősegítik a részletes, alapszintű becslések és a számlázási intézkedése alapjainak beállítását a projektlapú munkához.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| **Név** | A szerződéssor neve, amely azonosítja a becsült szerződés különálló összetevőjét. Az árajánlatból létrehozott projekt-szerződések esetén a program a projekt alapú árajánlati sor kapcsolódó értékéből másolja át az értéket. | A számla létrehozásakor ez a mezőérték át lesz másolva a projekt számlasorra, amelye ebből a szerződéssorból lesz létrehozva. |
| **Számlázási mód** | Az árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. Ez egy értékkészlet, amely a Project Operations által támogatott két fő szerződőmodellt képviseli:</br>- **Rögzített ár**</br>- **Idő és anyag** | A hivatkozott szerződéssor számlázási módja alapján a rendszer feldolgozza a tényleges tranzakciót. Ha a tényadat által hivatkozottszerződéssor idő-és anyagelszámolású számlázási módot tartalmaz, akkor a rendszer létrehozza a költség és a nem számlázott tényleges értékesítések rekordját. Ha a tényadat által hivatkozott szerződéssor rögzített árú számlázási móddal rendelkezik, akkor csak egy tényleges költség jön létre. |
| **Project** | Ezzel a mezővel azonosíthatja azt a projektet, amelyet az adott aktivitással kapcsolatos munkára fog használni. | Ennek a mezőnek az értéket a program a **Hozzáadott feladatok** és **Hozzáadott tranzakcióosztályok** mezőkkel együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon. |
| **Idővel együtt** | A jelölő jelzi, hogy a kiválasztott projekthez tartozó időtranzakciók vagy munkaköltségek szerepelnek-e ebben a szerződéssorban. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó időtranzakciók vagy munkaköltségek nem fognak szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fognak. | Ezt a mezőértéket a program a projekttel együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon. |
| **Költséggel együtt** | A jelölő jelzi, hogy a kiválasztott projekthez tartozó önköltség szerepelni fog ebben a szerződéssorban. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó önköltség nem fog szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fog. | Ezt a mezőértéket a program a projekttel együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon. |
| **Díjjal együtt** | A jelölő jelzi, hogy a kiválasztott projekthez tartozó díjak szerepelni fognak ebben a szerződéssorban. A **Nem** érték azt jelzi, hogy a kiválasztott projekthez tartozó díjak nem fognak szerepelni ebben a szerződéssorban. Az **Igen** érték azt jelzi, hogy fognak. | Ezt a mezőértéket a program a projekttel együtt használja, hogy feloldja a szerződéssor hivatkozását egy tényadaton vagy egy becsléssor-rekordon. |
| **Szerződésben rögzített összeg** | Rögzített árú szerződéssor esetén ez egy megállapodott érték, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz. Idő és anyag szerződéssor esetén ez az összeg becsült érték arra vonatkozóan, ami számlázva lesz az ügyfélnek a szerződéssorhoz társított összes munkaösszetevőhöz. Árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő összegből összegzi. | Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő összegek módosításával. Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövek után fizetendő összeg generálására szolgál. |
| **Becsült adó** | A felhasználó módosíthatja ezt a mezőt, hogy a szerződéssor összegére vonatkozóan megadja a becsült adót. Ha egy projektalapú szerződéssor sorrészleteket tartalmaz, akkor a mező szerkesztésre zárolva van, és a program a szerződéssor részleteiben szereplő adóösszegből összegzi. | Ha a szerződéssorhoz tartoznak sorrészletek, akkor ez az érték módosítható a sor részleteiben szereplő adóösszegek módosításával. Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adózás előtti összeg generálására szolgál. |
| **Szerződésben rögzített összeg adózás után** | A szerződéssor összege adózás után. Ez a mező csak olvasható, és számítása a következő: **Szerződött összeg + adó**. | Rögzített árú szerződéssor esetén ez az érték a periodikus számlázási mérföldkövekhez kapcsolódó adó generálására szolgál. |
| **Nem meghaladandó korlát** | A felhasználó szerkesztheti ezt a mezőt, és csak olyan projektalapú szerződéssorok esetén érhető el, amelyek számlázási módja idő és anyag. | A felhasználó szerkesztheti ezt a mezőt. Ha egy időhöz vagy kiadáshoz tartozó tényadat erre a szerződéssorra hivatkozik, akkor tényadathoz tartozó összeg össze lesz vetve a szerződéssor nem túlléphető határértékével, miután figyelembe lettek véve a már elköltött és lekötött összegek. |
| **Ügyfél költségvetése** | Ez a mező szerkeszthető, és árajánlatból létrehozott projekt-szerződésben a program a az ajánlatsor kapcsolódó mezőjéből másolja át az értéket. | Ez a mező csak tájékoztatásra szolgál, és nincs későbbi jelentősége. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>A Projektalapú szerződéssorok Általános lapjának beállításaira vonatkozó ellenőrzési szabály

Szabály: Egy projekt és egy adott tranzakciós osztály csak egy projektalapú szerződéssor része lehet a szerződésben.

| Szerződés | Szerződéssor | Project | Idővel együtt | Költséggel együtt | Díjjal együtt | Érvényes/nem érvényes | Ok                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | I1      | Igen          | Igen             | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje díjai és költségei a CL1 és CL2 szerződéssorokon is szerepelnek.                                                                                       |
| C1       | CL2           | I1      | Igen          | Igen             | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje díjai és költségei a CL1 és CL2 szerződéssorokon is szerepelnek.                                                                                       |
| C1       | CL1           | I1      | Igen          | Nincs              | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje és díjai a CL1 és CL2 szerződéssorokon is szerepelnek.                                                                                                   |
| C1       | CL2           | I1      | Igen          | Igen             | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje és díjai a CL1 és CL2 szerződéssorokon is szerepelnek.                                                                                                   |
| C1       | CL1           | I1      | Igen          | Nincs              | Igen         | Érvényes           | A P1 projektre vonatkozó idő és a díjak a CL1 sorban szerepelnek. A P1 projektre vonatkozó költséget a CS2 tartalmazza. </br>   Az egyes szerződéssorok tartalma között nincs átfedés, ezért érvényes.  |
| C1       | CL2           | I1      | Nincs           | Igen             | Nincs          | Érvényes           | A P1 projektre vonatkozó idő és a díjak a CL1 sorban szerepelnek. A P1 projektre vonatkozó költséget a CS2 tartalmazza. </br>   Az egyes szerződéssorok tartalma között nincs átfedés, ezért érvényes.  |
| C1       | CL1           | I1      | Igen          | Igen             | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje díjai és költségei mindkét szerződés sorain szerepelnek.                                                                                               |
| CL2      | CL2           | I1      | Igen          | Igen             | Igen         | Nem érvényes       | Megsérti a szabályt. A P1 projekt ideje díjai és költségei mindkét szerződés sorain szerepelnek.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]