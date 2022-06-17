---
title: Projektidő-beviteli mobil munkaterület
description: Ez a cikk a Projekt időbevitel mobil munkaterületéről nyújt tájékoztatást. Ez a munkaterület lehetővé teszi, hogy a felhasználók a mobileszköz segítségével időt adjanak meg és mentsenek a projekthez.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: a163e32dae0231b5d71d1de2dbb473593b989164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919541"
---
# <a name="project-time-entry-mobile-workspace"></a>Projektidő-beviteli mobil munkaterület

[!include [banner](../includes/banner.md)]

Ez a cikk a **Projekt időbevitel** mobil munkaterületéről nyújt tájékoztatást. Ez a munkaterület lehetővé teszi, hogy a felhasználók a mobileszköz segítségével időt adjanak meg és mentsenek a projekthez.

Ez a mobil munkaterület a Dynamics 365 Unified Ops mobilalkalmazással való használatra készült. 

## <a name="overview"></a>Áttekintés
A napi munkájuk részeként a projektek erőforrásai gyakran vannak helyszínen vagy utaznak. A **Projektidő-beviteli** mobil munkaterület lehetővé teszi, hogy a felhasználók a kiválasztott mobileszközön bevigyék egy projekthez tartozó számlázható vagy nem számlázható idejüket. Ezért a projekterőforrások bármikor és bárhol rögzíthetik az időbejegyzéseket. Emellett megtekinthetik a már rögzített időbejegyzéseket is. 

A **Projektidő-beviteli** mobil munkaterületen a felhasználók konkrétan a következő feladatokat végezhetik el:

-   A kiválasztott dátumnál adja meg az adott feladatra fordított órák számát.
-   Kereshet projekt neve vagy ügyfél alapján, hogy megtalálja a projektet, amelyhez időt kíván megadni.
-   Meghatározhatja a felhasznált idő kategóriáját és tevékenységét.
-   Rögzítse az időt számlázhatóként vagy nem számlázhatóként a projekt számára.
-   Opcionálisan megadhat külső és belső megjegyzéseket.

## <a name="prerequisites"></a>Előfeltételek
Az előfeltételek eltérnek a szervezetnél telepített Microsoft Dynamics 365 verziójától függően.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Előfeltételek, ha Dynamics 365 Finance
Ha a szervezetnél Finance van telepítve, a rendszergazdának közzé kell tennie a **Projektidő-beviteli** mobil munkaterületet. További információk: [Mobil munkaterület közzététele](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Előfeltételek, ha az 1611-es verziót használja a 3. vagy újabb platformfrissítéssel
Ha a z 1611-es verzió van telepítve a szervezeténél a 3. vagy újabb platformfrissítéssel, akkor a rendszergazdának a következő előfeltételeket kell elvégeznie. 

<table>
<thead>
<tr class="header">
<th>Előfeltétel</th>
<th>Szerepkör</th>
<th>Ismertetés</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Telepítse a KB 4018050 elemet.</td>
<td>Rendszergazda</td>
<td>A KB 4018050 egy X++-frissítés vagy -metaadat-gyorsjavítás, amely a <strong>Projektidő-beviteli</strong> mobil munkaterületet tartalmazza. A KB 4018050 megvalósításához a rendszergazdának az alábbi lépéseket kell követnie.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Töltse le a metaadat-gyorsjavítást a Microsoft Dynamics Lifecycle Services (LCS) szolgáltatásból</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Telepítse a metaadat-gyorsjavítást</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Hozzon létre egy telepíthető csomagot,</a> amely tartalmazza az <strong>ApplicationSuite</strong> és <strong>ProjectMobile</strong> modelleket, majd töltse fel a telepíthető csomagokat az LCS-re.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Alkalmazza a telepíthető csomagot</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Tegye közzé a <strong>Projektidő-beviteli</strong> mobil munkaterületet.</td>
<td>Rendszergazda</td>
<td>Lásd: <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil munkaterület közzététele</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilalkalmazás letöltése és telepítése

Töltse le és telepítse a Finance and Operations mobilalkalmazást:

-   [Android rendszerű telefonokhoz](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone-okhoz](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bejelentkezés a mobilalkalmazásba
1.  Indítsa el az alkalmazást a mobileszközén.
2.  Írja be a Dynamics 365 URL-címét.
3.  Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát. Adja meg a hitelesítő adatait.
4.  A bejelentkezés után megjelennek a vállalata számára elérhető munkaterületek. Ne feledje, hogy ha a rendszergazda később új munkaterületet tesz közzé, akkor frissítenie kell a mobil munkaterületek listáját.

[![Frissítés húzással.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Idő megadása a Projektidő-beviteli mobil munkaterület használatával
1.  A mobileszközön jelölje ki a **Projektidő-beviteli** munkaterületet.
2.  Válassza az **Időbevitel** elemet. A rendszer megjeleníti az aktuális hét naptári dátumait.
3.  A kiválasztott dátumnál válassza a **Művelet** &gt; **Új bejegyzés** lehetőséget.
4.  Adja meg a rögzítendő órák számát.
5.  Válassza ki a projektet az időbevitelhez. A listák az alkalmazásba offline használat céljából betöltött projekteket jelenítik meg. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. További tudnivalókért lásd: [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Ha a projekt nem szerepel a listában, akkor válassza a **Keresés** lehetőséget. Keressen név szerint, vagy váltson át projektnév vagy ügyfél szerinti keresésre.
7.  Válasszon ki egy kategóriát. A listák az alkalmazásba offline használat céljából betöltött kategóriákat jelenítik meg. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. További tudnivalókért lásd: [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Ha a kategória nem szerepel a listában, akkor válassza a **Keresés** lehetőséget. Keressen kategória szerint, vagy váltson a kategórianév szerint történő keresésre.
9.  Válasszon egy tevékenységet. A listák az alkalmazásba offline használat céljából betöltött tevékenységeket jelenítik meg. Alapértelmezés szerint 50 elem van betöltve, de a fejlesztők megváltoztathatják ezt a számot. További tudnivalókért lásd: [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Ha a tevékenység nem szerepel a listában, akkor válassza a **Keresés** lehetőséget. Keressen a tevékenység száma alapján, vagy váltson át cél szerinti keresésre.

11. Válassza ki a sortulajdonságot.
12. Opcionális: Megadhat külső és belső megjegyzéseket.
13. Válassza a **Kész** lehetőséget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]