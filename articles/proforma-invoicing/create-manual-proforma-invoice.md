---
title: Kézi proforma számla létrehozása
description: Ez a témakör a proforma számlák létrehozását ismerteti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3289b8bcaddaebe1a3657b5902c1d324f9e0fd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287781"
---
# <a name="create-a-manual-proforma-invoice"></a>Kézi proforma számla létrehozása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A számlázás használata esetén a projektvezetők egy második szintű jóváhagyást kapnak, mielőtt elkészítik a számlákat az ügyfelek számára. Az első szintű jóváhagyás akkor fejeződik be, amikor a projektcsoport tagjai által benyújtott idő- és költségbejegyzéseket jóváhagyják.

A Dynamics 365 Project Operations rendszert nem az ügyféloldali számlák előállítására tervezték, a következő okok miatt:

- Nem tartalmaz adóinformációkat.
- Megfelelően beállított árfolyamok használatával sem válthat át más valutákat a számlázási pénznemre.
- Nem tudja úgy formázni a számlákat, hogy kinyomtathatók legyenek.

A létrehozott számlajavaslatokból származó információkat használó ügyféloldali számlák létrehozására ehelyett használhat pénzügyi vagy számviteli rendszert.

## <a name="creating-project-invoices"></a>Projektszámlák létrehozása

A projektszámlák egyenként vagy ömlesztve hozhatók létre. Ezeket kézzel is létrehozhatja, vagy beállíthatja, hogy automatikus futtatások során jöjjenek létre.

### <a name="manually-create-project-invoices"></a>Projektszámlák kézi létrehozása 

A **Projektszerződések** lista oldalon létrehozhat projektszámlákat külön-külön minden egyes projektszerződéshez, illetve ömlesztve, ha több projektszerződésről van szó.

Kövesse ezeket a lépéseket egy adott projektszerződés számlájának létrehozásához.

- A **Projektszerződések** listán nyissa meg a projektszerződést, majd válassza a **Számla létrehozása** lehetőséget.

    Egy számla készül az összes tranzakcióhoz azon kiválasztott projekt szerződés esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, a mérföldköveket és a termékalapú szerződési sorokat.

Kövesse ezeket a lépéseket az ömlesztett számlák létrehozásához.

1. A **Projektszerződések** listán válasszon ki egy vagy több projektszerződést, amelyhez számlát kell létrehoznia, majd válassza a **Projektszámlák létrehozása** lehetőséget.

    Egy figyelmeztető üzenet tájékoztatja arról, hogy a számlák létrehozása némileg késhet. Ezzel egyidejűleg a folyamat is látható.

2. Az üzenetablak bezárásához válassza az **OK** lehetőséget.

    Egy számla kerül létrehozásra valamennyi tranzakcióhoz olyan szerződéssor esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, a mérföldköveket és a termékalapú szerződési sorokat.

3. A létrehozott számlák megtekintéséhez lépjen az **Értékesítés** \> **Számlázás** \> **Számlák** pontra. Mindegyik projekt-szerződéshez egy számlát fog látni.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektszámlák automatikus létrehozásának beállítása 

Automatikus számlafuttatás a következő lépésekkel állítható be.

1. Lépjen a **Beállítások** \> **Kötegelt feladatok** menüpontra.
2. Hozzon létre egy kötegelt feladatot, és adja neki a **Project operations számlák létrehozása** nevet. A kötegelt feladat nevének tartalmaznia kell a „Számlák létrehozása” kifejezést.
3. A **Feladat típusa** mezőben válassza a **Nincs** lehetőséget. Alapértelmezés szerint a **Napi gyakoriság** és az **Aktív** opciók értéke **Igen**.
4. Válassza a **Munkamenet futtatása** lehetőséget. A **Rekord keresése** párbeszédpanelen három munkafolyamatot láthat:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Válassza a **ProcessRunCaller** elemet, majd a **Hozzáadás** lehetőséget.
6. A következő párbeszédpanelen válassza az **OK** lehetőséget. Az **Alvás** munkafolyamatot egy **Folyamat** munkafolyamat követi.

    Az 5. lépésben a **ProcessRunner** lehetőséget is választhatja. Ezt követően, ha az **OK** lehetőséget választja, a **Folyamat** munkafolyamatot egy **Alvás** munkafolyamat követi.

A **ProcessRunCaller** és a **ProcessRunner** munkafolyamatok számlákat hoznak létre. **A ProcessRunCaller** munkafolyamat meghívja a **ProcessRunner** munkafolyamatot. A **ProcessRunner** az a munkafolyamat, amely ténylegesen létrehozza a számlákat. Végighalad az összes szerződési soron, amelyhez számlákat kell létrehozni, és számlákat hoz létre ezekre a sorokhoz. Azon szerződési sorok meghatározásához, amelyekhez számlákat kell létrehozni, a feladat megvizsgálja a szerződési sorok számlafuttatási dátumait. Ha az adott szerződéshez tartozó szerződési sorok egyazon számlafuttatási dátummal rendelkeznek, a tranzakciók egyetlen számlába kerülnek egyesítésre, amely két számlasorral fog rendelkezni. Ha nincsenek tranzakciók a számlák létrehozására, akkor a feladat kihagyja a számla létrehozását.

