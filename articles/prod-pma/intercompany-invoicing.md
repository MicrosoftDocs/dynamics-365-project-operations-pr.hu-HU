---
title: Vállalatközi számlázás
description: Ez a cikk a projekteket érintő vállalatközi számlázással kapcsolatos információkat és példákat tartalmaz.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078118"
---
# <a name="intercompany-invoicing"></a>Vállalatközi számlázás

[!include [banner](../includes/banner.md)]

Ez a cikk a projekteket érintő vállalatközi számlázással kapcsolatos információkat és példákat tartalmaz.

Előfordulhat, hogy a szervezethez több olyan részleg, leányvállalat és más jogi személy tartozik, amelyek termékeket és szolgáltatásokat biztosítanak egymásnak a projektjeihez. A szolgáltatást vagy a terméket biztosító jogi személyt *kölcsönadó jogi személynek* , míg a szolgáltatást vagy a terméket fogadó jogi személyt *kölcsönbe vevő jogi személynek* nevezzük. 

A következő ábrán egy tipikus forgatókönyv látható, ahol két jogi személy, az SI FR (a kölcsönbe vevő jogi személy) és az SI USA (a kölcsönadó jogi személy) megosztja az erőforrásait az „A” ügyfél projektének megvalósítása érdekében. Ennél a forgatókönyvnél a szerződés értelmében az SI FR teljesíti a munkát az „A” ügyfél részére. 

