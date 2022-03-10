---
title: Számlázás a Project Service Automation alkalmazásban
description: Ez a témakör a számlázással kapcsolatban nyújt információkat.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 58259c05939cfe870ce5e36b4a0221cd93b8e8d2b4be582efc9167e82579699e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985504"
---
# <a name="invoicing-in-project-service-automation"></a>Számlázás a Project Service Automation alkalmazásban

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation alkalmazásban végzett számlázás azért hasznos, mert a projektvezetőknek egy második szintű jóváhagyást biztosít, mielőtt számlákat készítenek az ügyfelek számára. Az első szintű jóváhagyás akkor fejeződik be, amikor a projektcsoport tagjai által benyújtott idő- és költségbejegyzéseket jóváhagyják.

A PSA-t nem az ügyféloldali számlák előállítására tervezték, a következő okok miatt:

- Nem tartalmaz adóinformációkat.
- Megfelelően beállított árfolyamok használatával sem válthat át más valutákat a számlázási pénznemre.
- Nem tudja úgy formázni a számlákat, hogy kinyomtathatók legyenek.

Ehelyett pénzügyi vagy számviteli rendszert használhat az ügyféloldali számlák létrehozására, amelyek felhasználják a PSA-ban létrehozott számlajavaslatokból származó információkat.

## <a name="creating-project-invoices-in-psa"></a>Projektszámlák létrehozása a PSA-ban

A projektszámlák egyenként vagy ömlesztve hozhatók létre. Ezeket kézzel is létrehozhatja, vagy beállíthatja, hogy automatikus futtatások során jöjjenek létre.

### <a name="manually-create-project-invoices-in-psa"></a>Projektszámlák kézi létrehozása a PSA-ban

A **Projektszerződések** lista oldalon létrehozhat projektszámlákat külön-külön minden egyes projektszerződéshez, illetve ömlesztve, ha több projektszerződésről van szó.

Kövesse ezeket a lépéseket egy adott projektszerződés számlájának létrehozásához.

- A **Projektszerződések** listán nyissa meg a projektszerződést, majd válassza a **Számla létrehozása** lehetőséget.

    ![Projektszámlák létrehozása egy adott projektszerződéshez.](media/CreateProjectInvoicesOneByOne.png)

    Egy számla készül az összes tranzakcióhoz azon kiválasztott projekt szerződés esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, a mérföldköveket és a termékalapú szerződési sorokat.

Kövesse ezeket a lépéseket az ömlesztett számlák létrehozásához.

1. A **Projektszerződések** listán válasszon ki egy vagy több projektszerződést, amelyhez számlát kell létrehoznia, majd válassza a **Projektszámlák létrehozása** lehetőséget.

    ![Projektszámlák ömlesztett létrehozása.](media/CreateProjectInvoicesBulk.png)

    Egy figyelmeztető üzenet tájékoztatja arról, hogy a számlák létrehozása némileg késhet. Ezzel egyidejűleg a folyamat is látható.

2. Az üzenetablak bezárásához válassza az **OK** lehetőséget.

    Egy számla kerül létrehozásra valamennyi tranzakcióhoz olyan szerződéssor esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, a mérföldköveket és a termékalapú szerződési sorokat.

3. A létrehozott számlák megtekintéséhez lépjen az **Értékesítés** \> **Számlázás** \> **Számlák** pontra. Mindegyik projekt-szerződéshez egy számlát fog látni.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Projektszámlák automatikus létrehozásának beállítása a PSA-ban

Kövesse ezeket a lépéseket a PSA-ban egy automatikus számlafuttatásnak történő beállításához.

