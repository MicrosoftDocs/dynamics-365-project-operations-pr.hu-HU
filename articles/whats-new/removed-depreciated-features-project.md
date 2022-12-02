---
title: Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations szolgáltatásban
description: Ez a cikk azokat a funkciókat ismerteti, amelyek el lettek távolítva, vagy eltávolításuk be van tervezve a Dynamics 365 Project Operations alkalmazásban.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028332"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations szolgáltatásban

_**A következőre vonatkozik:** Project Operations az erőforrás-/nem készletalapú forgatókönyvekhez, Lite központi telepítés – ajánlattól proforma számlázásig, és Project Operations a készlet-/termelésalapú forgatókönyvekhez_

Ez a cikk azokat a funkciókat ismerteti, amelyek el lettek távolítva, vagy eltávolításuk be van tervezve a Dynamics 365 Project Operations alkalmazásban.

- Az *eltávolított* funkciók a továbbiakban nem érhetőek el a termékben.
- Az *elavult* funkciók nem állnak aktív fejlesztés alatt, és eltávolíthatják őket egy későbbi frissítésben.

Ez a lista segítséget kíván nyújtani Önnek ezen eltávolítások és elavult funkciók figyelembe vételében saját tervezés céljából.

> [!NOTE]
> A pénzügyi és műveleti alkalmazások objektumaival kapcsolatban részletes információkat a [**Technikai referenciajelentésekben**](/dynamics/s-e/global/axtechrefrep_61) talál. Ezen jelentések különböző verzióit összehasonlíthatja, hogy megismerje azokat az objektumokat, melyek módosítva lettek vagy el lettek távolítva a pénzügyi és műveleti alkalmazások egyes verzióiban.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Eltávolított vagy elavult funkciók a Project Operations alkalmazás 2022 márciusi kiadásában

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektmenedzsment és könyvelés „Mindig hozzon létre helyesbítési tranzakciót” paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Az auditálás céljából szükség van a helyesbítési tranzakciókra. Az avultatás után a paraméter rejtett lesz. A rendszer mindig létrehozza a helyesbítési tranzakciókat, ahogy most, amikor a paraméter értéke **Igen**. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projekt Operations gyártási/készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy mindig létrejöjjenek a helyesbítési tranzakciók. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektmenedzsment és könyvelés "A helyesbítési dátum használata új projektdátumként" paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Ezt a paramétert eredetileg a helyesbítések elérhetővé tételéhez használták a pénzügyi időszak lezárásakor. Azonban már nincs szükség rá, mert a tranzakció könyvelési dátuma, ha konfigurálva van a nyitott időszak első dátumra módosítható. A projekt dátumát nem szabad módosítani, mert a tranzakció bekövetkezésének dátumát jelzi. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projekt Operations gyártási/készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy a projekt dátuma sose legyen módosítva korrekciók esetén. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Erőforráskérelem munkafolyamat Project Operations készleten vagy gyártáson alapuló forgatókönyvek esetén

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Az alacsony használati és tranzakciómennyiség-korlátozások miatt elavult. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projekt Operations gyártási/készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-ig letiltjuk az erőforrások igénylését a projekthez a munkafolyamat használatával. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekt számlajavaslat oldal Fejléc és Sorok nézet nélkül

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Avultatva lett az oldal javításai miatt, amelyek a **Projektszámla-ajánlat és számlanapló űrlapok használata Fejléc és Sorok nézetben** funkciókulccsal együtt lettek bevezetve. |
| **Másik funkció váltja fel?** | Igen |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Project Operations termelési vagy készletezett forgatókönyvekhez; Projektműveletek erőforrás/nem készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-ig kikapcsoljuk a korábbi (örökölt) oldalt, és alapértelmezetten bekapcsoljuk a **Projektszámla-ajánlat és számlanapló űrlapok használata Fejléc és Sorok nézetben** funkciót. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Eltávolított vagy elavult funkciók a Project Operations alkalmazás 2021 decemberi kiadásában

### <a name="collaboration-workspaces"></a>Együttműködési munkaterületek

[Együttműködési munkaterület létrehozása vagy hivatkozás rá (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Az alacsony használat miatt elavult. Az erőforrás-/nem készlet alapú forgatókönyvekben a Project Operations alkalmazást használó ügyfelek az [Együttműködés Office-csoportokkal](../project-management/collaboration-groups.md) funkciót használhatják. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás  |
| **Központi telepítés lehetősége** | Projekt Operations gyártási/készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2022. december 1-túl a tervek szerint nem támogatjuk az Együttműködési munkaterületeket. |
