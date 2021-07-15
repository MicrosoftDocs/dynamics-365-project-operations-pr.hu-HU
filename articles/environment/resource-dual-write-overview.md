---
title: Project Operations kettős írás integrálása
description: Ez a témakör áttekintést nyújt a Project Operations kettős írású integrációjáról.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368434"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations kettős írás integrálásának áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Project Operations [kettős írási képességeket](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) alkalmaz az adatok szinkronizálására a(z) Microsoft Dataverse és a(z) Dynamics 365 Finance felületen.

Az alábbi ábra azt mutatja be, hogyan szinkronizálják az adatokat a(z) Dataverse és a pénzügyek közötti integráció részeként.

![Project Operations adatáramlásainak áttekintése](./media/ProjectOperationsFlows.jpg)

A(z) Dataverse felületen futó Project Operations modern felhasználói felületet (UI) és egyszerű, kód nélküli/alacsony kódú bővíthetőséget biztosít a(z) Power Platform képességek használatával. A projektmenedzserek, az erőforrás-kezelők, a projektcsapat tagjai és más front-office dolgozók a(z) Dataverse felületen végzik Project Operations-tevékenységeiket.

A Project Operations in Finance projektkönyvelési és bevételelismerési támogatást nyújt. A Project Operations a pénzügyi keretrendszerhez csatlakozik a forgalmi adó kiszámításához, a valutaárfolyamokhoz, a pénzügyi dimenzió jelentéséhez és így tovább. A Projekt könyvelői tapasztalatai többnyire a pénzügyeken alapulnak.

A Project Operations integráció a következő komponensintegrációból áll:


- [Project Operations telepítése és a konfigurációs adatok integrációja](resource-dual-write-setup-integration.md) 
- [Projektbecslések és tényleges adatok integrációja](resource-dual-write-estimates-actuals.md)
- [Projektszámlák](resource-dual-write-project-invoice.md)
- [Költségkezelés](resource-dual-write-expense.md)
- [Szállítói számla](resource-dual-write-vendor-invoice.md)
