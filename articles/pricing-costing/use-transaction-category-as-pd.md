---
title: Tranzakciókategória használata árképzési dimenzióként
description: Ez a témakör a tranzakciós kategória mező árazási dimenzióként való használatáról nyújt tájékoztatást.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513992"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Tranzakciókategória használata árképzési dimenzióként


_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


Ez a témakör bemutatja, hogyan lehet a **Tranzakciós kategória** mezőt használni árképzési dimenzióként. 

## <a name="prerequisites"></a>Előfeltételek
Az ebben a témakörben található az eljárások befejezése előtt egy új árképzési dimenzió megoldással kell rendelkeznie a szervezet számára. Ha még nem hozott létre ilyet, olvassa el az [Egyéni mezők és entitások létrehozása árazási dimenzióként](create-custom-fields-entities-pricing-dimensions.md) című témakört.

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Adja hozzá a Tranzakciós kategória mezőt az űrlapokhoz és nézetekhez
Ha azt szeretné , hogy a **Tranzakciós kategória** mező látható legyen az árképzési dimenzió megoldásban, akkor az összes űrlaphoz és nézethez hozzá kell adnia a mezőt entitásként.

Az alábbi táblázat entitásonként sorolja fel az összes előre telepített űrlapot és nézetet. Az új mezőt hozzá kell adnia a testreszabott entitások további űrlapjaihoz vagy nézeteihez is.

|  Entity        | Űrlapok     |Nézetek        |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár| Tájékoztatás |- Erőforrás-kategória aktív árai<br> - Erőforrás-kategória ára társítva |
|  Szerepkörárrés| Tájékoztatás|- Aktív szerepkörárrés<br>- Szerepkörárrés társítva |
|  Árajánlatsor részletei|- Projektinformáció<br>- Projekt gyorslétrehozása| - Aktív árajánlatsor-részlet<br>- Kombinált árajánlatsor részletei<br>- Árajánlatsor-részlet társított nézete |
|  Projektszerződés sorának részletei|- Projektinformáció<br>- Projekt gyorslétrehozása|- Kombinált szerződéssorrészletek<br>- Aktív szerződéssorrészletek<br>- Társított szerződéssor-részletek |
|  Projektfeladat|- Tájékoztatás<br>- Új űrlap| &nbsp; |
|  Projektcsoporttag|- Tájékoztatás<br>- Új űrlap|- Aktív projektcsoporttagok<br>- Projektcsoporttagok<br>- Projektcsoporttagok társítva |
|  Időbejegyzés|- Tájékoztatás<br>- Időbejegyzés létrehozása|- Saját időbejegyzések dátum szerint<br>- Saját időbejegyzések ezen a héten<br>- Jóváhagyandó időbejegyzések|
|  Naplósor|- Tájékoztatás<br>- Gyorslétrehozás|- Aktív naplósorok<br>- Naplósor társított nézete|
|  Számlasor részletei|- Tájékoztatás<br>- Gyorslétrehozás|- Aktív számlasorrészlet<br>- Számlázható számlatranzakciók<br>- Kiegészítő számlatranzakciók<br>- Társított számlasorrészlet <br>- Nem díjazható számlatranzakciók|
|  Tényadat|- Tájékoztatás<br>- Aktív tényleges adatok| Tényleges adatok társítva |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Tranzakciós kategória használata árképzési dimenzióként

1. Válassza a **Beállítások** > **Paraméterek** lehetőséget. 
2. A **Paraméterek** oldal **Mennyiségalapú árazási dimenziók** fülén ellenőrizze, hogy a fülön található rács az **Árazási dimenzió** entitás bejegyzéseit mutatja.
3. Adja hozzá a **Tranzakciós Kategóriát** ehhez a listához, és állítsa be a **Vonatkozó költség** és **Vonatkozik eladásra** mezők beállítását **Igen** értékre.
4. A **Dimenzió típusa** mezőben válassza az **Összeg alapú** lehetőséget , majd válassza a **Tranzakciós kategória** prioritását, mivel ez kapcsolódik a költségekhez és az eladásokhoz.
