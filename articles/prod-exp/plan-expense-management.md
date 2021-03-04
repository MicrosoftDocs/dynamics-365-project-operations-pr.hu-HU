---
title: Költségkezelés konfigurálása
description: Ez a cikk azokat a szempontokat és döntéseket ismerteti, amelyeket a tervezési folyamat során el kell végeznie a Költségkezelés konfigurálása előtt a Microsoft Dynamics 365 Finance szolgáltatásban.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960340"
---
# <a name="configure-expense-management"></a><span data-ttu-id="351dc-103">Költségkezelés konfigurálása</span><span class="sxs-lookup"><span data-stu-id="351dc-103">Configure expense management</span></span>

<span data-ttu-id="351dc-104">Ez a témakör azokat a szempontokat és döntéseket ismerteti, amelyeket a tervezési folyamat során el kell végeznie a Költségkezelés konfigurálása előtt.</span><span class="sxs-lookup"><span data-stu-id="351dc-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="351dc-105">A Költségkezelés során információkat tárolhat a fizetési módszerekről, az utazási igénylésekről, a költségjelentésekről, a házirendekről stb.</span><span class="sxs-lookup"><span data-stu-id="351dc-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="351dc-106">Mivel a Költségkezelésre szolgáló konfiguráció megtervezése során számos döntés a szervezet hierarchiája és pénzügyi struktúrája alapján történik, az adott területek esetén át kell tekintenie tervezési dokumentumokat.</span><span class="sxs-lookup"><span data-stu-id="351dc-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="351dc-107">Vállalatközi kiadások</span><span class="sxs-lookup"><span data-stu-id="351dc-107">Intercompany expenses</span></span>

<span data-ttu-id="351dc-108">A vállalatközi kiadások engedélyezésekor lehetővé teszi, hogy a jogi személyek és alkalmazottak egy másik jogi személy nevében felmerülő költségeket fizessenek, és a szervezeten belül begyűjtsenek egy fizetést a jogi entitásból.</span><span class="sxs-lookup"><span data-stu-id="351dc-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="351dc-109">Például az A jogi személy egy alkalmazottja teljesíti a B jogi személy projektjét, és a projekt az utazáshoz kapcsolódó költségeket vállalja.</span><span class="sxs-lookup"><span data-stu-id="351dc-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="351dc-110">Ha a vállalatközi kiadások engedélyezve vannak, az alkalmazott ezután egy Költségjelentés segítségével benyújthatja a költséget a B jogi entitásnak, és ezt követően a költséget az A jogi entitásnak kell kifizetnie. Ha a szervezetnél nincs több jogi személy, nem kell engedélyeznie a vállalatközi költségeket.</span><span class="sxs-lookup"><span data-stu-id="351dc-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="351dc-111">**Döntés:** Engedélyezni szeretné a vállalatközi költségeket?</span><span class="sxs-lookup"><span data-stu-id="351dc-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="351dc-112">Pénzügyi kezelés</span><span class="sxs-lookup"><span data-stu-id="351dc-112">Financial management</span></span>

<span data-ttu-id="351dc-113">A Költségkezelés szorosan integrálódik a szervezet pénzügyi irányításával.</span><span class="sxs-lookup"><span data-stu-id="351dc-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="351dc-114">A Költségkezelés számos konfigurációja a szervezet pénzügyeit érintő döntéseken alapul majd.</span><span class="sxs-lookup"><span data-stu-id="351dc-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="351dc-115">A következő szakaszok ismertetik a tervezést és döntéseket igénylő különböző területeket a szervezet pénzügyi döntései és a vezető csapatának útmutatása alapján.</span><span class="sxs-lookup"><span data-stu-id="351dc-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="351dc-116">Napidíjak</span><span class="sxs-lookup"><span data-stu-id="351dc-116">Per diems</span></span>

<span data-ttu-id="351dc-117">Meg kell adnia a szervezet által biztosított alkalmazotti napidíjat.</span><span class="sxs-lookup"><span data-stu-id="351dc-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="351dc-118">Mivel a napidíjak általában a költségek, például az étkezés, a szállás és az egyéb járulékos kiadások fedezésére szolgálnak, létrehozhatja a szervezet által kínált napidíjra vonatkozó szabályokat.</span><span class="sxs-lookup"><span data-stu-id="351dc-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="351dc-119">a napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet.</span><span class="sxs-lookup"><span data-stu-id="351dc-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="351dc-120">Amikor napidíjat határoz meg, megadhatja, hogy a napidíj bizonyos százalékát visszatartsák, ha egy dolgozó ingyenes étkezést vagy szolgáltatásokat kap.</span><span class="sxs-lookup"><span data-stu-id="351dc-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="351dc-121">Meghatározhat napidíjszinteket is, hogy beállítsa azt a minimális és maximális óraszámot is, amelyre a napidíj a dolgozó utazása esetében vonatkozhat.</span><span class="sxs-lookup"><span data-stu-id="351dc-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="351dc-122">**Döntés:**</span><span class="sxs-lookup"><span data-stu-id="351dc-122">**Decisions:**</span></span>

