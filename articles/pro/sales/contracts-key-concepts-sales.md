---
title: A projektszerződések fő fogalmai – Lite
description: Ez a témakör a projektszerződések fő fogalmaival kapcsolatos információkat tartalmaz.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3381707457ef35ff604c716592afd8382b98ad5d
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643041"
---
# <a name="project-contracts---key-concepts---lite"></a>A projektszerződések fő fogalmai – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ez a témakör bemutatja a legfontosabb fogalmakat, amelyeket ismernie kell a Dynamics 365 Project Operations projektszerződéseinek használata előtt:

## <a name="contracting-unit"></a>Szerződő részleg

A szerződő részleg a projekt teljesítését birtokló részleget vagy gyakorlatot jelöli. Az egyes szerződő részlegekre vonatkozóan beállíthat erőforrásköltségeket. Ha egy erőforrás erőforrásköltséget ad meg egy erőforráshoz, akkor az erőforrásokhoz különböző költségárakat is beállíthat. Ez a szerződő egység ezeket az erőforrásokat a vállalaton belüli egyéb divízióból vagy gyakorlatból kölcsönözi. Ezek az erőforrásokhoz tartozó költségárak transzferárakként, erőforrás-kölcsönzésként vagy átváltási árakként hivatkozunk. Amikor beállítja az önköltségi árakat, hogy más részlegekből kölcsönözzenek erőforrásokat a kölcsönadó részleg pénznemét használja.

## <a name="cost-currency"></a>Költség pénzneme

A költség pénzneme az a pénznem, amelyben a költségeket jelentik képernyőn. Ez a pénznem a szerződés és a projekt **Szerződő részleg** mezőjéhez kapcsolt pénznemből származik. A költségek bármilyen pénznemben naplózhatók a projektben. Történik azonban pénznemváltás a pénznemről, amelyben a költségek rögzítve lettek, a projekt költségeinek pénznemére, amikor megjelenik a képernyőn.

A Common Data Service CDS-platform átváltási árfolyamai miatt nem lehet naprakész, a képernyőn megjelenő végösszegek idővel változhatnak, ha pénznem átváltási árfolyama frissül. Az adatbázisban rögzített költségek azonban változatlanok maradnak, mert az összegeket abban a pénznemben tárolják, amelyben felmerültek.

## <a name="sales-currency"></a>Értékesítési pénznem

A Project Operations értékesítési pénzneme az a pénznem, amelyben a becsült és a tényleges értékesítési összeget rögzítik, és megjelenítik. Az értékesítés pénzneme egyúttal az a pénznem, amelyben az ügyfél az üzletkötésre vonatkozó számlát kapja. A projektszerződésben az értékesítési pénznem alapértelmezés szerint az ügyfél- vagy a partnerrekordból veszi az alapértelmezett értékét, és a szerződés létrehozásakor módosítható. Amikor a szerződés létrehozása egy ajánlat lezártként való lezárásával történik, a szerződés pénzneme alapértelmezés szerint az ajánlat pénzneme lesz.

Ha a projektszerződést a semmiből hozza létre, az **Értékesítési pénznem** mezője nem szerkeszthető. A termékek és a projektek árlistája a szerződés ezen pénznemét veszi fel alapértelmezett értékként.

A költségekkel ellentétben az értékesítési értékeket csak az értékesítési pénznemben lehet nyilvántartani.

## <a name="billing-method"></a>Számlázási mód

A projektek esetében általánosságban két szerződési mód használatos: rögzített díj- és fogyasztásalapú. Ezek a modellek két lehetséges értékkel rendelkező számlázási módszerként jelennek meg a Project Operations alkalmazásban:

- Idő és anyag: Egy fogyasztásalapú szerződési modell, ahol minden felmerült költséget a megfelelő bevétellel kell alátámasztani. A további költségek megbecslése vagy felmerülése során a megfelelő becsült és tényleges értékesítés is növekedni fog. Határozzon meg nem túlléphető korlátozásokat azon szerződéssorok esetében, amelyek ezt a számlázási módszert tartalmazzák a tényleges bevétel realizálásához. A becsült bevételt nem érintik a nem meghaladandó korlátok.
- Rögzített ár: A rögzített díjazású szerződési modell, amely jelzi, hogy az értékesítési értékek függetlenek a felmerült költségektől. Az értékesítési érték rögzített, és további költségek becslésével vagy felmerülésével.

