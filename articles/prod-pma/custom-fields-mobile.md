---
title: Egyéni mezők létrehozása a Microsoft Dynamics 365 Project Timesheet mobilalkalmazásban iOS és Android rendszereken
description: Ez a témakör általános mintákat mutat be az egyéni mezők létrehozására szolgáló bővítmények használatához.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078146"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="0f005-103">Egyéni mezők létrehozása a Microsoft Dynamics 365 Project Timesheet mobilalkalmazásban iOS és Android rendszereken</span><span class="sxs-lookup"><span data-stu-id="0f005-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f005-104">Ez a témakör általános mintákat mutat be az egyéni mezők létrehozására szolgáló bővítmények használatához.</span><span class="sxs-lookup"><span data-stu-id="0f005-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="0f005-105">Az alábbi témakörökről esik szó:</span><span class="sxs-lookup"><span data-stu-id="0f005-105">The following topics are covered:</span></span>

- <span data-ttu-id="0f005-106">Az egyéni mezők keretrendszere által támogatott különféle adattípusok</span><span class="sxs-lookup"><span data-stu-id="0f005-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="0f005-107">Útmutatás az írásvédett vagy szerkeszthető mezők időnyilvántartási bejegyzésekben történő megjelenítéséhez, illetve a felhasználó által megadott értékek adatbázisba történő mentéséhez</span><span class="sxs-lookup"><span data-stu-id="0f005-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="0f005-108">Útmutatás az írásvédett mezők az időnyilvántartás fejlécében történő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="0f005-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="0f005-109">Útmutatás egyéb egyéni üzleti logikák integrálásához (az alapértelmezett értékek mezőkben való megadása céljából), illetve további ellenőrzések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="0f005-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="0f005-110">Célközönség</span><span class="sxs-lookup"><span data-stu-id="0f005-110">Audience</span></span>

