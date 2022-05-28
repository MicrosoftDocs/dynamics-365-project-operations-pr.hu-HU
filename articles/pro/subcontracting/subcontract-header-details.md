---
title: Az alvállalkozói szerződések fejlécének adatai
description: Ez a témakör a Project Operations alvállalkozói szerződés fejlécének funkcióit ismerteti.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fade0ff876486ad60ffd9ad618be7864c1b28185
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598169"
---
# <a name="header-details-for-subcontracts"></a>Az alvállalkozói szerződések fejlécének adatai

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a témakör a Dynamics 365 Project Operations alvállalkozói szerződés fejlécén található funkciókat ismerteti.

A projektmenedzser a projektek tervezése és végrehajtása során alvállalkozókat alkalmazhat, valamint termékeket és szolgáltatásokat vásárolhat a szállítóktól. Ha egy projektmenedzsernek termékeket vagy szolgáltatásokat kell vásárolnia, a Project Operations-ben alvállalkozói szerződést hozhat létre.

Alvállalkozói szerződés létrehozásához hajtsa végre a következő lépéseket.

1. A navigációs ablaktáblán válassza az **Alvállalkozói szerződések** lehetőséget, majd az **Alvállalkozói szerződés** lapon válassza az **Új** lehetőséget.
2. Írja be a szükséges információkat, majd kattintson a **Mentés** elemre.

    A következő táblázat az **Alvállalkozói szerződés fejlécének** mezőivel kapcsolatos információkat tartalmazza.

    | Mező | Ismertetés |Funkcionális hatás |
    |---|------|---| 
    | Adatfolyam neve | Az alvállalkozói szerződés neve. | Minden alvállalkozói szerződés legördülő listán az alvállalkozói szerződés neve szerepel az első oszlopban, amely segít azonosítani az alvállalkozói szerződést. | 
    | Ismertetés | Az alvállalkozói szerződés keretében megvásárolt szolgáltatások és termékek rövid leírása. | Egyik sem |
    | Beszállító | Annak a vállalatnak a neve, amelytől a termékeket és szolgáltatásokat vásárolják. Ez a számlarekord a **Szállító** vagy a **Beszállító** kapcsolattípusával rendelkezik. | A kijelölt szállítótól függően a rendszer automatikusan beírt alapértelmezett értékeket a következő mezőkhöz:<br/> **• Pénznem** </br> **• Árlisták** </br> **• Fizetési feltételek**</br> **• Fizetési cím**</br> **• Számlázási cím**</br> **• Számlázási név** </br>**• Szállítói ügyfélfelelős**|
    | Alvállalkozói szerződés dátuma | Az alvállalkozói szerződés létrehozási dátuma. | Az alvállalkozói szerződés dátuma a megfelelő beszerzési árlista kiválasztására használatos a kapcsolódó szállítóhoz csatolt árlistákból vagy a projektparaméterekből. |
    | Állapot oka | Az alvállalkozói szerződés státusza. | Az állapot meghatározza, hogy az alvállalkozói szerződés hol van az üzleti folyamatban, és hogy szerkeszthető-e. <br/>Az értékek többek között az alábbiak lehetnek:<br>• **Vázlat**: Az alvállalkozói szerződés szerkeszthető. Csak **Vázlat** állapotú alvállalkozói szerződések szerkeszthetők.<br/>• **Jóváhagyva**: Az alvállalkozóval való egyeztetés befejeződött, és az alvállalkozó jóváhagyásra kerül a szállításhoz. <br/>• **Lezárva**: Az alvállalkozói szerződéshez tartozó szállítás befejeződött.<br/>• **Visszavonva**: Az alvállalkozói szerződést visszavonták, és nem terveznek szállítást.  | 
    | Pénznem | A pénznem, amelyben a termékeket és szolgáltatásokat megvásárolják. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói fiókból, de ez módosítható. | Az alvállalkozói szerződés pénzneme a beszerzési árlista kiválasztására használatos a kapcsolódó szállítóhoz csatolt árlistákból vagy a projektparaméterekből. A más pénznemben található árlisták nem társíthatóak az alvállalkozóhoz. Az alvállalkozó által az alvállalkozói erőforrások részéről szállított idő-, költség- és anyagköltség ebben a pénznemben van rögzítve a projekthez. Az alvállalkozó rekord mentése után az alvállalkozói szerződés pénzneme nem módosítható.|
    | Szerződő részleg | A vállalat azon részlege, amely a szállítóval adásvételi szerződést vagy alvállalkozói szerződést köt. | Egyik sem |
    | Fizetési feltételek | Az alvállalkozói szerződés alapján kiadott szállítói számlák fizetési feltételei. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | A rendszer az alvállalkozói szerződés fizetési feltételeit az alvállalkozói szerződéssel kapcsolatos összes szállítói számlára másolja. A fizetési feltételek frissíthetők, ha az alvállalkozói szerződés **Vázlat** állapotú. | 
    | Fizetési cím | Annak a szállítónak a címe, akinek a kifizetéseket küldeni kell. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | A rendszer az alvállalkozói szerződés kifizetési címét kifizetési címként másolja át az alvállalkozói szerződéshez létrehozott minden szállítói számlára. A kifizetési cím frissíthető, ha az alvállalkozói szerződés **Vázlat** állapotú.|
    | Számlázási név | Annak a személynek vagy részlegnek a neve a szállító cégénél, aki a számlát küldi. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | A rendszer az alvállalkozói szerződés **Számlázási név** értékét az alvállalkozói szerződéssel kapcsolatos összes szállítói számlára másolja. Ez a mező frissíthető, ha az alvállalkozói szerződés **Vázlat** állapotú.|
    | Számlázási cím | A szállítói számlákon használt cím. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. | Ez a cím az alvállalkozói szerződéshez létrehozott szállítói számlák "számla kiállítója" címe. |
    | Részösszeg | Ha egy alvállalkozói szerződésnek nincsenek sorai, adja meg a rendelés részösszegét az adók előtt. Ha az alvállalkozói szerződés sorokkal rendelkezik, ez a mező csak olvasható. A megjelenő összeg az alvállalkozói szerződés összes sorából származó részösszeg. | Egyik sem |
    | Összes adó | Ha egy alvállalkozói szerződésnek nincsenek sorai, adja meg az összes adót ezen az alvállalkozói szerződésen. Ha az alvállalkozói szerződés sorokkal rendelkezik, ez a mező csak olvasható. A megjelenő összeg az alvállalkozói szerződés összes sorából származó adóösszeg. | Egyik sem |
    | Teljes összeg | Ez a számított mező az alvállalkozói szerződés teljes összegét mutatja az adók figyelembevétele után. | Egyik sem |
    | Megerősítés dátuma | Az alvállalkozói szerződés megerősítésének dátuma. | Egyik sem |
    | Kérelmező | A mező alapértelmezés szerint az alvállalkozói szerződést létrehozó felhasználó nevére van beállítva. Az alvállalkozói szerződés létrehozója azonban módosíthatja az értéket annak a személynek a feltüntetéséhez, aki nevében az alvállalkozói szerződést létrehozza. | Egyik sem |
    | Szállítói ügyfélfelelős | A szállítói számla elsődleges kapcsolattartójának neve. Az alapértelmezett értéket a rendszer automatikusan beírta a szállítói partnerrekordból. Másik kapcsolattartót is kijelölhet az alvállalkozói szerződés alvállalkozó partnerkezelőjeként. | Beállíthatja, hogy az ártárgyalásokat követően e-mailben értesítést küldjön a kapcsolattartónak az alvállalkozói szerződésen végrehajtott módosításokról. |
