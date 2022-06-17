---
title: Speciális szervezeti egységek
description: Ez a cikk a szervezeti egységekről nyújt tájékoztatást Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: dd9de490b7d6d847e3226b371e06ac671a7836a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927101"
---
# <a name="about-organizational-units"></a>A szervezeti egységekről 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Egy Dynamics 365 Project Service Automation szervezeti egység egy másik csoport vagy osztály egy professzionális szolgáltatásokat nyújtó vállalatnál, amely más költség arányú számlázható erőforrásokat alkalmaz.

A különböző gyakorlati területeken vagy üzletágakban technikai forrásokat foglalkoztató professzionális szolgáltatásokat nyújtó vállalatok esetében az egyik gyakorlati területen vagy üzletágban egy szerepkör kitöltésének költsége eltérhet egy másik gyakorlati területen vagy üzletágban fellépő költségtől. A szervezeti egységek rendszere ebben a forgatókönyvben segítséget nyújt egy vállalati osztály számlázható szerepköreinek csoportosításában, amely eltérő költségstruktúrával rendelkezik.

## <a name="key-attributes-and-associations-of-organizational-units"></a>A szervezeti egységek legfontosabb attribútumai és társításai

Egy PSA szervezeti egység meghatározott pénznemmel és önköltségi árlistával rendelkezik.

Egy szervezeti egység pénzneme a költségek nyomon követésére szolgáló elsődleges pénznem.

Az egyes szervezeti egységekhez egy vagy több önköltségi árlista is csatolható. A PSA a következő korlátozásokat szabja a szervezeti egységhez csatolható árlisták esetén:

- Az árlisták a szervezeti egység pénznemében jelennek meg.
- Az árlisták csak önköltségi árlisták lehetnek.

Emellett az erőforrás entitás szervezeti egységéhez tartozik egy attribútum. Minden erőforrás hozzárendelhető egy szervezeti egységhez.

## <a name="roles-of-organizational-units"></a>A szervezeti egységek szerepe

A szervezeti egységek két szerepet töltenek be a PSA-ban:

- **Szerződő részleg** – Az a szervezeti egység, amely azt a vállalatot vagy részleget reprezentálja, amely elsősorban felelős az értékesítés megnyeréséért és a munka és szolgáltatások ügyfélnek történő leszállításáért. A szerződő részleget a fejlécben a **Szerződő részleg** mező azonosítja a **Lehetőség**, **Árajánlat**, **Projektszerződés** és **Projekt** oldalon.
- **Erőforrás-kezelő részleg** – Az a szervezeti egység, amelyhez egy erőforrás tartozik, vagy hozzá van rendelve. Ez a szervezeti egység erőforrásokat biztosít bizonyos szerepkörökhöz a munkanyilatkozatoknál (SOW) és projekteknél, amelyek a szerződő egység tulajdonában vannak.

