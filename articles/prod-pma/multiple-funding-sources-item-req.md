---
title: Több finanszírozási forrással rendelkező projektszerződések tételkövetelményei
description: Ez a témakör a cikkszükségletek több finanszírozási forrással való konfigurálásáról és használatáról nyújt tájékoztatást.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728086"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Több finanszírozási forrással rendelkező projektszerződések tételkövetelményei

_**A következőre vonatkozik:** Project Operations készleten vagy gyártáson alapuló forgatókönyvekhez_

A projektalapú eredményekre vonatkozó egyes szerződéses megállapodások több finanszírozási forrást is igényelhetnek. Ez a témakör bemutatja, hogyan lehet kiválasztani és konfigurálni a kívánt finanszírozási forrásokat, ha egy projekt- vagy projektszerződéshez több forrásra van szükség.

## <a name="terminology"></a>Terminológia

- **Finanszírozási forrás** – Az a szervezet, amely finanszírozza a projektszerződési munkát. Ez az entitás lehet belső szervezet vagy külső számlaszámla (vevő vagy támogatás).
- **Projekt vevő** – az az entitás, amelynek a projektmunkát kézbesítik.
- **Számlaszámla** – A projektmunkát fizető külső entitás.

## <a name="example"></a>Példa

Contoso két ügyfelével, az Adatum US-val és az Adatum Corporate vállalattal nyert berendezésmegújítási szerződést. A szerződés hardver- és telepítési szolgáltatásokat tartalmaz, amelyeket az Adatum US (a projekt ügyfele) részére szállítanak. A hardvert az Adatum Corporate (1. számlaszámla) finanszírozza, a telepítési munkát pedig az Adatum US (2. számlaszámla) finanszírozza.

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Számlaszámla alapértelmezett szabályainak beállítása cikkszükségletekhez

### <a name="prerequisites"></a>Előfeltételek

- Microsoft Dynamics 365 A több számlaszámlával rendelkező cikkkövetelmények használatához a 10.0.27-es vagy újabb **pénzügyi és műveleti** verziónak kell használnia.
- A rendszergazdának engedélyeznie kell a **Cikkszükségletek engedélyezése több finanszírozási forrással a Szolgáltatáskezelő** munkaterületen található **Projektműveletek készletezett/termelésalapú forgatókönyvek** szolgáltatásához.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>A számlaszámla alapértelmezett szabályainak beállítása

A számlaszámla alapértelmezett szabályainak beállításához hajtsa végre az alábbi lépéseket.

1. Lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
1. **Az Általános** lap **Értékesítési rendelések és Cikkkövetelmények** szakaszában állítsa az **Engedélyezés több finanszírozási forrással** rendelkező projektek engedélyezése beállítást Igen **értékre**.
1. **Az Alapértelmezett vevő** mezőben adja meg, hogy a cikkszükségletben szereplő projektkézbesítési vevő alapértelmezés szerint honnan származik:

    - **Finanszírozási forrásból** – Az alapértelmezett projektkézbesítési ügyfél a finanszírozási forrásból származik. Ha több finanszírozási forrás kapcsolódik a projektszerződéshez, a lista első finanszírozási forrását használja a rendszer.
    - **Projektből** – Az alapértelmezett projektkézbesítési vevő a Projekt rekordszámla **mezőben** kiválasztott vevőtől származik.

1. Nem kötelező: Az alapértelmezett számlaszámla beállítása vagy módosítása a projektrekordokon:

    1. Nyissa meg a **Projektmenedzsment és könyvelési** \> **projektek minden** \> **projektet**, és nyissa meg a projektbejegyzés részleteit.
    2. **Az Általános** lapon állítsa be vagy frissítse az **Alapértelmezett számlaszámla** mezőt. A megadott számla a projekthez létrehozott új cikkszükségletek alapértelmezett számlaszámlájaként lesz használva. Ha üresen hagyja a mezőt, a program alapértelmezés szerint az első projektszerződés-finanszírozási forrás számlaszámláját használja. A felhasználók azonban a rekord mentésekor módosíthatják a fiókot.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Cikkszükséglet létrehozásakor használandó számlaszámla kiválasztása

A cikkszükséglet létrehozásakor használandó számlaszámla kiválasztásához hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Projektmenedzsment és könyvelési** \> **projektek minden** \> **projektet**, és válassza ki a projektbejegyzést.
1. A Terv **lapon válassza** a **Cikkkövetelmények lehetőséget**.
1. Hozzon létre egy új cikkszükséglet-rekordot.

    - Alapértelmezés szerint a **rekord Számla számla mezője** a projekthez beállított számlaszámlára van állítva. Módosíthatja a Számla számla **mező értékét,** majd mentheti a rekordot. A rekord mentése után már nem frissítheti a **Számla számla** értékét. Ha frissítenie kell a **cikkszükséglet Számla számlaértékét**, törölje a meglévő cikkszükségletet, majd hozzon létre egy újat, amely rendelkezik a kívánt értékkel.
    - Alapértelmezés szerint a **cikkszükséglet Vevő** mezője a **Projektkezelés és könyvelési paraméterek** lapon beállított **Alapértelmezett vevő** érték alapján van beállítva.

    A cikkszükségleti rekord mentésekor a rendszer a Cikkszükséglet eladási rendelés **fejlécrekordjához** társítja. Ha egyetlen nyitott értékesítési rendelés fejében sem szerepel a kijelölt számlaszámla, a rendszer létrehoz egyet, és társítja hozzá a cikkszükségletsort.

> [!NOTE]
> A cikkszükségletek mindig teljes mértékben kiszámlázhatók a rekordban beállított számlaszámlára. A rendszer jelenleg nem támogatja a cikkkövetelményekkel rendelkező finanszírozási felosztási szabályokat, és nem osztja fel a feladást a finanszírozásallokációs szabályok beállítása alapján.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Cikkszükséglet létrehozása cikk-előrejelzési rekordból

Cikk-előrejelzési rekordból cikkszükséglet létrehozásához hajtsa végre az alábbi lépéseket.

1. Ugrás a **Projektmenedzsment és könyvelés** \> **projektek minden** \> **projektre,** és válassza ki a projektbejegyzést.
1. A Terv **lapon válassza a** Cikk-előrejelzések **lehetőséget**.
1. Hozzon létre egy új cikk-előrejelzési rekordot.
1. Nem kötelező: A **Projekt** lap Finanszírozási forrás **mezőjében** válassza ki a kívánt számlaszámlát.
1. Válassza az **Elemszükséglet** létrehozása lehetőséget, és erősítse meg a kapott üzenetet.

    > [!NOTE]
    > A rendszer átmásolja a **Finanszírozási forrás** értékét a cikk-előrejelzési rekordból az újonnan létrehozott cikkszükséglet-rekordba.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Alapértelmezett számlaszámla, amikor a rendszer automatikusan létrehoz egy cikkszükségletet egy beszerzésirendelés-sorból

Ha a Projektkezelés és könyvelési paraméterek **lapon a** **Cikkszükséglet** létrehozása beállítás **értéke Igen**, a rendszer egy új projekt beszerzésirendelés-sor mentésekor automatikusan létrehoz egy cikkszükségletet. Alapértelmezés szerint a Számla számla és a **Cikkszükséglet** mezők a projektrekord Alapértelmezett számla számla **mezőjének értékére** vannak **beállítva.** A rendszer jelenleg nem támogatja az ilyen típusú rekordok számlafiókjának frissítését vagy módosítását.