<span data-ttu-id="0f005-111">Ez a témakör olyan fejlesztők számára készült, akik egyéni mezők integrálását végzik Apple iOS és Google Android rendszereken elérhető Microsoft Dynamics 365 Project Timesheet mobilalkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="0f005-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="0f005-112">A témakör olyan olvasóknak készült, akik ismerik az X++ fejlesztést és a projektszintű időnyilvántartási funkciót.</span><span class="sxs-lookup"><span data-stu-id="0f005-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="0f005-113">Adatszerződés – TSTimesheetCustomField X++ osztály</span><span class="sxs-lookup"><span data-stu-id="0f005-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="0f005-114">A **TSTimesheetCustomField** osztály egy X++ adatszerződési osztály, amely az időnyilvántartási funkció egyéni mezőire vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="0f005-115">A rendszer az egyéni mezők mobilalkalmazásban történő megjelenítéséhez az egyéni mezők objektumainak listáit a TSTimesheetDetails adatszerződésen és a TSTimesheetEntry adatszerződésen keresztül is továbbítja.</span><span class="sxs-lookup"><span data-stu-id="0f005-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="0f005-116">**TSTimesheetDetails** – az időnyilvántartási fejléc szerződése.</span><span class="sxs-lookup"><span data-stu-id="0f005-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="0f005-117">**TSTimesheetEntry** – az időnyilvántartási tranzakció szerződése.</span><span class="sxs-lookup"><span data-stu-id="0f005-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="0f005-118">A megegyező a projektadatokkal és **timesheetLineRecId** értékkel rendelkező objektumokok csoportjai közösen alkotnak egy sort.</span><span class="sxs-lookup"><span data-stu-id="0f005-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="0f005-119">fieldBaseType (Types)</span><span class="sxs-lookup"><span data-stu-id="0f005-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="0f005-120">Az alkalmazásban megjelenő mező típusát a **TsTimesheetCustom** objektum **FieldBaseType** tulajdonsága határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="0f005-121">Az alábbi **Típusú** értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="0f005-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="0f005-122">Típusok értéke</span><span class="sxs-lookup"><span data-stu-id="0f005-122">Types value</span></span> | <span data-ttu-id="0f005-123">Típus szerint</span><span class="sxs-lookup"><span data-stu-id="0f005-123">Type</span></span>              | <span data-ttu-id="0f005-124">Megjegyzések</span><span class="sxs-lookup"><span data-stu-id="0f005-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="0f005-125">0</span><span class="sxs-lookup"><span data-stu-id="0f005-125">0</span></span>           | <span data-ttu-id="0f005-126">Karakterlánc (és felsorolás)</span><span class="sxs-lookup"><span data-stu-id="0f005-126">String (and Enum)</span></span> | <span data-ttu-id="0f005-127">A mező szöveges mezőként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="0f005-128">0</span><span class="sxs-lookup"><span data-stu-id="0f005-128">1</span></span>           | <span data-ttu-id="0f005-129">Integer</span><span class="sxs-lookup"><span data-stu-id="0f005-129">Integer</span></span>           | <span data-ttu-id="0f005-130">Az érték tizedesjegyek nélküli számként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="0f005-131">2</span><span class="sxs-lookup"><span data-stu-id="0f005-131">2</span></span>           | <span data-ttu-id="0f005-132">Valós</span><span class="sxs-lookup"><span data-stu-id="0f005-132">Real</span></span>              | <span data-ttu-id="0f005-133">Az érték tizedesjeggyel rendelkező számként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="0f005-134">Ha a valós értéket pénznemként szeretné megjeleníteni az alkalmazásban, használja a **fieldExtenededType** tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="0f005-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="0f005-135">A **numberOfDecimals** tulajdonság használatával megadhatja a megjelenített tizedesjegyek számát.</span><span class="sxs-lookup"><span data-stu-id="0f005-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="0f005-136">3</span><span class="sxs-lookup"><span data-stu-id="0f005-136">3</span></span>           | <span data-ttu-id="0f005-137">Dátum</span><span class="sxs-lookup"><span data-stu-id="0f005-137">Date</span></span>              | <span data-ttu-id="0f005-138">A rendszer a **Felhasználói beállítások** **Nyelvre és országra/régióra vonatkozó beállítások** lehetőség alatt megadott **Dátum-, idő- és számformátum** alapján határozza meg a dátumformátumot.</span><span class="sxs-lookup"><span data-stu-id="0f005-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="0f005-139">4</span><span class="sxs-lookup"><span data-stu-id="0f005-139">4</span></span>           | <span data-ttu-id="0f005-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="0f005-140">Boolean</span></span>           | |
| <span data-ttu-id="0f005-141">15</span><span class="sxs-lookup"><span data-stu-id="0f005-141">15</span></span>          | <span data-ttu-id="0f005-142">GUID</span><span class="sxs-lookup"><span data-stu-id="0f005-142">GUID</span></span>              | |
| <span data-ttu-id="0f005-143">16</span><span class="sxs-lookup"><span data-stu-id="0f005-143">16</span></span>          | <span data-ttu-id="0f005-144">Int64</span><span class="sxs-lookup"><span data-stu-id="0f005-144">Int64</span></span>             | |

