---
title: Értékesítési folyamatok
description: Ez a témakör információkat nyújt az alapvető értékesítési folyamatokról.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 58d5aa68dd5af7fc2b39caac429948e55bbc94c39dfb7fc9ae15a37cc3c92ce6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000534"
---
# <a name="sales-processes"></a>Értékesítési folyamatok

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A projektalapú szervezetekben alkalmazott értékesítési folyamatok különböznek a termékalapú szervezeteknél alkalmazott értékesítési folyamatoktól. Ez a különbség azért merül fel, mert a projektalapú szervezetek értékesítési ciklusai hosszabbak és testreszabott becslési technikákat igényelnek az egyes ügyletek elemzéséhez és árajánlatok létrehozásához. A Dynamics 365 Project Service Automation ugyanazt a funkciót használja, amelyet a Dynamics 365 Sales az értékesítési folyamatában használ. Íme néhány példa:

- Egy Potenciális ügyfél entitás használható az értékesítési folyamat nyomon követésére.
- A jogosult potenciális ügyfeleket lehetőségekként követik. Az értékesítési folyamat lehetőséggel is indulhat.
- A lehetőségekhez kapcsolódó összes műtárgy elérhető. Ezek a műtárgyak tartalmazzák az értékesítési csapatot, az érdekelt feleket, a valószínűséget, a minősítést, az értékesítési szakaszokat és az üzleti folyamatokat.
- Több árajánlat jön létre egy lehetőségre.
- Az árajánlat **Megnyertként lezárva** jelöléssel adható meg értékesítési rendeléshez. A PSA-ban az értékesítési rendelés testreszabott, és projektszerződésnek nevezik.

Az alábbi ábra egy tipikus értékesítési folyamatot mutat be egy projektalapú szervezetben.

