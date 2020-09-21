---
title: Jelentés kezdőlapja
description: Ez a témakör a Dynamics 365 Project Service Automation rendszerben történő jelentések leírását tartalmazza.
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ee9bdfc6-123d-4146-8706-eab76fa37b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 42e24f42fd80b445718f81f4ff40e52c8cdaa7ba
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752278"
---
# <a name="reporting-home-page"></a>Jelentés kezdőlapja

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Microsoft Dynamics 365 Project Service Automation lehetővé teszi, hogy a projektalapú szervezetek hatékonyan irányítsák üzleti tevékenységeiket. Bármely projektnél a csapat tagjainak kezelnie kell a lehetőséget, árajánlatot kell tenniük és meg kell terveznie a munkát, forrásokat kell készítenie a projektekre, a munkát a terv szerint kell irányítania, a munkáról számlát kell készítenie, majd meg kell tennie a munkát a projekt befejezéséhez. A műveletekről szóló jelentések készítése kulcsfontosságú a szervezet állapotának meghatározásához és a szükséges korrekciós intézkedések megtételéhez. A PSA Microsoft Dynamics 365 jelentési módszert és technológiát alkalmaz az összes jelentésre. A jelentéskészítési lehetőségekkel kapcsolatos további információkért tekintse meg [Jelentéskészítési útmutató a Dynamics 365 Customer Engagement (on-premises) 9.es verziójához](../analytics/reporting-analytics-with-dynamics-365.md) című témakört.

## <a name="report-wizard"></a>Jelentéskészítő varázsló

A Jelentés varázsló segítségével a nem fejlesztők egyszerű jelentéseket készíthetnek. Mivel az alkalmazás egy meglévő platformra épül, az élmény ugyanaz, mint az az élmény, amely a [Jelentés létrehozása vagy szerkesztése a Jelentés varázslóban](../basics/create-edit-copy-report-wizard.md) van dokumentálva. Ugyanakkor a Project Service Automation-specifikus entitásokat fogja használni.

## <a name="custom-sql-server-reporting-services-reports"></a>Egyéni SQL Server Reporting Services jelentések

Ha vállalkozása olyan konkrét jelentést igényel, amelyet nem lehet a Jelentés varázslóval létrehozni, létrehozhat egyéni jelentést. Telepítenie kell a Microsoft Visual Studio- t, a megfelelő Microsoft SQL Server Data Tools-vel és a Jelentés-készítő kiterjesztésekkel együtt. Az eszközökkel és a verziókkal kapcsolatos további információkért lásd: [Jelentésírási környezet SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md) segítségével. Az egyedi jelentés létrehozásáról lásd: [Új jelentés létrehozása a SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md) segítségével.

## <a name="power-bi-insights-apps"></a>Power BI betekintési alkalmazások

A Microsoft Power BI és a Dynamics 365 együttesen hatékony módszert kínál adatainak kezelésére betekintő alkalmazások formájában. A betekintést nyújtó alkalmazások elérhetőségéről a [Power BI Betekintési alkalmazások oldalon](https://powerbi.microsoft.com/power-bi-insights-apps/) tájékozódhat.


## <a name="additional-resources"></a>További információforrások
A PSA-ban történő jelentéssel kapcsolatos további információkért lásd a következő témákat:

- [Munka a Project Service adatmodellel](reports-working-project-service-data-model.md)
- [Irányítópultok](reports-dashboards.md)

