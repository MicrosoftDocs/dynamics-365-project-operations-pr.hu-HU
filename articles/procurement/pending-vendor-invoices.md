---
title: Nem raktározott anyagok vagy beszerzési kategóriák vásárlása függőben lévő szállítói számla használatával
description: Ez a cikk a függőben lévő szállítói számlák rögzítésének módját ismerteti.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921995"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nem raktározott anyagok vagy beszerzési kategóriák vásárlása függőben lévő szállítói számla használatával

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Mivel egy vállalat nem raktározott anyagokat vagy beszerzési kategóriákat szerez be egy projekthez, a költségek azonnal nyilvántarthatók a projekttel szemben. 

A Contoso Robotics US például egy berendezés felújítási projektjét végzi, és szoftverlicencekre van szüksége. Ezeket a licenceket egy harmadik fél szállítótól szerzik be.  A Dynamics 365 Finance használatával a Kötelezettségekért felelős ügyintéző egy függőben lévő szállítói számladokumentumot rögzít, és a licencköltségeket közvetlenül a berendezés megújítási projektjéhez rendeli. 

> [!IMPORTANT]
> A cikkben ismertetett funkciók használata előtt tekintse át és alkalmazza a szükséges konfigurációkat. További tájékoztatás: [Nem készletezett anyagok és függőben lévő szállítói számlák](configure-materials-nonstocked.md) engedélyezése és [Beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projekthez kapcsolódó, függőben lévő szállítói számla kiküldése 

A függőben lévő szállítói számlák a **Függőben lévő szállítói számlák** oldalon (**Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák**) rögzíthetők. A következő lépésekkel tegye közzé a projekttel kapcsolatos, függőben lévő szállítói számlát:

1. Lépjen a Kötelezettségek számlák **lapra** > **·**, és válassza az Új **lehetőséget**. 
1. **A Számla számlamezőben** válasszon ki egy szállítót, majd a **Szám** mezőbe írja be a szállítói számla azonosítóját.
1. Adjon hozzá egy sort a szállítói számlához, majd a **Cikkszám** mezőben válassza ki a szállítótól vásárolt nem készletezett cikket. Másik lehetőségként a **Beszerzési kategória** mezőben válassza ki a szállítótól beszerzett beszerzési kategóriát.   
1. Adja hozzá a megvásárolt mennyiséget. A rendszer kitölti az egységárat a nem raktározott cikkár-konfiguráció alapján. 
1. Ellenőrizze a sorban a teljes összeget és az egyéb szükséges adatokat.
1. A sor részleteiben, a **Projekt** lapon válassza ki annak a projektnek az azonosítóját, amelybe ezt az elemet rögzíteni fogja.
1. Nem kötelező: Válassza ki a tevékenység számát, és frissítse a projektkategóriát és a sortulajdonságot.
1. Adja fel a függőben lévő szállítói számlát. A számla feladásakor a rendszer a következő információkat rögzíti:
    
    - A szállító egyenlege.
    - Az áfa összege.
    - A projekttel szembeni költséget a rendszer a beszerzési integrációs számlához rögzíti.
    - A projekt tényadat költségtranzakciója a Dataverse-ben.  A tranzakció további feldolgozása a [Project Operations Integration napló](../project-accounting/project-operations-integration-journal.md) segítségével történik. Ennek a naplónak a közzétételével az összeg a beszerzési integrációs számlából a projektköltség-számlába kerül át. 
    - A projektügyfél számára az idő és az anyag számlázási módja segítségével számlázható vásárlások. Emellett a Dataverse-ben is létrejönnek leszámlázatlan értékesítési tranzakciók. A termék árlistája a Dataverse-ben nem számlázott értékesítési tranzakció értékesítési árára és mennyiségeire használatos.
