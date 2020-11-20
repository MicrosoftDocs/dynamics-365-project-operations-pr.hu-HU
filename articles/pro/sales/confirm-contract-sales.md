---
title: Projektszerződés jóváhagyása
description: Ez a témakör a szerződések Project Operations alkalmazásban való megerősítéséről nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128286"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="bd47a-103">Projektszerződés jóváhagyása</span><span class="sxs-lookup"><span data-stu-id="bd47a-103">Confirm a project contract</span></span>

<span data-ttu-id="bd47a-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="bd47a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd47a-105">A Dynamics 365 Project Operations alkalmazásban a projektben szereplő szerződések a **Megerősített** okkal aktívak, illetve az **Elveszett** okkal lezártak lehetnek.</span><span class="sxs-lookup"><span data-stu-id="bd47a-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="bd47a-106">A project-szerződések jóváhagyása esetén az állapot-frissítések **Vázlat** értékről **Aktív** értékre módosul az állapot oka pedig **Megerősítve**.</span><span class="sxs-lookup"><span data-stu-id="bd47a-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="bd47a-107">Aktív vagy lezárt szerződés nem módosítható és nem nyitható meg újra.</span><span class="sxs-lookup"><span data-stu-id="bd47a-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="bd47a-108">Egy projektszerződés megerősítésének pénzügyi hatása</span><span class="sxs-lookup"><span data-stu-id="bd47a-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="bd47a-109">A projektszerződés megerősítését követően az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újraszámítja a költségeket.</span><span class="sxs-lookup"><span data-stu-id="bd47a-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="bd47a-110">Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel az új aktuális költségeket.</span><span class="sxs-lookup"><span data-stu-id="bd47a-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="bd47a-111">Ha a tényleges költségek egy Idő és Anyag szerződéssorra hivatkoznak, akkor az alkalmazás automatikusan újra létrehozza a megfelelő, nem számlázott tényleges értékesítéseket.</span><span class="sxs-lookup"><span data-stu-id="bd47a-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="bd47a-112">Ha a tényleges költség egy rögzített árú szerződéssora hivatkozik, akkor az alkalmazás leállítja a tényleges költségek újrafeldolgozását.</span><span class="sxs-lookup"><span data-stu-id="bd47a-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="bd47a-113">A nem meghaladandó korlátok, számlázhatóság beállítása és az árképzés és költségek a tényadatokon értékelve lesznek, majd frissítve a megerősítési folyamat részeként.</span><span class="sxs-lookup"><span data-stu-id="bd47a-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="bd47a-114">Projektszerződés lezárása befejezettként</span><span class="sxs-lookup"><span data-stu-id="bd47a-114">Close a project contract as lost</span></span>

<span data-ttu-id="bd47a-115">Ha elveszettként zár le egy projektszerződést, a szerződés állapota **Lezárva** értékre módosul, és a állapot oka **Elveszett** lesz.</span><span class="sxs-lookup"><span data-stu-id="bd47a-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="bd47a-116">A projekt szerződés írásvédett lesz.</span><span class="sxs-lookup"><span data-stu-id="bd47a-116">The project contract becomes read-only.</span></span> <span data-ttu-id="bd47a-117">Egymegerősítő párbeszédpanel jelenik meg a változtatások végrehajtása előtt, mert a lezárt projektek nem nyithatók meg újra.</span><span class="sxs-lookup"><span data-stu-id="bd47a-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="bd47a-118">Ha az elveszettként lezárt projektszerződés a soraiban egy projektre hivatkozik, akkor azt a projektet is lezártként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="bd47a-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="bd47a-119">Az ettől a naptól a függőben lévő összes erőforrás-foglalás visszavonásra kerül.</span><span class="sxs-lookup"><span data-stu-id="bd47a-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="bd47a-120">A program sztornírozza a szerződésben szereplő, még nem számlázott tényleges értékesítéseket.</span><span class="sxs-lookup"><span data-stu-id="bd47a-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="bd47a-121">A Dynamics 365 Project Operations alkalmazásban a projektszerződések elveszettként való lezárása nem befolyásolja a hozzárendelt lehetőség állapotát.</span><span class="sxs-lookup"><span data-stu-id="bd47a-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="bd47a-122">A lehetőség nyitva marad, és kézzel kell le zárni.</span><span class="sxs-lookup"><span data-stu-id="bd47a-122">The opportunity will remain open and must be manually closed.</span></span>
