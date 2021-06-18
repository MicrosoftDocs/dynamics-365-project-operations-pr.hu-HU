---
title: Árajánlatok fő fogalmai - Lite
description: Ez a témakör a projektárajánlatok Project Operationsben való használatáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bd225bfea6e04839b57dfcc9436315fe1cd6a204
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994275"
---
# <a name="concepts-unique-to-project-quotes"></a>A csak Projektárajánlatokra jellemző fogalmak

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A következők a legfontosabb fogalmak, amelyeket ismernie kell a Dynamics 365 Project Operations projektajánlatainak használata előtt:

## <a name="contracting-unit"></a>Szerződő részleg

A szerződő részleg a projekt teljesítését birtokló részleget vagy gyakorlatot jelöli. Az egyes szerződő részlegekre vonatkozóan beállíthat erőforrásköltségeket. Ha a szerződő részleg erőforrásához ad meg erőforrás-költséget, akkor külön költségarányokat is beállíthat a szerződő részleg által kölcsönvett erőforrásokhoz vagy a vállalaton belüli más részlegekhez vagy gyakorlatokhoz. Ezekre transzferárakként, erőforrás-kölcsönzésként vagy átváltási árakként hivatkozunk. Ha egy másik részlegből kíván erőforrásokat kölcsönözni, akkor választhatja, hogy a kölcsönadó részleg pénznemében állítja be a költségarányokat.

## <a name="cost-currency"></a>Költség pénzneme

A költség pénzneme a Project Operationsben az a pénznem, amelyben a költségeket jelentik. Ez a pénznem az árajánlat, a szerződés és a projekt **Szerződő részleg** mezőjéhez kapcsolt pénznemből származik. A költségek bármilyen pénznemben naplózhatók a projektben. Történik azonban pénznemváltás a pénznemről, amelyben a költségek rögzítve lettek, a projekt költségeinek pénznemére.

A CDS-platform átváltási árfolyamai miatt nem lehet naprakész, a képernyőn megjelenő végösszegek idővel változhatnak, ha pénznem átváltási árfolyama frissül. Az adatbázisban rögzített költségek azonban változatlanok maradnak, mert az összegeket abban a pénznemben tárolják, amelyben felmerültek.

## <a name="sales-currency"></a>Értékesítés pénzneme

A Project Operations értékesítési pénzneme az a pénznem, amelyben a becsült és a tényleges értékesítési összeget rögzítik, és megjelenítik. Ez egyúttal az a pénznem, amelyben az ügyfél az üzletkötésre vonatkozó számlát kapja. A projektárajánlatában az értékesítési pénznem alapértelmezés szerint az ügyfél- vagy a partnerrekordból veszi az alapértelmezett értékét, és az árajánlat létrehozásakor módosítható. Az árajánlat mentése után az értékesítési pénznem nem módosítható. A termékek és a projektek árlistája az árajánlat értékesítési pénznemét veszi fel alapértelmezett értékként.

A költségekkel ellentétben az értékesítési értékeket csak az értékesítési pénznemben lehet nyilvántartani.

## <a name="billing-method"></a>Számlázási mód

A projektek általában rögzített díj- és fogyasztásalapú szerződési modellekkel rendelkeznek. Ez a Project Operationsben **Számlázási mód** néven jelenik meg, és két értékkel rendelkezik, idő és anyag, valamint rögzített ár.

- **Idő és anyag:** Ez egy fogyasztásalapú szerződési modell, ahol minden felmerült költséget a megfelelő bevétellel kell alátámasztani. A további költségek megbecslése vagy felmerülése során a megfelelő becsült és tényleges értékesítés is növekedni fog. A számlázási módszert használó árajánlatsorokon nem meghaladandó korlátokat adhat meg. Ez korlátozni fogja a tényleges bevételt. A becsült bevételt nem érintik a nem meghaladandó korlátok.
- **Rögzített ár:** Ez egy rögzített díjazású szerződési modell, amely jelzi, hogy az értékesítési értékek függetlenek a felmerült költségektől. Az értékesítési érték rögzített, és további költségek becslésével vagy felmerülésével.

