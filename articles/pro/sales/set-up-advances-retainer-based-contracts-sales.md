---
title: Foglalón alapuló szerződések beállítása – Lite
description: Ez a témakör a Project Operationsban szereplő foglaló alapú szerződési modellek és előlegek információit tartalmazza.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180870"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Foglalón alapuló szerződések beállítása – Lite


_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations támogatja a foglaló alapú szerződéseket. A foglaló alapú szerződés olyan egyenlően elosztott kifizetések tárgyalt csoportja, amelyért az ügyfélnek számláznak a projekt időtartama alatt. Az ilyen típusú szerződéseket általában idő-és anyagelszámolású, illetve fogyasztási alapú számlázási modellekhez használatosak, ahol meg kell adni az ügyfélnek az előrejelezhető számlát és a fizetési ütemezést. Az egyes időszakokban elhatárolt tényleges bevételeket az időszak elején egyeztetik az ügyféltől kapott fizetéssel. Az idő-és anyagelszámolású számlázási modell fogalmával összhangban az egyes időszakok során elhatárolt bevételi értékek a felmerült költségektől függően változhatnak. Ha az elhatárolt bevétel nagyobb, mint az időszak elején kapott összeg, a projektvégrehajtó vállalat a következőket teheti:

- Csak a többletet számlázza az ügyfélnek 
- A bevétel egyeztetését elhalasztja a következő számlázási időszakra, és a projekt végén egy utolsó számlát kell létrehozni a többi nem egyeztetett bevételre vonatkozóan.

A foglaló alapú és a rögzített árú szerződéses modell közötti fő különbség a Project Operationsban az, hogy a rögzített árú szerződés modellben a számla összege nem kapcsolódik össze, illetve nem kötik össze a felmerült költségekhez. A számlázás mérföldkőn alapuló megközelítést követ, amely összhangban van az adott időszakra vonatkozóan felmerült költségekkel. A foglaló alapú szerződésekben a számlázható bevételeket a program a szerződéssor számlázási módja alapján rögzíti. Amikor a számlázási módszer idő és anyagelszámolás, a számlázott bevétel az adott időszakban felmerült költségekhez kötődik, és időszakról időszakra változhat. Az ügyfélnek azonban csak az időszakos foglaló összegét számlázzák. A rendszer egy másik számlát használ az időszak végén, hogy összehangolja az időszak során rögzített számlázható bevételt azzal az összeggel, amelyet az ügyfélnek az időszak kezdetén számláztak.

Ennek a módszernek az az előnye, hogy az ügyfél költségei a foglaló ütemezésében előrejelezhetők lesznek a tipikus idő-és anyagelszámolású modellektől eltérően. A projektet végrehajtó szervezetnek is van egy kis tere a kockázat fedezésére, hogy a hatókör növekedése miatt felmerült költségeket fedezze, amit a rögzített árú modell nem engedte volna meg.

Az időszakos foglaló alapú ütemezés mellett a Project Operations egyszeri előleget rögzíthet az ügyféltől, és összeegyeztetheti a különböző projektköltség-összetevőkkel.

A Project Operations foglalója nem használható fel, amíg nem számlázták ki az ügyfélnek. Ezt az alábbi mezők jelzik a részrácson az előlegek és a foglalók számára.

| Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
| --- | --- | --- |
| Rendelkezésre álló összeg | A foglaló vagy az előleg rekordján elérhető, használható összeg. | Amíg az előleget vagy a foglalót nem számlázzák, nem használható, azaz az elérhető összeg nulla lesz. |
| Felhasznált mennyiség | A foglaló vagy az előleg rekordján már felhasznált összeg. | Az előleg vagy a foglaló részben egyeztethető a számlán a tényleges költséggel, és részben megjelölhető már felhasznált vagy elfogyasztott típusúként. Az előleg vagy a foglaló további összege elérhető a jövőbeli, tényleges költségekkel rendelkező számlák egyeztetésére. |