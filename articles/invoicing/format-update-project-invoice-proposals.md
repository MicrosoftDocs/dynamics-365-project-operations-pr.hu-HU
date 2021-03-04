---
title: Projekt számlaajánlatok kezelése
description: A témakör az ügyfél felé irányuló számlák Project Operations szolgáltatással való feldolgozását részletezi az erőforrás/nem készletezett anyagokon alapuló forgatókönyvekhez.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089254"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="1471f-103">Projekt számlaajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="1471f-103">Manage project invoice proposals</span></span>

<span data-ttu-id="1471f-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="1471f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1471f-105">A projekt számlajavaslatait feldolgozhatja a számlázási osztály, ha teljesül a következő két feltétel:</span><span class="sxs-lookup"><span data-stu-id="1471f-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="1471f-106">A projektmenedzser jóváhagyja a proforma számlát a Microsoft Dataverse-ben.</span><span class="sxs-lookup"><span data-stu-id="1471f-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="1471f-107">A proforma számlán szereplő minden időre és anyagra vonatkozó számlázatlan értékesítési tranzakciók szerepet azon a proforma számlán, amelyet a Dynamics 365 **Project Operations integrációs** naplója segítségével tettek közzé.</span><span class="sxs-lookup"><span data-stu-id="1471f-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="1471f-108">A következő lépésekkel teljesítsen egy projekt számlajavaslatot a Dynamics 365 Finance-ben.</span><span class="sxs-lookup"><span data-stu-id="1471f-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="1471f-109">Tekintse át az időpont- és anyagtranzakciók számlázási adatait, és tegye közzé a **Project Operations integrációs** naplót.</span><span class="sxs-lookup"><span data-stu-id="1471f-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="1471f-110">Tekintse át a rögzített árú számlázási mérföldkövek számlázási adatait.</span><span class="sxs-lookup"><span data-stu-id="1471f-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="1471f-111">Tekintse át és formázza a projektszámlázási javaslatot.</span><span class="sxs-lookup"><span data-stu-id="1471f-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="1471f-112">Tegyen közzé és nyomtasson projektszámlákat.</span><span class="sxs-lookup"><span data-stu-id="1471f-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="1471f-113">Kezelje a számlázási adatokat a Project Operations integrációs naplóban</span><span class="sxs-lookup"><span data-stu-id="1471f-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="1471f-114">A Dataverse-ben lévő projekt tényleges adatait áttekintette és közzétette a Projekt könyvelője a Finance szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="1471f-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="1471f-115">A Project Operations integrációs naplójának használatáról további tájékoztatást az [Integrációs napló a Project Operations-ben](../project-accounting/project-operations-integration-journal.md) részben talál.</span><span class="sxs-lookup"><span data-stu-id="1471f-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="1471f-116">A költség tényleges adatai és a számlázatlan értékesítési tényleges adatai külön sorként kerülnek az integrációs naplóba:</span><span class="sxs-lookup"><span data-stu-id="1471f-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="1471f-117">A projekt Dataverse-ben lévő tényleges költségtranzakciója után a Költség tényleges alapértelmezett adatainak kiszerelési önköltségi ára és összege.</span><span class="sxs-lookup"><span data-stu-id="1471f-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="1471f-118">A Számlázatlan értékesítési tranzakció alapértelmezéseinek egységárai és értékesítési összege a projekt tényleges adataiból, számlázatlan értékesítési tranzakcióiból a Dataverse-ben.</span><span class="sxs-lookup"><span data-stu-id="1471f-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="1471f-119">Számlázási áfa</span><span class="sxs-lookup"><span data-stu-id="1471f-119">Billing sales tax</span></span>

