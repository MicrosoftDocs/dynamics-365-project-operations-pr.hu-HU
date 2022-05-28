---
title: Szervezeti egységek
description: Ez a témakör a szervezeti egységek fogalmát ismerteti, és ismerteti, hogyan hozhat létre és tarthat fenn szervezeti egységeket a Microsoftban Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581379"
---
# <a name="organizational-units-overview"></a>Szervezeti egységek – áttekintés

A Microsoftban Dynamics 365 Project Operations a *szervezeti egység* egy professzionális szolgáltató vállalat különálló csoportja vagy részlege, amely költségdíjakkal rendelkező számlázható erőforrásokat alkalmaz.

A különböző gyakorlati területeken vagy üzletágakban műszaki erőforrásokat foglalkoztató professzionális szolgáltató vállalatok esetében a szerepkör betöltésének költsége a gyakorlati területtől vagy az üzletágtól függően változhat, ahol a szerepkört betöltik. Ebben a forgatókönyvben a szervezeti egységek fogalma segít azáltal, hogy módot biztosít a számlázható szerepkörök csoportosítására egy olyan vállalat részlegében, amely külön költségstruktúrával rendelkezik ezekhez a szerepkörökhöz.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>A szervezeti egységek fogalma a projektműveletekben

A Project Operations programban egy szervezeti egység rendelkezik egy adott pénznemmel és konkrét önköltségi árlistával.

Egy szervezeti egység pénzneme a költségek nyomon követésére szolgáló elsődleges pénznem.

Az egyes szervezeti egységekhez egy vagy több önköltségi árlista is csatolható. A Project Operations a következő korlátozásokat korlátozza a szervezeti egységhez csatolható árlistákon:

- Az árlistáknak a szervezeti egység pénznemében kell lenniük.
- Az árlistáknak önköltségi árlistáknak kell lenniük.

Ezenkívül az Erőforrás entitás tartalmaz egy attribútumot a szervezeti egységhez. Minden erőforrás hozzárendelhető egy szervezeti egységhez.

### <a name="roles-of-organizational-units"></a>A szervezeti egységek szerepe

A szervezeti egység két szerepet tölt be a Projektműveletekben:

- **Szerződő részleg** – Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért. A szerződő részleget a fejlécben a **Szerződő részleg** mező azonosítja a **Lehetőség**, **Árajánlat**, **Projektszerződés** és **Projekt** oldalon.
- **Erőforrás-kezelő részleg** – Az a szervezeti egység, amelyhez egy erőforrás tartozik, vagy hozzá van rendelve. Ez a szervezeti egység erőforrásokat biztosít bizonyos szerepkörökhöz a munkanyilatkozatoknál (SOW) és projekteknél, amelyek a szerződő egység tulajdonában vannak.

