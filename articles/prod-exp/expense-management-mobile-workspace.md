---
title: Költségkezelés mobil munkaterület
description: Ez a témakör a Költségkezelés mobilos munkaterület használatáról nyújt információkat. A munkaterület lehetővé teszi, hogy a felhasználók rögzítsék és feltöltsék a nyugtákat, amelyeket így a későbbiekben csatolni lehet a költségjelentésekhez. Csatolt nyugtákkal a felhasználók költségsorokat is gyorsan hozhatnak létre, illetve létrehozhatják és kezelhetik a költségjelentéseiket.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6d577861a6ebfae55b64a8a06143256e0f1ff40
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960475"
---
# <a name="expense-management-mobile-workspace"></a>Költségkezelés mobil munkaterület

Ez a témakör a **Költségkezelés** mobilos munkaterület használatáról nyújt információkat. A munkaterület lehetővé teszi, hogy a felhasználók rögzítsék és feltöltsék a nyugtákat, amelyeket így a későbbiekben csatolni lehet a költségjelentésekhez. Csatolt nyugtákkal a felhasználók költségsorokat is gyorsan hozhatnak létre, illetve létrehozhatják és kezelhetik a költségjelentéseiket. A jóváhagyók ezenkívül a **Költségkezelés** mobilos munkaterületen megtekinthetik, jóváhagyhatják vagy elutasíthatják a hozzájuk rendelt költségjelentésket.


Ez a mobil munkaterület a Dynamics 365 Unified Ops mobilalkalmazással való használatra készült.


## <a name="overview"></a>Áttekintés

Számos szervezetnél kötelezően csatolni kell a nyugtákat az olyan, utazáshoz vagy az üzleti tevékenységhez kapcsolódó költségjelentésekhez, amelyeket az alkalmazottak beküldenek a költségtérítési igények leadásakor. A **Költségkezelés** mobilos munkaterületen a felhasználók a nyugta fényképének használatával gyorsan hozhatnak létre új költségsorokat az általuk kiválasztott mobileszközön. Másik lehetőségként a felhasználók fényképet készíthetnek a nyugtáról, majd a képet csatolhatják egy költségjelentéshez. Az alkalmazottak ugyancsak hozhatnak létre és kezelhetnek költségjelentéseket, majd a mobileszközükkel elküldhetik őket jóváhagyásra és így kérhetik a költségek visszatérítését.


A **Költségkezelés** mobilos munkaterületen a következő feladatok hajthatók végre:

- Készítsen fényképet a nyugtáról, és töltse fel a Dynamics 365 Finance alkalmazásba. Ezt követően a fotót csatolhatja egy költségjelentéshez.
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

