---
title: Több forrással rendelkező projektszerződések cikk-követelményei
description: Ebből a cikkből megtudhatja hogyan konfigurálhatók és használhatók az cikk-követelmények több finanszírozási forrással.
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

Egyes projektalapú szállítandó termékekkel kapcsolatos szerződéses megállapodásokhoz több finanszírozási forrás is szükséges lehet. Ez a cikk ismerteti, hogyan válassza ki és konfigurálja a kívánt finanszírozási forrásokat, amikor egy projekthez vagy projektszerződéshez több forrásra van szükség.

## <a name="terminology"></a>Terminológia

- **Finanszírozási forrás**: A projektszerződés munkáját finanszírozó entitás. Ez az entitás lehet belső szervezet vagy külső számlapartner (ügyfél vagy engedély).
- **Projekt ügyfele** – Az entitás, amelynek a projekt munkáját szállítják.
- **Számlapartner** – A projektért fizető külső entitás.

## <a name="example"></a>Példa

A Contoso két ügyfelével megnyert egy berendezés-felújítási szerződést: az Adatum US és az Adatum Corporate cégekkel. A szerződés hardver- és telepítési szolgáltatásokat tartalmaz, amelyek az Adatum US (a projekt ügyfele) számára lesznek leszállítva. A hardvereszközöket az Adatum Corporate (1. számlapartner), a telepítési munkát pedig az Adatum US (2. számlapartner) finanszírozza majd.

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Számlafiók alapértelmezési szabályainak beállítása a cikk-követelményekhez

### <a name="prerequisites"></a>Előfeltételek

- A több számlaspartnerrel rendelkező cikk-követelmények alkalmazásához használatához a Microsoft Dynamics 365 Finance **10.0.27-es vagy újabb verziója** szükséges.
- A rendszergazdának engedélyeznie kell a **Több finanszírozási forrással rendelkező cikk-követelmények engedélyezése e Project Operations készletezett / termelésalapú forgatókönyveihez** funkciót a **Funkciókezelés** munkaterületen.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>A számlapartner alapértelmezési szabályainak beállítása

A számlapartner alapértelmezési szabályainak beállításhoz hajtsa végre a következő lépéseket.

1. Lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
1. Az **Általános** lap **Beszerzési rendelések és cikk-követelmények** szakaszában állítsa a **Több finanszírozási forrással rendelkező projektek engedélyezése** beállítást **Igen** értékre.
1. Adja meg az **Alapértelmezett ügyfél** mezőben, hogy alapértelmezetten honnan származik a cikk-követelmény projektszállítási ügyfele:

    - **Finanszírozási forrásból** Az alapértelmezett projekt szállítási ügyfele a finanszírozási forrásból származik. Ha a projektszerződéshez több finanszírozási forrás is társítva van, akkor a listában az első finanszírozási forrás lesz használva.
    - **Projektből** – Az alapértelmezett projekt szállítási ügyféle abból az ügyfélből származik, aki ki van jelölve a **Projektrekord partnere** mezőben

1. Nem kötelező: Az alapértelmezett számlapartner beállítása vagy módosítása projektrekordokhoz:

    1. Nyissa meg a **Projektmenedzsment és könyvelés** \> **Projektek** \> **Minden projekt** lehetőséget, és nyissa meg a projektrekord részleteit.
    2. Az **Általános** lapon állítsa be vagy frissítse az **Alapértelmezett számlapartner** mezőt. A megadott partner lesz a projekthez létrehozott új cikkkövetelmények alapértelmezett számlapartnerének használva. Ha üresen hagyja a mezőt, a program alapértelmezés szerint az első projektszerződés finanszírozási forrása számlapartnerét használja. A felhasználók azonban a rekord mentésekor módosíthatják a partnert.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Válassza ki a cikk-követelmény létrehozásakor használni kívánt számlapartnert

A cikk-követelmény létrehozásakor használni kívánt számlapartner kiválasztásához kövesse az alábbi lépéseket.

1. Válassza ki a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** lehetőséget, és válasszon ki egy projektrekordot.
1. A **Terv** lapon válassz a **Cikk-követelmények** lehetőséget.
1. Hozzon létre egy új cikk-követelmény rekordot.

    - Alapértelmezés szerint a rekord **Számlapartner** mezőjének beállítása a projekthez beállított számlapartner. Módosíthatja a **Számlapartner** mező értékét, majd mentheti a rekordot. A rekord mentése után a **Számlapartner** értéke már nem frissíthető. Ha frissítenie kell a **Számlapartner** értékét a cikk-követelményhez, törölje a meglévő cikk-követelményt, majd hozzon létre egy újat, amely a kívánt értékkel rendelkezik.
    - Alapértelmezés szerint a cikk-követelményhez tartozó **Ügyfél** mező a **Projektmenedzsment és a könyvelés paraméterei** lapon beállított **Alapértelmezett ügyfél** értéke alapján van beállítva.

    A cikk követelmény-rekord mentésekor a rendszer társítja azt a **Cikk követelmény értékesítési rendelése** fejlécrekordhoz. Ha egyetlen megnyitott értékesítési rendelés fejléce sem rendelkezik a kijelölt számlapartnerrel, akkor a rendszer létrehoz egyet, és társítja hozzá a cikk-követelmény sorát.

> [!NOTE]
> A cikk-követelmények mindig teljes mértékben számlázva vannak a rekordban beállított számlapartner felé. A rendszer jelenleg nem támogatja az finanszírozási hozzárendelési szabályokat, amelyekhez cikk-követelmények tartoznak, és a feladást nem osztja fel a finanszírozáselosztási szabályokkal.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Cikk-követelmény létrehozása cikkelőrejelzési rekordból

Cikk-követelmény létrehozásához egy cikkelőrejelzési rekordból kövesse az alábbi lépéseket.

1. Válassza ki a **Projektvezetés és könyvelés** \> **Projektek** \> **Minden projekt** lehetőséget, és válasszon ki egy projektrekordot.
1. A **Terv** lapon válassz a **Cikk-előrejelzések** lehetőséget.
1. Hozzon létre egy új cikk-előrejelzési rekordot.
1. Nem kötelező: Válassza ki a kívánt számlapartnert a **Projekt** lap **Finanszírozási forrás** mezőjében.
1. Válassza a **Cikk-követelmény létrehozása** lehetőséget, és erősítse meg a kapott üzenetet.

    > [!NOTE]
    > A rendszer a **Finanszírozási forrást** másolja a cikk-előrejelzési rekordjából az újonnan létrehozott cikk-követelmény rekordba.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Alapértelmezett számlapartner, amikor a rendszer automatikusan hoz létre cikk-követelményt egy beszerzésirendelés-sorból

Ha a **Projektvezetés könyvelés paraméterei** lapon a **Cikk-követelmény létrehozása** beállítása **Igen**, akkor a rendszer automatikusan létrehoz egy cikk-követelményt az új projekt beszerzésirendelés-sorának mentésekor. Alapértelmezés szerint a **Számlapartner** és a **Cikk-követelmény** mező a projektrekord **Alapértelmezett számlapartner** mezőjének az értékére lesz beállítva. A rendszer jelenleg nem támogatja az ilyen típusú rekordokhoz tartozó számlapartner frissítését vagy megváltoztatását.
