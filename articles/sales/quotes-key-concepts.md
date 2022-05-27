---
title: Árajánlatok – alapfogalmak
description: Ez a témakör a Project Operations projektárajánlatairól és értékesítési árajánlatairól nyújt információt.
author: rumant
ms.date: 09/18/2020
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
ms.openlocfilehash: fbaed6a0967ce4ef4eec572de9e2a7da95c3cbd9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579915"
---
# <a name="concepts-unique-to-project-based-quotes"></a>A csak Projektalapú árajánlatokra jellemző fogalmak

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations rendszerben kétféle árajánlat létezik: projektárajánlat és értékesítési árajánlat. A két típusú árajánlat a következőkben különbözik:

- **Egyes sorelemekhez tartozó rácsok**: Az értékesítési árajánlatban csak egy rács szerepelhet a sorokban. A projektárajánlatokban két rács tartozik a sorelemekhez. Az egyik rács a projektek soraihoz, a másik pedig a termékek soraihoz használható.
- **Aktiválás és revíziók**: Az értékesítéi árajánlatok támogatják az aktiválást és a revíziókat. A projektárajánlatokban ezek a folyamatok nem támogatottak.
- **Csatolt megrendelések**: Az értékesítési árajánlatokhoz több megrendelés is csatolható. Egy projektárajánlathoz csak egy projektszerződés csatolható.
- **Árajánlat megnyerése** : Ha megnyer egy értékesítési árajánlatot, a kapcsolódó lehetőség nyitva maradhat. A projekt árajánlatának megszerzése után a kapcsolódó lehetőség le lesz zárva.
- **Mezők és fogalmak**: Az értékesítési árajánlat nem tartalmaz bizonyos olyan mezőket és fogalmakat, amelyek szerepelnek egy projektárajánlatban. A mezők közé tartozik a **Szerződő részleg**, a **Partnerkezelő** és a **Számlázási kapcsolattartó neve**.  
- **Típus**: Az értékesítési árajánlatokat és a projektárajánlatokat egy értékkészlet-alapú **Típus** mező is azonosítja. Értékesítési árajánlat esetén ebben a mezőben az érték **elemalapú**. A projektárajánlat esetén az érték **Munkaalapú**.

Ez a témakör a projektárajánlat részletes adataival foglalkozik.

A Project Operations projektárajánlata több sorelemmel vagy árajánlatsorral is rendelkezhet. A projektárajánlat két rácsot tartalmaz a sorokhoz. Az egyik rács a projektalapú sorokhoz használható, amelyek lehetővé teszik a részletes becslést. A másik rács az egyszerű egységárat és a mennyiségi alapú megközelítést használó termékalapú sorokhoz tartozik.

- **Projektalapú**: A megajánlott értéket a rendszer a szükséges munka mennyiségének megbecslése után határozza meg. A munkát megbecsülheti magas szinten, közvetlenül az árajánlat egyes sorai alatt lévő részletként, illetve előirányzott becslések alapján, projekt és projektterv segítségével. A projektalapú árajánlatsorok csak a Project Operations használatával létrehozott, projektalapú árajánlatokban találhatók. Az ilyen típusú árajánlatsor a Microsoft Dynamics 365 Sales-ben elérhető, nem katalogizált árajánlatsorok testreszabott formája.

- **Termékalapú**: A megajánlott értéket az eladott egységek mennyisége és a termék értékesítési ára alapján kerül határozza meg a rendszer. A termékalapú sor terméke származhat a Sales termékkatalógusából, vagy lehet olyan termék, amelyet Ön határoz meg. Az ilyen típusú árajánlatsor a Project Operations használatával létrehozott, projektalapú árajánlatokon is elérhető.

Az árajánlatban szereplő összeg a termékalapú sorok és a projektalapú sorok teljes összege.

> [!NOTE]
> A Project Operationsben nem kötelező árajánlatokat és árajánlatsorokat megadni. A projektfolyamat egy projektszerződéssel indítható (értékesített projekt). Lehetőségre azonban mindig szükség van függetlenül attól, hogy árajánlattal vagy projektszerződéssel kezd-e.

## <a name="project-based-quote-lines"></a>Projektalapú árajánlatsorok

A Project Operations projektalapú árajánlatsora a következő számlázási módszerekkel rendelkezik:

- Idő és anyag
- Rögzített ár

### <a name="time-and-material"></a>Idő és anyag

