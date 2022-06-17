---
title: Szervezeti egységek
description: Ez a cikk a szervezeti egységek fogalmát ismerteti, és elmagyarázza, hogyan hozhat létre és tarthat fenn szervezeti egységeket a Microsoftban Dynamics 365 Project Operations.
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
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921627"
---
# <a name="organizational-units-overview"></a>Szervezeti egységek áttekintése

A Microsoftban Dynamics 365 Project Operations a *szervezeti egység* egy különálló csoport vagy részleg egy professzionális szolgáltató vállalatnál, amely költségtérítéssel rendelkező számlázható erőforrásokat alkalmaz.

Azoknál a professzionális szolgáltató vállalatoknál, amelyek különböző gyakorlati területeken vagy üzletágakban alkalmaznak műszaki erőforrásokat, a szerepkör betöltésének költsége változhat, attól függően, hogy a szerepkört melyik szakterületen vagy üzletágban töltik be. Ebben a forgatókönyvben a szervezeti egységek fogalma segít abban, hogy lehetővé teszi a számlázható szerepkörök csoportosítását egy olyan vállalat részlegében, amely külön költségstruktúrával rendelkezik az adott szerepkörökhöz.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>A szervezeti egységek fogalma a projektműveletekben

A Project Operationsben egy szervezeti egység egy adott pénznemmel és egy adott önköltségi árlistákkal rendelkezik.

Egy szervezeti egység pénzneme a költségek nyomon követésére szolgáló elsődleges pénznem.

Az egyes szervezeti egységekhez egy vagy több önköltségi árlista is csatolható. A Project Operations a következő korlátozásokat alkalmazza a szervezeti egységhez csatolható árlistákon:

- Az árlistáknak a szervezeti egység pénznemében kell lenniük.
- Az árlistáknak önköltségi árlistáknak kell lenniük.

Ezenkívül az Erőforrás entitás tartalmaz egy attribútumot a szervezeti egységhez. Minden erőforrás hozzárendelhető egy szervezeti egységhez.

### <a name="roles-of-organizational-units"></a>A szervezeti egységek szerepe

A szervezeti egység két szerepet játszik a projektműveletekben:

- **Szerződő részleg** – Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért. A szerződő részleget a fejlécben a **Szerződő részleg** mező azonosítja a **Lehetőség**, **Árajánlat**, **Projektszerződés** és **Projekt** oldalon.
- **Erőforrás-kezelő részleg** – Az a szervezeti egység, amelyhez egy erőforrás tartozik, vagy hozzá van rendelve. Ez a szervezeti egység erőforrásokat biztosít bizonyos szerepkörökhöz a munkanyilatkozatoknál (SOW) és projekteknél, amelyek a szerződő egység tulajdonában vannak.

