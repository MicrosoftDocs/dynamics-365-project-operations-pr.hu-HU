---
title: Projekt-előrejelzések és költségvetések
description: A Microsoft Dynamics 365 Finance projekt-előrejelzéseket és projektköltségvetéseket biztosít a projektek kezeléséhez és ellenőrzéséhez.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078205"
---
# <a name="project-forecasts-and-budgets"></a>Projekt-előrejelzések és költségvetések

[!include [banner](../includes/banner.md)]

Két módon kezelheti és ellenőrizheti a projektjeit: projekt-előrejelzésekkel és projektköltségvetésekkel. 

Projekt-előrejelzést akkor érdemes használni, ha a szervezet az operatív szempontokra összpontosít, és az egyes tranzakciókból származó bevételekre és költségekre fókuszál. Ha a szervezet nagyobb figyelmet fordít a pénzügyekre, akkor érdemes a költségvetést alkalmazni. 

A projekt-előrejelzések és a projektköltségvetések előrejelzési modelleket használnak a tervezett tranzakciós összegek tárolására. 

Mindegyik metódusnak megvannak a maga előnyei. A következő pontokat érdemes megfontolnia a szervezetre vonatkozó módszer kiválasztása előtt.

|   Felosztási mód       |           Projekt-előrejelzés            |        Projekt-költségvetés                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Időszakfelosztás**     | A tranzakciókat nem lehet kifejezetten a pénzügyi időszakra felosztani. Ehelyett az előrejelzés és az előrejelzés ellenőrzése a projekt élettartamán alapul. Mivel az előrejelzések egy adott dátumon alapulnak, az időszakot a dátumtól kell lekövetkeztetni. | A tranzakciókat az egész projektre vagy egy pénzügyi időszakra oszthatja fel. Ha egy időszakra osztja fel, akkor a fel nem használt összegeket a következő pénzügyi időszakra viszi át. |
| **Tranzakciók megtekintése**  | Az előrejelzési űrlapokon megtekintheti a tranzakciókat, ahol a hierarchiától függetlenül megtekintheti az egész vállalatra és az összes projektre vonatkozó előrejelzéseket. Ha egy adott projektre szeretne összpontosítani, akkor szűrnie kell az adatokat.                                       | Egyetlen projekthierarchia tervezett tranzakcióit is megtekintheti. Ezért megtekintheti a szülő projekt vagy alprojektjeinek tranzakciós adatait.                 |
| **Tranzakciós változók** | Ha előrejelzési tranzakciókat ad meg, akkor a tényleges tranzakcióhoz tartozó összes attribútumot használhatja. Ez nagyobb részletességet tesz lehetővé az előrejelzésben. Megadhatja például a mennyiségekre, a munkavállalókra, a tételekre vagy a sortulajdonságokra vonatkozó adatokat.         | A költségvetés részleteinek megadásakor csak az összegeket, a kategóriákat és a tevékenységeket használhatja.                    |
| **Biztonság**              | Az előrejelzés az előrejelzési űrlapokon megadott tranzakciókon alapul, és nem tartalmaz folyamatellenőrzési mechanizmust. Az előrejelzési űrlapra vonatkozó jogosultságokkal rendelkező alkalmazottak jóváhagyás nélkül módosíthatják az információkat.                                        | A költségvetés a munkafolyamat rendszert használja, amely lehetővé teszi a változások kezelését, és lehetővé teszi a módosítások előzményeinek megtartását.         |
| **Bejegyzéstípusok**           | Az előrejelzési tranzakciók bejegyzései az egységek számától, illetve a költségtől és az értékesítési egységáraktól függenek.  | A költségvetés részletei az összegeken alapulnak, amelyek a költségek és a bevételek között oszlanak meg.                                          |
| **Előrejelzési modellek**       | Mivel az egyes előrejelzéseket modellhez kell rendelni, több előrejelzési modellt is létrehozhat, valamint almodelleket is beállíthat.           | A projektköltségvetés készítése korlátozza a költségvetés-készítéshez használt előrejelzési modelleket. A rövidebb előrejelzési modellek segítségével növelheti a prognózis konzisztenciáját.                           |
| **Költségek túlfutása**         | Csak olyan tranzakciók bevitelét engedélyezheti vagy tilthatja el, amelyek túllépést eredményeznek.   | A projektköltségvetés készítése további ellenőrzési lehetőségeket biztosít a felhasználók számára. Lehetőség van a figyelmeztetések és a túlfutások engedélyezésére.                    |
| **Vezérlő**               | Az előrejelzés-ellenőrzést az előrejelzés-csökkentés segítségével hajthatja végre. A tényleges összegeket a rendszer az előrejelzési tranzakciós egyenlegekből vonja le auditnapló nélkül. Ez nehezebbé teheti a tényleges tranzakciók helyének nyomon követését.                   | A projektköltségvetés ellenőrzésében a rendszer kivonja a tényleges összegeket a fennmaradó költségvetés összegeiből. Ez világosabb auditnaplót tesz lehetővé.                                   |

## <a name="project-forecasts"></a>Projekt-előrejelzések
A projekt-előrejelzés használatakor minden tranzakciótípus esetén megadhat előrejelzési tranzakciókat az előrejelzési űrlapokon. A tényleges tranzakciókhoz rendelkezésre álló összes attribútum felhasználható előrejelzési tranzakcióhoz – például sor jövedelmezősége, sorattribútumok, munkavállalók vagy leírások. Azt is előrevetítheti, hogy a költség felmerülése után mennyi idővel számlázza azt az ügyfélnek. 

A projekt-előrejelzés tranzakciói az egységeken és az összegeken alapulnak. 

