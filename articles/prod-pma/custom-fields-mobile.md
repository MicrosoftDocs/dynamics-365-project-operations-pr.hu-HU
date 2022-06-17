---
title: Egyéni mezők létrehozása a Microsoft Dynamics 365 Project Timesheet mobilalkalmazásban iOS és Android rendszereken
description: Ez a cikk gyakori mintákat tartalmaz a bővítmények egyéni mezők megvalósításához való használatához.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913715"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Egyéni mezők létrehozása a Microsoft Dynamics 365 Project Timesheet mobilalkalmazásban iOS és Android rendszereken

[!include [banner](../includes/banner.md)]

Ez a cikk gyakori mintákat tartalmaz a bővítmények egyéni mezők megvalósításához való használatához. A következő cikkek a következőkre terjednek ki:

- Az egyéni mezők keretrendszere által támogatott különféle adattípusok
- Útmutatás az írásvédett vagy szerkeszthető mezők időnyilvántartási bejegyzésekben történő megjelenítéséhez, illetve a felhasználó által megadott értékek adatbázisba történő mentéséhez
- Útmutatás az írásvédett mezők az időnyilvántartás fejlécében történő megjelenítéséhez
- Útmutatás egyéb egyéni üzleti logikák integrálásához (az alapértelmezett értékek mezőkben való megadása céljából), illetve további ellenőrzések elvégzéséhez

## <a name="audience"></a>Célközönség

Ez a cikk azoknak a fejlesztőknek szól, akik egyéni mezőiket integrálják az Apple iOS és a Microsoft Dynamics 365 Project Timesheet Google számára elérhető mobilalkalmazásba Android. A témakör olyan olvasóknak készült, akik ismerik az X++ fejlesztést és a projektszintű időnyilvántartási funkciót.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Adatszerződés – TSTimesheetCustomField X++ osztály

A **TSTimesheetCustomField** osztály egy X++ adatszerződési osztály, amely az időnyilvántartási funkció egyéni mezőire vonatkozó információkat jeleníti meg. A rendszer az egyéni mezők mobilalkalmazásban történő megjelenítéséhez az egyéni mezők objektumainak listáit a TSTimesheetDetails adatszerződésen és a TSTimesheetEntry adatszerződésen keresztül is továbbítja.

- **TSTimesheetDetails** – az időnyilvántartási fejléc szerződése.
- **TSTimesheetEntry** – az időnyilvántartási tranzakció szerződése. A megegyező a projektadatokkal és **timesheetLineRecId** értékkel rendelkező objektumokok csoportjai közösen alkotnak egy sort.

### <a name="fieldbasetype-types"></a>fieldBaseType (Types)

Az alkalmazásban megjelenő mező típusát a **TsTimesheetCustom** objektum **FieldBaseType** tulajdonsága határozza meg. Az alábbi **Típusú** értékek támogatottak.

| Típusok értéke | Típus szerint              | Megjegyzések |
|-------------|-------------------|-------|
| 0           | Karakterlánc (és felsorolás) | A mező szöveges mezőként jelenik meg. |
| 1           | Integer           | Az érték tizedesjegyek nélküli számként jelenik meg. |
| 2           | Valós              | Az érték tizedesjeggyel rendelkező számként jelenik meg.<p>Ha a valós értéket pénznemként szeretné megjeleníteni az alkalmazásban, használja a **fieldExtenededType** tulajdonságot. A **numberOfDecimals** tulajdonság használatával megadhatja a megjelenített tizedesjegyek számát.</p> |
| 3           | Dátum              | A rendszer a **Felhasználói beállítások** **Nyelvre és országra/régióra vonatkozó beállítások** lehetőség alatt megadott **Dátum-, idő- és számformátum** alapján határozza meg a dátumformátumot. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ha a **TSTimesheetCustomField** objektum nem rendelkezik **stringOptions** tulajdonsággal, akkor a felhasználó számára egy szabadszöveges mező is elérhető.

    A **stringLength** tulajdonság a felhasználók által megadható maximális karakterlánc-hosszúság beállítására használható.

