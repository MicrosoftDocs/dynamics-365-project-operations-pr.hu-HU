---
title: Mintaadatok telepítése
description: Ez a témakör a Project Service Automation alkalmazásban a mintaadatok telepítésével kapcsolatos tudnivalókat tartalmaz.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 01e2f1f6b29e040d5c72af402031e13a867736405c4ee161e49b74a30e4b506e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985549"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>A Project Service alkalmazás mintaadatok telepítése

[!include [banner](../includes/psa-now-project-operations.md)]

Saját bemutatókörnyezetének felépítéséhez a Microsoft letölthető mintaadat-csomagokat biztosít, amelyek bemutatják az alkalmazások képességeit. Kétféle mintafájlcsomag létezik:
- hivatkozási/beállítási adatok
- demóadatok (hivatkozási/beállítási és a tranzakciós adatok, például a munkarendelések és projektek)

A minta **referencia** adatcsomagok három különböző csomagban tölthetők le, akár csak a Project Service, vagy csak a Field Service számára is telepíthetők, illetve mindkét alkalmazás mintaadatai egyszerre is telepíthetők.

A minta beállítási/referencia adatcsomagok a következők:

- [**V902PSMasterData** - csak Project Service 3.x verzió](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - csak Field Service 8.x verzió](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x és Project Service 3.x verzió](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

A legújabb **demó** adatcsomag a következő:

 - [**FPSDemoData** - Field Service 8.x és Project Service 3.x verzió](https://aka.ms/fpsdemodatapackage)

   A telepítési utasítások a szakasz létrehozásához és konfigurálásához a felhasználókban kissé eltérhet, de a többi ugyanaz, mint ez előző [**blogbejegyzésben**](https://aka.ms/fpsdemodatablog). A csomag tartalmaz egy korlátozott demó adatkészletet, és telepíteni körülbelül 3 óráig tart.

A mintaadatcsomagok csak angolul érhetők el.

> [!IMPORTANT]
> **Nem lehetséges a mintaadatok eltávolítása.** Ezért ezt a csomagokat csak demonstrációs, kiértékelési, oktatási vagy tesztrendszerekre telepítse. Ne feledje, hogy az egy csomag telepítése, majd a másik csomag telepítése nem támogatott. (Ez azt jelenti, akkor nem tudja telepíteni az **FSMasterData** csomag után a **PSMasterData** csomagot, illetve fordítva.) Ha saját a jövőben mindkét alkalmazáshoz szükségük lehet a mintaadatokra, telepítse a **v902FPSMasterData** csomagot.

Amikor telepíti a mintaadatcsomagok, a telepítési folyamat az alábbi műveleteket hajtja végre:

- A Project Service, Field Service vagy mindkét alkalmazáshoz használt (amennyiben van) alapértelmezett paramétereket hoz léte, és állít be.

- Mintaadatokat importál az alkalmazásokhoz, például a foglalható erőforrásokat, az alkalmazás-specifikus szerepköröket, értékesítési és a önköltség árlistákat, szervezeti egységeket értékesítési folyamat bejegyzéseket és más entitásokat a fontos funkciók bemutatásához.  

A **demóadatok** csomaggal a fentiek és további tranzakciós adatok jelennek meg, például a munkarendelések és a projektek.

Kíváncsi, hogy milyen műveleteket demózhat a mintaadatokkal? A Fabrikam Robotics fikcionális esetét alább, a [Műszaki megjegyzések](#technical-notes) részben találja.

Ha kérdése van a mintaadatcsomagok telepítéséről [küldjön egy e-mailt az fpsdemodata@microsoft.com címre](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Követelmények

A telepítés protokoll feltételezi, a következőket a célpéldányról (szervezet):

- Az alapnyelv az angol, és az alappénznem az amerikai dollár (USD,$).

- A szervezet még nem rendelkezik Project Service vagy Field Service adatokkal, vagy csak az új szervezetekhez tartozó legszükségesebb alapértelmezett adatokat tartalmazza.

- Az üzleti alkalmazás megfelelő verziója már telepítve van:
       
    - **A FPSDemoData vagy v902FPSMasterData esetén:** A Field Service 8.x és a Project Service 3.x verziója telepítve van a szervezethez.

    - **A v902PSMasterData:** A Project Service verziója 3.x telepítve van szervezethez.

    - **v902FSMasterData esetében:** A Field Service 8.x verziója telepítve van a szervezethez.

> [!NOTE]
> Ha a mintaadatokat egy meglévő Project Service és a Field Service próba- vagy a demókörnyezetre kell telepítenie, amelynek már vannak adatai (nem ajánlott), a telepítő biztonsági ellenőrzéseinek felfüggesztése szükséges. További tudnivalókat a lenti műszaki megjegyzések rész tartalmaz.

## <a name="prepare-for-installation"></a>Felkészülés a telepítésre

A Windows egy újabb verziójával (lehetőleg Windows 10) rendelkező számítógépen futtassa a telepítőprogramot.

Úgy kell terveznie, hogy a számítógép kapcsolódva maradjon egy hálózathoz, a telepítés futása **egy óráig** is eltarthat a **beállítási/referencia adatok** esetén. (Általában a a telepítés körülbelül 30 percig tart a **FPSMasterData** esetén, amelynek részei a mindkét alkalmazáshoz való mintaadatok.) Az **FPSDemoData** esetén a telepítés körülbelül **3 óráig** tart.

A számítógépen ki kell kapcsolni a képernyővédő funkciót. Ellenkező esetben a telepítés munkamenetének hitelesítő adatai elveszhetnek, amikor a képernyővédő bekapcsol (kivéve, ha a munkamenet végig aktív marad).

> [!div class="mx-imgBorder"]
> ![A képernyőkímélő beállításainak képernyőképe, amikor a képernyővédő ki van kapcsolva.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Letöltés és kicsomagolás

A Project Service és a Field Service mintaadatok telepítő terjesztése egy önkicsomagoló végrehajtható fájlban történik. A fájlnevek eltérők lehetnek a mintaadatcsomagtól függően, de egyébként a lépések ugyanazok, függetlenül attól, hogy mely csomagot telepíti.

A csomag letöltése után futtassa az .exe fájlt, és fogadja el a feltételeket a tömörített fájl kibontásához. Tömörítse ki a fájl tartalmát a számítógép egy tetszőleges mappájába.

Az operációs rendszertől és a biztonsági beállításoktól függően szükség lehet a következő lépések elvégzésére a .zip fájlok fájlt kicsomagolása után:

1. Keresse meg, majd kattintson a jobb gombbal az **FPSDemoData.dll** fájlra a **v902FPSMasterData** / **PackageDeployer_FPSDemoData** mappában.

2. Válassza a **Tiltás feloldása** lehetőséget.

3. Válassza az **Alkalmaz** lehetőséget.

4. Kattintson az **OK** gombra.


## <a name="create-or-configure-users"></a>Felhasználók létrehozása vagy konfigurálása

Az **FPSDemoData** csomaghoz hat felhasználó szükséges, míg az **FPSMasterData** csomagokhoz szükséges egy felhasználó. A helyes változatra vonatkozó adatokkal foglalkozzon az Ön mintaadat-csomagjához.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Felhasználók létrehozása vagy konfigurálása - beállítási/referencia adatcsomagok

Az **FPSMasterData** csomag arra szolgál, hogy egy Spencer Low nevű felhasználót az itt ismertetett beállításokkal telepítsen. A csomag megfelelő telepítéséhez létre kell hoznia (vagy ideiglenesen át kell neveznie) felhasználókat a környezetében, hogy azok megfeleljenek a beérkező mintaadatok konfigurációjának.

A felhasználókat létrehozásához vagy konfigurálásához válasza a **Beállítások** > **Biztonság** > **Felhasználók** lehetőséget, és tegye a következőket:

1. A UserFullname = „Spencer Low” a felhasználónév „spencerl” (**kisbetűs**) a Projektmenedzser és Gyakorlatmenedzser szerepkörökhöz.

2. Válassza ki **Spenver Low** felhasználót majd a **Szerepkörök kezelése** lehetőséget. Keresse meg és jelölje ki a **Rendszergazda** szerepkört, majd válassza az **OK** lehetőséget, hogy rendszergazdai jogokaz adjon Spencer Lownak. Ez a lépés szükséges annak biztosítására, hogy mintarekordok megfelelő felhasználói tulajdonjoggal jöjjenek létre és ezért megfelelően legyenek megjelenítve a nézetek.

3. A letöltött csomagból a adatleképezési fájlját frissítenie kell az alapértelmezett felhasználói környezet e-mail-címeivel. Ehhez nyissa meg a **PkgFolder** mappát, majd keresse és nyissa meg az **ImportUserMapFile.xml** fájlt a Jegyzettömbben (vagy a Visual Studio-val vagy egy másik XML-szerkesztővel). Állítsa be a **DefaultUserToMapTo =** mezőt Spencer Low felhasználó e-mail címére.

4. Ha nem használ Spencer Low felhasználót **spencerl** felhasználónévvel, egy további fájlt is frissítenie kell. Nyissa meg a **DemoDataPreImportConfig.xml** fájlt, és keresse meg a **userstocreateandconfigure** címkét. Frissítse a **\<login\>** címkét a Horváth Tamás felhasználónévvel. További részleteket a lenti [Műszaki megjegyzések](#technical-notes) rész tartalmaz.

## <a name="create-or-configure-users---demo-data-package"></a>Felhasználók létrehozása vagy konfigurálása - demó adatcsomag

A demó adatcsomaghoz hat felhasználó szükséges. Hogy a csomag telepítése megfelelő legyen, tegye a következőket:

 1. Hozzon létre, vagy ideiglenesen nevezze át a felhasználókat, hogy megegyezzenek a bejövő minta datok konfigurációjával úgy, hogy ugorjon a **Beállítások** > **Biztonság** > **Felhasználók** lehetőségre.
 
    Ezekre a szerepkörökre csak az általános személy-alapú bemutatóknál van szükség.  
    - Felhasználó teljes neve = "David So" mint helyszíni szolgáltatási technikus   
    - Felhasználó teljes neve = "Jamie Reding" ügyfélszolgálati & helyszíni szolgáltatási diszpécser   
    - Felhasználói teljes név = "Molly Clark" mint partnermenedzser   
    - Felhasználói teljes név = "Spencer Low" mint gyakorlati és projektmenedzser  
    - Felhasználói teljes név = "Veronica Quek" mint csoporttag   
    - Felhasználói teljes név = "William Contoso"
  
2. A demóadatok importálásának céljából rendelje hozzá a fenti hat felhasználóhoz a Rendszergazdai szerepkört, hogy a mintarekordok helyesen importálódjanak. 

3. Nyissa meg a **PkgFolder** elemet, majd keresése és nyissa meg a **ImportUserMapFile.xml** fájlt. Frissítse az **Új =** mezőket a rendszerben található megfelelő felhasználók e-mail címéhez.

   > [!div class="mx-imgBorder"]
   > ![UserMapFile képernyőképe.](media/sample-data-7.png)

4. Ha a „Spencer Low” teljes nevű felhasználónak más a felhasználói azonosítója, mint a **„spencerl”**, frissítenie kell a kiegészítő fájlt. Nyissa meg a **DemoDataPreImportConfig.xml** fájlt, és keresse meg a **userstocreateandconfigure** címkét. Frissítse a **\<login\>** címkét a loginId azonosítóval (kis-és nagybetűk megkülönböztetésével). 

5. Az első felhasználó naptárja (a **userstocreateandconfigure** címkén belül) a munkaórák feltöltésére használatos a demóadatok importálásához szükséges minden foglalható erőforrásra vonatkozóan. Navigáljon a **Beállítások** > **Biztonság** > **Felhasználók** elemhez, keresse meg az "Spencer Low" felhasználót, és nyissa meg a "Munkaórák" lehetőséget. Módosítsa a meglévő munkaórákat, válassza ki a **Teljes heti ismétlődési minta kezdéstől a befejezésig** lehetőséget. Ellenőrizze, hogy a **munkaidő 8:00-17:00-ig (9 óra) tart, hétfőtől péntekig, az időzóna pedig Csendes-óceáni idő (USA és Kanada)**. Ez biztosítja, hogy a projekt és ütemezési tábla megjelenítése az elvártnak megfelelő.

**Javaslat:** Érdemes most megfontolni biztonsági másolat készítését a szervezetről arra az esetre ha vissza kellene állítania a kezdő állapotot, ha baj történne a példaadatok telepítése során. További információkért, látogasson el erre az oldalra: [Biztonsági és visszaállítási példányok.](/dynamics365/customer-engagement/admin/backup-restore-instances)

## <a name="run-the-package-deployer"></a>Futtassa a Package Deployer alkalmazást

1. Keresse meg és futtassa a **PackageDeployer.exe** állományt a **v902FPSMasterData** vagy **PackageDeployer_FPSDemoData** mappában.

2. Fogadja el a feltételeket.

3. A következő ablakban:

   a. Telepítési típus kiválasztása **Office 365**.

   b. Használja a „Felhasználók létrehozása és konfigurálása” helyen létrehozott rendszergazda („spencerl” felhasználónevű „Spencer Low” felhasználó) felhasználónevét és jelszavát.

   c. Győződjön meg arról, hogy a **Rendelkezésre álló szervezetek listájának képernyője** ki van választva.

      > [!div class="mx-imgBorder"]
      > ![Képernyőkép az Package Deployer „Elérhető szervezetek listájának megjelenítése” kiválasztott lehetőséget tartalmazó ablakról](media/sample-data-2.png)

4. Válassza ki azt a szervezetet, ahova a mintaadatokat telepíteni szeretné.

5. Válassza a **Következő** lehetőséget. amíg meg nem jelenik a **Bemutatóadatok beállítása** párbeszédpanel.

   > [!div class="mx-imgBorder"]
   > ![A bemutatóadatok telepítése állapotablak képernyőfotója.](media/sample-data-3.png)

6. A folytatás előtt fontos tudni, hogy a mintaadatok telepítése akár egy óráig is eltarthat (általában ~ 10 perc). Biztosítsa, hogy a számítógép és a kapcsolódva maradjon a hálózathoz, a telepítési folyamat során, hogy a munkamenet aktív maradjon.   

7. Amikor elkészült, kattintson a **Következő** gombra a mintaadatok telepítésének megkezdéséhez. A mintaadatok betöltése után kattintson a **Befejezés** gombra.

## <a name="verify-the-sample-data-installation"></a>A mintaadatok telepítésének ellenőrzése

Alapvető ellenőrzésként ellenőrizze, hogy a bejegyzések száma és az entitástípusok Fabrikam Robotics kitalált esetnél megfelelően jelennek meg.

A mintaadatok teljesen betöltését követően, jelentkezzen be Spencer Low felhasználóval, és ellenőrizze a következőket:

- Ha a Project Service alkalmazás telepítve van, lépjen **Project Service** > **Beállítások** > **Árlisták** helyre. Győződjön meg arról, hogy a számlázási díjak és a költségárfolyamok megtalálhatók az egyes országoknak/régióknak megfelelő pénznemben.

- Ha a Project Service alkalmazás telepítve van, lépjen a **Universal Resource Scheduling** > **Beállítások** > **Szervezeti egységek** helyre. Győződjön meg arról, hogy a megfelelő pénznem lett társítva az önköltségiköltségi árlistához minden egyes szervezeti egységnél (kivéve a város bejegyzések). Ha bármelyik hiányzik, keresse meg és társítsa a megfelelő önköltségi árlistát.

- Ha a Field Service alkalmazás telepítve van, lépjen **Project Service** > **Beállítások** > **Árlisták** helyre. Ellenőrizze, hogy számlázási díjak és a költségárfolyamok megvannak-e. Nyissa meg **Field Service** > **Beállítások** > **Árlisták** menüt, és ellenőrizze, hogy számlázási díjak és a költségárfolyamok léteznek, a megfelelő pénznemben, minden egyes országhoz/régióhoz az adatkészletben.

  > [!div class="mx-imgBorder"]
  > ![Az aktív árlisták képernyőfotója.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Az aktív szervezeti egységek képernyőfotója.](media/sample-data-5.png)

## <a name="technical-notes"></a>Technikai megjegyzések

Az adatok a telepítésével kapcsolatos további technikai információkat alább találja.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Meglévő adataira mintaadatok telepítése (nem ajánlott)

Megjegyzés: Ha a mintaadatokat egy meglévő Field Service vagy Project Service próba vagy a bemutató környezetre kell telepítenie, amelynek már vannak adatait(nem ajánlott), a telepítő biztonsági ellenőrzéseinek felfüggesztése szükséges.

Ehhez nyissa meg a **PkgFolder** mappát, keresse meg, és nyissa meg a **DemoDataPreImportConfig.xml** fájlt a Jegyzettömbbel (vagy egy másik XML-szerkesztővel).

Keresse meg a következő értéket, majd módosítsa a értékét igazról hamisra:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Ezt a változást kényszeríti a telepítőt néhány fontos biztonsági ellenőrzés figyelmen kívül hagyására, többek között:

- Annak ellenőrzése hogy nincs egynél több aktív **Szervezeti egység** rekord, majd átnevezni **Fabrikam US** értékre.

- Annak ellenőrzése, hogy nincs egynél több aktív **Munkasablon** bejegyzés.

- Annak ellenőrzése hogy nincs egynél több aktív **Projektparméter** rekord, majd a bejegyzést **Paraméterek** értékre.

### <a name="configuration-components"></a>Konfigurációs összetevők

Számos konfigurációs összetevők található az importálás előtti konfigurációs fájlban. A technikai felhasználók számára ezek az alábbiak:

- A(z) **\<RequiredSolutions\>** előfeltételt jelentő megoldás-összetevőket és azok verziószámát adja meg.

- A(z) **\<InstallSampleData\>** azt vezérli, hogy a kész mintaadatok települjenek-e az alkalmazásokhoz.

    - hamis - beépített adatok telepítésének átugrása (ez cserélhető)

    - igaz - telepíti a beépített adatokat az FS- és PSA-mintaadatok telepítésével együtt

- A(z) **\<PreImportDataCollection\>** meghatározza az egyszintű-fájl adatleképezéseket és a társított rekordokat, amelyek a fő mintaadatok telepítése előtt importálva lesznek.

- A(z) **\<EntitiesToEnableScheduling\>** megadja, hogy mely entitások legyenek engedélyezve a foglaláshoz a Microsoft Dynamics Scheduling rendszerben (más néven Universal Resource Scheduling).

- A(z) **\<UsersToCreateAndConfigure\>** meghatározza a létrehozandó foglalható erőforrásokat (ha még nem léteznek), mielőtt végrehajtja a mintaadatok importálását. Ne feledje, hogy a Foglalható erőforrás forrásrendszer-mintaadatok megegyeznek a célrendszer foglalható erőforrás-rekordjaival az egyes erőforrások FullName és bejelentkezés eleménél. Ezért nem lehetséges az előzetes fájlban a nevek módosítása, kivéve, ha a mintaadatok először ezeket a neveket használva importálja a célrendszerbe, majd nevezze átnevezi a kívánt névre a foglalható erőforrások az Engedélyezett felhasználói rekordokkal együtt, és ezután exportálja az adatokat importálásra a végső rendszerbe (megfelelően frissítve az **ImportUserMapFile.xml** régi és az új bejegyzéseit).

- A(z) **\<PluginsToDisable\>** meghatározza azokat az egyedi sortétel beépülő modulokat, amely le lesznek tiltva a mintaadatok importálása során, majd azt követően ismét engedélyezve lesznek.

### <a name="fabrikam-robotics-fictitious-scenario"></a>A Fabrikam Robotics kitalált forgatókönyv

A Field Service és Project Service minta referenciaadat-csomagok telepítik a **Fabrikam Manufacturing Master Data (v3.0.0.0) megoldást**, körülbelül 4000 bejegyzéssel és mintegy 40 különböző entitással együtt. A külön mintaadatcsomagok a Field Service és Project Service alkalmazásokhoz a **v902FPSMasterData** mintadatok adott alkalmazásra vonatkozó részét tartalmazzák. A **Demóadat** csomag telepíti a **Fabrikam Manufacturing Demo Data (v3.0.0.7) megoldást** körülbelül 148 entitás 22 000 rekordjával.

A Fabrikam Robotics képzeletbeli cég egy elektronikus eszközök összeszereléséhez használt robotokat gyárt, és híres a termei minőségéről, innovációiról és kiváló ügyfélszolgálatáról – foglalkoznak telepítéssel, tervezéssel, kivitelezéssel és folyamatos karbantartással. A Fabrikam székhelye az Egyesült Államokban van (US Fabrikam) és projektalapú szolgáltatási műveletei vannak Franciaország, India, Egyesült Királyság és Svájc területén.

A helyszíni szolgáltatási műveletek központja az Egyesült Államokban van, leginkább Seattle vonzáskörzetében. A vállalat a Dolgok Internete(IoT) konnektivitásra koncentrál, hogy megfigyelhesse az ügyfelek eszközeinek teljesítményét, egyre proaktívabb helyszíni szolgáltatásokat nyújthasson.

A mintaadatok átfogó áttekintése:

- Közös mintaadatelemek (mindkét alkalmazás része)

    - 1 felhasználó

    - 71 partner

    - 137 névjegy

    - Különféle típusú tranzakciók és kategóriák

    - 50 termék 1 termékárlistával

    - 14 ár-/önköltségiár-lista

    - 31 jellemző (forrásképességek) 2 értékelési modellben, 3 szinttel (értékelési értékek)

- Project Service

    - 8 szervezetiegység

    - 6 szerepkörspecifikus felhasználási szint

    - 2,8 e + szerepkörár-specifikáció

- Field Service

    - 4 terület

    - 5 munkarendelés-típus

    - 22 ügyféleszköz

    - 9 ügytípus, hozzárendelt erőforráskarakterisztika-tartománnyal (9) szolgáltatások (13) és szolgáltatási feladatok (13)
   
A **Demóadatok** csomag körülbelül 179 munkarendelést, 12 projektet és társított tranzakciós adatok telepít. 

### <a name="change-the-work-hours-for-sample-resources"></a>A mintaadat-erőforrásokhoz tartozó munkaidő módosítása

Alapértelmezés szerint minden foglalható erőforráshoz 24 munkaórás naptár tartozik.

Ha módosítania kell a munkaórákat minta foglalható erőforrásokhoz, nyissa meg a **Universal Resource Scheduling** > **Ütemezés** > **Erőforrások** részt.

Jelöljön ki egy felhasználót (például Spencer Low), és Spencer a munkaidejét módosítsa arra az értékre, amelyet a többi felhasználóhoz is szeretne használni. Nyissa meg a **Universal Resource Scheduling** > **Beállítások** > **Munkaidősablonok** elemet és szerkessze az **Alapértelmezett munkasablon** rekordot. A **Sablonerőforrás** mezőben, jelöljön ki egy felhasználót akinek munkaóráit szeretne alkalmazni más erőforrásokhoz. Válassza az **Universal Resource Scheduling** > **Ütemezés** > **Erőforrások** > **Aktív lefoglalható erőforrások**. Jelölje ki az erőforrások, amelyeket módosítani szeretne és jelölje ki a **Naptár beállítása** elemet. A **Munkasablon** legördülő listán jelölje ki az **Alapértelmezett munkaidő** sablont vagy egy mási sablont a vonatkozó sablonerőforrással. Ha az ütemezési táblát megtekinti, látnia kell, hogy az erőforrásokhoz frissített munkaidő tartozik.

> [!div class="mx-imgBorder"]
> ![Az aktív lefoglalható erőforrások képernyőfotója.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]