Az egyes projektek előrejelzéseit egy előrejelzési modellhez kell társítania. Ha egy előrejelzési tranzakciót ad meg, a rendszer automatikusan javasolja az előrejelzési modellt. Az előrejelzési modell az előrejelzési tranzakciók tárolójáként működik. 

Az előrejelzési modelleket a modell almodelljeiként jelölheti meg. Ez lehetővé teszi, hogy régiónként, időszakonként vagy osztályonként készítsen előrejelzést. Az előrejelzési tranzakciókat modellbe másolva új modellt hozhat létre, és a tranzakciókat átviheti a főkönyvbe is. Mivel az előrejelzés és a modell között egy az egyhez kapcsolat van, mindegyik előrejelzési modell külön költségvetést alkot egy projekthez. 

Az előrejelzési modellek az előrejelzések csökkentését használhatják a projektek ellenőrzési mechanizmusaként. Az előrejelzés-csökkentésben a tényleges tranzakciók csökkentik az előrejelzési tranzakciós egyenlegeket. Mivel azonban az előrejelzés-csökkentés a hierarchiában legmagasabban elhelyezkedő projektre vonatkozik, korlátozott képet ad az előrejelzésben bekövetkezett változásokról. Ha például egy dolgozó egy alprojekthez van társítva, akkor a rendszer a munkavállaló tényleges tranzakcióit a szülő projektbe könyveli. Ez megnehezíti a változások nyomon követését, mert nem tudja könnyen meghatározni, hogy mely alprojekt mely tranzakciója okozta az előrejelzési összeg csökkenését. Ezért célszerű létrehozni egy előrejelzési modell egy példányát az előrejelzés-csökkentés általi használathoz. Ezután jelentések segítségével megtekintheti, hogy mi volt eredetileg előrejelezve. 

A projektek előrejelzéseit áttekintheti, átmásolhatja, törölheti, illetve átviheti a főkönyvi költségvetésbe. Azonban nincs folyamat-ellenőrzés. Az előrejelzési űrlapra vonatkozó jogosultsággal rendelkező alkalmazottak áttekintés nélkül módosíthatják az információkat.

-   **Módosítás** – Módosíthatja az előrejelzési tranzakciókat azokon az űrlapokon, amelyeken az eredeti bejegyzések létrehozásra kerültek.
-   **Másolás vagy törlés** – Az előrejelzési tranzakciók másolása során az egyik előrejelzési modell tranzakciós sorait egy másik előrejelzési modellbe másolja. Ha töröl egy előrejelzést, akkor az előrejelzési modellből törli az előrejelzett tranzakciókat. A másolt vagy törölt előrejelzési tranzakciók korlátozásához jelöljön ki adott tranzakciótípusokat és dátumokat. Ez lehetővé teszi az előrejelzés csak bizonyos részeinek másolását vagy törlését.
-   **Átvitel** – A projekt-előrejelzésnek a főkönyvi költségvetésbe történő átvitelekor az előrejelzési modell előrejelzési tranzakcióit átviszi a főkönyvi költségvetésbe. A korábban átvitt tranzakciókat felülírhatja abban a főkönyvi költségvetésben, amelybe átviszi a projekt-előrejelzését.

## <a name="project-budgets"></a>Projektköltségvetések
A projektköltségvetés készítése egyszerűbb módszer, mint az előrejelzés, bár az előrejelzési modellekkel nem integrálható. Az eredeti költségvetés részleteihez és a módosításaihoz egyetlen beviteli űrlapot használ, és lehetővé teszi az olyan leképezéseket, amelyek csak összegen, kategórián vagy tevékenységen alapulnak. 

A projektköltségvetés készítése során minden eredeti költségvetést és módosítást el kell küldeni egy projekt-munkafolyamatba jóváhagyás céljából. A munkafolyamatok nagyobb ellenőrzést biztosítanak a folyamat felett, és a módosítási előzmények rekordját is létrehozzák. 

A projektköltségvetés készítése a főkönyvi költségvetés készítéséhez hasonlít, de gyorsabban és könnyebben állítható be. A főkönyvi költségvetés készítésének számos opcióját (például a számsorozatokat vagy a pénznemet) nem kell külön beállítani a projektek számára.

A projektköltségvetéseket a rendszer automatikusan két előrejelzési modellhez társítja. Az egyik az eredeti költségvetés, a másik pedig a fennmaradó költségvetés. Ezért az előrejelzési modelleken alapuló jelentések használhatnak költségvetési adatokat. A projektköltségvetés véglegesítése esetén a rendszer a kapcsolódó modellek alapján hozza létre az előrejelzési tranzakciókat, amelyeket jelentéskészítési és ellenőrzési célokra használnak.

## <a name="forecast-models"></a>Előrejelzési modellek
Az előrejelzési modellek egyrétegű hierarchiával rendelkeznek. Ez azt jelenti, hogy egy projekt előrejelzését egyetlen előrejelzési modellhez kell társítani.

Ha projekt-előrejelzést használ, akkor a modelleket almodellekként azonosíthatja. Ezután létrehozhat előrejelzéseket részlegenként, időszakonként vagy régiónként. Létrehozhat például egy évre vonatkozó előrejelzési modellt, majd létrehozhatja az északkeleti, délkeleti, északnyugati és délnyugati területi előrejelzések almodelljét, amelyek a regionális vezetők küldenek be. Ha a rendelkezésre álló jelentésekben különböző beállításokat választ ki, akkor az adatokat megtekintheti teljes előrejelzésenként vagy almodellenként.





[!INCLUDE[footer-include](../includes/footer-banner.md)]