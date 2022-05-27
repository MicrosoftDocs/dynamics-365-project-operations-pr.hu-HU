---
title: Szállítói számlák fejadatai
description: Ez a témakör a Microsoft szállítói számlafejlécén található funkciókat ismerteti Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575583"
---
# <a name="header-details-for-vendor-invoices"></a>Szállítói számlák fejadatai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Microsoft szállítói számlafejlécén található funkciókat ismerteti Dynamics 365 Project Operations.

Mivel a projektmenedzserek projekteket terveznek és hajtanak végre, alvállalkozókat alkalmazhatnak, és termékeket és szolgáltatásokat vásárolhatnak a szállítóktól. A projekt végrehajtása során a költségek a szállítókkal kötött alvállalkozói szerződések során beszerzett szolgáltatásokból, anyagokból és költségkategóriákból származnak. A szállítók szállítói számlák létrehozásával számlázzák ki ezeket a költségeket a projekteknek.

Az alábbi táblázat a Projektműveletek szállítói számlafejléceinek mezőiről tartalmaz tájékoztatást.

| Mező | Description | Funkcionális hatás |
| --- | --- | --- |
| Name | A szállítói számla neve. | Az összes szállítói számla legördülő listában a szállítói számla neve az első oszlopban szerepel, amely segít azonosítani a szállítói számlát. Alapértelmezés szerint, amikor egy szállítói számlát alvállalkozói szerződésből hoznak létre, a **szállítói számla Név** mezője olyan értékre van állítva, amely az alvállalkozó nevéből és az aktuális dátumból áll. |
| Description | A szállítói számlán számlázott szolgáltatások és termékek rövid leírása. | None |
| Beszállító | A termékekért és szolgáltatásokért számlázó vállalat neve. Ennek a vállalatnak olyan számlabejegyzésnek kell lennie, amely szállító **vagy** szállító kapcsolattípussal **rendelkezik**. | <p>A kijelölt szállító alapján a program automatikusan beírja az alapértelmezett értékeket a következő mezőkbe:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul> |
| Alvállalkozói szerződés | Hivatkozás a szállítói számla alvállalkozói szerződésére. | <p>A kijelölt alvállalkozói szerződés alapján a rendszer automatikusan beírja az alapértelmezett értékeket a következő mezőkbe:</p><ul><li>Pénznem</li><li>Árlisták</li><li>Fizetési feltételek</li><li>Fizetési cím</li></ul><p>A szállítói számlafejen kiválasztott alvállalkozói szerződés alapértelmezés szerint be van írva a szállítói számlasorokba, és ott nem módosítható.</p> |
| Számla dátuma | A szállítói számla megerősítésekor létrehozandó költségalapokat tartalmazó dátum. | A számladátum a megfelelő beszerzési árlista kiválasztására is szolgál a kapcsolódó szállítóhoz csatolt árlistákból vagy a projektparaméterekből. |
| Állapot oka | A szállítói számla állapota. | <p>Az állapot határozza meg, hogy a szállítói számla hol van az üzleti folyamatban, és hogy szerkeszthető-e. Íme néhány a rendelkezésre álló értékek közül:</p><ul><li>**Vázlat** – a szállítói számla szerkeszthető.</li><li>**Megerősítve** – a szállítói számlát ellenőrizték és megerősítették. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők és nem törölhetők.</li><li>**Folyamatban** – a szállítói számla felülvizsgálata folyamatban van. Az ebben az állapotban lévő szállítói számlák szerkeszthetők, de nem törölhetők.</li><li>**Visszavonva** – a szállítói számla érvénytelenítve. Az ebben az állapotban lévő szállítói számlák nem szerkeszthetők és nem törölhetők.</li></ul> |
| Pénznem | Az a pénznem, amelyben a szállító a szállítói számlán szereplő termékekhez és szolgáltatásokhoz számláz. | Az alvállalkozói szerződésre hivatkozó szállítói számlán alapértelmezés szerint az alvállalkozó pénzneme lesz megadva a szállítói számla pénznemeként. Olyan szállítói számlán, amely nem hivatkozik alvállalkozói szerződésre, a program az alapértelmezett értéket a szállítói számlabejegyzésből adja meg, és módosítható. A szállítói számla mentése után a pénznem már nem szerkeszthető. |
| Szerződő részleg | A szolgáltatások és/vagy termékek szállítótól történő átvételéért felelős vállalat részlege. | None |
| Fizetési feltételek | A kiállított szállítói számlák fizetési feltételei. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | Az alvállalkozói szerződésből származó fizetési feltételeket a program az alvállalkozói szerződéshez kapcsolódó összes szállítói számlára átmásolja. A fizetési feltételek frissíthetők, ha a szállítói számla állapota **Vázlat**. |
| Fizetési cím | Annak a szállítónak a címe, akinek a kifizetéseket küldeni kell. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | Az alvállalkozói szerződésből származó fizetési cím kifizetési címként átmásolódik az adott alvállalkozóhoz létrehozott összes szállítói számlára. A fizetési cím frissíthető, ha a szállítói számla állapota **Piszkozat**. |
| Részösszeg | Ha a szállítói számlán nincsenek sorok, adja meg a számla részösszegét adózás előtt. Ha a szállítói számla sorai vannak, ez a mező írásvédett. Ebben az esetben a megjelenített összeg a szállítói számla összes sorából származó részösszeg. | None |
| Teljes adó | Ha a szállítói számlán nincsenek sorok, adja meg az alvállalkozó összes adóját. Ha a szállítói számla sorai vannak, ez a mező írásvédett. Ebben az esetben a megjelenített összeg a szállítói számla összes sorából származó adóösszegek összege. | None |
| Végösszeg | Ez a kiszámított mező a szállítói számla teljes összegét mutatja az adók belefoglalása után. | None |

> [!NOTE]
> A szállítói számla következő mezői nem módosíthatók a szállítói számla mentése után: **Szállító, Alvállalkozó** **,** Pénznem **,** Szerződéskötési egység **és** Fizetési **feltételek**. Ha a szállítói számlán ezeknek a mezőknek a módosítása szükséges, törölje a szállítói számlát, és hozzon létre egy új szállítói számlát.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