## <a name="project-price-lists"></a>Projektárlisták

A projektárlisták az idő, kiadások és egyéb projekttel kapcsolatos összetevők alapértelmezett áraihoz és nem költségeihez kerülnek felhasználásra. Több árlista is lehet. Minden árlista saját hatályossági dátummal rendelkezik az egyes projektszerződésekhez. A Project Operations nem támogatja az átfedésben lévő dátumérvényességet a projektárlistákon.

Ha a projektszerződés egy projektajánlat megnyerésével jön létre, a projekt-árlisták a szerződés nevével és a benne szereplő dátummal lesznek másolva. Az adatok másolása a Project-szerződésben szereplő projekt-összetevők egyéni árazását jelenti.

## <a name="product-price-lists"></a>Termékárlisták

A termékárlisták a szerződés termékalapú sorainak alapértelmezett áraihoz kerülnek felhasználásra, és nem a költségarányukhoz. Szerződésenként csak egy termékárlista lehetséges.

## <a name="transaction-classes"></a>Tranzakciós osztályok

A Project Operations négyféle típusú tranzakciót támogat:

- Időpont
- Költség
- Anyag
- Díj

A költség és értékesítés értékei megbecsülhetők, és felszámíthatók az Idő, Kiadás és Anyag tranzakcióosztályokban. A díj csak bevételi tranzakcióosztály.

## <a name="work-entities-and-billing-entities"></a>Munkaentitások és Számlázási entitások

A munkát képviselő entitások a projektek és feladatok. A számlázási aspektusokat képviselő entitások a szerződéssorok. A számlázási beállításokhoz különböző munkaentitások csatolhatók a szerződéssorok hozzárendelésével.

## <a name="multi-customer-deals"></a>Több ügyfél közötti üzletek

A több ügyfél közötti üzletek esetében ha több ügyfélnek kell számlázni. Néhány általános példa:

- Az OEM-vállalkozások és partnereik: A partnerek és a viszonteladók bizonyos hozzáadott értéket képviselő szolgáltatásokkal értékesítik a termékeket, jellemzően egy ügyfélhez tartozó konkrét üzlettel. Az OEM a projekt egy részét finanszírozza. 

- A közszféra projektjei: Egy helyi önkormányzat több osztálya vállalja a projekt finanszírozását, és egy korábban megállapodott felosztás szerint kerülnek számlázásra. Például egy iskolai körzet és a helyi önkormányzat egy osztálya vállalja, hogy egy uszoda épületét finanszírozza.

## <a name="invoice-schedules"></a>Számlaütemezések

A számlázási ütemezések az egyes szerződéssorokra vonatkoznak, és az automatikus számlázáshoz szükségesek. A számlázási ütemezések bizonyos kezdő és befejező dátumok és a számlázási gyakoriság alapján jönnek létre. Az ütemezés a szerződés fázisában történik, amikor az automatikus számlalétrehozási folyamat konfigurálásra kerül. Amikor egy árajánlatból egy szerződés kerül létrehozásra, a számlázási ütemezést a rendszer az ajánlatból másolja át.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>A Dynamics 365 Sales szerződésének változásai

A Project Operations árajánlatai a Dynamics 365 Sales szerződéseire épülnek. Vannak azonban olyan fontos eltérések a funkciókban, amelyekkel tisztában kell lennie:

- A Project Operations szerződések két különböző típusú sorral rendelkeznek, egy a projektekhez és egy a termékekhez.
- A Project Operations szerződések magukban foglalják saját űrlap- és a felhasználói felület elemeiket, az üzleti szabályokat, az üzleti logikát a beépülő modulokban és az ügyféloldali parancsfájlokat, amelyek megkülönbözteti őket a Sales szerződéseitől.

A fenti okok miatt nem szabad a Sales szerződéseket és a Projekt szerződéseket felcserélhető módon használni.
