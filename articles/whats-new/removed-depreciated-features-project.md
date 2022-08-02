---
title: Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations
description: Ez a cikk azokat a funkciókat ismerteti, amelyeket eltávolítottak, vagy amelyeket a Dynamics 365 Project Operations.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations

_**A következőre vonatkozik:** Project Operations az erőforrás-/nem készletalapú forgatókönyvekhez, Lite központi telepítés – ajánlattól proforma számlázásig, és Project Operations a készlet-/termelésalapú forgatókönyvekhez_

Ez a cikk azokat a funkciókat ismerteti, amelyeket eltávolítottak, vagy amelyeket a Dynamics 365 Project Operations.

- Az *eltávolított* funkciók a továbbiakban nem érhetőek el a termékben.
- Az *elavult* funkciók nem állnak aktív fejlesztés alatt, és eltávolíthatják őket egy későbbi frissítésben.

Ez a lista segítséget kíván nyújtani Önnek ezen eltávolítások és elavult funkciók figyelembe vételében saját tervezés céljából.

> [!NOTE]
> A pénzügyi és műveleti alkalmazások objektumairól részletes információk a [**Technikai referenciajelentésekben találhatók**](/dynamics/s-e/global/axtechrefrep_61). A jelentések különböző verzióinak összehasonlításával megismerheti azokat az objektumokat, amelyek megváltoztak vagy el lettek távolítva a pénzügyi és üzemeltetési alkalmazások egyes verzióiban.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>A Project Operations 2022. márciusi kiadásában eltávolított vagy elavult funkciók

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektmenedzsment és könyvelés "Mindig hozzon létre korrekciós tranzakciót" paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Ellenőrzési célokból korrekciós tranzakciókra van szükség. Az elavulás után ez a paraméter el lesz rejtve. A rendszer mindig korrekciós tranzakciókat hoz létre, ahogyan jelenleg is teszi, ha a paraméter Igen értékre **van állítva**. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek éles/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy a korrekciós tranzakciók mindig létrejöjjenek. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektvezetés és könyvelés "A módosítási dátum használata új projektdátumként" paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Ezt a paramétert eredetileg arra használták, hogy lehetővé tegyék a beállításokat, amikor egy pénzügyi időszak bezártak. Erre azonban már nincs szükség, mert a tranzakció könyvelési dátuma a nyílt időszak első dátumára módosítható, ha konfigurálva van. A projekt dátumát nem szabad megváltoztatni, mert az a tranzakció bekövetkezésének dátumát jelöli. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek éles/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy a projekt dátuma soha ne változzon a korrekciókon. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Erőforrás-kérelem munkafolyamata a Project Operationsben készletezett/éles környezetben

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Elavult az alacsony használat és a tranzakciós volumen korlátozásai miatt. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek éles/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig letiltjuk az erőforrások kérésének lehetőségét a projekthez a munkafolyamat használatával. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>A projektszámla-javaslat lap fejléc és sorok nézetek nélkül

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Elavult a Projektszámla-javaslat és a számlanapló-űrlapok használata a **Fejléc és sorok nézet** funkciókulcstal együtt bevezetett oldal fejlesztései miatt. |
| **Másik funkció váltja fel?** | Igen |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek termelési/raktározott forgatókönyvekhez; Projektműveletek erőforrás-/nem készletezett forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig kikapcsoljuk a korábbi (örökölt) oldalt, és alapértelmezés szerint bekapcsoljuk a **Projektszámla-javaslat és a számlanapló űrlapok használata a Fejléc és sorok nézet** funkciókulcsgal. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>A Project Operations 2021. decemberi kiadásában eltávolított vagy elavult funkciók

### <a name="collaboration-workspaces"></a>Együttműködési munkaterületek

[Együttműködési munkaterület létrehozása vagy csatolása (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Az alacsony használat miatt elavult. Azok az ügyfelek, akik a Project Operationst erőforrás-/nem készletezett forgatókönyvekhez használják, kihasználhatják [az Office-csoportokkal](../project-management/collaboration-groups.md) való együttműködést. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás  |
| **Központi telepítés lehetősége** | Projektműveletek éles/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2022. december 1-jéig azt tervezzük, hogy már nem támogatjuk az együttműködési munkaterületeket. |