- <span data-ttu-id="0f005-145">Ha a **TSTimesheetCustomField** objektum nem rendelkezik **stringOptions** tulajdonsággal, akkor a felhasználó számára egy szabadszöveges mező is elérhető.</span><span class="sxs-lookup"><span data-stu-id="0f005-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="0f005-146">A **stringLength** tulajdonság a felhasználók által megadható maximális karakterlánc-hosszúság beállítására használható.</span><span class="sxs-lookup"><span data-stu-id="0f005-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="0f005-147">Ha a **stringOptions** tulajdonság meg van adva a **TSTimesheetCustomField** objektumban, akkor a felhasználók csak ezeket a listaelemeket választhatják ki a választógombok segítségével.</span><span class="sxs-lookup"><span data-stu-id="0f005-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="0f005-148">Ebben az esetben a karakterlánc mező felhasználói bejegyzések céljából felsorolási értékként is működhet.</span><span class="sxs-lookup"><span data-stu-id="0f005-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="0f005-149">Ha az értéket felsorolásként szeretné menteni az adatbázisba, akkor az adatbázisba való mentés előtt manuálisan végezze el a karakterlánc értékének felsorolási értékre való leképezését egy parancssor használatával. Példákat a témakör „Parancssor használata a TSTimesheetEntryService osztályon az időnyilvántartási bejegyzés alkalmazásból az adatbázisba történő mentéséhez” című részében talál.</span><span class="sxs-lookup"><span data-stu-id="0f005-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="0f005-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="0f005-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="0f005-151">Ennek a tulajdonságnak a használatával a valós értékeket pénznemmé formázhatja.</span><span class="sxs-lookup"><span data-stu-id="0f005-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="0f005-152">Ez a megközelítés csak akkor alkalmazható, ha a **fieldBaseType** értéke **Valós**.</span><span class="sxs-lookup"><span data-stu-id="0f005-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="0f005-153">**TSCustomFieldExtendedType:None** – nincs alkalmazva formázás.</span><span class="sxs-lookup"><span data-stu-id="0f005-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="0f005-154">**TSCustomFieldExtendedType::Currency** – az érték formázása pénznemként.</span><span class="sxs-lookup"><span data-stu-id="0f005-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="0f005-155">Ha a pénznemformázás aktív, akkor a **stringValue** mező használható a pénznemkód átadására, amelynek az alkalmazásban kell megjelennie.</span><span class="sxs-lookup"><span data-stu-id="0f005-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="0f005-156">Az érték írásvédett.</span><span class="sxs-lookup"><span data-stu-id="0f005-156">The value is a read-only value.</span></span>

    <span data-ttu-id="0f005-157">A **realValue** mező az adatbázisba mentendő pénzösszeget tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0f005-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="0f005-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="0f005-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="0f005-159">Ezzel a tulajdonsággal megadhatja, hogy hol jelenjen meg az egyéni mező az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="0f005-160">**TSCustomFieldSection::Header** – a mező az alkalmazás **További részletek megtekintése** részében jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="0f005-161">Ezek a mezők mindig írásvédettek.</span><span class="sxs-lookup"><span data-stu-id="0f005-161">These fields are always read-only.</span></span>
- <span data-ttu-id="0f005-162">**TSCustomFieldSection::Line** – a mező az időnyilvántartási bejegyzések összes alapértelmezett sormezője után jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="0f005-163">Ezek a mezők szerkeszthetők és írásvédettek is lehetnek.</span><span class="sxs-lookup"><span data-stu-id="0f005-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="0f005-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="0f005-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="0f005-165">Ez a tulajdonság azonosítja a mezőt, amikor a rendszer menti az alkalmazás által szolgáltatott értékeket az adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="0f005-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="0f005-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="0f005-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="0f005-167">Ez a tulajdonság azonosítja a mezőt, amikor a rendszer menti az alkalmazás által szolgáltatott értékeket az adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="0f005-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="0f005-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="0f005-168">isEditable (NoYes)</span></span>

<span data-ttu-id="0f005-169">A tulajdonság **Igen** értékre állításával megadhatja, hogy a felhasználók szerkeszthetik-e az beviteli részében lévő mezőt.</span><span class="sxs-lookup"><span data-stu-id="0f005-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="0f005-170">A tulajdonság **Nem** értékre állításával a mező írásvédett lesz.</span><span class="sxs-lookup"><span data-stu-id="0f005-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="0f005-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="0f005-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="0f005-172">A tulajdonság **Igen** értékre állításával megadhatja, hogy az időnyilvántartás beviteli részében lévő mező megjelenése kötelező legyen-e.</span><span class="sxs-lookup"><span data-stu-id="0f005-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="0f005-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="0f005-173">label (str)</span></span>