- Ha a **stringOptions** tulajdonság meg van adva a **TSTimesheetCustomField** objektumban, akkor a felhasználók csak ezeket a listaelemeket választhatják ki a választógombok segítségével.

    Ebben az esetben a karakterlánc mező felhasználói bejegyzések céljából felsorolási értékként is működhet. Ha az értéket enumként szeretné menteni az adatbázisba, manuálisan képezze vissza a karakterlánc értékét az enum értékre, mielőtt az adatbázisba mentené a parancslánc használatával (példaként tekintse meg a cikk későbbi, "A TSTimesheetEntryService osztály parancsláncának használata az alkalmazásból az alkalmazásból az adatbázisba való visszamentéséhez" című szakaszát).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Ennek a tulajdonságnak a használatával a valós értékeket pénznemmé formázhatja. Ez a megközelítés csak akkor alkalmazható, ha a **fieldBaseType** értéke **Valós**.

- **TSCustomFieldExtendedType:None** – nincs alkalmazva formázás.
- **TSCustomFieldExtendedType::Currency** – az érték formázása pénznemként.

    Ha a pénznemformázás aktív, akkor a **stringValue** mező használható a pénznemkód átadására, amelynek az alkalmazásban kell megjelennie. Az érték írásvédett.

    A **realValue** mező az adatbázisba mentendő pénzösszeget tartalmazza.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Ezzel a tulajdonsággal megadhatja, hogy hol jelenjen meg az egyéni mező az alkalmazásban.

- **TSCustomFieldSection::Header** – a mező az alkalmazás **További részletek megtekintése** részében jelenik meg. Ezek a mezők mindig írásvédettek.
- **TSCustomFieldSection::Line** – a mező az időnyilvántartási bejegyzések összes alapértelmezett sormezője után jelenik meg. Ezek a mezők szerkeszthetők és írásvédettek is lehetnek.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ez a tulajdonság azonosítja a mezőt, amikor a rendszer menti az alkalmazás által szolgáltatott értékeket az adatbázisba.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ez a tulajdonság azonosítja a mezőt, amikor a rendszer menti az alkalmazás által szolgáltatott értékeket az adatbázisba.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

A tulajdonság **Igen** értékre állításával megadhatja, hogy a felhasználók szerkeszthetik-e az beviteli részében lévő mezőt. A tulajdonság **Nem** értékre állításával a mező írásvédett lesz.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

A tulajdonság **Igen** értékre állításával megadhatja, hogy az időnyilvántartás beviteli részében lévő mező megjelenése kötelező legyen-e.

### <a name="label-str"></a>label (str)

Ez a tulajdonság az alkalmazásban található mező mellett látható címke megadására szolgál.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Ez a tulajdonság csak akkor használható, ha a **fieldBaseType** paraméter a **String** értékre van állítva. Ha a **stringOptions** karakterlánc be van állítva, akkor a választógombokkal kijelölhető karakterláncértékeket a listán lévő karakterláncok határozzák meg. Ha nincs megadva sztring, a karakterláncmező szabad szöveges bejegyzése engedélyezett (példaként lásd a cikk későbbi, "A TSTimesheetEntryService osztály parancsláncának használata az alkalmazásból származó időnyilvántartás-bejegyzés mentéséhez az alkalmazásból az adatbázisba" című szakaszát).

### <a name="stringlength-int"></a>stringLength (int)

Ez a tulajdonság a karakterláncmező maximális hosszát adja meg. Csak akkor használható, ha a **fieldBaseType** paraméter a **String** értékre van állítva.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ez a tulajdonság a valós érték mezőben megjelenített tizedesjegyek számát adja meg. Csak akkor használható, ha a **fieldBaseType** paraméter a **Valós** értékre van állítva.

### <a name="ordersequence-int"></a>orderSequence (int)

Ez a tulajdonság határozza meg, hogy az egyéni mezők milyen sorrendben jelennek meg az alkalmazásban, ha egynél több egyéni mező van megadva. Az alacsonyabb számokat tartalmazó mezők előbb jelennek meg.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

A **Boolean** típusú mezők esetében ez a tulajdonság továbbítja a mező Boolean értékét a kiszolgáló és az alkalmazás között.

### <a name="guidvalue-guid"></a>guidValue (guid)

A **GUID** típusú mezők esetében ez a tulajdonság továbbítja a mező globálisan egyedi azonosítójának (GUID) az értékét a kiszolgáló és az alkalmazás között.

