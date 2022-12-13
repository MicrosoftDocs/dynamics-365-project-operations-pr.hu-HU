---
title: Erőforrás-hozzárendelések létrehozása
description: Ez a cikk az általános és a megnevezett erőforrás-hozzárendelések létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811996"
---
# <a name="create-resource-assignments"></a>Erőforrás-hozzárendelések létrehozása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


Az erőforrás-hozzárendelés a projektcsapat valamely tagjának közvetlen társítása egy levélcsomópont-feladathoz. Ez a cikk információkat nyújt az erőforrások hozzárendelésének különböző módjairól.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Általános csapattag létrehozása feladat-hozzárendeléssel


Ha a feladat-hozzárendelésen keresztül egy általános csoporttagot hoz létre, akkor létre kell hoznia egy helyőrzőt vagy egy általános erőforrást. Ez az általános erőforrás annak a megnevezett erőforrásnak a jellemzőit írja le, amelyeken végül dolgozni szeretne. Ezután létrehozhat egy követelményt, vagy elküldhet egy kérést a megnevezett erőforrás kereséséhez és lefoglalásához használt követelmény használatával.

1. A feladat Ütemezés rácsán válassza az Erőforrás ikont az **Erőforrás** cellájában.
2. Írjon be egy nevet, amely a helyőrző erőforrás neveként szolgál. Például: Programkezelő.
3. Válassza a **Létrehozás** lehetőséget, majd a **Gyors létrehozás: Projektcsapattag** mezőben adja meg az általános erőforrás szerepkörét.
4. Szükség szerint feladatokat rendelhet hozzá e helyőrző erőforrásához, ha az **Erőforrásválasztóban** kiválasztja az erőforrást a feladathoz. Az erőforrások a **Csapattagok** területen vannak felsorolva.
5. Ha végzett az általános erőforrás hozzárendelésével, a Csapat **lapon válassza ki az általános erőforrást, majd válassza a** Követelmény **létrehozása lehetőséget** az általános erőforrás erőforrásigényének létrehozásához.
6. Jelölje be a **Foglalás** elemet az általános erőforráshoz, és aztán az ütemezési tábla használatával kereshet és foglalhat le egy tényleges erőforrást. El is küldheti a követelményt egy erőforrás-menedzser általi teljesítésre.
7. Ha az általános erőforrás teljes mértékben teljesül egy megnevezett erőforrással, az általános erőforrás el lesz távolítva a csapatból. (Az erőforrás-követelmények részleges teljesítése nem eredményez erőforrás-hozzárendelést.) Az általános erőforrás tevékenység-hozzárendelései ahhoz a megnevezett erőforráshoz vannak rendelve, amely teljesítette az általános erőforrás erőforrásigényét.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Elnevezett erőforrás hozzárendelése az összes foglalható erőforrás listájából

Használhatja az **Erőforrásválasztó** keresési mezőjét, hogy minden aktív, foglalható erőforrásra kereshessen, és hozzárendelhesse őket bármely levélcsomópont-feladathoz. Az így hozzárendelt erőforrások foglalás nélkül lesznek hozzáadva a csapathoz. Ez hasonló ahhoz, amikor csapattagot ad hozzá, és a **Nincs** beosztási módszert választja. Az erőforrás a **Csapat**, az **Erőforrás-hozzárendelés** és az **Egyeztetés** lapon jelenik meg csak hozzárendelésekkel és beosztási hiánnyal rendelkező erőforrásokként. Ha a rendelkezésre állásukat használni kívánja, foglalja le őket.

1. A feladat rácsa, táblája vagy idővonala alatt keresse meg a **Hozzárendelve a következőhöz:** cellát.
2. A keresőmezőbe kezdje beírni a nevet. A név keresési eredményei megjelennek az **Erőforrás választóban** az **Egyéb erőforrások** részen.
3. Jelölje ki a feladathoz hozzárendelni kívánt erőforrást, vagy jelölje ki az erőforrás nevét a **Csoport egyéb erőforrásai** között.