<span data-ttu-id="1471f-120">A számlázás áfaszámítását a **Számlázási áfacsoport** és a **Számlázási cikk áfacsoport** mező kombinációja határozza meg a **Project Operations integrációs** naplósorában egy számlázatlan értékesítési rekordon.</span><span class="sxs-lookup"><span data-stu-id="1471f-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="1471f-121">A rendszer ezeket a mezőértékeket alapértelmezettként adja meg a **Projektmenedzsment és a könyvelési paraméterek** oldal **Pénzügyek** lapján található beállítások alapján.</span><span class="sxs-lookup"><span data-stu-id="1471f-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="1471f-122">A számlázási értékesítési áfacsoport alapértelmezett logikáját az **Értékesítési áfacsoport módszer** határozza meg:</span><span class="sxs-lookup"><span data-stu-id="1471f-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="1471f-123">**Projekt**: A projekt számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="1471f-124">A projekt alapértelmezett számlázási értékesítési adócsoportját a **Minden projekt** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="1471f-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="1471f-125">**Projektszerződés**: A projektszerződés számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="1471f-126">A projektszerződés alapértelmezett számlázási értékesítési adócsoportját a **Minden projektszerződés** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="1471f-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="1471f-127">**Ügyfél**: Az ügyfél számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="1471f-128">**Keresés**: A keresés az összes fenti entitásban fog keresni, és kiválasztja az elérhető első értéket.</span><span class="sxs-lookup"><span data-stu-id="1471f-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="1471f-129">A keresés a **Projekt** entitással, majd a **Projekt szerződés** entitással, végül az **Ügyfél** entitással kezdődik.</span><span class="sxs-lookup"><span data-stu-id="1471f-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="1471f-130">A számlázási cikk értékesítési áfacsoport alapértelmezett logikáját a **Cikk értékesítési áfacsoport módszer** határozza meg:</span><span class="sxs-lookup"><span data-stu-id="1471f-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="1471f-131">Az idő, költség és díj tranzakciótípusok esetében a számlázási cikk értékesítési áfacsoportja mindig alapértelmezett a **Projektkategória** entitásból.</span><span class="sxs-lookup"><span data-stu-id="1471f-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="1471f-132">Az anyagtranzakció-típusok esetén a számlázási cikk értékesítési áfacsoport alapértelmezései a **Cikk áfacsoport módszer** **Projektkezelés és könyvelési paraméterek** beállításán alapulnak.</span><span class="sxs-lookup"><span data-stu-id="1471f-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="1471f-133">A cikkszám alapértelmezései a **Kiadott termék** entitás cikk értékesítési áfacsoportját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1471f-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="1471f-134">A kategória alapértelmezései a **Projektkategória** entitás cikk értékesítési áfacsoportját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1471f-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="1471f-135">Pénzügyi dimenziók</span><span class="sxs-lookup"><span data-stu-id="1471f-135">Financial dimensions</span></span>

<span data-ttu-id="1471f-136">A **Project Operations integrációs** naplójában lévő számlázatlan értékesítési rekordok pénzügyi dimenziói alapértelmezetten **Projekt** entitásából származnak.</span><span class="sxs-lookup"><span data-stu-id="1471f-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="1471f-137">A pénzügyi dimenziók az **Összegek elosztása** lehetőség kiválasztásával áttekinthetők és módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="1471f-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="1471f-138">Ha az integráció közzétettele után, de a Proforma számla megerősítését megelőzően módosítania kell a számlázatlan értékesítési rekord pénzügyi dimenzióit, menjen a **Minden projekt** > **Kezelés** > **Közzétett tranzakciók** lehetőséget, majd válassza ki a tranzakciót, és válassza a **Folyamat** > **Könyvelés beállítása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="1471f-139">Átváltási árfolyamok</span><span class="sxs-lookup"><span data-stu-id="1471f-139">Exchange rates</span></span>

<span data-ttu-id="1471f-140">A Dataverse-ben lévő számlázatlan tranzakciós pénznem a Finance-ben tranzakciós pénznemként használatos, és átváltják a vállalat könyvelési pénznemére a Finance-ben meghatározott átváltási árfolyamok használatával.</span><span class="sxs-lookup"><span data-stu-id="1471f-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="1471f-141">A számlázási mérföldkövek pénzügyi attribútumainak kezelése</span><span class="sxs-lookup"><span data-stu-id="1471f-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="1471f-142">A rögzített árú számlázási módot használó projektszerződéssorok számlázása [Rögzített árú mérföldkövek](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) segítségével megy végbe.</span><span class="sxs-lookup"><span data-stu-id="1471f-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="1471f-143">A Projekt könyvelője áttekintheti a Finance számlázási mérföldköveit a **Projektkezelés és könyvelés** > **Minden projekt** > **Kezelés** > **Részletszámlázási tranzakciók** oldalon.</span><span class="sxs-lookup"><span data-stu-id="1471f-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="1471f-144">Számlázási áfa</span><span class="sxs-lookup"><span data-stu-id="1471f-144">Billing sales tax</span></span>