## <a name="prerequisites"></a>Előfeltételek
Az előfeltételek a szervezetnél használt verziótól függően eltérnek.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Előfeltételek a Dynamics 365 Finance használata esetén 
Ha a szervezet a Finance rendszert használja, a rendszergazdának közzé kell tennie a **Költségkezelés** mobilos munkaterületet. További információk: [Mobil munkaterületek közzététele](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Előfeltételek az 1611-es verzió 3. vagy újabb platformfrissítéssel való használata esetén
Ha a szervezet az 1611-es verziót telepítette 3. vagy újabb platformfrissítéssel, akkor a rendszergazdának a következő előzetes műveleteket kell elvégeznie. 

<table>
<thead>
<tr class="header">
<th>Előfeltétel</th>
<th>Szerepkör</th>
<th>Adatfolyam leírása</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Telepítse a KB 4019015 elemet.</td>
<td>Rendszergazda</td>
<td>A KB 4019015 olyan X++-frissítés vagy -metaadat-gyorsjavítás, amely a <strong>Költségkezelés</strong> mobilos munkaterületet tartalmazza. A KB 4019015 megvalósításához a rendszergazdának az alábbi lépéseket kell követnie.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Töltse le a metaadat-gyorsjavítást a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Telepítse a metaadat-gyorsjavítást</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Hozzon létre egy olyan telepíthető csomagot,</a> amely tartalmazza az <strong>ApplicationSuite</strong> és az <strong>ExpenseMobile</strong> modellt, majd töltse fel a telepíthető csomagokat az LCS-re.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Alkalmazza a telepíthető csomagot</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Tegye közzé a <strong>Költségkezelés</strong> mobilos munkaterületet.</td>
<td>Rendszergazda</td>
<td>Lásd: <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil munkaterület közzététele</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>A Dynamics 365 for Operations mobilalkalmazás letöltése és telepítése
A Dynamics 365 Unified Ops mobilalkalmazás letöltése és telepítése:

- [Android rendszerű telefonokhoz](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone-okhoz](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bejelentkezés a mobilalkalmazásba
1. Indítsa el az alkalmazást a mobileszközén.
2. Írja be a Dynamics 365 URL-címét.
4. Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát. Adja meg a hitelesítő adatait.
5. A bejelentkezés után megjelennek a vállalata számára elérhető munkaterületek. Ne feledje, hogy ha a rendszergazda később új munkaterületet tesz közzé, akkor frissítenie kell a mobil munkaterületek listáját.


[![Frissítés húzással](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Nyugta rögzítése a Költségkezelés mobilos munkaterülettel

1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Nyugta rögzítése** lehetőséget.
3. Válassza a **Fénykép készítése** vagy a **Kép kiválasztása** lehetőséget.
4. Hajtsa végre az alábbi lépések egyikét:

    - Ha a **Fénykép készítése** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

        1. A mobileszköz kamerájával tud fényképet készíteni a nyugtáról. Ha elkészült a fénykép, az elfogadásához válassza az **OK** lehetőséget.
        2. Nem kötelező: Adjon nevet a fényképnek, és adjon hozzá megjegyzést.

    - Ha a **Kép kiválasztása** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

        1. A listáról válasszon ki egy képet.
        2. Nem kötelező: Adjon nevet a képnek, és adjon hozzá megjegyzést.

5. Válassza a **Kész** lehetőséget.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Költségek gyors bevitele a Költségkezelés mobilos munkaterülettel
1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Gyors költségbevitel** lehetőséget.
3. Válassza ki a költség kategóriáját. Láthatja az alkalmazásba offline használatra betöltött költségkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a kategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen költségkategória szerint, vagy váltson a költségtípus szerint történő keresésre.
4. Adja meg a költség tranzakciójának dátumát.
5. Nem kötelező: Adja meg a kereskedőt a költséghez.
6. Írja be a költség összegét.
7. Válassza ki a költség pénznemét. Láthatja az alkalmazásba offline használatra betöltött pénznemkódok listáját. Alapértelmezés szerint 400 pénznem van betöltve, de a fejlesztők módosíthatják ezt. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a pénznem nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen pénznem szerint, vagy váltson a név szerint történő keresésre.
8. Válassza a **Fénykép készítése** vagy a **Kép kiválasztása** lehetőséget.
9. Hajtsa végre az alábbi lépések egyikét:

    - Ha a **Fénykép készítése** lehetőséget választotta, a mobileszköz kamerájával tud fényképet készíteni a nyugtáról. Ha elkészült a fénykép, az elfogadásához válassza az **OK** lehetőséget.
    - Ha a **Kép kiválasztása** lehetőséget választotta, válasszon ki egy képet a listából.

10. Válassza a **Kész** lehetőséget.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Költségjelentés jóváhagyása a Költségkezelés mobilos munkaterület használatával (ha a 2017. júliusi frissítést használja)
1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. A **Kiadások jóváhagyása** részen látható, hogy hány költségjelentést rendeltek Önhöz jóváhagyásra. A szám hozzávetőlegesen 30 percenként frissül. Válassza a **Kiadások jóváhagyása** lehetőséget.

    Megjelenik az Önhöz jóváhagyásra rendelt költségjelentések listája.
    
3. A költségjelentés kiválasztásával megtekintheti a költség részleteit.
4. A költség részleteinek megtekintéséhez válasszon ki egy költséget. A költséghez megjelenített információk között a nyugták, a vendégek és a tételezés részletei is szerepelnek.
5. A **Költségjelentés** oldalon válassza ki, hogy jóváhagyja-e vagy elutasítja-e a költségjelentést.
6. Adja meg az esetleges megjegyzéseket a jóváhagyási művelethez.
7. Válassza a **Kész** lehetőséget.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Új költségjelentés létrehozása és beküldése jóváhagyásra a Költségkezelés mobilos munkaterület használatával (ha a 2017. júliusi frissítést használja)
1. A mobileszközön nyissa meg a **Költségkezelés** munkaterületet.
2. Válassza a **Költségbevitel** lehetőséget.
3. Válassza az **Új jelentés** lehetőséget, vagy válasszon ki egy meglévő költségjelentést a listából.
4. Új költségjelentés esetén adja meg a célt és a rendelkezésre álló további információkat. Ez az információ attól függően változik, hogy a költségkezelés hogy van beállítva a vállalatnál.
5. Válassza a **Kész** lehetőséget.
6. Meglévő költségek (például hitelkártya-tranzakciók) költségjelentéshez való hozzáadásához válassza a **Csatolás** lehetőséget.
7. Válasszon ki egy vagy több költséget a listából.
8. Válassza a **Kész** lehetőséget.
9. Ha új költséget szeretne hozzáadni a költségjelentéshez, válassza az **Új költség** lehetőséget.
10. Válassza ki a költség kategóriáját. Láthatja az alkalmazásba offline használatra betöltött költségkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a kategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen költségkategória szerint, vagy váltson a költségtípus szerint történő keresésre.
11. Nem kötelező: Adja meg a kereskedőt a költséghez.
12. Adja meg a költség tranzakciójának dátumát.
13. Írja be a költség összegét.
14. Válassza ki a költség pénznemét. Láthatja az alkalmazásba offline használatra betöltött pénznemkódok listáját. Alapértelmezés szerint 400 pénznem van betöltve, de a fejlesztők módosíthatják ezt. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a pénznem nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen pénznem szerint, vagy váltson a név szerint történő keresésre.
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

            3.  Válassza a **Kész** lehetőséget.

        - Ha a **Nyugta csatolása** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1.  Válasszon ki egy vagy több képet a listából.
            2.  Válassza a **Kész** lehetőséget.

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

            1. Válasszon ki egy vagy több korábbi vendéget a listából. Láthatja az alkalmazásba offline használatra betöltött korábbi költségjelentésekhez hozzáadott korábbi vendégek listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a korábbi vendég nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen név szerint, vagy váltson át szervezet, ország vagy titulus szerinti keresésre.
            2. Válassza a **Kész** lehetőséget.

        - Ha a **Munkatársak** lehetőséget választotta, hajtsa végre az alábbi lépéseket:

            1. Válasszon ki egy vagy több munkatársat a listából. Láthatja az alkalmazásba offline használatra betöltött munkatársak listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha a munkatárs nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen név szerint, vagy váltson át vállalat vagy titulus szerinti keresésre.
            2. Válassza a **Kész** lehetőséget.

    3. A **Vissza** gombbal térjen vissza a költség részleteihez.

19. Ha a vállalati szabályzat értelmében a költséget tételezni kell, akkor válassza a **Tételezés** lehetőséget, majd hajtsa végre a következő lépéseket:

    1. Válassza ki az első tételezendő dátumot.
    2. Válassza a **Tételezés hozzáadása** lehetőséget.
    3. Válassza ki a költségtételezés alkategóriáját. Láthatja az alkalmazásba offline használatra betöltött költség-alkategóriák listáját. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. A fejlesztők a [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page) című cikkben találnak további információt. Ha az alkategória nem szerepel a listában, akkor az online kereséshez válassza a **Keresés** lehetőséget. Keressen a költség alkategóriájának neve szerint.
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
