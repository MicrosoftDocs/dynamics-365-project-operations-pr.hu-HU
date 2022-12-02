---
title: Az értékesítési árak meghatározása a becslésekhez és a tényekhez
description: Ez a cikk arról nyújt tájékoztatást, hogy a az értékesítési árakat hogyan használják a projektalapú becslésekhez, és a tényadatok hogyan lesznek meghatározva.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475187"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Az értékesítési árak meghatározása a becslésekhez és a tényekhez

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az értékesítési árak meghatározásához a becsléseken és tényadatokon a Microsoft Dynamics 365 Project Operations alkalmazásban, a rendszer a bejövő becslés dátumát és pénznemét használja vagy az értékesítési ár meghatározásához használt aktuális kontextust. A tényleges kontextusban a rendszer a **Tranzakció dátuma** mező segítségével határozza meg, hogy melyik árlista alkalmazandó. A rendszer összeveti a bejövő becslés vagy tényadat **Tranzakció dátum** értékét az árlista **Hatályos kezdő dátum (Időzónától független)** és **Hatályos befejező dátum (Időzónától független)** értékeivel. Az értékesítési árlista meghatározását követően a rendszer meghatározza az értékesítési vagy a számlázási rátát.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>A tényleges és a becslési sorok értékesítési arányainak meghatározása időpontra

Az **Idő** becsült környezete a következőre utal:

- Árajánlatsor részletei **Időhöz**.
- Szerződéssor részletei **Időhöz**.
- Erőforrás-hozzárendelések egy projektben.

Az **Idő** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai az **Időhöz**.
- Időbejegyzés beküldésekor létrehozott naplósorok.
- Számlasor részletei **Időhöz**. 

Miután meghatározásra került az értékesítési árlista, a rendszer a következő lépéseket hajtja végre az alapértelmezett számlázási ráta meghatározásához.

1. A rendszer a becslésben található **Szerepkör** és **Erőforrás-kezelési egység** mezők kombinációjával vagy az **Idő** aktuális kontextusával a szerepkörársorokkal a árlistában. Ez a megfeleltetés feltételezi, hogy a számlázási árakhoz beépített árazási dimenziókat használ. Ha bármely más mező alapján konfigurálja az árképzést, vagy a **Szerepkör**, és az **Erőforrás-kezelési egység** mellett, akkor a rendszer ezen mezők a kombinációjával kéri le az egyező szerepkörársort.
1. Ha a rendszer egy olyan szerepkörársort talál, amely rendelkezik számlázási rátával a **szerepkör** és az **erőforrás-kezelési egység** mező kombinációjára, akkor az a számlázási ráta lesz alapértelmezett számlázási rátának használva.
1. Ha a rendszer nem tudja egyeztetni a **Szerepkör** és az **Erőforrás-kezelő egység** értékeit, akkor lekéri azokat a szerepkörársorokat, amelyek egyező értékekkel rendelkeznek a **Szerepkör** mezőhöz, de nulla értékekkel az **Erőforrás-kezelő egység** mezőhöz. Ha a rendszer talál egy megfelelő szerepkörárrekordot, akkor ennek a rekordnak a számlázási rátája lesz használva alapértelmezett számlázási rátaként. Ez az egyeztetés feltételezi, hogy létezik beépített konfiguráció a **Szerepkör** és az **Erőforrás-kezelési egység** relatív prioritásához értékesítési árképzési dimenzióként.

> [!NOTE]
> Ha eltérő prioritást állított be a **Szerepkör** és **Erőforrás-kezelési egység** mezőkhöz, vagy ha más, magasabb prioritású dimenziók találhatók, az előző viselkedés ennek megfelelően változik. A rendszer lekéri a szerepkörár rekordokat, amelyek olyan értékekkel rendelkeznek, amely megegyezik az egyes árképzési dimenziók értékével a prioritás sorrendjében. A dimenziókhoz null értékkel rendelkező sorok következnek utoljára.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>A tényleges és a becslési sorok értékesítési arányainak meghatározása költséghez

A **Költség** becsült környezete a következőre utal:

- Árajánlatsor részletei **Költésghez**.
- Szerződéssor részletei **Költésghez**.
- Költségbecslés-sorok a projektben.

A **Költség** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai a **Költséghez**.
- Költségbejegyzés beküldésekor létrehozott naplósorok.
- Számlasor részletei **Költséghez**. 

Miután meghatározásra került az értékesítési árlista, a rendszer a következő lépéseket hajtja végre az alapértelmezett értékesítési egységár megadásához.

1. A rendszer a **Költségre** vonatkozó becslési sorban található **Kategória** és **Egység** mezőkombinációval felelteti meg a kategória-ársorokat a megoldott árlistában.
1. Ha a rendszer egy olyan kategória-ársort talál, amely rendelkezik értékesítési rátával a **Kategória** és az **Egység** mező kombinációjára, akkor ez az értékesítési ráta lesz használva alapértelmezett értékesítési rátaként.
1. Ha a rendszer megfelelő kategória-árlistát talál, akkor az árképzési mód használható az alapértelmezett értékesítési ár megadásához. A következő táblázat mutatja be a költségárak alapértelmezésének viselkedését a Project Operations alkalmazásban.

    | Környezet | Árképzési mód | Alapértelmezett ár |
    | --- | --- | --- |
    | Becslés | Egységár | A kategória ár sora alapján. |
    |        | Költségen | 0.00. |
    |        | Haszonkulcs feletti költség | 0.00. |
    | Tényleges | Egységár | A kategória ár sora alapján. |
    |        | Költségen | A kapcsolódó költségek tényleges értéke alapján. |
    |        | Haszonkulcs feletti költség | A kategória ár sora szerint megadott árrés van alkalmazva a kapcsolódó költség tényleges értékének egységköltségrátájára. |

1. Ha a rendszer nem tudja összeegyeztetni a **Kategória** és az **Egység** értékeket, az értékesítési ráta alapértelmezetten **0**-ra (nulla) csökken.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Értékesítési árak meghatározása a tényekhez és a becslésekhez az Anyag számára

Az **Anyag** becsült környezete a következőre utal:

- Árajánlatsor részletei **Anyaghoz**.
- Szerződéssor részletei **Anyaghoz**.
- Anyagbecslés-sorok a projekten.

Az **Anyag** aktuális környezete a következőre utal:

- A Beviteli és Helyesbítési napló sorai **Anyaghoz**.
- Az Anyaghasználati napló beküldésekor létrehozott naplósorok.
- Számlasor részletei **Anyaghoz**. 

Miután meghatározásra került az értékesítési árlista, a rendszer a következő lépéseket hajtja végre az alapértelmezett értékesítési egységár megadásához.

1. A rendszer a becslési sorban szereplő **Termék** és **Egység** mező kombinációját egyezteti a becsléssoron az **Anyaghoz** az árlista-cikksorokkal szemben az árlistán.
1. Ha a rendszer olyan árlistaelem sort talál, amely a **Termék** és az **Egység** kombináció eladási díját tartalmazza, illetve az árképzési módszer **Pénznem összege**, akkor a rendszer az árlistasorban megadott eladási árat használja. 
1. Ha a **Termék** és az **Egység** mező értékei nem egyeznek meg, vagy ha az árképzési mód nem **Pénznem összege**, az értékesítési arány alapértelmezés szerint **0** (nulla) lesz. Ez a viselkedés azért fordul elő, mert a Project Operations a projektnél használt anyagok esetében csak **Pénznemösszeg** árképzési módot támogatja.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