Miután a **ProcessRunner** munkafolyamat futtatása befejeződött, meghívja a **ProcessRunCaller** munkafolyamatot, megadja a befejezési időt, és bezáródik. A **ProcessRunCaller** ezután elindít egy időzítőt, amely a megadott befejezési időtől kezdve 24 órán át működik. Az időzítő végén a **ProcessRunCaller** bezáródik.

A számlák létrehozására szolgáló kötegelt folyamat feladat ismétlődő feladat. Ha ezt a kötegelt folyamatot többször futtatja, akkor a feladatból több példány jön létre, és hibákat okoz. Ezért a kötegelt folyamatot csak egyszer kell elindítania, és csak akkor kell újraindítania, ha az leáll.

> [!NOTE]
> A kötegelt számlázás csak a számlázási ütemezések szerint konfigurált projektek szerződéssoraihoz fut. A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges. Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását. Ugyanez érvényes a projektalapú szerződéssor esetében is.      
 
### <a name="edit-a-draft-invoice"></a>Számlatervezet szerkesztése

Projektszámla-vázlat létrehozásakor minden olyan még nem számlázott értékesítési tranzakció, amelyet az idő- és költségbejegyzésének jóváhagyásának időpontjában hoztak létre, a számlára kerül. A számla vázlatos szakaszában a következő módosításokat végezheti el:

- A számlasor részleteinek törlése vagy módosítása.
- A mennyiség és a számlázási típus szerkesztése és módosítása.
- Idők, költsségek és díjak közvetlen hozzáadása a számlához tranzakcióként. Ezt a funkciót akkor használhatja, ha a számlasor olyan szerződési sorra van leképezve, amely lehetővé teszi ezeket a tranzakciós osztályokat.

A számla megerősítéséhez válassza a **Megerősítés** lehetőséget. A Megerősítés egyirányú művelet. Ha a **Megerősítés** lehetőséget választja, a rendszer a számlát csak olvashatóvá teszi, és tényleges számlázott értékesítési értékeket hoz létre az egyes számlasorok adatairól. Ha a számlasor-adat egy nem számlázott tényleges értékesítésre mutat, akkor a rendszer a nem számlázott értékesítési értéket is megfordítja. (Azon számlasor-adatok, amelyeket egy idő- vagy költségbejegyzés alapján hoztak létre, egy nem számlázott tényleges értékesítésre vonatkoznak.) A főkönyvi integrációs rendszerek ezt a visszafordítást felhasználhatják a folyamatban lévő projektmunka (WIP) megfordítására, számviteli célokból.

### <a name="correct-a-confirmed-invoice"></a>Megerősített számla kijavítása

A megerősített számlák szerkeszthetők (korrigálhatók). Megerősített számla kijavításakor új korrekciós számlavázlat jön létre. Mivel a feltételezés az, hogy meg akarja fordítani az eredeti számla összes tranzakcióját és mennyiségeéét, ez a korrekciós számla tartalmazza az eredeti számla összes tranzakcióját, és az összes mennyisége 0 (nulla).

Ha bármely tranzakció nem igényel javítást, akkor eltávolíthatja azt a korrekciós számlavázlatból. Ha csak részleges mennyiséget kíván megfordítani, vagy visszatéríteni, az adatsor részleteit a **Mennyiség** mezőben. Ha kinyitja a számlasor részleteit, láthatja az eredeti számlamennyiséget. Ezután módosíthatja az aktuális számlamennyiséget oly módon, hogy az kevesebb vagy több legyen, mint az eredeti számlamennyiség.

A korrekciós számla megerősítésekor az eredetileg számlázott tényleges értékesítés megfordul, és létrejön egy újonnan számlázott tényleges értékesítés. Ha a mennyiséget csökkentették, a különbség egy új, nem számlázott értékesítés létrehozását is eredményezi. Ha például az eredeti számlázott értékesítés nyolc órán keresztül történt, és a korrekciós számla sorában lévő részlet hat óra, a rendszer megfordítja az eredeti számlázott értékesítési sort, és két új aktuális értéket hoz létre:

- Hat órás tényleges számlázott értékesítés.
- Nem számlázott tényleges értékesítés a fennmaradó két órára. Ezt a tranzakciót később számlázhatják, vagy pedig díjmentesnek jelölhetik, az ügyféllel folytatott tárgyalásoktól függően.


[!INCLUDE[footer-include](../includes/footer-banner.md)]