### <a name="int64value-int64"></a>int64Value (int64)

Az **Int64** típusú mezők esetében ez a tulajdonság továbbítja a mező Int64 értékét a kiszolgáló és az alkalmazás között.

### <a name="intvalue-int"></a>intValue (int)

Az **Int** típusú mezők esetében ez a tulajdonság továbbítja a mező Int értékét a kiszolgáló és az alkalmazás között.

### <a name="realvalue-real"></a>realValue (real)

A **Valós** típusú mezők esetében ez a tulajdonság továbbítja a mező valós értékét a kiszolgáló és az alkalmazás között.

### <a name="stringvalue-str"></a>stringValue (str)

A **String** típusú mezők esetében ez a tulajdonság továbbítja a mező String értékét a kiszolgáló és az alkalmazás között. A pénznemként formázott **Valós** típusú mezők esetében is használatos. Ezen mezők esetében a tulajdonság a pénznemkód alkalmazásba való továbbítására szolgál.

### <a name="datevalue-date"></a>dateValue (date)

A **Dátum** típusú mezők esetében ez a tulajdonság továbbítja a mező dátumértékét a kiszolgáló és az alkalmazás között.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Egyéni mezők megjelenítése és mentése az időnyilvántartás beviteli szakaszában

Az alábbiakban az időnyilvántartási bejegyzések létrehozását bemutató képernyőkép látható a mobilalkalmazásból. A képen az alapértelmezett mezők, illetve az „Időbejegyzés” részben található „Tesztkarakterlánc” nevű egyéni mező látható. Ennél a mezőnél a „Második lehetőség” nevű felsorolási érték már be van állítva.

![Tesztkarakterlánc egyéni mezője az alkalmazásban.](media/timesheet-entry.jpg)



Az alábbiakban egy képernyőkép látható a mobilalkalmazásból, amelyen a felhasználó a „Tesztkarakterlánc” nevű egyéni mező felsorolási lehetőségei közül választ.  A két lehetőség választógomb formájában jelenik meg: „Első lehetőség” és „Második lehetőség”. Jelenleg a második lehetőség van kiválasztva.

