---
title: Projekttámogatások
description: Ez a cikk elmagyarázza, hogyan hozhat létre és módosíthat egy támogatást.
author: RadhikaRS
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 40357bdfb74b6afdb26663e6439f90e762b79029
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913623"
---
# <a name="project-grants"></a>Projekttámogatások

[!include [banner](../includes/banner.md)]

A támogatás egy adott célra vagy projektre vonatkozó pénzajándék. Általában vannak olyan korlátozások, amelyekkel a támogatás elkölthető. A projektmenedzsment és a könyvelés során megadhatja és nyomon követheti a támogatásokat, és meghatározhatja a projektekre és a projektszerződésekre vonatkozó kapcsolatokat. Például az alábbi feladatokat elvégezheti:

- A támogatások projektekkel és finanszírozási forrásokkal történő társítása a **projekt** és a **projekt szerződés részletei** oldalaira mutató hivatkozások segítségével.
- Adja meg és kövesse nyomon a támogatás változásait, ahogy az egyik állapotból a másikba költözik.
- Adja meg és kövesse nyomon a költségeket, a kért összegeket és a díjazott összegeket.
- Hozzon létre fő támogatásokat, és társítson hozzájuk altámogatásokat.

A támogatást létrehozhatja egy új rekord összes adatának megadásával, illetve a részletek átmásolásával egy meglévő támogatásból, majd frissítheti azokat.

## <a name="create-a-new-grant"></a>Új támogatás létrehozása

1. Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.
2. Válassza az **Új** \> **Támogatás** lehetőséget.
3. A támogatás részletei lap **általános** gyorslapján, a **támogatási azonosító** mezőben adja meg a támogatás alfanumerikus azonosítóját.
4. A **Támogatás neve** mezőben adjon egy egyedi nevet a támogatásnak.
5. A **Leírás** mezőben adja meg az új támogatás részleteit.

    Az oldal többi mezőjének nagy része nem kötelezően kitöltendő, és a kívánt módon annyi adatot ad meg, amennyit szeretne.

    A következő felsorolás a támogatási részletek oldal egyes gyorslapján megadott információkat ismerteti:

    - **Általános** – adja meg a támogatás nevét, az állapotot, a megnevezést, a célt és az összeget.
    - **Kapcsolatfelvételi adatok** – adja meg a munkatársakra vonatkozó adatokat, a támogatást kezelő részleget, valamint a támogatás ügyfél vagy a támogatás szervezeti forrását. Azt is megadhatja, hogy a szervezet átadó entitás-e, amely megkapja a támogatást, majd átadja egy másik címzettnek. Válassza a **Hozzáadás** lehetőséget a kapcsolattartói adatok (például telefonszámok és e-mail-címek) hozzáadásához a támogatást biztosító szervezet számára.
    - **Dátumok és határidők** – adja meg a támogatáshoz és a támogatási kérelemhez kapcsolódó időpontokat. A példák közé tartozik a pályázat határideje, a beküldési dátum, valamint a támogatás jóváhagyása vagy elutasítása.
    - **Társított projektek és projektszerződések** – csak akkor adhat meg adatokat ezen a gyorslapon, ha az **Általános** gyorslapon a **támogatási állapot** mező **aktív** vagy **Díjazott** értékre van állítva. A kapcsolódó feladat végrehajtásához válasszon a következő lehetőségek közül:

        - **Finanszírozási forrás hozzáadása** – új finanszírozási forrás hozzáadása a támogatáshoz. Most megadhatja az összes adatot, vagy használhatja az alapértelmezett adatokat, majd később frissítheti.
        - **Projektszerződés hozzáadása** – projektszerződés adatainak hozzáadása vagy módosítása.
        - **Projekt hozzáadása** – a projekt részleteinek hozzáadása vagy módosítása.

    - **Beállítás** – adja meg a megfelelő alapok adatait, ha ez szükséges. A támogatásokat odaítélő szervezetek közül sokak számára szükséges, hogy a támogatottak saját pénzük vagy erőforrásaik adott összegét költsék el, amely megfelel a támogatásban odaítélt összegnek. A **helyi projekt- vagy követési azonosító** mezőben megadhat egy azonosítót, amely eltér a projekt azonosítójától.

        > [!NOTE]
        > Ha a támogatás egy részét egy másik szervezetnek ítélik oda, akkor állítsa a **Résztámogató** értéket **Igen** értékre. Az Egyesült Államokban odaítélt támogatások esetében megadhatja, hogy a támogatást állami megbízás vagy szövetségi megbízás alapján ítélik-e oda.

    - **Lehívási adatok** – információ hozzáadása vagy frissítése arról, hogy milyen gyakran hívhatók le a támogatási pénzalapok, milyen gyakran számlázhatók vagy költhetők.

## <a name="create-a-new-grant-from-a-copy"></a>Új támogatás létrehozása másolatból

1. Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.
2. Válassza az **Új** \> **Másolat támogatásból** lehetőséget.
3. Adja meg az új támogatás alfanumerikus azonosítóját és nevét, majd kattintson az **OK** gombra.
4. A támogatás részletei lapon tekintse át a másolt támogatás részleteit, és végezze el a szükséges módosításokat. A lapon található mezők nagy része nem kötelező.

## <a name="view-or-modify-grant-details"></a>A támogatási adatok megtekintése vagy módosítása

1. Lépjen a **Projektvezetés és könyvelés** \> **Támogatások** \> **Támogatások** elemre.
2. Válassza ki a módosítani kívánt támogatást.
3. A Műveleti ablaktáblán a **Támogatás** lapon, a **Karbantartás** csoportban válassza a **Szerkesztés** lehetőséget.
4. Tekintse át a támogatási adatokat, és végezze el a szükséges módosításokat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]