## <a name="editing-resource-assignment-contours"></a>Erőforrás-hozzárendelési kontúrok szerkesztése

Alapértelmezés szerint, amikor az erőforrások egy tevékenységhez vannak rendelve az ütemezésben, az erőfeszítéseik lineárisan oszlanak el az egyes erőforrások között az adott erőforrás munkaideje és a projekt ütemezési módja alapján. A projektmenedzser az erőforrás-hozzárendelési rács segítségével finomíthatja az egy vagy több tevékenységhez rendelt egyes erőforrások munkamennyiség-becsléseit a különböző időskálákon. Ez a funkció segít a projektmenedzsereknek pontosabb költség- és értékesítési becsléseket készíteni, amelyeket az erőforrás tevékenységhez való hozzárendelésekor generált erőforrás-hozzárendelési kontúrok vezérelnek. Ezenkívül a projektmenedzserek könnyebben tükrözhetik az erőforrásigényt, amely az erőforrásigény kiépítéséhez szükséges.

### <a name="navigation"></a>Navigálás

A kontúrszerkesztő rács eléréséhez a projektmenedzser először kiválasztja a Tevékenységek **lapot a projekt főoldalán, majd kiválasztja** a **Hozzárendelések** lapot.

![Hozzárendelések lap a projekt főoldalának Feladatok lapján.](media/AssignmentGrid.png)

A rács két módszert támogat a csoportosításhoz: **csoportosítás erőforrás** szerint és **csoportosítás tevékenység** szerint. A rácsnézettől eltérően az oszlopok nem konfigurálhatók. Az egyetlen látható oszlop a Hozzárendelve **, a Feladat neve**, a **Hozzárendelés kezdete,** **a** Hozzárendelés befejezése **és** a Hozzárendelés **erőfeszítése**.

A rács kezdeti renderelésekor a legkorábbi hozzárendelési kontúrnál kezdődik. Ha az ütemezés nem tartalmaz erőfeszítéssel járó hozzárendeléseket, a rács üres lesz, és nem jelenít meg semmit.

![Üres hozzárendelési rács.](media/emptyassignmentgrid.png)

Ha meg szeretné tekinteni a kontúrokat és a különböző időskálákat, a csak olvasható erőforrás-hozzárendelési rács és az erőforrás-egyeztetési rács is elérhető.

### <a name="resource-calendars"></a>Erőforrásnaptárak

Egy adott nap kontúrjának szerkesztésére való képességet az erőforrás munkanapjai szabályozzák, ahogyan az a naptárban is tükröződik. Ha egy cella le van tiltva egy adott erőforrásnál, az erőforrásnak nincs munkanapja az adott időszakban.

Az erőforrás körvonalai túlnyúlhatnak a hozzárendelt tevékenység aktuális kezdési és befejezési dátumán. Ha egy eloszlás úgy frissül, hogy az a tevékenység legkésőbbi befejezési dátuma vagy a tevékenység legkorábbi kezdési dátuma után van, a tevékenység záró vagy kezdési dátuma a megfelelő módon módosul. Ha azonban egy kontúrt úgy frissítenek, hogy az korábbi legyen, mint egy megelőző tevékenységhez kapcsolt tevékenység kezdési dátuma, a frissítés sikertelen lesz, mert a hozzárendelés elindítja a tevékenységet, mielőtt a megelőző befejeződik, és ez a viselkedés jelenleg nem támogatott.

### <a name="co-authoring"></a>Társszerzőség

Az erőforrás-hozzárendelési rács módosításai automatikusan megjelennek a társított nézetekben, beleértve a diagram-, idővonal-, tábla- és rácsnézeteket. Ha egyszerre több felhasználó is áttekinti a projektet, az egy felhasználó által végrehajtott módosítások megjelennek a rácsban. Ezzel szemben az erőforrás-hozzárendelési rácsban végrehajtott módosítások megjelennek az összes többi felhasználó számára, akik ugyanabban a munkamenetben tekintik meg a projektet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
