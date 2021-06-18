---
title: Projektszerződések
description: Ez a témakör példákat tartalmaz a különféle típusú projektekhez és finanszírozási forrásokhoz létrehozható projektszerződésekre, valamint a szerződések kezelésére és a projektügyfeleknek történő számlázásra.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999764"
---
# <a name="project-contracts"></a>Projektszerződések

[!include [banner](../includes/banner.md)]

Ez a cikk példákat tartalmaz a különféle típusú projektekhez és finanszírozási forrásokhoz létrehozható projektszerződésekre, valamint a szerződések kezelésére és a projektügyfeleknek történő számlázásra.

A projektszerződéshez létrehozott projekt típusa határozza meg a projektügyfelek esetében alkalmazott számlázási módot. A projektszerződések és a kapcsolódó projektek módosíthatók, de a projekttípus nem. 

A projektszerződések használatával egyszerre számlázhat egy vagy több projektet. A projektszerződés segít továbbá a projekt struktúrájában szereplő összes alprojekt egységes számlázási eljárásának biztosításában. 

Minden számlázásra kerülő projektet egy projektszerződéshez kell társítani. A projektszerződés beállításai a projektszerződéshez társított összes projektre és alprojektre vonatkoznak. 

A projektszerződések egy vagy több finanszírozási forrást is meghatározhatnak. Ezért feloszthatja a számlázási több finanszírozói között, beállíthat finanszírozási korlátokat, hogy a finanszírozási források esetében egy megadott összeget ne lépjen túl a számlázás, és konfigurálhatja a kiadások felszámítására vonatkozó finanszírozási szabályok.

## <a name="funding-for-project-contracts"></a>Projektszerződések finanszírozása
Egyes projektszerződések azt határozzák meg, hogy több fél osztozik a felelősségen a projekt költségeinek finanszírozása terén. Íme néhány példa:

-   A több divíziót tartalmazó nagy ügyfél azt kéri, hogy a projektek finanszírozása divíziók szerint legyen megosztva.
-   A vállalat egy nagy projekt költségeit egy külső szervezettel osztja meg.
-   Egy közúti projektet két önkormányzat társfinanszíroz.
-   Egy hídprojektet kormányzati támogatás és egy magánvállalat finanszíroz.

A Dynamics 365 Finance alkalmazásban egyetlen tranzakció vagy egy teljes projekt számlázását feloszthatja több ügyfél, támogatás vagy szervezet között. 

A több finanszírozóval rendelkező projektek esetében a speciális finanszírozási projekt finanszírozásához hozzájáruló feleket finanszírozási forrásoknak nevezik. Az ügyfél, szervezet vagy támogatás finanszírozási forrásként való meghatározása után egy vagy több finanszírozási szabályhoz rendelhető hozzá. A finanszírozási szabályok tartalmazzák azokat a feltételeket, amelyek meghatározzák, hogy a felszámított költségek hogyan vannak kiosztva a projektek különböző finanszírozási forrásaihoz. 

Mivel a készletezett cikkek – például a beszerzési igénylésekben és a beszerzési rendeléseken megjelenő elemek – nem oszthatók szét, a költség összege nem osztható szét több finanszírozási forrás között a terjesztés időpontjában. A finanszírozási forrás értéke ezért 0 (nulla) marad a készletkiadás könyveléséig. A készlet kiadásának könyvelésekor a program a költségösszeget a projekt partnerek közötti felosztási szabályainak megfelelően felosztja.

Az alábbiakban néhány lépést mutatunk be, amelyek végrehajtásával megkönnyítheti a számlázás több finanszírozási forrás közötti felosztását:

