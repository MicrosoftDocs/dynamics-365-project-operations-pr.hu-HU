---
title: Foglalások és hozzárendelések
description: Ez a cikk az erőforrás-foglalások és az erőforrás-hozzárendelések közötti különbségeket ismerteti.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918591"
---
# <a name="bookings-vs-assignments"></a>Foglalások és hozzárendelések

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A foglalások a források nehéz vagy puha elosztása egy projekthez. A kemény foglalások felhasználják az erőforrás kapacitását. A foglalások a csapatok szervezeti koncepcióit képviselik, így megismerhetik, hogyan vesznek részt az erőforrások különféle projektekben. A Dynamics 365 Project Operations a foglalásokat projektszintű fogalomnak tekinti. 

A foglalásoktó eltérően a hozzárendelések az erőforrások kötelezettségvállalásai a projekt feladataihoz a projekt ütemtervében. Az erőforrások lehetnek megnevezettek vagy általánosak.  Ha egy erőforrás-követelmény a projektfeladatok hozzárendeléseiből származik, a Project Operations az erőforrások hozzárendelésének ráfordítási eloszlásokat felhasználva építik az erőforrás-követelmény részleteinek részletezett részleteit. Az erőforrás-hozzárendelésekre való hivatkozás azonban nem tartható fenn. Az erőforrás-követelményekből származó foglalások frissítései nem frissítik az erőforrás-hozzárendeléseket.

Az erőforráshoz tartozó foglalások összege általában egy vagy több tevékenységen belül megegyezik az erőforrás hozzárendeléseinek összegével. A Project Operations azonban nem kényszeríti ezt a megállapodást. Az **Egyeztetés** nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.




[!INCLUDE[footer-include](../includes/footer-banner.md)]