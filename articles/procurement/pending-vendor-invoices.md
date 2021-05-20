---
title: Nem készleten lévő anyagok beszerzése függőben lévő szállítói számla alapján
description: Ez témakör ismerteti, hogyan lehet rögzíteni a függőben lévő szállítói számlákat.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880652"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="3922c-103">Nem készleten lévő anyagok beszerzése függőben lévő szállítói számla alapján</span><span class="sxs-lookup"><span data-stu-id="3922c-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="3922c-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="3922c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3922c-105">Amikor egy vállalat nem készleten lévő anyagokat szerez egy projekthez, a költségek azonnal rögzítve lesznek a projekten belül.</span><span class="sxs-lookup"><span data-stu-id="3922c-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="3922c-106">A Contoso Robotics US például egy berendezésfelújítási projektjét hajtják végre, és szoftverlicencekre van szüksége.</span><span class="sxs-lookup"><span data-stu-id="3922c-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="3922c-107">Ezeket a licenceket egy harmadik fél szállítótól szerzik be.</span><span class="sxs-lookup"><span data-stu-id="3922c-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="3922c-108">A(z) Dynamics 365 Finance használata esetén a kinnlevőségek számlák könyvelője rögzíti a függőben lévő szállítói számla dokumentumát, és a licencköltségeket közvetlenül a berendezésfelújítási projekthez rendeli.</span><span class="sxs-lookup"><span data-stu-id="3922c-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3922c-109">Mielőtt a jelen témakör leírt funkciókat használod, tekintsd át és alkalmazd a szükséges konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="3922c-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="3922c-110">További információkért lásd: [Nem raktározott anyagok és függőben lévő szállítói számlák engedélyezése](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="3922c-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="3922c-111">Projekthez kapcsolódó, függőben lévő szállítói számla kiküldése</span><span class="sxs-lookup"><span data-stu-id="3922c-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="3922c-112">A függőben lévő szállítói számlák a **Függőben lévő szállítói számlák** oldalon (**Kötelezettségek** > **Számlák** > **Függőben lévő szállítói számlák**) rögzíthetők.</span><span class="sxs-lookup"><span data-stu-id="3922c-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="3922c-113">A következő lépésekkel tegye közzé a projekttel kapcsolatos, függőben lévő szállítói számlát:</span><span class="sxs-lookup"><span data-stu-id="3922c-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="3922c-114">Lépjen a **Kötelezettségek** > **Számlák** pontra, és válassza az **Új** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3922c-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="3922c-115">A **Számla** mezőben jelöljön ki egy szállítót, a **Szám** mezőben pedig adja meg a szállítói számla azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="3922c-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="3922c-116">Vegyen fel egy sort a szállító számlájához, és a **Cikkszám** mezőben jelölje ki a szállítótól megvásárolt, nem készleten kívüli tételt.</span><span class="sxs-lookup"><span data-stu-id="3922c-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="3922c-117">A szállító számlasorai, amelyek valamely beszerzési kategórián alapulnak, nem rögzíthetők a projekthez.</span><span class="sxs-lookup"><span data-stu-id="3922c-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="3922c-118">Adja hozzá a megvásárolt mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="3922c-118">Add the quantity purchased.</span></span> <span data-ttu-id="3922c-119">A rendszer a nem készleten alapuló cikkárkonfiguráció alapján kitölti az egységárat.</span><span class="sxs-lookup"><span data-stu-id="3922c-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="3922c-120">Ellenőrizze a sorban a teljes összeget és az egyéb szükséges adatokat.</span><span class="sxs-lookup"><span data-stu-id="3922c-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="3922c-121">A sor részleteiben a **Projekt** lapon jelölje ki annak a projektnek az azonosítóját, amelybe ezt az elemet rögzíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="3922c-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="3922c-122">Tetszés szerint kiválaszthatja a tevékenység számát, és frissítheti a projektkategóriát és a sortulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="3922c-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="3922c-123">Függőben lévő szállítói számla kibocsátása.</span><span class="sxs-lookup"><span data-stu-id="3922c-123">Post pending vendor invoice.</span></span> <span data-ttu-id="3922c-124">A számla kibocsátásakor a rendszer a következő bejegyzéseket rögzíti:</span><span class="sxs-lookup"><span data-stu-id="3922c-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="3922c-125">A szállító egyenlege.</span><span class="sxs-lookup"><span data-stu-id="3922c-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="3922c-126">Az áfa összege.</span><span class="sxs-lookup"><span data-stu-id="3922c-126">The sales tax amount.</span></span>
    - <span data-ttu-id="3922c-127">A projekttel szembeni költséget a rendszer a beszerzési integrációs számlához rögzíti.</span><span class="sxs-lookup"><span data-stu-id="3922c-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="3922c-128">A projekt aktuális tranzakciója itt: Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3922c-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="3922c-129">A tranzakció további feldolgozása a [Project Operations Integration napló](../project-accounting/project-operations-integration-journal.md) segítségével történik.</span><span class="sxs-lookup"><span data-stu-id="3922c-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="3922c-130">Ennek a naplónak a közzétételével az összeg a beszerzési integrációs számlából a projektköltség-számlába kerül át.</span><span class="sxs-lookup"><span data-stu-id="3922c-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
