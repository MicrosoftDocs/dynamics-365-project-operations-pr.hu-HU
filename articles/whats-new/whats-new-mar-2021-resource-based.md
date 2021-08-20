---
title: Újdonságok – 2021. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén
description: Ez a témakör információval szolgál az erőforrás/nem készletalapú forgatókönyvek projektjeihez tartozó minőségi frissítésekről, amelyek a Project Operations 2021 márciusi kiadásában váltak elérhetővé.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006339"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Újdonságok – 2021. március – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a következő Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations a Dataverse-környezet 4.8.0.91 verzióján 
- Projektmenedzsment és könyvelés a Dynamics 365 Finance környezetének 10.0.16-es verziójában 

## <a name="quality-updates"></a>Minőségi frissítések

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse alatt


| **Funkcióterület** | **Hivatkozási szám** | **Minőségi frissítés** |
| --- | --- | --- |
| Számlázás és árképzés | 2133873 | Rögzítették az **Egységenkénti értékesítési ár** pénznemszimbólumának megjelenítését a **Költségbecslések** rácson. |
| Számlázás és árképzés | 2174616 | A megnyert ajánlatok esetében az ajánlatból másolt szerződéssorok részleteiben a szerződés egyéni árlistája hivatkozik a rendszer. |
| Lehetőségkezelés | 2167475 | A helyesbítési számlán szereplő rögzített adó összege, amelyből egy számlázatlan tényleges tétel származik. |
| Lehetőségkezelés | 2176285 | Az adó összegét nem szabad az értékesítési szerződés/ajánlatsor részleteiből a költségszerződés/ajánlatsor részleteibe másolni. |
| Lehetőségkezelés | 2188079 | Nem szabad felosztott számlázási szabályt létrehozni a nem munkaalapú szerződésekhez. |
| Tervezés és nyomon követés | 2125274 | A **Projekt kezdő dátumának leképezése** elem **Projekt kettős írási leképezés** attribútuma az **msdyn\_taskearlieststart** értékről az **msdyn\_actualstart** értékre lesz frissítve. |
| Tervezés és nyomon követés | 2138853 | A projektmásoló funkció frissítése biztosítja, hogy a feladatokra hivatkozó költségbecslési sorok a célprojektbe legyenek másolva. |
| Tervezés és nyomon követés | 2154306 | A költségbecskélek törlésével kapcsolatos problémák javításra kerültek a készletalapú forgatókönyvekhez készült Project Operations alkalmazásban. |
| Tervezés és nyomon követés | 2173259 | A projekt másolási funkciója frissült, hogy bizonyos esetekben ne jelenítse meg a **WBS másolása** hibaüzenetet. |
| Idő és költség | 2148910 | Az **Időbejegyzés** rács **Bejegyzés szerkesztése** oldalának megjelenítési problémája javításra került. |
| Idő és költség | 2159798 | Szigorúbb vezérlés annak biztosítása érdekében, hogy a jóváhagyott költségbejegyzések ne legyenek szerkeszthetők. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmenedzsment és könyvelés a Dynamics 365 Finance szolgáltatásban

További információkért lásd: [Újdonságok – 2021. január – Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Szabályozási frissítések

A Finance and Operations alkalmazások szabályozási frissítéseivel kapcsolatos további tudnivalók a [szabályozási frissítések](/dynamics365/finance/localizations/regulatory-updates) című témakörben olvashatók. A szabályozási frissítések megismerésének másik módja, ha bejelentkezik az LCS szolgáltatásba, és a problémakereső eszközzel megtekinti a tervezett szabályozási frissítéseket. A Problémakereső segítségével országonként, a szolgáltatás típusa és a kiadás között kereshet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]