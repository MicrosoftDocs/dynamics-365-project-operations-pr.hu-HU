---
title: Számlázható projektek könyvelésének konfigurálása
description: A témakör a számlázható projektek könyvelési lehetőségeivel kapcsolatos információkat biztosít.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cbc6bcbfa527486df4c740c52cec8c4be1dabe0478783fb7d2e71a65f18c050f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991038"
---
# <a name="configure-accounting-for-billable-projects"></a>Számlázható projektek könyvelésének konfigurálása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations különféle könyvelési lehetőségeket támogat a számlázható projektekhez, amelyek időpontokat és anyagokat, valamint rögzített árú tranzakciókat tartalmaznak.

- **Idővel és anyaggal kapcsolatos tranzakciók**: Ezeket a tranzakciókat a rendszer a projektnek az órák, a kiadások, a cikkek vagy a díjak fogyasztásán alapuló előrehaladása szerint számlázza. Ezek a tranzakciós költségek megfeleltethetők az egyes tranzakciók bevételeinek, és a projekt a munkafolyamat előrehaladásával kerül számlázásra. A projekt bevétele felhalmozható akkor is, amikor a tranzakció történik. A számlázás során a bevételt a rendszer felismeri, és adott esetben visszafordítja a bevételt.
- **Rögzített árú tranzakciók**: Ezeket a tranzakciókat a projektszerződésben meghatározott számlázási ütemezés szerint kell kiszámlázni. A rögzített árú tranzakciók bevétele elismerhető a számlázásnál, vagy időszakonként kiszámítva és könyvelve, a **Teljesített szerződés** vagy a **Teljesített százalék** módszer szerint.

A projekt akkor tekinthető számlázhatónak, ha egy vagy több szerződéssorral van társítva. A projektszerződéssor határozza meg, hogy milyen számlázási módszer és tranzakciótípusok engedélyezettek.

Például a Fabrikam Robotics elnyert egy projektszerződést az Adatum vállalatnál a berendezések optimalizálására. Az Adatum a projekt felmerült költségeinek fedezésére egy rögzített 10 000 USD összeget fog fizetni. Ez egy rögzített áras számlázási módszer. A projekt ideje és díja a használat alapján kerül számlázásra. Ez egy idő- ás anyagalapú számlázási módszer. A rendszer minden munkát egyetlen, Adatum berendezésoptimalizálás nevű projekt keretében követ nyomon.

A projektcsapat tagjai nyolc órányi munkát küldenek be az Adatum berendezésoptimalizálás projekten végzett munkaként. Amikor a projektmenedzser jóváhagyja ezt az időpontot, a rendszer az idő- és anyagalapú számlázási módot használja a tényleges adatokon alapuló tranzakciók, a számla és a partner létrehozásához. Ez a tranzakció nem kerül bele a rögzített áras bevétel becslési számításaiba.

Egy másik projektcsapat tagja 2000,00 USD összegben utazási költséget nyújt az Adatum berendezésoptimalizálás projektjéhez. Amikor a projektmenedzser jóváhagyja ezt a beküldést, a rendszer a rögzített árú számlázási módot használja a tényleges adatokon alapuló tranzakciók és a partner létrehozásához ehhez a projektköltséghez. Az ügyfél felé nem történik számlázás a tranzakció alapján. Ehelyett ezeket külön konfigurált számlázási mérföldkövek használatával számlázza a rendszer. Ez a költségtranzakció a költségbecslésekkel együtt belekerül a rögzített áras bevétel becslési számításaiba.

A projekttranzakciók számviteli elveit a projekt költség- és bevételi profiljai határozzák meg. A rendszer minden projecttranzakciónál meghatározza a projekt megfelelő költség- és bevételi profilját a projekt beállított költség- és bevételi profiljához tartozó szabályok használatával.

## <a name="define-project-cost-and-revenue-profiles"></a>Projekt költség- és bevételi profiljának meghatározása 

A projekt költség- és bevételi profiljai meghatározzák a projekttranzakciók számviteli szabályait. Ezek a profilok a Projektmenedzsment és könyvelés területén állíthatók be. 

A következő lépések végrehajtásával hozzon létre egy új projektköltség- és bevételi profilt. 

