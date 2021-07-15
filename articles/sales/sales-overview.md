---
title: Értékesítési folyamat áttekintése
description: Ez a témakör információkat nyújt az alapvető értékesítési folyamatokról.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: ed9731193e83eebd35e979adffcea529a289b9c5
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368344"
---
# <a name="sales-process-overview"></a>Értékesítési folyamat áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A projektalapú szervezetekben alkalmazott értékesítési folyamatok különböznek a termékalapú szervezeteknél alkalmazott értékesítési folyamatoktól. Ez azért van, mert a projektalapú szervezetek értékesítési ciklusai hosszabbak és testreszabott becslési technikákat igényelnek az egyes ügyletek elemzéséhez és árajánlatok létrehozásához. A Dynamics 365 Project Operations az alábbi, értékesítési folyamatban használt funkciókat használja:

- Egy Potenciális ügyfél rekord használható az értékesítési folyamat nyomon követésére.
- A jogosult potenciális ügyfeleket lehetőségekként követik.
- A lehetőségekhez kapcsolódó összes műtárgy elérhető. Ezek a műtárgyak tartalmazzák az értékesítési csapatot, az érdekelt feleket, a valószínűséget, a minősítést, az értékesítési szakaszokat és az üzleti folyamatokat.
- Több árajánlat jön létre egy lehetőségre.
- Az árajánlat **Megnyertként lezárva** állapotú lesz az értékesítési rendelés létrehozásához. A Project Operationsben az értékesítési rendelés testreszabott, és projektszerződésnek nevezik.

## <a name="estimate-a-sale"></a>Értékesítés becslése
Az értékesítés értéke a korábban teljesített projektek és a projektek összetettsége alapján becsülhető meg. Olyan projektek esetén, amelyek kiterjesztik a korábbi projekteket, vagy olyan projektek esetében, amelyekben a beszállító szaktudása magas, és jól ismert munkasablonokat használnak, egyszerűbb becslési eljárás is használható. A bonyolultabb projektek beszerzési folyamata általában hosszabb. Ezért az értékesítés becslési folyamatban több szakasz van. A folyamat elején az értékesítési csapat a fiókkezelők és a téma szakértőinek (kkv-k) adatait használja fel, hogy magas szintű becslést készítsen az árajánlatban szereplő munka minden egyes különálló eleméhez. A munka ezen alkotóelemeit az árajánlat sorai képviselik. 

Létrehozhatja az ajánlat magas szintű becslését. Végül ezt a magas szintű becslést egy részletesebb becslés váltja fel, amely egy olyan projekttervre épül, amelyet a szabványosított projektsablonok segítségével készítettek. Ezek a sablonok segítenek az ütemterv felépítésében, és meghatározhatják az árajánlat és annak összetevői (árajánlatsorok) monetáris értékeit. 

Létrehozhat több árajánlatot is egy projekthez, és egyetlen lehetőségrekordba csoportosíthatja őket. Végül az egyik árajánlat **Nyertesként lezárva** jelöléssel szerepel, és létrejön egy projektszerződés vagy munkadokumentum (SOW). A projektszerződés az egyes alkotóelemek (szerződéssorok) szerződéses értékét tartalmazza, amelyeket az ügyfél a szállításhoz elfogad. A SOW-ot általában Microsoft Word-dokumentumként hozzák létre. Az összes számla, amelyet az ügyfélnek küldenek a projekt teljesítése során, a projektszerződésre vagy a SOW-ra hivatkozik.

Emellett alternatív árajánlatokat is létrehozhat egy lehetőségrekord alatt, vagy beállíthatja a rendszert úgy, hogy egy projektszerződés jöjjön létre, amikor egy árajánlat nyer. Ebben az esetben csatolhat egy Word-dokumentumot, amely a SOW-ot képviseli a projektszerződés-rekordhoz.

## <a name="configure-the-sales-process"></a>Az értékesítési folyamat konfigurálása
Az üzleti folyamatok felhasználhatók az értékesítési folyamat konfigurálásához. Ezek a folyamatok irányított vizuális felületet biztosítanak az üzleteknek az értékesítési folyamat szakaszain történő átvitelére.

