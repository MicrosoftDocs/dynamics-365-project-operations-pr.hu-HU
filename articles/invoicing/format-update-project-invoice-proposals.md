---
title: Projekt számlaajánlatok kezelése
description: A cikk az ügyfél felé irányuló számlák Project Operations szolgáltatással való feldolgozását részletezi az erőforrás/nem készletezett anyagokon alapuló forgatókönyvekhez.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ef6003499f1372a51d7d1606db6f5bf9722a369d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927837"
---
# <a name="manage-project-invoice-proposals"></a>Projekt számlaajánlatok kezelése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projekt számlajavaslatait feldolgozhatja a számlázási osztály, ha teljesül a következő két feltétel:

  - A projektmenedzser jóváhagyja a proforma számlát a Microsoft Dataverse-ben.
  - A proforma számlán szereplő minden időre és anyagra vonatkozó számlázatlan értékesítési tranzakciók szerepet azon a proforma számlán, amelyet a Dynamics 365 **Project Operations integrációs** naplója segítségével tettek közzé.

A következő lépésekkel teljesítsen egy projekt számlajavaslatot a Dynamics 365 Finance-ben.

1. Tekintse át az időpont- és anyagtranzakciók számlázási adatait, és tegye közzé a **Project Operations integrációs** naplót.
2. Tekintse át a rögzített árú számlázási mérföldkövek számlázási adatait.
3. Tekintse át és formázza a projektszámlázási javaslatot.
4. Tegyen közzé és nyomtasson projektszámlákat.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Kezelje a számlázási adatokat a Project Operations integrációs naplóban

A Dataverse-ben lévő projekt tényleges adatait áttekintette és közzétette a Projekt könyvelője a Finance szolgáltatásban. A Project Operations integrációs naplójának használatáról további tájékoztatást az [Integrációs napló a Project Operations-ben](../project-accounting/project-operations-integration-journal.md) részben talál.

A költség tényleges adatai és a számlázatlan értékesítési tényleges adatai külön sorként kerülnek az integrációs naplóba:

  - A projekt Dataverse-ben lévő tényleges költségtranzakciója után a Költség tényleges alapértelmezett adatainak kiszerelési önköltségi ára és összege.
  - A Számlázatlan értékesítési tranzakció alapértelmezéseinek egységárai és értékesítési összege a projekt tényleges adataiból, számlázatlan értékesítési tranzakcióiból a Dataverse-ben.

### <a name="billing-sales-tax"></a>Számlázási áfa

A számlázás áfaszámítását a **Számlázási áfacsoport** és a **Számlázási cikk áfacsoport** mező kombinációja határozza meg a **Project Operations integrációs** naplósorában egy számlázatlan értékesítési rekordon. A rendszer ezeket a mezőértékeket alapértelmezettként adja meg a **Projektmenedzsment és a könyvelési paraméterek** oldal **Pénzügyek** lapján található beállítások alapján.

- A számlázási értékesítési áfacsoport alapértelmezett logikáját az **Értékesítési áfacsoport módszer** határozza meg:
  
  - **Projekt**: A projekt számlázási áfacsoportja mindig alapértelmezett. A projekt alapértelmezett számlázási értékesítési adócsoportját a **Minden projekt** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.
  - **Projektszerződés**: A projektszerződés számlázási áfacsoportja mindig alapértelmezett. A projektszerződés alapértelmezett számlázási értékesítési adócsoportját a **Minden projektszerződés** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.
  - **Ügyfél**: Az ügyfél számlázási áfacsoportja mindig alapértelmezett.
  - **Keresés**: A keresés az összes fenti entitásban fog keresni, és kiválasztja az elérhető első értéket. A keresés a **Projekt** entitással, majd a **Projekt szerződés** entitással, végül az **Ügyfél** entitással kezdődik.

