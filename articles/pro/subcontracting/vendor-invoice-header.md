---
title: Fejléc részletei szállítói számlákhoz
description: Ez a cikk a Microsoft szállítói számla fejlécében található funkciókat ismerteti Dynamics 365 Project Operations.
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

Ez a cikk a Microsoft szállítói számla fejlécében található funkciókat ismerteti Dynamics 365 Project Operations.

Miközben a projektmenedzserek projekteket terveznek és hajtanak végre, alvállalkozókat alkalmazhatnak, és termékeket és szolgáltatásokat vásárolhatnak a szállítóktól. A projekt végrehajtása során a költségek olyan szolgáltatásokból, anyagokból és költségkategóriákból származnak, amelyeket a szállítókkal kötött alvállalkozói szerződések alapján szereznek be. A szállítók ezeket a költségeket szállítói számlák létrehozásával számlázzák ki a projekteknek.

Az alábbi táblázat a Szállítói számlafejlécek mezőiről nyújt tájékoztatást a Project Operations alkalmazásban.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve. | Az összes szállítói számla legördülő listában a szállítói számla neve az első oszlopban jelenik meg, hogy segítsen azonosítani a szállítói számlát. Alapértelmezés szerint, ha egy szállítói számlát alvállalkozói szerződésből hoznak létre, a **szállítói számla Név** mezőjét olyan értékre állítja be, amely az alvállalkozó neve és az aktuális dátum alapján van beállítva. |
| Description | A szállítói számlán kiszámlázott szolgáltatások és termékek rövid leírása. | None |
| Beszállító | Annak a vállalatnak a neve, amely a termékekért és szolgáltatásokért számlázik. Ennek a vállalatnak olyan számlarekordnak kell lennie, amelynek kapcsolattípusa **Szállító** vagy **Szállító**. | <p>A kiválasztott szállító alapján a rendszer automatikusan beírja az alapértelmezett értékeket a következő mezőkbe:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul> |
| Alvállalkozói szerződés | Hivatkozás a szállítói számla alvállalkozására. | <p>A kiválasztott alvállalkozói szerződés alapján a rendszer automatikusan megadja az alapértelmezett értékeket a következő mezőkben:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul><p>A szállítói számla fejlécében kiválasztott alvállalkozói szerződés alapértelmezés szerint meg van adva a szállítói számlasorokban, és ott nem módosítható.</p> |
| Számla dátuma | A szállítói számla megerősítésekor létrehozandó költség tényleges dátumának dátuma. | A számla dátuma arra is szolgál, hogy kiválassza a helyes beszerzési árlistát a kapcsolódó szállítóhoz csatolt árlistákból vagy a projektparaméterekből. |
| Állapot oka | A szállítói számla állapota. | <p>Az állapot határozza meg, hogy a szállítói számla hol van az üzleti folyamatban, és hogy szerkeszthető-e. Íme néhány a rendelkezésre álló értékek közül:</p><ul><li>**Piszkozat** – A szállítói számla szerkeszthető.</li><li>**Visszaigazolt** – A szállítói számla ellenőrzése és visszaigazolása megtörtént. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők vagy törölhetők.</li><li>**Folyamatban** – A szállítói számla felülvizsgálata folyamatban van. Az ebben az állapotban lévő szállítói számlák szerkeszthetők, de nem törölhetők.</li><li>**Törölve** – A szállítói számlát törölték. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők vagy törölhetők.</li></ul> |
| Pénznem | Az a pénznem, amellyel a szállító a szállítói számlán szereplő termékekért és szolgáltatásokért számlázik. | Az alvállalkozói szerződésre hivatkozó szállítói számlán alapértelmezés szerint az alvállalkozói szerződés pénzneme lesz megadva a szállítói számla pénznemeként. Olyan szállítói számlán, amely nem hivatkozik alvállalkozói szerződésre, az alapértelmezett érték a szállítói számlarekordból kerül megírásra, és módosítható. A szállítói számla mentése után a pénznem már nem szerkeszthető. |
| Szerződő részleg | Annak a vállalatnak a részlege, amely felelős a szolgáltatások és/vagy termékek eladótól való fogadásáért. | None |
| Fizetési feltételek | A kiállított szállítói számlák fizetési feltételei. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | Az alvállalkozói szerződésből származó fizetési feltételeket a rendszer átmásolja az alvállalkozói szerződéshez kapcsolódó összes szállítói számlára. A fizetési feltételek akkor frissíthetők, ha a szállítói számla állapota **Piszkozat**. |
| Fizetési cím | Annak a szállítónak a címe, akinek a kifizetéseket küldeni kell. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | Az alvállalkozói szerződésből származó fizetési cím fizetési címként átmásolódik az adott alvállalkozói szerződéshez létrehozott összes szállítói számlára. A fizetési cím frissíthető, ha a szállítói számla állapota **Piszkozat**. |
| Részösszeg | Ha a szállítói számlának nincsenek sorai, adja meg a számla adózás előtti részösszegét. Ha a szállítói számla sorokat tartalmaz, ez a mező csak olvasható. Ebben az esetben a megjelenített összeg a szállítói számla összes sorából származó részösszeg. | None |
| Összes adó | Ha a szállítói számla nem tartalmaz sorokat, adja meg az alvállalkozói szerződés összes adóját. Ha a szállítói számla sorokat tartalmaz, ez a mező csak olvasható. Ebben az esetben a megjelenített összeg a szállítói számla összes sorából származó adóösszegek összege. | None |
| Végösszeg | Ez a kiszámított mező a szállítói számla teljes összegét mutatja az adók szerepeltetése után. | None |

> [!NOTE]
> A szállítói számla következő mezői nem módosíthatók a szállítói számla mentése után: Szállító, Alvállalkozó, **Pénznem** **,** Szerződéses egység **és** Fizetési feltételek **.** **·** Ha a szállítói számlán módosítani kell ezeket a mezőket, törölnie kell a szállítói számlát, és létre kell hoznia egy új szállítói számlát.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