- <span data-ttu-id="351dc-123">Alapértelmezett napidíj szabályai az első és az utolsó napra:</span><span class="sxs-lookup"><span data-stu-id="351dc-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="351dc-124">Mi az a minimális óraszám, amelyet egy alkalmazott igényelhet egy napra, és még mindig megkapja a napidíjat?</span><span class="sxs-lookup"><span data-stu-id="351dc-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="351dc-125">Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk étkezésre?</span><span class="sxs-lookup"><span data-stu-id="351dc-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="351dc-126">Ha van csökkentés, mi a csökkentés százalékos aránya?</span><span class="sxs-lookup"><span data-stu-id="351dc-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="351dc-127">Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk szállásra?</span><span class="sxs-lookup"><span data-stu-id="351dc-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="351dc-128">Ha van csökkentés, mi a csökkentés százalékos aránya?</span><span class="sxs-lookup"><span data-stu-id="351dc-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="351dc-129">Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk az egyéb felmerült költségekre?</span><span class="sxs-lookup"><span data-stu-id="351dc-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="351dc-130">Ha van csökkentés, mi a csökkentés százalékos aránya?</span><span class="sxs-lookup"><span data-stu-id="351dc-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="351dc-131">A napidíjra vonatkozó alapértelmezett szabályok:</span><span class="sxs-lookup"><span data-stu-id="351dc-131">Default per diem rules:</span></span>

    - <span data-ttu-id="351dc-132">Van-e százalékos csökkentés a napidíjban az egyes étkezésekre, ha például az étkezés ingyenes?</span><span class="sxs-lookup"><span data-stu-id="351dc-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="351dc-133">Ha van csökkentés, mi a csökkentés százalékos aránya az egyes étkezéseknél?</span><span class="sxs-lookup"><span data-stu-id="351dc-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="351dc-134">Az étkezésre vonatkozó csökkentés naponta, utazásonként vagy az étkezések napi száma alapján számolandó?</span><span class="sxs-lookup"><span data-stu-id="351dc-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="351dc-135">A napidíjban szereplő összegeket a szokásos módon kell lekerekíteni, vagy felkerekíteni?</span><span class="sxs-lookup"><span data-stu-id="351dc-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="351dc-136">A napidíjat 24 órás időszakra vagy naptári napra számítják?</span><span class="sxs-lookup"><span data-stu-id="351dc-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="351dc-137">A helyen alapuló napidíj-szabályok:</span><span class="sxs-lookup"><span data-stu-id="351dc-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="351dc-138">A napidíj aránya a helytől függően változik?</span><span class="sxs-lookup"><span data-stu-id="351dc-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="351dc-139">Milyen helyeket tartalmaz a rendszer?</span><span class="sxs-lookup"><span data-stu-id="351dc-139">What locations are included?</span></span>
    - <span data-ttu-id="351dc-140">Ha a napidíjak a helytől függően változnak, minden egyes helynél a következő típusú kiadások esetében milyen százalékos összeget biztosít a rendszer:</span><span class="sxs-lookup"><span data-stu-id="351dc-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="351dc-141">Étkezések</span><span class="sxs-lookup"><span data-stu-id="351dc-141">Meals</span></span>
        - <span data-ttu-id="351dc-142">Szálloda</span><span class="sxs-lookup"><span data-stu-id="351dc-142">Hotel</span></span>
        - <span data-ttu-id="351dc-143">Egyéb kiadások</span><span class="sxs-lookup"><span data-stu-id="351dc-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="351dc-144">Költségkezelés-naplók és -partnerek</span><span class="sxs-lookup"><span data-stu-id="351dc-144">Expense management journals and accounts</span></span>

<span data-ttu-id="351dc-145">A költségkezeléshez több napló és partner használata szükséges.</span><span class="sxs-lookup"><span data-stu-id="351dc-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="351dc-146">Meg kell határoznia például, hogy ugyanazt a számlát használják-e a készpénzelőlegek és a hitelkártya-jogviták esetében.</span><span class="sxs-lookup"><span data-stu-id="351dc-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="351dc-147">**Döntés:**</span><span class="sxs-lookup"><span data-stu-id="351dc-147">**Decisions:**</span></span>

