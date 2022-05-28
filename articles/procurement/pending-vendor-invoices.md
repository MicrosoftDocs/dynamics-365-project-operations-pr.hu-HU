---
title: Nem raktározott anyagok vagy beszerzési kategóriák beszerzése függőben lévő szállítói számlával
description: Ez témakör ismerteti, hogyan lehet rögzíteni a függőben lévő szállítói számlákat.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612660"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nem raktározott anyagok vagy beszerzési kategóriák beszerzése függőben lévő szállítói számlával

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Mivel egy vállalat nem raktározott anyagokat vagy beszerzési kategóriákat szerez be egy projekthez, a költségek azonnal elszámolhatók a projekttel szemben. 

A Contoso Robotics US például egy berendezés felújítási projektjét végzi, és szoftverlicencekre van szüksége. Ezeket a licenceket egy harmadik fél szállítótól szerzik be.  A Dynamics 365 Finance használatával a Kötelezettségek ügyintézője rögzít egy függőben lévő szállítói számlabizonylatot, és a licencköltségeket közvetlenül a berendezés megújítási projektjéhez rendeli. 

> [!IMPORTANT]
> Mielőtt a jelen témakör leírt funkciókat használod, tekintsd át és alkalmazd a szükséges konfigurációkat. További információt a nem raktározott anyagok és függőben lévő szállítói számlák [engedélyezése, valamint](configure-materials-nonstocked.md) a beszerzési kategóriák használata projekt beszerzési rendelésekkel és függőben lévő szállítói számlákkal című témakörben talál.[...](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projekthez kapcsolódó, függőben lévő szállítói számla kiküldése 

A függőben lévő szállítói számlák a **Függőben lévő szállítói számlák** oldalon (**Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák**) rögzíthetők. A következő lépésekkel tegye közzé a projekttel kapcsolatos, függőben lévő szállítói számlát:

1. Nyissa meg a Kötelezettségek **számlák lehetőséget** > **, és válassza az** Új **lehetőséget**. 
1. **A Számla számla** mezőben jelöljön ki egy szállítót, majd a **Szám** mezőbe írja be a szállítói számla azonosítóját.
1. Adjon hozzá egy sort a szállítói számlához, majd a **Cikkszám** mezőben válassza ki a szállítótól beszerzett nem raktározott cikket. Másik lehetőségként a **Beszerzés kategória** mezőben válassza ki a szállítótól beszerzett beszerzési kategóriát.   
1. Adja hozzá a beszerzett mennyiséget. A rendszer a nem raktározott cikkár-konfiguráció alapján kitölti az egységárat. 
1. Ellenőrizze a sorban a teljes összeget és az egyéb szükséges adatokat.
1. A sor részleteinek **Projekt** lapján válassza ki annak a projektnek az azonosítóját, amelyhez a cikk rögzítésre kerül.
1. Nem kötelező: Válassza ki a tevékenység számát, és frissítse a projektkategória és a sortulajdonságot.
1. A függőben lévő szállítói számla feladása. A számla könyvelésekor a rendszer a következő adatokat rögzíti:
    
    - A szállító egyenlege.
    - Az áfa összege.
    - A projekttel szembeni költséget a rendszer a beszerzési integrációs számlához rögzíti.
    - A projekt tényadat költségtranzakciója a Dataverse-ben.  A tranzakció további feldolgozása a [Project Operations Integration napló](../project-accounting/project-operations-integration-journal.md) segítségével történik. Ennek a naplónak a közzétételével az összeg a beszerzési integrációs számlából a projektköltség-számlába kerül át. 
    - A projektügyfél számára az idő és az anyag számlázási módja segítségével számlázható vásárlások. Emellett a Dataverse-ben is létrejönnek leszámlázatlan értékesítési tranzakciók. A termék árlistája a Dataverse-ben nem számlázott értékesítési tranzakció értékesítési árára és mennyiségeire használatos.
