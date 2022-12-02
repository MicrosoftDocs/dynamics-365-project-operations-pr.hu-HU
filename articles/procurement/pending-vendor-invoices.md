---
title: Nem készletezett anyagok vagy beszerzési kategóriák beszerzése függőben lévő szállítói számla alapján
description: Ez a cikk ismerteti, hogyan lehet rögzíteni a függőben lévő szállítói számlákat.
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
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nem készletezett anyagok vagy beszerzési kategóriák beszerzése függőben lévő szállítói számla alapján

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Amikor egy vállalat nem készleten lévő vagy beszerzési kategóriákat szerez egy projekthez, a költségek azonnal rögzítve lesznek a projekten belül. 

A Contoso Robotics US például egy berendezés felújítási projektjét végzi, és szoftverlicencekre van szüksége. Ezeket a licenceket egy harmadik fél szállítótól szerzik be.  A Dynamics 365 Finance használata esetén a kinnlevőségek számlák könyvelője rögzíti a függőben lévő szállítói számla dokumentumát, és a licencköltségeket közvetlenül a berendezésfelújítási projekthez rendeli. 

> [!IMPORTANT]
> Mielőtt a jelen cikk leírt funkciókat használod, tekintsd át és alkalmazd a szükséges konfigurációkat. További információ: [Nem raktározott anyagok és függőben lévő szállítói számlák engedélyezése](configure-materials-nonstocked.md) és [Használjon beszerzési kategóriákat a projekt beszerzési rendeléseihez és a függőben lévő szállítói számlákhoz](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projekthez kapcsolódó, függőben lévő szállítói számla kiküldése 

A függőben lévő szállítói számlák a **Függőben lévő szállítói számlák** oldalon (**Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák**) rögzíthetők. A következő lépésekkel tegye közzé a projekttel kapcsolatos, függőben lévő szállítói számlát:

1. Lépjen a **Kötelezettségek** > **Számlák** pontra, és válassza az **Új** lehetőséget. 
1. A **Számlapartner** mezőben jelöljön ki egy szállítót, a **Szám** mezőben pedig adja meg a szállítói számla azonosítóját.
1. Vegyen fel egy sort a szállító számlájához, majd a **Cikkszám** mezőben jelölje ki a szállítótól megvásárolt, nem készleten kívüli tételt. Másik lehetőségként válassza ki a **Beszerzési kategória** mezőben azt a kategóriát, amit az beszállítótól vásárolt.   
1. Adja hozzá a megvásárolt mennyiséget. A rendszer a nem készleten alapuló cikkárkonfiguráció alapján kitölti az egységárat. 
1. Ellenőrizze a sorban a teljes összeget és az egyéb szükséges adatokat.
1. A sor részleteiben a **Projekt** lapon jelölje ki annak a projektnek az azonosítóját, amelybe ezt az elemet rögzíteni fogja.
1. Opcionális: Válassza ki a tevékenység számát, és frissítse a projektkategóriát és a sortulajdonságot.
1. Adja fel a függőben lévő szállítói számlát. A rendszer a következő információkat rögzíti a számla feladásakor:
    
    - A szállító egyenlege.
    - Az áfa összege.
    - A projekttel szembeni költséget a rendszer a beszerzési integrációs számlához rögzíti.
    - A projekt tényadat költségtranzakciója a Dataverse-ben.  A tranzakció további feldolgozása a [Project Operations Integration napló](../project-accounting/project-operations-integration-journal.md) segítségével történik. Ennek a naplónak a közzétételével az összeg a beszerzési integrációs számlából a projektköltség-számlába kerül át. 
    - A projektügyfél számára az idő és az anyag számlázási módja segítségével számlázható vásárlások. Emellett a Dataverse-ben is létrejönnek leszámlázatlan értékesítési tranzakciók. A termék árlistája a Dataverse-ben nem számlázott értékesítési tranzakció értékesítési árára és mennyiségeire használatos.
