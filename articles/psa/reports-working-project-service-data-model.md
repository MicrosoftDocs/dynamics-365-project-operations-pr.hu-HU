---
title: Munka a Project Service Automation adatmodelljével
description: Ez a témakör információt nyújt az adatmodell működéséről.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c212ef2c9fd9dcd6be0b8f0a31aa5a948176bc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147656"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Munka a Project Service Automation adatmodelljével

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

A Dynamics 365 Project Service Automation kiterjeszti más alkalmazás entitásokat, és bevezeti saját entitásokat az Common Data Service adatmodellben. Ez a témakör leírja azokat az entitásokat, amelyekkel tipikus PSA jelentési forgatókönyvekben találkozhat.

## <a name="reporting-on-opportunities"></a>Jelentés a lehetőségekről

A Project Service Automation kibővíti a Dynamics 365 Sales **Opportunity** entitását olyan mezők hozzáadásával, amelyek lehetővé teszik a projekt alapú forgatókönyveket. Ezeket a mezőket egy sémanév azonosítja, amelyet az **msdyn\_** előtaggal jelölnek meg. Az egyik új terület, amely a PSA-lehetőségek beszámolása szempontjából fontos a **Rendelés típusa**. Ennek a mezőnek a **Munka alapú** értéke azt jelzi, hogy a lehetőség PSA lehetőség. Az entitáshoz hozzáadott egyéb mezők között szerepel a **Szerződő Szervezet**, amely megragadja a lehetőséget birtokló szervezetet, és a **Számlavezető**, amely rögzíti a lehetőségért felelős számlavezető nevét.

A **Lehetőség sor** entitás olyan mezőket is tartalmaz, amelyek a Project Service-hez kapcsolódnak. A **Számlázási módszer** jelzi, hogy az opció sorát idő- és anyag alapon, vagy rögzített áron kell-e számlázni, és a **Projekt** rögzíti annak a projektnek a nevét, amely támogatja a lehetőséget. Egyéb mezők, amelyekről beszámolhat a sor elfogási költségeiről és az ügyfél költségvetési összegeiről.

## <a name="reporting-on-quotes"></a>Jelentés az árajánlatokról

A PSA a projekthez kapcsolódó mezők hozzáadásával kibővíti az Értékesítési **Ajánlat** entitást. A **Megrendelés típusa** megkülönbözteti a PSA és a nem PSA árajánlatokat. Ennek a mezőnek a **Munka alapú** értéke azt jelzi, hogy az ajánlat PSA-ajánlat. A PSA-árajánlatok jelentése szempontjából releváns mezők között szerepelnek az összegmezők , például: **Díjköteles költségek**, **Nem terhelhető költségek**, **Bruttó fedezet**, **Becslések** és **Költségvetés**. Egyéb hasznos mezők jelzik, hogy az árajánlat jövedelmező-e, vajon teljesül-e az ütemezés szerint, és megfelel-e az ügyfél költségvetési várakozásainak.

A PSA kiterjeszti az Értékesítési **Árajánlat sor** entitást. Az egyik mező, amelyet a PSA hozzáad, a **Számlázási módszer**, amely megmutatja, hogy az árajánlat sorának hogyan kell számlázni (idő és anyagok, vagy rögzített ár). Az entitáshoz hozzáadott egyéb mezők rögzítik a kapcsolódó projektet, amely támogatja az árajánlati sort, a számlázást, a költségeket és a költségvetést.

A PSA új árajánlatokkal kapcsolatos entitásokat is hozzáad a Dynamics 365 adatmodellhez. Íme néhány példa:

- **Árajánlat sor részlete** - Ez az entitás az ajánlati sor projekt becslés részleteit tartalmazza. Minden ajánlatsorhoz két rekord tartozik. Az egyik rekord az árajánlat sor költségeit és költségeit, a másik rekord az árajánlat sorának értékesítését és eladási részleteit tárolja.
- **Árajánlatsor számla ütemezése** - Ez az entitás tartalmazza az árajánlati sor számlázási ütemezését. Ezt az ütemezést az árajánlati sorhoz rendelt számlázási gyakoriság alapján állítják elő.
- **Árajánlat sor mérföldköve** - Ez az entitás a rögzített árú árajánlati sorok számlázási mérföldköveit tartalmazza.
- **Árajánlat sor elemzési bontás** - Ez az entitás az árajánlat sor pénzügyi részleteit tartalmazza. Ezek a részletek hasznosak lehetnek az árajánlati eladások és a becsült költségek különféle dimenziók szerinti jelentésére.

Egyéb elemek, amelyeket a PSA hozzáad az árajánlatokhoz, a következők: **Árajánlatsor projekt árlista**, **Árajánlatsor erőforrás kategória** és **Árajánlat sor tranzakciós kategória**.

