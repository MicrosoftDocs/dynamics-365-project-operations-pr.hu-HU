---
title: Nem készleten lévő anyagok beszerzése függőben lévő szállítói számla alapján
description: Ez témakör ismerteti, hogyan lehet rögzíteni a függőben lévő szállítói számlákat.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009039"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Nem készleten lévő anyagok beszerzése függőben lévő szállítói számla alapján

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Amikor egy vállalat nem készleten lévő anyagokat szerez egy projekthez, a költségek azonnal rögzítve lesznek a projekten belül. 

A Contoso Robotics US például egy berendezésfelújítási projektjét hajtják végre, és szoftverlicencekre van szüksége. Ezeket a licenceket egy harmadik fél szállítótól szerzik be.  A(z) Dynamics 365 Finance használata esetén a kinnlevőségek számlák könyvelője rögzíti a függőben lévő szállítói számla dokumentumát, és a licencköltségeket közvetlenül a berendezésfelújítási projekthez rendeli. 

> [!IMPORTANT]
> Mielőtt a jelen témakör leírt funkciókat használod, tekintsd át és alkalmazd a szükséges konfigurációkat. További információkért lásd: [Nem raktározott anyagok és függőben lévő szállítói számlák engedélyezése](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projekthez kapcsolódó, függőben lévő szállítói számla kiküldése 

A függőben lévő szállítói számlák a **Függőben lévő szállítói számlák** oldalon (**Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák**) rögzíthetők. A következő lépésekkel tegye közzé a projekttel kapcsolatos, függőben lévő szállítói számlát:

1. Lépjen a **Kötelezettségek** > **Számlák** pontra, és válassza az **Új** lehetőséget. 
2. A **Számla** mezőben jelöljön ki egy szállítót, a **Szám** mezőben pedig adja meg a szállítói számla azonosítóját.
3. Vegyen fel egy sort a szállító számlájához, és a **Cikkszám** mezőben jelölje ki a szállítótól megvásárolt, nem készleten kívüli tételt. 

    > [!NOTE]
    > A szállító számlasorai, amelyek valamely beszerzési kategórián alapulnak, nem rögzíthetők a projekthez. 
    
5. Adja hozzá a megvásárolt mennyiséget. A rendszer a nem készleten alapuló cikkárkonfiguráció alapján kitölti az egységárat. 
6. Ellenőrizze a sorban a teljes összeget és az egyéb szükséges adatokat.
7. A sor részleteiben a **Projekt** lapon jelölje ki annak a projektnek az azonosítóját, amelybe ezt az elemet rögzíteni fogja.
8. Tetszés szerint kiválaszthatja a tevékenység számát, és frissítheti a projektkategóriát és a sortulajdonságot.
9. Függőben lévő szállítói számla kibocsátása. A számla kibocsátásakor a rendszer a következő bejegyzéseket rögzíti:
    
    - A szállító egyenlege.
    - Az áfa összege.
    - A projekttel szembeni költséget a rendszer a beszerzési integrációs számlához rögzíti.
    - A projekt aktuális tranzakciója itt: Dataverse. A tranzakció további feldolgozása a [Project Operations Integration napló](../project-accounting/project-operations-integration-journal.md) segítségével történik. Ennek a naplónak a közzétételével az összeg a beszerzési integrációs számlából a projektköltség-számlába kerül át.
