---
title: Szállítói számlák létrehozása
description: Ez a cikk ismerteti a szállítói számlák fogalmát, és ismerteti azok létrehozási módszerét a Microsoft Dynamics 365 Project Operations alkalmazásban.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475467"
---
# <a name="create-vendor-invoices"></a>Szállítói számlák létrehozása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A cikkben ismertetett funkciók használatához engedélyeznie kell a **Szolgáltatáskezelés** munkaterületén az **Alvállalkozói tényadatok feldolgozásának engedélyezése a Project Operations alkalmazással erőforrás alapú forgatókönyvekben** funkciót.

A Microsoft Dynamics 365 Project Operations alkalmazásban a szállítói számlázás a szállítók által a projekten elvégzett szolgáltatásokból és/vagy anyagokból származó költségek rögzítésére használható.

Amikor szolgáltatásokat és/vagy anyagokat alvállalkozásba ad egy beszállítónak, az alvállalkozói szerződés az adott szállítóval kötött szerződéses megállapodást képviseli. Amint az szállító teljesíti a szolgáltatásokat, vagy ahogy az anyagokat megérkeztek és felhasználták a projektfeladatok során, a költségeket a projekthez rögzíti a rendszer. Ezt követően a szállító időszakosan számlákat küld. Ezeket a számlákat ellenőrzik és megfelelteti a projektben rögzített költségekhez. Az ellenőrzési folyamat befejezése után a a szállító számlája meg lesz erősítve, és engedélyezve lesz a kifizetése.

## <a name="scenarios-for-use"></a>Használati forgatókönyvek

A Project Operations alkalmazásban szereplő szállítói számlák két különböző forgatókönyv támogatására használhatók:

- Az ügyfelek, akik a teljes alvállalkozói élményt használják.
- Az ügyfelek, akik nem használják a teljes alvállalkozói élményt, de egységes képben nézetet látni a projektek költségeiről a Project Operations alkalmazásban.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Az ügyfelek, akik a teljes alvállalkozói élményt használják

A szállítói számla élmények lehetőséget biztosítanak az alvállalkozó által alvállalkozásba adott összetevőkre hivatkozó idő-, anyaghasználati és költségbejegyzések ellenőrzésére, valamint a szállítói számlasorokkal való egyeztetésére. Ezzel a folyamattal ellenőrizhető a szállítói számlasorok pontossága. Az ellenőrzési folyamat befejezése és a szállítói számla jóváhagyása után a rendszer visszavonja a jóváhagyott idő-, költség- és anyaghasználati naplókban rögzített tényadatokat, majd a szállító számlasorait használva új költség-tényadatokat hoz létre.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Az ügyfelek, akik nem használják a teljes alvállalkozói élményt, de egységes képben nézetet látni a projektek költségeiről a Project Operations alkalmazásban

Ha egy harmadik fél rendszerében követi nyomon az alvállalkozói folyamatokat, akkor az adott külső rendszerből a Project Operations alkalmazásba rögzítheti a költségeket olyan szállítói számlák létrehozásával, amelyek nem hivatkoznak az alvállalkozói szerződésekre. Így a projektvezetők egyetlen, egységes nézetben tekinthetik meg az adott projekt összes költségét.

## <a name="create-vendor-invoices-in-project-operations"></a>Szállítói számlák létrehozása a Project Operations alkalmazásban

A szállítók számlái a Dynamics 365 Finance alkalmazásban hozhatók létre a **Kötelezettségek** modul használatával. A szállítói számlák nem hozhatók létre közvetlenül a Dataverse-ben.

### <a name="set-up-vendor-invoice-verification"></a>Szállítói számla ellenőrzésének beállítása

Ha a szállító számláját egy alvállalkozói szerződéshez szánják a Dataverse-ben, engedélyeznie kell a **Projektvezető manuális ellenőrzése szükséges** paramétert. A beállítás azt határozza meg, hogy a szállító számláját automatikusan meg kell-e erősíteni a Dataverse-ben, vagy manuális megerősítést igényel-e. Minden projekt szállítói számláinak fejlécében lehetőség van ugyanarra a névre. Alapértelmezés szerint a projektszállítói számlák fejlécén az itt megadott értékre lesznek beállítva. Az értéket azonban szükség szerint frissítheti az egyes szállítók számláinak fejlécében.

Ha a beállítás **Igen**, akkor a Finance-ban létrehozott és Dataverse-ben a szinkronizált számla állapota **Vázlat** lesz. Ezt követően a számlát a projektmenedzsernek ellenőriznie és hitelesítenie kell, és meg kell erősítenie, mielőtt feldolgozzák és feladják a megfelelő projekthez a főkönyvi számlára a Finance-ben.

Ha a beállítás **Nem**, a szállító számlája automatikusan meg lesz erősítve. További művelet nem szükséges.

A szállítói számlák ellenőrzésének beállításához kövesse az alábbi lépéseket:

1. A Finance-ben a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
1. Ha a vállalati irányelv az alvállalkozók számláinak ellenőrzését igényli, akkor állítsa a **Pénzügyi** lapon a **Projektvezető manuális ellenőrzése szüksége** paramétert **Igen** értékre. Ha a projektvezető által végzett ellenőrzés nem kötelező a Dataverse-ben, hagyja az értékkészletet **Nem** értéken. Alapértelmezés szerint a **Függőben lévő szállítói számla** oldal beállítása lesz használva.

> [!NOTE]
> Az alvállalkozók számára létrehozott szállítói számlák a Dataverse-ben csak akkor dolgozhatóak fel megfelelően, ha a **Projektvezető manuális ellenőrzése szükséges** beállítása **Igen**. Az alvállalkozók által létrehozott idő-, anyag- és költség tényadatokat a projektvezető csak akkor tudja manuálisan megfeleltetni a szállítói számla sorainak, ha a beállítás **Igen**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Beszerzési integrációs fiók beállítása a szállítói számlákhoz

Amikor egy szállító számláját feladják a Finance for Project Operations szolgáltatásban – Az integrált környezet (nem készletezett) pénzügyi adatok fel lesznek adva Beszerzési integrációs számlára.. A rendszer elő létrehozza a feladott számlához tartozó tényadatokat a Dataverse-ben. Ezek a tényadatok fel lesznek adva a Pénzügyben a Projektintegrációs naplóval. A Projektintegrációs napló a közzététele közzé teszi a valós költséget, és visszavonja a Beszerzési integrációs fiókot.

Beszerzési integrációs fiók beállításához a szállítói számlákhoz kövesse az alábbi lépéseket.

1. A Finance-ben a **Projektmenedzsment és könyvelés** \> **Beállítás** \> **Projektmenedzsment és könyvelési paraméterek** lehetőségre.
1. A **Project Operations a Dynamics 365 Customer Engagement alkalmazásban** lapon válassza az **Anyagok** \> **Beszerzési integráció** lehetőséget.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Alvállalkozói szállítói számlák létrehozása feladása

Amikor egy Kötelezettségkezelő adminisztrátor számlát kap az alvállalkozótól, a Finance-ben új számla jön létre.

1. A Finance-ben válassza a **Kötelezettségek** \> **Számlák** \> **Nyitott szállítói számlák** menüpontot.
1. A **Műveleti Panelen** válassza az **Új** lehetőséget új szállítói számla létrehozásához.
1. A **Számla** mező számlafejlécében válassza az **Alvállalkozó** lehetőséget.
1. Válassza ki a számla dátumát.
1. A **Fejléc** lapon állítsa a **Projektvezető manuális ellenőrzése szükséges** paramétert **Igen** lehetőségre. Ennek a beállításnak az alapértelmezett beállítása a **Projektmenedzsment és könyvelési paraméterek** oldalról jön. A szállítói számlák szintjén azonban ez módosítható.
1. A **Számla sor** gyorslapon válassza a **Sor hozzáadása** lehetőséget a szállítói számlasor létrehozásához.
1. Válassza ki az alvállalkozói sorok számára létrehozott beszerzési kategóriákat, majd adja meg az egységárat, a mértékegységet és a mennyiséget.
1. A **Projekt** lap szállítói számlasorok szakaszában válassza ki azt a projektet, amelyhez az alvállalkozó megosztja az alvállalkozó számláját.
1. Válassza ki a projektkategóriát. Lehet bármilyen típusú **Cikk**, **Költség**, **Anyag** vagy **Óra** lehet.
1. Csak akkor jelölje ki a szerepkört, ha a kijelölt projektkategória **Óra** típusú.
1. Adja fel a szállítói számlát a **Feladás** gombot választva.

Másik lehetőségként létrehozhat egy szállítói számlát a **Kötelezettségek** \> **Számlák** \> **Szállítói számlák megnyitása** menüpontban az **Új** lehetőséggel.

Amikor feladják a szállító számláját, az elérhetővé válik Dataverse-ben a projektvezető számára ellenőrzéshez és feldolgozáshoz.

## <a name="vendor-invoice-processing-in-dataverse"></a>Szállítói számla feldolgozása a Dataverse-ben

A Dataverse-ben létrehozott szállítói számlán bizonyos mezőértékek a Finance-ben rögzített szállítói számláról jönnek. Más értékek az alvállalkozóból származó alapértelmezett értékek.

A következő mezőket és kapcsolódó rekordokat a rendszer az alvállalkozói szerződésből a szállítói számla fejlécébe másolja:

- Pénznem
- Szerződő részleg
- Fizetési feltételek

A szállítói számlasorokon a Project Operations a következő mezőértékeket használja az alapértelmezett alvállalkozói és alvállalkozói sor hivatkozásait:

- Tranzakcióosztály
- Beosztás
- Tranzakció kategóriája
- Termék mezők
- Project
- Feladatok

> [!NOTE]
> A Project Operations nem támogatja a rögzített árú alvállalkozói sorokat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
