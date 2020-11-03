---
title: Biztonsági modell
description: Ez a témakör a Dynamics 365 Project Operations biztonsági modelljéről nyújt információkat.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4077977"
---
# <a name="security-model"></a>Biztonsági modell

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Microsoft Dynamics 365 Project Operations egy egyedi biztonsági modellt tartalmaz, amely lehetővé teszi egy olyan szerepkörön alapuló üzleti biztonsági modell használatát, amely együttműködik a Microsoft Office Csoportokkal. 


## <a name="security-roles"></a>Biztonsági szerepkörök
A Project Operations előtéri szolgáltatásai a következő szerepköröket tartalmazzák:

| Szerepkör                          | Adatfolyam leírása                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Gyakorlatmenedzser              | Támogatja a projektközi jelentéskészítést.                                                                                                            | Üzleti egység              |
| Projekt jóváhagyója              | A projekt idő- és költségfelhasználását hagyja jóvá.                                                                                                                              | Üzleti egység |
| Projektszámlázási adminisztrátor | Létrehozza a számlajavaslatot.                                                                                                                                                 | Üzleti egység |
| Projektvezető               | Létrehozza a projekttervet, és erőforrásokat igényel.                                                                                                                              | Üzleti egység |
| Projekterőforrás              | A csoporttagok, akik foglalhatók, és jelentik az időt.                                                                                                          | Üzleti egység|
| Erőforrás-kezelő              | Minden erőforrás-kezelési funkció, például az erőforrás-kérelmek és -foglalások teljesítése elkülönítve, hogy támogassa a hibrid projektmenedzser + erőforrás-kezelő konfigurációt és az egyetlen és központosított erőforrás-kezelői szerepkört. | Üzleti egység |


A Microsoft webes projekt a következő szerepköröket tartalmazza:

| Szerepkör           | Adatfolyam leírása                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projektfelhasználó   | A projekt együttműködő felhasználója, aki saját projekteket hozhat létre, és megtekintheti a vele megosztott projekteket. | Felhasználó   |
| Projektrendszer | Az alkalmazáskörnyezethez használt szerepkör. Az ügyfelek nem használhatják ezt a rendszerszerepkört.                                    | Globális |

## <a name="security-enforcement"></a>Biztonsági szabályok kikényszerítése
A projektek szintjén végrehajtott műveletek a bejelentkezett felhasználó kontextusában kerülnek végrehajtásra. Ez azt jelenti, hogy a projektek létrehozásához, megnyitásához és törléséhez a felhasználónak hozzáféréssel kell rendelkezniük a CDS-ben. A hozzáférés a CDS-ben a platform bármely lehetséges mechanizmusán keresztül megadható. A nagyobb hatókörű felhasználók például hozzáférhetnek a projekthez, vagy ha egy olyan explicit projektmegosztási műveletet hajtottak végre, amely a felhasználó számára hozzáférést biztosít.

Fontos figyelembe venni ezt a projektek Project Operationsben történő létrehozásakor.

## <a name="modern-group-collaboration-with-project-operations"></a>Modern csoportos együttműködés a Project Operations alkalmazással
A Webes projektek és a Project Operations támogatja a modern csoportos együttműködést. A projekthez egy csoporton keresztül felvett felhasználók módosíthatják a projekttervet.

A Webes projekt a hozzárendeléskor automatikusan hozzáadja a felhasználókat a csoporthoz.

A csoportok lehetővé teszik a projektek jogosultságait és támogatják az együttműködési műtermékeken végzett közös munkát. A következő ábra a csoportos hozzárendelési folyamat során bekövetkező eseményeket és állapotváltozásokat ábrázolja.

A Project Operations nem hoz létre csoportot implicit művelet révén, és csak a csoportok kifejezett megnyomására hajtja ezt végre.

A csoport tagjainak keresése a **Csoportkezelés** párbeszédpanelen azokra korlátozódik, akik a környezet biztonsági csoportja részeként vannak beállítva. További információkért lásd: [Felhasználók hozzáférésének szabályozása a környezetekhez: biztonsági csoportok és licencek](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Csoportos mód](./media/groupsmode.png)

1. A projektet a létrehozó felhasználó hozza létre és birtokolja.
2. A projekt tulajdonosa a csoportra van frissítve.
3. A tulajdonos csoport a megadott vagy létrehozott Office-csoportra van leképezve.
4. A projekt eredeti tulajdonosa hozzáadásra kerül az Office-csoporthoz.

## <a name="deployment-recommendation"></a>Telepítési javaslat
Mivel az Office-csoport együttműködési modellje fejlődik, további funkciók kerülnek később hozzáadásra, amelyek részletesebb ellenőrzést biztosítanak. A Project Operationst ma telepítő ügyfeleket arra ösztönözzük, hogy a hagyományos Microsoft Dynamics 365 biztonsági modellre összpontosítsanak.

További tudnivalókért lásd: [Biztonság a Common Data Service rendszerben](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations és a Microsoft Dynamics 365 Finance biztonsága
A Project Operations a következő szerepköröket tartalmazza:

- Projektvezető
- Projekt könyvelője

A pénzügyi biztonsággal kapcsolatos további információkért lásd: [Szerepköralapú biztonság](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