<span data-ttu-id="0f005-174">Ez a tulajdonság az alkalmazásban található mező mellett látható címke megadására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0f005-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="0f005-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="0f005-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="0f005-176">Ez a tulajdonság csak akkor használható, ha a **fieldBaseType** paraméter a **String** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="0f005-177">Ha a **stringOptions** karakterlánc be van állítva, akkor a választógombokkal kijelölhető karakterláncértékeket a listán lévő karakterláncok határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="0f005-178">Ha nem ad meg karakterláncot, akkor a karakterláncmezőben szabadszöveges bejegyzés megadása engedélyezésre kerül. Példákat a témakör „Parancssor használata a TSTimesheetEntryService osztályon az időnyilvántartási bejegyzés alkalmazásból az adatbázisba történő mentéséhez” című részében talál.</span><span class="sxs-lookup"><span data-stu-id="0f005-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="0f005-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="0f005-179">stringLength (int)</span></span>

<span data-ttu-id="0f005-180">Ez a tulajdonság a karakterláncmező maximális hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="0f005-181">Csak akkor használható, ha a **fieldBaseType** paraméter a **String** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="0f005-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="0f005-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="0f005-183">Ez a tulajdonság a valós érték mezőben megjelenített tizedesjegyek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="0f005-184">Csak akkor használható, ha a **fieldBaseType** paraméter a **Valós** értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="0f005-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="0f005-185">orderSequence (int)</span></span>

<span data-ttu-id="0f005-186">Ez a tulajdonság határozza meg, hogy az egyéni mezők milyen sorrendben jelennek meg az alkalmazásban, ha egynél több egyéni mező van megadva.</span><span class="sxs-lookup"><span data-stu-id="0f005-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="0f005-187">Az alacsonyabb számokat tartalmazó mezők előbb jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="0f005-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="0f005-188">booleanValue (boolean)</span></span>

<span data-ttu-id="0f005-189">A **Boolean** típusú mezők esetében ez a tulajdonság továbbítja a mező Boolean értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="0f005-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="0f005-190">guidValue (guid)</span></span>

<span data-ttu-id="0f005-191">A **GUID** típusú mezők esetében ez a tulajdonság továbbítja a mező globálisan egyedi azonosítójának (GUID) az értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="0f005-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="0f005-192">int64Value (int64)</span></span>

<span data-ttu-id="0f005-193">Az **Int64** típusú mezők esetében ez a tulajdonság továbbítja a mező Int64 értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="0f005-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="0f005-194">intValue (int)</span></span>

<span data-ttu-id="0f005-195">Az **Int** típusú mezők esetében ez a tulajdonság továbbítja a mező Int értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="0f005-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="0f005-196">realValue (real)</span></span>

<span data-ttu-id="0f005-197">A **Valós** típusú mezők esetében ez a tulajdonság továbbítja a mező valós értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="0f005-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="0f005-198">stringValue (str)</span></span>

<span data-ttu-id="0f005-199">A **String** típusú mezők esetében ez a tulajdonság továbbítja a mező String értékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="0f005-200">A pénznemként formázott **Valós** típusú mezők esetében is használatos.</span><span class="sxs-lookup"><span data-stu-id="0f005-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="0f005-201">Ezen mezők esetében a tulajdonság a pénznemkód alkalmazásba való továbbítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0f005-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="0f005-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="0f005-202">dateValue (date)</span></span>

<span data-ttu-id="0f005-203">A **Dátum** típusú mezők esetében ez a tulajdonság továbbítja a mező dátumértékét a kiszolgáló és az alkalmazás között.</span><span class="sxs-lookup"><span data-stu-id="0f005-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="0f005-204">Egyéni mezők megjelenítése és mentése az időnyilvántartás beviteli szakaszában</span><span class="sxs-lookup"><span data-stu-id="0f005-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="0f005-205">Az alábbiakban az időnyilvántartási bejegyzések létrehozását bemutató képernyőkép látható a mobilalkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="0f005-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="0f005-206">A képen az alapértelmezett mezők, illetve az „Időbejegyzés” részben található „Tesztkarakterlánc” nevű egyéni mező látható. Ennél a mezőnél a „Második lehetőség” nevű felsorolási érték már be van állítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Tesztkarakterlánc egyéni mezője az alkalmazásban](media/timesheet-entry.jpg)



