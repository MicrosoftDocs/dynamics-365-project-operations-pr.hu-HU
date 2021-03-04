---
title: Nem meghaladandó állapot és ellenőrzések kezelése
description: Ez a témakör információt nyújt a Project Operationsban végrehajtott nem meghaladandó korlát ellenőrzéseiről.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129996"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Nem meghaladandó állapot és ellenőrzések kezelése 

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

## <a name="not-to-exceed-on-approvals"></a>Nem meghaladható jóváhagyáskor

Egy idő- vagy költségbejegyzés elküldése esetén a rendszer jóváhagyási rekordot hoz létre. Ha a jóváhagyás számlázható, és egy idő- és anyagelszámolású szerződéssorhoz van leképezve, a rendszer a következő szinteken teljesíti a nem-túllépési érvényesítési ellenőrzést:

  - Az ügyfélre vonatkozóan beállított korlát ellenőrzése a projektszerződéssoron
  - A beállított korlát ellenőrzése a szerződéssoron
  - A beállított korlát ellenőrzése az ügyfélre vonatkozóan
  - A beállított korlát ellenőrzése a szerződésen

Az egyes szinteken végzett ellenőrzésekkel biztosítható, hogy az ebben a jóváhagyásban szereplő értékesítési érték ne sértse meg az adott szinten a már rögzített számlázási visszamaradt összeg elszámolását követően a nem meghaladandó korlátot, valamint az adott szinten számlázott összeget.

Ha az ellenőrzés megfelel, a jóváhagyáshoz a rendszer **Sikerült** ellenőrzési állapotot ad.

Ha az ellenőrzés nem felel meg, a jóváhagyáshoz a rendszer **Sikertelen** ellenőrzési állapotot ad. A meg nem haladandó ellenőrzési részletek tájékoztatják a felhasználót, hogy melyik szinten hiúsult meg az ellenőrzés.

Ha az elküldött idő- vagy költségbejegyzés nem számlázhatónak számít, a nem meghaladandó ellenőrzési állapot beállítása **Nem érvényes**, ahol az ellenőrzési részlet egyenlő a **Nem érvényes** értékkel.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nem meghaladandó érték a nem számlázott értékesítési tényadatokon

Amikor egy idő- vagy Költségbejegyzés jóvá van hagyva, a költség és a nem számlázott értékesítések tényadatrekordjai létrejönnek. Ha a létrehozott nem számlázott értékesítési tényadat számlázható, és egy idő- és anyagelszámolású szerződéssorhoz van leképezve, az alkalmazás a következő szinteken teljesíti a nem-túllépési érvényesítési ellenőrzést:

  - Az ügyfélre vonatkozóan beállított korlát ellenőrzése a projektszerződéssoron
  - A beállított korlát ellenőrzése a szerződéssoron
  - A beállított korlát ellenőrzése az ügyfélre vonatkozóan
  - A beállított korlát ellenőrzése a szerződésen

Az egyes szinteken végzett ellenőrzésekkel biztosítható, hogy a tényadaton szereplő értékesítési érték ne sértse meg az adott szinten a már rögzített számlázási visszamaradt összeg elszámolását követően a nem meghaladandó korlátot, valamint az adott szinten számlázott összeget.

Ha az ellenőrzés megfelel, a nem számlázott értékesítési tényadathoz a rendszer **Véglegesítve** nem meghaladandó állapotot ad.

Ha az ellenőrzés sikertelen, a nem számlázott értékesítések tényleges értéke nem haladhatja meg a **sikertelen** nem meghaladandó állapotot. Az ellenőrzési részletek tájékoztatják a felhasználót, hogy melyik szinten hiúsult meg az ellenőrzés.

Amikor a nem számlázott értékesítési tényadat nem számlázható vagy ingyenes, ha nincs nem meghaladandó korlát beállítva a négy szint egyikén sem, vagy ha a létrehozni kívánt tényadat Költség, Foglaló, Erőforrás-kezelő részleg vagy Szervezetközi értékesítés típusú, a **Nem meghaladandó állapot** és a **Nem meghaladandó ellenőrzési adat** mezők értékének **Nem érvényes** értéknek kell lennie.

## <a name="reset-the-not-to-exceed-status"></a>Nem meghaladandó állapot alaphelyzetbe állítása

A nem meghaladandó állapot tömeges visszaállítását is végrehajthatja. Ez lehetővé teszi, hogy a projektmenedzserek úgy állítsák be a nem meghaladandó ellenőrzést, hogy egy adott munka, idő vagy költségtípus számlázását priorizálják másokkal szemben, amelyeket már vállaltak a rendelkezésre álló nem meghaladandó összegből.

A nem meghaladó állapotra vonatkozó alaphelyzetbe állítás után a rendszer csökkenti a vállalt összeget. A projektmenedzser kiválaszthat egy másik munkafolyamatot, időpontot vagy költséget, amely korábban meghiúsult a nem meghaladandó ellenőrzésen, és újraértékelheti őket. A vállalt összeg csökkentésével ezek a tényadatok most már megfelelnek az érvényesítésen. Ez segíti a projektmenedzsert abban, hogy nagyobb befolyással és irányítással rendelkezzen az adott időszakra vonatkozó számlázható tranzakciók felett.

A nem meghaladandó állapot visszaállításához jelöljön ki egy vagy több tényleges értéket az **Idő- és anyagszámlázási hátralék** vagy a **Tényleges adatok** nézetből, majd válassza a **Nem meghaladandó állapot alaphelyzetbe állítása** elemet.

A nem meghaladandó állapotot a rendszer alaphelyzetbe állítja **Nincs értékelve** állapotra az összes releváns kiválasztott tényadaton. Azok a tényadatok, amelyeknek alaphelyzetbe állították a nem meghaladandó állapotát, olyan nem számlázott értékesítési tényadatok, amelyeket még nem számláztak, nem szerepelnek piszkozat állapotú számlán, és számlázhatóként vannak megjelölve. A program figyelmen kívül hagyja a többi kijelölt tényadatot.

## <a name="reevaluate-not-to-exceed-status"></a>Nem meghaladandó állapot újbóli értékelése

A nem meghaladandó állapot tömeges újraértékelését is elvégezheti. A nem meghaladandó állapot újraértékelése akkor lehet hasznos, ha:

  - A nem meghaladandó korláttal kapcsolatban ügyféllel folytatott újratárgyalás történt, és a tényadatokat át kell értékelni.
  - A projektmenedzser azt szeretné, hogy a nem számlázott értékesítési hátralékok számlázását egyik munkavégzés másik munkavégzés feletti priorizálásával finomhangolná.

A nem meghaladandó állapot újraértékeléséhez jelöljön ki egy vagy több tényleges értéket az **Idő- és anyagszámlázási hátralék** vagy a **Tényleges adatok** nézetből, majd válassza a **Nem meghaladandó állapot újraértékelés** elemet.

A rendszer az összes releváns, nem meghaladandó korláttal rendelkező kijelölt tényleges értéket értékeli a nem meghaladandó korlát beállításához viszonyítva. Azok a tényadatok, amelyek számára releváns a nem meghaladandó állapot újraértékelése, olyan nem számlázott értékesítési tényadatok, amelyeket nem számláztak, nem szerepelnek piszkozat állapotú számlán, és számlázhatóként vannak megjelölve. A többi kijelölt tényleges érték kijelölése.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]