- <span data-ttu-id="351dc-148">Melyik főkönyvi naplóban szerepelnek a jóváhagyott Költségjelentések?</span><span class="sxs-lookup"><span data-stu-id="351dc-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="351dc-149">Milyen számlát használnak a készpénzelőlegek esetén?</span><span class="sxs-lookup"><span data-stu-id="351dc-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="351dc-150">Azonnal fel kell adni a készpénzelőlegeket?</span><span class="sxs-lookup"><span data-stu-id="351dc-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="351dc-151">Fizetési módok</span><span class="sxs-lookup"><span data-stu-id="351dc-151">Payment methods</span></span>

<span data-ttu-id="351dc-152">Ha lehetővé teszi, hogy az alkalmazottak a vállalat nevében költségeket igényeljenek, meg kell határoznia azokat a fizetési módszereket, amelyeket az alkalmazottak használhatnak.</span><span class="sxs-lookup"><span data-stu-id="351dc-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="351dc-153">Például lehetővé teheti, hogy az alkalmazottak készpénzt vagy vállalati hitelkártyát használjanak.</span><span class="sxs-lookup"><span data-stu-id="351dc-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="351dc-154">Előfordulhat, hogy az alkalmazottak személyes hitelkártyát is használhatnak, majd visszafizetik az alkalmazottakat.</span><span class="sxs-lookup"><span data-stu-id="351dc-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="351dc-155">A következő döntéseket kell meghoznia minden engedélyezett fizetési módra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="351dc-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="351dc-156">**Döntések:**</span><span class="sxs-lookup"><span data-stu-id="351dc-156">**Decisions:**</span></span>

- <span data-ttu-id="351dc-157">Milyen fizetési módok megengedettek?</span><span class="sxs-lookup"><span data-stu-id="351dc-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="351dc-158">Kihez tartoznak a fizetési mód költségei?</span><span class="sxs-lookup"><span data-stu-id="351dc-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="351dc-159">Van ellenoldali számlatípus?</span><span class="sxs-lookup"><span data-stu-id="351dc-159">Is there an offset account type?</span></span> <span data-ttu-id="351dc-160">Ha van egy Ellenszámla típusa, mi az?</span><span class="sxs-lookup"><span data-stu-id="351dc-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="351dc-161">Ha van egy Ellenszámla, mi az a számla?</span><span class="sxs-lookup"><span data-stu-id="351dc-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="351dc-162">Ha a fizetési mód hitelkártya, akkor a fizetési módot csak az importált tranzakciókkal lehet használni?</span><span class="sxs-lookup"><span data-stu-id="351dc-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="351dc-163">Költségkategóriák és megosztott kategóriák</span><span class="sxs-lookup"><span data-stu-id="351dc-163">Expense categories and shared categories</span></span>

<span data-ttu-id="351dc-164">Amikor az alkalmazottak költségjelentést készítenek, az általuk rögzített kiadásoknak egy költségkategóriához kell társítva lennie.</span><span class="sxs-lookup"><span data-stu-id="351dc-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="351dc-165">A költségkategóriák olyan megosztott kategóriákból származnak, amelyek megoszthatók a szervezet jogi entitásai között.</span><span class="sxs-lookup"><span data-stu-id="351dc-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="351dc-166">Ezek a kategóriák megoszthatók a projektmenedzsmentben és a könyvelésben is, attól függően, hogy milyen módon határozta meg a szervezetet.</span><span class="sxs-lookup"><span data-stu-id="351dc-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="351dc-167">A szervezet definíciója és a megvalósítási csoport útmutatása alapján meg kell határozni, hogy a költségkezelésben használt kategóriákat csak a költségkezelésben használja a program, vagy meg kell osztania a projektmenedzsment és a könyvelés és költségkezelés között.</span><span class="sxs-lookup"><span data-stu-id="351dc-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="351dc-168">Felhívjuk figyelmét, hogy ezek a kategóriák megoszthatók a Projekt és Költség, vagy a Projekt és Termelés között, de a Költség és Termelés között nem.</span><span class="sxs-lookup"><span data-stu-id="351dc-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="351dc-169">Minden egyes költség kategóriára vonatkozóan a következő döntéseket kell meghoznia.</span><span class="sxs-lookup"><span data-stu-id="351dc-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="351dc-170">**Döntések:**</span><span class="sxs-lookup"><span data-stu-id="351dc-170">**Decisions:**</span></span>