<span data-ttu-id="0f005-208">Az alábbiakban egy képernyőkép látható a mobilalkalmazásból, amelyen a felhasználó a „Tesztkarakterlánc” nevű egyéni mező felsorolási lehetőségei közül választ.</span><span class="sxs-lookup"><span data-stu-id="0f005-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="0f005-209">A két lehetőség választógomb formájában jelenik meg: „Első lehetőség” és „Második lehetőség”.</span><span class="sxs-lookup"><span data-stu-id="0f005-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="0f005-210">Jelenleg a második lehetőség van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="0f005-210">The second option is currently selected.</span></span>

![A tesztkarakterlánc egyéni mezőjének választógombjai](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="0f005-212">A TSTimesheetLine táblázat kibővítése egyéni mezővel</span><span class="sxs-lookup"><span data-stu-id="0f005-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="0f005-213">Tipikus helyzetekben valószínű, hogy az időnyilvántartás beviteli szakaszában szereplő egyéni mező adatait a rendszer a TSTimesheetLine táblázatba menti.</span><span class="sxs-lookup"><span data-stu-id="0f005-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="0f005-214">Azonban más táblázatok is használhatók, ha az adatok egy megadott TSTimesheetTrans rekord alapján is lekérhetők, illetve ha nem rendelkeznek konkrét rekordkörnyezettel (ha például a mezőt írásvédettre állították a projektparaméterekben).</span><span class="sxs-lookup"><span data-stu-id="0f005-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="0f005-215">Ne feledje, hogy az egyéni mezőkhöz nem szükséges semmilyen háttérben tárolt adatbázisrekord.</span><span class="sxs-lookup"><span data-stu-id="0f005-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="0f005-216">X++ logika alapján dinamikusan is létrehozhatók.</span><span class="sxs-lookup"><span data-stu-id="0f005-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="0f005-217">Ez a megközelítés írásvédett adatok esetén bizonyulhat hasznosnak. Dinamikusan létrehozott egyénimező-értékekre példát a „Parancssor használata a TSTimesheetEntryService osztályon, illetve a buildCustomFieldListForHeader metódus használata az időnyilvántartási adatok megadására” című részben talál.</span><span class="sxs-lookup"><span data-stu-id="0f005-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="0f005-218">Az alábbiakban Visual Studio alkalmazásobjektumokat tartalmazó fájáról készült képernyőkép látható.</span><span class="sxs-lookup"><span data-stu-id="0f005-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="0f005-219">A képen a TSTimesheetLine táblázat kiterjesztése és az egyéni mezőként hozzáadott a TestLineString mező látható.</span><span class="sxs-lookup"><span data-stu-id="0f005-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Sor karakterlánca](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="0f005-221">Parancssor használata a TSTimesheetSettings osztály buildCustomFieldList metódusán az időnyilvántartás beviteli szakaszában lévő mező megjelenítésére</span><span class="sxs-lookup"><span data-stu-id="0f005-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="0f005-222">Ez a kód a mező megjelenítési beállításait szabályozza az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="0f005-223">Ez szabályozza például a mező típusát, a címkét, hogy kötelező legyen-e a mező, és hogy melyik szakaszban jelenjen meg a mező.</span><span class="sxs-lookup"><span data-stu-id="0f005-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="0f005-224">A következő példa egy karakterláncmezőt jelenít meg az időnyilvántartásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="0f005-225">A mezőben két lehetőség közül választhat a választógombok segítségével: **Első lehetőség** és **Második lehetőség**.</span><span class="sxs-lookup"><span data-stu-id="0f005-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="0f005-226">Az alkalmazásban található mező a TSTimesheetLine táblázathoz hozzáadott **TestLineString** mezőhöz van társítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="0f005-227">Használja a **TSTimesheetCustomField::newFromMetatdata()** metódust az egyéni mező tulajdonságai inicializálásának leegyszerűsítésére: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** és **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="0f005-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="0f005-228">Ha szeretné, a paramétereket kézzel is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="0f005-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="0f005-229">Parancssor használata a TSTimesheetEntry osztály buildCustomFieldListForEntry metódusán értékek megadására az időnyilvántartási bejegyzésbe</span><span class="sxs-lookup"><span data-stu-id="0f005-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="0f005-230">A **buildCustomFieldListForEntry** metódus a mobilalkalmazáson belül mentett időnyilvántartási sorokban lévő értékek megadására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0f005-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="0f005-231">Paraméterként egy TSTimesheetTrans rekordot használ.</span><span class="sxs-lookup"><span data-stu-id="0f005-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="0f005-232">Az adott rekord mezői az alkalmazásban szereplő egyénimező-értékek megadására használhatók.</span><span class="sxs-lookup"><span data-stu-id="0f005-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="0f005-233">Parancssor használata a TSTimesheetEntryService osztályon az időnyilvántartási bejegyzés alkalmazásból az adatbázisba történő mentéséhez</span><span class="sxs-lookup"><span data-stu-id="0f005-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="0f005-234">Ha egy egyéni mezőt tipikus használat során szeretne az adatbázisba menteni, az alábbi metódusokat kell bővítenie:</span><span class="sxs-lookup"><span data-stu-id="0f005-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="0f005-235">A **timesheetLineNeedsUpdating** metódus alkalmazásával megállapítható, hogy az alkalmazásban a felhasználó módosította-e a sor rekordját és azt a az adatbázisba kell-e menteni.</span><span class="sxs-lookup"><span data-stu-id="0f005-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="0f005-236">A teljesítmény miatt nem kell aggódni, akkor ez a metódus egyszerűsíthető, hogy mindig az **igaz** értéket adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0f005-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="0f005-237">A **populateTimesheetLineFromEntryDuringCreate** és a **populateTimesheetLineFromEntryDuringUpdate** metódusok bővíthetők úgy, hogy a megadott TSTimesheetEntry adatszerződés-rekordban megadott értékeket a TSTimesheetLine adatbázisrekordba adják meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="0f005-238">Az alábbi példában látható, hogy az adatbázismező és a beviteli mező között hogyan hajtható végre kézi leképezés az X++ kóddal.</span><span class="sxs-lookup"><span data-stu-id="0f005-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="0f005-239">A **populateTimesheetWeekFromEntry** metódus akkor is bővíthető, ha a **TSTimesheetEntry** objektumra leképezett egyéni mezőnek vissza kell írnia egy értéket a TSTimesheetLineweek adatbázis-táblázatba.</span><span class="sxs-lookup"><span data-stu-id="0f005-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="0f005-240">A következő példa a **firstOption** , illetve **secondOption** értékét menti, amelyet a felhasználó nyers karakterláncértékként választ az adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="0f005-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="0f005-241">Ha az adatbázis mező **Felsorolás** típusú mező, akkor ezek az értékek kézileg is leképezhetők egy felsorolási értékre, majd menthetők az adatbázis-táblázat felsorolási mezőjébe.</span><span class="sxs-lookup"><span data-stu-id="0f005-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="0f005-242">Egyéni mezők megjelenítése az időnyilvántartás fejlécében</span><span class="sxs-lookup"><span data-stu-id="0f005-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="0f005-243">Az alábbiakban egy időnyilvántartást olvasó felhasználót bemutató képernyőkép látható a mobilalkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="0f005-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="0f005-244">A jobb felső sarokban lévő „További információ” gombot úgy állították be, hogy a „További részletek megtekintése” lehetőséget jelenítse meg.</span><span class="sxs-lookup"><span data-stu-id="0f005-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![További részletek megjelenítése parancs](media/show-more.png)

<span data-ttu-id="0f005-246">Az alábbiakban az időnyilvántartás „Egyebek” részét bemutató képernyőkép látható a mobilalkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="0f005-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="0f005-247">A rendszer hozzáadta az „Időnyilvántartás kihasználtsági rátája (kiszámított egyéni mező)” nevű egyéni mezőt az időnyilvántartás fejlécszakaszához.</span><span class="sxs-lookup"><span data-stu-id="0f005-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="0f005-248">Az egyéni mezőben beállított írásvédett érték a „0,667”.</span><span class="sxs-lookup"><span data-stu-id="0f005-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Egyebek szakasz](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="0f005-250">A TSTimesheetTable táblázat kibővítése egyéni mezővel</span><span class="sxs-lookup"><span data-stu-id="0f005-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="0f005-251">Tipikus helyzetekben valószínű, hogy az fejlécben szereplő egyéni mező adatait a rendszer a TSTimesheetHeader táblázatból kéri le.</span><span class="sxs-lookup"><span data-stu-id="0f005-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="0f005-252">Azonban más táblázatok is használhatók, ha az adatok egy megadott TSTimesheetTable rekord alapján is lekérhetők, illetve ha nem rendelkeznek konkrét rekordkörnyezettel (ha például a mezőt írásvédettre állították a projektparaméterekben).</span><span class="sxs-lookup"><span data-stu-id="0f005-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="0f005-253">Ne feledje, hogy az egyéni mezőkhöz nem szükséges semmilyen háttérben tárolt adatbázisrekord.</span><span class="sxs-lookup"><span data-stu-id="0f005-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="0f005-254">X++ logika alapján dinamikusan is létrehozhatók.</span><span class="sxs-lookup"><span data-stu-id="0f005-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="0f005-255">Az alábbi példa ezt a megközelítést mutatja be.</span><span class="sxs-lookup"><span data-stu-id="0f005-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="0f005-256">A fejlécben található mezők mindig írásvédettek az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="0f005-257">Parancssor használata a TSTimesheetSettings osztály buildCustomFieldList metódusán a fejlécszakaszban lévő mező megjelenítésére</span><span class="sxs-lookup"><span data-stu-id="0f005-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="0f005-258">Ez a kód a mező megjelenítési beállításait szabályozza az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="0f005-259">Ez szabályozza például a mező típusát, a címkét, hogy kötelező legyen-e a mező, és hogy melyik szakaszban jelenjen meg a mező.</span><span class="sxs-lookup"><span data-stu-id="0f005-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="0f005-260">Az alábbi példa egy kiszámított értéket mutat be az alkalmazás fejlécében.</span><span class="sxs-lookup"><span data-stu-id="0f005-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="0f005-261">Parancssor használata a TSTimesheetDetails osztály buildCustomFieldListForHeader metódusán az időnyilvántartási részletek megadására</span><span class="sxs-lookup"><span data-stu-id="0f005-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="0f005-262">A **buildCustomFieldListForHeader** metódus a mobilalkalmazás időnyilvántartási fejlécében lévő értékek megadására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0f005-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="0f005-263">Paraméterként egy TSTimesheetTable rekordot használ.</span><span class="sxs-lookup"><span data-stu-id="0f005-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="0f005-264">Az adott rekord mezői az alkalmazásban szereplő egyénimező-értékek megadására használhatók.</span><span class="sxs-lookup"><span data-stu-id="0f005-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="0f005-265">A következő példa semmilyen értéket nem olvas be az adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="0f005-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="0f005-266">Ehelyett az X++ logikát használja az alkalmazásban megjelenő kiszámított érték létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="0f005-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="0f005-267">Egyéb konfigurálási/bővítési lehetőségek</span><span class="sxs-lookup"><span data-stu-id="0f005-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="0f005-268">További ellenőrzés hozzáadása az alkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="0f005-268">Adding additional validation for the app</span></span>

<span data-ttu-id="0f005-269">Az időnyilvántartási funkció adatbázisszintű logilája továbbra is változatlanul fogja folytatni a működését.</span><span class="sxs-lookup"><span data-stu-id="0f005-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="0f005-270">A mentési vagy küldési műveletek befejezésének megszakításához, illetve egy adott hibaüzenet megjelenítéséhez egy parancssori bővítménnyel adja hozzá a **throw error("message to user")** szöveget a kódhoz.</span><span class="sxs-lookup"><span data-stu-id="0f005-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="0f005-271">Az alábbiakban három példát talál a hasznos bővíthető metódusokra:</span><span class="sxs-lookup"><span data-stu-id="0f005-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="0f005-272">Ha a **validateWrite** az időnyilvántartási sor mentése során **hamis** értéket ad vissza a TSTimesheetLine táblázatban, akkor megjelenik egy hibaüzenet a mobilalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="0f005-273">Ha a **validateSubmit** az időnyilvántartás alkalmazásban történő küldése során **hamis** értéket ad vissza a TSTimesheetTable táblázatban, akkor a rendszer megjelenít egy hibaüzenetet.</span><span class="sxs-lookup"><span data-stu-id="0f005-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="0f005-274">Az **insert** metódus során a TSTimesheetLine táblázaton alkalmazott, mezők kitöltésére szolgáló logika (például a **Sortulajdonság** ) továbbra is futni fog.</span><span class="sxs-lookup"><span data-stu-id="0f005-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="0f005-275">Alapértelmezett mezők elrejtése és írásvédettként való megjelölése konfigurálással</span><span class="sxs-lookup"><span data-stu-id="0f005-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="0f005-276">A projektparaméterek beállításaival írásvédetté teheti, illetve elrejtheti az alapértelmezett mezőket a mobilalkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="0f005-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="0f005-277">**Projektvezetési és könyvelési paraméterek** lap **Időnyilvántartás** fülének **Mobil időnyilvántartások** szakaszában állíthatja be a lehetőségeket.</span><span class="sxs-lookup"><span data-stu-id="0f005-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparaméterek](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="0f005-279">A kiválasztásra elérhető tevékenységek módosítása a bővítmények segítségével</span><span class="sxs-lookup"><span data-stu-id="0f005-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="0f005-280">A projektekhez kiválasztható tevékenységeket a rendszer a **getActivitiesForProject()** és a **getActivityQuery()** metódusok alkalmazásával adja meg a **TsTimesheetProjectService** osztályban.</span><span class="sxs-lookup"><span data-stu-id="0f005-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="0f005-281">Parancssort használva módosíthat ezen, hogy összeegyeztesse az üzleti helyzetet az adott projekt kiválasztásra elérhető tevékenységekkel.</span><span class="sxs-lookup"><span data-stu-id="0f005-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="0f005-282">Alapértelmezett projektkategória megadása az időnyilvántartási bejegyzésekben</span><span class="sxs-lookup"><span data-stu-id="0f005-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="0f005-283">Az alapértelmezett projektkategória időnyilvántartási bejegyzésbe történő megadása három szinten megy végbe.</span><span class="sxs-lookup"><span data-stu-id="0f005-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="0f005-284">A kívánt működés eléréséhez parancssor használatával bővítheti a viselkedést bármelyik vagy akár mindegyik szinten.</span><span class="sxs-lookup"><span data-stu-id="0f005-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="0f005-285">A rendszer az alábbi hierarchiát használja:</span><span class="sxs-lookup"><span data-stu-id="0f005-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="0f005-286">Az alkalmazás megpróbálja elhelyezni az alapértelmezett kategóriát a projekterőforrásból.</span><span class="sxs-lookup"><span data-stu-id="0f005-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="0f005-287">Ez az alapértelmezett kategória a **TSTimesheetSettingsService** osztály **getCurrentUserResource** és **getDelegatedResourcesForCurrentUser** metódusaiban van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="0f005-288">Ha az alapértelmezett kategória nincs megadva a projekterőforrási szintjen, az alkalmazás a projekttevékenységből próbálja meg lekérni.</span><span class="sxs-lookup"><span data-stu-id="0f005-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="0f005-289">Ez az alapértelmezett kategória a **TSTimesheetProjectService** osztály **getActivitiesForProject** metódusában van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="0f005-290">Ha az alapértelmezett kategória nincs megadva a projekttevékenységi szintjen, a rendszer lekéri a az alapértelmezett kategóriát a projektparaméterekből.</span><span class="sxs-lookup"><span data-stu-id="0f005-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="0f005-291">Ez az alapértelmezett kategória a **TSTimesheetProjectService** osztály **getProjectDetailsbyRule** metódusában van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0f005-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