<span data-ttu-id="1471f-145">Az új számlázási mérföldkő Dataverse-ből való létrehozásakor az **Értékesítési áfacsoport** és a **Cikk értékesítési áfacsoport** értékei alapértelmezetten a beállításokból származnak.</span><span class="sxs-lookup"><span data-stu-id="1471f-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="1471f-146">A rendszer ezeket az értékeket alapértelmezettként adja a mezőkhöz a **Projektmenedzsment és a könyvelési paraméterek** oldal **Pénzügy** lapján található beállítások alapján.</span><span class="sxs-lookup"><span data-stu-id="1471f-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="1471f-147">A **Számlázási értékesítési áfacsoport** alapértelmezett logikáját az **Értékesítési áfacsoport módszer** határozza meg:</span><span class="sxs-lookup"><span data-stu-id="1471f-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="1471f-148">**Projekt**: a projekt számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="1471f-149">A projekt alapértelmezett értékesítési adócsoportját a **Minden projekt** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="1471f-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="1471f-150">**Projektszerződés**: a projektszerződés számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="1471f-151">A projektszerződés alapértelmezett számlázási értékesítési adócsoportját a **Minden projektszerződés** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="1471f-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="1471f-152">**Ügyfél**: az ügyfél számlázási áfacsoportja mindig alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="1471f-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="1471f-153">**Keresés**: a keresés a listában szereplő összes entitásban fog keresni, és kiválasztja az elérhető első értéket.</span><span class="sxs-lookup"><span data-stu-id="1471f-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="1471f-154">A keresés a **Projekt** entitással, majd a **Projekt szerződés** entitással, majd az **Ügyfél** entitással kezdődik.</span><span class="sxs-lookup"><span data-stu-id="1471f-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="1471f-155">**A rögzített árú mérföldkő cikk értékesítési áfacsoportja** a **Cikk értékesítési áfacsoport** mező értékének alapértelmezett beállítására használatos.</span><span class="sxs-lookup"><span data-stu-id="1471f-155">**Fixed price milestone item sales tax group** is used to default the value to the **Item sales tax group** field.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="1471f-156">Pénzügyi dimenziók</span><span class="sxs-lookup"><span data-stu-id="1471f-156">Financial dimensions</span></span>

<span data-ttu-id="1471f-157">A rögzített árú számlázási mérföldkövek alapértelmezett pénzügyi dimenziói a Projekt szerződéssorokon vannak beállítva.</span><span class="sxs-lookup"><span data-stu-id="1471f-157">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="1471f-158">Menjen a **Projektszerződések** > **Alapértelmezett könyvelés megjelenítése** lehetőségre, és a **Szerződéssorok** lapon válassza ki az **árszerződéssor** lehetőséget, majd állítsa be az alapértelmezettként használni kívánt pénzügyi dimenzióértékeket.</span><span class="sxs-lookup"><span data-stu-id="1471f-158">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="1471f-159">A Projekt könyvelője a projekt számlajavaslatának létrehozása előtt módosíthatja a számla mérföldköveinek értékesítési áfa- és pénzügyi dimenziókra vonatkozó adatait.</span><span class="sxs-lookup"><span data-stu-id="1471f-159">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="1471f-160">Projekt számlajavaslatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="1471f-160">Create project invoice proposals</span></span>