-   Adja meg, hogy a projekthez bevitt összes tranzakció ugyanazt az értékesítési pénznemet használja, mint a projektszerződés.
-   Állítson be finanszírozási korlátokat, hogy egy finanszírozási forrás irányában egy adott összegnél több ne legyen kiszámlázva a projekttel kapcsolatban.
-   Konfigurálja a finanszírozási szabályokat és a finanszírozási korlátozásokat az egyes dolgozók, cikkek, kategóriák, kategóriacsoportok és tranzakciótípusok esetén (vagy minden tranzakciótípus esetén).
-   Válasszon ki opcionális kezdő és záró dátumokat az egyes finanszírozási szabályok érvényességi idejének meghatározásához.
-   Határozza meg az egyes finanszírozási források felelősségének százalékos arányát.
-   Határozza meg, hogy melyik finanszírozási forrás felelős a finanszírozási allokációs számítások miatti kerekítési különbségekért.
-   Állítson be szabályokat, amelyek meghatározzák, hogy a projekt költségei hogyan kerülnek kiszámlázásra a külső ügyfelek számára, és hogyan kerülnek felszámításra a belső szervezetek számára.
-   Rögzítse a tranzakciókat egy visszatartott finanszírozási számlán, amíg további finanszírozás nem szerezhető, vagy amíg úgy nem dönt, hogy a költségeket belsőleg viseli.

Annak megállapításához, hogy mely adócsoport társítandó egy tranzakcióhoz, a rendszer egy adócsoport-hozzárendelést keres a projektben. Ha a projekt szintjén nem történt meg az adócsoport-hozzárendelés, a program a projektszerződésben keres.

### <a name="example-multiple-funding-sources-simple"></a>Példa: Több finanszírozási forrás (egyszerű)

A következő táblázat a több finanszírozási forrás közötti finanszírozásfelosztás kezelésére szolgáló forgatókönyveket tartalmaz. Ezek a forgatókönyvek a következő feltételezéseken alapulnak:

-   A prioritási beállításokat a rendszer figyelembe veszi a pénzösszegek felosztásában a finanszírozási szabályok egyéb feltételeinek alkalmazása előtt.
-   Nincs megadva dátumtartomány a d időszak meghatározására, amikor a finanszírozási szabály érvényes.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Forgatókönyv</strong></td>
<td><strong>Finanszírozási forrás</strong></td>
<td><strong>Felosztási százalék</strong></td>
<td><strong>Felosztás prioritása</strong></td>
</tr>
<tr class="even">
<td>A költségeket csak egy finanszírozási forráshoz kívánja felosztani, amíg a pénzösszegei ki nem merülnek, ezután a költségeket a második finanszírozási forráshoz osztja fel, amíg a pénzösszegei ki nem merülnek, majd végül a fennmaradó költségeket egy harmadik finanszírozási forráshoz osztja fel.</td>
<td><ul>
<li>1. finanszírozási forrás</li>
<li>2. finanszírozási forrás</li>
<li>3. finanszírozási forrás</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>A költségek 75 százalékát egy finanszírozási forráshoz, 25 százalékát pedig egy második finanszírozási forráshoz kívánja felosztani. Ha a finanszírozási források bármelyike kimerül, a fennmaradó költségeket egy harmadik finanszírozási forrásból kívánja fizetni.</td>
<td><ul>
<li>1. finanszírozási forrás</li>
<li>2. finanszírozási forrás</li>
<li>3. finanszírozási forrás</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>A költségek 75 százalékát egy finanszírozási forráshoz, 25 százalékát pedig egy második finanszírozási forráshoz kívánja felosztani. Ha a finanszírozási források bármelyike kimerül, a fennmaradó költségeket egy harmadik finanszírozási forrás és egy negyedik finanszírozási forrás között kívánja felosztani.</td>
<td><ul>
<li>1. finanszírozási forrás</li>
<li>2. finanszírozási forrás</li>
<li>3. finanszírozási forrás</li>
<li>4. finanszírozási forrás</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>A költségek 25 százalékát egy finanszírozási forráshoz, a maradékot pedig egy második finanszírozási forráshoz kívánja felosztani.</td>
<td><ul>
<li>1. finanszírozási forrás</li>
<li>2. finanszírozási forrás</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Példa: Több finanszírozási forrás (összetett)

