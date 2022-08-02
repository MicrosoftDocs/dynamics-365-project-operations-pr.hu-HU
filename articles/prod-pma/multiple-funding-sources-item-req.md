---
title: Több forrással rendelkező projektszerződések cikk-követelményei
description: Ez a cikk arról nyújt tájékoztatást, hogyan konfigurálhatja és használhatja az elemkövetelményeket több finanszírozási forrással.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028476"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Több forrással rendelkező projektszerződések cikk-követelményei

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

A projektalapú teljesítésekre vonatkozó egyes szerződéses megállapodásokhoz több finanszírozási forrásra is szükség lehet. Ez a cikk azt ismerteti, hogyan választhatja ki és konfigurálhatja a kívánt finanszírozási forrásokat, ha egy projekthez vagy projektszerződéshez több forrásra van szükség.

## <a name="terminology"></a>Terminológia

- **Finanszírozási forrás** – A projektszerződés munkáját finanszírozó entitás. Ez az entitás lehet belső szervezet vagy külső számlaszámla (vevő vagy támogatás).
- **Projektügyfél** – Az az entitás, amelyhez a projektmunkát kézbesítik.
- **Számla számla** – A projektmunkáért fizető külső entitás.

## <a name="example"></a>Példa

Contoso két ügyfelével, az Adatum US-val és az Adatum Corporate-val nyerte el a berendezés megújítására vonatkozó szerződést. A szerződés hardver- és telepítési szolgáltatásokat tartalmaz, amelyeket az Adatum US-nek (a projektügyfelnek) szállítanak. A hardvert az Adatum Corporate finanszírozza (1. számlaszámla), a telepítési munkákat pedig az Adatum US finanszírozza (2. számlaszámla).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Számlaszámla alapértelmezett szabályainak beállítása a cikkkövetelményekhez

### <a name="prerequisites"></a>Előfeltételek

- Microsoft Dynamics 365 A Finance **10.0.27-es vagy újabb** verziója szükséges a több számlaszámlával rendelkező cikkkövetelmények használatához.
- A rendszergazdának engedélyeznie kell a Több finanszírozási forrással rendelkező elemkövetelmények engedélyezése a **Project Operations készletezett/éles környezetben futó forgatókönyvekhez** funkciót a **Funkciókezelés** munkaterületen.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>A számla számla alapértelmezett szabályainak beállítása

A számlafiók alapértelmezett szabályainak beállításához kövesse az alábbi lépéseket.

1. Lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
1. **Az Általános** lap **Értékesítési rendelések és cikkkövetelmények** szakaszában állítsa az **Engedélyezés több finanszírozási forrással** rendelkező projektekhez beállítást Igen **értékre**.
1. **Az Alapértelmezett vevő** mezőben adja meg, hogy a cikkszükségleten szereplő projektszállítási vevő honnan származik alapértelmezés szerint:

    - **Finanszírozási forrásból** – Az alapértelmezett projektteljesítési ügyfél a finanszírozási forrásból származik. Ha több finanszírozási forrás van társítva a projektszerződéshez, a rendszer a lista első finanszírozási forrását használja.
    - **Projektből** – Az alapértelmezett projektszállítási ügyfél a Projektrekord-fiók **mezőben kiválasztott** vevőtől származik.

1. Választható: Állítsa be vagy módosítsa az alapértelmezett számlafiókot a projektrekordokban:

    1. Lépjen a Projektvezetési és **könyvelési**\> projektek **·**\> Minden projekt **elemre**, és nyissa meg a projektrekord részleteit.
    2. **Az Általános** lapon állítsa be vagy frissítse az **Alapértelmezett számlaszámla** mezőt. A megadott fiók lesz a projekthez létrehozott új cikkkövetelmények alapértelmezett számlaszámla- fiókja. Ha üresen hagyja a mezőt, a rendszer alapértelmezés szerint az első projektszerződés-finanszírozási forrás számlaszámláját használja. A felhasználók azonban megváltoztathatják a fiókot a rekord mentésekor.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Válassza ki a cikkszükséglet létrehozásakor használni kívánt számlaszámlát

A cikkszükséglet létrehozásakor használni kívánt számlafiók kiválasztásához kövesse az alábbi lépéseket.

1. Lépjen a Projektvezetési és **könyvelési**\> projektek **·**\> Minden projekt **elemre**, és válassza ki a projektrekordot.
1. A Csomag **lapon válassza a** Cikkkövetelmények **lehetőséget**.
1. Hozzon létre egy új cikkszükségletrekordot.

    - Alapértelmezés szerint a **rekord Számlaszámla** mezője a projekthez beállított számlafiókra van beállítva. Módosíthatja a Számlaszámla **mező értékét,** majd mentheti a rekordot. A rekord mentése után már nem frissítheti a **Számla számla értékét**. Ha frissítenie kell a **számlaszámla** értékét a cikkszükséglethez, törölje a meglévő cikkszükségletet, majd hozzon létre egy újat, amely rendelkezik a kívánt értékkel.
    - Alapértelmezés szerint a **cikkszükséglet Vevő** mezője a **Projektvezetési és könyvelési paraméterek** oldalon **beállított Alapértelmezett vevői** érték alapján van beállítva.

    A cikkszükségletrekord mentésekor a rendszer társítja azt a **Cikkszükséglet értékesítési rendelés** fejlécrekordjához. Ha nincs nyitott értékesítésirendelés fejléce a kiválasztott számlaszámlával, a rendszer létrehoz egyet, és társítja hozzá a cikkszükségleti sort.

> [!NOTE]
> A cikkszükségletek számlázása mindig teljes egészében a rekordban beállított számlaszámlára történik. A rendszer jelenleg nem támogatja a cikkkövetelményekkel rendelkező finanszírozásfelosztási szabályokat, és nem osztja fel a feladást a forrásallokációs szabályok beállítása alapján.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Cikkszükséglet létrehozása cikk-előrejelzési rekordból

Ha cikkszükségletet szeretne létrehozni egy cikk-előrejelzési rekordból, kövesse az alábbi lépéseket.

1. Lépjen a Projektvezetési és **könyvelési**\> projektek **·**\> Minden projekt **elemre,** és válassza ki a projektrekordot.
1. A Csomag lapon válassza a **Cikk-előrejelzések lehetőséget** **.**
1. Hozzon létre egy új cikk-előrejelzési rekordot.
1. Választható lehetőség: A **Projekt** lap Finanszírozási forrás **mezőjében** válassza ki a kívánt számlaszámlát.
1. Válassza az Elemszükséglet **létrehozása lehetőséget**, és erősítse meg a kapott üzenetet.

    > [!NOTE]
    > A rendszer átmásolja a **Finanszírozási forrás** értékét a cikk-előrejelzési rekordból az újonnan létrehozott cikkszükségletrekordba.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Alapértelmezett számlaszámla, ha a rendszer automatikusan létrehoz egy cikkszükségletet egy beszerzésirendelés-sorból

Ha a **Cikkszükséglet** létrehozása beállítás Igen **értékre** van állítva a **Projektvezetési és könyvelési** paraméterek lapon, a rendszer automatikusan létrehoz egy cikkszükségletet egy új projektvásárlási rendelési sor mentésekor. Alapértelmezés szerint a Számlaszámla **és** a **Cikk követelmény** mezők a projektrekord Alapértelmezett számlaszámla **mezőjének értékére** vannak beállítva. A rendszer jelenleg nem támogatja az ilyen típusú rekordok számlafiókjának frissítését vagy módosítását.