1. Lépjen a **Projektmenedzsment és könyvelés** > **Beállítás** > **Feladás** > **Projekt költség- és bevételi profiljai** részre. 
2. Válassza az **Új** lehetőséget új projektköltség- és bevételi profil létrehozásához.
3. A **Név** mezőben adja meg a profil nevét és rövid leírását.
4. A **Számlázási mód** mezőben válassza az **Idő és anyag** vagy a **Rögzített ár** lehetőséget.
5. Bontsa ki a **Főkönyv** gyorslapot. Az ezen a lapon található mezők határozzák meg azokat a számviteli elveket, amelyeket a rendszer a Project Operations integrációs naplójának használatával naplóz, majd a Projektszámlázási javaslat segítségével számláz.
6. Válassza ki a megfelelő adatokat a **Főkönyv** gyorslap következő mezőiben:

    - **Költségek feladása – óra**:

       - *Nincs főkönyv*: Az időtranzakciók költségét a rendszer nem könyveli a főkönyvbe, amikor a Project Operations integrációs naplója kerül feladásra. A könyvelő azonban a Költségek feladása funkcióval későbbi időpontban is könyvelheti a költségeket.
       - **Egyenleg**: Az időtranzakciók költsége a *Folyamatban lévő munka – költségértéke* főkönyvi számla típuson kerül terhelésre, valamint a *Bérlistafelosztási számlán* kerül jóváírásra a Főkönyvi feladás beállítása részben. A könyvelő a Költségek könyvelése funkció segítségével rendszeres időszakonként áthelyezi ezt a költséget egy Mérlegszámláról egy Eredményszámlára.
       - **Eredmény**: Amikor a Project Operations integrációs naplóba történik feladás, az időtranzakció költsége terhelésre kerül a *Költség* főkönyvi számla típuson, és jóváírásra kerül a **Főkönyvi feladás beállítása** oldal (**Projektmenedzsment és könyvelés** \> **Beállítás** \> **Feladás** \> **Főkönyvi feladás beállítása**) **Költség** lapjának *Bérlistafelosztási számla* részén. Ez az idő-és anyagalapú tranzakciók leggyakrabban használt beállítása.
        - *Nem kerül főkönyvbe*: Az időtranzakciók költségét a rendszer soha nem könyveli a főkönyvbe.

    - **Költségek feladása – kiadás**:

         - **Egyenleg**: A Project Operations integrációs naplóba történő feladáskor a rendszer a kiadási tranzakciós költséget a *Folyamatban lévő munka – költségértéke* főkönyvi számla típusra terheli a **Főkönyvi feladás beállítása** oldal **Költség** lapján megadott módon, és a naplósor ellenszámlájára írja jóvá. Az alapértelmezett ellenszámla a költségekhez a **Projektmenedzsment és könyvelés** > **Beállítás** \> **Feladás** \> **Alapértelmezett ellenszámla a költségekhez** részben van meghatározva. A könyvelő a **Költségek könyvelése** funkció segítségével rendszeres időszakonként áthelyezi ezt a költséget a mérlegszámláról egy eredményszámlára.
        - **Eredmény**: A Project Operations integrációs naplóba történő feladáskor a rendszer a kiadási tranzakciós költséget a *Költség* főkönyvi számla típusra terheli a **Főkönyvi feladás beállítása** oldal **Költség** lapján megadott módon, és a naplósor ellenszámlájára írja jóvá. Az alapértelmezett ellenszámla a költségekhez a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Feladás** \> **Alapértelmezett ellenszámla a költségekhez** részben van meghatározva.
      
    - **Költségek könyvelése – cikk**:

         - **Egyenleg**: A Project Operations integrációs naplójának könyvelésekor a cikktranzakció költsége a Főkönyvi számla típusa *WIP – Költségérték – cikk* lesz, amint az meg van határozva a **Főkönyv könyvelési beállítás** lap **Költség** fülén, és a következő jóváírást tette:
    
              - Dokumentumtípus használatához: **Költség - cikk** számla a **Főkönyvi könyvelési beállításon**.  
              - Dokumentumtípus vásárlásához: **Beszerzési integrációs fiók** a **Projektmenedzsment és a könyvelési paramétereken**.
           A könyvelő a **Költségek könyvelése** funkció segítségével rendszeres időszakonként áthelyezi ezt a költséget a mérlegszámláról egy eredményszámlára.
        - **Profit és veszteség**: A Project Operations integrációs naplójának könyvelésekor a cikktranzakció költsége a Főkönyvi számla típusa *Költség* lesz, amint az meg van határozva a **Főkönyv könyvelési beállítás** lap **Költség** fülén, és a következő jóváírást tette:
         
             - Dokumentumtípus használatához: **Költség - cikk** számla a **Főkönyvi könyvelési beállításon**.  
             - Dokumentumtípus vásárlásához: **Beszerzési integrációs fiók** a **Projektmenedzsment és a könyvelési paramétereken**.
       
    - **Partneren történő számlázás**:

        - **Egyenleg**: A Projektszámlázási javaslat feladásakor egy számlára irányuló tranzakció (számlázási mérföldkő) kerül jóváírásra a *Számlázott folyamatban lévő munka – számlára* főkönyvi számlatípuson a **Főkönyvi feladás beállítása** oldal **Bevétel** lapján megadott módon, és terhelésre kerül az Ügyfél egyenlegszámláján.
         - **Eredmény**: A Projektszámlázási javaslat feladásakor egy számlára irányuló tranzakció (számlázási mérföldkő) kerül jóváírásra a *Számlázott bevétel – számlára* főkönyvi számlatípuson a **Főkönyvi feladás beállítása** oldal **Bevétel** lapján megadott módon, és terhelésre kerül az Ügyfél egyenlegszámláján. Az ügyfélegyenleg-számlák a **Követelések** \> **Beállítás** \> **Ügyfélfeladási profilok** részben vannak meghatározva.

   Az idő- és anyagszámlázási módszerek könyvelési profiljainak meghatározásakor tranzakciótípusonként (óra, költség, cikk és díj) bevétel halmozódhat fel. Ha az **Elhatárolt bevétel** beállítás értéke **Igen**, akkor a Project Operations integrációs naplójában a nem számlázott értékesítési tranzakciók a főkönyvi naplóban kerülnek rögzítésre. Az értékesítési érték a **Folyamatban lévő munka – értékesítési érték számlán** kerül terhelésre, és az **Elhatárolt bevétel – értékesítési érték** számlán kerül jóváírásra, amely a **Főkönyvi feladás beállítása** lapon, a **Bevétel** lapon van beállítva. 
  
  > [!NOTE]
  > Az **Elhatárolt bevétel** lehetőség csak akkor érhető el, ha a megfelelő **Költség** tranzakciótípus feladásra kerül az eredményszámlára.
    
