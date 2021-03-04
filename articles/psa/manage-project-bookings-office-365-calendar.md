---
title: A Office 365 naptárban lévő projektek és foglalások kezelése
description: Projektek és foglalások kezelése a Office 365 naptárban
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c575bd3deba5bcde2526ccfc598327917bf91642
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144461"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>A naptárban lévő projektek és foglalások kezelése (Project Service)

> [!Note]
> KIVEZETVE: Ez a szolgáltatás elavult, és már nem érhető el.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Megjeleníthetők személyes találkozók, projektmunka-foglalások és field service munkarendelés feladatok az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptári segítségével.  
  
 Így mindent egy helyen megtalál, ezáltal sokkal gördülékenyebb a munkamenet. Az értekezletek, találkozók, foglalások és feladatok mind elérhetők az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárban.  
  
 Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] alkalmazást használ, akkor megadhatja a személyes találkozóit is a Project Service időbejegyzés nézetben. Ez lehetővé teszi, hogy a projekt és erőforrás-menedzserek lássák mikor elérhető egy projekthez. Időt is megtakaríthat, mivel nem kell kétszer megadni a személyes találkozói adatait. Egyszerűen importálhatja a személyes találkozókat a naptárból a Project Service időbejegyzés nézetbe.  
  
 A naptár szinkronizálja a projekt és munkarendelés foglalásokat a mai naptól kezdve az elkövetkezendő pár héten át. Ez a beállítás nem módosítható.  
  
 A szinkronizálás csak egy irányba támogatott a PSA-ból az Ön [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] naptárába. Fordított irányban is szinkronizálhat. 
  
 Az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptár használatával kapcsolatos további információkat itt talál: [Outlook webes naptár vállalati verzió](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Beállítás  
 Mielőtt megtekintheti és kezelheti a foglalásait az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárban, be kell állítania néhány dolgot.  
  
- Szüksége lesz az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] globális rendszergazda vagy a Rendszergazda hitelesítő adataira.  
  
- A rendszergazdájának konfigurálnia kell a levelezési kiszolgálói profilt és az egyes felhasználóknak is konfigurálniuk kell a postafiókjaikat. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [E-mail-feldolgozás beállítása kiszolgálóoldali szinkronizáláson keresztül](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Kapcsolja be a szervezet szinkronizálását (adminisztrátori feladat)  
  
1.  A főmenüben kattintson a **Beállítások** > **Adminisztráció** lehetőségre.  
  
2.  Kattintson a **Rendszerbeállítások** lehetőségre.  
  
3.  Kattintson a **Szinkronizálás** lapra.  
  
4.  A **Erőforrás-foglalás szinkronizálásának engedélyezésének kiválasztása ezzel** lehetőségnél válassza ki az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőséget.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Kapcsolja be a felhasználói profil szinkronizálását (felhasználói feladat)  
  
1.  A képernyő jobb felső sarkában kattintson a **Beállítások** gombra .  
  
2.  Kattintson a **Beállítások** pontra.  
  
3.  Kattintson a **Szinkronizálás** lapra.  
  
4.  Az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőségnél válassza az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőséget.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importálja a személyes találkozókat (felhasználói feladat)  
 Importálhatja a személyes találkozókat a naptárból a Project Service Automation időbejegyzés nézetbe.  
  
1. Nyissa meg az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárat, majd kattintson az **Adatok importálása** lehetőségre.  
  
2. A Szűrők képernyőn válassza ki a **Tőzsdei találkozók** majd az **Alkalmaz** lehetőséget.  
  
3. A rendszer átemeli a találkozókat az időbejegyzés nézetbe javasolt bejegyzésekként az adott hétbe. Egy másik hét bejegyzéseinek hozzáadásához kattintson az **Előző** vagy **Következő** lehetőségre.  
  
4. Válassza ki a találkozót, amit hozzá szeretne adni a Project Service Automation időbejegyzés nézethez.  
  
5. Az **Időbejegyzés** felugró menüben válassza ki a megfelelő lehetőségeket, hogy átalakíthassa a találkozót Project Service Automation időbejegyzés nézetté.  
  
6. Kattintson a **Mentés** gombra.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Idő, Költségek és Együttműködési útmutató](../psa/time-expense-collaboration-guide.md)
