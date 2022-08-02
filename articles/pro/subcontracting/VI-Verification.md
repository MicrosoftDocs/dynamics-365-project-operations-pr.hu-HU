---
title: A szállítói számlák ellenőrzése jóváhagyott tényadatokkal
description: Ez a cikk azt ismerteti, hogy a Microsoft Dynamics 365 Project Operations projektmenedzserei hogyan ellenőrzik a szállítói számlákat a vállalkozók által a munka és a rögzített idő, valamint a projektcsapat tagjai által használt költségek és anyagok tényleges adataival.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204177"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>A szállítói számlák ellenőrzése jóváhagyott tényadatokkal

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Microsoft Dynamics 365 Project Operations a projektmenedzserek a következő módokon ellenőrzik a szállítói számlasorokat:

- Használja az **Ellenőrzés állapota** mezőt a szállítói számlasorokon.
- Ha a szállítói számlasorok alvállalkozói sorra hivatkoznak, az alvállalkozói tevékenységből származó költség tényleges adatait összekapcsolja az adott szállítói számlasorokkal. A hivatkozás úgy jön létre, hogy a költség tényleges adatait egyezteti a szállítói számlasorokkal.

    > [!NOTE]
    > Bár az ellenőrzés állapota nyomon követhető azoknál a szállítói számlasoroknál, amelyek nem hivatkoznak alvállalkozói szerződésre, a tényleges költségek nem kapcsolhatók össze ezekkel a szállítói számlasorokkal.

## <a name="verification-status"></a>Ellenőrzési állapot

A **szállítói számlasor Ellenőrzési állapota** mezője az ellenőrzés állapotát jelzi. A következő állapotok támogatottak:

1. Nem kezdődött el
2. Folyamatban
3. Teljesítés

A Nem elindított **ellenőrzési állapotú** szállítói számlasorok szerkeszthetők.

A Folyamatban **lévő ellenőrzési állapotú** szállítói számlasorok már nem szerkeszthetők. Alvállalkozói szerződésre hivatkozó szállítói számlasor esetében az ellenőrzési állapot automatikusan Folyamatban van **értékre lesz állítva**, amint az első tényleges költség megegyezik a szállítói számla sorával.

A Kész **ellenőrzési állapotú** szállítói számlasorok már nem szerkeszthetők. Ha a szállítói számla összes sora rendelkezik ezzel az igazolási állapottal, a szállítói számla megerősíthető.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Költség-tényleges adatok egyeztetése a szállítói számlasorokkal

A költség tényleges adatainak egyeztetése segít a szállítói számlasorok ellenőrzési folyamatában. Ha a költség tényleges adatait egy szállítói számlasorhoz szeretné egyeztetni, kövesse az alábbi lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza a **Nem egyező költség tényleges adatai** lapot. A rács a költség tényleges adatainak listáját jeleníti meg, amelyek ugyanarra az alvállalkozói sorra hivatkoznak, mint a szállítói számlasor.
2. Jelöljön ki egy vagy több tényleges költségértéket, majd válassza az Egyezés **lehetőséget** a rács feletti eszköztáron. A rendszer ellenőrzi, hogy a kiválasztott költség tényleges adatai párosíthatók-e. Az érvényesítés után a költség tényleges adatai összekapcsolják a szállítói számlasort.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>A tényleges költségadatoknak a szállítói számlasorokkal való összekapcsolására használt érvényességi feltételek

Az egyeztetési folyamat során a tényleges költség és a szállítói számlasor közötti kapcsolat csak akkor hozható létre, ha mindkét alábbi feltétel teljesül:

- A **Kiigazítás állapota** mezőnek minden kiválasztott tényleges költséghez üresnek kell lennie. Más szóval, a tényleges költségeket nem szabad más tényleges költségekkel helyettesíteni a visszahívási, jóváhagyási vagy javítási naplófolyamat során.
- A következő mezők értékei megegyeznek a szállítói számlasor és a kiválasztott tényleges költség között. Ha valamelyik mező nincs beállítva a szállítói számla sorában, akkor azt nem veszi figyelembe az egyezésnél.

    - Projektszerződés
    - Projektszerződéssor
    - Tranzakcióosztály
    - Project
    - Feladatok
    - Erőforrás-kategória
    - Tranzakció kategóriája
    - Termék
    - Alvállalkozói vonal
    - Lefoglalható erőforrás

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>A szállítói számlasorból származó költség tényleges adatok leválasztása

A tényleges költség nem egyezése a szállítói számlán lévő ellenőrzési folyamatban is segíthet, mivel lehetővé teszi a korábban létrehozott hivatkozások eltávolítását. A költség-tényleges adatok csak azokból a szállítói számlasorokból vonhatók össze, amelyek ellenőrzési állapota **Folyamatban** van. Ha le szeretné bontani a költség tényleges adatait egy szállítói számlasorból, kövesse az alábbi lépéseket.

1. Nyissa meg a szállítói számlasort, és válassza az **Egyező költség tényleges adatai** lapot. A rács a szállítói számlasorra hivatkozó költség tényleges adatok listáját jeleníti meg.
2. Jelöljön ki egy vagy több tényleges költségértéket, majd válassza a Leegyezés **lehetőséget** a rács feletti eszköztáron.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