Három finanszírozási forrással rendelkezik, amelyeket a következő sorrendben szeretné használni:

1.  A 2. finanszírozási forrást és a 3. finanszírozási forrást egyenlően használja, amíg a 2. finanszírozási forrást ki nem merül.
2.  Folytatja a 3. finanszírozási forrás használatát, amíg az ki nem merül.
3.  Az 1. finanszírozási forrást használja, miután a 3. finanszírozási forrást kimerül.

Ennek a célnak a teljesítéséhez az alábbiakat kell végrehajtania:

-   Finanszírozási korlátokat kell beállítania a 2. finanszírozási forrás és a 3. finanszírozási forrás számára a megfelelő összegekkel.
-   Hozz létre a következő finanszírozási szabályt::
    -   1. szabály (1. prioritás): Ossza fel a tranzakciók 50 százalékát a 2. finanszírozási forráshoz, és 50 százalékát a 3. finanszírozási forráshoz.
    -   2. szabály (2. prioritás): Ossza fel a tranzakciók 100 százalékát a 3. finanszírozási forráshoz.
    -   3. szabály (3. prioritás): Ossza fel a tranzakciók 100 százalékát az 1. finanszírozási forráshoz.

Ez a beállítás azért működik, mert a rendszer ellenőrzi a tranzakciókat a szabályok és a korlátozások alapján, hogy ezek közül bármelyik a tranzakcióra vonatkozik-e. Ha a tranzakcióra nem érvényesek konkrét szabályok vagy korlátozások, a Minden tranzakció szabály érvényes. A Minden tranzakció szabály minden tranzakcióra érvényes. 

Ha a rendszer egy olyan szabályt talál, amely megfelel egy tranzakciónak, akkor először a szabályban lefoglalt százalékértéket alkalmazza, de csak azután, hogy az egyezések esetében ellenőrizte a beállított korlátokat. Ha a költségek elérik a korlátot, és a finanszírozási forrás pénzösszegei kimerültek, a finanszírozási korlátozáshoz kapcsolódó finanszírozási szabály figyelmen kívül marad, és a program ellenőrzi a következő vonatkozó szabályt. 

Bizonyos esetekben a tranzakciónak csak egy része osztható fel egy szabály értelmében. Ez azért fordulhat elő, mert a tranzakció felosztásakor a költség eléri a korlátot. Ebben az esetben csak bizonyos összeg kerül felosztásra az adott szabály szerint, például 50 százalék az egyes finanszírozási forrásokhoz. Ez az az eset az 1. szabályban, amelyet a fejezet korábban ismertet. A maradékot a program a sorban következő szabály szerint osztja fel. 

