---
title: Alvállalkozók beállítása lefoglalható erőforrásként
description: A témakör ismerteti, hogyan lehet a rendszerben felhasználókból és kapcsolattartókból létrehozott alvállalkozói erőforrásokat beállítani és karbantartani, hogy azok a Microsoft Dynamics 365 Project Operations alkalmazásban alvállalkozókhoz társíthatók legyenek.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994189"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Alvállalkozók beállítása lefoglalható erőforrásként

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A következő lépésekkel lehet beállítani az alvállalkozókat lefoglalható erőforrásként a Microsoft Dynamics 365 Project Operations alkalmazásban.

1. Válassza a **Projekt** \> **Erőforrások** lehetőséget, és válassza az **Új** lehetőséget.
2. Az **Új lefoglalható erőforrás** lap **Erőforrástípus** mezőjében válasszon egyet az alábbi lehetőségek közül:

    - **Felhasználó** – Akkor jelölje ki ezt az erőforrástípust, ha az alvállalkozónak hozzá kell férnie a Project Operationshöz, hogy időt vagy költségeket adjon meg. Ha a **Felhasználó** lehetőséget választja, akkor az alvállalkozónak érvényes licencre van szüksége a rendszer használatához.
    - **Kapcsolattartó** vagy **Partner** – Válassza ki az egyik ilyen erőforrástípust, ha az alvállalkozónak nincs szüksége a Project Operations-hozzáférésére, de feladat-hozzárendeléshez vagy projektekhez való foglaláshoz elérhetőnek kell lennie. Ezen erőforrástípusok egyikének sem ad hozzáférést a rendszerhez. Válassza a **Partner** lehetőséget, ha a szállító vállalatát képviseli foglalható erőforrásként. Válassza a **Kapcsolattartó** lehetőséget, ha a szállító egyik alkalmazottját képviseli.

3. A kiválasztott erőforrás típusától függően a rendszer kéri a megfelelő felhasználó-, partner- vagy kapcsolattartó-bejegyzés kiválasztására.
4. A **Dolgozó típusa** mezőben válassza a "Szerződéses dolgozó" lehetőséget az alvállalkozó foglalható erőforrásként való beállításhoz.

    > [!NOTE]
    > Ha üresen hagyja a **Dolgozó típus** mezőt kihagyja, akkor a foglalható erőforrás alkalmazottnak számít.

5. Ha a feldolgozó típusaként a **Szerződéses dolgozó** lehetőséget választotta, akkor jelölje ki azt a szállítót, akihez az erőforrás dolgozik.
6. Jelölje ki az erőforrás időzónáját, majd válassza a **Mentés** lehetőséget. Ha munkaóra-sablont szeretne hozzárendelni a foglalható erőforráshoz, akkor válassza a **Naptár beállítása** lehetőséget a **Foglalható erőforrások** listaoldalán.

Ahhoz, hogy a társítani lehessen az elszerződés sorához, a foglalható erőforrásnak teljesítenie kell az alábbi feltételeket:

- A foglalható erőforrásnak szerződéses dolgozónak kell lennie.
- A **Kapcsolattartó** erőforrástípusú foglalható erőforrását kapcsolattartóként kell társítani a szállítói partnerhez. A **Felhasználó** erőforrástípusú foglalható erőforrását nem kell kapcsolattartóként társítani a szállítói partnerhez.
- A foglalható erőforrás **Szállító** mezőjének értékének meg kell egyeznie az alvállalkozó **Szállító** mezőjének értékével.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>A lefoglalható erőforrások dolgozó és szállító leképezéseinek frissítése

A lefoglalható erőforrás **Dolgozó típusa** mezője azt határozza meg, hogy a foglalható erőforrás szerződéses dolgozó vagy alkalmazott-e. A **Szállító** mező definiálja azt a szállítói partnert, amelyhez a foglalható erőforrás társítva van. Ha egy foglalható erőforrást társít egy szállítóhoz kapcsolattartóként, jelzi, hogy a kapcsolattartó a szállító vállalat alkalmazottja.

Ha módosul a lefoglalható erőforrás **Dolgozó típusa** és **Szállító** mezője, akkor a módosítások hatással vannak a foglalható erőforrás által létrehozott új rekordokon, például időrekordokon végrehajtott esetleges ellenőrzésekre. A módosítások azonban nem érvénytelenítik a meglévő rekordokat.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
