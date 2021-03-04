---
title: Újdonságok – 2021. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2021 februári kiadásában váltak elérhetővé.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141319"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. február – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations a Dataverse-környezetben 4.7.0.95
- Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.16-es verziójában 

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt

| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| **Számlázás és árképzés** | 2053736 | A számlasor részletei most már elérhetők a **Számla** > **Kapcsolódó információk** oldalon. |
| **Számlázás és árképzés** | 2122613 | Az **Aktiválás** és **Inaktiválás** műveletek el vannak távolítva az **Árlista** társítási entitásokból. |
| **Számlázás és árképzés** | 2128606 | A **GetEstimatesForProject** beépülő modulban megoldotta az **ullReferenceException** programmal kapcsolatos problémát. |
| **Központi telepítés és konfiguráció** | 2139346 | Megoldotta a nem felügyelt **Dynamics365ProjectOperationsDualWrite** megoldás importálásával kapcsolatos problémát. |
| **Központi telepítés és konfiguráció** | 2140569 | Nem szabad telepíteni a Dataverse Teams környezetben a projektmegoldást. |
| **Központi telepítés és konfiguráció** | 2086991 | A webes erőforrások korlátozott testreszabási lokalizációja. |
| **Lehetőségkezelés** | 2136794 | A megfelelő hibaüzenetet jeleníti meg, ha a **Számla megerősítése** vagy a **Számla megjelölése kifizetettként** folyamatok sikertelenek. |
| **Lehetőségkezelés** | 2139330 | A projekt projektmenedzserének módosítása nem állíthatja vissza a tulajdonos vállalatot az alapértelmezett értékre. |
| **Lehetőségkezelés** | 2146376 | A fel nem számítható tényadatok korrigált adóösszegét a számla visszaigazolásából hozzák létre. |
| **Projekttervezés és nyomon követés** | 2099879 | A Dataverse-környezet központi telepítésének létre kell hoznia egy statikus azonosítóval rendelkező alapértelmezett tranzakciókategóriát, és nem hozhat létre véletlenszerűen környezetenként egyet. |
| **Projekttervezés és nyomon követés** | 2128577 | Rögzítette a Project Service felhasználói jogosultságait, hogy frissítse a tranzakciókategóriát egy erőforrás-hozzárendelésen. |
| **Projekttervezés és nyomon követés** | 2164035 | Kijavította a **Projekt másolása** funkcióval kapcsolatos problémákat. |
| **Időbejegyzés** | 2129161 | Szigorúbb korlátozások vonatkoznak annak biztosítására, hogy a felhasználók ne módosíthassák és ne frissíthessék a beküldött vagy jóváhagyott időbejegyzéseket. |
| **Időbejegyzés** | 2103572 | A projekten kívüli időbejegyzések időjóváhagyása nem kereshet projektjóváhagyói szerepkört. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance szolgáltatásban 

A Dynamics 365 Finance projektmenedzsmentjéről és könyveléséről, lásd a [Újdonságok – 2021. január – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén](whats-new-jan-2021-resource-based.md) című részt.


## <a name="regulatory-updates"></a>Szabályozási frissítések

A Finance and Operations alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [szabályozási frissítések](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. A szabályozási frissítések megismerésének másik módja, ha bejelentkezik a Lifecycle Services (LCS) szolgáltatásba, és a problémakereső eszközzel megtekinti a tervezett szabályozási frissítéseket. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.