A következő táblázat részletesebben megvizsgálja ezt a forgatókönyvet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fókusz</strong></td>
<td><strong>Részletek</strong></td>
</tr>
<tr class="even">
<td>Finanszírozási szabályok</td>
<td><ul>
<li>1. szabály (1. prioritás): Minden tranzakció. Felosztás a 2. finanszírozási forrásra 50%-ban és a 3 finanszírozási forrásra 50%-ban.</li>
<li>2. szabály (2. prioritás): Minden tranzakció. Felosztás a 3. finanszírozási forrásra 100%-ban.</li>
<li>3. szabály (2. prioritás): Minden tranzakció. Felosztás az 1. finanszírozási forrásra 100%-ban.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finanszírozási korlátozások</td>
<td><ul>
<li>1. finanszírozási forrás korlátja = 10 000,00</li>
<li>2. finanszírozási forrás korlátja = 500,00</li>
<li>3. finanszírozási forrás korlátja = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>1. tranzakció</td>
<td><strong>Tranzakció összege:</strong> 100,00<strong>Finanszírozás:</strong> A tranzakció csak az 1. szabály szerint kerül kifizetésre, mert a tranzakció teljes mértékben ki van fizetve az 1. szabály alkalmazása után. A tranzakciót egyformán finanszírozza a 2. finanszírozási forrás és a 3. finanszírozási forrás.
<ul>
<li>2. finanszírozási forrás: 50,00</li>
<li>3. finanszírozási forrás: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. tranzakció</td>
<td><strong>Tranzakció összege:</strong> 5000,00<strong>Finanszírozás:</strong> A tranzakció mindhárom szabály szerint kerül kifizetésre. <strong>1. szabály</strong>
<ul>
<li>2. finanszírozási forrás: 450,00</li>
<li>3. finanszírozási forrás: 450,00</li>
</ul>
<strong>2. szabály</strong>
<ul>
<li>3. finanszírozási forrás: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>3. szabály</strong>
<ul>
<li>1. finanszírozási forrás: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Az egyes finanszírozási forrásokhoz szétosztott teljes pénzösszeg</td>
<td><ul>
<li>1. finanszírozási forrás: 3850,00</li>
<li>2. finanszírozási forrás: 500,00</li>
<li>3. finanszírozási forrás: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Számlázási szabályok
Amikor az ügyféllel egyeztet egy projektszerződést, meghatározhatja, hogyan és mikor számlázhatja a projekten végzett munkát az ügyfélnek. A projektszerződés és a projekt beállítása után megadhatja a projekt számlázási szabályait. A számlázási szabályok a projektszerződésben megadott feltételeken alapulnak. A létrehozható számlázási szabályok a projektszerződés feltételeitől és a projekttípustól (például Idő és anyag vagy a Rögzített ár) függenek, amelyeket a számlázási szabályhoz társít. A projektszerződéshez több számlázási szabály is létrehozható. Számlázási szabályt hozzárendelhet több olyan projekthez, amelyek ugyanahhoz a projektszerződéshez vannak társítva, és hasonló számlázási feltételekkel rendelkeznek. 

A következő típusú számlázási szabályokat állíthatja be:

-   **Szállítási egység** – Az ügyfélnek egy szállítási egység teljesítésekor számláz. A szállítási egységeket a szerződésben definiálja.
-   **Előrehaladás** – Az ügyfélnek a projekt megadott százalékának teljesítése után számláz. Beállíthat egy számlázási szabályt, amely automatikusan kiszámítja a befejezett munka százalékos arányát, vagy manuálisam kiszámíthatja a befejezett munka százalékos arányát, valamint az ügyfélnek számlázandó összeget.
-   **Mérföldkő** – A mérföldkő elérésekor a projekt mérföldkövének teljes összege kerül számlázásra az ügyfélnek.
-   **Díj** – Az ügyfélnek a szolgáltatásainak díja, valamint egy kezelési díj kerül kiszámlázásra, amely jellemzően a szolgáltatások költségének adott százaléka.
-   **Idő és anyag** – A projektben használt idő és anyagok értéke kerül számlázásra az ügyfélnek.

Minden számlázásiszabály-típus esetében megadhat egy visszatartási százalékot, amely levonásra kerül az ügyfelek számláiból, amíg a projekt elér egy megállapodás szerinti fázist. A fizetési visszatartási százalék a projektszerződésben van megadva. Az összeget a rendszer az ügyfélszámla sorainak teljes értékéből számítja ki és kivonja ki. 

Az **Idő és anyag** és a **Folyamatban lévő** számlázási szabályok esetében a felszámítható kategóriákat is hozzárendelhet. A felszámítható kategóriák jelzik azokat a tranzakciókat, amelyeket szerepeltetni kell az ügyfelek számláján. 

Amikor készen áll az ügyfél felé történő számlázásra, a program a számlázási szabályok alapján számítja ki a projektre vonatkozó számla összegét, és létrehoz egy projektszámla-javaslatot. 

A következő szakaszok példákat tartalmaznak, amelyek bemutatják, hogyan állíthatók be és kezelhetők a projektek számlázási szabályai.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Példa: A leszállított egységek számán alapuló számlázási szabály létrehozása

A szervezete olyan megállapodást köt, amely összesen öt képzés alkalmat biztosít az ügyfél alkalmazottainak, képzési alkalmanként 10 000 költség ellenében. Minden képzési alkalom után számláz az ügyfélnek. 