1. Lépjen a **Project Service** \> **Beállítások** \> **Kötegelt feladatok** pontra.
2. Hozzon létre egy kötegelt feladatot, és adja neki a **PSA számlák létrehozása** nevet. A kötegelt feladat nevének tartalmaznia kell a „Számlák létrehozása” kifejezést.
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
> A Project Service Automation alkalmazásban a kötegelt számlázás csak azoknál a projekt-szerződéssoroknál fut, amelyeket a számlák ütemezései konfigurálnak. A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges. Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását. A számlázási gyakoriság egy ajánlati soron alapuló projekt környezetében történő beállításával kapcsolatos információk az [Árajánlatok és árajánlatsorok](basic-quote-lines.md#invoice-schedule) témakörben találhatók. Ugyanez érvényes a projektalapú szerződéssor esetében is.      
 
### <a name="edit-a-draft-psa-invoice"></a>PSA számlavázlat szerkesztése

Projektszámla-vázlat létrehozásakor minden olyan még nem számlázott értékesítési tranzakció, amelyet az idő- és költségbejegyzésének jóváhagyásának időpontjában hoztak létre, a számlára kerül. A számla vázlatos szakaszában a következő módosításokat végezheti el:

- A számlasor részleteinek törlése vagy módosítása.
- A mennyiség és a számlázási típus szerkesztése és módosítása.
- Idők, költsségek és díjak közvetlen hozzáadása a számlához tranzakcióként. Ezt a funkciót akkor használhatja, ha a számlasor olyan szerződési sorra van leképezve, amely lehetővé teszi ezeket a tranzakciós osztályokat.

A számla megerősítéséhez válassza a **Megerősítés** lehetőséget. A Megerősítés egyirányú művelet. Ha a **Megerősítés** lehetőséget választja, a rendszer a számlát csak olvashatóvá teszi, és tényleges számlázott értékesítési értékeket hoz létre az egyes számlasorok adatairól. Ha a számlasor-adat egy nem számlázott tényleges értékesítésre mutat, akkor a rendszer a nem számlázott értékesítési értéket is megfordítja. (Azon számlasor-adatok, amelyeket egy idő- vagy költségbejegyzés alapján hoztak létre, egy nem számlázott tényleges értékesítésre vonatkoznak.) A főkönyvi integrációs rendszerek ezt a visszafordítást felhasználhatják a folyamatban lévő projektmunka (WIP) megfordítására, számviteli célokból.

### <a name="correct-a-confirmed-psa-invoice"></a>Megerősített PSA száml a kijavítása

A megerősített PSA számlák szerkeszthetők (korrigálhatók). Megerősített számla kijavításakor új korrekciós számlavázlat jön létre. Mivel a feltételezés az, hogy meg akarja fordítani az eredeti számla összes tranzakcióját és mennyiségeéét, ez a korrekciós számla tartalmazza az eredeti számla összes tranzakcióját, és az összes mennyisége 0 (nulla).

Ha bármely tranzakció nem igényel javítást, akkor eltávolíthatja azt a korrekciós számlavázlatból. Ha csak részleges mennyiséget kíván megfordítani, vagy visszatéríteni, az adatsor részleteit a **Mennyiség** mezőben. Ha kinyitja a számlasor részleteit, láthatja az eredeti számlamennyiséget. Ezután módosíthatja az aktuális számlamennyiséget oly módon, hogy az kevesebb vagy több legyen, mint az eredeti számlamennyiség.

A korrekciós számla megerősítésekor az eredetileg számlázott tényleges értékesítés megfordul, és létrejön egy újonnan számlázott tényleges értékesítés. Ha a mennyiséget csökkentették, a különbség egy új, nem számlázott értékesítés létrehozását is eredményezi. Például, ha az eredeti számlázott értékesítés nyolc órán keresztül történt, és a korrekciós számla sor részlete kevesebb, mint hat óra, a PSA megfordítja az eredeti számlázott értékesítési sort, és két új aktuális értéket hoz létre:

- Hat órás tényleges számlázott értékesítés.
- Nem számlázott tényleges értékesítés a fennmaradó két órára. Ezt a tranzakciót később számlázhatják, vagy pedig díjmentesnek jelölhetik, az ügyféllel folytatott tárgyalásoktól függően.


[!INCLUDE[footer-include](../includes/footer-banner.md)]