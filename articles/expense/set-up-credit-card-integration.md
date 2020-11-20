---
title: Hitelkártya-integráció beállítása
description: Ez a témakör a költséggel kapcsolatos hitelkártya-tranzakciók importálását és karbantartását ismerteti.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120861"
---
# <a name="set-up-credit-card-integration"></a>Hitelkártya-integráció beállítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A költséggel kapcsolatos hitelkártya-tranzakciók úgy is beállíthatók, hogy a rendszer ismétlődően, ütemezés szerint, automatikusan importálja őket. Szükség esetén manuálisan is importálhatja a tranzakciókat. A hitelkártya-tranzakciók importálása a Hitelkártya-tranzakciók adatentitáson keresztül történik.

## <a name="import-credit-card-transactions"></a>Hitelkártya-tranzakciók importálása

1. A **Hitelkártya-tranzakciók** oldalon válassza a **Tranzakciók importálása** lehetőséget. Ha első alkalommal használja az adatkezelési funkciót, a folytatás előtt a rendszernek frissítenie kell az adatentitások listáját.
2. A **Név** mezőben adja meg az importálási feladat egyedi leírását.
3. A **Forrás adatformátuma** mezőben válassza ki az importálandó hitelkártya-tranzakciókat tartalmazó fájl formátumát.
4. Válassza a **Feltöltés** lehetőséget, majd keresse meg és jelölje ki az importálandó fájlt.
5. A fájl feltöltése után érvényesítse a hitelkártya-tranzakciós fájl és a hitelkártya-tranzakciók adatentitáshoz tartozó oszlopok leképezését a csempe **Leképezés megtekintése** hivatkozásával. Ha vannak leképezési hibák, vagy ha módosítania kell a leképezést, akkor a szükséges módosításokat a **Leképezés vizualizációja** vagy a **Leképezés részletei** lapon adhatja meg.
6. A hitelkártya-tranzakciók automatizálásához válassza az **Ismétlődő feladat létrehozása adatokhoz** lehetőséget. Ezután beállíthatja azt az ismétlődést, amely meghatározza, hogy milyen gyakran kerüljön sor a hitelkártya-tranzakciók importálására. Ha végzett, válassza az **OK** lehetőséget.
7. Ha azonnal szeretné importálni a kijelölt fájlt, válassza az **Importálás** lehetőséget.
8. Ha az importálás során hiba történik, akkor a végrehajtási naplóban vagy az előkészítési adatok között tekintheti meg azokat a hibákat, amelyeket ki kell javítania, hogy az importálás sikeres legyen.

> [!NOTE]
> Ha több fájlformátumot kell importálnia, akkor mindegyik formátumtípushoz külön importálási feladatot kell létrehoznia.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Lezárt alkalmazottakhoz tartozó hitelkártya-tranzakciók ismételt hozzárendelése

Ha egy alkalmazott rekordját lezárják, az alkalmazott Active Directory Domain Services-fiókja (AD DS) le lesz tiltva. Előfordulhat azonban, hogy vannak olyan aktív hitelkártya-tranzakciók, amelyeket továbbra is ki kell fizetni, és meg kell téríteni. A **Hitelkártya-tranzakciók** oldalon újra hozzárendelheti az alkalmazottat az olyan hitelkártya-tranzakciók esetén, ahol a társított alkalmazott le van zárva.

Jelöljön ki egy vagy több hitelkártya-tranzakciót, majd válassza a **Tranzakciók ismételt hozzárendelése** lehetőséget. Ezután kiválaszthat egy másik alkalmazottat, akit hozzá szeretne rendelni a hitelkártya-tranzakciókhoz. A hitelkártya-tranzakciók újbóli hozzárendelése után ezeket a tranzakciókat a rendszer kiválaszthatja a költségjelentésekhez, és kifizethetők a visszatérítések a a költségjelentés szokásos folyamatán keresztül.
