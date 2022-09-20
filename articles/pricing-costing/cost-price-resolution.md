---
title: Költséghányadok meghatározása projektalapú becslésekhez és tényleges adatokhoz
description: Ez a cikk arról nyújt tájékoztatást, hogyan határozzák meg a projektalapú becslések és tényleges költségek költségarányát.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475276"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Költséghányadok meghatározása projektalapú becslésekhez és tényleges adatokhoz

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Microsoftnál Dynamics 365 Project Operations a becslések és a tényleges adatok alapján történő költségárak meghatározásához a rendszer először a dátumot és a pénznemet használja a bejövő becslésben vagy a tényleges környezetben az eladási árlista meghatározásához. Konkrétan a tényleges kontextusban a rendszer a **Tranzakció dátuma** mezőt használja annak meghatározására, hogy melyik árlista alkalmazható. A **bejövő becslés vagy tényleges tranzakciódátum-értékét** összehasonlítjuk az **árlistában szereplő Tényleges kezdés (Időzóna-független)** és **Tényleges befejezés (Időzóna-független)** értékekkel. Az önköltségi árlista meghatározása után a rendszer meghatározza a költséghányadot.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>A költségszintek meghatározása a becsült és a tényleges kontextusban az időhöz

Az idő **kontextusának** becslése a következőkre utal:

- Idézet sor részletei az **Időhöz**.
- A szerződéssor részletei az **Időhöz**.
- Erőforrás-hozzárendelések egy projekten.

Az Idő **tényleges kontextusa** a következőkre utal:

- Bejegyzési és javítási naplósorok az **Időhöz**.
- Naplósorok, amelyek az időbevitel elküldésekor jönnek létre.

Az önköltségi árlista meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett költségdíj megadásához.

1. A rendszer megfelelteti a Szerepkör **,** a Forrásvállalat **és** az **Erőforrásegység** mezők kombinációját az Idő becsült vagy tényleges kontextusában **az árlistában** szereplő szerepkör-ársorokkal. Ez az egyezés feltételezi, hogy a munkaerőköltséghez a standard díjszabási dimenziókat használja. Ha úgy konfigurálta a rendszert, hogy a Szerepkör **, az Erőforrás-kezelő vállalat** és **az Erőforrásegységen** kívül vagy azon kívül **más mezőket is egyeztessen, a rendszer egy másik kombinációt használ a megfelelő szerepkör-ársor lekéréséhez**.
1. Ha a rendszer olyan szerepkör-ársort talál, amely költségtárat tartalmaz a szerepkör **,** az erőforrás-kezelő vállalat **és** az **erőforrásegység** kombinációjához, akkor ezt a költségrátát használja alapértelmezett költséghányadként.
1. Ha a rendszer nem tudja egyeztetni a szerepkör **,** az erőforrás-vállalat **és** az **erőforrásegység** értékeit, akkor eldobja a legalacsonyabb prioritású dimenziót, megkeresi azokat a szerepkör-ársorokat, amelyek megegyeznek a másik két dimenzióértékkel, és továbbra is fokozatosan csökkenti a dimenziókat, amíg meg nem találja a megfelelő szerepkör-ársort. A rekordból származó költségráta lesz az alapértelmezett költségdíj. Ha a rendszer nem talál egyező szerepkör ársort, az ár alapértelmezés szerint 0 **(nulla) lesz beállítva**.

> [!NOTE]
> Ha a Szerepkör **és** az **Erőforrásegység** mezők eltérő rangsorolását konfigurálja, vagy ha más dimenziói is vannak, amelyek magasabb prioritással rendelkeznek, az előző viselkedés ennek megfelelően változik. A rendszer lekéri azokat a szerepkör-árrekordokat, amelyek olyan értékeit tartalmazza, amelyek prioritási sorrendben egyeznek az egyes árképzési dimenziók értékével. Azok a sorok, amelyek null értékűek ezekhez a dimenziókhoz, az utolsók.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>A tényleges költségdíjak meghatározása és a költség becsült sorai

A költség **becsült kontextusa** a következőkre utal:

- Árajánlat sor részletei a **Költséghez**.
- A szerződéssor részletei a **Költséghez**.
- Egy projekt költségbecslései.

A Költség **tényleges kontextusa** a következőkre vonatkozik:

- Bejegyzési és javítási naplósorok a **Költséghez**.
- Naplósorok, amelyek a költségbejegyzés elküldésekor jönnek létre.

Az önköltségi árlista meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett költségdíj megadásához.

1. A rendszer megfelelteti a Kategória és **az** Egység **mezők kombinációját a Költség** becsült vagy tényleges kontextusában **az árlistában** szereplő kategóriaársorokkal.
1. Ha a rendszer olyan kategória-ársort talál, amely a Kategória **és** az Egység **kombinációhoz tartozik költségdíjjal, akkor ezt a** költségrátát használja alapértelmezett költségként.
1. Ha a rendszer nem tud megfelelni a Kategória és az **Egység** értéknek **, az ár alapértelmezés szerint 0** (nulla) **értékre van állítva.**
1. A becslési környezetben, ha a rendszer talál egy megfelelő kategória ársort, de az árképzési módszer nem más, mint **az egységenkénti** ár, a költségráta alapértelmezés szerint 0 **(nulla) értékre** van állítva.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>A tényleges költségszintek meghatározása és a material becsült sorai

Az anyag **becsült kontextusa** a következőkre utal:

- Idézet sor részletei az **anyaghoz**.
- A Szerződéssor részletei az **anyaghoz**.
- Anyagbecslések egy projektről.

Az Anyag **tényleges kontextusa** a következőkre utal:

- Bejegyzési és javítási naplósorok az **anyaghoz**.
- Naplósorok, amelyek az anyaghasználati napló elküldésekor jönnek létre.

Az önköltségi árlista meghatározása után a rendszer a következő lépéseket hajtja végre az alapértelmezett költségdíj megadásához.

1. A rendszer a Termék és az **Egység** mezők kombinációját használja az Anyag **becsült vagy tényleges kontextusában** az árlista árlista cikksoraival **szemben.**
1. Ha a rendszer olyan árlista-cikksort talál, amely a Termék **és** az Egység **kombinációhoz tartozó költséghányadot tartalmaz, akkor ezt a** költségrátát használja alapértelmezett költségdíjként.
1. Ha a rendszer nem tud megegyezni a **Termék** és **az Egység** értékekkel, az egységköltség alapértelmezés szerint 0 **(nulla) értékre van állítva**.
1. A becsült vagy a tényleges környezetben, ha a rendszer talál egy megfelelő árlista-tételsort, de az árképzési módszer nem más, mint **a Pénznem összege**, az egységköltség alapértelmezés szerint 0-ra **van** állítva. Ez a viselkedés azért fordul elő, mert a Project Operations csak a **pénznemösszeg-árazási** módszert támogatja a projektben használt anyagokhoz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