- <span data-ttu-id="351dc-171">Mi a költségkategória?</span><span class="sxs-lookup"><span data-stu-id="351dc-171">What is the expense category?</span></span> <span data-ttu-id="351dc-172">Ilyenek például a repülőjáratok, a szállodák vagy az útiköltségtérítés kategóriái.</span><span class="sxs-lookup"><span data-stu-id="351dc-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="351dc-173">A költségkategória használható a Projektmenedzsment és könyvelés modulban is?</span><span class="sxs-lookup"><span data-stu-id="351dc-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="351dc-174">Mi a költségtípus?</span><span class="sxs-lookup"><span data-stu-id="351dc-174">What is the expense type?</span></span>
- <span data-ttu-id="351dc-175">Mi a költségkategória alapértelmezett fizetési módja?</span><span class="sxs-lookup"><span data-stu-id="351dc-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="351dc-176">A költség kategóriába tartozó költségeket tételezni kell?</span><span class="sxs-lookup"><span data-stu-id="351dc-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="351dc-177">Mi a költségkategória fő alapértelmezett számlája?</span><span class="sxs-lookup"><span data-stu-id="351dc-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="351dc-178">Mi a költségkategória alapértelmezett cikkáfacsoportja?</span><span class="sxs-lookup"><span data-stu-id="351dc-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="351dc-179">Engedélyezve vannak a költségkategóriához további fizetési módok?</span><span class="sxs-lookup"><span data-stu-id="351dc-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="351dc-180">Ha további fizetési módok engedélyezettek, mik ezek?</span><span class="sxs-lookup"><span data-stu-id="351dc-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="351dc-181">Vannak alkategóriák ebben a költségkategóriában?</span><span class="sxs-lookup"><span data-stu-id="351dc-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="351dc-182">Ha vannak alkategóriák, akkor a következő döntéseket kell meghoznia:</span><span class="sxs-lookup"><span data-stu-id="351dc-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="351dc-183">Van olyan alkategória, amely ki van zárva az adó visszaigényléséből?</span><span class="sxs-lookup"><span data-stu-id="351dc-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="351dc-184">Mi ezen alkategóriák cikkáfacsoportja?</span><span class="sxs-lookup"><span data-stu-id="351dc-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="351dc-185">Ha a költség kategória a projektmenedzsmentben és a könyvelésben is használatban van, válaszolja meg a hátralévő kérdéseket.</span><span class="sxs-lookup"><span data-stu-id="351dc-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="351dc-186">Ellenkező esetben lépjen a következő szakaszba.</span><span class="sxs-lookup"><span data-stu-id="351dc-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="351dc-187">Milyen költségszámlákat fog használni a következő kiadásokhoz?</span><span class="sxs-lookup"><span data-stu-id="351dc-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="351dc-188">Költség</span><span class="sxs-lookup"><span data-stu-id="351dc-188">Cost</span></span>
    - <span data-ttu-id="351dc-189">Bérlista-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="351dc-189">Payroll allocation</span></span>
    - <span data-ttu-id="351dc-190">Folyamatban lévő termelés költségértéke</span><span class="sxs-lookup"><span data-stu-id="351dc-190">WIP-cost value</span></span>
    - <span data-ttu-id="351dc-191">Költségelem</span><span class="sxs-lookup"><span data-stu-id="351dc-191">Cost-item</span></span>
    - <span data-ttu-id="351dc-192">Folyamatban lévő termelés költségérték-eleme</span><span class="sxs-lookup"><span data-stu-id="351dc-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="351dc-193">Elhatárolt veszteség</span><span class="sxs-lookup"><span data-stu-id="351dc-193">Accrued loss</span></span>
    - <span data-ttu-id="351dc-194">Folyamatban lévő termelés elhatárolt vesztesége</span><span class="sxs-lookup"><span data-stu-id="351dc-194">WIP-accrued loss</span></span>

- <span data-ttu-id="351dc-195">Milyen bevételszámlákat fog használni a következőkhöz?</span><span class="sxs-lookup"><span data-stu-id="351dc-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="351dc-196">Számlázott bevétel</span><span class="sxs-lookup"><span data-stu-id="351dc-196">Invoiced revenue</span></span>
    - <span data-ttu-id="351dc-197">Elhatárolt bevétel – Értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="351dc-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="351dc-198">Folyamatban lévő termelés – értékesítési érték</span><span class="sxs-lookup"><span data-stu-id="351dc-198">WIP-sales value</span></span>
    - <span data-ttu-id="351dc-199">Elhatárolt bevétel – termelés</span><span class="sxs-lookup"><span data-stu-id="351dc-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="351dc-200">Folyamatban lévő termelés</span><span class="sxs-lookup"><span data-stu-id="351dc-200">WIP-production</span></span>
    - <span data-ttu-id="351dc-201">Elhatárolt bevétel – profit</span><span class="sxs-lookup"><span data-stu-id="351dc-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="351dc-202">Folyamatban lévő termelés – profit</span><span class="sxs-lookup"><span data-stu-id="351dc-202">WIP-profit</span></span>
    - <span data-ttu-id="351dc-203">Elhatárolt bevétel – előfizetés</span><span class="sxs-lookup"><span data-stu-id="351dc-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="351dc-204">Folyamatban lévő termelés – előfizetés</span><span class="sxs-lookup"><span data-stu-id="351dc-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="351dc-205">Adók</span><span class="sxs-lookup"><span data-stu-id="351dc-205">Taxes</span></span>

