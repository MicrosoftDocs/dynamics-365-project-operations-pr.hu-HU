---
title: Tranzakciós kategória használata árképzési dimenzióként
description: Ez a témakör a tranzakciós kategória árazási dimenzióként való használatáról nyújt tájékoztatást.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752296"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Tranzakciós kategória használata árképzési dimenzióként
Ez a témakör bemutatja, hogyan lehet tranzakciós kategóriát használni árképzési dimenzióként. Mielőtt elkezdené, ha még nem hozott létre árképzési megoldást, akkor létre kell hoznia egy újat. Ha már van árképzési dimenziós megoldása, akkor megváltoztathatja azt. Ha még nem hozott létre új árképzési dimenziós megoldást a szervezetének, akkor hajtsa végre az [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md) témakörben szereplő eljárásokat.

## <a name="add-transaction-category-to-forms-and-views"></a>Tranzakciós kategória hozzáadása űrlapokhoz és nézetekhez
Annak érdekében, hogy a tranzakciós kategóriák megjelenjenek az árazási dimenzió megoldás felhasználói felületén, végig kell lépnie a főbb entitások összes űrlapján és nézeté, és ezeket a mezőket hozzá kell adnia ezen entitások űrlapjaihoz és nézeteihez.
Az alábbi táblázat entitásonként felsorolva, átfogó módon tartalmazza azon beépített űrlapokat és nézeteket, amelyeket frissíteni szükséges az új mezőkkel. Ha ezeknek az entitásoknak a testreszabásaiban további nézetek vagy űrlapok vannak, akkor az új mezőket is hozzá kell adni azokhoz.

|  Entitás        | Űrlapok     |Nézetek        |
| ------------------------------|---------------------------------|----------------------------------|
|  Szerepkörár|• Információ |• Aktív erőforrás kategóriaárak<br> • Erőforrás-kategóriaárhoz kapcsolódó nézet|
|  Szerepkörárrés|• Információ|• Aktív szerepkör felár<br>• Aktív szerepkör felárral kapcsolatos nézet|
|  Árajánlatsor részletei|• Projektinformációk<br>• Projekt Gyors létrehozás|• Aktív ajánlati sor részlete<br>• Kombinált ajánlatsor részletei<br>• Ajánlatsorral kapcsolatos nézet|
|  A projekt szerződés sorának részlete|• Projektinformációk<br>• Projekt Gyors létrehozás|• Kombinált szerződés sor részletei<br>• Aktív szerződéses sor részletei<br>• A szerződéses sor részletekkel társított nézet|
|  Projektcsoporttag|• Információ<br>• Új űrlap|• Aktív projektcsapattagok<br>• Projektcsapattagok<br>• A Projektcsapattagokkal társított nézet|
|  Időbejegyzés|• Információ<br>• Időbejegyzés létrehozása|• Saját időbejegyzés dátum szerint<br>• Saját időbejegyzések erre a hétre<br>• Saját időbejegyzések jóváhagyása|
|  Naplósor|• Információ<br>• Gyors létrehozás|• Aktív naplósorok<br>• A Naplósorhoz kapcsolódó nézet|
|  Számlasor részletei|• Információ<br>• Gyors létrehozás|• Aktív számlasor részletei<br>• Díjazható számlatranzakciók<br>• Ingyenes számlatranzakciók<br>• A számlához tartozó sor részletének nézete<br>• Nem díjazható számlatranzakciók|
|  Tény|• Információ<br>• Aktív adatok|• Tényleges társított nézet|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Tranzakciós kategória használata árképzési dimenzióként

1. A webes felületen lépjen a **Project Service** > **Beállítások** > **Paraméterek** oldalra. 
2. A **Paraméterek** oldal **Mennyiségalapú árazási dimenziók** fülén látható, hogy a fülön található rács az **Árazási dimenzió** entitás bejegyzéseit mutatja.
3. Adja hozzá a **Tranzakciós Kategóriát** ehhez a listához, és állítsa be a **Vonatkozó költség** és **Vonatkozik eladásra** mezők beállítását **Igen** értékre.
4. A **Dimenzió típusa** mezőben válassza az **Összeg alapú** lehetőséget , majd válassza a **Tranzakciós kategória** prioritását a költségekkel és az eladásokkal kapcsolatban.