![A tesztkarakterlánc egyéni mezőjének választógombjai.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>A TSTimesheetLine táblázat kibővítése egyéni mezővel

Tipikus helyzetekben valószínű, hogy az időnyilvántartás beviteli szakaszában szereplő egyéni mező adatait a rendszer a TSTimesheetLine táblázatba menti. Azonban más táblázatok is használhatók, ha az adatok egy megadott TSTimesheetTrans rekord alapján is lekérhetők, illetve ha nem rendelkeznek konkrét rekordkörnyezettel (ha például a mezőt írásvédettre állították a projektparaméterekben).

Ne feledje, hogy az egyéni mezőkhöz nem szükséges semmilyen háttérben tárolt adatbázisrekord. X++ logika alapján dinamikusan is létrehozhatók. Ez a megközelítés írásvédett adatok esetén bizonyulhat hasznosnak. Dinamikusan létrehozott egyénimező-értékekre példát a „Parancssor használata a TSTimesheetEntryService osztályon, illetve a buildCustomFieldListForHeader metódus használata az időnyilvántartási adatok megadására” című részben talál.

Az alábbiakban Visual Studio alkalmazásobjektumokat tartalmazó fájáról készült képernyőkép látható. A képen a TSTimesheetLine táblázat kiterjesztése és az egyéni mezőként hozzáadott a TestLineString mező látható.

![Sor karakterlánca.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Parancssor használata a TSTimesheetSettings osztály buildCustomFieldList metódusán az időnyilvántartás beviteli szakaszában lévő mező megjelenítésére

Ez a kód a mező megjelenítési beállításait szabályozza az alkalmazásban. Ez szabályozza például a mező típusát, a címkét, hogy kötelező legyen-e a mező, és hogy melyik szakaszban jelenjen meg a mező.

A következő példa egy karakterláncmezőt jelenít meg az időnyilvántartásban. A mezőben két lehetőség közül választhat a választógombok segítségével: **Első lehetőség** és **Második lehetőség**. Az alkalmazásban található mező a TSTimesheetLine táblázathoz hozzáadott **TestLineString** mezőhöz van társítva.

Használja a **TSTimesheetCustomField::newFromMetatdata()** metódust az egyéni mező tulajdonságai inicializálásának leegyszerűsítésére: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** és **numberOfDecimals**. Ha szeretné, a paramétereket kézzel is megadhatja.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Parancssor használata a TSTimesheetEntry osztály buildCustomFieldListForEntry metódusán értékek megadására az időnyilvántartási bejegyzésbe

A **buildCustomFieldListForEntry** metódus a mobilalkalmazáson belül mentett időnyilvántartási sorokban lévő értékek megadására szolgál. Paraméterként egy TSTimesheetTrans rekordot használ. Az adott rekord mezői az alkalmazásban szereplő egyénimező-értékek megadására használhatók.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Parancssor használata a TSTimesheetEntryService osztályon az időnyilvántartási bejegyzés alkalmazásból az adatbázisba történő mentéséhez

Ha egy egyéni mezőt tipikus használat során szeretne az adatbázisba menteni, az alábbi metódusokat kell bővítenie:

- A **timesheetLineNeedsUpdating** metódus alkalmazásával megállapítható, hogy az alkalmazásban a felhasználó módosította-e a sor rekordját és azt a az adatbázisba kell-e menteni. A teljesítmény miatt nem kell aggódni, akkor ez a metódus egyszerűsíthető, hogy mindig az **igaz** értéket adja vissza.
- A **populateTimesheetLineFromEntryDuringCreate** és a **populateTimesheetLineFromEntryDuringUpdate** metódusok bővíthetők úgy, hogy a megadott TSTimesheetEntry adatszerződés-rekordban megadott értékeket a TSTimesheetLine adatbázisrekordba adják meg. Az alábbi példában látható, hogy az adatbázismező és a beviteli mező között hogyan hajtható végre kézi leképezés az X++ kóddal.
- A **populateTimesheetWeekFromEntry** metódus akkor is bővíthető, ha a **TSTimesheetEntry** objektumra leképezett egyéni mezőnek vissza kell írnia egy értéket a TSTimesheetLineweek adatbázis-táblázatba.

> [!NOTE]
> A következő példa a **firstOption**, illetve **secondOption** értékét menti, amelyet a felhasználó nyers karakterláncértékként választ az adatbázishoz. Ha az adatbázis mező **Felsorolás** típusú mező, akkor ezek az értékek kézileg is leképezhetők egy felsorolási értékre, majd menthetők az adatbázis-táblázat felsorolási mezőjébe.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Egyéni mezők megjelenítése az időnyilvántartás fejlécében

Az alábbiakban egy időnyilvántartást olvasó felhasználót bemutató képernyőkép látható a mobilalkalmazásból. A jobb felső sarokban lévő „További információ” gombot úgy állították be, hogy a „További részletek megtekintése” lehetőséget jelenítse meg.  

![További részletek megjelenítése parancs.](media/show-more.png)

Az alábbiakban az időnyilvántartás „Egyebek” részét bemutató képernyőkép látható a mobilalkalmazásból. A rendszer hozzáadta az „Időnyilvántartás kihasználtsági rátája (kiszámított egyéni mező)” nevű egyéni mezőt az időnyilvántartás fejlécszakaszához. Az egyéni mezőben beállított írásvédett érték a „0,667”.

![Egyebek szakasz.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>A TSTimesheetTable táblázat kibővítése egyéni mezővel

Tipikus helyzetekben valószínű, hogy az fejlécben szereplő egyéni mező adatait a rendszer a TSTimesheetHeader táblázatból kéri le. Azonban más táblázatok is használhatók, ha az adatok egy megadott TSTimesheetTable rekord alapján is lekérhetők, illetve ha nem rendelkeznek konkrét rekordkörnyezettel (ha például a mezőt írásvédettre állították a projektparaméterekben).

Ne feledje, hogy az egyéni mezőkhöz nem szükséges semmilyen háttérben tárolt adatbázisrekord. X++ logika alapján dinamikusan is létrehozhatók. Az alábbi példa ezt a megközelítést mutatja be.

A fejlécben található mezők mindig írásvédettek az alkalmazásban.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Parancssor használata a TSTimesheetSettings osztály buildCustomFieldList metódusán a fejlécszakaszban lévő mező megjelenítésére

Ez a kód a mező megjelenítési beállításait szabályozza az alkalmazásban. Ez szabályozza például a mező típusát, a címkét, hogy kötelező legyen-e a mező, és hogy melyik szakaszban jelenjen meg a mező.

Az alábbi példa egy kiszámított értéket mutat be az alkalmazás fejlécében.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Parancssor használata a TSTimesheetDetails osztály buildCustomFieldListForHeader metódusán az időnyilvántartási részletek megadására

A **buildCustomFieldListForHeader** metódus a mobilalkalmazás időnyilvántartási fejlécében lévő értékek megadására szolgál. Paraméterként egy TSTimesheetTable rekordot használ. Az adott rekord mezői az alkalmazásban szereplő egyénimező-értékek megadására használhatók. A következő példa semmilyen értéket nem olvas be az adatbázisból. Ehelyett az X++ logikát használja az alkalmazásban megjelenő kiszámított érték létrehozásához.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Egyéb konfigurálási/bővítési lehetőségek

### <a name="adding-additional-validation-for-the-app"></a>További ellenőrzés hozzáadása az alkalmazáshoz

Az időnyilvántartási funkció adatbázisszintű logilája továbbra is változatlanul fogja folytatni a működését. A mentési vagy küldési műveletek befejezésének megszakításához, illetve egy adott hibaüzenet megjelenítéséhez egy parancssori bővítménnyel adja hozzá a **throw error("message to user")** szöveget a kódhoz. Az alábbiakban három példát talál a hasznos bővíthető metódusokra:

- Ha a **validateWrite** az időnyilvántartási sor mentése során **hamis** értéket ad vissza a TSTimesheetLine táblázatban, akkor megjelenik egy hibaüzenet a mobilalkalmazásban.
- Ha a **validateSubmit** az időnyilvántartás alkalmazásban történő küldése során **hamis** értéket ad vissza a TSTimesheetTable táblázatban, akkor a rendszer megjelenít egy hibaüzenetet.
- Az **insert** metódus során a TSTimesheetLine táblázaton alkalmazott, mezők kitöltésére szolgáló logika (például a **Sortulajdonság**) továbbra is futni fog.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Alapértelmezett mezők elrejtése és írásvédettként való megjelölése konfigurálással

A projektparaméterek beállításaival írásvédetté teheti, illetve elrejtheti az alapértelmezett mezőket a mobilalkalmazásban. **Projektvezetési és könyvelési paraméterek** lap **Időnyilvántartás** fülének **Mobil időnyilvántartások** szakaszában állíthatja be a lehetőségeket.

![Projektparaméterek.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>A kiválasztásra elérhető tevékenységek módosítása a bővítmények segítségével

A projektekhez kiválasztható tevékenységeket a rendszer a **getActivitiesForProject()** és a **getActivityQuery()** metódusok alkalmazásával adja meg a **TsTimesheetProjectService** osztályban. Parancssort használva módosíthat ezen, hogy összeegyeztesse az üzleti helyzetet az adott projekt kiválasztásra elérhető tevékenységekkel.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Alapértelmezett projektkategória megadása az időnyilvántartási bejegyzésekben

Az alapértelmezett projektkategória időnyilvántartási bejegyzésbe történő megadása három szinten megy végbe. A kívánt működés eléréséhez parancssor használatával bővítheti a viselkedést bármelyik vagy akár mindegyik szinten. A rendszer az alábbi hierarchiát használja:

1. Az alkalmazás megpróbálja elhelyezni az alapértelmezett kategóriát a projekterőforrásból. Ez az alapértelmezett kategória a **TSTimesheetSettingsService** osztály **getCurrentUserResource** és **getDelegatedResourcesForCurrentUser** metódusaiban van beállítva.
2. Ha az alapértelmezett kategória nincs megadva a projekterőforrási szintjen, az alkalmazás a projekttevékenységből próbálja meg lekérni. Ez az alapértelmezett kategória a **TSTimesheetProjectService** osztály **getActivitiesForProject** metódusában van beállítva.
3. Ha az alapértelmezett kategória nincs megadva a projekttevékenységi szintjen, a rendszer lekéri a az alapértelmezett kategóriát a projektparaméterekből. Ez az alapértelmezett kategória a **TSTimesheetProjectService** osztály **getProjectDetailsbyRule** metódusában van beállítva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]