<span data-ttu-id="351dc-206">A költséggel kapcsolatos adók esetében meg kell határozni, hogy mi szerepel, illetve van engedélyezve a költségjelentésekben.</span><span class="sxs-lookup"><span data-stu-id="351dc-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="351dc-207">**Döntések:**</span><span class="sxs-lookup"><span data-stu-id="351dc-207">**Decisions:**</span></span>

- <span data-ttu-id="351dc-208">Szerepel a költségösszegben az áfa?</span><span class="sxs-lookup"><span data-stu-id="351dc-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="351dc-209">Engedélyezni kell az adókedvezmény használatát a költségeken?</span><span class="sxs-lookup"><span data-stu-id="351dc-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="351dc-210">Ha a főkönyv tervezésekor úgy döntött, hogy alkalmazza az USA-beli forgalmi adót és alkalmazza az adószabályokat, nem engedélyezheti az adó-visszaigénylést a költségeknél.</span><span class="sxs-lookup"><span data-stu-id="351dc-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="351dc-211">(Az Egyesült államokbeli forgalmi adó és az adózási szabályok alkalmazása érdekében állítsa be a **Az ÁFA-adózási szabályok alkalmazása** beállítást **Igen** értékre.)</span><span class="sxs-lookup"><span data-stu-id="351dc-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="351dc-212">Házirendek</span><span class="sxs-lookup"><span data-stu-id="351dc-212">Policies</span></span>

<span data-ttu-id="351dc-213">A költségjelentés-házirendek létrehozásával segítséget nyújthat a szervezet számára, hogy időt és pénzt takarítson meg abban az esetben, ha az alkalmazottak költséget jelentenek a nevében.</span><span class="sxs-lookup"><span data-stu-id="351dc-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="351dc-214">A házirendek segítségével garantálható, hogy az alkalmazottak betartják a költségvetést, megadják az összes szükséges információt, és csak a számukra szükséges pénzt költik el.</span><span class="sxs-lookup"><span data-stu-id="351dc-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="351dc-215">Minden egyes költségjelentési házirendre és a létrehozott Költségjelentés-jóváhagyási házirendre vonatkozóan a következő döntéseket kell meghoznia.</span><span class="sxs-lookup"><span data-stu-id="351dc-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="351dc-216">**Döntések:**</span><span class="sxs-lookup"><span data-stu-id="351dc-216">**Decisions:**</span></span>

- <span data-ttu-id="351dc-217">Mi a szabályzat neve?</span><span class="sxs-lookup"><span data-stu-id="351dc-217">What is the name of the policy?</span></span>
- <span data-ttu-id="351dc-218">Mire vonatkozik a költséggel kapcsolatos irányelv?</span><span class="sxs-lookup"><span data-stu-id="351dc-218">What is the expense policy for?</span></span>
- <span data-ttu-id="351dc-219">Ha korábban úgy döntött, hogy engedélyezi a vállalatközi kiadásokat, a szervezethez tartozó melyik vállalatokra vonatkozik ez a szabályzat?</span><span class="sxs-lookup"><span data-stu-id="351dc-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="351dc-220">Mikor válik hatályossá a házirend?</span><span class="sxs-lookup"><span data-stu-id="351dc-220">When does the policy become effective?</span></span>
- <span data-ttu-id="351dc-221">Mikor jár le a házirend?</span><span class="sxs-lookup"><span data-stu-id="351dc-221">When does the policy expire?</span></span>
- <span data-ttu-id="351dc-222">Mi a házirendi szabály?</span><span class="sxs-lookup"><span data-stu-id="351dc-222">What is the policy rule?</span></span>
- <span data-ttu-id="351dc-223">Mi a házirendi szabály kimenete?</span><span class="sxs-lookup"><span data-stu-id="351dc-223">What is the outcome of the policy rule?</span></span>
