---
title: A csak projektalapú árajánlatokra jellemző fogalmak
description: Ez a cikk a Microsoft projektajánlatairól nyújt tájékoztatást Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824330"
---
# <a name="concepts-unique-to-project-based-quotes"></a>A csak projektalapú árajánlatokra jellemző fogalmak

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Mielőtt elkezdené használni a projektajánlatokat a Microsoftban Dynamics 365 Project Operations, tisztában kell lennie a következő kulcsfogalmakkal.

## <a name="owning-company"></a>Tulajdonos vállalat

A tulajdonos vállalat képviseli azt a jogi személyt, amely a projekt megvalósításának tulajdonosa. Az árajánlatban szereplő vevőnek érvényes vevőnek kell lennie az adott jogi személyben a Pénzügyi és műveleti alkalmazásokban. A tulajdonos vállalat pénznemének és a projektalapú árajánlatban kiválasztott szerződő egység pénznemének meg kell egyeznie.

## <a name="contracting-unit"></a>Szerződő részleg

A szerződő egység azt a részleget vagy gyakorlatot képviseli, amely a projekt teljesítését birtokolja. Az egyes szerződő részlegekre vonatkozóan beállíthat erőforrásköltségeket. Amikor erőforrásköltségeket ad meg egy erőforráshoz egy szerződő egységben, különböző költségrátákat állíthat be a szerződő egység által kölcsönvett erőforrásokhoz, illetve a gazdálkodó más részlegeihez vagy gyakorlatához. Ezeket a költségrátákat transzferáraknak, erőforrás-kölcsönzésnek vagy átváltási áraknak nevezzük. Amikor beállítja az erőforrások más részlegektől való kölcsönzésének költségét, a költségrátákat a kölcsönzési részleg pénznemében állíthatja be.

## <a name="cost-currency"></a>Költség pénzneme

A Project Operations költségpénzneme az a pénznem, amelyben a költségek jelentésre kerülnek. Ez a pénznem az árajánlat, a szerződés és a **projekt Szerződő egység** mezőjéhez csatolt pénznemből származik. A projekttel kapcsolatos költségek bármilyen pénznemben elszámolhatók. A pénznemek átváltása azonban a költségek rögzítésének pénzneméről a projekt költségpénznemére történik.

Mivel a platformon az átváltási árfolyamok nem lehetnek dátumfüggőek, a képernyőn megjelenő költségösszegek idővel változhatnak, ha frissíti a Dataverse devizaárfolyamokat. Az adatbázisban rögzített költségek azonban változatlanok maradnak, mivel az összegek abban a pénznemben vannak tárolva, amelyben felmerültek.

## <a name="sales-currency"></a>Értékesítés pénzneme

A Project Operations rendszerben az értékesítési pénznem az a pénznem, amelyben a becsült és a tényleges értékesítési összegeket rögzítik és megjelenítik. Ez az a pénznem is, amelyben a vevőnek számlázzák az ügyletet. Projektajánlat esetén az alapértelmezett értékesítési pénznem a vevőből vagy a partnerrekordból van beállítva, és az árajánlat létrehozásakor módosítható. Az értékesítési pénznem azonban nem módosítható az árajánlat mentése után. Az alapértelmezett termék- és projektárlisták az ajánlat értékesítési pénzneme alapján vannak beállítva.

A költségekkel ellentétben az értékesítési értékek csak **az értékesítési pénznemben rögzíthetők** .

## <a name="billing-method"></a>Számlázási mód

A projektek jellemzően fix díjas és fogyasztásalapú szerződéskötési modellekkel rendelkeznek. A Project Operations alkalmazásban a projekt szerződéskötési modelljét a számlázási módszer képviseli. A számlázási módszernek két értéke van: idő és anyag, valamint rögzített ár.

- **Idő és anyag**  – Fogyasztásalapú szerződéskötési modell, ahol minden felmerülő költséget a megfelelő bevétel fedez. A további költségek megbecslése vagy felmerülése során a megfelelő becsült és tényleges értékesítés is növekedni fog. A számlázási módszert használó árajánlatsorokon nem meghaladandó korlátokat adhat meg. Ily módon korlátozhatja a tényleges bevételt. A becsült bevételt nem befolyásolják a korlátok túllépésének tilalma.
- **Fix ár**  – Rögzített díjú szerződéskötési modell, ahol az értékesítési értékek függetlenek a felmerült költségektől. Az értékesítési érték rögzített, és további költségek becslésével vagy felmerülésével.

## <a name="project-price-lists"></a>Projektárlisták

