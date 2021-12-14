---
title: Hitelkártya-integráció beállítása
description: Ez témakör ismerteti, hogyan dolgozzon a költségekkel kapcsolatos hitelkártya-tranzakciókkal.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826259"
---
# <a name="set-up-credit-card-integration"></a>Hitelkártya-integráció beállítása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A költséggel kapcsolatos hitelkártya-tranzakciók úgy is beállíthatók, hogy a rendszer ismétlődően, ütemezés szerint, automatikusan importálja őket. Szükség esetén manuálisan is importálhatja a tranzakciókat. A hitelkártya-tranzakciók importálása a hitelkártya-tranzakciók adatentitáson keresztül történik.

## <a name="import-credit-card-transactions"></a>Hitelkártya-tranzakciók importálása

Hitelkártya-tranzakciók importálása esetén kövesse az alábbi lépéseket:

1. A **Hitelkártya-tranzakciók** oldalon válassza a **Tranzakciók importálása** lehetőséget. Ha először nyitja meg az adatkezelést, a rendszernek frissítenie kell az adatkapcsolatok listáját a folytatás előtt.
2. A **Név** mezőbe írja be az importálási feladat egyedi leírását.
3. A **Forrás adatformátuma** mezőben válassza ki az importálandó hitelkártya-tranzakciókat tartalmazó fájl formátumát.
4. Válassza a **Feltöltés** lehetőséget, majd keresse meg és jelölje ki az importálandó fájlt.
5. A fájl feltöltése után érvényesítse a hitelkártya-tranzakciós fájl és a hitelkártya-tranzakciók adatentitáshoz tartozó oszlopok leképezését a csempe **Leképezés megtekintése** hivatkozásával. Ha vannak leképezési hibák, vagy ha módosítania kell a leképezést, akkor a szükséges módosításokat a **Leképezés vizualizációja** vagy a **Leképezés részletei** lapon adhatja meg.
6. A hitelkártya-tranzakciók automatizálásához válassza az **Ismétlődő feladat létrehozása adatokhoz** lehetőséget. Ezután beállíthatja azt az ismétlődést, amely meghatározza, hogy milyen gyakran kerüljön sor a hitelkártya-tranzakciók importálására. Ha végzett, válassza az **OK lehetőséget**.
7. Ha azonnal szeretné importálni a kijelölt fájlt, válassza az **Importálás** lehetőséget.
8. Ha az importálás során hibák történnek, megtekintheti a végrehajtási naplót vagy az előkészítési adatokat a sikeres importálás érdekében javítható hibák megtekintéséhez.

> [!NOTE]
> Ha egynél több fájlformátumot kell importálnia, minden formátumtípushoz külön importálási feladatokat kell létrehoznia.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Lezárt alkalmazottakhoz tartozó hitelkártya-tranzakciók ismételt hozzárendelése

Az alkalmazotti rekord megszűnése után az alkalmazott Active Directory tartományi szolgáltatások (AD DS) fiókja le van tiltva. Előfordulhat azonban, hogy vannak olyan aktív hitelkártya-tranzakciók, amelyeket továbbra is ki kell fizetni, és meg kell téríteni. A **Hitelkártya-tranzakciók** lapon újra hozzárendelheti az alkalmazottat minden olyan hitelkártya-tranzakcióhoz, ahonnan a társított alkalmazottat eltávolították.

Jelöljön ki egy vagy több hitelkártya-tranzakciót, majd válassza a **Tranzakciók ismételt hozzárendelése** lehetőséget. Ezután kiválaszthat egy másik alkalmazottat, akit hozzá szeretne rendelni a hitelkártya-tranzakciókhoz. A hitelkártya-tranzakciók újbóli hozzárendelése után ezeket a tranzakciókat a rendszer kiválaszthatja a költségjelentésekhez, és kifizethetők a visszatérítések a a költségjelentés szokásos folyamatán keresztül.

## <a name="delete-credit-card-transactions"></a>Hitelkártya-tranzakciók törlése 

Előfordulhat, hogy a hitelkártya-tranzakciók importálása után bizonyos tranzakciókat törölni kell. Ennek oka az lehet, hogy a tranzakciók ismétlődőek, vagy azért, mert az adatok nem pontosak. A rendszergazdák a **„Hitelkártya-tranzakciók törlése”** funkcióval kiválaszthatják és törölhetik azokat a hitelkártya-tranzakciókat, amelyek **nem kapcsolódnak** költségjelentéshez. 

1. Menjen az **Időszakos feladatok** > **Hitelkártya-tranzakciók törlése** lehetőségre.
2. Válassza a **Szűrés** lehetőséget, és adjon meg adatokat a felvenni kívánt rekordok azonosításához.
3. A rekordok törléséhez válassza az **OK** elemet. 

## <a name="storing-credit-card-numbers"></a>Hitelkártyaszámok tárolása

A hitelkártyaszámok tárolására három lehetőség áll rendelkezésre. A hitelkártyaszámok a **Költségkezelési paraméterek** oldalon tárolódnak.

- **A kártyaszám bejegyzésének megakadályozása** – A hitelkártyaszámok nem tárolódnak.
- **Kivonatkártyaszámok (tárolja az utolsó négy számjegyet)** - A hitelkártyaszámok utolsó négy számjegye titkosított formátumban tárolódik.
- **Áruházi kártyaszámok** – A hitelkártyaszámok titkosítatlan formátumban tárolódnak. Ez a beállítás nem felel meg a fizetésikártya-iparág (PCI) adatbiztonsági szabványának (DSS). Ezért annak érdekében, hogy szervezetük megfeleljen a PCI DSS előírásoknak, a szervezeti rendszergazdáknak úgy kell dönteniük, hogy nem tárolják a hitelkártyaszámokat, vagy tárolják a kivonatkártya-számokat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