> ![Szerződő egységek és erőforrás-kezelő részlegek.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Szervezeti egység GYIK

Az alábbiakban a szervezeti egységekkel kapcsolatos leggyakrabban elhangzó kérdéseket válaszoljuk meg.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hogyan kapcsolódik a Dynamics 365 alkalmazásban már létező Szervezet entitáshoz a PSA Szervezeti egység entitása?

A Microsoft Dynamics 365 alkalmazás Szervezet entitása a globális Dynamics 365-példány nevének felel meg. Ez a név általában a globális vállalat neve is.

A Szervezeti egység entitás a globális vállalat egy csoportjának vagy osztályának felel meg. Ez a csoport vagy osztály szerepköröket és önköltségi árlistát tartalmaz ezekhez a szerepkörökhöz, ezek a szerepkörök és árlisták pedig eltérnek a vállalaton belüli egyéb csoportok vagy osztályok szerepköreitől és árától.

A PSA telepítésekor egy alapértelmezett szervezeti egység jön létre a szervezet alapján. Minden létező erőforrás hozzá van rendelve az alapértelmezett szervezeti egységhez. Ha az Active Directory bármelyik új felhasználóját vagy erőforrását importálja a Dynamics 365 rendszerbe, akkor a felhasználói importálási folyamat a PSA alapértelmezett szervezeti egységéhez rendeli hozzá azokat.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Miben különbözik a szervezeti egység entitás a részleg entitástól?

A Dynamics 365 alkalmazásban a részleg entitás egy biztonsági konstrukció. Egy részleg felhasználójának társítása határozza meg azokat az entitásokat és entitás-rekordokat, amelyekhez a felhasználó hozzáférhet. Meghatározza továbbá a felhasználó által az entitás rekordjaihoz tartozó engedélyeket (Létrehozás, Olvasás, Írás, Törlés, Hozzáfűzés, Hozzáadás, Hozzárendelés vagy Megosztás).

A Szervezeti egység entitás egy olyan vállalati csoportot vagy részleget reprezentál, amely a hozzárendelt alkalmazottakra vonatkozó költséggel rendelkezik. Az erőforrások szervezeti egységhez való társítása határozza meg az erőforrás költségét egy projekt aktivitási arányánál.

A Dynamics 365 telepítése során optimalizálja a részlegek hierarchiájának biztonsági engedélyezését és a felhasználók részlegek számára történő hozzárendelését. Rendelje hozzá azokat a felhasználókat, akiknek általában ugyanazokhoz a bejegyzésekhez kell hozzáférniük, ugyanannál a részlegnél. A szervezeti egységnek nincs hatása a biztonsági engedélyezésre vagy a hozzáférésre.

#### <a name="example-of-organizational-units-and-business-units"></a>Példa szervezeti egységekre és részlegekre

A Contoso Ltd. rendelkezik a Microsoft egy virágzó technológiai gyakorlatával. Ferenc és Etelka mindketten C\#-fejlesztők, de Etelka az Egyesült Államokban dolgozik, Ferenc pedig Indiában. A projektek nagy részéhez szükség van a Contoso India és a Contoso USA erőforrásaira is, így Ferencnek és Etelkának ugyanolyan szintű biztonsági hozzáférésre van szüksége a gyakorlati terület projektjeire vonatkozóan. A Contoso India fejlesztőinek költsége azonban jelentősen eltér a Contoso USA fejlesztőinek költségétől.

Az alábbiakban optimális megoldást talál ennek a forgatókönyvnek a megoldására a Dynamics 365 és a PSA használatával.

1. Hozzon létre egy Microsoft technológiai gyakorlatot egy részlegre vonatkozóan, és társítsa ezzel Ferencet és Etelkát. Így biztosítható, hogy mindkét alkalmazott ugyanolyan szintű biztonsági hozzáféréssel rendelkezzen az adott gyakorlati területen lévő minden projekthez. Mindketten ellenőrizhetik a folyamatot, és jelenthetik az idő, a költségek és a feladatok frissítéseit. 
2. Hozzon létre két szervezeti egységet, amelyek segítségével biztosítható, hogy a projekt költségét helyesen tükrözze a rendszer. 
3. Társítsa Etelkát a Contoso USA-hoz, Ferencet pedig a Contoso Indiához.
4. Rendelje hozzá a megfelelő önköltségi árlistát mindkét szervezeti egységhez. Így biztosíthatja, hogy a projektben Ferenc és Etelka által rögzített költségek pontosan tükrözzék a Contoso USA és a Contoso India közötti különbségeket.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Tartoznak szervezeti egységek a Dynamics 365 alkalmazás értékesítési területeihez?

Nincs társítás vagy kapcsolat az értékesítési területek és a szervezeti egységek között. Az értékesítési terület jellemzően olyan földrajzi terület, ahol az értékesítés történik. Az egyes értékesítési területekhez értékesítési árlista társítható.

A szervezeti egység a vállalat olyan belső csoportja vagy részlege, amely a más részlegek vagy külső vevők számára értékesített szerepkörök egy csoportjának költségeit követi nyomon.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Példa szervezeti egységekre és értékesítési területekre

A Contoso Ltd. két fejlesztési központtal rendelkezik: Contoso USA és Contoso India. Az erőforrások költségei nagyban különböznek a két fejlesztési központban.

A Contoso számos nemzetközi piacon értékesíti informatikai szolgáltatásait, többek között Latin-Amerikában, Észak-Amerikában, Ázsiában és a csendes-óceáni térségben, Nyugat-Európában és a Közel-Keleten. Az ugyanahhoz a projekt-szerepkörhöz tartozó számlázási díjak ezek között a piacok között is széles körben változhatnak.

A Contoso USA-t és a Contoso Indiát szervezeti egységként kell beállítani, és mindegyik szervezeti egységnek saját önköltségi árlistával kell rendelkeznie. Ázsiát és a csendes-óceáni térséget, Latin-Amerikát, Észak-Amerikát, Nyugat-Európát és a Közel-Keletet értékesítési területként kell beállítani, és minden értékesítési területnek rendelkeznie kell saját értékesítési árlistával.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Miért van korlátozás az árlisták szervezeti egységekkel való társítására? 

Az értékesítési árképzés általában egyedi azokon a földrajzi területeken vagy piacokon, ahol a szolgáltatásokat értékesítik. Egy vállalat belső divíziói általában nem rendelkeznek saját értékesítési árképzéssel a hasonló típusú szolgáltatásoknál. A belső divíziók értékesített termékeinek költségei azonban eltérőek, attól függően, hogy milyen képzettséggel rendelkeznek az általuk foglalkoztatott személyek, és milyen munkakörülmények jellemzik a régió működését. Mivel a szervezeti egységek a vállalat belső részlegei, csak önköltségi árlistákkal rendelkezhetnek.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Miért nem társíthatók az értékesítési árlisták a szervezeti egységekhez?

A PSA-ban az értékesítési árlisták az ügyfelekhez és az értékesítési területekhez rendelhetők hozzá. A tranzakciós entitásokat – például a Lehetőséget, az Árajánlatot, a Projektszerződést és a Projektet – az ügyfél fiókjához vagy az értékesítési területhez rendelik hozzá, hogy értékesítési árlisták segítségével megállapítsák a számlázási díjakat és a potenciális bevételt a projekt aktivitási arányánál.

A önköltségi árlisták szervezeti egységekhez vannak társítva. A tranzakciós entitások – például a Lehetőség, az Árajánlat, a Projektszerződés és a Projekt – olyan önköltségi árlistákat használnak, amelyek a szerződő részleghez vannak csatolva a projektek teljesítési költségeinek meghatározásához.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Hierarchikusak a szervezeti egységek a PSA-ban?

Szám A PSA jelenlegi kiadásában a szervezeti egységek nem hierarchikusak. Ez azt jelenti, hogy nem lehet:

- Alapértelmezés szerinti önköltségi árakra vonatkozó mintát konfigurálni, amely végighalad egy hierarchián. 
- A szervezeti egység hierarchiájának különböző szintjein összesítve jelenteni a bevételt vagy a költséget.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Nagy multinacionális vállalat vagyunk komplex, többszintű költséghelyekkel, osztályokkal és számlázási irodákkal. Hogyan használhatjuk a leghatékonyabban a szervezeti egység fogalmát a Project Service alkalmazás ezen verziójában?

Ha komplex hierarchiájú költséghelyekkel, osztályokkal, számlázási irodákkal stb. rendelkezik, akkor az adott hierarchia levélcsomópontjait külön szervezeti egységként kell beállítani.
A következő példa egy tipikus hierarchiát mutat:

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
 
Ha hierarchiája hasonló, akkor az itt látható módon, lapos listaként kell beállítani:
- Contoso India – SAP-gyakorlat – Műszaki tanácsadók 
- Contoso India – SAP-gyakorlat – Funkcionális tanácsadók       
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók 
- Contoso India – Microsoft technológiai gyakorlat – Műszaki tanácsadók 
- Contoso USA – SAP-gyakorlat – Műszaki tanácsadók  
- Contoso USA – SAP-gyakorlat – Funkcionális tanácsadók  
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók 
- Contoso USA – Microsoft technológiai gyakorlat – Műszaki tanácsadók

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Kis professzionális szolgáltatást nyújtó vállalat vagyunk, amely egyetlen részlegként működik. Hogyan lehet legjobban használni a szervezeti egység fogalmát a jelenlegi PSA-verzióban?

Ha vállalata egy önköltségi árlistát tartalmazó egyetlen egységként működik, nem kell semmilyen szervezeti egységet beállítania. A PSA telepítése során a Dynamics 365 egy alapértelmezett szervezeti egységet hoz létre, amelynek neve megegyezik a szervezet nevével. Alapértelmezés szerint minden felhasználó hozzá van rendelve a szervezeti egységhez. Ha a rendszernek ki kell választania egy szervezeti egységet, akkor alapértelmezés szerint ez a szervezeti egység lesz kiválasztva.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Ha létrehoz egy projektet árajánlat vagy projekt-szerződéssor alapján, az alapértelmezett szerződő részleg az árajánlatból vagy a projektszerződésből származik. Ha a projekt létrehozása az értékesítési entitások, például az Árajánlat vagy a Projektszerződés létrehozása előtt történik, mi lesz az alapértelmezett szerződő részleg?

Ha önmagában egy projektet hoznak létre, a projekt alapértelmezett szerződő részlege az a felhasználó, aki létrehozza azt. Ez a felhasználó egyben az alapértelmezett projektvezető is. Ha a projekt egy értékesítési entitásra van leképezve – például Árajánlathoz vagy Projektszerződéshez –, akkor a projektben szereplő szerződő részleg az értékesítési entitáson alapul. Ebben az esetben a projektbecslések újraszámíthatók, mivel az önköltségi árlista segítségével kiszámíthatók a költségbecslés változásai, a szerződő részleg módosulása esetén. Az értékesítési árlista segítségével kiszámíthatók a módosítani kívánt értékesítési becslések, hogy azok szinkronban legyenek az árajánlat projekt árlista mezőjében szereplő árakkal.

A **Szerződő részleg** és a **Pénznem** mezők nem szerkeszthetők, mivel szinkronban kell lenniük az értékesítési entitások értékeivel (árajánlat vagy projektszerződés), amelyekre a projekt le van képezve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
