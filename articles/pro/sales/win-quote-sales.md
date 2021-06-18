---
title: Árajánlat lezárása - Lite
description: Ez a témakör az árajánlatok Project Operationsben való lezárásáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994139"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="e0564-103">Árajánlat lezárása - Lite</span><span class="sxs-lookup"><span data-stu-id="e0564-103">Close a quote - lite</span></span>

<span data-ttu-id="e0564-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="e0564-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e0564-105">A projektárajánlat megnyertként vagy elvesztettként zárható le.</span><span class="sxs-lookup"><span data-stu-id="e0564-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="e0564-106">A tervezet ajánlatok azért zárhatóak le, mert a Microsoft Dynamics 365 Project Operations nem támogatja az ajánlatok aktiválása és átdolgozása műveleteket.</span><span class="sxs-lookup"><span data-stu-id="e0564-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="e0564-107">Árajánlat lezárása megnyertként</span><span class="sxs-lookup"><span data-stu-id="e0564-107">Close a quote as Won</span></span>

<span data-ttu-id="e0564-108">Ha Megnyertként zár le egy projektajánlatot, akkor az állapota Lezárva, és az állapot oka Megnyert lesz.</span><span class="sxs-lookup"><span data-stu-id="e0564-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="e0564-109">Az árajánlatok lezárása csak olvashatóvá teszi a projektárajánlatot, és az összes árajánlati információval létrehozza a projektszerződés vázlatát.</span><span class="sxs-lookup"><span data-stu-id="e0564-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="e0564-110">Mivel a lezárt ajánlat nem nyitható meg újra, a megerősítő párbeszédpanel fogja megerősíteni a változtatásokat.</span><span class="sxs-lookup"><span data-stu-id="e0564-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e0564-111">Ha az árajánlat egy lehetőséghez van csatolva, akkor a lehetőségen szereplő bármely más projektárajánlat automatikusan lezáródik elveszítettként.</span><span class="sxs-lookup"><span data-stu-id="e0564-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="e0564-112">Az árajánlat megnyertként történő lezárásának pénzügyi hatása</span><span class="sxs-lookup"><span data-stu-id="e0564-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="e0564-113">Ha egy projektre vonatkozó tényadatokat a tervezet ajánlatához csatolja, csak az idő- vagy pénzköltséget rögzíti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="e0564-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="e0564-114">Miután egy árajánlatot megnyertként lezárnak, az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újrabontja a költségeket.</span><span class="sxs-lookup"><span data-stu-id="e0564-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="e0564-115">Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel ezeket a tényleges költségértékeket.</span><span class="sxs-lookup"><span data-stu-id="e0564-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="e0564-116">Ha a költség tényadatai idő- és anyagszerződéssorra hivatkoznak, a rendszer a megfelelő számlázatlan értékesítési tényadatokat hozza létre az ajánlat lezáráskor és a projektszerződés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="e0564-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="e0564-117">Ha a költség tényadatai egy rögzített árú szerződéssorra hivatkoznak, az alkalmazás leállítja a projektszerződés ügyfeleire vonatkozó számlázási szabályokon alapuló költségtényadatok újbóli feldolgozását.</span><span class="sxs-lookup"><span data-stu-id="e0564-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="e0564-118">Árajánlat lezárása elvesztettként:</span><span class="sxs-lookup"><span data-stu-id="e0564-118">Closing a quote as lost:</span></span>

<span data-ttu-id="e0564-119">Ha Elvesztettként zár le egy projektajánlatot, akkor az állapota Lezárva, és az állapot oka Elvesztett lesz.</span><span class="sxs-lookup"><span data-stu-id="e0564-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="e0564-120">Az ajánlat lezárása írásvédetté teszi a projektárajánlatot.</span><span class="sxs-lookup"><span data-stu-id="e0564-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="e0564-121">Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e0564-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e0564-122">Ha az Elvesztettként lezárt projektajánlat hivatkozik valamelyik sorában lévő projektre, akkor az adott projekt Lezártként is meg lesz jelölve.</span><span class="sxs-lookup"><span data-stu-id="e0564-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="e0564-123">Az ettől a naptól a függőben lévő összes erőforrás-foglalás visszavonásra kerül.</span><span class="sxs-lookup"><span data-stu-id="e0564-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="e0564-124">A Project Operationsben az árajánlat megnyertként vagy elvesztettként való lezárása nem befolyásolja a lehetőség állapotát, amely mindaddig nyitva marad, amíg manuálisan le nem zárja.</span><span class="sxs-lookup"><span data-stu-id="e0564-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]