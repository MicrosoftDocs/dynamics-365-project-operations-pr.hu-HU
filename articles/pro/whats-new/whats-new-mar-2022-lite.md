---
title: Újdonságok – 2022. március – Project Operations Lite központi telepítés
description: Ez a cikk a Project Operations lite telepítésének 2022. márciusi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
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

Ez a cikk a Microsoft Dynamics 365 Project Operations következő összetevőire és verzióira vonatkozik:

- Project Operations egy Dataverse környezeti verzióban 4.30.0.99

## <a name="features-included-in-this-release"></a>Az ebben a kiadásban elérhető funkciók

- Alvállalkozói szerződés: Szállítói számla létrehozása és egyeztetési élménye

## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Idő és költség | 2388011 | Elutasító megjegyzések megjelenítése az időbejelentőknek a tömeges jóváhagyás során. |
| Projekttervezés és nyomon követés | 2495294 | A projekt részletei nem szerkeszthetők a **Tevékenység részletei** lapon. |
| Számlázás és árképzés | 2499605 | Az árajánlat mérföldkövekből létrehozott szerződéses mérföldkövek helytelenül írásvédettként vannak megjelölve. |
| Projekttervezés és nyomon követés | 2506050 | A műveletkészlet egy órán át függőben marad, ha nincs mentendő módosítás. A készletet ezután tévesen Sikertelenként **jelölik** meg, míg azonnal be kell fejezni. |
| Számlázás és árképzés | 2507401 | Az alapértelmezett szerződéses egységek helytelenül vannak megadva a projektekben a helytelen gyorsítótárazás miatt. |
| Számlázás és árképzés | 2541660 | **Az értékesítési rendelések létrehozásának ellenőrzése** kettős írásban csak projektalapú rendelésekre vonatkozhat. |
| Számlázás és árképzés | 2552745 | Az adó nem oszlik meg azon ügyfelek között, akik megosztott számlázási szabályokat állítottak be. |
| Számlázás és árképzés | 2558859 | Továbbfejlesztett hibaüzenetek a díjszabási dimenziók beállításakor. |
| Számlázás és árképzés | 2558933 | **A Project Estimates-ből** való importálás sikertelen lesz, ha **az msdyn\_ projektet** tarifadimenzióként adja hozzá. |
| Számlázás és árképzés | 2559101 | A projektparaméterek törlése nincs letiltva, és problémákat okoz. |
|   Lehetőségkezelés | 2570390 | A kettős írású beépülő modul arra kényszeríti a fióktípust az árajánlatokra, megrendelésekre és lehetőségekre, hogy Ügyfél **legyen**, még akkor is, ha az adott fióktípus nem megfelelő. |
| Számlázás és árképzés | 2586097 | A felosztott számlázott költség tényleges adatai nem lesznek visszafordítva, amikor egy projektet eltávolítanak egy projektszerződés-sorból. |
| Számlázás és árképzés | 2589619 | A beírt anyagra kivetett adót a számlázatlan értékesítési tényleges adatokra és a számlára terjesztik. |
|   Lehetőségkezelés | 2594015 | Az árajánlat nem zárható le a megnyert módon azoknál az ügyfeleknél, akik net60 **fizetési feltételekkel rendelkeznek**. |
| Projekttervezés és nyomon követés | 2595841 | A Webes Projectben a felhasználók hibaüzenetet kapnak egy hiányzó **msdyn\_ actualstart** értékről, amikor új erőforrás-kérést hoznak létre. |
| Idő és költség | 2602511 | Az **Időbejegyzések Elutasítva mezője** a Rendszer **jelenik meg** a megnevezett felhasználó helyett elutasítóként. |
| Idő és költség | 2602528 | A projektjóváhagyók jóváhagyhatják az olyan projektek idejét, amelyek nem szerepelnek jóváhagyóként. |
| Számlázás és árképzés | 2608550 | A helyesbítő számla akkor is visszaigazolható, ha az eredeti nem változik. |

## <a name="removed-and-deprecated-features"></a>Eltávolított és elavult funkciók

A [Project Operations](../../whats-new/removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiról szóló cikk azokat a funkciókat ismerteti, amelyek eltávolításra vagy elavultak Dynamics 365 Project Operations.

- Az eltávolított funkciók a továbbiakban nem érhetőek el a termékben.
- Az elavult funkciók nincsenek aktív fejlesztés alatt, és előfordulhat, hogy egy későbbi frissítés során el lesznek távolítva.

Az elalvasztási bejelentés 12 hónappal azelőtt jelenik meg a [Project Operations](../../whats-new/removed-depreciated-features-project.md) eltávolított vagy elavult funkcióiban, hogy bármely funkciót eltávolítana a termékből.
