---
title: Project Operations kettős írás integrálása
description: Ez a témakör áttekintést nyújt a Project Operations kettős írású integrációjáról.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955661"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="2eddc-103">Project Operations kettős írás integrálásának áttekintése</span><span class="sxs-lookup"><span data-stu-id="2eddc-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="2eddc-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="2eddc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2eddc-105">A Project Operations [kettős írási képességeket](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) alkalmaz az adatok szinkronizálására a(z) Microsoft Dataverse és a(z) Dynamics 365 Finance felületen.</span><span class="sxs-lookup"><span data-stu-id="2eddc-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="2eddc-106">Az alábbi ábra azt mutatja be, hogyan szinkronizálják az adatokat a(z) Dataverse és a pénzügyek közötti integráció részeként.</span><span class="sxs-lookup"><span data-stu-id="2eddc-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations adatáramlásainak áttekintése](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="2eddc-108">A(z) Dataverse felületen futó Project Operations modern felhasználói felületet (UI) és egyszerű, kód nélküli/alacsony kódú bővíthetőséget biztosít a(z) Power Platform képességek használatával.</span><span class="sxs-lookup"><span data-stu-id="2eddc-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="2eddc-109">A projektmenedzserek, az erőforrás-kezelők, a projektcsapat tagjai és más front-office dolgozók a(z) Dataverse felületen végzik Project Operations-tevékenységeiket.</span><span class="sxs-lookup"><span data-stu-id="2eddc-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="2eddc-110">A Project Operations in Finance projektkönyvelési és bevételelismerési támogatást nyújt.</span><span class="sxs-lookup"><span data-stu-id="2eddc-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="2eddc-111">A Project Operations a pénzügyi keretrendszerhez csatlakozik a forgalmi adó kiszámításához, a valutaárfolyamokhoz, a pénzügyi dimenzió jelentéséhez és így tovább.</span><span class="sxs-lookup"><span data-stu-id="2eddc-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="2eddc-112">A Projekt könyvelői tapasztalatai többnyire a pénzügyeken alapulnak.</span><span class="sxs-lookup"><span data-stu-id="2eddc-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="2eddc-113">A Project Operations integráció a következő komponensintegrációból áll:</span><span class="sxs-lookup"><span data-stu-id="2eddc-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="2eddc-114">Project Operations telepítése és a konfigurációs adatok integrációja</span><span class="sxs-lookup"><span data-stu-id="2eddc-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="2eddc-115">Projektbecslések és tényleges adatok integrációja</span><span class="sxs-lookup"><span data-stu-id="2eddc-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="2eddc-116">Projektszámlák</span><span class="sxs-lookup"><span data-stu-id="2eddc-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="2eddc-117">Költségkezelés</span><span class="sxs-lookup"><span data-stu-id="2eddc-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="2eddc-118">Szállítói számla</span><span class="sxs-lookup"><span data-stu-id="2eddc-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
