---
title: Költségekkel kapcsolatos mobilalkalmazás
description: Ez a cikk a Költségkezelés mobil munkaterületről nyújt tájékoztatást.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ba7ccae04fbb02252e3ceb01f123ce1e85375b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930229"
---
# <a name="mobile-expense-app"></a>Költségekkel kapcsolatos mobilalkalmazás

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a cikk a **Költségkezelés** mobil munkaterületről nyújt tájékoztatást. A munkaterület lehetővé teszi, hogy a felhasználók rögzítsék és feltöltsék a nyugtákat, amelyeket így a későbbiekben csatolni lehet a költségjelentésekhez. Csatolt nyugtákkal a felhasználók költségsorokat is gyorsan hozhatnak létre, illetve létrehozhatják és kezelhetik a költségjelentéseiket. A jóváhagyók ezenkívül a **Költségkezelés** mobilos munkaterületen megtekinthetik, jóváhagyhatják vagy elutasíthatják a hozzájuk rendelt költségjelentésket.

Ez a mobil munkaterület a Dynamics 365 Unified Ops mobilalkalmazással való használatra készült.

Számos szervezetnél kötelezően csatolni kell a nyugtákat az olyan, utazáshoz vagy az üzleti tevékenységhez kapcsolódó költségjelentésekhez, amelyeket az alkalmazottak beküldenek a költségtérítési igények leadásakor. A **Költségkezelés** mobilos munkaterületen a felhasználók a nyugta fényképének használatával gyorsan hozhatnak létre új költségsorokat az általuk kiválasztott mobileszközön. Másik lehetőségként a felhasználók fényképet készíthetnek a nyugtáról, majd a képet csatolhatják egy költségjelentéshez. Az alkalmazottak ugyancsak hozhatnak létre és kezelhetnek költségjelentéseket, majd a mobileszközükkel elküldhetik őket jóváhagyásra és így kérhetik a költségek visszatérítését.

A **Költségkezelés** mobilos munkaterületen a következő feladatok hajthatók végre:

- Nyugta fényképének elkészítése. Töltse fel a nyugta képét, és csatolja egy költségjelentéshez.
- Töltse fel a fájlt rögzített nyugtaként. Ezt követően a fájlt csatolhatja egy költségjelentéshez.
- Hozzon létre új költségsort csatolt nyugta használatával. Ezután hozzáadhatja a sortételt egy költségjelentéshez, majd beküldheti jóváhagyásra és visszatérítést kérhet.

A következő funkciók ugyancsak rendelkezésre állnak:

- Hozzon létre új költségjelentést.
- Csatolja a hitelkártya-tranzakciókat és más, korábban létrehozott kiadásokat egy költségjelentéshez.
- Hozzon létre új kiadásokat egy költségjelentéshez.
- Csatoljon nyugtákat a költségjelentés bármilyen költségeihez úgy, hogy fényképet készít a nyugtáról vagy rögzített nyugtát tartalmazó fájlt tölt fel.
- A vállalat költségekre vonatkozó szabályaitól függően adja hozzá a vendégek listáját a költségekhez.
- A vállalat költségekre vonatkozó szabályaitól függően tételezze a költségeket.
- Küldjön be költségjelentés jóváhagyásra és a költségek visszatérítéséhez.
- Hagyja jóvá vagy utasítsa el azokat a költségjelentéseket, amelyeknek Ön a hozzárendelt jóváhagyója.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Előfeltételek, ha Dynamics 365 Finance

Ha a szervezet a Finance rendszert használja, a rendszergazdának közzé kell tennie a **Költségkezelés** mobilos munkaterületet. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>A Dynamics 365 Unified Ops mobilalkalmazás letöltése és telepítése
A Dynamics 365 Unified Ops mobilalkalmazás letöltése és telepítése:

- [Android rendszerű telefonokhoz](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone-okhoz](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bejelentkezés a mobilalkalmazásba
1. Indítsa el az alkalmazást a mobileszközén.
2. Írja be a Dynamics 365 URL-címét.
4. Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát. Adja meg a hitelesítő adatait.
5. A bejelentkezés után megjelennek a vállalata számára elérhető munkaterületek. Ha a rendszergazda később új munkaterületet tesz közzé, akkor frissítenie kell a mobilos munkaterületek listáját.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Nyugta rögzítése a Költségkezelés mobilos munkaterülettel

1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Nyugta rögzítése** lehetőséget.
3. Válassza a **Fénykép készítése** vagy a **Kép kiválasztása** lehetőséget.
4. Hajtsa végre az alábbi lépések egyikét:

    - Ha a **Fénykép készítése** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

        1. A mobileszköz kamerájával tud fényképet készíteni a nyugtáról. 
        2. Ha elkészült a fénykép, az elfogadásához válassza az **OK** lehetőséget.
        3. Nem kötelező: Adjon nevet a fényképnek, és adjon hozzá megjegyzést.

    - Ha a **Kép kiválasztása** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

        1. A listáról válasszon ki egy képet.
        2. Nem kötelező: Adjon nevet a képnek, és adjon hozzá megjegyzést.

5. Válassza a **Kész** lehetőséget.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Költségek gyors bevitele a Költségkezelés mobilos munkaterülettel

1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Gyors költségbevitel** lehetőséget.
3. Válassza ki a költség kategóriáját. Láthatja az alkalmazásba offline használatra betöltött költségkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a kategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen költségkategória szerint, vagy váltson a költségtípus szerint történő keresésre.
4. Adja meg a költség tranzakciójának dátumát.
5. Nem kötelező: Adja meg a kereskedőt a költséghez.
6. Írja be a költség összegét.
7. Válassza ki a költség pénznemét. Láthatja az alkalmazásba offline használatra betöltött pénznemkódok listáját. Alapértelmezés szerint 400 pénznem van betöltve, de a fejlesztők módosíthatják ezt. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a pénznem nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen pénznem szerint, vagy váltson a név szerint történő keresésre.
8. Válassza a **Fénykép készítése** vagy a **Kép kiválasztása** lehetőséget.
9. Hajtsa végre az alábbi lépések egyikét:

    - Ha a **Fénykép készítése** lehetőséget választotta, a mobileszköz kamerájával tud fényképet készíteni a nyugtáról. Ha elkészült a fénykép, az elfogadásához válassza az **OK** lehetőséget.
    - Ha a **Kép kiválasztása** lehetőséget választotta, válasszon ki egy képet a listából.

10. Válassza a **Kész** lehetőséget.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Költségjelentés jóváhagyása a Költségkezelés mobil munkaterület használatával

1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. A **Kiadások jóváhagyása** részen látható, hogy hány költségjelentést rendeltek Önhöz jóváhagyásra. A szám hozzávetőlegesen 30 percenként frissül. Válassza a **Kiadások jóváhagyása** lehetőséget.

    Megjelenik az Önhöz jóváhagyásra rendelt költségjelentések listája.

3. A költségjelentés kiválasztásával megtekintheti a költség részleteit.
4. A költség részleteinek megtekintéséhez válasszon ki egy költséget. A költséghez megjelenített információk között a nyugták, a vendégek és a tételezés részletei is szerepelnek.
5. A **Költségjelentés** oldalon válassza ki, hogy jóváhagyja-e vagy elutasítja-e a költségjelentést.
6. Adja meg az esetleges megjegyzéseket a jóváhagyási művelethez.
7. Válassza a **Kész** lehetőséget.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Hozzon létre egy új költségjelentést, és küldje el jóváhagyásra a Költségkezelés mobil munkaterület használatával

1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Költségbevitel** lehetőséget.
3. Válassza az **Új jelentés** lehetőséget, vagy válasszon ki egy meglévő költségjelentést a listából.
4. Új költségjelentés esetén adja meg a célt és a rendelkezésre álló további információkat. Ez az információ attól függően változik, hogy a költségkezelés hogy van beállítva a vállalatnál.
5. Válassza a **Kész** lehetőséget.
6. Meglévő költségek (például hitelkártya-tranzakciók) költségjelentéshez való hozzáadásához válassza a **Csatolás** lehetőséget.
7. Válasszon ki egy vagy több költséget a listából.
8. Válassza a **Kész** lehetőséget.
9. Ha új költséget szeretne hozzáadni a költségjelentéshez, válassza az **Új költség** lehetőséget.
10. Válassza ki a költség kategóriáját. Láthatja az alkalmazásba offline használatra betöltött költségkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a kategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen költségkategória szerint, vagy váltson a költségtípus szerint történő keresésre.
11. Nem kötelező: Adja meg a kereskedőt a költséghez.
12. Adja meg a költség tranzakciójának dátumát.
13. Írja be a költség összegét.
14. Válassza ki a költség pénznemét. Láthatja az alkalmazásba offline használatra betöltött pénznemkódok listáját. Alapértelmezés szerint 400 pénznem van betöltve, de a fejlesztők módosíthatják ezt. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a pénznem nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen pénznem szerint, vagy váltson a név szerint történő keresésre.
15. Válassza a **Kész** lehetőséget.
16. Ha további adatokat kíván felvenni a költséghez, válassza a **További részletek hozzáadása** lehetőséget. A rendelkezésre álló mezők a vállalat költségkezelési beállításaitól függenek.
17. Ha a vállalati szabályzat értelmében nyugtát kell csatolni a költséghez, akkor válassza a **Nyugták** lehetőséget, majd hajtsa végre a következő lépéseket:

    1. Válassza a **Nyugta rögzítése** vagy a **Nyugta csatolása** lehetőséget.
    2. Hajtsa végre az alábbi lépések egyikét:

        - Ha a **Nyugta rögzítése** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Válassza a **Fénykép készítése** vagy a **Kép kiválasztása** lehetőséget.
            2. Hajtsa végre az alábbi lépések egyikét:

                - Ha a **Fénykép készítése** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

                    1. A mobileszköz kamerájával tud fényképet készíteni a nyugtáról. Ha elkészült a fénykép, az elfogadásához válassza az **OK** lehetőséget.
                    2. Nem kötelező: Adjon nevet a fényképnek, és adjon hozzá megjegyzést.

                - Ha a **Kép kiválasztása** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

                    1. A listáról válasszon ki egy képet.
                    2. Nem kötelező: Adjon nevet a képnek, és adjon hozzá megjegyzést.

            3. Válassza a **Kész** lehetőséget.

        - Ha a **Nyugta csatolása** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Válasszon ki egy vagy több képet a listából.
            2. Válassza a **Kész** lehetőséget.

    3. A **Vissza** gombbal térjen vissza a költség részleteihez.

18. Ha a vállalati szabályzat értelmében vendégeket kell csatolni a költséghez, akkor válassza a **Vendégek** lehetőséget, majd hajtsa végre a következő lépéseket:

    1. Válassza a **Vendég**, a **Korábbi vendégek** vagy a **Munkatársak** lehetőséget.
    2. Hajtsa végre az alábbi lépések egyikét:

        - Ha a **Vendég** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Adja meg a vendég nevét.
            2. Nem kötelező: Adja meg a vendég szervezetét és/vagy országát.
            3. Nem kötelező: Adja meg a vendég titulusát.
            4. Válassza a **Kész** lehetőséget.

        - Ha a **Korábbi vendégek** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Válasszon ki egy vagy több korábbi vendéget a listából. Láthatja az alkalmazásba offline használatra betöltött korábbi költségjelentésekhez hozzáadott korábbi vendégek listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a korábbi vendég nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen név szerint, vagy váltson át szervezet, ország vagy titulus szerinti keresésre.
            2. Válassza a **Kész** lehetőséget.

        - Ha a **Munkatársak** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Válasszon ki egy vagy több munkatársat a listából. Láthatja az alkalmazásba offline használatra betöltött munkatársak listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha a munkatárs nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen név szerint, vagy váltson át vállalat vagy titulus szerinti keresésre.
            2. Válassza a **Kész** lehetőséget.

    3. A **Vissza** gombbal térjen vissza a költség részleteihez.

19. Ha a vállalati szabályzat értelmében a költséget tételezni kell, akkor válassza a **Tételezés** lehetőséget, majd hajtsa végre a következő lépéseket:

    1. Válassza ki az első tételezendő dátumot.
    2. Válassza a **Tételezés hozzáadása** lehetőséget.
    3. Válassza ki a költségtételezés alkategóriáját. Láthatja az alkalmazásba offline használatra betöltött költség-alkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) című cikkben találnak további információt. Ha az alkategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen a költség alkategóriájának neve szerint.
    4. Adja meg a tételehéshez tartozó tranzakciós összeget.
    5. Ha szükséges, módosítsa a tranzakció dátumát.
    6. Válassza a **Kész** lehetőséget.
    7. Ismételje meg újra az előző lépéseket, amíg hozzá nem adja a kijelölt dátumhoz tartozó összes tételezést.
    8. További napok esetén a **Másolás a következő napra** lehetőséggel másolhatja át a tételezéseket a következő napra. Másik lehetőségként kiválaszthatja a tételezés dátumát, majd ugyanúgy hozzáadhatja a tételezéseket, ahogy az első dátum esetében tette.
    9. Miután befejezte a költség tételezését, a **Vissza** gombra kattintva térjen vissza a költség részleteihez.

