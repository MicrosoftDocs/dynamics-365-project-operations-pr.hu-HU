---
title: A Project Operations bemutató adatainak alkalmazása a Finance felhőben szolgáltatott környezetbe
description: Ez a témakör ismerteti, hogyan lehet alkalmazni a Project Operations bemutató adatait a Dynamics 365 Finance felhőben szolgáltatott környezetre.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948915"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>A Project Operations bemutató adatainak alkalmazása a Finance felhőben szolgáltatott környezetbe

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

>[Fontos] Ez a témakör csak a Microsoft Dynamics 365 Finance 10.0.13-as verziója esetében alkalmazható, és csak felhőben üzemeltetett környezeten hajtható végre. A minőségi frissítések környezetbe való alkalmazása **ELŐTT** hajtsa végre a témakör lépéseit.

1. Az LCS-projektben nyissa meg a **Környezet részletei** oldalt. Figyelje meg, hogy tartalmazza a környezethez a távoli asztali protokoll (RDP) használatával való kapcsolódáshoz szükséges adatokat.

![A  környezetek részletei](./media/1EnvironmentDetails.png)

A kiemelt hitelesítő adatok első csoportja a helyi fiók hitelesítő adatai, és a távoli asztali kapcsolatra mutató hivatkozást tartalmaz. A hitelesítő adatok tartalmazzák a környezet rendszergazdai felhasználónevét és jelszavát. A hitelesítő adatok második csoportja az SQL Server alkalmazásba való belépésre szolgál ebben a környezetben.

2. Kapcsolódjon távolról a környezethez a **Helyi fiókok** hivatkozással, és használja a **Helyi fiók hitelesítő adatait** a hitelesítéshez.
3. Nyissa meg az **Internet Information Services** > **Alkalmazáskészletek** > **AOSService** részt, és állítsa le a szolgáltatást. Ezen a ponton leállítja a szolgáltatást, hogy folytathassa az SQL adatbázis cseréjét.

![AOS leállítása](./media/2StopAOS.png)

4. Nyissa meg a **Szolgáltatások** részt, és állítsa le a következő két elemet:

- Microsoft Dynamics 365 Unified Operations : Kötegkezelő szolgáltatás
- Microsoft Dynamics 365 Unified Operations: Adatimportálási és -exportálási keretrendszer

![Szolgáltatások leállítása](./media/3StopServices.png)

5. Nyissa meg a Microsoft SQL Server Management Studio alkalmazást. Jelentkezzen be az SQL-szerver hitelesítő adataival, és használja az axdbadmin felhasználót és jelszót az LCS **Környezetek részletei** oldaláról.

![SQL Server Management Studio](./media/4SSMS.png)

6. Az objektumtallózó **Adatbázisok** részén keresse meg az **AXDB** elemet. Az adatbázist egy új adatbázissal helyettesíti, amely a [letöltőközpontban](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) található. 
7. Másolja a zip-fájlt a virtuális gépre, és csomagolja ki a zip-tartalmat.
8. Az SQL Server Management Studio alkalmazásban kattintson a jobb gombbal az **AxDB** elemre, majd válassza a **Feladatok** > **Visszaállítás** > **Adatbázis** lehetőséget.

![Adatbázis visszaállítása](./media/5RestoreDatabase.png)

9. Válassza a **Forráseszköz** lehetőséget, és keresse meg a másolt zip-ből kibontott fájlt.

![Forráseszközök](./media/6SourceDevice.png)

10. Válassza a **Beállítások** lehetőséget, majd válassza a **Meglévő adatbázis felülírása** és a **Céladatbázissal meglévő kapcsolatok lezárása** lehetőséget. 
11. Kattintson az **OK** gombra.

![Beállítások visszaállítása](./media/7RestoreSetting.png)

A rendszer megerősíti, hogy az AXDB-visszaállítás sikeresen megtörtént. A visszaigazolás kézhezvételét követően lezárhatja az SQL Services Management Studio alkalmazást.

12. Lépjen vissza az **Internet Information Services** > **Alkalmazáskészletek** > **AOSService** részhez, és indítsa el az AOSService alkalmazást.
13. Nyissa meg a **Szolgáltatások** részt, és indítsa el a korábban leállított két szolgáltatást.

14. Keresse meg az AdminUserProvisioning eszközt ezen a virtuális gépen. Keresse a K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe alatt.
15. Futtassa a .ext-fájlt a saját felhasználói címét használva az **E-mail-cím** mezőben. 
16. Válassza a **Küldés** lehetőséget.

![Rendszergazdai felhasználó átadása](./media/8AdminUserProvisioning.png)

Ez pár percet is igénybe vehet. Kapnia egy megerősítő üzenetet, hogy a rendszergazdai felhasználó sikeresen frissítve lett.

17. Végül, futtassa a parancssort rendszergazdaként az iisreset végrehajtásához

![IIS alaphelyzetbe állítás](./media/9IISReset.png)

18. Zárja be a távoli asztali munkamenetet, és az LCS **Környezet részletei** oldal használatával lépjen be a környezetbe, és ellenőrizze, hogy az a várt módon működik.

![Finance and Operations](./media/10FinanceAndOperations.png)