- A számlázási cikk értékesítési áfacsoport alapértelmezett logikáját a **Cikk értékesítési áfacsoport módszer** határozza meg:
  
  - Az idő, költség és díj tranzakciótípusok esetében a számlázási cikk értékesítési áfacsoportja mindig alapértelmezett a **Projektkategória** entitásból.
  - Az anyagtranzakció-típusok esetén a számlázási cikk értékesítési áfacsoport alapértelmezései a **Cikk áfacsoport módszer** **Projektkezelés és könyvelési paraméterek** beállításán alapulnak. A cikkszám alapértelmezései a **Kiadott termék** entitás cikk értékesítési áfacsoportját tartalmazza. A kategória alapértelmezései a **Projektkategória** entitás cikk értékesítési áfacsoportját tartalmazza.

### <a name="financial-dimensions"></a>Pénzügyi dimenziók

A **Project Operations integrációs** naplójában lévő számlázatlan értékesítési rekordok pénzügyi dimenziói alapértelmezetten **Projekt** entitásából származnak. A pénzügyi dimenziók az **Összegek elosztása** lehetőség kiválasztásával áttekinthetők és módosíthatók. Ha az integráció közzétettele után, de a Proforma számla megerősítését megelőzően módosítania kell a számlázatlan értékesítési rekord pénzügyi dimenzióit, menjen a **Minden projekt** > **Kezelés** > **Közzétett tranzakciók** lehetőséget, majd válassza ki a tranzakciót, és válassza a **Folyamat** > **Könyvelés beállítása** lehetőséget.

### <a name="exchange-rates"></a>Átváltási árfolyamok

A Dataverse-ben lévő számlázatlan tranzakciós pénznem a Finance-ben tranzakciós pénznemként használatos, és átváltják a vállalat könyvelési pénznemére a Finance-ben meghatározott átváltási árfolyamok használatával.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>A számlázási mérföldkövek pénzügyi attribútumainak kezelése 

A rögzített árú számlázási módot használó projektszerződéssorok számlázása [Rögzített árú mérföldkövek](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) segítségével megy végbe. A Projekt könyvelője áttekintheti a Finance számlázási mérföldköveit a **Projektkezelés és könyvelés** > **Minden projekt** > **Kezelés** > **Részletszámlázási tranzakciók** oldalon.

### <a name="billing-sales-tax"></a>Számlázási áfa

Az új számlázási mérföldkő Dataverse-ből való létrehozásakor az **Értékesítési áfacsoport** és a **Cikk értékesítési áfacsoport** értékei alapértelmezetten a beállításokból származnak. A rendszer ezeket az értékeket alapértelmezettként adja a mezőkhöz a **Projektmenedzsment és a könyvelési paraméterek** oldal **Pénzügy** lapján található beállítások alapján.

- A **Számlázási értékesítési áfacsoport** alapértelmezett logikáját az **Értékesítési áfacsoport módszer** határozza meg:

    - **Projekt**: a projekt számlázási áfacsoportja mindig alapértelmezett. A projekt alapértelmezett értékesítési adócsoportját a **Minden projekt** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.
    - **Projektszerződés**: a projektszerződés számlázási áfacsoportja mindig alapértelmezett. A projektszerződés alapértelmezett számlázási értékesítési adócsoportját a **Minden projektszerződés** lapon az **Alapértelmezett könyvelés megjelenítése** lehetőség kiválasztásával tudja áttekinteni vagy módosítani.
    - **Ügyfél**: az ügyfél számlázási áfacsoportja mindig alapértelmezett.
    - **Keresés**: a keresés a listában szereplő összes entitásban fog keresni, és kiválasztja az elérhető első értéket. A keresés a **Projekt** entitással, majd a **Projekt szerződés** entitással, majd az **Ügyfél** entitással kezdődik.

- A **Fixáras mérföldőtétel forgalmiadó-csoportja** a számlázási mérföldkő **Tétel forgalmiadó-csoportja** mezőjének alapértelmezett értékeként használatos. A könyvelő ezt az értéket a **Számlán végzett tranzakciók** oldalon tekintheti át és módosíthatja. A rendszer a projektszámla-javaslatsor létrehozásakor a számlán szereplő tranzakció értékét használja.
 

