---
title: Időbeviteli naptár
description: Ez a témakör az időbeviteli naptár használatáról nyújt információkat.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752267"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="d2c78-103">Időbeviteli naptár</span><span class="sxs-lookup"><span data-stu-id="d2c78-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d2c78-104">Az **Időbevitel** oldalon megtekintheti az időbejegyzéseket a naptárban a **Megjelenítés mint** \> **Naptárvezérlés** kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="d2c78-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="d2c78-105">Frissített naptárvezérlés</span><span class="sxs-lookup"><span data-stu-id="d2c78-105">Updated calendar control</span></span>

<span data-ttu-id="d2c78-106">A Dynamics 365 Project Service Automation új és meghosszabbítható időbeviteli élményt kínál.</span><span class="sxs-lookup"><span data-stu-id="d2c78-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="d2c78-107">Ez az új élmény felváltja a korábbi verziókban használt Egyéni naptárvezérlőt.</span><span class="sxs-lookup"><span data-stu-id="d2c78-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="d2c78-108">Az időbejegyzéseket azonban csak olvasható naptárvezérlőn tekintheti meg, amelyet az Egyesített interfész keretrendszer biztosít napi, heti vagy havi nézetekhez.</span><span class="sxs-lookup"><span data-stu-id="d2c78-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="d2c78-109">A naptár nem támogatja az egyes naptári tételekkel kapcsolatos műveleteket, és egy vagy több naptár elemet nem választhat be benyújtásra vagy törlésre.</span><span class="sxs-lookup"><span data-stu-id="d2c78-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="d2c78-110">Ehelyett válassza ki a naptár elemet az **Időbejegyzés** entitásoldal megnyitásához, ahol elvégezheti a szükséges műveleteket.</span><span class="sxs-lookup"><span data-stu-id="d2c78-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="d2c78-111">Bővíthetőség</span><span class="sxs-lookup"><span data-stu-id="d2c78-111">Extensibility</span></span>

<span data-ttu-id="d2c78-112">Az **Időbejegyzések** oldalon, amelyen megtalálható az időbeviteli rács, hozzáadhat egyéni mezőket, beállíthat keresési mezőket, és létrehozhat egyéni nézeteket.</span><span class="sxs-lookup"><span data-stu-id="d2c78-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="d2c78-113">Beállíthat egyéni üzleti logikát is, amely az egyéni mezőkben kiválasztott vagy bevitt értékeken alapul.</span><span class="sxs-lookup"><span data-stu-id="d2c78-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