![Árajánlatot, árajánlatsort és projektkapcsolatokat mutató diagram](media/PS-Reporting-image2.png "Árajánlatot, árajánlatsort és projektkapcsolatokat mutató diagram")

## <a name="reporting-on-project-contracts"></a>Jelentés a projektszerződésekről

A PSA kiterjeszti az Értékesítési **Megrendelés** entitást, amelyet a projektszerződések rögzítésekor használnak. Hozzátesz egy fontos új mezőt, a **Megrendelés típusa**, amely a szerződést PSA projektszerződésként azonosítja értékesítési rendelés helyett. Ennek a mezőnek a **Munka alapú** értéke azt jelzi, hogy a megrendelés PSA projekt szerződés. A **Megrendelés** entitáshoz hozzáadott egyéb új mezők a költségekkel, a PSA-szerződés státusával és a szerződéssel bíró szervezettel kapcsolatos részleteket tartalmaznak.

A PSA kiterjeszti az **Értékesítési rendelés sor** entitását is. A hozzáadott mezők között szerepelnek azok a mezők, amelyek rögzítik a számlázási módszert (idő és anyagok vagy rögzített ár), az ügyfél költségvetési összegeit és az alapul szolgáló projektet.

A PSA új entitásokat is felvesz, amelyeket projektszerződésekre terveztek. Íme néhány példa:

- **Projektszerződés sor részletek** - Ez az entitás tartalmazza a sorszintű részleteket, amelyek a szerződés sor összegét adják ki. Ezek lehetnek olyan részletesek, mint a sorok, amelyeket a feladat szintjén a projekt ütemezése generál.
- **Szerződéses számla ütemezése** - Ez az entitás tartalmazza a számlázási ütemezést, amelyet a szerződéshez rendelt számlázási gyakoriság alapján állítanak elő.
- **Szerződés mérföldköve** - Ez az entitás a számlázási mérföldköveket tartalmazza azon szerződéses sorok számlázására, amelyek rögzített árú számlázási időtartammal rendelkeznek.

Egyéb elemek, amelyeket a PSA hozzáad a szerződésekhez, a következők: **Projektszerződés sor projekt árlista**, **Projektszerződés sor erőforrás kategória** és **Projektszerződés sor tranzakciós kategória**.

![Megrendelést, megredneléssort és projektkapcsolatokat mutató diagram](media/PS-Reporting-image3.png "Megrendelést, megredneléssort és projektkapcsolatokat mutató diagram")

## <a name="reporting-on-projects"></a>Jelentés a projektekről

A **Projekt** entitás és az ahhoz kapcsolódó entitás kizárólag a PSA számára tartozik. A **Projekt** a felső szintű entitás hogy használják, hogy elfog a munka és a költségek oldalán műveleteket. Itt található a kapcsolódó entitások listája:

- **Projektcsoport tagja** - Ez az entitás részleteket tartalmaz a projekthez rendelt foglalható forrásokról. Ezek az erőforrások lehetnek általános megrendelhető források, vagy elnevezhetők megrendelhető forrásoknak, amelyeket vagy a projektmenedzser ad meg, vagy a projekt ütemezéséből állítanak elő.
- **Projektfeladat** - Ez az entitás azokat a feladatokat tartalmazza, amelyek képezik a projekt tervet vagy ütemtervet.
- **Erőforrás-hozzárendelés** - Ez az entitás a foglalható erőforrás feladat-hozzárendelését tartalmazza.
- **Erőforrásigény** - Ez az entitás tartalmazza az általános erőforráscsoport tagjaira vonatkozó követelményeket.
- **Becslés** és **Becslés sor** - Ezeknek az entitásoknak fejléc/sor kapcsolata van, és tartalmazzák a projekt költségbecsléseit. A feladatbecsléseket az **Erőforrás becslés** entitás tárolja.

![Erőforrás-szükségletet és projektkapcsolatokat mutató diagram](media/PS-Reporting-image4.png "Erőforrás-szükségletet és projektkapcsolatokat mutató diagram")

## <a name="reporting-on-resources"></a>Jelentés az erőforrásokról

A projekt erőforrásai a Universal Resource Scheduling (URS) **Foglalható erőforrás** entitásokat használják, amelyeket megosztanak más alkalmazásokkal, például a Microsoft Dynamics 365 Field Service alkalmazással. Az alábbiakban felsoroljuk azokat az entitásokat, amelyeket esetleg használnia kell, amikor jelentést készít a projekt erőforrásairól:

- **Foglalható erőforrás-jellemzők** - ez az elem képviseli a projekt csapatban használt felhasználót, kapcsolatot, általános erőforrást, csoportot vagy használt berendezéseket.
- **Foglalható erőforrás-jellemzők** - Ez az entitás tartalmazza az erőforrás készségeit, igazolásait vagy oktatását. A jellemzőknek lehetnek olyan minősítési értékei, amelyeket a minősítési modell határoz meg.
- **Foglalható erőforrás-kategória** - Ez az entitás képviseli a foglalható erőforrás szerepét.
- **Foglalható erőforrás-foglalások** - Ez az entitás azt az időtartamot jelöli, amelyet a forrásokra a projekteknél lefoglalnak. Mindegyik foglalásnak van fejléces entitása és vonal entitásai is, és minden sornak egy olyan státusza van, amely a foglalás státusát jelzi.

![Foglalható erőforrás-jellemzők kapcsolatait mutató diagram](media/PS-Reporting-image5.png "Foglalható erőforrás-jellemzők kapcsolatait mutató diagram")

## <a name="reporting-on-actual-transactions"></a>Jelentés a tényleges tranzakciókról

Ha jóváhagy egy munkaidőt vagy költséget, vagy kiszámláz egy szerződést a PSA-ban, akkor az üzleti tranzakciót rögzíti az **Tényleges** entitás. Ez az entitás alapjául szolgálhat a PSA-ban szinte valamennyi pénzügyi vonatkozású jelentéshez. A **Tényleges** entitás rögzíti az üzleti esemény költségeit és értékesítési tranzakcióit. Ezenkívül számos releváns tulajdonságot rögzít.

Amikor a **Tényleges** entitással dolgozik, fontos, hogy megértse, mely tranzakciókat vagy tranzakciókat rögzítik az entitásban, és mikor rögzítik a tranzakciókat. Itt van a tipikus folyamat, amikor időbeírásokkal dolgozik (a költségek bejegyzésének folyamata hasonló):

1. Az időbejegyzés mentésekor a **Tényleges** entitás nem hoz létre rekordokat.
2. Az időbejegyzés benyújtásakor a **Tényleges** entitás nem hoz létre rekordokat.
3. Az időbejegyzés jóváhagyása után létrejön egy rekord a **Tényleges** entitásban, és egy második rekord is létrehozható. Az első rekord az időbejegyzés költségeit tárolja. A második rekord az időbejegyzés nem értékesített mennyiségét tárolja. A második rekord attól függ, hogy a projekt rendelkezik-e vevővel, árajánlattal vagy szerződéses sorral.

    | Dokumentum kelte | Tranzakció típusa | Tranzakcióosztály | Ügyfél         | Szerződés   | Erőforrás     | Erőforrás szerepköre | Számlázás típusa | Mennyiség | Egységár | Összeg |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Költség             | Time              | Alpesi síház | Alpesi CRM | Ashley Chinn | Projekt Mgr   | Felszámítható   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Számlázatlan értékesítés   | Time              | Alpesi síház | Alpesi CRM | Ashley Chinn | Projekt Mgr   | Felszámítható   | 8.0      | 100.00     | 800.00 |

    Ez a két rekord különálló, de kapcsolódó rekordok. Ezek sem terhelések, sem jóváírások.

4. Ha a projekthez egy szerződés kapcsolódik, akkor az időbejegyzés kiszámlázásakor további két rekord jön létre a **Tényleges** entitásban. Először negatív összeget hoznak létre a nem működő értékesítési rekordért. Ez a rekord lényegében megfordítja a nem értékesített eladásokat. Másodszor, létrejön egy tranzakció a számlázott eladáshoz. Ezek a nyilvántartások ismét különálló, de kapcsolódó nyilvántartások, nem terhelések és jóváírások.

    | Dokumentum kelte | Tranzakció típusa | Tranzakcióosztály | Ügyfél         | Szerződés   | Erőforrás     | Erőforrás szerepköre | Számlázás típusa | Mennyiség | Egységár | Összeg   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Számlázatlan értékesítés   | Time              | Alpesi síház | Alpesi CRM | Ashley Chinn | Projekt Mgr   | Felszámítható   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Számlázott értékesítés     | Time              | Alpesi síház | Alpesi CRM | Ashley Chinn | Projekt Mgr   | Felszámítható   | 8.0      | 100.00     | 800.00   |

A **Tranzakció eredete** entitás rögzíti a **Tényleges** rekord eredetét, és a **Tranzakciós kapcsolat** entitás rögzíti a kapcsolódó nyilvántartásokat a **Tényleges** rekordhoz. Ezenkívül a **Tényleges** referenciák tartalmazzák a projektet, a projekt szerződést (megrendelés), a megrendelhető forrást és az ügyfelet.

![Tranzakciós kapcsolatot, eredetet és tényleges kapcsolatokat mutató diagram](media/PS-Reporting-image6.png "Tranzakciós kapcsolatot, eredetet és tényleges kapcsolatokat mutató diagram")