### <a name="financial-dimensions"></a>Pénzügyi dimenziók

A rögzített árú számlázási mérföldkövek alapértelmezett pénzügyi dimenziói a Projekt szerződéssorokon vannak beállítva. Menjen a **Projektszerződések** > **Alapértelmezett könyvelés megjelenítése** lehetőségre, és a **Szerződéssorok** lapon válassza ki az **árszerződéssor** lehetőséget, majd állítsa be az alapértelmezettként használni kívánt pénzügyi dimenzióértékeket.

A Projekt könyvelője a projekt számlajavaslatának létrehozása előtt módosíthatja a számla mérföldköveinek értékesítési áfa- és pénzügyi dimenziókra vonatkozó adatait.


## <a name="create-project-invoice-proposals"></a>Projekt számlajavaslatok létrehozása

A projektszámla javaslatok áttekinthetők a **Projektmenedzsment és könyvelés** modulban, csak menjen a **Projektszámlák** > **Projekt számlajavaslatok** elemre.

A Projekt számlajavaslat fejléce a Pénzügyben jön létre, amikor megerősítették a Proforma számlát a Dataverse-ben. A könnyebb kezelhetőség érdekében a rendszer a Projekt számla javaslatok számét a Pénzügyben ugyanarra a számra állítja be, mint ami a Proforma számlaazonosító a Dataverse-ben. Mivel a Proforma számlák nem minden esetben a létrehozás sorrendjében vannak megerősítve, a Projektszámla javaslat Pénzügyben lévő számsorozatának engedélyeznie kell a kisebb és nagyobb számokra való változtatást. Adja meg a számsorozatokat a következő lépések segítségével:

1. A Pénzügyben menjen a **Szervezetfelügyelet** > **Sorszámok** > **Sorszámok** lehetőségre.
2. A **Terület** szűrőben válassza a **Projektek** lehetőséget.
3. A **Referencia** szűrőben válassza a **Számlajavaslat** lehetőséget.
4. A **Vállalat** mező segítségével szűrheti az egyes entitásokat a Project Operations Dataverse integrálásának engedélyezésével.
5. Nyissa meg a **Sorszám részletei** lehetőséget, és az **Általános** fülön állítsa be:

    - **Felhasználói módosítások engedélyezése: Kisebb számra** = **Igen**
    - **Felhasználói módosítások engedélyezése: Nagyobb számra** = **Igen**

A rendszer hozzáadja a projekt számlajavaslat-sorokat az **Importálás az előkészítési táblából** (**Projektmenedzsment és könyvelés** > **Periodikus** > **Project Operations integráció** > **Importálás az előkészítési táblából**) segítségével. Ezt a műveletet manuálisan vagy egy periodikus ütemezéssel lehet futtatni. A rendszer addig nem ad sorokat a számlajavaslat-dokumentumhoz, amíg az összes sor készen nem áll a számlázásra. Az időpont- és anyagtranzakciók csak akkor lesznek készen a számlázásra, ha a **Project Operations integráció** segítségével közzéteszik őket.

## <a name="format-and-print-invoice-proposals"></a>Számlázási javaslatok formázása és nyomtatása

A Projekt könyvelője testre szabhatja a projekt számláinak nyomtatását a **Számlajavaslatok formázása** lap és a nyomtatáskezelési képességek segítségével.

### <a name="format-invoice-proposals"></a>Számlázási javaslatok formázása

A **Számlajavaslatok formázása** lapon az egyéni csoportosítási tranzakciók megjeleníthetőek az ügyfél projektszámláján.

