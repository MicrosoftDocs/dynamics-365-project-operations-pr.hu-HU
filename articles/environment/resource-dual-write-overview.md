---
title: Project Operations kettős írás integrálása
description: Ez a cikk áttekintést nyújt a Project Operations kettős írású integrációjáról.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927975"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations kettős írás integrálásának áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Project Operations [kettős írási képességekkel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) szinkronizálja az adatokat az adatok között Microsoft Dataverse és Dynamics 365 Finance.

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
