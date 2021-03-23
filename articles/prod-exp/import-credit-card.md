---
title: Bankkártya-tranzakciók importálása és karbantartása
description: Ez a témakör a költséggel kapcsolatos hitelkártya-tranzakciók importálását és karbantartását ismerteti. Ezek a tranzakciók úgy állíthatók be, hogy ismétlődő ütemezésben automatikusan importálásra kerülnek, illetve szükség esetén kézzel is importálhatók.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271581"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Bankkártya-tranzakciók importálása és karbantartása

A költséggel kapcsolatos hitelkártya-tranzakciók úgy is beállíthatók, hogy a rendszer ismétlődően, ütemezés szerint, automatikusan importálja őket. Szükség esetén manuálisan is importálhatja a tranzakciókat. A hitelkártya-tranzakciók importálása a Hitelkártya-tranzakciók adatentitáson keresztül történik.

Az adatentitásokkal kapcsolatos további tudnivalókért lásd: [Adatentitások](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]