1. A **Projekt számlajavaslat** lapon válassza a **Nyomtatás** > **Számlajavaslat formázása** lehetőséget.
2. Válassza az **Új** lehetőséget, ha új csoportosítást szeretne létrehozni a Projektszámla nyomtatásához.
3. A **Részletek/Összegzés** mezőben adja meg a csoportosítás lehetőségeit:

    - Válassza a **Részletek** lehetőséget az ügyfélszámla tranzakciórészleteinek nyomtatáshoz.
    - Válassza az **Összegzés** lehetőséget az ügyfélszámla tranzakcióösszegzésének nyomtatáshoz.

> [!NOTE]
> A **Számlajavaslat formázása** lapon a **Részletek/Összegzés** mezőben megadott beállítás felülbírálja a **Számlajavaslatok** oldal **Számla formázása** mezőben kijelölt beállítást, és így részletes számlát vagy összesítő számlát nyomtathat.

- Válassza ki azokat a tranzakciósorokat, amelyek ezt a szakaszt tartalmazzák a **Rendelkezésre álló tranzakciók** fülön, majd válassza a **Tranzakciók belefoglalása** lehetőséget, és helyezze át azokat a **Kijelölt tranzakciók** fülre.
- Válassza a **Felmozgatás** és a **Lemozgatás** lehetőséget a szakaszok sorrendjének módosításhoz.
- Válassza a **Nyomtatási kép előnézete** lehetőséget a formázott számla előnézetének megtekintéséhez.

### <a name="print-management"></a>Nyomtatáskezelés

A nyomtatáskezelés különböző jelentésfájlokat használ a nyomtatáshoz, a célpontok megadásához és a számla láblécszövegének testreszabásához. A nyomtatáskezelés a modul szintjén beállítható, azonban ezek a beállítások felülírhatóak egy adott ügyfél, szerződés vagy számlajavaslat esetében. Ha hozzá szeretné férni ehhez a funkcióhoz a **Projekt számlajavaslat** oldalon, akkor válassza a **Nyomtatás** > **Nyomtatáskezelés** lehetőséget.

A nyomtatáskezelési beállítások egy fanézetben jelennek meg, ahol minden csomópontszint megjeleníti a módosítható dokumentumokat. Az egyéni nyomtatások a modul, az ügyfél, a szerződés vagy a számla ajánlati dokumentumszinten rendelhetők hozzá. Az eredeti dokumentum nyomtatásának módosításához bontsa ki a kívánt csomópontot, és válassza az **Eredeti cikk** lehetőséget. A **Jelentésformátum** mezőben jelölje ki a nyomtatáshoz használni kívánt jelentésformátumot. Az egyéni jelentésformátumok a [Vállalat dokumentumkezelési keretrendszer](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management) segítségével használhatók.

## <a name="post-invoice-proposals"></a>Számlázási javaslatok közzététele

Miután a számlát átnézték és szerkesztték, és megfelelőek a számlajavaslatok sorai, ellenőrizze a számlaösszegeket és az áfát. A **Részletek** csoportban válassza az **Összesítések**, majd a **Közzététel** lehetőséget a számla közzétételéhez.

Ha meg szeretné tekinteni a számlát a közzététel előtt, akkor törölje a jelölést a **Közzététel** jelölőnégyzetből. A **Pro forma** szöveg rá lesz nyomtatva a számlára, ez jelzi, hogy ez egy sablonszámla. A számla nyomtatása előtt jelölje be a **Számla nyomtatása** jelölőnégyzetet.

A **Számlajavaslat** lap mellett a számlajavaslatokat a periodikus feladat, a **Számlajavaslatok közzététele** futtatásával is közzéteheti. A feladat kereséséhez menjen a **Projektkezelés és a könyvelés** > **Periodikus** > **Projektszámlák** > **Projektjavaslatok közzététele** lehetőségre.

Ez az oldal megjeleníti a közzétételre kész összes számlajavaslatot. A **Köteg** lehetőség kiválasztásával ütemezheti is a számlajavaslatok közzétételét. Állítsa a **Kötegfeldolgozás paraméter** lehetőséget **Igen** értékre, és állítsa be a kötegfeldolgozás ismétlődését az **Ismétlődés** lehetőség kiválasztásával.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
