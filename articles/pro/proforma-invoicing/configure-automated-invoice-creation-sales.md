---
title: Automatikus számlalétrehozás beállítása
description: Ez a cikk a proforma számlák automatikus létrehozásának beállításáról és konfigurálásáról nyújt tájékoztatást.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5160b22bd0d8a738c31a5105d83bd15cf136fab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911734"
---
# <a name="set-up-automatic-invoice-creation"></a>Automatikus számlalétrehozás beállítása 
 
_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Konfigurálhatja az automatikus számlalétrehozást a Dynamics 365 Project Operationsben. A rendszer egy proforma számlát hoz létre, amely az egyes projektek és szerződéssorok számlázási ütemezése alapján készült. A számlázási ütemezések a szerződéssorok szintjén konfigurálhatók. A szerződés minden sora rendelkezhet külön számlázási ütemezéssel, vagy ha a szerződés minden sorában ugyanazt a számlázási ütemezést lehet is lehet használni.

A számla létrehozásakor a rendszer mindig legalább egy számlát hoz létre projektszerződésenként. Bizonyos esetekben több számla is létrehozható. Ha például a szerződés több ügyfelet tartalmaz, ugyanannyi számla jön létre, mint azoknak az ügyfeleknek a száma, akiknek számlázható tranzakciói vannak a projekt szerződésben.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Ebből a részből megtudhatja, hogyan kerülnek a tranzakciók egy számlára 

Időnként minden projektalapú szerződéssor külön számlázási ütemezést határoz meg. Például az Adatum szerződés megvalósítási szolgáltatásai az alábbi szerződéssorokat tartalmazzák:

- Prototípusmunka, amely rögzített árú, két kézzel létrehozott mérföldkővel.
- A bevezetési munkák időpontot foglalnak magukban, és kéthetente, hétfőnként lesznek számlázva.
- A felmerült költségeket, amelyeket havonta kell kiszámlázni minden hónap első hétfőjén.

A két sorra vonatkozóan meghatározott számlázási ütemezések a következő táblázatban láthatók:

| Szerződéssor | Számlakészítés dátuma | Tranzakció határideje | Mérföldkő dátuma | Mérföldkő összege |
| --- | --- | --- | --- | --- |
| Prototípusmunka | Október 5., hétfő | - | Október 5., hétfő | 5000 USD |
| - | November 3., kedd | - | November 3., kedd | 12,000 USD |
| Bevezetési munka | Október 5., hétfő | Október 4., vasárnap | - | - |
| - | Október 19., hétfő | Október 18., vasárnap | - | - |
| - | November 2., hétfő | November 1., vasárnap | - | - |
| - | November 16., hétfő | November 15., vasárnap | - | - |
| Felmerült kiadások | Október 5., hétfő | Október 4., vasárnap | - | - |
| - | November 2., hétfő | November 1., vasárnap | - | - |

Ebben a példában, amikor az automatikus számlázás fut:

- **Október 4. vagy bármely korábbi időpont**: Nem jön létre számla a szerződéshez, mert az egyes szerződéssorok **Számlázási ütemezés** táblázata nem hívja meg a számla futási dátumaként az október 4., vasárnap dátumot.
- **Október 5., hétfő**: Egy számla a következőhöz jön létre:

    - A mérföldkövet tartalmazó számító prototípus-mű, ha a **Számlázásra kész** értékkel van megjelölve.
    - A bevezetési munkák közé tartozik az összes Időtranzakció, amelyet a tranzakció zárási dátuma előtt hoztak létre. október 4., vasárnap előtt, ennek értéke **Számlázásra kész**.
    - A felmerült költségek közé tartozik az összes költségtranzakció, amelyet a tranzakció zárási dátuma előtt hoztak létre. október 4., vasárnap előtt, ennek értéke **Számlázásra kész**.
  
