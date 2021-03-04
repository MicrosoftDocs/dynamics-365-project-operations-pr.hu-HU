---
title: Költségkezelés konfigurálása
description: Ez a cikk azokat a szempontokat és döntéseket ismerteti, amelyeket a tervezési folyamat során el kell végeznie a Költségkezelés konfigurálása előtt a Microsoft Dynamics 365 Finance szolgáltatásban.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960340"
---
# <a name="configure-expense-management"></a>Költségkezelés konfigurálása

Ez a témakör azokat a szempontokat és döntéseket ismerteti, amelyeket a tervezési folyamat során el kell végeznie a Költségkezelés konfigurálása előtt. A Költségkezelés során információkat tárolhat a fizetési módszerekről, az utazási igénylésekről, a költségjelentésekről, a házirendekről stb.

Mivel a Költségkezelésre szolgáló konfiguráció megtervezése során számos döntés a szervezet hierarchiája és pénzügyi struktúrája alapján történik, az adott területek esetén át kell tekintenie tervezési dokumentumokat.

## <a name="intercompany-expenses"></a>Vállalatközi kiadások

A vállalatközi kiadások engedélyezésekor lehetővé teszi, hogy a jogi személyek és alkalmazottak egy másik jogi személy nevében felmerülő költségeket fizessenek, és a szervezeten belül begyűjtsenek egy fizetést a jogi entitásból. Például az A jogi személy egy alkalmazottja teljesíti a B jogi személy projektjét, és a projekt az utazáshoz kapcsolódó költségeket vállalja. Ha a vállalatközi kiadások engedélyezve vannak, az alkalmazott ezután egy Költségjelentés segítségével benyújthatja a költséget a B jogi entitásnak, és ezt követően a költséget az A jogi entitásnak kell kifizetnie. Ha a szervezetnél nincs több jogi személy, nem kell engedélyeznie a vállalatközi költségeket.

**Döntés:** Engedélyezni szeretné a vállalatközi költségeket?

## <a name="financial-management"></a>Pénzügyi kezelés

A Költségkezelés szorosan integrálódik a szervezet pénzügyi irányításával. A Költségkezelés számos konfigurációja a szervezet pénzügyeit érintő döntéseken alapul majd. A következő szakaszok ismertetik a tervezést és döntéseket igénylő különböző területeket a szervezet pénzügyi döntései és a vezető csapatának útmutatása alapján.

### <a name="per-diems"></a>Napidíjak

Meg kell adnia a szervezet által biztosított alkalmazotti napidíjat. Mivel a napidíjak általában a költségek, például az étkezés, a szállás és az egyéb járulékos kiadások fedezésére szolgálnak, létrehozhatja a szervezet által kínált napidíjra vonatkozó szabályokat. a napidíj az évszaktól, az utazás helyétől vagy mindkettőtől függhet. Amikor napidíjat határoz meg, megadhatja, hogy a napidíj bizonyos százalékát visszatartsák, ha egy dolgozó ingyenes étkezést vagy szolgáltatásokat kap. Meghatározhat napidíjszinteket is, hogy beállítsa azt a minimális és maximális óraszámot is, amelyre a napidíj a dolgozó utazása esetében vonatkozhat.

**Döntés:**

- Alapértelmezett napidíj szabályai az első és az utolsó napra:

    - Mi az a minimális óraszám, amelyet egy alkalmazott igényelhet egy napra, és még mindig megkapja a napidíjat?
    - Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk étkezésre? Ha van csökkentés, mi a csökkentés százalékos aránya?
    - Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk szállásra? Ha van csökkentés, mi a csökkentés százalékos aránya?
    - Csökken az az összeg, amelyet az első nap és az utolsó nap számára kínálunk az egyéb felmerült költségekre? Ha van csökkentés, mi a csökkentés százalékos aránya?

- A napidíjra vonatkozó alapértelmezett szabályok:

    - Van-e százalékos csökkentés a napidíjban az egyes étkezésekre, ha például az étkezés ingyenes? Ha van csökkentés, mi a csökkentés százalékos aránya az egyes étkezéseknél?
    - Az étkezésre vonatkozó csökkentés naponta, utazásonként vagy az étkezések napi száma alapján számolandó?
    - A napidíjban szereplő összegeket a szokásos módon kell lekerekíteni, vagy felkerekíteni?
    - A napidíjat 24 órás időszakra vagy naptári napra számítják?

- A helyen alapuló napidíj-szabályok:

    - A napidíj aránya a helytől függően változik? Milyen helyeket tartalmaz a rendszer?
    - Ha a napidíjak a helytől függően változnak, minden egyes helynél a következő típusú kiadások esetében milyen százalékos összeget biztosít a rendszer:

        - Étkezések
        - Szálloda
        - Egyéb kiadások

### <a name="expense-management-journals-and-accounts"></a>Költségkezelés-naplók és -partnerek

A költségkezeléshez több napló és partner használata szükséges. Meg kell határoznia például, hogy ugyanazt a számlát használják-e a készpénzelőlegek és a hitelkártya-jogviták esetében.

**Döntés:**

- Melyik főkönyvi naplóban szerepelnek a jóváhagyott Költségjelentések?
- Milyen számlát használnak a készpénzelőlegek esetén?
- Azonnal fel kell adni a készpénzelőlegeket?

### <a name="payment-methods"></a>Fizetési módok