A szerződés számlázási szabályainak beállításakor a következő értékek használhatók:

-   A szállítási egység egy képzési alkalom.
-   Az egységár 10 000 képzési alkalmanként.
-   Az egységek teljes száma öt képzési alkalom.

Amikor befejezte az egyik képzési alkalmat, a 10 000 összegű számlát hoz létre a leszállított első egységre vonatkozóan, és elküldi a számlát az üygfélnek.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Példa: A projekt készültségének meghatározott százalékán alapuló számlázási szabály létrehozása (manuális számítás)

A szervezete, egy szoftvertanácsadó vállalat megállapodást köt az ügyféllel, hogy kifejleszti az ügyfél által fejlesztett termék egy részét. A szervezete vállalja, hogy hat hónap alatt szállítja le a szoftver kódját. Az ügyfél vállalja, hogy a munkáért összesen 100 000-et fizet a szervezetlnek. Számlázási szabályt hoz létre, amely az ügyfelet a projektből a szerződésben meghatározott százalékban elkészült munkamennyiség alapján számlázza.

-   Az első hónap végén találkozik az ügyféllel, hogy megállapítsa a befejezett munka százalékos arányát. Miután az ügyféllel áttekinti a projektet, úgy döntenek, hogy a projekt 15 százaléka készült el.
-   Létrehoz egy 15 000 (a teljes 100 000-es összeg 15%-a) összegű számlát, és elküldi az ügyfélnek.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Példa: A projekt készültségének meghatározott százalékán alapuló számlázási szabály létrehozása (automatikus számítás)

Szervezete, egy szoftverfejlesztő cég vállalja, hogy kidolgoz egy bérszámfejtési csomagot egy ügyfél számára 30 000-ért. Az ügyfél vállalja, hogy a munkáért az elkészült munka százalékos aránya alapján fizet. Úgy becsüli, hogy a projekt költségei 20 000-et tesznek ki. A projektszerződés meghatározza a számlázási folyamatban használt munkakategóriákat. Olyan számlázási szabályokat kell beállítani, amelyek automatikusan kiszámítják a számlaösszegeket az egyes kategóriákhoz tartozó befejezett munkamennyiségek százalékos arányai alapján. Minden egyes kategóriához beállít egy költségvetést:

-   **Fejlesztés** – 15 000 költség és 20 000 árbevétel
-   **Telepítés** – 5000 költség és 10 000 árbevétel

Amikor első alkalommal hoz létre egy ügyfélszámlát, a rendszer automatikusan kiszámítja a számla összegét az alábbi adatok alapján:

-   Egy hónap elteltével a projekt munkatársa elküldi a projekthez tartozó munkaidő-nyilvántartást. A dolgozói órák ára 5000 a fejlesztés és 1000 a telepítés esetében. A fejlesztési munka 33 százaléka készült el (5000 tényleges költség/15 000 költségvetési költség), a telepítési munkának pedig 20%-a készült el (1000 tényleges költség/5000 költségvetési költség).
-   A rendszer automatikusan kiszámítja a 8667 összeget (20 000 33 százaléka + 10 000 20 százaléka).
-   Létrehoz egy 8667 összegű számlát, és elküldi az ügyfélnek.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Példa: Megállapodás szerinti mérföldköveken alapuló számlázási szabály létrehozása

A szervezete, egy menedzsmenttanácsadó cég vállalja, hogy az ügyfél által értékesíteni tervezett termékre vonatkozóan piackutatást végez. Az ügyfél vállalja, hogy a szolgáltatásait márciusi kezdettel három hónapig igénybe veszi, és beleegyezik, hogy a szervezetének 50 000-et fizet. A projekthez három mérföldkő tartozik:

-   1. mérföldkő: Fogyasztói adatok gyűjtése – Március 31.út 31
-   2. mérföldkő: Fogyasztói adatok elemzése – Április 30.
-   3. mérföldkő: Termék életképességére vonatkozó javaslat bemutatása – Május 31.

