---
title: Szállítói számlák ellenőrzése jóváhagyott tényleges értékekkel
description: Ez a témakör bemutatja, hogy a Microsoft Dynamics 365 Project Operations let's project managers hogyan ellenőrzi a szállítói számlákat a vállalkozók által jóváhagyott tényleges adatokkal, a munka elvégzésével és a rögzített idővel, valamint a projektcsapat tagjai által használt költségekkel és anyagokkal.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585473"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Szállítói számlák ellenőrzése jóváhagyott tényleges értékekkel

[!include [banner](../../includes/dataverse-preview.md)]

_ **Vonatkozik:** Lite telepítés - foglalkozik proforma számlázás

A Microsoft Dynamics 365 Project Operations let's project managers a következő módokon ellenőrzi a szállítói számlasorokat:

- Használja a **szállítói számla sorok Ellenőrzés állapot** mezőjét.
- Ha a szállítói számlasorok alvállalkozói sorra hivatkoznak, kapcsolja össze az alvállalkozói tevékenység költség-tényleges adatait az adott szállítói számlasorokkal. A hivatkozás úgy jön létre, hogy a költségalapokat a szállítói számlasorokhoz igazítja.

    > [!NOTE]
    > Bár az ellenőrzés állapota nyomon követhető az alvállalkozói szerződésre nem hivatkozó szállítói számlasorok esetében, a költség tényleges adatai nem csatolhatók ezekhez a szállítói számlasorokhoz.

## <a name="verification-status"></a>Ellenőrzés állapota

A **szállítói számlasor Ellenőrzés állapot** mezőjében az ellenőrzés állapota látható. A következő állapotok támogatottak:

1. Nem kezdődött el
2. Folyamatban
3. Teljesítés

A Nem indított **ellenőrzési állapotú** szállítói számlasorok szerkeszthetők.

A Folyamatban **állapotú** szállítói számlasorok már nem szerkeszthetők. Az alvállalkozói szerződésre hivatkozó szállítói számlasor esetében az ellenőrzési állapot automatikusan Folyamatban **értékre** lesz állítva, amint az első tényleges költség megegyezik a szállítói számlasorsal.

A Kész **állapotú** szállítói számlasorok már nem szerkeszthetők. Ha a szállítói számlán szereplő összes sor ilyen ellenőrzési állapotú, a szállítói számla megerősíthető.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Költségalapot egyeztet a szállítói számlasorokkal

A költségacélok egyeztetése segít a szállítói számlasor ellenőrzési folyamatában. Ha a költségalapokat egy szállítói számlasorhoz szeretné egyeztetni, hajtsa végre az alábbi lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza a **Páratlan költség tényleges érték** lapot. A rács azoknak a költségalapokat mutatja, amelyek ugyanarra az alvállalkozói sorra hivatkoznak, mint a szállítói számlasor.
2. Jelöljön ki egy vagy több költségalapot, majd válassza az Egyezés **lehetőséget** a rács feletti eszköztáron. A rendszer ellenőrzi, hogy a kiválasztott költség-ténylegesek kiegyenlíthetők-e. Az ellenőrzés letelte után a költség-tényleges értékek a szállítói számlasorhoz kapcsolódnak.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>A költség tényleges értékeinek szállítói számlasorokhoz való kapcsolására használt ellenőrzési feltételek

Az egyeztetési folyamat során a tényleges költség és a szállítói számlasor közötti kapcsolat csak akkor állapítható meg, ha mindkét alábbi feltétel teljesül:

- A **helyesbítés állapot** mezőjének minden kiválasztott tényleges költséghez üresnek kell lennie. Más szóval, a költség-tényleges költségeket nem helyettesíthették más költség-tényleges költségekkel a visszahívási, jóváhagyási törlési vagy javítási naplófolyamat során.
- A következő mezők értékei a szállítói számlasor és a kiválasztott tényleges költség között egyeznek. Ha a szállítói számlasorban nincs beállítva mező, akkor az nem tekinthető egyeztetésnek.

    - Projektszerződés
    - Projektszerződéssor
    - Tranzakcióosztály
    - Project
    - Feladatok
    - Erőforráskategória
    - Tranzakció kategóriája
    - Termék
    - Alvállalkozói sor
    - Lefoglalható erőforrás

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Kiegyenlítetlen költségalapokat szállítói számlasorból

A költségatékok páratlan kiegyenlítése segíthet a szállítói számlán szereplő ellenőrzési folyamatban is azáltal, hogy lehetővé teszi a korábban létrehozott hivatkozások eltávolítását. A költségalapokat csak olyan szállítói számlasorokból lehet párosítani, amelyek ellenőrzési állapota **Folyamatban van**. Ha egy szállítói számlasor költség-tényleges értékét szeretné kiegyenlíteni, hajtsa végre az alábbi lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza az **Egyeztetett költség tényleges** érték lapot. A rács a szállítói számlasorra hivatkozó költségalapokat jeleníti meg.
2. Jelöljön ki egy vagy több költségalapot, majd válassza a rács feletti eszköztár Egyezés **megszüntetése lehetőséget**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