20. A **Vissza** gombbal térjen vissza a **Költségjelentés** oldalra.
21. Ismételje meg az előző lépéseket, amíg hozzá nem adott minden költséget.
22. Válassza a **Küldés** lehetőséget.
23. Adja meg a jóváhagyó számára az esetleges megjegyzéseket.
24. Válassza a **Kész** lehetőséget.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Miért nem adja meg alapértelmezés szerint az Expense mobilalkalmazás a fizetési módot?

A szervezetek testre szabhatják az **Alapértelmezett fizetési mód** beállítást az egyes költségkategóriákhoz a létrehozásukkor. Ezenkívül a fizetési módok beállításakor beállíthatja az **Alapértelmezett fizetési mód** mezőt Csak importálás **értékre**.

Ha **a csak** importálás engedélyezve van egy fizetési módhoz, a rendszer alapértelmezés szerint nem adja meg a fizetési módot. Üres lesz azokban a költségkategóriákban, ahol ez a fizetési mód be van állítva. Ez a viselkedés mind a webes, mind a mobilos élményben konzisztens.
    
Ha **a csak** importálás nincs engedélyezve egy fizetési módhoz, a rendszer alapértelmezés szerint megadja a beállított értéket azoknál a költségkategóriáknál, ahol ez a fizetési mód be van állítva. Van azonban egy ismert probléma, amely miatt az alapértelmezett érték nincs megadva az Expense mobilalkalmazásban. A probléma megoldásához manuálisan válasszon ki egy fizetési módot a költségjelentés mentése előtt. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Miért nem tudok pénzügyi dimenziókat hozzáadni vagy szerkeszteni az Expense mobilalkalmazásban?

