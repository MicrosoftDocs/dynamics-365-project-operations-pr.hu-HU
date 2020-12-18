---
title: Vállalatközi számlázás áttekintése
description: Ez a témakör információkat és példákat tartalmaz a vállalatközi számlázásról a projektekhez.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595487"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="8a80c-103">Vállalatközi számlázás áttekintése</span><span class="sxs-lookup"><span data-stu-id="8a80c-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="8a80c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="8a80c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8a80c-105">Előfordulhat, hogy a szervezethez több olyan részleg, leányvállalat és más jogi személy tartozik, amelyek termékeket és szolgáltatásokat biztosítanak egymásnak a projektjeihez.</span><span class="sxs-lookup"><span data-stu-id="8a80c-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="8a80c-106">Az a jogi személy, aki a szolgáltatást vagy terméket nyújtja, az úgynevezett *kölcsönadó jogi személy*.</span><span class="sxs-lookup"><span data-stu-id="8a80c-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="8a80c-107">Az a jogi személy, aki a szolgáltatást vagy terméket kapja, az úgynevezett *kölcsönvevő jogi személy*.</span><span class="sxs-lookup"><span data-stu-id="8a80c-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="8a80c-108">A következő ábra egy tipikus forgatókönyvet mutat be, ahol két jogi személy, a Contoso Robotics USA (a kölcsönvevő jogi személy) és a Contoso Robotics UK (a kölcsönvevő jogi személy) erőforrásokat oszt meg az ügyfélnek, a Kalandorboltnak.</span><span class="sxs-lookup"><span data-stu-id="8a80c-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="8a80c-109">Ebben az esetben a Contoso Robotics USA szerződést kötött egy munka szállítására az Adventure Works számára.</span><span class="sxs-lookup"><span data-stu-id="8a80c-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Vállalatközi számlázás](./media/IntercompanyScenario.png) 

<span data-ttu-id="8a80c-111">A Dynamics 365 Project Operations a következő folyamatot használja a vállalatközi tranzakciók feldolgozásához:</span><span class="sxs-lookup"><span data-stu-id="8a80c-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="8a80c-112">A kölcsönadó jogi személy vállalatközi idő- és költségtranzakciói felhasználása költségtranzakciókként úgy, hogy időt és költséget könyvelnek a kölcsönvevő jogi személy projektjeivel szemben.</span><span class="sxs-lookup"><span data-stu-id="8a80c-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="8a80c-113">Az idő-és költség árát a kölcsönadó vállalatnál vannak rögzítve a kölcsönvevő vállalat önköltségi árlistájával.</span><span class="sxs-lookup"><span data-stu-id="8a80c-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="8a80c-114">A vállalatközi számlázatlan értékesítési tranzakciók a kölcsönadó vállalatnál vannak rögzítve a kölcsönvevő vállalat önköltségi árlistájával.</span><span class="sxs-lookup"><span data-stu-id="8a80c-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="8a80c-115">A nem számlázott bevételeket a kölcsönvevő vállalatnál lehet nyilvántartani a projekt szerződés értékesítési árlistája segítségével.</span><span class="sxs-lookup"><span data-stu-id="8a80c-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="8a80c-116">Az ügyfél részére akkor lehet számlázni, ha nem számlázott bevételt rögzítenek.</span><span class="sxs-lookup"><span data-stu-id="8a80c-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="8a80c-117">Az ügyfélnek nem kell megvárnia, amíg a vállalatközi számla feldolgozása befejeződött.</span><span class="sxs-lookup"><span data-stu-id="8a80c-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="8a80c-118">A vállalatközi ügyfélszámlák rendszeresen létrejönnek a kölcsönadó vállalatnál.</span><span class="sxs-lookup"><span data-stu-id="8a80c-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="8a80c-119">A számlák létrehozása manuálisan vagy periodikus automatizált folyamat segítségével történik.</span><span class="sxs-lookup"><span data-stu-id="8a80c-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="8a80c-120">Létrehozható egyetlen számla minden egyes kölcsönvevő jogi személyhez, illetve külön számlák is létrehozhatók projekt szerint.</span><span class="sxs-lookup"><span data-stu-id="8a80c-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="8a80c-121">Amikor a vállalatközi ügyfélszámlát feladják a kölcsönadó jogi személyben, ez ennek megfelelő szállítói számla létrejön a kölcsönvevő jogi személynél.</span><span class="sxs-lookup"><span data-stu-id="8a80c-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="8a80c-122">A függőben lévő szállítói számla költségeit a rendszer a számla könyvelésekor rögzíti a projekt alkönyvébe.</span><span class="sxs-lookup"><span data-stu-id="8a80c-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="8a80c-123">A következő ábra a vállalatközi számlázást mutatja be, ahogy az kapcsolódik könyvelési eseményekhez és a várt feladásokhoz a főkönyvbe.</span><span class="sxs-lookup"><span data-stu-id="8a80c-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Vállalatközi folyamat](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="8a80c-125">További információforrások</span><span class="sxs-lookup"><span data-stu-id="8a80c-125">Additional resources</span></span>

- [<span data-ttu-id="8a80c-126">A vállalatközi számlázás konfigurálása</span><span class="sxs-lookup"><span data-stu-id="8a80c-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="8a80c-127">Vállalatközi tranzakciók rögzítése</span><span class="sxs-lookup"><span data-stu-id="8a80c-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="8a80c-128">Vállalatközi ügyfél- és szállítói számlák létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a80c-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
