---
title: A futásteljesítmény beállítása futásteljesítmény-szintek használatával
description: A témakör a futásteljesítménnyel és futásteljesítmény-szintekkel kapcsolatosan tartalmaz információkat.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083674"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>A futásteljesítmény beállítása futásteljesítmény-szintek használatával

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A költség jelentése esetén, amennyiben a kiválasztott költségkategória a **Futásteljesítmény**, az adott költségsorra vonatkozó összege a *futásteljesítmény költsége* mennyiséggel van kiszámítva. Ezt az összeget meghatározott futásteljesítmény-szintek használatával, illetve amennyiben nincsenek beállított futásteljesítmény-szintek, akkor a futásteljesítmény normál díja határozza meg. 

A futásteljesítmény-szintek a **Költségkezelés** > **Beállítás** > **Általános** > **Költségkategóriák** > **Futásteljesítmény** > **Kategóriabeállítás** helyen állíthatók be.

A 10.0.18-as verzióra való frissítés után, ha a szervezet a futásteljesítmény költségkategóriát használja, érdemes megfontolni a futásteljesítmény funkció engedélyezését az alábbi tervezési változtatások áttekintése után. 

A futásteljesítmény-szintek új kialakítása hatással van a **Mennyiség** mező értékének feldolgozására. A 10.0.18-as verzió megjelenése előtt a **Mennyiség** mezőben szereplő érték volt az alsó korlát. Ha az összegyűlés átlépte ezt az értéket, az annak megfelelő árfolyamot használta a rendszer.  10.0.18-tól a **Mennyiség** mező értéke a felső korlátnak számít. A ennek megfelelő arányt akkor használja a rendszer, ha a kilométer-futásteljesítmény kisebb a **Mennyiség** mezőben szereplő értéknél.  A futásteljesítmény-szintek új modellje segíti a futásteljesítmény-szintek egységes voltát és a jobb használhatóságot.   

A jóváhagyott költségjelentéseket a rendszer újraszámoláskor az új kialakításnak megfelelően számítja újra.

## <a name="example"></a>Példa
 
### <a name="before-version-10018"></a>A 10.0.18-as verzió előtt
Két futásteljesítmény-szint esetén az egyes szintek **Mennyiség** mezője az alacsonyabb futásteljesítmény-korlátnak megfelelő. Jelenleg az első szint érték (0) és az aránya 0,45 az értéke, a második értéke 1000, illetve az aránya 0,25. Ha a összegyűjtött kilométerek vagy mérföldek a mezőben megadott értéket átlépik, akkor a program a kapcsolódó arányt használja. Ha nincs nulla mennyiséggel megadva sor, akkor a rendszer a költségkezelésben megadott futásteljesítményt használja. 
 
Ha egy alkalmazott 1500 mérfölddel küld be költségjelentést, akkor a közzétett költségjelentés két futásteljesítmény-sora a következő lehet: 1000 (0,45-ös arány) + 500 (0,25-ös arány) = 575,00.

### <a name="after-version-10018"></a>A 10.0.18-as verzió után
A 10.0.18-as verzióban a **Mennyiség** mezőben az egyes szintek a szint felső korlátját jelentik. Jelenleg az első szint értéke 999 és az aránya 0,45, a második értéke 999 999 999,00, illetve az aránya 0,25. Ha a összegyűjtött kilométerek vagy mérföldek a **Mennyiség** mezőben megadott értéket átlépik, akkor a program a kapcsolódó arányt használja. Ha az összes felső határ túl lett lépve, akkor a rendszer a költségkezelésben megadott futásteljesítményt használja. 
 
Ugyanezen forgatókönyv helyes kiszámításához módosítani kell a beállított szintet. Az első szint **Mennyiség** mezőjének értéke 999,00, a másodikban pedig 999 999 999,00 az érték. Ha egy alkalmazott meghaladja az első szintben található kilométerek vagy mérföldek teljes mennyiséget , a rendszer a költségkezelésben megadott futásteljesítmény-arányt használja. 
  
Ha egy alkalmazott 1500 mérfölddel küld be költségjelentést, akkor a közzétett költségjelentés két futásteljesítmény-sora a következő lehet: 1000 (0,45-ös arány) + 500 (0,25-ös arány) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>A futásteljesítmény összeg kiszámításának engedélyezése több futásteljesítmény-szinthez azonos aránnyal funkció

A **Futásteljesítmény összeg kiszámításának engedélyezése több futásteljesítmény-szinthez azonos aránnyal funkció** javítja a futásteljesítmény-díj számítását. A szolgáltatás engedélyezéséhez kövesse az alábbi lépéseket.

1. Válassza a **Munkaterületek** > **Szolgáltatáskezelés** lehetőséget. 
2. A listában keresse meg és válassza ki a listában a **A futásteljesítmény összeg kiszámításának engedélyezése több futásteljesítmény-szinthez azonos aránnyal** lehetőséget, majd válassza az **Engedélyezés most** lehetőséget.

A funkció engedélyezése után állítsa vissza a futásteljesítményt úgy, hogy az megfelelően tükrözze a **Mennyiség** mező értékét. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