Ha lehetővé teszi, hogy az alkalmazottak a vállalat nevében költségeket igényeljenek, meg kell határoznia azokat a fizetési módszereket, amelyeket az alkalmazottak használhatnak. Például lehetővé teheti, hogy az alkalmazottak készpénzt vagy vállalati hitelkártyát használjanak. Előfordulhat, hogy az alkalmazottak személyes hitelkártyát is használhatnak, majd visszafizetik az alkalmazottakat. A következő döntéseket kell meghoznia minden engedélyezett fizetési módra vonatkozóan.

**Döntések:**

- Milyen fizetési módok megengedettek?
- Kihez tartoznak a fizetési mód költségei?
- Van ellenoldali számlatípus? Ha van egy Ellenszámla típusa, mi az?
- Ha van egy Ellenszámla, mi az a számla?
- Ha a fizetési mód hitelkártya, akkor a fizetési módot csak az importált tranzakciókkal lehet használni?

### <a name="expense-categories-and-shared-categories"></a>Költségkategóriák és megosztott kategóriák

Amikor az alkalmazottak költségjelentést készítenek, az általuk rögzített kiadásoknak egy költségkategóriához kell társítva lennie. A költségkategóriák olyan megosztott kategóriákból származnak, amelyek megoszthatók a szervezet jogi entitásai között. Ezek a kategóriák megoszthatók a projektmenedzsmentben és a könyvelésben is, attól függően, hogy milyen módon határozta meg a szervezetet. A szervezet definíciója és a megvalósítási csoport útmutatása alapján meg kell határozni, hogy a költségkezelésben használt kategóriákat csak a költségkezelésben használja a program, vagy meg kell osztania a projektmenedzsment és a könyvelés és költségkezelés között. Felhívjuk figyelmét, hogy ezek a kategóriák megoszthatók a Projekt és Költség, vagy a Projekt és Termelés között, de a Költség és Termelés között nem. Minden egyes költség kategóriára vonatkozóan a következő döntéseket kell meghoznia.

**Döntések:**

- Mi a költségkategória? Ilyenek például a repülőjáratok, a szállodák vagy az útiköltségtérítés kategóriái.
- A költségkategória használható a Projektmenedzsment és könyvelés modulban is?
- Mi a költségtípus?
- Mi a költségkategória alapértelmezett fizetési módja?
- A költség kategóriába tartozó költségeket tételezni kell?
- Mi a költségkategória fő alapértelmezett számlája?
- Mi a költségkategória alapértelmezett cikkáfacsoportja?
- Engedélyezve vannak a költségkategóriához további fizetési módok? Ha további fizetési módok engedélyezettek, mik ezek?
- Vannak alkategóriák ebben a költségkategóriában? Ha vannak alkategóriák, akkor a következő döntéseket kell meghoznia:

    - Van olyan alkategória, amely ki van zárva az adó visszaigényléséből?
    - Mi ezen alkategóriák cikkáfacsoportja?

Ha a költség kategória a projektmenedzsmentben és a könyvelésben is használatban van, válaszolja meg a hátralévő kérdéseket. Ellenkező esetben lépjen a következő szakaszba.

- Milyen költségszámlákat fog használni a következő kiadásokhoz?

    - Költség
    - Bérlista-hozzárendelés
    - Folyamatban lévő termelés költségértéke
    - Költségelem
    - Folyamatban lévő termelés költségérték-eleme
    - Elhatárolt veszteség
    - Folyamatban lévő termelés elhatárolt vesztesége

- Milyen bevételszámlákat fog használni a következőkhöz?

    - Számlázott bevétel
    - Elhatárolt bevétel – Értékesítési érték
    - Folyamatban lévő termelés – értékesítési érték
    - Elhatárolt bevétel – termelés
    - Folyamatban lévő termelés
    - Elhatárolt bevétel – profit
    - Folyamatban lévő termelés – profit
    - Elhatárolt bevétel – előfizetés
    - Folyamatban lévő termelés – előfizetés

### <a name="taxes"></a>Adók

A költséggel kapcsolatos adók esetében meg kell határozni, hogy mi szerepel, illetve van engedélyezve a költségjelentésekben.

**Döntések:**

- Szerepel a költségösszegben az áfa?
- Engedélyezni kell az adókedvezmény használatát a költségeken?

    > [!NOTE]
    > Ha a főkönyv tervezésekor úgy döntött, hogy alkalmazza az USA-beli forgalmi adót és alkalmazza az adószabályokat, nem engedélyezheti az adó-visszaigénylést a költségeknél. (Az Egyesült államokbeli forgalmi adó és az adózási szabályok alkalmazása érdekében állítsa be a **Az ÁFA-adózási szabályok alkalmazása** beállítást **Igen** értékre.)

## <a name="policies"></a>Házirendek

A költségjelentés-házirendek létrehozásával segítséget nyújthat a szervezet számára, hogy időt és pénzt takarítson meg abban az esetben, ha az alkalmazottak költséget jelentenek a nevében. A házirendek segítségével garantálható, hogy az alkalmazottak betartják a költségvetést, megadják az összes szükséges információt, és csak a számukra szükséges pénzt költik el. Minden egyes költségjelentési házirendre és a létrehozott Költségjelentés-jóváhagyási házirendre vonatkozóan a következő döntéseket kell meghoznia.

**Döntések:**

- Mi a szabályzat neve?
- Mire vonatkozik a költséggel kapcsolatos irányelv?
- Ha korábban úgy döntött, hogy engedélyezi a vállalatközi kiadásokat, a szervezethez tartozó melyik vállalatokra vonatkozik ez a szabályzat?
- Mikor válik hatályossá a házirend?
- Mikor jár le a házirend?
- Mi a házirendi szabály?
- Mi a házirendi szabály kimenete?
