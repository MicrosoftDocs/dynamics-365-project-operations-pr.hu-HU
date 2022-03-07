---
title: Újdonságok 2021. májusában – Project Operations egyszerű telepítés
description: Ez témakör a Project Operations egyszerű telepítés 2021 májusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005979"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Újdonságok 2021. májusában – Project Operations egyszerű telepítés

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

   - Project Operations a Dataverse-környezet 4.10.0.186 verzióján.

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

Ez a kiadás a következő funkciókat tartalmazza:

- [Ütemezési módok](../../project-management/scheduling-modes.md): A projektmenedzserek immár definiálhatják, hogy a projekteket a rögzített időtartam, rögzített munka vagy rögzített egységek ütemezési módjával kell-e kezelni.

## <a name="quality-updates"></a>Minőségi frissítések

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2224568 | Hozzáadott logika a számlameghívó beépülő modult megerősítő testreszabások engedélyezéséhez. |
| Számlázás és árképzés | 2101098 | A proforma számlák alapértelmezett mezőinek logikáját továbbfejlesztettük. Ezek a mezők többek között a **Számlázási cím**, a **Számlázási név** és a **Fizetési feltételek**. A mezők ettől az alapértelmezett értéktől származnak a projektszerződés megfelelő ügyfélrekordja alapján. |
| Számlázás és árképzés | 2021413 | Frissítette a **Tényleges költség** és **Értékesítés** mezőket a **Feladat** entitáson, hogy tartalmazza a feladatokon a számlázatlan és számlázott kiadások értékesítési értékeit. |
| Számlázás és árképzés | 2182110 | Projektszerződés másolásakor a szerződéssor azonosítója újra lesz generálva a célprojekt-szerződésben, hogy biztosítsák egyediségét. |
| Lehetőségkezelés | 2186741 | Hozzáadott ellenőrzések annak biztosítására, hogy az **Eredet** mező és a tranzakciótípus ne legyen frissíthető a meglévő árajánlatsor részleteivel kapcsolatban. |
| Lehetőségkezelés | 2191353 | Mérföldkövek létrehozását nem szabad idő- és anyagszerződési sorokban engedélyezni. |
| Lehetőségkezelés | 2216956 | Kijavítottuk az **Árak frissítésével** kapcsolatos problémákat. |
| Tervezés és nyomon követés | 2182979 | A projektmásolási funkció tovább lett fejlesztve annak biztosítására, hogy a költségbecslési sorok át legyenek másolva az eredeti projektből. |
| Tervezés és nyomon követés | 2184144 | A projektmásolási funkció tovább lett fejlesztve annak biztosítására, hogy az erőforráspozíció neve át legyen másolva az eredeti projektből. |
| Tervezés és nyomon követés | 2184799 | Szigorított vezérlés projekt másoláskor annak biztosítására, hogy a becsült kezdési dátum ne legyen módosítható a másolás közben. |
| Tervezés és nyomon követés | 2185134 | Egy projekt másolása során célprojekt becsült kezdési dátuma a mai dátumra van állítva. |
| Tervezés és nyomon követés | 2196373 | Győződjön meg arról, hogy a projektmenedzser és a csoporttag rekordjai nem ismétlődnek meg a projektcsoportban egy projekt másolása során. |
| Tervezés és nyomon követés | 2211833 | Az erőforrás-hozzárendelések a forrásprojekt-feladatból a célprojektbe másolhatók. |
| Tervezés és nyomon követés | 2186541 | A **Becslések** rácsban, az **Erőforrás** szerinti csoportosításkor felmerült problémák kijavítva. |
| Tervezés és nyomon követés | 2166906 | A feladat tranzakciókategóriáit át kell másolni az **Erőforrás-hozzárendelés** entitásba. |
| Erőforráskezelés | 2125362 | Az általános csoporttag óraalapú felosztási módszerrel történő létrehozással kapcsolatos problémák kijavítva. |
| Idő és költség | 2113603 | Az attribútumok **Időbejegyzés** lapról való eltávolításával, a testreszabással kapcsolatos probléma kijavítva. A rendszer most ellenőrzi, hogy az attribútum létezik-e a lapon, mielőtt parancsfájl használatával hozzáférne az attribútumhoz. |
| Idő és költség | 2204377 | A másolt munkaidő-nyilvántartásoknak automatikusan meg kell jelenniük, amikor a **Hét másolása** lehetőséget választja. |
| Idő és költség | 2209059 | Az **Állapot** mező szerkeszthető a Dynamics 365 Field Service időbejegyzésekhez. |