## <a name="project-price-lists"></a>Projektárlisták

A projektárlisták azok az árlisták, amelyek az idő, kiadások és egyéb projekttel kapcsolatos összetevők alapértelmezett áraihoz és nem költségeihez kerülnek felhasználásra. Több árlista is lehet, és mindegyik lista rendelkezhet saját dátumérvényességgel az egyes projektárajánlatokhoz. A Project Operations nem támogatja az átfedésben lévő dátumérvényességet a projektárlistákon.

## <a name="product-price-lists"></a>Termékárlista

A termékárlisták azok az árlisták, amelyek az árajánlat termékalapú sorainak alapértelmezett áraihoz kerülnek felhasználásra, és nem a költségarányukhoz. Árajánlatonként csak egy termékárlista lehetséges.

## <a name="transaction-classes"></a>Tranzakció osztályai

A Project Operations négyféle típusú tranzakciót támogat:

- Időpont
- Költség
- Anyag
- Díj

A költség és értékesítés értékei megbecsülhetők, és felszámíthatók az Idő, Kiadás és Anyag tranzakcióosztályokban. A díj csak bevétel tranzakcióosztály.

## <a name="work-entities-and-billing-entities"></a>Munkaentitások és számlázási entitások

A munkát képviselő entitások a projektek és feladatok. A számlázást képviselő entitások az árajánlatsorok és a szerződéssorok. A számlázási beállításokhoz különböző munkaentitások csatolhatók árajánlat- vagy szerződéssorok hozzárendelésével.

## <a name="multi-customer-deals"></a>Több ügyfél közötti üzletek

A több ügyfél közötti üzletek akkor merülnek fel, ha több ügyfélnek kell számlázni. A gyakori példák közé tartoznak a következők:

- **OEM-vállalatok és partnereik:** A partnerek és a viszonteladók a hozzáadott értékű szolgáltatásokkal értékesítik a termékeket. Ez általában olyan eset, amikor egy ügyféllel folytatott adott ügylet során az OEM felajánlja a projekt egy részének finanszírozását. 

- **A közszféra projektjei:** Egy helyi önkormányzat több osztálya vállalja a projekt finanszírozását, és egy korábban megállapodott felosztás szerint kerülnek számlázásra. Például egy iskolai körzet és a város vagy a helyi önkormányzat egy osztálya vállalja, hogy egy uszoda épületét finanszírozza.

## <a name="invoice-schedules"></a>Számlaütemezések

A számlázási ütemezések az egyes árajánlatsorokra jellemzőek, és szintén nem kötelezőek. A számlázási ütemezések bizonyos kezdő és befejező dátumok és a számlázási gyakoriság alapján jönnek létre. A számlák ütemezése a szerződés fázisában történik, amikor az automatikus számlalétrehozási folyamat konfigurálásra kerül. Az árajánlati fázisban az ütemezések nem kötelezőek. Ha az **Árajánlat** fázisában a számlázási ütemezések jönnek létre, akkor a program a projektárajánlat megnyerése után létrejövő projektszerződésbe másolja azokat.

## <a name="changes-from-dynamics-365-sales-quote"></a>A Dynamics 365 Sales árajánlat változásai:

A Project Operations árajánlatai a Dynamics 365 Sales árajánlataira épülnek. Vannak azonban olyan fontos eltérések a funkciókban, amelyekkel tisztában kell lennie:

- Az **Áttekintés** és **Aktiválás** műveletek nem támogatottak.
- A Project Operations árajánlatai két különböző típusú sorral rendelkeznek. Az egyik a projektek számára, a másik pedig a termékek számára.
- A Project Operations árajánlatok magukban foglalják saját űrlap- és a felhasználói felület elemeiket, az üzleti szabályokat, az üzleti logikát a beépülő modulokban és az ügyféloldali parancsfájlokat, amelyek megkülönbözteti őket a Sales árajánlataitól.

A fenti okok miatt nem ajánlott a Sales árajánlatot és a Project Operations árajánlatot egymás helyett használni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
