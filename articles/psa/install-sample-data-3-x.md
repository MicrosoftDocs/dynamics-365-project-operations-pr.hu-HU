---
title: Mintaadatok telepítése
description: Ez a témakör a Project Service Automation alkalmazásban a mintaadatok telepítésével kapcsolatos tudnivalókat tartalmaz.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 46dbd8d125396baa97537ea5d11c47864558c113
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078157"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="68045-103">A Project Service alkalmazás mintaadatok telepítése</span><span class="sxs-lookup"><span data-stu-id="68045-103">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="68045-104">Saját bemutatókörnyezetének felépítéséhez a Microsoft letölthető mintaadat-csomagokat biztosít, amelyek bemutatják az alkalmazások képességeit.</span><span class="sxs-lookup"><span data-stu-id="68045-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="68045-105">Kétféle mintafájlcsomag létezik:</span><span class="sxs-lookup"><span data-stu-id="68045-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="68045-106">hivatkozási/beállítási adatok</span><span class="sxs-lookup"><span data-stu-id="68045-106">reference/setup data</span></span>
- <span data-ttu-id="68045-107">demóadatok (hivatkozási/beállítási és a tranzakciós adatok, például a munkarendelések és projektek)</span><span class="sxs-lookup"><span data-stu-id="68045-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="68045-108">A minta **referencia** adatcsomagok három különböző csomagban tölthetők le, akár csak a Project Service, vagy csak a Field Service számára is telepíthetők, illetve mindkét alkalmazás mintaadatai egyszerre is telepíthetők.</span><span class="sxs-lookup"><span data-stu-id="68045-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="68045-109">A minta beállítási/referencia adatcsomagok a következők:</span><span class="sxs-lookup"><span data-stu-id="68045-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="68045-110">**V902PSMasterData** - csak Project Service 3.x verzió</span><span class="sxs-lookup"><span data-stu-id="68045-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="68045-111">**V902FSMasterData** - csak Field Service 8.x verzió</span><span class="sxs-lookup"><span data-stu-id="68045-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="68045-112">**V902FPSMasterData** - Field Service 8.x és Project Service 3.x verzió</span><span class="sxs-lookup"><span data-stu-id="68045-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="68045-113">A legújabb **demó** adatcsomag a következő:</span><span class="sxs-lookup"><span data-stu-id="68045-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="68045-114">**FPSDemoData** - Field Service 8.x és Project Service 3.x verzió</span><span class="sxs-lookup"><span data-stu-id="68045-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="68045-115">A telepítési utasítások a szakasz létrehozásához és konfigurálásához a felhasználókban kissé eltérhet, de a többi ugyanaz, mint ez előző [**blogbejegyzésben**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="68045-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="68045-116">A csomag tartalmaz egy korlátozott demó adatkészletet, és telepíteni körülbelül 3 óráig tart.</span><span class="sxs-lookup"><span data-stu-id="68045-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="68045-117">A mintaadatcsomagok csak angolul érhetők el.</span><span class="sxs-lookup"><span data-stu-id="68045-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68045-118">**Nem lehetséges a mintaadatok eltávolítása.**</span><span class="sxs-lookup"><span data-stu-id="68045-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="68045-119">Ezért ezt a csomagokat csak demonstrációs, kiértékelési, oktatási vagy tesztrendszerekre telepítse.</span><span class="sxs-lookup"><span data-stu-id="68045-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="68045-120">Ne feledje, hogy az egy csomag telepítése, majd a másik csomag telepítése nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="68045-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="68045-121">(Ez azt jelenti, akkor nem tudja telepíteni az **FSMasterData** csomag után a **PSMasterData** csomagot, illetve fordítva.) Ha saját a jövőben mindkét alkalmazáshoz szükségük lehet a mintaadatokra, telepítse a **v902FPSMasterData** csomagot.</span><span class="sxs-lookup"><span data-stu-id="68045-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData** , or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="68045-122">Amikor telepíti a mintaadatcsomagok, a telepítési folyamat az alábbi műveleteket hajtja végre:</span><span class="sxs-lookup"><span data-stu-id="68045-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="68045-123">A Project Service, Field Service vagy mindkét alkalmazáshoz használt (amennyiben van) alapértelmezett paramétereket hoz léte, és állít be.</span><span class="sxs-lookup"><span data-stu-id="68045-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="68045-124">Mintaadatokat importál az alkalmazásokhoz, például a foglalható erőforrásokat, az alkalmazás-specifikus szerepköröket, értékesítési és a önköltség árlistákat, szervezeti egységeket értékesítési folyamat bejegyzéseket és más entitásokat a fontos funkciók bemutatásához.</span><span class="sxs-lookup"><span data-stu-id="68045-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="68045-125">A **demóadatok** csomaggal a fentiek és további tranzakciós adatok jelennek meg, például a munkarendelések és a projektek.</span><span class="sxs-lookup"><span data-stu-id="68045-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="68045-126">Kíváncsi, hogy milyen műveleteket demózhat a mintaadatokkal?</span><span class="sxs-lookup"><span data-stu-id="68045-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="68045-127">A Fabrikam Robotics fikcionális esetét alább, a [Műszaki megjegyzések](#technical-notes) részben találja.</span><span class="sxs-lookup"><span data-stu-id="68045-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="68045-128">Ha kérdése van a mintaadatcsomagok telepítéséről [küldjön egy e-mailt az fpsdemodata@microsoft.com címre](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="68045-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="68045-129">Követelmények</span><span class="sxs-lookup"><span data-stu-id="68045-129">Requirements</span></span>

<span data-ttu-id="68045-130">A telepítés protokoll feltételezi, a következőket a célpéldányról (szervezet):</span><span class="sxs-lookup"><span data-stu-id="68045-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="68045-131">Az alapnyelv az angol, és az alappénznem az amerikai dollár (USD,$).</span><span class="sxs-lookup"><span data-stu-id="68045-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="68045-132">A szervezet még nem rendelkezik Project Service vagy Field Service adatokkal, vagy csak az új szervezetekhez tartozó legszükségesebb alapértelmezett adatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="68045-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="68045-133">Az üzleti alkalmazás megfelelő verziója már telepítve van:</span><span class="sxs-lookup"><span data-stu-id="68045-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="68045-134">**A FPSDemoData vagy v902FPSMasterData esetén:** A Field Service 8.x és a Project Service 3.x verziója telepítve van a szervezethez.</span><span class="sxs-lookup"><span data-stu-id="68045-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="68045-135">**A v902PSMasterData:** A Project Service verziója 3.x telepítve van szervezethez.</span><span class="sxs-lookup"><span data-stu-id="68045-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="68045-136">**v902FSMasterData esetében:** A Field Service 8.x verziója telepítve van a szervezethez.</span><span class="sxs-lookup"><span data-stu-id="68045-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="68045-137">Ha a mintaadatokat egy meglévő Project Service és a Field Service próba- vagy a demókörnyezetre kell telepítenie, amelynek már vannak adatai (nem ajánlott), a telepítő biztonsági ellenőrzéseinek felfüggesztése szükséges.</span><span class="sxs-lookup"><span data-stu-id="68045-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="68045-138">További tudnivalókat a lenti műszaki megjegyzések rész tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="68045-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="68045-139">Felkészülés a telepítésre</span><span class="sxs-lookup"><span data-stu-id="68045-139">Prepare for installation</span></span>

<span data-ttu-id="68045-140">A Windows egy újabb verziójával (lehetőleg Windows 10) rendelkező számítógépen futtassa a telepítőprogramot.</span><span class="sxs-lookup"><span data-stu-id="68045-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="68045-141">Úgy kell terveznie, hogy a számítógép kapcsolódva maradjon egy hálózathoz, a telepítés futása **egy óráig** is eltarthat a **beállítási/referencia adatok** esetén.</span><span class="sxs-lookup"><span data-stu-id="68045-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="68045-142">(Általában a a telepítés körülbelül 30 percig tart a **FPSMasterData** esetén, amelynek részei a mindkét alkalmazáshoz való mintaadatok.) Az **FPSDemoData** esetén a telepítés körülbelül **3 óráig** tart.</span><span class="sxs-lookup"><span data-stu-id="68045-142">(Normally the installation takes around 30 minutes for **FPSMasterData** , which includes sample data for both applications.) For the **FPSDemoData** , the installation will take around **3 hours**.</span></span>

<span data-ttu-id="68045-143">A számítógépen ki kell kapcsolni a képernyővédő funkciót.</span><span class="sxs-lookup"><span data-stu-id="68045-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="68045-144">Ellenkező esetben a telepítés munkamenetének hitelesítő adatai elveszhetnek, amikor a képernyővédő bekapcsol (kivéve, ha a munkamenet végig aktív marad).</span><span class="sxs-lookup"><span data-stu-id="68045-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="68045-145">![A képernyőkímélő beállításainak képernyőképe, amikor a képernyővédő ki van kapcsolva](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="68045-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="68045-146">Letöltés és kicsomagolás</span><span class="sxs-lookup"><span data-stu-id="68045-146">Download and unpack</span></span>

<span data-ttu-id="68045-147">A Project Service és a Field Service mintaadatok telepítő terjesztése egy önkicsomagoló végrehajtható fájlban történik.</span><span class="sxs-lookup"><span data-stu-id="68045-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="68045-148">A fájlnevek eltérők lehetnek a mintaadatcsomagtól függően, de egyébként a lépések ugyanazok, függetlenül attól, hogy mely csomagot telepíti.</span><span class="sxs-lookup"><span data-stu-id="68045-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="68045-149">A csomag letöltése után futtassa az .exe fájlt, és fogadja el a feltételeket a tömörített fájl kibontásához.</span><span class="sxs-lookup"><span data-stu-id="68045-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="68045-150">Tömörítse ki a fájl tartalmát a számítógép egy tetszőleges mappájába.</span><span class="sxs-lookup"><span data-stu-id="68045-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="68045-151">Az operációs rendszertől és a biztonsági beállításoktól függően szükség lehet a következő lépések elvégzésére a .zip fájlok fájlt kicsomagolása után:</span><span class="sxs-lookup"><span data-stu-id="68045-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="68045-152">Keresse meg, majd kattintson a jobb gombbal az **FPSDemoData.dll** fájlra a **v902FPSMasterData** / **PackageDeployer_FPSDemoData** mappában.</span><span class="sxs-lookup"><span data-stu-id="68045-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="68045-153">Válassza a **Tiltás feloldása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="68045-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="68045-154">Válassza az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="68045-154">Select **Apply**.</span></span>

4. <span data-ttu-id="68045-155">Kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="68045-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="68045-156">Felhasználók létrehozása vagy konfigurálása</span><span class="sxs-lookup"><span data-stu-id="68045-156">Create or configure users</span></span>

<span data-ttu-id="68045-157">Az **FPSDemoData** csomaghoz hat felhasználó szükséges, míg az **FPSMasterData** csomagokhoz szükséges egy felhasználó.</span><span class="sxs-lookup"><span data-stu-id="68045-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="68045-158">A helyes változatra vonatkozó adatokkal foglalkozzon az Ön mintaadat-csomagjához.</span><span class="sxs-lookup"><span data-stu-id="68045-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="68045-159">Felhasználók létrehozása vagy konfigurálása - beállítási/referencia adatcsomagok</span><span class="sxs-lookup"><span data-stu-id="68045-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="68045-160">Az **FPSMasterData** csomag arra szolgál, hogy egy Spencer Low nevű felhasználót az itt ismertetett beállításokkal telepítsen.</span><span class="sxs-lookup"><span data-stu-id="68045-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="68045-161">A csomag megfelelő telepítéséhez létre kell hoznia (vagy ideiglenesen át kell neveznie) felhasználókat a környezetében, hogy azok megfeleljenek a beérkező mintaadatok konfigurációjának.</span><span class="sxs-lookup"><span data-stu-id="68045-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="68045-162">A felhasználókat létrehozásához vagy konfigurálásához válasza a **Beállítások** > **Biztonság** > **Felhasználók** lehetőséget, és tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="68045-162">To create or configure users, go to **Settings** > **Security** > **Users** , and do the following:</span></span>

1. <span data-ttu-id="68045-163">A UserFullname = „Spencer Low” a felhasználónév „spencerl” ( **kisbetűs** ) a Projektmenedzser és Gyakorlatmenedzser szerepkörökhöz.</span><span class="sxs-lookup"><span data-stu-id="68045-163">Set UserFullname="Spencer Low" with username "spencerl" ( **lowercase** ) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="68045-164">Válassza ki **Spenver Low** felhasználót majd a **Szerepkörök kezelése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="68045-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="68045-165">Keresse meg és jelölje ki a **Rendszergazda** szerepkört, majd válassza az **OK** lehetőséget, hogy rendszergazdai jogokaz adjon Spencer Lownak.</span><span class="sxs-lookup"><span data-stu-id="68045-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="68045-166">Ez a lépés szükséges annak biztosítására, hogy mintarekordok megfelelő felhasználói tulajdonjoggal jöjjenek létre és ezért megfelelően legyenek megjelenítve a nézetek.</span><span class="sxs-lookup"><span data-stu-id="68045-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="68045-167">A letöltött csomagból a adatleképezési fájlját frissítenie kell az alapértelmezett felhasználói környezet e-mail-címeivel.</span><span class="sxs-lookup"><span data-stu-id="68045-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="68045-168">Ehhez nyissa meg a **PkgFolder** mappát, majd keresse és nyissa meg az **ImportUserMapFile.xml** fájlt a Jegyzettömbben (vagy a Visual Studio-val vagy egy másik XML-szerkesztővel).</span><span class="sxs-lookup"><span data-stu-id="68045-168">To do this, open **PkgFolder** , and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="68045-169">Állítsa be a **DefaultUserToMapTo =** mezőt Spencer Low felhasználó e-mail címére.</span><span class="sxs-lookup"><span data-stu-id="68045-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="68045-170">Ha nem használ Spencer Low felhasználót **spencerl** felhasználónévvel, egy további fájlt is frissítenie kell.</span><span class="sxs-lookup"><span data-stu-id="68045-170">If you aren't using Spencer Low with username **spencerl** , you need to update an additional file.</span></span> <span data-ttu-id="68045-171">Nyissa meg a **DemoDataPreImportConfig.xml** fájlt, és keresse meg a **userstocreateandconfigure** címkét.</span><span class="sxs-lookup"><span data-stu-id="68045-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="68045-172">Frissítse a **\<login\>** címkét a Horváth Tamás felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="68045-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="68045-173">További részleteket a lenti [Műszaki megjegyzések](#technical-notes) rész tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="68045-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="68045-174">Felhasználók létrehozása vagy konfigurálása - demó adatcsomag</span><span class="sxs-lookup"><span data-stu-id="68045-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="68045-175">A demó adatcsomaghoz hat felhasználó szükséges.</span><span class="sxs-lookup"><span data-stu-id="68045-175">The demo data package requires six users.</span></span> <span data-ttu-id="68045-176">Hogy a csomag telepítése megfelelő legyen, tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="68045-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="68045-177">Hozzon létre, vagy ideiglenesen nevezze át a felhasználókat, hogy megegyezzenek a bejövő minta datok konfigurációjával úgy, hogy ugorjon a **Beállítások** > **Biztonság** > **Felhasználók** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="68045-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="68045-178">Ezekre a szerepkörökre csak az általános személy-alapú bemutatóknál van szükség.</span><span class="sxs-lookup"><span data-stu-id="68045-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="68045-179">Felhasználó teljes neve = "David So" mint helyszíni szolgáltatási technikus</span><span class="sxs-lookup"><span data-stu-id="68045-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="68045-180">Felhasználó teljes neve = "Jamie Reding" ügyfélszolgálati & helyszíni szolgáltatási diszpécser</span><span class="sxs-lookup"><span data-stu-id="68045-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="68045-181">Felhasználói teljes név = "Molly Clark" mint partnermenedzser</span><span class="sxs-lookup"><span data-stu-id="68045-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="68045-182">Felhasználói teljes név = "Spencer Low" mint gyakorlati és projektmenedzser</span><span class="sxs-lookup"><span data-stu-id="68045-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="68045-183">Felhasználói teljes név = "Veronica Quek" mint csoporttag</span><span class="sxs-lookup"><span data-stu-id="68045-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="68045-184">Felhasználói teljes név = "William Contoso"</span><span class="sxs-lookup"><span data-stu-id="68045-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="68045-185">A demóadatok importálásának céljából rendelje hozzá a fenti hat felhasználóhoz a Rendszergazdai szerepkört, hogy a mintarekordok helyesen importálódjanak.</span><span class="sxs-lookup"><span data-stu-id="68045-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="68045-186">Nyissa meg a **PkgFolder** elemet, majd keresése és nyissa meg a **ImportUserMapFile.xml** fájlt.</span><span class="sxs-lookup"><span data-stu-id="68045-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="68045-187">Frissítse az **Új =** mezőket a rendszerben található megfelelő felhasználók e-mail címéhez.</span><span class="sxs-lookup"><span data-stu-id="68045-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="68045-188">![UserMapFile képernyőképe](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="68045-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="68045-189">Ha a „Spencer Low” teljes nevű felhasználónak más a felhasználói azonosítója, mint a **„spencerl”** , frissítenie kell a kiegészítő fájlt.</span><span class="sxs-lookup"><span data-stu-id="68045-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"** , then you need to update an additional file.</span></span> <span data-ttu-id="68045-190">Nyissa meg a **DemoDataPreImportConfig.xml** fájlt, és keresse meg a **userstocreateandconfigure** címkét.</span><span class="sxs-lookup"><span data-stu-id="68045-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="68045-191">Frissítse a **\<login\>** címkét a loginId azonosítóval (kis-és nagybetűk megkülönböztetésével).</span><span class="sxs-lookup"><span data-stu-id="68045-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="68045-192">Az első felhasználó naptárja (a **userstocreateandconfigure** címkén belül) a munkaórák feltöltésére használatos a demóadatok importálásához szükséges minden foglalható erőforrásra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="68045-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="68045-193">Navigáljon a **Beállítások** > **Biztonság** > **Felhasználók** elemhez, keresse meg az "Spencer Low" felhasználót, és nyissa meg a "Munkaórák" lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="68045-193">Navigate to **Settings** > **Security** > **Users** , find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="68045-194">Módosítsa a meglévő munkaórákat, válassza ki a **Teljes heti ismétlődési minta kezdéstől a befejezésig** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="68045-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="68045-195">Ellenőrizze, hogy a **munkaidő 8:00-17:00-ig (9 óra) tart, hétfőtől péntekig, az időzóna pedig Csendes-óceáni idő (USA és Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="68045-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="68045-196">Ez biztosítja, hogy a projekt és ütemezési tábla megjelenítése az elvártnak megfelelő.</span><span class="sxs-lookup"><span data-stu-id="68045-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="68045-197">**Javaslat:** Érdemes most megfontolni biztonsági másolat készítését a szervezetről arra az esetre ha vissza kellene állítania a kezdő állapotot, ha baj történne a példaadatok telepítése során.</span><span class="sxs-lookup"><span data-stu-id="68045-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="68045-198">További információkért, látogasson el erre az oldalra: [Biztonsági és visszaállítási példányok.](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances)</span><span class="sxs-lookup"><span data-stu-id="68045-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="68045-199">Futtassa a Package Deployer alkalmazást</span><span class="sxs-lookup"><span data-stu-id="68045-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="68045-200">Keresse meg és futtassa a **PackageDeployer.exe** állományt a **v902FPSMasterData** vagy **PackageDeployer_FPSDemoData** mappában.</span><span class="sxs-lookup"><span data-stu-id="68045-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="68045-201">Fogadja el a feltételeket.</span><span class="sxs-lookup"><span data-stu-id="68045-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="68045-202">A következő ablakban:</span><span class="sxs-lookup"><span data-stu-id="68045-202">On the next window:</span></span>

   <span data-ttu-id="68045-203">a.</span><span class="sxs-lookup"><span data-stu-id="68045-203">a.</span></span> <span data-ttu-id="68045-204">Telepítési típus kiválasztása **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="68045-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="68045-205">b.</span><span class="sxs-lookup"><span data-stu-id="68045-205">b.</span></span> <span data-ttu-id="68045-206">Használja a „Felhasználók létrehozása és konfigurálása” helyen létrehozott rendszergazda („spencerl” felhasználónevű „Spencer Low” felhasználó) felhasználónevét és jelszavát.</span><span class="sxs-lookup"><span data-stu-id="68045-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="68045-207">c.</span><span class="sxs-lookup"><span data-stu-id="68045-207">c.</span></span> <span data-ttu-id="68045-208">Győződjön meg arról, hogy a **Rendelkezésre álló szervezetek listájának képernyője** ki van választva.</span><span class="sxs-lookup"><span data-stu-id="68045-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="68045-209">![Képernyőkép az Package Deployer „Elérhető szervezetek listájának megjelenítése” kiválasztott lehetőséget tartalmazó ablakról](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="68045-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="68045-210">Válassza ki azt a szervezetet, ahova a mintaadatokat telepíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="68045-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="68045-211">Válassza a **Következő** lehetőséget. amíg meg nem jelenik a **Bemutatóadatok beállítása** párbeszédpanel.</span><span class="sxs-lookup"><span data-stu-id="68045-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="68045-212">![A bemutatóadatok telepítése állapotablak képernyőfotója](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="68045-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="68045-213">A folytatás előtt fontos tudni, hogy a mintaadatok telepítése akár egy óráig is eltarthat (általában ~ 10 perc).</span><span class="sxs-lookup"><span data-stu-id="68045-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="68045-214">Biztosítsa, hogy a számítógép és a kapcsolódva maradjon a hálózathoz, a telepítési folyamat során, hogy a munkamenet aktív maradjon.</span><span class="sxs-lookup"><span data-stu-id="68045-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="68045-215">Amikor elkészült, kattintson a **Következő** gombra a mintaadatok telepítésének megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="68045-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="68045-216">A mintaadatok betöltése után kattintson a **Befejezés** gombra.</span><span class="sxs-lookup"><span data-stu-id="68045-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="68045-217">A mintaadatok telepítésének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="68045-217">Verify the sample data installation</span></span>

<span data-ttu-id="68045-218">Alapvető ellenőrzésként ellenőrizze, hogy a bejegyzések száma és az entitástípusok Fabrikam Robotics kitalált esetnél megfelelően jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="68045-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="68045-219">A mintaadatok teljesen betöltését követően, jelentkezzen be Spencer Low felhasználóval, és ellenőrizze a következőket:</span><span class="sxs-lookup"><span data-stu-id="68045-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="68045-220">Ha a Project Service alkalmazás telepítve van, lépjen **Project Service** > **Beállítások** > **Árlisták** helyre.</span><span class="sxs-lookup"><span data-stu-id="68045-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="68045-221">Győződjön meg arról, hogy a számlázási díjak és a költségárfolyamok megtalálhatók az egyes országoknak/régióknak megfelelő pénznemben.</span><span class="sxs-lookup"><span data-stu-id="68045-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="68045-222">Ha a Project Service alkalmazás telepítve van, lépjen a **Universal Resource Scheduling** > **Beállítások** > **Szervezeti egységek** helyre.</span><span class="sxs-lookup"><span data-stu-id="68045-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="68045-223">Győződjön meg arról, hogy a megfelelő pénznem lett társítva az önköltségiköltségi árlistához minden egyes szervezeti egységnél (kivéve a város bejegyzések).</span><span class="sxs-lookup"><span data-stu-id="68045-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="68045-224">Ha bármelyik hiányzik, keresse meg és társítsa a megfelelő önköltségi árlistát.</span><span class="sxs-lookup"><span data-stu-id="68045-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="68045-225">Ha a Field Service alkalmazás telepítve van, lépjen **Project Service** > **Beállítások** > **Árlisták** helyre.</span><span class="sxs-lookup"><span data-stu-id="68045-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="68045-226">Ellenőrizze, hogy számlázási díjak és a költségárfolyamok megvannak-e.</span><span class="sxs-lookup"><span data-stu-id="68045-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="68045-227">Nyissa meg **Field Service** > **Beállítások** > **Árlisták** menüt, és ellenőrizze, hogy számlázási díjak és a költségárfolyamok léteznek, a megfelelő pénznemben, minden egyes országhoz/régióhoz az adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="68045-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="68045-228">![Az aktív árlisták képernyőfotója](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="68045-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="68045-229">![Az aktív szervezeti egységek képernyőfotója](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="68045-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="68045-230">Technikai megjegyzések</span><span class="sxs-lookup"><span data-stu-id="68045-230">Technical notes</span></span>

<span data-ttu-id="68045-231">Az adatok a telepítésével kapcsolatos további technikai információkat alább találja.</span><span class="sxs-lookup"><span data-stu-id="68045-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="68045-232">Meglévő adataira mintaadatok telepítése (nem ajánlott)</span><span class="sxs-lookup"><span data-stu-id="68045-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="68045-233">Megjegyzés: Ha a mintaadatokat egy meglévő Field Service vagy Project Service próba vagy a bemutató környezetre kell telepítenie, amelynek már vannak adatait(nem ajánlott), a telepítő biztonsági ellenőrzéseinek felfüggesztése szükséges.</span><span class="sxs-lookup"><span data-stu-id="68045-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="68045-234">Ehhez nyissa meg a **PkgFolder** mappát, keresse meg, és nyissa meg a **DemoDataPreImportConfig.xml** fájlt a Jegyzettömbbel (vagy egy másik XML-szerkesztővel).</span><span class="sxs-lookup"><span data-stu-id="68045-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="68045-235">Keresse meg a következő értéket, majd módosítsa a értékét igazról hamisra:</span><span class="sxs-lookup"><span data-stu-id="68045-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="68045-236">Ezt a változást kényszeríti a telepítőt néhány fontos biztonsági ellenőrzés figyelmen kívül hagyására, többek között:</span><span class="sxs-lookup"><span data-stu-id="68045-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="68045-237">Annak ellenőrzése hogy nincs egynél több aktív **Szervezeti egység** rekord, majd átnevezni **Fabrikam US** értékre.</span><span class="sxs-lookup"><span data-stu-id="68045-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="68045-238">Annak ellenőrzése, hogy nincs egynél több aktív **Munkasablon** bejegyzés.</span><span class="sxs-lookup"><span data-stu-id="68045-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="68045-239">Annak ellenőrzése hogy nincs egynél több aktív **Projektparméter** rekord, majd a bejegyzést **Paraméterek** értékre.</span><span class="sxs-lookup"><span data-stu-id="68045-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="68045-240">Konfigurációs összetevők</span><span class="sxs-lookup"><span data-stu-id="68045-240">Configuration components</span></span>

<span data-ttu-id="68045-241">Számos konfigurációs összetevők található az importálás előtti konfigurációs fájlban.</span><span class="sxs-lookup"><span data-stu-id="68045-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="68045-242">A technikai felhasználók számára ezek az alábbiak:</span><span class="sxs-lookup"><span data-stu-id="68045-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="68045-243">A(z) **\<RequiredSolutions\>** előfeltételt jelentő megoldás-összetevőket és azok verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68045-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="68045-244">A(z) **\<InstallSampleData\>** azt vezérli, hogy a kész mintaadatok települjenek-e az alkalmazásokhoz.</span><span class="sxs-lookup"><span data-stu-id="68045-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="68045-245">hamis - beépített adatok telepítésének átugrása (ez cserélhető)</span><span class="sxs-lookup"><span data-stu-id="68045-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="68045-246">igaz - telepíti a beépített adatokat az FS- és PSA-mintaadatok telepítésével együtt</span><span class="sxs-lookup"><span data-stu-id="68045-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="68045-247">A(z) **\<PreImportDataCollection\>** meghatározza az egyszintű-fájl adatleképezéseket és a társított rekordokat, amelyek a fő mintaadatok telepítése előtt importálva lesznek.</span><span class="sxs-lookup"><span data-stu-id="68045-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="68045-248">A(z) **\<EntitiesToEnableScheduling\>** megadja, hogy mely entitások legyenek engedélyezve a foglaláshoz a Microsoft Dynamics Scheduling rendszerben (más néven Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="68045-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="68045-249">A(z) **\<UsersToCreateAndConfigure\>** meghatározza a létrehozandó foglalható erőforrásokat (ha még nem léteznek), mielőtt végrehajtja a mintaadatok importálását.</span><span class="sxs-lookup"><span data-stu-id="68045-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="68045-250">Ne feledje, hogy a Foglalható erőforrás forrásrendszer-mintaadatok megegyeznek a célrendszer foglalható erőforrás-rekordjaival az egyes erőforrások FullName és bejelentkezés eleménél.</span><span class="sxs-lookup"><span data-stu-id="68045-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="68045-251">Ezért nem lehetséges az előzetes fájlban a nevek módosítása, kivéve, ha a mintaadatok először ezeket a neveket használva importálja a célrendszerbe, majd nevezze átnevezi a kívánt névre a foglalható erőforrások az Engedélyezett felhasználói rekordokkal együtt, és ezután exportálja az adatokat importálásra a végső rendszerbe (megfelelően frissítve az **ImportUserMapFile.xml** régi és az új bejegyzéseit).</span><span class="sxs-lookup"><span data-stu-id="68045-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="68045-252">A(z) **\<PluginsToDisable\>** meghatározza azokat az egyedi sortétel beépülő modulokat, amely le lesznek tiltva a mintaadatok importálása során, majd azt követően ismét engedélyezve lesznek.</span><span class="sxs-lookup"><span data-stu-id="68045-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="68045-253">A Fabrikam Robotics kitalált forgatókönyv</span><span class="sxs-lookup"><span data-stu-id="68045-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="68045-254">A Field Service és Project Service minta referenciaadat-csomagok telepítik a **Fabrikam Manufacturing Master Data (v3.0.0.0) megoldást** , körülbelül 4000 bejegyzéssel és mintegy 40 különböző entitással együtt.</span><span class="sxs-lookup"><span data-stu-id="68045-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution** , along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="68045-255">A külön mintaadatcsomagok a Field Service és Project Service alkalmazásokhoz a **v902FPSMasterData** mintadatok adott alkalmazásra vonatkozó részét tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="68045-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="68045-256">A **Demóadat** csomag telepíti a **Fabrikam Manufacturing Demo Data (v3.0.0.7) megoldást** körülbelül 148 entitás 22 000 rekordjával.</span><span class="sxs-lookup"><span data-stu-id="68045-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="68045-257">A Fabrikam Robotics képzeletbeli cég egy elektronikus eszközök összeszereléséhez használt robotokat gyárt, és híres a termei minőségéről, innovációiról és kiváló ügyfélszolgálatáról – foglalkoznak telepítéssel, tervezéssel, kivitelezéssel és folyamatos karbantartással.</span><span class="sxs-lookup"><span data-stu-id="68045-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="68045-258">A Fabrikam székhelye az Egyesült Államokban van (US Fabrikam) és projektalapú szolgáltatási műveletei vannak Franciaország, India, Egyesült Királyság és Svájc területén.</span><span class="sxs-lookup"><span data-stu-id="68045-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="68045-259">A helyszíni szolgáltatási műveletek központja az Egyesült Államokban van, leginkább Seattle vonzáskörzetében.</span><span class="sxs-lookup"><span data-stu-id="68045-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="68045-260">A vállalat a Dolgok Internete(IoT) konnektivitásra koncentrál, hogy megfigyelhesse az ügyfelek eszközeinek teljesítményét, egyre proaktívabb helyszíni szolgáltatásokat nyújthasson.</span><span class="sxs-lookup"><span data-stu-id="68045-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="68045-261">A mintaadatok átfogó áttekintése:</span><span class="sxs-lookup"><span data-stu-id="68045-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="68045-262">Közös mintaadatelemek (mindkét alkalmazás része)</span><span class="sxs-lookup"><span data-stu-id="68045-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="68045-263">1 felhasználó</span><span class="sxs-lookup"><span data-stu-id="68045-263">1 user</span></span>

    - <span data-ttu-id="68045-264">71 partner</span><span class="sxs-lookup"><span data-stu-id="68045-264">71 accounts</span></span>

    - <span data-ttu-id="68045-265">137 névjegy</span><span class="sxs-lookup"><span data-stu-id="68045-265">137 contacts</span></span>

    - <span data-ttu-id="68045-266">Különféle típusú tranzakciók és kategóriák</span><span class="sxs-lookup"><span data-stu-id="68045-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="68045-267">50 termék 1 termékárlistával</span><span class="sxs-lookup"><span data-stu-id="68045-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="68045-268">14 ár-/önköltségiár-lista</span><span class="sxs-lookup"><span data-stu-id="68045-268">14 price/cost lists</span></span>

    - <span data-ttu-id="68045-269">31 jellemző (forrásképességek) 2 értékelési modellben, 3 szinttel (értékelési értékek)</span><span class="sxs-lookup"><span data-stu-id="68045-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="68045-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="68045-270">Project Service</span></span>

    - <span data-ttu-id="68045-271">8 szervezetiegység</span><span class="sxs-lookup"><span data-stu-id="68045-271">8 organizational units</span></span>

    - <span data-ttu-id="68045-272">6 szerepkörspecifikus felhasználási szint</span><span class="sxs-lookup"><span data-stu-id="68045-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="68045-273">2,8 e + szerepkörár-specifikáció</span><span class="sxs-lookup"><span data-stu-id="68045-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="68045-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="68045-274">Field Service</span></span>

    - <span data-ttu-id="68045-275">4 terület</span><span class="sxs-lookup"><span data-stu-id="68045-275">4 territories</span></span>

    - <span data-ttu-id="68045-276">5 munkarendelés-típus</span><span class="sxs-lookup"><span data-stu-id="68045-276">5 work order types</span></span>

    - <span data-ttu-id="68045-277">22 ügyféleszköz</span><span class="sxs-lookup"><span data-stu-id="68045-277">22 customer assets</span></span>

    - <span data-ttu-id="68045-278">9 ügytípus, hozzárendelt erőforráskarakterisztika-tartománnyal (9) szolgáltatások (13) és szolgáltatási feladatok (13)</span><span class="sxs-lookup"><span data-stu-id="68045-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="68045-279">A **Demóadatok** csomag körülbelül 179 munkarendelést, 12 projektet és társított tranzakciós adatok telepít.</span><span class="sxs-lookup"><span data-stu-id="68045-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="68045-280">A mintaadat-erőforrásokhoz tartozó munkaidő módosítása</span><span class="sxs-lookup"><span data-stu-id="68045-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="68045-281">Alapértelmezés szerint minden foglalható erőforráshoz 24 munkaórás naptár tartozik.</span><span class="sxs-lookup"><span data-stu-id="68045-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="68045-282">Ha módosítania kell a munkaórákat minta foglalható erőforrásokhoz, nyissa meg a **Universal Resource Scheduling** > **Ütemezés** > **Erőforrások** részt.</span><span class="sxs-lookup"><span data-stu-id="68045-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="68045-283">Jelöljön ki egy felhasználót (például Spencer Low), és Spencer a munkaidejét módosítsa arra az értékre, amelyet a többi felhasználóhoz is szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="68045-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="68045-284">Nyissa meg a **Universal Resource Scheduling** > **Beállítások** > **Munkaidősablonok** elemet és szerkessze az **Alapértelmezett munkasablon** rekordot.</span><span class="sxs-lookup"><span data-stu-id="68045-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="68045-285">A **Sablonerőforrás** mezőben, jelöljön ki egy felhasználót akinek munkaóráit szeretne alkalmazni más erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="68045-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="68045-286">Válassza az **Universal Resource Scheduling** > **Ütemezés** > **Erőforrások** > **Aktív lefoglalható erőforrások**.</span><span class="sxs-lookup"><span data-stu-id="68045-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="68045-287">Jelölje ki az erőforrások, amelyeket módosítani szeretne és jelölje ki a **Naptár beállítása** elemet.</span><span class="sxs-lookup"><span data-stu-id="68045-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="68045-288">A **Munkasablon** legördülő listán jelölje ki az **Alapértelmezett munkaidő** sablont vagy egy mási sablont a vonatkozó sablonerőforrással.</span><span class="sxs-lookup"><span data-stu-id="68045-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="68045-289">Ha az ütemezési táblát megtekinti, látnia kell, hogy az erőforrásokhoz frissített munkaidő tartozik.</span><span class="sxs-lookup"><span data-stu-id="68045-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="68045-290">![Az aktív lefoglalható erőforrások képernyőfotója](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="68045-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
