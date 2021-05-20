---
title: Jelentés kezdőlapja
description: Ez a témakör a Dynamics 365 Project Service Automation rendszerben történő jelentések leírását tartalmazza.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951482"
---
# <a name="reporting-home-page"></a><span data-ttu-id="5be58-103">Jelentéskészítés kezdőlapja</span><span class="sxs-lookup"><span data-stu-id="5be58-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5be58-104">A Microsoft Dynamics 365 Project Service Automation lehetővé teszi, hogy a projektalapú szervezetek hatékonyan irányítsák üzleti tevékenységeiket.</span><span class="sxs-lookup"><span data-stu-id="5be58-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="5be58-105">Bármely projektnél a csapat tagjainak kezelnie kell a lehetőséget, árajánlatot kell tenniük és meg kell terveznie a munkát, forrásokat kell készítenie a projektekre, a munkát a terv szerint kell irányítania, a munkáról számlát kell készítenie, majd meg kell tennie a munkát a projekt befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="5be58-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="5be58-106">A műveletekről szóló jelentések készítése kulcsfontosságú a szervezet állapotának meghatározásához és a szükséges korrekciós intézkedések megtételéhez.</span><span class="sxs-lookup"><span data-stu-id="5be58-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="5be58-107">A PSA Microsoft Dynamics 365 jelentési módszert és technológiát alkalmaz az összes jelentésre.</span><span class="sxs-lookup"><span data-stu-id="5be58-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="5be58-108">A jelentéskészítési lehetőségekkel kapcsolatos további információkért tekintse meg [Jelentéskészítési útmutató a Dynamics 365 Customer Engagement (on-premises) 9.es verziójához](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365) című témakört.</span><span class="sxs-lookup"><span data-stu-id="5be58-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="5be58-109">Jelentéskészítő varázsló</span><span class="sxs-lookup"><span data-stu-id="5be58-109">Report Wizard</span></span>

<span data-ttu-id="5be58-110">A Jelentés varázsló segítségével a nem fejlesztők egyszerű jelentéseket készíthetnek.</span><span class="sxs-lookup"><span data-stu-id="5be58-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="5be58-111">Mivel az alkalmazás egy meglévő platformra épül, az élmény ugyanaz, mint az az élmény, amely a [Jelentés létrehozása vagy szerkesztése a Jelentés varázslóban](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) van dokumentálva.</span><span class="sxs-lookup"><span data-stu-id="5be58-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="5be58-112">Ugyanakkor a Project Service Automation-specifikus entitásokat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5be58-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="5be58-113">Egyéni SQL Server Reporting Services jelentések</span><span class="sxs-lookup"><span data-stu-id="5be58-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="5be58-114">Ha vállalkozása olyan konkrét jelentést igényel, amelyet nem lehet a Jelentés varázslóval létrehozni, létrehozhat egyéni jelentést.</span><span class="sxs-lookup"><span data-stu-id="5be58-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="5be58-115">Telepítenie kell a Microsoft Visual Studio- t, a megfelelő Microsoft SQL Server Data Tools-vel és a Jelentés-készítő kiterjesztésekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="5be58-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="5be58-116">Az eszközökkel és a verziókkal kapcsolatos további információkért lásd: [Jelentésírási környezet SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools) segítségével.</span><span class="sxs-lookup"><span data-stu-id="5be58-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="5be58-117">Az egyedi jelentés létrehozásáról lásd: [Új jelentés létrehozása a SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools) segítségével.</span><span class="sxs-lookup"><span data-stu-id="5be58-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="5be58-118">Power BI betekintési alkalmazások</span><span class="sxs-lookup"><span data-stu-id="5be58-118">Power BI insights apps</span></span>

<span data-ttu-id="5be58-119">A Microsoft Power BI és a Dynamics 365 együttesen hatékony módszert kínál adatainak kezelésére betekintő alkalmazások formájában.</span><span class="sxs-lookup"><span data-stu-id="5be58-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="5be58-120">A betekintést nyújtó alkalmazások elérhetőségéről a [Power BI Betekintési alkalmazások oldalon](https://powerbi.microsoft.com/power-bi-insights-apps/) tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="5be58-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5be58-121">További információforrások</span><span class="sxs-lookup"><span data-stu-id="5be58-121">Additional resources</span></span>
<span data-ttu-id="5be58-122">A PSA-ban történő jelentéssel kapcsolatos további információkért lásd a következő témákat:</span><span class="sxs-lookup"><span data-stu-id="5be58-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="5be58-123">Munka a Project Service adatmodellel</span><span class="sxs-lookup"><span data-stu-id="5be58-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="5be58-124">Irányítópultok</span><span class="sxs-lookup"><span data-stu-id="5be58-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]