- **Október 6. vagy bármely október 19. előtti időpont**: Nem jön létre számla a szerződéshez, mert az egyes szerződéssorok **Számlázási ütemezés** táblázata nem hívja meg a számla futási dátumaként október 6. és október 19 közötti dátumot.
- **Október 19,. hétfő** Egy számla lesz generálva a bevezetési munkákhoz ami az összes Időtranzakciót tartalmazza, amelyet a tranzakció zárási dátuma előtt hoztak létre. október 18., vasárnap előtt, ennek értéke **Számlázásra kész**.
- **November 2., hétfő**: Egy számla a következőhöz jön létre:

    - A bevezetési munkák közé tartozik az összes Időtranzakció, amelyet a tranzakció zárási dátuma előtt hoztak létre. November 1., vasárnap előtt, ennek értéke **Számlázásra kész**.
    - A felmerült költségek közé tartozik az összes költségtranzakció, amelyet a tranzakció zárási dátuma előtt hoztak létre. november 1., vasárnap előtt, ennek értéke **Számlázásra kész**.

- **November 3., kedd** : Egy számla jön létre a prototípus munkára, amely tartalmazza a 12000 USD értékű mérföldkövet, ha meg van jelölve, **Számlázásra kész** értékkel.

## <a name="configure-automatic-invoicing"></a>Automatikus számlázás konfigurálása

Automatikus számlafuttatás a következő lépések elvégzésével állítható be.

1. A **Project Operations** alatt nyissa meg a **Beállítások** > **Ismétlődő számla beállítása** lehetőséget.
2. Hozzon létre egy kötegelt feladatot, és adja neki a **Project operations számlák létrehozása** nevet. A kötegelt feladat nevének tartalmaznia kell a „számlák létrehozása” szavakat.
3. A **Feladat típusa** mezőben válassza a **Nincs** lehetőséget. Alapértelmezés szerint a **Napi gyakoriság** és az **Aktív** mezők értéke **Igen**.
4. Válassza a **Munkamenet futtatása** lehetőséget. A **Rekord keresése** párbeszédpanelen három munkafolyamatot láthat:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Válassza a **ProcessRunCaller** elemet, majd a **Hozzáadás** lehetőséget.
6. A következő párbeszédpanelen válassza az **OK** lehetőséget. Az **Alvás** munkafolyamatot egy **Folyamat** munkafolyamat követi. 

> [!NOTE]
> Az 5. lépésben a **ProcessRunner** lehetőséget is választhatja. Ezt követően, ha az **OK** lehetőséget választja, a **Folyamat** munkafolyamatot egy **Alvás** munkafolyamat követi.

A **ProcessRunCaller** és a **ProcessRunner** munkafolyamatok számlákat hoznak létre. **A ProcessRunCaller** munkafolyamat meghívja a **ProcessRunner** munkafolyamatot. A **ProcessRunner** az a munkafolyamat, amely ténylegesen létrehozza a számlákat. A munkafolyamat végighalad az összes szerződési soron, amelyhez számlákat kell létrehozni, és számlákat hoz létre ezekre a sorokhoz. Azon szerződési sorok meghatározásához, amelyekhez számlákat kell létrehozni, a feladat megvizsgálja a szerződési sorok számlafuttatási dátumait. Ha az adott szerződéshez tartozó szerződési sorok egyazon számlafuttatási dátummal rendelkeznek, a tranzakciók egyetlen számlába kerülnek egyesítésre, amely két számlasorral fog rendelkezni. Ha nincsenek tranzakciók a számlák létrehozására, akkor a feladat kihagyja a számla létrehozását.

Miután a **ProcessRunner** munkafolyamat futtatása befejeződött, meghívja a **ProcessRunCaller** munkafolyamatot, megadja a befejezési időt, és bezáródik. A **ProcessRunCaller** ezután elindít egy időzítőt, amely a megadott befejezési időtől kezdve 24 órán át működik. Az időzítő végén a **ProcessRunCaller** bezáródik.

A számlák létrehozására szolgáló kötegelt folyamat feladat ismétlődő feladat. Ha ezt a kötegelt folyamatot többször futtatja, akkor a feladatból több példány jön létre, és hibákat okoz. Ezért a kötegelt folyamatot csak egyszer kell elindítania, és csak akkor kell újraindítania, ha az leáll.

> [!NOTE]
> A kötegelt számlázás a Project Operations alkalmazásban csak a számlázási ütemezések szerint konfigurált projektek szerződéssoraihoz fut. A rögzített árú számlázási móddal rendelkező szerződéssornál a mérföldkövek konfigurálása szükséges. Az idő-és anyagelszámolású számlázási móddal rendelkező projekt-szerződéssorok esetében el kell végezni a dátum alapú számlázási ütemezés beállítását.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
