---
title: Árajánlatok lezárása
description: Ez a témakör az árajánlatok Project Operationsben való lezárásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078013"
---
# <a name="close-quotes"></a><span data-ttu-id="9771a-103">Árajánlatok lezárása</span><span class="sxs-lookup"><span data-stu-id="9771a-103">Close quotes</span></span> 

<span data-ttu-id="9771a-104">_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_</span><span class="sxs-lookup"><span data-stu-id="9771a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9771a-105">A projektárajánlat megnyertként vagy elvesztettként zárható le.</span><span class="sxs-lookup"><span data-stu-id="9771a-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="9771a-106">Az Aktiválás és Felülvizsgálat funkciók nem támogatottak a Microsoft Dynamics 365 Project Operations árajánlataiban, ezért a árajánlat-tervezetet lezárhatja.</span><span class="sxs-lookup"><span data-stu-id="9771a-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="9771a-107">Árajánlat lezárása megnyertként</span><span class="sxs-lookup"><span data-stu-id="9771a-107">Close a quote as Won</span></span>

<span data-ttu-id="9771a-108">A projektárajánlat megnyertként való lezárása az árajánlat állapotát Lezárt értékkel zárja le, és az állapot oka Megnyert lesz.</span><span class="sxs-lookup"><span data-stu-id="9771a-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="9771a-109">Az árajánlatok lezárása csak olvashatóvá teszi a projektárajánlatot, és az összes árajánlati információval létrehozza a projektszerződés vázlatát.</span><span class="sxs-lookup"><span data-stu-id="9771a-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="9771a-110">Mivel a lezárt árajánlat nem nyitható meg újra, egy megerősítő párbeszédpanel jelenik meg, amely a változtatások végrehajtása előtt megerősítést kér, mivel a lezárt árajánlat nem nyitható meg újra, és a változtatások visszafordíthatatlanok.</span><span class="sxs-lookup"><span data-stu-id="9771a-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="9771a-111">Ha az árajánlat egy lehetőséghez van csatolva, akkor a lehetőségen szereplő bármely más projektárajánlat automatikusan lezáródik elveszítettként.</span><span class="sxs-lookup"><span data-stu-id="9771a-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="9771a-112">Az árajánlat megnyertként történő lezárásának pénzügyi hatása</span><span class="sxs-lookup"><span data-stu-id="9771a-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="9771a-113">Ha a projekthez tényleges időadatok lettek rögzítve, miközben még csatolva van a vázlat árajánlathoz, akkor csak az idő vagy a kiadás költsége kerül rögzítésre.</span><span class="sxs-lookup"><span data-stu-id="9771a-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="9771a-114">Miután egy árajánlatot megnyertként lezárnak, az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újrabontja a költségeket.</span><span class="sxs-lookup"><span data-stu-id="9771a-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="9771a-115">Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel ezeket a tényleges költségértékeket.</span><span class="sxs-lookup"><span data-stu-id="9771a-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="9771a-116">Ha a tényleges költségadatok egy idő-és anyagelszámolású szerződéssorra hivatkoznak, a rendszer automatikusan létrehozza a megfelelő, nem számlázott tényleges értékesítési adatokat az ajánlat lezárásakor és a projektszerződés létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="9771a-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="9771a-117">Ha a tényleges költségadatok rögzített árú szerződéssorra hivatkoznak, akkor az alkalmazás leállítja a tényleges költségadatok feldolgozását a projektszerződés ügyfeleinek felosztott számlázási szabályai alapján.</span><span class="sxs-lookup"><span data-stu-id="9771a-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="9771a-118">Árajánlat lezárása elvesztettként:</span><span class="sxs-lookup"><span data-stu-id="9771a-118">Closing a quote as lost:</span></span>

<span data-ttu-id="9771a-119">A projektárajánlat elvesztettként való lezárása az árajánlat állapotát Lezárt értékre módosítja, és az állapot oka Elvesztett lesz.</span><span class="sxs-lookup"><span data-stu-id="9771a-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="9771a-120">Az ajánlat lezárása írásvédetté teszi a projektárajánlatot.</span><span class="sxs-lookup"><span data-stu-id="9771a-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="9771a-121">Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9771a-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="9771a-122">Ha az elvesztettként lezárt projektárajánlat valamely sorára egy projekt hivatkozik, akkor az a projekt lezártként van megjelölve, és az adott naptól kezdve az összes erőforrás-foglalás visszavonásra kerül.</span><span class="sxs-lookup"><span data-stu-id="9771a-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="9771a-123">A Project Operationsben az árajánlat megnyertként vagy elvesztettként való lezárása nem befolyásolja a lehetőség állapotát, amely mindaddig nyitva marad, amíg manuálisan le nem zárja.</span><span class="sxs-lookup"><span data-stu-id="9771a-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
