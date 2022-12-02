---
title: Árajánlatok és árajánlatsorok
description: Ez a cikk az árajánlatkról és az áranjánlatsorokról tartalmaz információkat.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 4c59f018adc7ee439fd77a819e2fb7620941e958
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933357"
---
# <a name="quotes-and-quote-lines"></a>Árajánlatok és árajánlatsorok

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation rendszerben kétféle árajánlat létezik: projektárajánlat és értékesítési árajánlat. A két típus a következőkben különbözik:

- Az értékesítési árajánlatban csak egy rács szerepelhet a sorokban. A projektárajánlatában a sorokhoz két rács tartozik: egy a projektsorokhoz és egy a termékcsaládokhoz.
- Az értékesítési árajánlat támogatja az aktiválást és a módosításokat. A projektárajánlat nem támogatja ezeket a folyamatokat.
- Az értékesítési árajánlathoz több megrendelés is csatolható. Egy projektárajánlathoz csak egy projektszerződés csatolható.
- Megszerezheti az értékesítési árajánlatot, és megtarthatja a kapcsolódó lehetőséget. A projekt árajánlatának megszerzése után a kapcsolódó lehetőség le lesz zárva.
- Az értékesítési árajánlat nem tartalmaz bizonyos olyan mezőket és fogalmakat, amelyek szerepelnek a projektárajánlatban. A mezők közé tartozik a **Szerződő részleg**, a **Partnerkezelő** és a **Számlázási kapcsolattartó neve**.  
- Az értékesítési árajánlatokat és a projektárajánlatokat egy értékkészlet-alapú **Típus** nevű mező is azonosítja. Értékesítési árajánlat esetén ebben a mezőben az érték **elemalapú**. A projektárajánlat esetén az érték **Munkaalapú**.

Ez a cikk a projektárajánlat részletes adatait veszi figyelembe.

A PSA-ban lévő projektárajánlat több sorral vagy ajánlati sorral is rendelkezhet. A projektárajánlat két rácsot tartalmaz a sorokhoz. Az egyik rács a projektalapú sorokhoz használható, amelyek lehetővé teszik a részletes becslést. A másik rács az egyszerű egységárat és a mennyiségi alapú megközelítést használó termékalapú sorokhoz tartozik.

- **Projektalapú** – az összeget (megajánlott érték) a rendszer a munka mennyiségének megbecslése után határozza meg. Magas szinten is megbecsülheti a munkát, vagy közvetlenül megbecsülheti az egyes árajánlati sorok alatti sorrészletekként. Végül projekt és projektterv segítségével megbecsülheti az előirányzott becslések alapján végzett munkát. A projektalapú árajánlatsorok csak a Project Service Automation használatával létrehozott, projektalapú árajánlatokban találhatók. Az ilyen típusú árajánlatsor a Microsoft Dynamics 365 Sales-ben elérhető, nem katalogizált árajánlatsorok testreszabott formája.
- **Termékalapú** – az összeg (megajánlott érték) az eladott egységek mennyisége és a termék értékesítési ára alapján kerül meghatározásra. A termékalapú sor terméke származhat a Sales termékkatalógusából, vagy lehet olyan termék, amelyet Ön határoz meg. Az ilyen típusú árajánlatsor a PSA használatával létrehozott, projektalapú árajánlatokon is elérhető.

Az árajánlatban szereplő összeg a termékalapú sorok és a projektalapú sorok teljes összege.

> [!NOTE]
> A PSA-ban nem kötelező árajánlatokat és árajánlatsorokat megadni. A projektfolyamat egy projektszerződéssel indítható (értékesített projekt). Lehetőségre azonban mindig szükség van függetlenül attól, hogy árajánlattal vagy projektszerződéssel kezd-e.

## <a name="project-based-quote-lines"></a>Projektalapú árajánlatsorok

A PSA projektalapú árajánlatsora a következő számlázási módszerekkel rendelkezik:

- Idő és anyag
- Rögzített ár

### <a name="time-and-material"></a>Idő és anyag

Az idő- és anyagelszámolású számlázási módszer a felhasználáson alapul. Ha ezt a számlázási módot választja, akkor a program a projektben felmerülő költségként számlázza az ügyfelet. A számlák dátumalapú, időszakos gyakorisággal jönnek létre. Az értékesítési folyamat során egy idő- és anyagelszámolású összetevő megajánlott értéke csak az ügyfélre vonatkozó végső költség becslését adja meg. Az eladó nem kötelezi magát arra, hogy pontosan az ajánlatban szereplő megajánlott értéken teljesítse a projektet. Az idő- és anyagelszámolású összetevők növelik az ügyfél kockázatát. Előfordulhat, hogy az ügyfelek a kockázat minimalizálása érdekében további nem meghaladható kikötéseket kívánnak elérni. A PSA nem támogatja a nem meghaladható kikötések beállítását.