Az idő- és anyagelszámolású számlázási módszer a felhasználáson alapul. Ha ezt a számlázási módot választja, akkor a program a projektben felmerülő költségként számlázza az ügyfelet. A számlák dátumalapú, időszakos gyakorisággal jönnek létre. Az értékesítési folyamat során egy idő- és anyagelszámolású összetevő megajánlott értéke csak az ügyfélre vonatkozó végső költség becslését adja meg. Az eladó nem kötelezi magát arra, hogy pontosan az ajánlatban szereplő megajánlott értéken teljesítse a projektet. Az idő- és anyagelszámolású összetevők növelik az ügyfél kockázatát. Előfordulhat, hogy az ügyfelek a kockázat minimalizálása érdekében további nem meghaladható kikötéseket kívánnak elérni. A Project Operations nem támogatja a nem meghaladható kikötések beállítását.

### <a name="fixed-price"></a>Rögzített ár

A rögzített árú számlázási módszerben a szolgáltató kötelezettséget vállal arra, hogy a projektet rögzített költségen nyújtja az ügyfélnek. Az ügyfél kiszámlázza a rögzített árú árajánlatsor megadott értékét, függetlenül attól, hogy a szolgáltató milyen költségek mellett teljesíti az ajánlatsort. A rögzített árú árajánlatsor a következő módszerek egyike szerint kerül kiszámlázásra: 

- Átalányösszegként a projekt elején vagy végén, vagy egy mérföldkő elérésekor. 
- Az árajánlatsor rögzített értékei egyenlő részleteinek dátumalapú gyakorisága alapján. Ezek a részletek időszakos mérföldkőként ismertek.
- Azokban a részletekben, amelyek olyan pénzügyi értékkel rendelkeznek, amely összhangban van a projektben megvalósított munkavégzéssel vagy adott mérföldkövevel. Ebben az esetben az egyes részletfizetések értéke eltérő lehet, de az összeset fel kell venni az árajánlatsor rögzített értékéhez.

A Project Operations a rögzített árú árajánlatsorokra vonatkozóan mindhárom típusú számlát támogatja.

## <a name="transaction-classification"></a>Tranzakció besorolása

A professzionális szolgáltatást végző szervezetek általában a költségek besorolásával készítenek árajánlatot, és számlázzák az ügyfelet. A költségeket a következő tranzakciós besorolások jelölik:

- **Idő**: Ez a besorolás a munka vagy a humán erőforrás idejének költségét jelöli a projektben.
- **Költség**: Ez a besorolás a projekt további költségeit jelöli. Mivel a költségek széles körben csoportosíthatók, a legtöbb szervezet olyan alkategóriákat hoz létre, mint az utazás, az autókölcsönzés, a szállodai vagy az irodai eszközök.
- **Díj**: Ez a besorolás vegyesen jelöli a karbantartást, a büntetéseket és az olyan további elemeket, amelyeket az ügyfélnek kell állnia. 
- **Adó**: Ez a besorolás a felhasználók által a költségek megadása során hozzáadott adó összegét jelöli.
- **Anyaggal kapcsolatos tranzakció**: Ez a besorolás a jóváhagyott projektszámlán lévő terméksorok tényleges értékét jelöli.
- **Mérföldkő**: Ezt a besorolást a rögzített árú számlázási logika használja.

Ezen tranzakcióosztályok egyike vagy ezek közül több is társítható az egyes árajánlatsorokkal. Az árajánlat megszerzése után a tranzakcióosztályozás és az árajánlatsor közötti leképezés a szerződéssorhoz kerül.
  
Előfordulhat például, hogy egy árajánlat a következő két ajánlatsort tartalmazza: 

- Az idő- és anyagelszámolású számlázási módszert használó konzultációs munka, ahol alkalmazható az idő- és a díj tranzakcióosztálya. Például a **Dynamics AX-megvalósítással** kapcsolatos összes idő- és díjtranzakciót a rendszer az ügyfélnek számlázza a felhasznált idő és anyag alapján. 
- Rögzített árú számlázási módszert használó kapcsolódó utazási költségek. Például a **Dynamics AX-megvalósítás** példaprojekt összes utazási költségét rögzített pénzértéken számlázza a rendszer.

> [!NOTE]
> Az **Idő**, a **Költség** és a **Díj** projekt- és tranzakcióosztályozási kombinációjának, amelyek árajánlatsorral vagy szerződéssorral vannak társítva, egyedinek kell lennie. Ha a projekt- és tranzakcióosztály egy adott kombinációja több szerződéssorhoz vagy árajánlatsorhoz van társítva, akkor a Project Operations nem fog megfelelően működni.

## <a name="billing-types"></a>Számlázási típusok

A **Számlázási típus** mező határozza meg a felszámíthatóság fogalmát. Ez egy értékkészlet, amelynek a következő lehetséges értékei vannak:

