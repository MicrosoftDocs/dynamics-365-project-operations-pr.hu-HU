---
title: Tranzakciós kategória használata árképzési dimenzióként
description: Ez a témakör a tranzakciós kategória árazási dimenzióként való használatáról nyújt tájékoztatást.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ede5f95a3ba7e122e28875acad1ecc63ff095e63
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593339"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Tranzakciós kategória használata árképzési dimenzióként

[!include [banner](../includes/psa-now-project-operations.md)]

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
|  Projektfeladat|• Információ<br>• Új űrlap||
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