A dimenziók és eloszlások bevitele nem támogatott. A korlátozás megkerüléséhez ezeket a mezőket alapértelmezés szerint beállíthatja a mobilalkalmazásban a projektenkénti vagy alkalmazotti alapértelmezett pénzügyi dimenziók beállításával.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Miért látok néha szinkronizálási hibát az Expense mobilalkalmazásban?

Ha a költségsorok nem felelnek meg a szabályzat követelményeinek, és a felhasználó a szabályzat figyelmeztetésének kezelése nélkül küldi el a költségjelentést, a rendszer nem szinkronizálja a mobiladatokat a kiszolgálóval, és szinkronizálási hiba lép fel. A szinkronizálási hiba bekövetkezte után elküldött összes költségjelentés sikertelen állapotban marad, és több szinkronizálási hibát okoz. A helyzet megoldásának egyetlen módja a szinkronizálási értesítések manuális törlése. A rendszer úgy hárította el a problémát, hogy leállította a költségjelentések benyújtását, ha a házirend-figyelmeztetéseket nem oldották meg, így elkerülhetők a szinkronizálási hibák.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Miért nem jelenik meg megfelelően a projekt- és kategóriaérvényesítés az Expense mobilalkalmazásban?

Ez az érvényesítés jelenleg nem támogatott. A jövőben azonban támogatásra kerülhet sor. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Milyen dokumentumtípusokat támogat a Költség mobilalkalmazás?

Az Expense mobilalkalmazás csak a képeket támogatja. Jelenleg nem támogatja a PDF-eket vagy más dokumentumokat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
