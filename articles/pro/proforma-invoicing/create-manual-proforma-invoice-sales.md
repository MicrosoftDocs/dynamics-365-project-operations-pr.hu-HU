---
title: Proforma projektszámlák
description: Ez a cikk a Projektműveletek proforma projektszámláiról nyújt tájékoztatást.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934553"
---
# <a name="proforma-project-invoices"></a>Proforma projektszámlák

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Proforma projektszámlázás azért hasznos, mert a projektvezetőknek egy második szintű jóváhagyást biztosít, mielőtt számlákat készítenek az ügyfelek számára. Az első szintű jóváhagyás akkor fejeződik be, amikor a projektcsoport tagjai által benyújtott idő-, költség- és anyagbejegyzéseket jóváhagyják.

A Dynamics 365 Project Operations Lite Deployment szolgáltatást nem ügyféloldali számlák létrehozására tervezték. Az alábbi lista azt mutatja, hogy miért nem lehet számlákat létrehozni:

- Nem tartalmaz adóinformációkat.
- Más pénznemek nem válthatók át a számlázási pénznemre.
- A nyomtatáshoz nem lehet helyesen formázni a számlákat.

Ehelyett pénzügyi vagy számviteli rendszert használhat az ügyféloldali számlák létrehozására, amelyek felhasználják a létrehozott számlajavaslatokból származó információkat.

## <a name="creating-project-invoices"></a>Projektszámlák létrehozása

A projektszámlák egyenként vagy ömlesztve hozhatók létre. Ezeket kézzel is létrehozhatja, vagy beállíthatja, hogy automatikus futtatások során jöjjenek létre.

### <a name="manually-create-project-invoices"></a>Projektszámlák kézi létrehozása 

A **Projektszerződések** lista oldalon létrehozhat projektszámlákat külön-külön minden egyes projektszerződéshez, illetve ömlesztve, ha több projektszerződésről van szó.

   - Ahhoz, hogy a **Projektszerződések** listaoldalon létrehozhasson számlát egy adott projektszerződéshez, nyisson meg egy projektszerződést, majd válassza ki a **Számla létrehozása** lehetőséget.

   Egy számla készül az összes tranzakcióhoz azon kiválasztott projekt szerződés esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, az anyagokat, a mérföldköveket, a termékalapú szerződéssorokat és az egyéb számlázatlan értékesítési naplósorokat, amelyek lehet, hogy jóvá lettek hagyva.

Számlák ömlesztett létrehozása:

1. A **Projektszerződések** listán válasszon ki egy vagy több projektszerződést, amelyhez számlát szeretne létrehozni, majd válassza a **Projektszámlák létrehozása** lehetőséget.
2. Egy figyelmeztető üzenet tájékoztatja arról, hogy a számlák létrehozása némileg késhet. Ezzel egyidejűleg a folyamat is látható. Az üzenetablak bezárásához válassza az **OK** lehetőséget.

   Egy számla kerül létrehozásra valamennyi tranzakcióhoz olyan szerződéssor esetén, amely állapota **Számlázásra kész**. Ezek a tranzakciók magukban foglalják az időt, a költségeket, az anyagokat, a mérföldköveket, a termékalapú szerződéssorokat és az egyéb számlázatlan értékesítési naplósorokat, amelyek lehet, hogy jóvá lettek hagyva.

3. A létrehozott számlák megtekintéséhez menjen az **Értékesítés** \> **Számlázás** \> **Számlák** pontra. Mindegyik projekt-szerződéshez egy számlát fog látni.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektszámlák automatikus létrehozásának beállítása 

Automatikus számlafuttatás a következő lépésekkel állítható be.

1. Lépjen a **Beállítások** \> **Kötegelt feladatok** menüpontra.
2. Hozzon létre egy kötegelt feladatot, és adja neki a **Project operations számlák létrehozása** nevet. A kötegelt feladat nevének tartalmaznia kell a „Számlák létrehozása” kifejezést.
3. A **Feladat típusa** mezőben válassza a **Nincs** lehetőséget. Alapértelmezés szerint a **Napi gyakoriság** és az **Aktív** opciók értéke **Igen**.
4. Válassza a **Munkamenet futtatása** lehetőséget. A **Rekord keresése** párbeszédpanelen az alábbi munkafolyamatokat láthatja:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Válassza a **ProcessRunCaller** elemet, majd a **Hozzáadás** lehetőséget.
6. A következő párbeszédpanelen válassza az **OK** lehetőséget. Az **Alvás** munkafolyamatot egy **Folyamat** munkafolyamat követi.

    Az 5. lépésben a **ProcessRunner** lehetőséget is választhatja. Ezt követően, ha az **OK** lehetőséget választja, a **Folyamat** munkafolyamatot egy **Alvás** munkafolyamat követi.

