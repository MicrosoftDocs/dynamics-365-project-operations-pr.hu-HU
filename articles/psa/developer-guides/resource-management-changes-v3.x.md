---
title: Erőforrás-menedzsment változások (Project Service Automation 3.x)
description: Ez a cikk az Erőforrás-kezelés terület változásairól nyújt tájékoztatást.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916015"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Erőforrás-menedzsment változások (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

A cikk szakaszai a 3.x verzió Erőforrás-kezelés területén Dynamics 365 Project Service Automation végrehajtott módosításokról nyújtanak információt.

## <a name="project-estimates"></a>Projektbecslések

Az **msdyn\_projecttask** entitás **(Projektfeladat**) helyett a projektbecslések az **msdyn\_resourceassignment** entitáson alapulnak (**Erőforrás hozzárendelés**). Az erőforrás-hozzárendelések váltak az igazság forrásává a feladatok ütemezése és árazása során.

## <a name="line-tasks"></a>Sori feladatok

A PSA 3.x-ben a sorfeladatok elavultak (elavultak). A hozzárendelések a soros feladatok helyett az egész feladatra mutatnak.

A következő példa bemutatja, hogy a PSA korábbi verzióiban és a PSA 3.x-ben egy „Tesztfeladat” elnevezésű feladatot kapnak az A és B csapat tagjai.

- **A PSA 3.x előtt:**

    - Tesztfeladat

        - Tesztfeladat - 1. sorfeladat

            - Hozzárendelés az A-hoz

        - Tesztfeladat - 2. sorfeladat

            - Hozzárendelés a B-hoz

- **PSA 3.x:**

    - Tesztfeladat

        - Hozzárendelés az A-hoz
        - Hozzárendelés a B-hoz

## <a name="unassigned-assignment"></a>Nincs hozzárendelve

A PSA 3.x-ben a hozzá nem rendelt hozzárendelés egy olyan hozzárendelés, amelyet egy **NULL** csapattaghoz és **NULL** erőforráshoz rendelnek. Rendeletlen hozzárendelések fordulhatnak elő néhány esetben:

- Ha létrehoztunk egy feladatot, de még nem adták hozzá senkihez a csapat tagjaihoz, akkor mindig hozzárendelés nélküli hozzárendelést hoznak létre. 
- Ha egy feladat összes megbízottját eltávolítják, akkor hozzárendelés nélküli hozzárendelést hoz létre a feladathoz.

## <a name="scheduling-fields-on-the-project-task-entity"></a>A mezők ütemezése a Project Task entitáson

Az **msdyn\_projecttask** entitás mezői elavultak vagy átkerültek az **msdyn\_resourceassignment** entitásba, vagy most hivatkoznak ezekre a **msdyn\_projectteam** entitásból (**Project Team Member**).

| Elavult mező az msdyn\_projecttaskban (Project Task) | Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés) | Megjegyzés |
|---|---|---|
| msdyn\_assignedresources | Nincs | |
| msdyn\_assignedteammembers | Nincs | |
| msdyn\_numberofresources | Nincs | |
| msdyn\_scheduledhours | Nincs | |
| msdyn\_effortcontour | msdyn\_plannedwork | A mezőben tárolt JavaScript Object Notation (JSON) adatszerkezet formátuma megváltozott. |

## <a name="schedule-contour"></a>Ütemezéskontúr

Az ütemezéskontúr van tárolva a **Tervezett munka** mezőben (**msdyn\_plannedwork**) az egyes **Erőforrás-hozzárendelés** egységekben (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktúra

Az ütemezési kontúr új struktúrája rugalmas időszeletekből áll, amelyeket az ütemterv minden napjára meghatároznak. Minden egyes szeletnek a következő tulajdonságai vannak:

- **Kezdés** - megkezdődik a munkaidő a nap szerint a projekt naptár.
- **Vége** - A napi munkaidő vége a projektnaptár szerint.
- **Órák** - A napra kijelölt órák száma.

**Példa**

Ez a példa egy olyan projektnaptárt használ, ahol a munkanap 9:00 és 17:00 között van az UTC-8 időzónában.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatikus ütemezés és kézi ütemezés

Ha egy feladat automatikus ütemezése van, az órák előre vannak töltve, és a feladat időtartama csökkenhet.

**Példa**

A következő feladat automatikusan ütemeződik 18 órára három nap alatt (2018. december 3., 2018. december 5.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Ha egy feladatot manuálisan ütemeznek, akkor az órák egyenletesen oszlanak meg az összes dátumra.

**Példa**

A következő feladatot kézzel, 18 órás időtartamra tervezzük három nap alatt (2018. december 3., 2018. december 5.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Hozzárendelési egység

A hozzárendelési egység elavult a PSA 3.x-ben. A feladat elvégzésének órái napi módon egyenlően oszlanak meg az összes hozzárendelt erőforrás között.

**Példa**

Ebben a példában a feladatot két erőforráshoz rendelik, és automatikusan ütemezik 36 órára három nap alatt (2018. december 3-tól 2018. december 5-ig).

- 1. feladat:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 2. feladat:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Árképzési dimenziók

A PSA 3.x alkalmazásban az erőforrás-specifikus árazási dimenziós mezőket (például **Szerep** és **Szervezeti egység**) eltávolították a **msdyn\_projecttask** entitásból. Ezek a mezők előhívhatók a megfelelő projekt csapat tagjából (**msdyn\_projectteam**) a erőforrás hozzárendelés (**msdyn\_resourceassignment**), amikor a projekt becslések keletkeznek. Egy új mező, az **msdyn\_organizationalunit** került hozzáadásra az **msdyn\_projectteam** entitáshoz.

| Elavult mező az msdyn\_projecttaskban (Project Task) | A helyette használt msdyn\_projectteam (Project Team Member) |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontúrok

Az árazási és becslési kontúrmezők elavultak az **msdyn\_projecttask** entitáson. Áthelyezték őket az **msdyn\_resourceassignment** entitásba.

| Elavult mező az msdyn\_projecttaskban (Project Task) | Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

A következő mezők kerültek hozzáadásra az **msdyn\_resourceassignment** entitáshoz:

* msdyn\_plannedcost
* msdyn\_plannedsales

A tervezett, a tényleges és a fennmaradó költségek és az értékesítés alábbi mezői nem változnak az **msdyn\_projecttask** entitáson:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
