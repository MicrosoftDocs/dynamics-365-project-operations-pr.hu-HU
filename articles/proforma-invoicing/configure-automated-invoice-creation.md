---
title: Automatikus számlalétrehozás konfigurálása
description: Ez a témakör a rendszer számlák automatikus létrehozásához történő konfigurálásáról tartalmaz információkat.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287916"
---
# <a name="configure-automatic-invoice-creation"></a>Automatikus számlalétrehozás konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_


Ha automatikus számla futtatását szeretnó konfigurálni a Dynamics 365 Project Operations alkalmazásban, hajtsa végre a következő lépéseket.

1. Lépjen a **Beállítások** > **Kötegelt feladatok** menüpontra.
2. Hozzon létre egy kötegelt feladatot, és adja neki a **Project operations számlák létrehozása** nevet. A kötegelt feladat nevének tartalmaznia kell a „számlák létrehozása” szavakat.
3. A **Feladat típusa** mezőben válassza a **Nincs** lehetőséget. Alapértelmezés szerint a **Napi gyakoriság** és az **Aktív** opciók értéke **Igen**.
4. Válassza a **Munkamenet futtatása** lehetőséget. A **Rekord keresése** párbeszédpanelen három munkafolyamatot láthat:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Válassza a **ProcessRunCaller** elemet, majd a **Hozzáadás** lehetőséget.
6. A következő párbeszédpanelen válassza az **OK** lehetőséget. Az **Alvás** munkafolyamatot egy **Folyamat** munkafolyamat követi.

  > [!NOTE]
  > Az 5. lépésben a **ProcessRunner** lehetőséget is választhatja. Ezt követően, ha az **OK** lehetőséget választja, a **Folyamat** munkafolyamatot egy **Alvás** munkafolyamat követi.

A **ProcessRunCaller** és a **ProcessRunner** munkafolyamatok számlákat hoznak létre. **A ProcessRunCaller** munkafolyamat meghívja a **ProcessRunner** munkafolyamatot. A **ProcessRunner** az a munkafolyamat, amely ténylegesen létrehozza a számlákat. Végighalad az összes szerződési soron, amelyhez számlákat kell létrehozni, és számlákat hoz létre ezekre a sorokhoz. Azon szerződési sorok meghatározásához, amelyekhez számlákat kell létrehozni, a feladat megvizsgálja a szerződési sorok számlafuttatási dátumait. Ha az adott szerződéshez tartozó szerződési sorok egyazon számlafuttatási dátummal rendelkeznek, a tranzakciók egyetlen számlába kerülnek egyesítésre, amely két számlasorral fog rendelkezni. Ha nincsenek tranzakciók a számlák létrehozására, akkor a feladat kihagyja a számla létrehozását.

Miután a **ProcessRunner** munkafolyamat futtatása befejeződött, meghívja a **ProcessRunCaller** munkafolyamatot, megadja a befejezési időt, és bezáródik. A **ProcessRunCaller** ezután elindít egy időzítőt, amely a megadott befejezési időtől kezdve 24 órán át működik. Az időzítő végén a **ProcessRunCaller** bezáródik.

A számlák létrehozására szolgáló kötegelt folyamat feladat ismétlődő feladat. Ha ezt a kötegelt folyamatot többször futtatja, akkor a feladatból több példány jön létre, és hibákat okoz. Ezért a kötegelt folyamatot csak egyszer kell elindítania, és csak akkor kell újraindítania, ha az leáll.

> [!NOTE]
> A kötegelt számlázás csak a számlázási ütemezések szerint konfigurált projektek szerződéssoraihoz fut. A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges. Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását. Ugyanez érvényes a projektalapú szerződéssor esetében is.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]