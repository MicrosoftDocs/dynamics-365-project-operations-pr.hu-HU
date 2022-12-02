---
title: Újdonságok – 2022. március – Project Operations Lite központi telepítés
description: Ez a cikk a Project Operations lite telepítés 2022. márciusi kiadásában elérhető minőségi frissítésekkel kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934231"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Újdonságok – 2022. március – Project Operations Lite központi telepítés

_Érvényesség: Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.30.0.99 verziójú Dataverse-környezetben

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

- Alvállalkozók : A szállítók számlakészítési és egyeztetési tapasztalatai

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Idő és költség | 2388011. | Elutasítási megjegyzések megjelenítése a tömeges jóváhagyás során az időbejegyzések benyújtóinak. |
| Projekttervezés és nyomon követés | 2495294. | A projekt részletei nem lehetnek szerkeszthetők a **Feladat részletei** oldalon. |
| Számlázás és árképzés | 2499605. | Az árajánlat mérföldköveiből létrehozott szerződés-mérföldkövek nem helytelenül vannak megjelölve írásvédettként megjelölve. |
| Projekttervezés és nyomon követés | 2506050. | A művelethalmaz egy órán át függőben marad, ha a nincs mentendő módosítás. Ezután a halmaz helytelenül a **Sikertelen** értékkel van megjelölve, annak ellenére, hogy azonnal el kellene végezni. |
| Számlázás és árképzés | 2507401. | A helytelen gyorsítótárazás miatt a projektekben helytelenül vannak megadva az alapértelmezett szerződő egységek. |
| Számlázás és árképzés | 2541660. | Az **Értékesítési rendelés létrehozásának ellenőrzése** a kettős írásban csak projektalapú megrendelésekhez kellene vonatkozzon. |
| Számlázás és árképzés | 2552745. | Az adót nem lehet felosztani a felosztott számlázási szabályokat beállító ügyfelek között. |
| Számlázás és árképzés | 2558859. | Továbbfejlesztett hibaüzenetek az árazási dimenziók beállításakor. |
| Számlázás és árképzés | 2558933. | A **Projektbecslésből történő importálás** nem sikerül, ha az **msdyn\_project** árképzési dimenzióként van hozzáadva. |
| Számlázás és árképzés | 2559101. | A projektparaméterek törlését nem blokkolja a rendszer, és ez problémákat okoz. |
|   Lehetőségkezelés | 2570390. | A kettős írású beépülő modul még akkor is kényszeríti a partnertípust az árajánlatokhoz, megrendelésekhez és lehetőségekhez **Ügyfél** legyen, ha a partnertípus nem megfelelő. |
| Számlázás és árképzés | 2586097. | A felosztott, számlázott tényleges költség nem sztornózható, ha egy projektet projektszerződéssorból eltávolítottak. |
| Számlázás és árképzés | 2589619. | A nem katalogizált anyagok adója továbbításra kerül a számlázatlan tényleges értékesítésekre és a számlára. |
|   Lehetőségkezelés | 2594015. | A **Net60** fizetési feltételekkel rendelkező ügyfelek esetében az árajánlat nem zárható le megnyertként. |
| Projekttervezés és nyomon követés | 2595841. | A Project for the Web alkalmazásban a felhasználók hibaüzenetet kapnak arról, hogy hiányzik az **msdyn\_actualstart** entitás, amikor új erőforrás-kérelmet hoznak létre. |
| Idő és költség | 2602511. | Az időbejegyzések **Elutasította** mezője a **Rendszer** értéket jeleníti meg elutasítóként a megnevezett felhasználó helyett. |
| Idő és költség | 2602528. | A projekt jóváhagyója jóváhagyhatja az olyan projektek idejét, amelyeknél nem szerepel jóváhagyóként. |
| Számlázás és árképzés | 2608550. | A helyesbítőszámla még akkor is meg lesz erősítve, ha az eredetin nem történt változtatás. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations eltávolított vagy elavult funkciói](../../whats-new/removed-depreciated-features-project.md) cikk ismerteti azokat a szolgáltatásokat, amelyek el lettek távolítva vagy avultatva lettek a Dynamics 365 Project Operations alkalmazásban.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nem állnak aktív fejlesztés alatt, és előfordulhat, eltávolíthatják őket egy későbbi frissítésben.

Az avultatási közlemény 12 hónappal az előtt jelenik meg a [Project Operations eltávolított vagy elavult funkciói](../../whats-new/removed-depreciated-features-project.md) cikkben, hogy a szolgáltatást eltávolítanák a termékből.
