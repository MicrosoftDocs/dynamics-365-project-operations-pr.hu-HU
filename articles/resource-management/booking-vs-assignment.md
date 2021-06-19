---
title: Foglalások és hozzárendelések
description: Ez a témakör információkat biztosít az erőforrás-foglalások és az erőforrás-hozzárendelések közötti különbségekről.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012769"
---
# <a name="bookings-vs-assignments"></a>Foglalások és hozzárendelések

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A foglalások a források nehéz vagy puha elosztása egy projekthez. A kemény foglalások felhasználják az erőforrás kapacitását. A foglalások a csapatok szervezeti koncepcióit képviselik, így megismerhetik, hogyan vesznek részt az erőforrások különféle projektekben. A Dynamics 365 Project Operations a foglalásokat projektszintű fogalomnak tekinti. 

A foglalásoktó eltérően a hozzárendelések az erőforrások kötelezettségvállalásai a projekt feladataihoz a projekt ütemtervében. Az erőforrások lehetnek megnevezettek vagy általánosak.  Ha egy erőforrás-követelmény a projektfeladatok hozzárendeléseiből származik, a Project Operations az erőforrások hozzárendelésének ráfordítási eloszlásokat felhasználva építik az erőforrás-követelmény részleteinek részletezett részleteit. Az erőforrás-hozzárendelésekre való hivatkozás azonban nem tartható fenn. Az erőforrás-követelményekből származó foglalások frissítései nem frissítik az erőforrás-hozzárendeléseket.

Az erőforráshoz tartozó foglalások összege általában egy vagy több tevékenységen belül megegyezik az erőforrás hozzárendeléseinek összegével. A Project Operations azonban nem kényszeríti ezt a megállapodást. Az **Egyeztetés** nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.




[!INCLUDE[footer-include](../includes/footer-banner.md)]