Az ügyfél vállalja, hogy kifizet a szervezetének 10 000-et az első mérföldkő, 20 000-et a második mérföldkő, és 20 000-et a harmadik mérföldkő eléréséért. 

A projektszerződés rögzítésekor beleegyezik, hogy az ügyfélnek a teljesített mérföldkövek alapján számláz. A számlázási szabály összeállítása a következő lépéseket tartalmazza:

-   A projekt mérföldköveinek megadása.
-   Az ügyfél felé számlázandó összeg meghatározása az egyes mérföldkövek teljesítésekor.

Amikor az első mérföldkő március 31-én elkészül, akkor megjelöli befejezettként a mérföldkövet, majd létrehoz egy számlát 10 000 összeggel, és elküldi az ügyfélnek. A mérföldkőhöz tartozó számla csak akkor hozható létre, ha a mérföldkő befejezettként van megjelölve.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Példa: Szolgáltatási és kezelési díjon alapuló számlázási szabály létrehozása

A szervezete, egy menedzsment-tanácsadó cég vállalja, hogy piackutatást hajt végre az ügyfél, egy kiskereskedelmi vállalat által fejlesztett termék életképességével kapcsolatban. A szerződés feltételei meghatározzák, hogy a három legjobb menedzsment-tanácsadója szolgáltatásait fogja biztosítani, akik idő és anyag alapon hajtják végre a kutatást. Az ügyfél beleegyezik, hogy a projekt esetében felszámított tanácsadási órákért 100 egységet fizet, valamint 10 százalék kezelési díjat. 

A projektszerződés megkötésekor hozzon létre egy számlázási szabályt, amely 10 százalékos kezelési költséget ad hozzá a projektre felszámolt tanácsadási órákhoz. 

Amikor számlát hoz létre az ügyfélnek, az ügyfél 10 százalékos kezelési díjról és a tanácsadási órák költségéről kap számlát. Ha például a három tanácsadó a projektben összesen 200 órát dolgozott, a 22 000 összegű számlát a következő számítás alapján hozza létre:

-   200 óra, óránként 100 egység áron = 20 000
-   10 százalékos kezelési díj = 2000
-   Teljes számlázott mennyiség = 22 000

Ha egy ügyfél esetében a díjak adókötelesek, és kiválaszt egy áfacsoportot a projektszerződésben, akkor az áfacsoport automatikusan megadásra kerül a díjak számlázási szabályaiban.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Példa: Számlázási szabály létrehozása az idő és az anyagok értékéhez

A szervezete, egy szoftvertanácsadó cég vállalja, hogy öt műszaki tanácsadót biztosít az ügyfele szoftverfejlesztési projektjén végzett munkára a következő hat hónapra. Az ügyfél beleegyezik, hogy minden tanácsadói órára 150-et fizet, valamint az irodaszerek költségét. A szervezete minden hónap végén számlát küld az ügyfélnek. 

A projektszerződés beállításakor vállalja, hogy az ügyfélnek havonta állít ki számlát a projekthez felhasznált időre és az anyagokra vonatkozóan. A következő információkat tartalmazó számlázási szabályt hoz létre:

-   A szerződés időszaka hat hónap.
-   A tanácsadási időt óránként 150-es áron számítja a rendszer.
-   Az irodaszerek számlázása költségen történik, és a projekt teljes költsége nem haladhatja meg a 10 000 értéket.
-   A projekt során minden naptári hónap végén létre kell hoznia egy vevői számlát.

Az első hónapban összesen 800 órát rögzítenek a projekten dolgozó tanácsadók. A projektre terhelt irodaszerek ára 2000. Ezért a hónap végén létrehoz egy 122 000 összegű számlát, amelyhez 800 órát számít fel 150-es óránkénti áron, valamint az irodai kellékanyagok esetében 2000-et.





[!INCLUDE[footer-include](../includes/footer-banner.md)]