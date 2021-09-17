---
title: Az alvállalkozói szerződések fejlécének adatai
description: Ez a témakör a Project Operations alvállalkozói szerződés fejlécének funkcióit ismerteti.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323644"
---
# <a name="header-details-for-subcontracts"></a>Az alvállalkozói szerződések fejlécének adatai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Dynamics 365 Project Operations alvállalkozói szerződés fejlécén található funkciókat ismerteti.

A projektmenedzser a projektek tervezése és végrehajtása során alvállalkozókat alkalmazhat, valamint termékeket és szolgáltatásokat vásárolhat a szállítóktól. Ha egy projektmenedzsernek termékeket vagy szolgáltatásokat kell vásárolnia, a Project Operations-ben alvállalkozói szerződést hozhat létre.

Alvállalkozói szerződés létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** lehetőséget, majd az **Alvállalkozói szerződés** lapon válassza az **Új** lehetőséget.
2. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.

    A következő táblázat az Alvállalkozói szerződés fejlécének mezőivel kapcsolatos információkat tartalmazza.

    | **Mező** | **Leírás** |
    | --- | --- | 
    | Adatfolyam neve | Az alvállalkozói szerződés neve. |
    | Ismertetés | Az alvállalkozói szerződés keretében megvásárolt szolgáltatások és termékek rövid leírása. |
    | Beszállító | Annak a vállalatnak a neve, amelytől a termékeket és szolgáltatásokat vásárolják. Ez a számlarekord a **Szállító** vagy a **Beszállító** kapcsolattípusával rendelkezik. |
    | Alvállalkozói szerződés dátuma | Az alvállalkozói szerződés létrehozásának dátuma. |
    | Állapot oka | Az alvállalkozói szerződés státusza. |
    | Pénznem | Az a pénznem, amelyben a termékeket és szolgáltatásokat vásárolják. A mező értéke alapértelmezés szerint a szállítói számla értéke, de megváltoztatható. Az alvállalkozói szerződésben szereplő termékek és szolgáltatások árazásához használt projektárlistáknak ebben a pénznemben kell szerepelniük. Az alvállalkozói szerződéshez nem lehet más pénznemben kiadott árlistákat társítani. Az alvállalkozói szerződés keretében felmerült termékek és szolgáltatások költségei ebben a pénznemben kerülnek elszámolásra a projektben. |
    | Szerződő részleg | A vállalat azon részlege, amely a szállítóval adásvételi szerződést vagy alvállalkozói szerződést köt. |
    | Fizetési feltételek | Az ezen alvállalkozói szerződés keretében kiállított szállítói számlák fizetési feltételei. A mező értéke alapértelmezés szerint a szállítói számla rekordjából származik. |
    | Fizetési cím | A cím, ahová a szállítói számlák kifizetését küldik. A mező értéke alapértelmezés szerint a szállítói számla rekordjából származik. |
    | Számlázási név | Annak a személynek vagy részlegnek a neve a szállító cégénél, aki a számlát küldi. A mező értéke alapértelmezés szerint a szállítói számla rekordból származik, és az alvállalkozói szerződéshez létrehozott szállítói számlákon az elsődleges kapcsolattartó neveként lesz használva. |
    | Számlázási cím | A szállítótól származó számlákon használt cím. A mező értéke alapértelmezés szerint a szállítói számla rekordjából származik. Ezt a címet használják az alvállalkozói szerződéshez kiállított szállítói számlák számlázási címeként is. |
    | Részösszeg | Ha egy alvállalkozói szerződésnek nincsenek sorai, akkor ebbe a mezőbe egy olyan értéket kell beírni, amely a megrendelés adózás előtti részösszegét jelöli. Ha az alvállalkozói szerződés sorokkal rendelkezik, ez a mező csak olvasható. A megjelenített összeg az alvállalkozói szerződés összes sorának részösszege. |
    | Összes adó | Ha egy alvállalkozói szerződésnek nincsenek sorai, akkor ebbe a mezőbe az alvállalkozói szerződés adóit jelölő értéket kell beírni. Ha az alvállalkozói szerződés sorokkal rendelkezik, ez a mező csak olvasható. A megjelenített összeg az alvállalkozói szerződés összes sorában szereplő adóösszeg összege. |
    | Teljes összeg |  Ez a számított mező az alvállalkozói szerződés teljes összegét mutatja az adók figyelembevétele után.  |
    | Megerősítés dátuma | Az alvállalkozói szerződés megerősítésének dátuma.  |
    | Kérelmező | A mező értéke alapértelmezés szerint az alvállalkozói szerződést létrehozó felhasználó neve. Ezt az értéket az alvállalkozói szerződés létrehozója módosíthatja annak a személynek a megjelölésére, akinek a nevében az alvállalkozói szerződést létrehozza.  |
    | Szállítói ügyfélfelelős | A szállítói számla elsődleges kapcsolattartójának neve. A mező értéke alapértelmezés szerint a szállítói számla rekordjából származik. Ezt a mezőértéket a felhasználó megváltoztathatja, hogy egy másik kapcsolattartót válasszon az alvállalkozói szerződés szállítói számlavezetőjének. E-mail riasztások és ártárgyalások konfigurálhatók és küldhetők ezen a kapcsolattartón keresztül. |