<span data-ttu-id="1471f-161">A projektszámla javaslatok áttekinthetők a **Projektmenedzsment és könyvelés** modulban, csak menjen a **Projektszámlák** > **Projekt számlajavaslatok** elemre.</span><span class="sxs-lookup"><span data-stu-id="1471f-161">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="1471f-162">A Projekt számlajavaslat fejléce a Pénzügyben jön létre, amikor megerősítették a Proforma számlát a Dataverse-ben.</span><span class="sxs-lookup"><span data-stu-id="1471f-162">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="1471f-163">A könnyebb kezelhetőség érdekében a rendszer a Projekt számla javaslatok számét a Pénzügyben ugyanarra a számra állítja be, mint ami a Proforma számlaazonosító a Dataverse-ben.</span><span class="sxs-lookup"><span data-stu-id="1471f-163">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="1471f-164">Mivel a Proforma számlák nem minden esetben a létrehozás sorrendjében vannak megerősítve, a Projektszámla javaslat Pénzügyben lévő számsorozatának engedélyeznie kell a kisebb és nagyobb számokra való változtatást.</span><span class="sxs-lookup"><span data-stu-id="1471f-164">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="1471f-165">Adja meg a számsorozatokat a következő lépések segítségével:</span><span class="sxs-lookup"><span data-stu-id="1471f-165">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="1471f-166">A Pénzügyben menjen a **Szervezetfelügyelet** > **Sorszámok** > **Sorszámok** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="1471f-166">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="1471f-167">A **Terület** szűrőben válassza a **Projektek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-167">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="1471f-168">A **Referencia** szűrőben válassza a **Számlajavaslat** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-168">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="1471f-169">A **Vállalat** mező segítségével szűrheti az egyes entitásokat a Project Operations Dataverse integrálásának engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="1471f-169">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="1471f-170">Nyissa meg a **Sorszám részletei** lehetőséget, és az **Általános** fülön állítsa be:</span><span class="sxs-lookup"><span data-stu-id="1471f-170">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="1471f-171">**Felhasználói módosítások engedélyezése: Kisebb számra** = **Igen**</span><span class="sxs-lookup"><span data-stu-id="1471f-171">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="1471f-172">**Felhasználói módosítások engedélyezése: Nagyobb számra** = **Igen**</span><span class="sxs-lookup"><span data-stu-id="1471f-172">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="1471f-173">A rendszer hozzáadja a projekt számlajavaslat-sorokat az **Importálás az előkészítési táblából** (**Projektmenedzsment és könyvelés** > **Periodikus** > **Project Operations integráció** > **Importálás az előkészítési táblából**) segítségével.</span><span class="sxs-lookup"><span data-stu-id="1471f-173">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="1471f-174">Ezt a műveletet manuálisan vagy egy periodikus ütemezéssel lehet futtatni.</span><span class="sxs-lookup"><span data-stu-id="1471f-174">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="1471f-175">A rendszer addig nem ad sorokat a számlajavaslat-dokumentumhoz, amíg az összes sor készen nem áll a számlázásra.</span><span class="sxs-lookup"><span data-stu-id="1471f-175">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="1471f-176">Az időpont- és anyagtranzakciók csak akkor lesznek készen a számlázásra, ha a **Project Operations integráció** segítségével közzéteszik őket.</span><span class="sxs-lookup"><span data-stu-id="1471f-176">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="1471f-177">Számlázási javaslatok formázása és nyomtatása</span><span class="sxs-lookup"><span data-stu-id="1471f-177">Format and print invoice proposals</span></span>

<span data-ttu-id="1471f-178">A Projekt könyvelője testre szabhatja a projekt számláinak nyomtatását a **Számlajavaslatok formázása** lap és a nyomtatáskezelési képességek segítségével.</span><span class="sxs-lookup"><span data-stu-id="1471f-178">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="1471f-179">Számlázási javaslatok formázása</span><span class="sxs-lookup"><span data-stu-id="1471f-179">Format invoice proposals</span></span>

<span data-ttu-id="1471f-180">A **Számlajavaslatok formázása** lapon az egyéni csoportosítási tranzakciók megjeleníthetőek az ügyfél projektszámláján.</span><span class="sxs-lookup"><span data-stu-id="1471f-180">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="1471f-181">A **Projekt számlajavaslat** lapon válassza a **Nyomtatás** > **Számlajavaslat formázása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-181">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="1471f-182">Válassza az **Új** lehetőséget, ha új csoportosítást szeretne létrehozni a Projektszámla nyomtatásához.</span><span class="sxs-lookup"><span data-stu-id="1471f-182">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="1471f-183">A **Részletek/Összegzés** mezőben adja meg a csoportosítás lehetőségeit:</span><span class="sxs-lookup"><span data-stu-id="1471f-183">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="1471f-184">Válassza a **Részletek** lehetőséget az ügyfélszámla tranzakciórészleteinek nyomtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1471f-184">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="1471f-185">Válassza az **Összegzés** lehetőséget az ügyfélszámla tranzakcióösszegzésének nyomtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1471f-185">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="1471f-186">A **Számlajavaslat formázása** lapon a **Részletek/Összegzés** mezőben megadott beállítás felülbírálja a **Számlajavaslatok** oldal **Számla formázása** mezőben kijelölt beállítást, és így részletes számlát vagy összesítő számlát nyomtathat.</span><span class="sxs-lookup"><span data-stu-id="1471f-186">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="1471f-187">Válassza ki azokat a tranzakciósorokat, amelyek ezt a szakaszt tartalmazzák a **Rendelkezésre álló tranzakciók** fülön, majd válassza a **Tranzakciók belefoglalása** lehetőséget, és helyezze át azokat a **Kijelölt tranzakciók** fülre.</span><span class="sxs-lookup"><span data-stu-id="1471f-187">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="1471f-188">Válassza a **Felmozgatás** és a **Lemozgatás** lehetőséget a szakaszok sorrendjének módosításhoz.</span><span class="sxs-lookup"><span data-stu-id="1471f-188">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="1471f-189">Válassza a **Nyomtatási kép előnézete** lehetőséget a formázott számla előnézetének megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="1471f-189">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="1471f-190">Nyomtatáskezelés</span><span class="sxs-lookup"><span data-stu-id="1471f-190">Print management</span></span>

