---
title: Külső ütemezés
description: Ez a cikk a külső ütemezéssel kapcsolatban nyújt információkat.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736986"
---
# <a name="external-scheduling"></a>Külső ütemezés

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A külső ütemezési mód lehetővé teszi a munkalebontási struktúrához (WBS) kapcsolódó entitások natív módon történő létrehozását, frissítését és törlését, de a Microsoft Project for the Web által érvényesített aktuális korlátok nélkül. Korlátozott ellenőrzést is biztosít. Ezt a módot csak a következő ügyfelek használják:

- Azok az ügyfelek, akik rendelkeznek azokkal az eszközökkel, amelyek szükségesek egy WBS definiálásához a Project Operations által biztosított ütemezési logikán kívül
- Azok az ügyfelek akiknek a következőket kell menedzselniük: ütemezési hierarchia, függőségek vagy feladatidőtartam

> [!IMPORTANT]
> Előfordulhat, hogy a WBS-hez kapcsolódó entitásokban nem megfelelően beírt adatok nem jelennek meg az erőforrás-egyeztetés rácsban, a becslések rácsban, a követési rácsban vagy az erőforrás-hozzárendelés rácsában.

## <a name="configuration"></a>Configuration

Alapértelmezetten ez a funkció engedélyezett. Azonban az projektek gyári főoldalán a kapcsolód mező alapértelmezetten nem látható. A mező engedélyezéséhez a Maker Portalon nyissa meg a projektentitás főoldalát, jelölje ki az **Ütemezési motor** mezőt, majd módosítsa a mezőt **Alapértelmezés szerint látható** értékre. Ha nem a gyári projektfőoldalt használja, szerkessze a meglévő oldalt, és vegye fel rá az **Ütemezési motor** mezőt.

## <a name="settings"></a>Beállítások

A külső ütemezési mód használatához először létre kell hoznia egy új projektet, és ki kell választania a **Kívülről ütemezett** ütemezési motort a projekt főoldalának legördülő listájában. Miután ezt a módot beállította egy projekthez, azt nem lehet módosítani.

## <a name="viewing-the-wbs"></a>A WBS megtekintése

Ha egy projekt kívülről ütemezett, a Project for The Web hozzáférése korlátozott a projekthez. A WBS megtekintéséhez meg kell nyitnia a nyomkövetési rácsot, ahol a teljes WBS látható.

## <a name="creating-and-editing-the-wbs"></a>A WBS létrehozása és szerkesztése

Ha egy projektnél engedélyezve van a külső ütemezés, minden WBS-entitásra vonatkozó adatot definiálnia kell, beleértve a feladatokat, csoporttagokat, erőforrás-hozzárendeléseket és függőségeket.

A következő ábrán a projekttervezés adatmodellje látható.

![Projekttervezés adatmodellje.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcionális korlátozások

A következő műveletek nem engedélyezettek külsőleg ütemezett projektek esetében.

### <a name="project-planning"></a>Projekt tervezése

- **Projekt másolása** Ez a művelet nem támogatott a külső ütemezésű projekteknél.
- **Projekt áthelyezése** – A projekt kezdő dátumának módosításaival nem változik meg a feladatok vagy erőforrás-hozzárendelések kezdete a WBS-ben.
- **A Projektmenedzser frissítése** – A projektmenedzser módosításai a projekt főoldalán nem hoznak létre automatikusan új projektcsoport-tagot, amíg meg nem történik a projekt átalakítása.
- **A projekt munkaidősablonjának frissítése** – A projekt munkaidősablonjának módosítása nem fogja újraszámítani a projekt ütemezését.
- **Erőforrás-hozzárendelési kontúrok** – Az erőforrás-hozzárendelések létrehozása nem frissíti automatikusan az **mdyn\_PlannedWork** mezőt. Ebben a mezőben tároljuk az erőforrás-hozzárendelési erőfeszítésekhez szükséges emberi erőforrásokat. Ha időfázisos erőfeszítéseket mutat az erőforrás-hozzárendelési rácson vagy az erőforrás-egyeztetési rácsban, akkor meg kell határoznia az erőforrás-hozzárendelés kontúrjait. Ezeket a kontúrokat helyesen kell formázni, hogy a költség és az értékesítési ár kontúrjainak kiszámítását elindítsák. Javasoljuk, hogy hozzon létre egy a Project for the Web által ütemezett teszt projektet, majd ellenőrizze a kapcsolódó adatokat a követelmények és a formázás megerősítése érdekében.

### <a name="resource-management"></a>Erőforrás-kezelés

- **Általános erőforrás-teljesítés** – Külsőleg ütemezett projektek esetén nem támogatott az Általános erőforrás-teljesítés. Az aktív nyitott követelmények teljesítésére tett kísérletek új projektcsoport tagokat hoznak létre, de ez nem törli általános csoporttagot vagy cseréli az általános csoporttagot bármely meglévő erőforrás-hozzárendelésen.
- **Csoporttag törlése** – A csoporttagok törlése nem törli automatikusan az erőforrás-hozzárendeléseket.

### <a name="quoting-and-contracting"></a>Árajánlatkészítés és szerződéskötés

- **Árajánlatsor és Szerződéssor részleteinek importálása** – Amikor egy projektből árajánlat vagy szerződéssort részleteit importálják, az alkalmazás úgy lett tesztelve,, hogy a WBA-ban legfeljebb 500 feladatot támogat, feladatonként 20 hozzárendelés korlátja alapján.

### <a name="actuals-and-invoicing"></a>Tényadatok és számlázás

- Annak ellenére, hogy a WBS és a pénzügyi tranzakciók meglévő ellenőrzései kapcsán fontos, hogy megfeleljen a teljes adatmodellnek, hogy a későbbi tranzakciók a várt módon fussanak.