Például az Ön vállalkozása az értékesítési folyamat következő hat szakaszával rendelkezhet:

1. Megfelel
2. Becslés
3. Belső felülvizsgálat
4. Szerződés
5. Kiszállítás
6. Bezárás
 
Előfordulhat, hogy szervezete különböző entitásokat használ fel ugyanazon ügylet reprezentálására, amint az alakul. Az értékesítési folyamat elején az ügyletet a Lehetőség entitás képviseli. Az idő múlásával és további részletek megjelenésével magas szintű becsléseket használhat egy vagy több árajánlat létrehozásához. Ha ezen árajánlatok egyikét a belső és az ügyfél érdekelt felei felülvizsgálják, akkor az Ajánlat entitás képviseli az ügyletet. Miután az ügyfél elfogadta az ajánlatot, egy projektszerződés vagy SOW képviseli az ügyletet. Ennek a viselkedésnek a támogatása érdekében a BPF-eket úgy strukturálják, hogy a folyamat egyes szakaszai különféle adatbázis-táblákhoz legyenek kapcsolva.

Az értékesítési folyamat **Minősítés** szakaszát egy Lehetőség entitás támogathatja. A **Becslés** és a **Belső felülvizsgálat** szakaszokat egy Árajánlat entitás támogathatja. A **Szerződés**, **Teljesítés** és **Lezárás** szakaszokat egy Projektszerződés entitás támogathatja.

Ahogyan az ügyletek a szakaszokon át mozognak, a rendszer felkéri Önt a megfelelő entitásrekord létrehozására, hogy segítsen és útmutatást nyújtson a folyamat során. A szakaszok feltételesek lehetnek. Például, ha csak egy árajánlat belső felülvizsgálatára van szüksége, ha az árajánlat egyéni árlistát használ, akkor konfigurálhatja ezt a feltételt az üzleti folyamat megfelelő szakaszában. A **Belső felülvizsgálat** szakasz csak akkor jelenik meg, ha egyéni árlistát használnak. Az összes többi ügylet és árajánlat esetében a **Becslés** szakaszt a **Szerződés** szakasz követi.

> [!NOTE]
> A Project Operations külön oldallal rendelkezik a Lehetőség, az Árajánlat, a Megrendelés és a Számla entitásrekordhoz. Ezeket a rekordokat a projekt információs lapjain kell létrehoznia ezekhez az entitásokhoz. Ellenkező esetben a rekordokat nem lehet megnyitni a **Projektinformációk** oldalon. Ha meg szeretne nyitni egy rekordot a **Projektinformációk** oldalon, akkor törölnie kell a rekordot, majd újra létre kell hoznia a **Projektinformációk** oldalon, ahol az összes entitástípus üzleti logikája biztosítja, hogy a rekord **Típus** mezője helyesen legyen beállítva, és az összes kötelező fogalom helyesen legyen inicializálva.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Az árajánlatok és a projekttervek felülvizsgálatainak nyomon követése az értékesítési ciklusban
A Project Operationsben nem követheti nyomon az árajánlatokon végzett módosításokat. Ehelyett meg kell jelölnie a meglévő ajánlatot **Elvesztettként lezárva** állapotra, majd létre kell hoznia egy új ajánlatot. Másolhat egy árajánlatot, illetve klónozhat egy projektalapú árajánlatot.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Az árajánlatok és a projektszerződések megjegyzéseinek és jóváhagyásának nyomon követése
Az árajánlatok és a projektszerződések felülvizsgálatát és jóváhagyását a nyilvántartási fal és a hozzászólások segítségével kezelheti. A szervezet létrehozhat egyéni munkafolyamatokat és beépülő modulokat a vélemények értesítéseinek hozzárendeléséhez, átirányításához, felterjesztéséhez és kezeléséhez, illetve a munkaelemek jóváhagyásához.


[!INCLUDE[footer-include](../includes/footer-banner.md)]