![Szerződő egységek és erőforrás-kezelő részlegek.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Szervezeti egység GYIK

Az alábbiakban a szervezeti egységekkel kapcsolatos leggyakrabban elhangzó kérdéseket válaszoljuk meg.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hogyan kapcsolódik a Project Operations Szervezeti egység entitása a Dynamics 365 rendszerben már létező Szervezet entitáshoz?

A Dynamics 365 Szervezet entitása egy globális Dynamics 365-példány nevét jelöli. Ez a név általában a globális vállalat neve is.

A Szervezeti egység entitás a globális vállalat egy csoportjának vagy osztályának felel meg. Ez a csoport vagy osztály szerepköröket és önköltségi árlistát tartalmaz ezekhez a szerepkörökhöz, ezek a szerepkörök és árlisták pedig eltérnek a vállalaton belüli egyéb csoportok vagy osztályok szerepköreitől és árától.

A Project Operations telepítésekor a szervezet alapján létrejön egy alapértelmezett szervezeti egység. Minden létező erőforrás hozzá van rendelve az alapértelmezett szervezeti egységhez. Ha új Active Directory-felhasználókat vagy -erőforrásokat importál a Dynamics 365-be, a felhasználói importálási folyamat hozzárendeli őket a Project Operations alapértelmezett szervezeti egységéhez.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Miben különbözik a Szervezeti egység entitás a Részleg entitástól?

A Dynamics 365 alkalmazásban a részleg entitás egy biztonsági konstrukció. Egy részleg felhasználójának társítása határozza meg azokat az entitásokat és entitás-rekordokat, amelyekhez a felhasználó hozzáférhet. Meghatározza továbbá a felhasználó által az entitás rekordjaihoz tartozó engedélyeket (Létrehozás, Olvasás, Írás, Törlés, Hozzáfűzés, Hozzáadás, Hozzárendelés vagy Megosztás).

A Szervezeti egység entitás egy olyan vállalati csoportot vagy részleget reprezentál, amely a hozzárendelt alkalmazottakra vonatkozó költséggel rendelkezik. Az erőforrások szervezeti egységhez való társítása határozza meg az erőforrás költségét egy projekt aktivitási arányánál.

A Dynamics 365 telepítése során optimalizálja a részlegek hierarchiájának biztonsági engedélyezését és a felhasználók részlegek számára történő hozzárendelését. Rendelje hozzá azokat a felhasználókat, akiknek általában ugyanazokhoz a bejegyzésekhez kell hozzáférniük, ugyanannál a részlegnél. A szervezeti egységnek nincs hatása a biztonsági engedélyezésre vagy a hozzáférésre.

**Példa, amely egy lehetséges különbséget mutat be a szervezeti egységek és üzleti egységek modellezésében**

A Contoso Ltd. rendelkezik a Microsoft egy virágzó technológiai gyakorlatával. Ferenc és Etelka mindketten C\#-fejlesztők, de Etelka az Egyesült Államokban dolgozik, Ferenc pedig Indiában. A projektfeladatok többsége erőforrásokat igényel mind Contoso Indiából, mind Contoso EGYESÜLT ÁLLAMOKból, Prakash és Tricia pedig ugyanolyan szintű biztonsági hozzáférést igényel a projektekhez ezen a gyakorlati területen. A Contoso India fejlesztőinek költsége azonban jelentősen eltér a Contoso USA fejlesztőinek költségétől.

Itt van egy optimális módszer a forgatókönyv tervezésére a Dynamics 365 és a Project Operations használatával.

1. Hozzon létre egy Microsoft technológiai gyakorlatot egy részlegre vonatkozóan, és társítsa ezzel Ferencet és Etelkát. Ily módon segít biztosítani, hogy mindkét alkalmazott azonos szintű biztonsági hozzáféréssel rendelkezzen az adott gyakorlati területen lévő projektekhez. Mindketten képesek lesznek ellenőrizni az előrehaladást, és jelenteni az időt, a költségeket, az anyaghasználatot és a tevékenységfrissítéseket.
2. Hozzon létre két szervezeti egységet, amelyek segítenek biztosítani, hogy a projekt költsége megfelelően tükröződjön.
3. Társítsd Triciát Contoso USA-val és Prakash-t Contoso Indiával.
4. Rendelje hozzá a megfelelő önköltségi árlistát mindkét szervezeti egységhez. Ily módon segít biztosítani, hogy a Prakash és Tricia projektjében rögzített költségek pontosan tükrözzék a Contoso Usa és Contoso India közötti költségkülönbséget.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Tartoznak szervezeti egységek a Dynamics 365 alkalmazás értékesítési területeihez?

Nincs társítás vagy kapcsolat az értékesítési területek és a szervezeti egységek között. Az értékesítési terület jellemzően olyan földrajzi terület, ahol az értékesítés történik. Az egyes értékesítési területekhez értékesítési árlista társítható.

A szervezeti egység a vállalat olyan belső csoportja vagy részlege, amely a más részlegek vagy külső vevők számára értékesített szerepkörök egy csoportjának költségeit követi nyomon.

**Példa, amely egy lehetséges különbséget mutat be a szervezeti egységek és értékesítési területek modellezésében**

A Contoso Ltd. két fejlesztési központtal rendelkezik: Contoso USA és Contoso India. Az erőforrások költsége nagymértékben eltér a két fejlesztési központ között. Contoso számos nemzetközi piacon értékesíti informatikai (IT) szolgáltatásait, például Latin-Amerikában, Észak-Amerikában, Ázsiában és a csendes-óceáni térségben, Nyugat-Európában és a Közel-Keleten. Az ugyanahhoz a projekt-szerepkörhöz tartozó számlázási díjak ezek között a piacok között is széles körben változhatnak. A Contoso USA-t és a Contoso Indiát szervezeti egységként kell beállítani, és mindegyik szervezeti egységnek saját önköltségi árlistával kell rendelkeznie. Ázsiát és a csendes-óceáni térséget, Latin-Amerikát, Észak-Amerikát, Nyugat-Európát és a Közel-Keletet értékesítési területként kell beállítani, és minden értékesítési területnek rendelkeznie kell saját értékesítési árlistával.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miért van korlátozás az árlisták szervezeti egységekkel való társítására?

Az értékesítési árképzés általában egyedi azokon a földrajzi területeken vagy piacokon, ahol a szolgáltatásokat értékesítik. Egy vállalat belső divíziói általában nem rendelkeznek saját értékesítési árképzéssel a hasonló típusú szolgáltatásoknál. A belső divíziók értékesített termékeinek költségei azonban eltérőek, attól függően, hogy milyen képzettséggel rendelkeznek az általuk foglalkoztatott személyek, és milyen munkakörülmények jellemzik a régió működését. Mivel a szervezeti egységek a vállalat belső részlegei, csak önköltségi árlistákkal rendelkezhetnek.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Miért nem tudjuk társítani az eladási árlistákat a szervezeti egységekhez?

A Project Operationsben az értékesítési árlisták hozzárendelhetők a vevőkhöz és az értékesítési területekhez. Az olyan tranzakciós entitások, mint a Lehetőség, az Árajánlat, a Projektszerződés és a Projekt, a vevői számlához vagy az értékesítési területhez csatolt eladási árlistákat használják a számlázási díjak és a projekttevékenység lehetséges bevételeinek meghatározásához.

A önköltségi árlisták szervezeti egységekhez vannak társítva. Az olyan tranzakciós entitások, mint a Lehetőség, az Árajánlat, a Projektszerződés és a Projekt, a szerződő egységhez csatolt önköltségi árlistákat használják a projektfelépítés költségeinek meghatározásához.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>A szervezeti egységek hierarchikus a Project Operationsben?

Nem. A Project Operations jelenlegi kiadásában a szervezeti egységek nem hierarchikus. Ezért nem hajthatja végre a következő feladatokat:

- Állítson be egy mintát az alapértelmezett önköltségi árak megadásához, amely felfelé halad a hierarchián.
- A szervezetiegység-hierarchia különböző szintjein felhalmozott bevétel vagy költség jelentése.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Nagy multinacionális cég vagyunk, amely összetett, többszintű hierarchiával rendelkezik költséghelyekből, divíziókból és számlázási irodákból. Hogyan tudjuk a legjobban kihasználni a szervezeti egységek fogalmát a Project Operations jelenlegi verziójában?

Ha a költséghelyek, divíziók, számlázási irodák stb. összetett hierarchiája van, állítsa be a hierarchia levélcsomópontjait különálló szervezeti egységekként.

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

Ha a hierarchia hasonlít erre a példára, akkor azt egy egyszerű listaként kell beállítania az itt látható módon:

- Contoso India – SAP-gyakorlat – Műszaki tanácsadók
- Contoso India – SAP-gyakorlat – Funkcionális tanácsadók
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso USA – SAP-gyakorlat – Műszaki tanácsadók
- Contoso USA – SAP-gyakorlat – Funkcionális tanácsadók
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kis professzionális szolgáltatást nyújtó vállalat vagyunk, amely egyetlen részlegként működik. Hogyan tudjuk a legjobban kihasználni a szervezeti egységek fogalmát a Project Operations jelenlegi verziójában?

Ha vállalata egy önköltségi árlistát tartalmazó egyetlen egységként működik, nem kell semmilyen szervezeti egységet beállítania. A Project Operations telepítése egy alapértelmezett szervezeti egységet hoz létre, amelynek neve megegyezik a szervezet nevével. Alapértelmezés szerint minden felhasználó hozzá van rendelve a szervezeti egységhez. Ha a rendszernek ki kell választania egy szervezeti egységet, akkor alapértelmezés szerint ez a szervezeti egység lesz kiválasztva.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Ha létrehoz egy projektet árajánlat vagy projekt-szerződéssor alapján, az alapértelmezett szerződő részleg az árajánlatból vagy a projektszerződésből származik. Mi az alapértelmezett szerződéses egység, ha egy projektet olyan értékesítési entitások előtt hoznak létre, mint az Árajánlat vagy a Projektszerződés?

Ha önmagában egy projektet hoznak létre, a projekt alapértelmezett szerződő részlege az a felhasználó, aki létrehozza azt. Ez a felhasználó egyben az alapértelmezett projektvezető is. Ha a projekt egy értékesítési entitásra, például árajánlatra vagy projektszerződésre van leképezve, akkor a projekt szerződő egysége az értékesítési entitáson alapul. Ebben az esetben a projektbecslések újraszámíthatók, mivel az önköltségi árlista segítségével kiszámíthatók a költségbecslés változásai, a szerződő részleg módosulása esetén. Az eladási árlista a rendszer arra szolgál, hogy kiszámítsa azokat az értékesítési becsléseket, amelyek úgy módosulnak, hogy azok szinkronban legyenek az árajánlat projekt árlistájával.

A **projekt Szerződéses egység** és **Pénznem** mezői szerkesztésre zárolva vannak, mert szinkronban kell lenniük annak az értékesítési entitásnak (árajánlat vagy projektszerződés) az értékeivel, amelyhez a projekt hozzá van rendelve.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Szervezeti egységek létrehozása és karbantartása a Project Operationsben

Ha szervezeti egységet szeretne létrehozni a Project Operationsben, kövesse az alábbi lépéseket.

1. Lépjen a Szervezeti egységek beállításai **lapra.\>**
2. Válassza az **Új** lehetőséget.
3. **Az Általános** terület Név **mezőjében** adja meg a szervezeti egység nevét. Ezután állítsa be a többi mezőt szükség szerint.
4. Válassza a Mentés **lehetőséget** a rekord létrehozásához, hogy továbbra is szerkeszthesse.
5. Az Önköltségi árlisták **alatt** válassza a pluszjelet (**+**) az árlista hozzáadásához. Itt csak olyan árlistákat adhat hozzá, amelyek költségkörnyezettel **rendelkeznek**.
6. **A Név** mezőben válassza a **Keresés** gombot, és válassza ki azt az árlistát, amelyet elérhetővé szeretne tenni a szervezeti egység számára. Szükség szerint folytassa az árlisták hozzáadását.
7. Ha befejezte az árlisták hozzáadását, válassza a Mentés **lehetőséget** az oldal jobb alsó sarkában.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