- **Felszámítható**: A jelen szerepkör/kategória által felhalmozott költség olyan közvetlen költség, amely a projektek végrehajtását eredményezi, és az ügyfél ezért a munkáért fizet. A kifizetést idő- és anyagelszámolású, illetve rögzített árú megállapodásként lehet kezelni. Az ezt az időt eltöltő alkalmazott azonban megkapja a megfelelő jóváírást a saját számlázható kihasználtságára vonatkozóan.
- **Nem felszámítható**: A jelen szerepkör/kategória által felhalmozott költség olyan közvetlen költség, amely a projektek végrehajtását eredményezi akkor is, ha az ügyfél ezt nem ismeri el, és nem fizet ezért a munkáért. Az ezt az időt eltöltő alkalmazott nem kapja meg a jóváírást a számlázható kihasználtságra vonatkozóan.
- **Kiegészítő**: A jelen szerepkör/kategória által felhalmozott költség olyan közvetlen költség, amely a projektek végrehajtását eredményezi, és az ügyfél ezt elismeri. Az ezt az időt eltöltő alkalmazott megkapja a jóváírást a számlázható kihasználtságra vonatkozóan. Ez a költség azonban nem lesz felszámítva az ügyfélnek.
- **Nem elérhető**: Ezzel a beállítással a rendszer azokat a költségeket követi nyomon, amelyek a bevétel nyomon követését nem igénylő belső projektek során merültek fel.

## <a name="invoice-schedule"></a>Számla ütemezése

A számlaütemezés a projektek számlázásakor bekövetkezett dátumok sorozata. Számlaütemezést tetszés szerint létrehozhat egy árajánlatsorban. Minden árajánlatsornak lehet saját számlaütemezése. A számlaütemezés létrehozásához meg kell adnia a következő attribútumértékeket:

- Számlázás kezdő dátuma 
- A projekt számlázásának befejezési dátumát jelentő szállítási dátum
- Számlázási gyakoriság

A rendszer ezt a három attribútumértéket használja az olyan feltételes dátumok meghatározásához, amelyek alapján elvégzi a számlázást.

## <a name="invoice-frequency"></a>Számlázási gyakoriság

A számlázás gyakorisága olyan entitás, amely a számla létrehozásának gyakoriságát kifejező attribútumértékeket tárol. A következő attribútumok fejezik ki vagy definiálják a számla gyakorisága entitást:

- **Időszak**: A havi, a kétheti és a heti időszak támogatott. 
- **Futtatások időszakonként**: A heti és a kétheti időszakokra vonatkozóan időszakonként csak egy futtatást lehet meghatározni. A havi időszakok esetén az egy–négy futtatást határozhat meg időszakonként. 
- **Futtatás napjai**: A napok, amikor a számlázásnak futnia kell. Ezt az attribútumot kétféleképpen konfigurálhatja:
  - **Hétköznapok**: Megadhatja például, hogy a számlázás hétfőnként vagy minden második hétfőn fusson. A számlázás munkanapokon történő futtatását beállítani köteles ügyfelek ezt a fajta konfigurációt részesítik előnyben. 
  - **Naptári napok**: Megadhatja például, hogy a számlázás minden hónap hetedik és huszonegyedik napján fusson. Előfordulhat, hogy néhány szervezet az ilyen típusú konfigurációt részesíti előnyben, mert ezzel biztosítható, hogy a számlázás havonta rögzített ütemezés szerint fusson.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Rögzített árú árajánlatsor számlázásának ütemezése

Rögzített árú árajánlatsor esetén a **Számla ütemezése** rács használatával hozhat létre számlázási mérföldkövet, amely megegyezik az árajánlatsor értékével.

- Az egyenlően eloosztott számlázási mérföldkövek létrehozásához válassza ki a számlázás gyakoriságát, írja be a számlázás kezdési dátumát az árajánlatsorba, és válassza a **Kért teljesítési dátumot** az árajánlatsor fejlécének **Összegzés** szakaszában. Ezután válassza az **Időszakos mérföldkövek létrehozása** lehetőséget a kiválasztott számlázási gyakoriság alapján egyformán elosztott mérföldkövek létrehozásához. 
- Ha átalányösszegű számlázási mérföldkövet szeretne létrehozni, hozzon létre egy mérföldkövet, majd adja meg az árajánlatsor értékét a mérföldkő összegeként.
- Ha a projektterv adott feladatain alapuló számlázási mérföldköveket szeretne létrehozni, hozzon létre mérföldkőet, és képezze le a projekt ütemezési elemére a számlázási mérföldkő felhasználó felületén.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
