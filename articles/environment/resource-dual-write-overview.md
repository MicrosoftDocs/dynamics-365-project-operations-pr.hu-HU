---
title: Project Operations kettős írás integrálása
description: Ez a témakör áttekintést nyújt a Project Operations kettős írású integrációjáról.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582759"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations kettős írás integrálásának áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Project Operations kettős írási képességeket [használ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) az adatok szinkronizálásához az adatok Dynamics 365 Finance Microsoft Dataverse között és Dynamics 365 Finance között.

Az alábbi ábra azt mutatja be, hogyan szinkronizálják az adatokat a(z) Dataverse és a pénzügyek közötti integráció részeként.

![Project Operations adatáramlásainak áttekintése.](./media/ProjectOperationsFlows.jpg)

A(z) Dataverse felületen futó Project Operations modern felhasználói felületet (UI) és egyszerű, kód nélküli/alacsony kódú bővíthetőséget biztosít a(z) Power Platform képességek használatával. A projektmenedzserek, az erőforrás-kezelők, a projektcsapat tagjai és más front-office dolgozók a(z) Dataverse felületen végzik Project Operations-tevékenységeiket.

A Project Operations in Finance projektkönyvelési és bevételelismerési támogatást nyújt. A Project Operations a pénzügyi keretrendszerhez csatlakozik a forgalmi adó kiszámításához, a valutaárfolyamokhoz, a pénzügyi dimenzió jelentéséhez és így tovább. A Projekt könyvelői tapasztalatai többnyire a pénzügyeken alapulnak.

A Project Operations integráció a következő komponensintegrációból áll:


- [Project Operations telepítése és a konfigurációs adatok integrációja](resource-dual-write-setup-integration.md) 
- [Projektbecslések és tényleges adatok integrációja](resource-dual-write-estimates-actuals.md)
- [Projektszámlák](resource-dual-write-project-invoice.md)
- [Költségkezelés](resource-dual-write-expense.md)
- [Szállítói számla](resource-dual-write-vendor-invoice.md)
