---
title: Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations
description: Ez a témakör az eltávolított vagy a programból való eltávolításra tervezett szolgáltatásokat ismerteti Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601573"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Eltávolított vagy elavult funkciók a Dynamics 365 Project Operations

_**A következőre vonatkozik:** Project Operations az erőforrás-/nem készletalapú forgatókönyvekhez, Lite központi telepítés – ajánlattól proforma számlázásig, és Project Operations a készlet-/termelésalapú forgatókönyvekhez_

Ez a témakör az eltávolított vagy a programból való eltávolításra tervezett szolgáltatásokat ismerteti Dynamics 365 Project Operations.

- Az *eltávolított* funkciók a továbbiakban nem érhetőek el a termékben.
- Az *elavult* funkciók nem állnak aktív fejlesztés alatt, és eltávolíthatják őket egy későbbi frissítésben.

Ez a lista segítséget kíván nyújtani Önnek ezen eltávolítások és elavult funkciók figyelembe vételében saját tervezés céljából.

> [!NOTE]
> A Pénzügy és műveletek alkalmazások objektumaival kapcsolatos részletes információk a [**Technikai referenciajelentésekben találhatók**](/dynamics/s-e/global/axtechrefrep_61). Összehasonlíthatja a jelentések különböző verzióit, hogy megismerje azokat az objektumokat, amelyek a Pénzügy és műveletek alkalmazások minden verziójában megváltoztak vagy el lettek távolítva.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>A Project Operations 2022. márciusi kiadásában eltávolított vagy elavult funkciók

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektmenedzsment és -könyvelés "Mindig hozzon létre korrekciós tranzakciót" paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Ellenőrzési célokra korrekciós tranzakciókra van szükség. Az elavulás után ez a paraméter el lesz rejtve. A rendszer mindig korrekciós tranzakciókat hoz létre, ugyanúgy, mint jelenleg, ha a paraméter **értéke Igen**. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek termeléshez/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy a korrekciós tranzakciók mindig létrejönjenek. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektmenedzsment és -számvitel "Helyesbítés dátumának használata új projektdátumként" paraméter

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Ezt a paramétert eredetileg a pénzügyi időszak bezárásakor történő kiigazítások engedélyezésére használták. Erre azonban már nincs szükség, mert a tranzakció könyvelési dátuma a nyitott időszak első dátumára módosítható, ha be van állítva. A projektdátumot nem szabad módosítani, mert a tranzakció időpontjában jelenik meg. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek termeléshez/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig elrejtjük a paramétert, és megváltoztatjuk a rendszer viselkedését, hogy a projekt dátuma soha ne módosuljon a módosításokkor. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Erőforrás-igénylő munkafolyamat a Project Operations-ben raktározott/termelésalapú forgatókönyvekhez

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Elavult az alacsony használat és a tranzakciós mennyiség korlátozása miatt. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek termeléshez/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig letiltjuk azt a lehetőséget, hogy erőforrásokat igényeljünk a projekthez a munkafolyamat használatával. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektszámla-javaslat lap Fejléc és Sorok nézet nélkül

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Elavult a Projekt használata számlajavaslattal és a Számlanapló képernyőkkel együtt bevezetett lap javítása miatt a **Fejléc és sorok nézet** funkcióval. |
| **Másik funkció váltja fel?** | Igen |
| **Érintett termékterületek** | Alkalmazás |
| **Központi telepítés lehetősége** | Projektműveletek termeléshez/raktározott forgatókönyvekhez; Projektműveletek erőforrás- és nem raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2023. március 1-jéig kikapcsoljuk a korábbi (örökölt) oldalt, és alapértelmezés szerint bekapcsoljuk a **Projekt használata számlajavaslatot és a számlanapló űrlapokat a Fejléc és sorok nézet** funkcióbillentyűvel. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>A Project Operations 2021. decemberi kiadásában eltávolított vagy elavult funkciók

### <a name="collaboration-workspaces"></a>Együttműködési munkaterületek

[Együttműködési munkaterület létrehozása vagy csatolása (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Elavulás/eltávolítás oka** | Az alacsony használat miatt elavult. Azok az ügyfelek, akik a Project Operations-t erőforrás-/nem raktározott forgatókönyvekhez használják, kihasználhatják [az Office-csoportokkal](../project-management/collaboration-groups.md) való együttműködést. |
| **Másik funkció váltja fel?** | No |
| **Érintett termékterületek** | Alkalmazás  |
| **Központi telepítés lehetősége** | Projektműveletek termeléshez/raktározott forgatókönyvekhez |
| **Állapot** | Elavult: 2022. december 1-jéig azt tervezzük, hogy a továbbiakban nem támogatjuk az együttműködési munkaterületeket. |
