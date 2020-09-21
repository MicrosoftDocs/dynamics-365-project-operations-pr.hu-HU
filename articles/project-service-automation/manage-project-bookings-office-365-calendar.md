---
title: A Office 365 naptárban lévő projektek és foglalások kezelése
description: Projektek és foglalások kezelése a Office 365 naptárban
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752142"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="6ff76-103">A naptárban lévő projektek és foglalások kezelése (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6ff76-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="6ff76-104">KIVEZETVE: Ez a szolgáltatás elavult, és már nem érhető el.</span><span class="sxs-lookup"><span data-stu-id="6ff76-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="6ff76-105">Megjeleníthetők személyes találkozók, projektmunka-foglalások és field service munkarendelés feladatok az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptári segítségével.</span><span class="sxs-lookup"><span data-stu-id="6ff76-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="6ff76-106">Így mindent egy helyen megtalál, ezáltal sokkal gördülékenyebb a munkamenet.</span><span class="sxs-lookup"><span data-stu-id="6ff76-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="6ff76-107">Az értekezletek, találkozók, foglalások és feladatok mind elérhetők az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárban.</span><span class="sxs-lookup"><span data-stu-id="6ff76-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="6ff76-108">Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] alkalmazást használ, akkor megadhatja a személyes találkozóit is a Project Service időbejegyzés nézetben.</span><span class="sxs-lookup"><span data-stu-id="6ff76-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="6ff76-109">Ez lehetővé teszi, hogy a projekt és erőforrás-menedzserek lássák mikor elérhető egy projekthez.</span><span class="sxs-lookup"><span data-stu-id="6ff76-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="6ff76-110">Időt is megtakaríthat, mivel nem kell kétszer megadni a személyes találkozói adatait.</span><span class="sxs-lookup"><span data-stu-id="6ff76-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="6ff76-111">Egyszerűen importálhatja a személyes találkozókat a naptárból a Project Service időbejegyzés nézetbe.</span><span class="sxs-lookup"><span data-stu-id="6ff76-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="6ff76-112">A naptár szinkronizálja a projekt és munkarendelés foglalásokat a mai naptól kezdve az elkövetkezendő pár héten át.</span><span class="sxs-lookup"><span data-stu-id="6ff76-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="6ff76-113">Ez a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="6ff76-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="6ff76-114">A szinkronizálás csak egy irányba támogatott a PSA-ból az Ön [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] naptárába.</span><span class="sxs-lookup"><span data-stu-id="6ff76-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="6ff76-115">Fordított irányban is szinkronizálhat.</span><span class="sxs-lookup"><span data-stu-id="6ff76-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="6ff76-116">Az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptár használatával kapcsolatos további információkat itt talál: [Outlook webes naptár vállalati verzió](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="6ff76-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="6ff76-117">Beállítás</span><span class="sxs-lookup"><span data-stu-id="6ff76-117">Setup</span></span>  
 <span data-ttu-id="6ff76-118">Mielőtt megtekintheti és kezelheti a foglalásait az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárban, be kell állítania néhány dolgot.</span><span class="sxs-lookup"><span data-stu-id="6ff76-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="6ff76-119">Szüksége lesz az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] globális rendszergazda vagy a Rendszergazda hitelesítő adataira.</span><span class="sxs-lookup"><span data-stu-id="6ff76-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="6ff76-120">A rendszergazdájának konfigurálnia kell a levelezési kiszolgálói profilt és az egyes felhasználóknak is konfigurálniuk kell a postafiókjaikat.</span><span class="sxs-lookup"><span data-stu-id="6ff76-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6ff76-121">[E-mail-feldolgozás beállítása kiszolgálóoldali szinkronizáláson keresztül](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="6ff76-121">[Set up email processing through server-side synchronization](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="6ff76-122">Kapcsolja be a szervezet szinkronizálását (adminisztrátori feladat)</span><span class="sxs-lookup"><span data-stu-id="6ff76-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="6ff76-123">A főmenüben kattintson a **Beállítások** > **Adminisztráció** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6ff76-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="6ff76-124">Kattintson a **Rendszerbeállítások** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6ff76-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="6ff76-125">Kattintson a **Szinkronizálás** lapra.</span><span class="sxs-lookup"><span data-stu-id="6ff76-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="6ff76-126">A **Erőforrás-foglalás szinkronizálásának engedélyezésének kiválasztása ezzel** lehetőségnél válassza ki az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6ff76-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="6ff76-127">Kapcsolja be a felhasználói profil szinkronizálását (felhasználói feladat)</span><span class="sxs-lookup"><span data-stu-id="6ff76-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="6ff76-128">A képernyő jobb felső sarkában kattintson a **Beállítások** gombra .</span><span class="sxs-lookup"><span data-stu-id="6ff76-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="6ff76-129">Kattintson a **Beállítások** pontra.</span><span class="sxs-lookup"><span data-stu-id="6ff76-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="6ff76-130">Kattintson a **Szinkronizálás** lapra.</span><span class="sxs-lookup"><span data-stu-id="6ff76-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="6ff76-131">Az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőségnél válassza az **Erőforrás-foglalás szinkronizálása az Outlook programmal** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6ff76-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="6ff76-132">Importálja a személyes találkozókat (felhasználói feladat)</span><span class="sxs-lookup"><span data-stu-id="6ff76-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="6ff76-133">Importálhatja a személyes találkozókat a naptárból a Project Service Automation időbejegyzés nézetbe.</span><span class="sxs-lookup"><span data-stu-id="6ff76-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="6ff76-134">Nyissa meg az [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-naptárat, majd kattintson az **Adatok importálása** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6ff76-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="6ff76-135">A Szűrők képernyőn válassza ki a **Tőzsdei találkozók** majd az **Alkalmaz** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6ff76-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="6ff76-136">A rendszer átemeli a találkozókat az időbejegyzés nézetbe javasolt bejegyzésekként az adott hétbe.</span><span class="sxs-lookup"><span data-stu-id="6ff76-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="6ff76-137">Egy másik hét bejegyzéseinek hozzáadásához kattintson az **Előző** vagy **Következő** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6ff76-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="6ff76-138">Válassza ki a találkozót, amit hozzá szeretne adni a Project Service Automation időbejegyzés nézethez.</span><span class="sxs-lookup"><span data-stu-id="6ff76-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="6ff76-139">Az **Időbejegyzés** felugró menüben válassza ki a megfelelő lehetőségeket, hogy átalakíthassa a találkozót Project Service Automation időbejegyzés nézetté.</span><span class="sxs-lookup"><span data-stu-id="6ff76-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="6ff76-140">Kattintson a **Mentés** gombra.</span><span class="sxs-lookup"><span data-stu-id="6ff76-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6ff76-141">Kapcsolódó információk</span><span class="sxs-lookup"><span data-stu-id="6ff76-141">See Also</span></span>  
 [<span data-ttu-id="6ff76-142">Idő, Költségek és Együttműködési útmutató</span><span class="sxs-lookup"><span data-stu-id="6ff76-142">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)