[![Példa a vállalatközi számlázásra](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

A cél az, hogy rugalmasabbá és hatékonyabbá tegyük a vállalatközi projekttranzakciókhoz kapcsolódó költségkontrollt, bevételelszámolásokat, adókat és transzferárakat. Emellett a következő lehetőségek állnak a rendelkezésére:

-   Ügyfélszámlák létrehozása kölcsönadó jogi személy projektjéhez a kölcsönbe vevő jogi személy vállalatközi munkaidő-nyilvántartásai, kiadásai és beszállítói számlái alapján.
-   Az adózási számítások és a közvetett költségek támogatása.
-   A bevételkönyvelések elhalasztása a kölcsönadó jogi személynél, illetve akkor, amikor a kölcsönbe vevő jogi személynek kell könyvelnie a költségeket.
-   Elhatárolás a kölcsönadó jogi személy folyamatban lévő munkából (WIP) származó bevételétől.
-   A különböző díjszabási modelleket alapul vevő transzferárak beállítása. Íme néhány példa:
    -   **Mennyiség** – Az **Árképzés** mezőben megadott összeg a mennyiségre vagy egységre vonatkozó tényleges ár.
    -   **Költségek összege** – A tranzakciónkénti ár/költség, valamint az **Árképzés** mezőben megadott költségek összege.
    -   **Költségszázalék** – A transzferár a tranzakciónkénti ár/költség és az **Árképzés** mezőben megadott költségszázalék szorzata.
    -   **Az eladási ár százaléka** – A kölcsönadó jogi személy részére átadott eladási ár százalékértéke.
    -   **Az eladási ár alatti összeg** – Az az összeg, amelyet a kölcsönbe vevő jogi személy visszatart az értékesítési árakból, mielőtt átadja a kölcsönadó jogi személy részére.
    -   **Hozzájárulás aránya** – Az **Árképzés** mezőben megadott szám a hozzájárulási arány, amely az eladási ár százalékban kifejezett értéke.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. példa: A vállalatközi számlázás paramétereinek beállítása
Ebben a példában a USSI egy kölcsönadó jogi személy, amelynek erőforrásai jelentik a ráfordított időt a végső ügyféllel szerződéses viszonyban álló, kölcsönbe vevő jogi személy, az FRSI részére. A USSI alkalmazottak által jelentett órák és kiadások szerepelhetnek az FRSI által létrehozott projektszámlán. Emellett van egy harmadik tranzakcióforrás is, amely a kölcsönadó jogi személy entitástól (ebben a példában a USSI) származik. Ilyen esetben a kölcsönadó jogi entitás közös szállítói szolgáltatásokat nyújt a leányvállalatoknak (például az FRSI), majd továbbadja azokat a költségeket az adott leányvállalatokon belüli projektekhez. Az összes megegyező számlázási bizonylat és adó számítását a Finance rendszer végzi el. 

Ebben a példában az FRSI a USSI jogi személy egyik ügyfele, a USSI pedig az FRSI jogi entitás szállítója. Ezután beállítható a vállalatközi kapcsolat a két jogi személy között. Az alábbi eljárás azt mutatja be, hogyan kell beállítani a paramétereket úgy, hogy mindkét jogi személy részt vehessen a vállalatközi számlázásban.

1. Az FRSI beállítása a USSI jogi személy ügyfeleként és a USSI beállítása az FRSI jogi entitás szállítójaként. A feladathoz szükséges lépésekhez három belépési pont tartozik.

   | Lépés |                                                       Belépési pont                                                        |                                                                                                                                                                                               Ismertetés                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | A USSI-nél kattintson a <strong>Követelések</strong> &gt; <strong>Ügyfelek</strong> &gt; <strong>Minden ügyfél</strong>lehetőségre. |                                                                                                                                                                  Hozzon létre egy új ügyfélbejegyzést az FRSI-re vonatkozóan, és válassza ki az ügyfélcsoportot.                                                                                                                                                                  |
   |  F   |    Az FRSI-nél kattintson a <strong>Kötelezettségek</strong> &gt; <strong>Szállítók</strong> &gt; <strong>Minden szállító</strong> lehetőségre.     |                                                                                                                                                                    Hozzon létre egy új szállítóbejegyzést a USSI-re vonatkozóan, és válassza ki a szállítócsoportot.                                                                                                                                                                    |
   |  C   |                                  Az FRSI-nél nyissa meg az imént létrehozott szállítóbejegyzést.                                  | A Műveleti ablaktáblán az <strong>Általános</strong> lap <strong>Beállítás</strong> csoportjában kattintson a <strong>Vállalatközi</strong> lehetőségre. A <strong>Vállalatközi</strong> oldal <strong>Kereskedelmi kapcsolat</strong> lapján állítsa az <strong>Aktív</strong> csúszkát az <strong>Igen</strong> lehetőségre. A <strong>Vevő vállalat</strong> mezőben jelölje ki azt az ügyfélbejegyzést, amelyet az „A” lépésben hozott létre. |


2. Kattintson a **Projektvezetés és könyvelés** &gt; **Beállítás** &gt; **Projektvezetés és könyvelés paraméterei** lehetőségre, majd kattintson a **Vállalatközi** lapra. A paraméterek beállításának módja attól függ, hogy Ön a kölcsönbe vevő jogi személy vagy a kölcsönadó jogi személy szerepkörével rendelkezik.
   -   Ha Ön a kölcsönbe vevő jogi személy, akkor válassza ki azt a beszerzési kategóriát, amelyet azon szállítói számlák egyeztetésére használnak, amelyeket a program automatikusan hozott létre.
   -   Ha Ön a kölcsönadó jogi személy az összes kölcsönbe vevő vevő jogi személyre vonatkozóan, válassza ki az alapértelmezett projektkategóriát minden egyes tranzakciótípusra vonatkozóan. A rendszer akkor használja a projektkategóriákat az adó konfigurációjára, ha a vállalatközi tranzakciókban kiszámlázott kategóriák csak a kölcsönbe vevő jogi személy lehetőségben léteznek. Választhatja a bevétel elhatárolását is a vállalatközi tranzakciókra vonatkozóan. A rendszer akkor hajt végre elhatárolást, amikor a tranzakciók könyvelése után a tranzakciókat a vállalatközi számla könyvelésekor sztornózzák.

3. Kattintson a **Projektvezetés és könyvelés** &gt; **Beállítás** &gt; **Árak** &gt; **Transzferár** lehetőségre.
4. Válassza ki a pénznemet, a tranzakciótípust és a transzferármodellt. A számlán feltüntetett pénznem az a pénznem, amelyet a kölcsönadó jogi személyhez tartozó ügyfélbejegyzésében állítottak be kölcsönbe vevő jogi személyre vonatkozóan. A pénznem a transzferártáblában szereplő tételek egyeztetésére szolgál.
5. Kattintson **Főkönyv** &gt; **Feladás beállítása** &gt; **Vállalatközi könyvelés** lehetőségre, majd állítsa be a USSI és az FRSI kapcsolatát.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. példa: Vállalatközi munkaidő-nyilvántartás létrehozása és feladása
A USSI, a kölcsönadó jogi személy, amelynek létre kell hoznia és fel kell adnia az FRSI kölcsönbe vevő jogi személytől származó projektre vonatkozó időnyilvántartást. A feladathoz szükséges lépésekhez két belépési pont tartozik.

| Lépés | Belépési pont                                                                       | Ismertetés                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektvezetés és könyvelés** &gt; **Munkaidő-nyilvántartások** &gt; **Minden munkaidő-nyilvántartás** | Hozzon létre új munkaidő-nyilvántartást. A munkaidő-nyilvántartási sorban, a **Jogi személy** mezőben válassza ki az **FRSI** lehetőséget. A **Projektazonosító** mezőben jelölje ki az FRSI-nél a projektet. Adja meg a hét egyes napjain teljesített munkaórák számát. |
| F    | **Időnyilvántartás** oldal                                                                | A munkafolyamat futtatása után adja fel a munkaidő-nyilvántartást , majd jegyezze fel a bizonylat számát.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. példa: Vállalatközi szállítói számla létrehozása és feladása
A USSI, a kölcsönadó jogi személy, amelynek létre kell hoznia és fel kell adnia az FRSI kölcsönbe vevő jogi személytől származó projektre vonatkozó vállalatközi szállítói számlát. A szállítói számla a USSI által fizetett szállítók által végrehajtott kiszervezett munkáról és a kiadásokról szól. A feladathoz szükséges lépésekhez két belépési pont tartozik.

| Lépés | Belépési pont                                                                                      | Ismertetés                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Kötelezettségek** &gt; **Számlák** &gt; **Nyitott szállítói számlák** &gt; **Új szállítói számla** | Hozzon létre új szállítói számlát, és adja meg azokat a szolgáltatásokat, amelyeket az FRSI projekt nevében szereztek be.                                                                                                                                                                                  |
| F    | A **Szállítói számla** oldal                                                                      | Adja meg azokat a sorokat, amelyek az FRSI nevében kiszervezett szolgáltatásokat jelenítik meg. A **Sor részletei** gyorslapon, a számlasorhoz tartozó **Projekt** lapon, a **Projektvállalat** mezőben adja meg az **FRSI** értéket. Adja meg a projektet és a megfelelő információkat. Ezt követően adja fel a szállítói számlát. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. példa: Vállalatközi számla létrehozása és feladása
A vállalatközi számlát az USSI hitelnyújtó jogi entitás hozza létre és adja fel. A feladathoz szükséges lépésekhez két belépési pont tartozik.

| Lépés | Belépési pont                                                                                             | Ismertetés                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektvezetés és könyvelés** &gt; **Projektszámlák** &gt; **Vállalatközi ügyfélszámla**  | Kattintson az **Új** lehetőségre a **Vállalatközi számla létrehozása** oldal megnyitásához.                                                                                  |
| F    | **Projektvezetés és könyvelés** &gt; **Projektszámlák** &gt; **Vállalatközi ügyfélszámlák** | A **Vállalatközi számla létrehozása** oldalon adja meg azt a jogi személyt és tranzakciót, amelyet a számlának tartalmaznia kell, majd kattintson a **Keresés** lehetőségre. |
| C    | **Projektvezetés és könyvelés** &gt; **Projektszámlák** &gt; **Vállalatközi ügyfélszámlák** | Jelölje ki a tranzakciót a számlához, vagy kattintson az **Összes kijelölése** lehetőségre a lista összes tranzakciójának számlázásához, majd kattintson az **OK** lehetőségre.                  |
| D    | A **Vállalatközi számla** oldal                                                                       | Ezen az oldalon láthatja vállalatközi ügyfélszámlára vonatkozó javaslatokat.                                                                                             |
| E    | A **Vállalatközi számla** oldal                                                                       | Kattintson a **Feladás** lehetőségre.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. példa: A szállítói számla feladása és a számlázás az ügyfél részére
Ha a USSI kölcsönadó jogi személy feladja a vállalatközi ügyfélszámlát, a rendszer az FRSI kölcsönbe vevő jogi személynél létrehoz egy egyeztetett, függőben lévő szállítói számlát. A szállítói számla feladása az FRSI az USSI által megadott órák alapján készít számlát a projektről az ügyfél részére. A feladathoz szükséges lépésekhez három belépési pont tartozik.

| Lépés | Belépési pont                                                                                        | Ismertetés                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Kötelezettségek** &gt; **Számlák** &gt; **Függőben lévő szállítói számlák**                            | Ellenőrizze, hogy a számla tartalmazza-e amunkaidő-nyilvántartás értékeit, majd tegye közzé a szállítói számlát.                  |
| F    | **Projektvezetés és könyvelés** &gt; **Projektszámlák** &gt; **Projekt számlajavaslatai** | Új projektszámlát hozhat létre a projektre vonatkozóan, és ellenőrizheti, hogy a közzétett óratranzakciók megjelennek-e.            |
| C    | A **Projektszámla** oldal                                                                       | Válassza ki a projektszámlát, és kattintson a **Részletek megjelenítése** lehetőségre a költség és az értékesítési összeg ellenőrzéséhez. Ezt követően adja fel a számlát. |


További információkért lásd: [Vállalatközi projektszámlázás konfigurálása](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]