![Szerződő egységek és erőforrás-kezelő részlegek.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Szervezeti egység GYIK

Az alábbiakban a szervezeti egységekkel kapcsolatos leggyakrabban elhangzó kérdéseket válaszoljuk meg.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hogyan kapcsolódik a Project Operations szervezeti egység entitása a Dynamics 365-ben már létező Szervezeti entitáshoz?

A Dynamics 365 szervezet entitása egy globális Dynamics 365-példány nevét jelöli. Ez a név általában a globális vállalat neve is.

A Szervezeti egység entitás a globális vállalat egy csoportjának vagy osztályának felel meg. Ez a csoport vagy osztály szerepköröket és önköltségi árlistát tartalmaz ezekhez a szerepkörökhöz, ezek a szerepkörök és árlisták pedig eltérnek a vállalaton belüli egyéb csoportok vagy osztályok szerepköreitől és árától.

A Project Operations telepítésekor a szervezet alapján létrejön egy alapértelmezett szervezeti egység. Minden létező erőforrás hozzá van rendelve az alapértelmezett szervezeti egységhez. Ha új Active Directory-felhasználókat vagy erőforrásokat importál a Dynamics 365-be, a felhasználói importálási folyamat hozzárendeli őket a Project Operations alapértelmezett szervezeti egységéhez.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Miben különbözik a szervezeti egység entitás a Részleg entitástól?

A Dynamics 365 alkalmazásban a részleg entitás egy biztonsági konstrukció. Egy részleg felhasználójának társítása határozza meg azokat az entitásokat és entitás-rekordokat, amelyekhez a felhasználó hozzáférhet. Meghatározza továbbá a felhasználó által az entitás rekordjaihoz tartozó engedélyeket (Létrehozás, Olvasás, Írás, Törlés, Hozzáfűzés, Hozzáadás, Hozzárendelés vagy Megosztás).

A Szervezeti egység entitás egy olyan vállalati csoportot vagy részleget reprezentál, amely a hozzárendelt alkalmazottakra vonatkozó költséggel rendelkezik. Az erőforrások szervezeti egységhez való társítása határozza meg az erőforrás költségét egy projekt aktivitási arányánál.

A Dynamics 365 telepítése során optimalizálja a részlegek hierarchiájának biztonsági engedélyezését és a felhasználók részlegek számára történő hozzárendelését. Rendelje hozzá azokat a felhasználókat, akiknek általában ugyanazokhoz a bejegyzésekhez kell hozzáférniük, ugyanannál a részlegnél. A szervezeti egységnek nincs hatása a biztonsági engedélyezésre vagy a hozzáférésre.

**Példa, amely egy lehetséges különbséget mutat a szervezeti egységek és részlegek modellezésében**

A Contoso Ltd. rendelkezik a Microsoft egy virágzó technológiai gyakorlatával. Ferenc és Etelka mindketten C\#-fejlesztők, de Etelka az Egyesült Államokban dolgozik, Ferenc pedig Indiában. A legtöbb projektfeladathoz mind Contoso indiából, mind Contoso Egyesült Államokból származó erőforrásokra van szükség, és Prakash és Tricia ugyanolyan szintű biztonsági hozzáférést igényel az ezen a gyakorlati területen lévő projektekhez. A Contoso India fejlesztőinek költsége azonban jelentősen eltér a Contoso USA fejlesztőinek költségétől.

Az alábbiakban az alábbi optimális módja annak, hogy a Dynamics 365 és a Project Operations használatával megtervezze ezt a forgatókönyvet.

1. Hozzon létre egy Microsoft technológiai gyakorlatot egy részlegre vonatkozóan, és társítsa ezzel Ferencet és Etelkát. Ily módon ön segít biztosítani, hogy mindkét alkalmazott ugyanolyan szintű biztonsági hozzáféréssel rendelkezzen az adott gyakorlati területen lévő projektekhez. Mindketten ellenőrizhetik az előrehaladást, és jelentést tehetnek az időről, a költségekről, az anyaghasználatról és a tevékenységfrissítésekről.
2. Hozzon létre két szervezeti egységet annak érdekében, hogy a projekt költsége helyesen jelenjen meg.
3. Társítsd Triciát Contoso Egyesült Államokkal és Prakash-t Contoso Indiával.
4. Rendelje hozzá a megfelelő önköltségi árlistát mindkét szervezeti egységhez. Ily módon ön segít biztosítani, hogy a Prakash és a Tricia projektjében rögzített költségek pontosan tükrözzék az Contoso Egyesült Államok és Contoso India közötti költségkülönbséget.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Tartoznak szervezeti egységek a Dynamics 365 alkalmazás értékesítési területeihez?

Nincs társítás vagy kapcsolat az értékesítési területek és a szervezeti egységek között. Az értékesítési terület jellemzően olyan földrajzi terület, ahol az értékesítés történik. Az egyes értékesítési területekhez értékesítési árlista társítható.

A szervezeti egység a vállalat olyan belső csoportja vagy részlege, amely a más részlegek vagy külső vevők számára értékesített szerepkörök egy csoportjának költségeit követi nyomon.

**Példa, amely egy lehetséges különbséget mutat a szervezeti egységek és értékesítési területek modellezésében**

A Contoso Ltd. két fejlesztési központtal rendelkezik: Contoso USA és Contoso India. Az erőforrások költsége nagymértékben eltér a két fejlesztési központ között. Contoso informatikai (IT) szolgáltatásait számos nemzetközi piacon értékesíti, például Latin-Amerikában, Észak-Amerikában, az ázsiai-csendes-óceáni térségben, Nyugat-Európában és a Közel-Keleten. Az ugyanahhoz a projekt-szerepkörhöz tartozó számlázási díjak ezek között a piacok között is széles körben változhatnak. A Contoso USA-t és a Contoso Indiát szervezeti egységként kell beállítani, és mindegyik szervezeti egységnek saját önköltségi árlistával kell rendelkeznie. Ázsiát és a csendes-óceáni térséget, Latin-Amerikát, Észak-Amerikát, Nyugat-Európát és a Közel-Keletet értékesítési területként kell beállítani, és minden értékesítési területnek rendelkeznie kell saját értékesítési árlistával.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miért van korlátozás az árlisták szervezeti egységekkel való társítására?

Az értékesítési árképzés általában egyedi azokon a földrajzi területeken vagy piacokon, ahol a szolgáltatásokat értékesítik. Egy vállalat belső divíziói általában nem rendelkeznek saját értékesítési árképzéssel a hasonló típusú szolgáltatásoknál. A belső divíziók értékesített termékeinek költségei azonban eltérőek, attól függően, hogy milyen képzettséggel rendelkeznek az általuk foglalkoztatott személyek, és milyen munkakörülmények jellemzik a régió működését. Mivel a szervezeti egységek a vállalat belső részlegei, csak önköltségi árlistákkal rendelkezhetnek.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Miért nem társíthatjuk az eladási árlistákat a szervezeti egységekkel?

A Project Operations programban az eladási árlisták társíthatók vevőkhöz és értékesítési területekhez. Az olyan tranzakciós entitások, mint a Lehetőség, az Ajánlat, a Projektszerződés és a Project, a vevői számlához vagy az értékesítési területhez csatolt eladási árlistákat használják a projektmegbízáshoz kapcsolódó számladíjak és potenciális bevételek meghatározásához.

A önköltségi árlisták szervezeti egységekhez vannak társítva. Az olyan tranzakciós entitások, mint a Lehetőség, az Ajánlat, a Projektszerződés és a Projekt, az ajánlatkérőhöz csatolt önköltségi árlistákat használják a projektkapcsolat költségeinek meghatározásához.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>A szervezeti egységek hierarchikus a projektműveletekben?

Nem. A Project Operations aktuális kiadásában a szervezeti egységek nincsenek hierarchikus. Ezért nem hajthatja végre a következő feladatokat:

- Konfiguráljon egy mintát a hierarchián áthaladó alapértelmezett önköltségi árak megadásához.
- A szervezeti egységhierarchia különböző szintjein összesített bevétel vagy költség jelentése.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Nagy multinacionális vállalat vagyunk, amely komplex, többszintű hierarchiával rendelkezik a költségközpontok, részlegek és számlázási irodák között. Hogyan használhatjuk a legjobban a szervezeti egységek fogalmát a Project Operations jelenlegi verziójában?

Ha költségközpontok, részlegek, számlázási irodák stb. összetett hierarchiájával rendelkezik, állítsa be a hierarchia levélcsomópontjait különálló szervezeti egységként.

Az alábbi példa egy tipikus hierarchiát mutat be.

**Contoso India**

- SAP-gyakorlat

    - Műszaki tanácsadók
    - Funkcionális tanácsadók

- Microsoft technológiai gyakorlat

    - Műszaki tanácsadók
    - Funkcionális tanácsadók

**Contoso USA**

- SAP-gyakorlat

    - Műszaki tanácsadók
    - Funkcionális tanácsadók

- Microsoft technológiai gyakorlat

    - Műszaki tanácsadók
    - Funkcionális tanácsadók

Ha a hierarchia hasonlít erre a példára, akkor azt lapos listaként kell beállítania, az itt látható módon:

- Contoso India – SAP-gyakorlat – Műszaki tanácsadók
- Contoso India – SAP-gyakorlat – Funkcionális tanácsadók
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso USA – SAP-gyakorlat – Műszaki tanácsadók
- Contoso USA – SAP-gyakorlat – Funkcionális tanácsadók
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kis professzionális szolgáltatást nyújtó vállalat vagyunk, amely egyetlen részlegként működik. Hogyan használhatjuk a legjobban a szervezeti egységek fogalmát a Project Operations jelenlegi verziójában?

Ha vállalata egy önköltségi árlistát tartalmazó egyetlen egységként működik, nem kell semmilyen szervezeti egységet beállítania. A Project Operations telepítése egy alapértelmezett szervezeti egységet hoz létre, amelynek neve megegyezik a szervezet nevével. Alapértelmezés szerint minden felhasználó hozzá van rendelve a szervezeti egységhez. Ha a rendszernek ki kell választania egy szervezeti egységet, akkor alapértelmezés szerint ez a szervezeti egység lesz kiválasztva.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Ha létrehoz egy projektet árajánlat vagy projekt-szerződéssor alapján, az alapértelmezett szerződő részleg az árajánlatból vagy a projektszerződésből származik. Mi az alapértelmezett szerződéskötési egység, ha egy projektet értékesítési entitások, például Ajánlat vagy Projektszerződés előtt hoznak létre?

Ha önmagában egy projektet hoznak létre, a projekt alapértelmezett szerződő részlege az a felhasználó, aki létrehozza azt. Ez a felhasználó egyben az alapértelmezett projektvezető is. Ha a projekt egy értékesítési entitáshoz, például ajánlathoz vagy projektszerződéshez van leképezve, a projekt összehúzó egysége inkább az értékesítési egységen alapul. Ebben az esetben a projektbecslések újraszámíthatók, mivel az önköltségi árlista segítségével kiszámíthatók a költségbecslés változásai, a szerződő részleg módosulása esetén. Az eladási árlista a módosítandó eladási becslések kiszámítására szolgál, hogy azok szinkronban legyenek az ajánlat projektárlistájával.

A **projekt Szerződési egység** és **Pénznem** mezői szerkesztésre zárolva vannak, mert szinkronban kell lenniük annak az értékesítési egységnek (ajánlatnak vagy projektszerződésnek) az értékeivel, amelyhez a projekt hozzá van rendelve.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Szervezeti egységek létrehozása és karbantartása a Projektműveletekben

Szervezeti egység project műveletekben való létrehozásához hajtsa végre az alábbi lépéseket.

1. Nyissa meg a **Szervezeti egységek \> beállításai** lehetőséget.
2. Válassza az **Új** lehetőséget.
3. **Az Általános** terület Név **mezőjébe** írja be a szervezeti egység nevét. Ezután állítsa be a többi mezőt a kívánt módon.
4. Válassza a Mentés **lehetőséget** a rekord létrehozásához, hogy folytathassa a szerkesztést.
5. Az Önköltségi árlisták csoportban **válassza** ki a pluszjelet (**+**) árlista hozzáadásához. Itt csak olyan árlistákat adhat hozzá, amelyek költségkörnyezettel **rendelkeznek**.
6. **A Név** mezőben jelölje ki a Keresés **gombot, és válassza ki azt az** árlistát, amelyet elérhetővé szeretne tenni a szervezeti egység számára. Szükség szerint folytassa az árlisták hozzáadását.
7. Ha befejezte az árlisták hozzáadását, válassza a Mentés **lehetőséget** a lap jobb alsó sarkában.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