A **ProcessRunCaller** és a **ProcessRunner** munkafolyamatok számlákat hoznak létre. **A ProcessRunCaller** munkafolyamat meghívja a **ProcessRunner** munkafolyamatot. A **ProcessRunner** az a munkafolyamat, amely létrehozza a számlákat. Ez a munkafolyamat végighalad az összes szerződéssoron, amelyhez számlákat kell létrehozni, és számlákat hoz létre. Azon szerződési sorok meghatározásához, amelyekhez számlákat kell létrehozni, a munkafolyamat megvizsgálja a szerződési sorok számlafuttatási dátumait. Ha az adott szerződéshez tartozó szerződési sorok egyazon számlafuttatási dátummal rendelkeznek, a tranzakciók egyetlen számlába kerülnek egyesítésre, amely két számlasorral fog rendelkezni. Ha nincsenek tranzakciók a számlák létrehozására, akkor egy számla sem lesz létrehozva.

Miután a **ProcessRunner** munkafolyamat futtatása befejeződött, meghívja a **ProcessRunCaller** munkafolyamatot, megadja a befejezési időt, és bezáródik. A **ProcessRunCaller** ezután elindít egy időzítőt, amely a megadott befejezési időtől kezdve 24 órán át működik. Az időzítő végén a **ProcessRunCaller** bezáródik.

A számlák létrehozására szolgáló kötegelt folyamat feladat ismétlődő feladat. Ha ezt a kötegelt folyamatot többször futtatja, akkor a feladatból több példány jön létre, és hibákat okozhat. A probléma megoldásához a kötegelt folyamatot csak egyszer szabad elindítania, és csak akkor indítsa újra, ha az leáll.

> [!NOTE]
> A kötegelt számlázás csak a számlázási ütemezések szerint konfigurált projektek szerződéssoraihoz fut. A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges. Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását. Ugyanez érvényes a projektalapú szerződéssor esetében is.      
 
### <a name="edit-a-draft-invoice"></a>Számlatervezet szerkesztése

Projektszámla-vázlat létrehozásakor minden olyan még nem számlázott értékesítési tranzakció, amelyet az idő- és költségbejegyzésének jóváhagyásának időpontjában hoztak létre, a számlára kerül. A számla vázlatos szakaszában a következő módosításokat végezheti el:

- A számlasor részleteinek törlése vagy módosítása.
- A mennyiség és a számlázási típus szerkesztése és módosítása.
- Idők, költsségek, anyagok és díjak közvetlen hozzáadása a számlához tranzakcióként. Ezt a funkciót akkor használhatja, ha a számlasor olyan szerződési sorra van leképezve, amely lehetővé teszi ezeket a tranzakciós osztályokat.

A számla megerősítéséhez válassza a **Megerősítés** lehetőséget. Ez egy egyirányú művelet. Ha a **Megerősítés** lehetőséget választja, a számla csak olvashatő lesz, és tényleges számlázott értékesítési értékeket hoz létre az egyes számlasorok adatairól. Ha a számlasor-adat egy nem számlázott tényleges értékesítésre mutat, akkor a nem számlázott értékesítési érték megfordul. Az idő-, költség- vagy anyagfelhasználási tételből létrehozott számlasor-részletek nem számlázott tényleges értékesítésre hivatkoznak. A főkönyvi integrációs rendszerek ezt a sztornírozást használhatják a folyamatban lévő projektmunka (WIP) könyveléséhez.

### <a name="correct-a-confirmed-invoice"></a>Megerősített számla kijavítása

A megerősített számlák szerkeszthetők. Megerősített számla kijavításakor új korrekciós számlavázlat jön létre. Mivel a feltételezés az, hogy meg akarja fordítani az eredeti számla összes tranzakcióját és mennyiségeéét, ez a korrekciós számla tartalmazza az eredeti számla összes tranzakcióját, és az összes mennyisége nulla.

Ha van olyan tranzakció, amely nem igényel javítást, akkor eltávolíthatja azt a korrekciós számlavázlatból. Ha csak részleges mennyiséget kíván megfordítani, vagy visszatéríteni, az adatsor részleteit a **Mennyiség** mezőben. Ha kinyitja a számlasor részleteit, láthatja az eredeti számlamennyiséget. Ezután módosíthatja az aktuális számlamennyiséget oly módon, hogy az kevesebb vagy több legyen, mint az eredeti számlamennyiség.

A korrekciós számla megerősítésekor az eredetileg számlázott tényleges értékesítés megfordul, és létrejön egy újonnan számlázott tényleges értékesítés. Ha a mennyiséget csökkentették, a különbség egy új, nem számlázott értékesítés létrehozását eredményezi. Ha például az eredeti számlázott értékesítés nyolc órán keresztül történt, és a korrekciós számla sorában lévő részlet hat óra, a rendszer megfordítja az eredeti számlázott értékesítési sort, és két új aktuális értéket hoz létre:

- Hat órás tényleges számlázott értékesítés.
- Nem számlázott tényleges értékesítés a fennmaradó két órára. Ezt a tranzakciót később számlázhatják, vagy díjmentesnek jelölhetik, az ügyféllel folytatott tárgyalásoktól függően.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