A projektárlisták olyan árlisták, amelyek az alapértelmezett árak, nem pedig a költségdíjak megadására szolgálnak az időhöz, a költséghez és a projekthez kapcsolódó egyéb összetevőkhöz. Több árlista is lehet, és mindegyik lista rendelkezhet saját dátumérvényességgel az egyes projektárajánlatokhoz. A Project Operations nem támogatja az egymást átfedő dátumhatékonyságot a projektárlistákhoz.

## <a name="product-price-lists"></a>Termékárlisták

A termékárlisták olyan árlisták, amelyek az árajánlat termékalapú sorainak alapértelmezett árainak, nem pedig költségdíjainak megadására szolgálnak. Árajánlatonként csak egy termékárlista van.

## <a name="transaction-classes"></a>Tranzakció osztályai

A Project Operations négyféle típusú tranzakciót támogat:

- Időpont
- Költség
- Anyag
- Díj

A költség- és értékesítési értékek becsülhetők és merülhetnek fel a Idő, a Költség **és** az Anyag **tranzakciós osztályokban**. **·**  **A díj** csak bevételi tranzakciós osztály.

## <a name="work-entities-and-billing-entities"></a>Munkaentitások és számlázási entitások

A projektek és a feladatok olyan entitások, amelyek a munkát képviselik. Az árajánlatsorok és a szerződéssorok olyan entitások, amelyek a számlázást képviselik. Különböző munkaentitásokat kapcsolhat a számlázási beállításokhoz, ha árajánlatsorokhoz vagy szerződéssorokhoz társítja őket.

## <a name="multi-customer-deals"></a>Több ügyfél közötti üzletek

Többügyfeles ügyletekre akkor kerül sor, ha számlánként egynél több vevő van. Íme néhány tipikus példa:

- **Eredetiberendezés-gyártó (OEM) vállalkozások és partnereik**  – A partnerek és viszonteladók olyan terméket értékesítenek, amely értéknövelt szolgáltatásokat tartalmaz. Az ügyféllel kötött megállapodás során az OEM általában felajánlja a projekt egy részének finanszírozását.
- **Közszférabeli projektek**  – Egy helyi önkormányzat több osztálya vállalja, hogy finanszíroz egy projektet, és a számlázás egy korábban egyeztetett felosztás szerint történik. Például egy iskolai körzet és a város vagy a helyi önkormányzat egy osztálya vállalja, hogy egy uszoda épületét finanszírozza.

## <a name="invoice-schedules"></a>Számlaütemezések

A számlaütemezések az egyes árajánlatsorokra vonatkoznak, és nem kötelezőek. A számlaütemezések meghatározott kezdő és záró dátumok, valamint a számla gyakorisága alapján jönnek létre. A rendszer a szerződés szakaszában használja őket, amikor az automatikus számlalétrehozási folyamat konfigurálva van. Az árajánlati szakaszban a számlaütemezések nem kötelezőek. Ha az árajánlat szakaszában hozták létre őket, akkor a projektajánlat megnyerésekor létrehozott projektszerződésbe másolódnak.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Eltérések a Dynamics 365 értékesítési ajánlatoktól

A Project Operations-ajánlatok Dynamics 365 értékesítési ajánlatokra épülnek. Vannak azonban olyan fontos eltérések a funkciókban, amelyekkel tisztában kell lennie:

- A Project Operations árajánlatok két különböző típusú sorból állnak: az egyik a projektekhez, a másik a termékekhez.
- A Project Operations árajánlatok saját oldal- és felhasználói felületi elemekkel, üzleti szabályokkal, beépülő modulok üzleti logikájával és ügyféloldali parancsfájlokkal rendelkeznek, amelyek megkülönböztetik őket az értékesítési ajánlatoktól.
- A Sales (Értékesítések) részben több rendelést is csatolhat egyetlen értékesítési ajánlathoz. A Project Operations alkalmazásban csak egy projektszerződést csatolhat egy projektajánlathoz.
- Ha megnyer egy értékesítési árajánlatot, a kapcsolódó lehetőség nyitva maradhat. A projekt árajánlatának megszerzése után a kapcsolódó lehetőség le lesz zárva.
- Az értékesítési ajánlat nem tartalmaz olyan mezőket és fogalmakat, amelyeket a projektajánlat tartalmaz. A mezők közé tartozik a **Szerződő részleg**, a **Partnerkezelő** és a **Számlázási kapcsolattartó neve**.
- Az értékesítési ajánlatokat és a projektajánlatokat a értékkészlet-alapú **Típus** mező azonosítja. Értékesítési ajánlat esetén a mező **értéke Cikkalapú**. Projektajánlat esetén az érték **Munkaalapú**.

Ezen különbségek miatt nem javasoljuk, hogy az értékesítési ajánlatokat és a Project üzemeltetési árajánlatokat felcserélhetően használja.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