### <a name="fixed-price"></a>Rögzített ár

A rögzített árú számlázási módszerben a szolgáltató kötelezettséget vállal arra, hogy a projektet rögzített költségen nyújtja az ügyfélnek. Az ügyfél kiszámlázza a rögzített árú árajánlatsor megadott értékét, függetlenül attól, hogy a szolgáltató milyen költségek mellett teljesíti az ajánlatsort. A rögzített árú árajánlatsor a következő módszerek egyike szerint kerül kiszámlázásra: 

- Átalányösszegként a projekt elején vagy végén, vagy egy mérföldkő elérésekor. 
- Az árajánlatsor rögzített értékei egyenlő részleteinek dátumalapú gyakorisága alapján. Ezek a részletek időszakos mérföldkőként ismertek.
- Azokban a részletekben, amelyek olyan pénzügyi értékkel rendelkeznek, amely összhangban van a projektben megvalósított munkavégzéssel vagy adott mérföldkövevel. Ebben az esetben az egyes részletfizetések értéke eltérő lehet, de az összeset fel kell venni az árajánlatsor rögzített értékéhez.

A PSA a rögzített árú árajánlatsorokra vonatkozóan mindhárom típusú számlát támogatja.

## <a name="transaction-classification"></a>Tranzakció besorolása

A professzionális szolgáltatást végző szervezetek általában a költségek besorolásával készítenek árajánlatot, és számlázzák az ügyfelet. A PSA-ban a költségeket a következő tranzakciós besorolások jelentik:

- **Idő** – ez az osztályozás a munka vagy a humánerőforrás idejének költségét jelenti a projektben.
- **Költség**: – ez az osztályozás jelenti a projekt minden egyéb költségét. Mivel a költségek széles körben csoportosíthatók, a legtöbb szervezet olyan alkategóriákat hoz létre, mint az utazás, az autókölcsönzés, a szállodai vagy az irodai eszközök.
- **Díj** – ez az osztályozás vegyesen vonatkozik a karbantartásra, a büntetésekre és egyéb elemekre, amelyeket az ügyfélnek kell állnia. 
- **Adó** – ez az osztályozás a felhasználók által a kiadások beírása során hozzáadott adó összegét jelenti.
- **Anyaggal kapcsolatos tranzakció** – ez az osztályozás a jóváhagyott projektszámlán lévő terméksorok tényleges értékét jelenti.
- **Mérföldkő** – ezt az osztályozást a rögzített árú számlázási logika használja a PSA-ban.

Ezen tranzakcióosztályok egyike vagy ezek közül több is társítható az egyes árajánlatsorokkal. Az árajánlat megszerzése után a tranzakcióosztályozás és az árajánlatsor közötti leképezés a szerződéssorhoz kerül.
 
> ![Képernyőkép a tranzakciótípusok árajánlatokra és szerződéssorokra való leképezéséről.](media/basic-guide-5.png)
  
Előfordulhat például, hogy egy árajánlat a következő két ajánlatsort tartalmazza: 
- Az idő- és anyagelszámolású számlázási módszert használó konzultációs munka, ahol alkalmazható az idő- és a díj tranzakcióosztálya. Például a **Dynamics AX-megvalósítással** kapcsolatos összes idő- és díjtranzakciót a rendszer az ügyfélnek számlázza a felhasznált idő és anyag alapján. 
- Rögzített árú számlázási módszert használó kapcsolódó utazási költségek. Például a **Dynamics AX-megvalósítás** példaprojekt összes utazási költségét rögzített pénzértéken számlázza a rendszer.

> [!NOTE]
> Az **Idő**, a **Költség** és a **Díj** projekt- és tranzakcióosztályozási kombinációjának, amelyek árajánlatsorral vagy szerződéssorral vannak társítva, egyedinek kell lennie. Ha a projekt- és tranzakcióosztály ugyanazon kombinációja egynél több szerződéssor vagy ajánlatsorhoz van társítva, akkor a PSA nem fog megfelelően működni.

## <a name="billing-types"></a>Számlázási típusok

A **Számlázási típus** mező határozza meg a PSA-ban a felszámíthatóság fogalmát. Ez egy értékkészlet, amelynek a következő lehetséges értékei vannak:

- **Felszámítható** – a szerepkör/kategória által elhatárolt költség egy közvetlen költség, amely a projektek végrehajtását eredményezi, és az ügyfél ezért a munkáért fizet. A kifizetést idő- és anyagelszámolású, illetve rögzített árú megállapodásként lehet kezelni. Az ezt az időt eltöltő alkalmazott azonban megkapja a megfelelő jóváírást a saját számlázható kihasználtságára vonatkozóan.
- **Nem felszámítható** – a szerepkör/kategória által elhatárolt költség egy közvetlen költség, amely a projektek végrehajtását eredményezi akkor is, ha az ügyfél ezt nem ismeri el, és nem fizet ezért a munkáért. Az ezt az időt eltöltő alkalmazott nem kapja meg a jóváírást a számlázható kihasználtságra vonatkozóan.
- **Kiegészítő** – a szerepkör/kategória által elhatárolt költség egy közvetlen költség, amely a projektek végrehajtását eredményezi, és az ügyfél ezt elismeri. Az ezt az időt eltöltő alkalmazott megkapja a jóváírást a számlázható kihasználtságra vonatkozóan. Ez a költség azonban nem lesz felszámítva az ügyfélnek.
- **Nem elérhető** – ezzel a beállítással a rendszer nyomon követi azokat a költségeket, amelyek a bevétel nyomon követését nem igénylő belső projektek során merültek fel.

## <a name="invoice-schedule"></a>Számla ütemezése

A számlaütemezés a projektek számlázásakor bekövetkezett dátumok sorozata. A számlaütemezést tetszés szerint létrehozhatja a PSA egy árajánlatsorában. Minden árajánlatsornak lehet saját számlaütemezése. A számlaütemezés létrehozásához meg kell adnia a következő attribútumértékeket:

- Számlázás kezdő dátuma 
- A projekt számlázásának befejezési dátumát jelentő szállítási dátum
- Számlázási gyakoriság

A PSA ezt a három attribútumértéket használja a számlázás beállításához a feltételes dátumok meghatározásához.

## <a name="invoice-frequency"></a>Számlázási gyakoriság

A számlázás gyakorisága olyan entitás, amely a számla létrehozásának gyakoriságát kifejező attribútumértékeket tárol. A következő attribútumok fejezik ki vagy definiálják a számla gyakorisága entitást:

- **Időszak** – a havi, kétheti és heti időszakok támogatottak. 
- **Futtatások időszakonként** – a heti és a kétheti időszakokra vonatkozóan időszakonként csak egy futtatást lehet meghatározni. A havi időszakok esetén az egy–négy futtatást határozhat meg időszakonként. 
- **Futtatás napjai** – a számlázás futtatásához szükséges napok. Ezt az attribútumot kétféleképpen konfigurálhatja:
  - **Hétköznapok** – megadhatja például, hogy a számlázás hétfőnként vagy minden második hétfőn fusson. A számlázás munkanapokon történő futtatását beállítani köteles ügyfelek ezt a fajta konfigurációt részesítik előnyben. 
  - **Naptári napok** – megadhatja például, hogy a számlázás minden hónap hetedik és huszonegyedik napján fusson. Előfordulhat, hogy néhány szervezet az ilyen típusú konfigurációt részesíti előnyben, mert ezzel biztosítható, hogy a számlázás havonta rögzített ütemezés szerint fusson.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Rögzített árú árajánlatsor számlázásának ütemezése

Rögzített árú árajánlatsor esetén a **Számla ütemezése** rács használatával hozhat létre számlázási mérföldkövet, amely megegyezik az árajánlatsor értékével.

- Az egyenlően eloosztott számlázási mérföldkövek létrehozásához válassza ki a számlázás gyakoriságát, írja be a számlázás kezdési dátumát az árajánlatsorba, és válassza a **Kért teljesítési dátumot** az árajánlatsor fejlécének **Összegzés** szakaszában. Ezután válassza az **Időszakos mérföldkövek létrehozása** lehetőséget a kiválasztott számlázási gyakoriság alapján egyformán elosztott mérföldkövek létrehozásához. 
- Ha átalányösszegű számlázási mérföldkövet szeretne létrehozni, hozzon létre egy mérföldkövet, majd adja meg az árajánlatsor értékét a mérföldkő összegeként.
- Ha a projektterv adott feladatain alapuló számlázási mérföldköveket szeretne létrehozni, hozzon létre mérföldkőet, és képezze le a projekt ütemezési elemére a számlázási mérföldkő felhasználó felületén.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