<span data-ttu-id="1471f-191">A nyomtatáskezelés különböző jelentésfájlokat használ a nyomtatáshoz, a célpontok megadásához és a számla láblécszövegének testreszabásához.</span><span class="sxs-lookup"><span data-stu-id="1471f-191">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="1471f-192">A nyomtatáskezelés a modul szintjén beállítható, azonban ezek a beállítások felülírhatóak egy adott ügyfél, szerződés vagy számlajavaslat esetében.</span><span class="sxs-lookup"><span data-stu-id="1471f-192">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="1471f-193">Ha hozzá szeretné férni ehhez a funkcióhoz a **Projekt számlajavaslat** oldalon, akkor válassza a **Nyomtatás** > **Nyomtatáskezelés** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-193">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="1471f-194">A nyomtatáskezelési beállítások egy fanézetben jelennek meg, ahol minden csomópontszint megjeleníti a módosítható dokumentumokat.</span><span class="sxs-lookup"><span data-stu-id="1471f-194">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="1471f-195">Az egyéni nyomtatások a modul, az ügyfél, a szerződés vagy a számla ajánlati dokumentumszinten rendelhetők hozzá.</span><span class="sxs-lookup"><span data-stu-id="1471f-195">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="1471f-196">Az eredeti dokumentum nyomtatásának módosításához bontsa ki a kívánt csomópontot, és válassza az **Eredeti cikk** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1471f-196">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="1471f-197">A **Jelentésformátum** mezőben jelölje ki a nyomtatáshoz használni kívánt jelentésformátumot.</span><span class="sxs-lookup"><span data-stu-id="1471f-197">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="1471f-198">Az egyéni jelentésformátumok a [Vállalat dokumentumkezelési keretrendszer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management) segítségével használhatók.</span><span class="sxs-lookup"><span data-stu-id="1471f-198">You can use custom report formats by using [Business Document Management framework](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="1471f-199">Számlázási javaslatok közzététele</span><span class="sxs-lookup"><span data-stu-id="1471f-199">Post invoice proposals</span></span>

<span data-ttu-id="1471f-200">Miután a számlát átnézték és szerkesztték, és megfelelőek a számlajavaslatok sorai, ellenőrizze a számlaösszegeket és az áfát.</span><span class="sxs-lookup"><span data-stu-id="1471f-200">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="1471f-201">A **Részletek** csoportban válassza az **Összesítések**, majd a **Közzététel** lehetőséget a számla közzétételéhez.</span><span class="sxs-lookup"><span data-stu-id="1471f-201">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="1471f-202">Ha meg szeretné tekinteni a számlát a közzététel előtt, akkor törölje a jelölést a **Közzététel** jelölőnégyzetből.</span><span class="sxs-lookup"><span data-stu-id="1471f-202">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="1471f-203">A **Pro forma** szöveg rá lesz nyomtatva a számlára, ez jelzi, hogy ez egy sablonszámla.</span><span class="sxs-lookup"><span data-stu-id="1471f-203">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="1471f-204">A számla nyomtatása előtt jelölje be a **Számla nyomtatása** jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="1471f-204">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="1471f-205">A **Számlajavaslat** lap mellett a számlajavaslatokat a periodikus feladat, a **Számlajavaslatok közzététele** futtatásával is közzéteheti.</span><span class="sxs-lookup"><span data-stu-id="1471f-205">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="1471f-206">A feladat kereséséhez menjen a **Projektkezelés és a könyvelés** > **Periodikus** > **Projektszámlák** > **Projektjavaslatok közzététele** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="1471f-206">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="1471f-207">Ez az oldal megjeleníti a közzétételre kész összes számlajavaslatot.</span><span class="sxs-lookup"><span data-stu-id="1471f-207">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="1471f-208">A **Köteg** lehetőség kiválasztásával ütemezheti is a számlajavaslatok közzétételét.</span><span class="sxs-lookup"><span data-stu-id="1471f-208">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="1471f-209">Állítsa a **Kötegfeldolgozás paraméter** lehetőséget **Igen** értékre, és állítsa be a kötegfeldolgozás ismétlődését az **Ismétlődés** lehetőség kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="1471f-209">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>