7. Bontsa ki a **Becslés** gyorslapot. Az ezen a lapon található mezők határozzák meg a rögzített áras bevételre vonatkozó becslések számítási beállításait. A lapon található mezők csak a **Rögzített áras** számlázási móddal rendelkező projektköltség- és bevételi profilokra vonatkoznak.
8. Válassza ki a megfelelő adatokat a **Becslés** gyorslap következő mezőiben:

    - **A projektek teljesítési számításaihoz használt elv**:

        - **Teljesített szerződés**: A költség egyeztetése és a bevétel elszámolása a projekt végéig nem történik meg. A költségek folyamatban lévő termelésként jelennek meg, amíg a projekt be nem fejeződik.
        - **Teljesített százalék**: Az elhatárolt bevételt a rendszer kiszámítja és a főkönyvbe könyveli minden időszakra a projekt készültségi százaléka alapján. A készültségi százalék kiszámításához többféle módszer áll rendelkezésre. Ezek a módszerek lehetnek automatikusak, a konfiguráció alapján, vagy a manuálisak.
        - **Nem folyamatban lévő termelés**: Ezt a beállítást rövid időtartamú, rögzített árú projektek esetén használja a rendszer, ahol a számla és a költségek ugyanabban az időszakban fordulnak elő. Ebben az esetben a rendszer a **Főkönyv** gyorslap **Részszámla készítése** mezőjét automatikusan **Eredmény** értékre állítja be, így biztosítva a bevétel elszámolását a számlázásnál. A Bevételbecslés folyamata nem kerül használatra ehhez a projektköltség- és bevételi profilhoz.

    - **Egyeztetési elv**: Ez a mező határozza meg, hogy a számított értékesítési érték (elhatárolt bevétel) hogyan kerül a főkönyvbe.

        - Az **Értékesítési érték** elv használatával a rendszer kiszámítja az értékesítési értéket a költségek és a bevétel egyeztetésével, majd ezt követően egy összegként könyveli azt.
        - A **Termelés és a profit** elv segítségével a rendszer az értékesítési értéket realizált költségre és számított profitra osztja fel. Ezeket külön könyveli a rendszer.

    - **Költségsablonok**: Lehetővé teszi a projekttranzakciók tranzakciótípus és projektkategória alapján történő csoportosítását, és ezekhez a csoportokhoz százalékos teljesítési számítási szabályokat határoz meg.
    - **Időszakkódok**: Megadja, hogy milyen gyakorisággal számítja ki a program az adott projektköltség- és bevételi profil bevételi becsléseit.
    - **Becslés kategóriái**: Az értékesítési érték (elhatárolt bevétel) Projekttranzakciókba történő feladására szolgál. Első lépésként állítsa be a dedikált projektkategóriát a **Díj** tranzakciótípushoz, majd állítsa be a **Becslés** jelzőt ehhez a projektkategóriához. Következő lépésként a kijelölt egyeztetési elv függvényében válassza ezt a projektkategóriát az **Értékesítés** érték vagy a **Profit** mezőben a projektköltség- és bevételi profilban.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>A projektköltség- és bevételi profilok mintakonfigurációi