> ![Értékesítési folyamat egy projektalapú szervezetben.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Értékesítés becslése
Az értékesítés értéke a korábban teljesített projektek és a projektek összetettsége alapján becsülhető meg. Olyan projektek esetén, amelyek kiterjesztik a korábbi projekteket, vagy olyan projektek esetében, amelyekben a beszállító szaktudása magas, és jól ismert munkasablonokat használnak, egyszerűbb becslési eljárás is használható. A bonyolultabb projektek beszerzési folyamata általában hosszabb. Ezért az értékesítés becslési folyamatban több szakasz van. A folyamat elején az értékesítési csapat a fiókkezelők és a téma szakértőinek (kkv-k) adatait használja fel, hogy magas szintű becslést készítsen az árajánlatban szereplő munka minden egyes különálló elemére. A munka ezen alkotóelemeit az árajánlat sorai képviselik. 

Létrehozhatja az ajánlat magas szintű becslését. Végül ezt a magas szintű becslést egy részletesebb becslés váltja fel, amely egy olyan projekttervre épül, amelyet a szabványosított projektsablonok segítségével készítettek. Ezek a sablonok segítenek az ütemterv felépítésében, és meghatározhatják az árajánlat és annak összetevői (árajánlatsorok) monetáris értékeit. 

Létrehozhat több árajánlatot is egy projekthez, és csoportosíthatja őket egyetlen lehetőségentitás-típusba. Végül az egyik árajánlat **Nyertesként lezárva** jelöléssel szerepel, és létrejön egy projektszerződés vagy munkadokumentum (SOW). A projektszerződés az egyes alkotóelemek (szerződéssorok) szerződéses értékét tartalmazza, amelyeket az ügyfél a szállításhoz elfogad. A SOW-ot általában Microsoft Word-dokumentumként hozzák létre. Az összes számla, amelyet az ügyfélnek küldenek a projekt teljesítése során, a projektszerződésre vagy a SOW-ra hivatkozik.

Emellett alternatív ajánlatokat is létrehozhat egy lehetőségentitás-típus alatt, vagy beállíthatja a rendszert úgy, hogy egy projektszerződés jön létre, amikor egy árajánlat nyer. Ebben az esetben csatolhat egy Word-dokumentumot, amely a SOW-ot képviseli a projektszerződés-rekordhoz.

![Árajánlat lezárása a projektszerződés létrehozásához.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Az értékesítési folyamat konfigurálása
Az üzleti folyamatok (BPF) felhasználhatók a Microsoft Dynamics 365-ben az értékesítési folyamat konfigurálásához. A BPF-ek vezetett vizuális felületet adnak az értékesítési munkatársaknak, amelyeket felhasználhatnak az ügyletek előrevitelére a vállalatra jellemző szakaszokon keresztül.

Például az Ön vállalkozása az értékesítési folyamat következő hat szakaszával rendelkezhet:

1. Minősítés
2. Becslés
3. Belső felülvizsgálat
4. Szerződés
5. Kiszállítás
6. Bezárás

Ezt a hat fázist chevronok (\>) reprezentálják, amelyeket azért kiválaszt ki, hogy kibővítse minden létrehozott lehetőségentitás-típusba.

![Üzleti folyamatok konfigurálása a Dynamics 365-ben.](media/basic-guide-3.png)
 
Előfordulhat, hogy szervezete különböző entitásokat használ fel ugyanazon ügylet reprezentálására, amint az alakul. Az értékesítési folyamat elején az ügyletet a Lehetőség entitás képviseli. Az idő múlásával és további részletek megjelenésével magas szintű becsléseket használhat egy vagy több árajánlat létrehozásához. Ha ezen árajánlatok egyikét a belső és az ügyfél érdekelt felei felülvizsgálják, akkor az Ajánlat entitás képviseli az ügyletet. Miután az ügyfél elfogadta az ajánlatot, egy projektszerződés vagy SOW képviseli az ügyletet. Ennek a viselkedésnek a támogatása érdekében a BPF-eket úgy strukturálják, hogy a folyamat egyes szakaszai különféle adatbázis-táblákhoz legyenek kapcsolva.

Az értékesítési folyamat **Minősítés** szakaszát egy Lehetőség entitás támogathatja. A **Becslés** és a **Belső felülvizsgálat** szakaszokat egy Árajánlat entitás támogathatja. A **Szerződés**, **Teljesítés** és **Lezárás** szakaszokat egy Projektszerződés entitás támogathatja.

Ahogyan az ügyletek a szakaszokon át mozognak, a rendszer felkéri Önt a megfelelő entitásrekord létrehozására, hogy segítsen és útmutatást nyújtson a folyamat során. A szakaszok feltételesek lehetnek. Például, ha csak egy árajánlat belső felülvizsgálatára van szüksége, ha az árajánlat egyéni árlistát használ, akkor konfigurálhatja ezt a feltételt az üzleti folyamat megfelelő szakaszában. A **Belső felülvizsgálat** szakasz csak akkor jelenik meg, ha egyéni árlistát használnak. Az összes többi ügylet és árajánlat esetében a **Becslés** szakaszt a **Szerződés** szakasz követi.

> [!NOTE]
> A PSA speciális oldalakat tartalmaz a Lehetőség, Ajánlat, Megrendelés és Számla entitások számára. E szervezetek projektinformációs oldalainak felhasználásával létre kell hoznia Project Service lehetőségeket, árajánlatokat, megrendeléseket és számlákat. Ha másik oldalt használ egy rekord létrehozásához, akkor nem tudja megnyitni a rekordot a **Projektinformáció** oldalon. Ha egy rekordot a **Projektinformáció** oldalról szeretne megnyitni, akkor törölnie kell a rekordot, és újra létre kell hoznia a **Projektinformáció** oldalon. A **Projektinformáció** oldalon az ezen entitástípusok mindegyikének üzleti logikája biztosítja, hogy a rekord **Típus** mezője helyesen legyen beállítva, és az összes kötelező fogalom megfelelően inicializálva legyen.

> ![Projektinformáció új rendeléshez.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>A Project Service Automation és az értékesítés közötti különbségek
Noha a PSA-ban az értékesítési folyamat az Értékesítés értékesítési folyamatának alapvető képességeit használja, a projektalapú szervezetek üzleti gyakorlatának eltérései miatt vannak bizonyos alapvető különbségek. Íme néhány példa:

- **Projektajánlatok** - A Project Service Automation szolgáltatásban az ajánlat lezárul, miután a projektszerződést létrehozták az ajánlatból. Az Értékesítésben nyitva tarthatja az árajánlatot, miután megnyerte. Ennek a különbségnek az az oka, hogy a projektalapú szervezetek számára jobb egy ajánlat és a projektszerződés közötti megfeleltetés. 
- **Aktiválás és revíziók** - A PSA-ban az aktiválás és revíziók nem támogatottak a projektajánlatokban. Az Értékesítésben az árajánlat zárolható a további szerkesztések megakadályozása érdekében.
- **Ajánlat lezárása elvesztettként vagy megnyertként** - A PSA-ban, amikor a projektárajánlatot megnyertként vagy elvesztettként zárják le, akkor a lehetőség nyitva marad. A lehetőség összes többi ajánlata elvesztettként záródik le. Az Értékesítésben, amikor az árajánlatot megnyertként vagy elvesztettként zárják le, a felhasználót kéri a rendszer, hogy tegyen lépést a lehetőséggel kapcsolatban. A felhasználói beviteltől függően a mögöttes lehetőség zárt vagy nyitva maradhat.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Az árajánlatok és a projekttervek felülvizsgálatainak nyomon követése az értékesítési ciklusban
A PSA-ban nem követheti nyomon az árajánlatokon végzett módosításokat. Ehelyett meg kell jelölnie a meglévő ajánlatot **Elvesztettként lezárva** állapotra, majd létre kell hoznia egy új ajánlatot. Másolhat egy ajánlatot vagy klónozhat egy projektalapú ajánlatot a PSA használatával.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Az árajánlatok és a projektszerződések megjegyzéseinek és jóváhagyásának nyomon követése
Az árajánlatok és a projektszerződések felülvizsgálatát és jóváhagyását a nyilvántartási fal és a hozzászólások segítségével kezelheti. A szervezet létrehozhat egyéni munkafolyamatokat és beépülő modulokat az áttekintési és jóváhagyási munkaelemek értesítéseinek hozzárendeléséhez, átirányításához, kibővítéséhez és kezeléséhez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]