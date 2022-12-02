---
title: Fejléc részletei szállítói számlákhoz
description: Ez a cikk a Microsoft Dynamics 365 Project Operations szállítói számlafejlécében biztosított szolgáltatást ismerteti.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261658"
---
# <a name="header-details-for-vendor-invoices"></a>Fejléc részletei szállítói számlákhoz

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a Microsoft Dynamics 365 Project Operations szállítói számlafejlécében biztosított szolgáltatást ismerteti.

Ahogy a projektmenedzser tervezi és végrehajtja a projekteket alvállalkozókat alkalmazhat, valamint termékeket és szolgáltatásokat vásárolhat a szállítóktól. A projekt végrehajtása során a költségek olyan szolgáltatásokból, anyagokból és költségkategóriákból merülnek fel, amelyek beszállítókat tartalmazó alvállalkozói szerződések alapján vannak beszerezve. A szállítók a szállítói számlák létrehozásával számlázzák ezeket a költségeket a projektekhez.

Az alábbi táblázat ismerteti a Project Operations számlafejléceiben található mezőket.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve. | Minden szállítói számla legördülő listán a szállítói számla neve szerepel az első oszlopban, amely segít azonosítani a szállítói számlát. Alapértelmezés szerint ha egy alvállalkozói szerződésből beszállítói számla jön létre, a szállítói számla **Név** mezője az alvállalkozó nevéből és az aktuális dátumból álló értékre van állítva. |
| Description | Az alvállalkozói számlán számlázott szolgáltatások és termékek rövid leírása. | None |
| Beszállító | Annak a vállalatnak a neve, amely a termékeket és szolgáltatásokat számlázza. Ez a vállalat egy olyan partnerrekord kell legyen amely **Szállító** vagy a **Beszállító** kapcsolattípussal rendelkezik. | <p>A kijelölt szállítótól függően a rendszer automatikusan beírt alapértelmezett értékeket a következő mezőkben:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul> |
| Alvállalkozói szerződés | Hivatkozás az szállítói számlája alvállalkozói szerződésére. | <p>A kijelölt alvállalkozói függően a rendszer automatikusan beírt alapértelmezett értékeket a következő mezőkbe:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul><p>A szállítói számlafejlécen kijelölt alvállalkozói szerződés alapértelmezés szerint meg van adva a szállítói számlasorokba, és az itt nem módosítható.</p> |
| Számla dátuma | A költség tényadatainak a szállítói számla megerősítéskor létrehozott dátuma. | A számla dátuma a megfelelő beszerzési árlista kiválasztására is használatos a kapcsolódó szállítóhoz csatolt árlistákból vagy a projektparaméterekből. |
| Állapot oka | A szállítói számla állapota. | <p>Az állapot meghatározza, hogy a szállítói számla hol van az üzleti folyamatban, és hogy szerkeszthető-e. Itt található néhány elérhető érték:</p><ul><li>**Vázlat**: A szállítói számla szerkeszthető.</li><li>**Megerősítve** – A szállító számláját ellenőrizve lett meg lett erősítve. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők vagy törölhetők.</li><li>**Folyamatban** – A szállító számlájának áttekintése folyamatban van. Az ebben az állapotban lévő szállítói számlák szerkeszthetők, de nem törölhetők.</li><li>**Visszavonva** – A szállító számláját visszavonták. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők vagy törölhetők.</li></ul> |
| Pénznem | Az a pénznem, amelyben a szállító számlázza a szállító számláján szereplő termékeket és szolgáltatásokat. | Egy alvállalkozói szerződésre hivatkozó szállítói számlán az alvállalkozói szerződés pénzneme alapértelmezés szerint a szállítói számla pénznemeként van megadva. Egy alvállalkozóra nem hivatkozó szállítói számlán az alapértelmezett érték a szállítói számla rekordjából lesz megadva, és módosítható. A szállítói számla mentése után a pénznem a továbbiakban nem szerkeszthető. |
| Szerződő részleg | A vállalat divíziója, amely a szolgáltatások és/vagy termékek szállítótól való fogadásáért felelős. | None |
| Fizetési feltételek | A kiadott szállítói számlák fizetési feltételei. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | A rendszer az alvállalkozói szerződés fizetési feltételeit az alvállalkozói szerződéssel kapcsolatos összes szállítói számlára másolja. A fizetési feltételek frissíthetők, ha az alvállalkozói szerződés **Vázlat** állapotú. |
| Fizetési cím | Annak a szállítónak a címe, akinek a kifizetéseket küldeni kell. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | A rendszer egy alvállalkozói szerződés kifizetési címét kifizetési címként másolja át az alvállalkozói szerződéshez létrehozott minden szállítói számlára. A kifizetési cím frissíthető, ha az alvállalkozói számla **Vázlat** állapotú. |
| Részösszeg | Ha egy szállítói számlának nincsenek sorai, adja meg a számla részösszegét az adók előtt. Ha a szállítói számla sorokkal rendelkezik, ez a mező csak olvasható. Ebben az esetben megjelenő összeg az szállítói számla összes sorából származó részösszeg. | None |
| Összes adó | Ha egy szállítói számlának nincsenek sorai, adja meg az alvállalkozói szerződés összes adóját. Ha a szállítói számla sorokkal rendelkezik, ez a mező csak olvasható. Ebben az esetben az adóösszegeknél megjelenő összeg az szállítói számla összes sorából származó részösszeg. | None |
| Végösszeg | Ez a számított mező a szállítói számla teljes összegét mutatja az adók figyelembevétele után. | None |

> [!NOTE]
> A szállítói számla alábbi mezői nem módosíthatók a szállítói számla mentése után: **Szállító**, **Alvállalkozói szerződés**, **Pénznem**, **Szerződő egység** és **Fizetési feltételek**. Ha ezeknek a mezőknek a módosításai szükségesek egy szállítói számlán, akkor törölnie kell a szállító számláját, és létre kell hoznia egy új szállítói számlát.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