Idő és anyagok – nem folyamatban lévő termelés

![Költség- és bevételi profil: Idő és anyagok – nem folyamatban lévő termelés.](media/time-material-no-wip.png)

Idő és anyagok – folyamatban lévő termelés (bevétel)

![Költség- és bevételi profil: Idő és anyagok – folyamatban lévő termelés.](media/time-material-with-wip.png)

Rögzített ár – nem folyamatban lévő termelés

![Költség- és bevételi profil: Rögzített ár – nem folyamatban lévő termelés.](media/fixed-price-no-wip.png)

Rögzített ár – teljesített szerződés

![Költség- és bevételi profil: Rögzített ár – teljesített szerződés.](media/fixed-price-completed-contract.png)

Rögzített ár – százalékos teljesítés

![Költség- és bevételi profil: Rögzített ár – százalékos teljesítés.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>A projektköltség- és bevételi profilok mintáinak könyvelésiesemény-példái.

| Könyvelési esemény                  | Idő és anyag – Nem folyamatban lévő termelés                       | Idő és anyag – Folyamatban lévő termelés                                                                                           | Rögzített ár – nem folyamatban lévő termelés                                            | Rögzített ár – Teljesített szerződés                                                                            | Rögzített ár – Százalékos teljesítés                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Időtranzakciók naplózása    | Terhelés – Költség <br>Jóváírás – Bérlista-hozzárendelés          | Terhelés – Költség <br>Jóváírás – Bérlista-hozzárendelés <br>Terhelés – Folyamatban lévő termelés értékesítési értéke <br>Jóváírás – Elhatárolt bevétel értékesítési értéke                | Terhelés – Költség <br>Jóváírás – Bérlista-hozzárendelés                         | Terhelés – Költség <br>Jóváírás – Bérlista-hozzárendelés                                                                    | Terhelés – Költség <br>Jóváírás – Bérlista-hozzárendelés                       |
| Kiadástranzakciók naplózása | Terhelés – Költség <br>Jóváírás – Ellenszámla a kiadáshoz | Terhelés – Költség <br>Jóváírás – Ellenszámla a kiadáshoz <br>Terhelés – Folyamatban lévő termelés értékesítési értéke <br>Jóváírás – Elhatárolt bevétel értékesítési értéke      | Terhelés – Költség <br>Jóváírás – Ellenszámla a kiadáshoz                 | Terhelés – Költség<br> Jóváírás – Ellenszámla a kiadáshoz                                                            | Terhelés – Költség <br>Jóváírás – Ellenszámla a kiadáshoz               |
| Ügyfélszámlázás                | Terhelés – Ügyfélegyenleg <br>Jóváírás – Számlázott bevétel | Terhelés – Ügyfélegyenleg <br>Jóváírás – Számlázott bevétel <br>Jóváírás – Folyamatban lévő munka értékesítési értéke Terhelés – Elhatárolt bevétel értékesítési értéke | Terhelés – Ügyfélegyenleg <br>Jóváírás – Számlázott bevétel – részszámlázás | Terhelés – Ügyfélegyenleg <br>Jóváírás – Folyamatban lévő termelés – Részszámlázás                                                  | Terhelés – Ügyfélegyenleg <br>Jóváírás – Folyamatban lévő termelés – Részszámlázás    |
| Bevételbecslés feladása             | Nem alkalmazható                                   | Nem alkalmazható                                                                                                    | Nem alkalmazható                                                  | Terhelés – a folyamatban lévő munka költségének értéke <br>Jóváírás – Költség                                                                         | Terhelés – Folyamatban lévő termelés – Értékesítési érték <br>Jóváírás – Elhatárolt bevétel értékesítési értéke |
| Eltávolítás                         | Nem alkalmazható                                   | Nem alkalmazható                                                                                                    | Nem alkalmazható                                                  | Jóváírás – a folyamatban lévő munka költségének értéke <br>Terhelés – Költség <br>Jóváírás – Elhatárolt bevétel – Értékesítési érték <br>Terhelés – Folyamatban lévő termelés részszámlázása | Terhelés – Folyamatban lévő termelés – Részszámlázás <br>Jóváírás – Folyamatban lévő termelés értékesítési értéke     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projektköltség- és bevételi profil szabályainak konfigurálása

A projektköltség-és bevételi profil szabályai határozzák meg a projektköltség-és bevételi profilt, amelyet a számlázható projekttranzakciók feldolgozása során kell használni. A szabályok definiálásához lépjen a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Feladás** \> **Projektköltség- és bevételi profil szabályai** részre.

A szabályok meghatározhatók projektszerződés, projektcsoport vagy adott projekt szerint. A rendszer mindig a legmagasabb részletességű szabályt választja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
