---
title: Projektszámla integrációja
description: Ez a cikk a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029027"
---
# <a name="project-invoice-integration"></a>Projektszámla integrációja

Ez a cikk a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.

A Project Operations felületen a projektmenedzser kezeli a projekt számlázási lemaradást, és proforma számlát hoz létre az ügyfél számára a(z) Microsoft Dataverse felületen. A proforma számla alapján a Kötelezettségek ügyintézője vagy Projektkönyvelő létrehoz egy vevői számlát. A kettős írás integrációja biztosítja, hogy a proforma számla adatai szinkronizálva legyenek a pénzügyi és műveleti alkalmazásokkal. Az ügyféloldali számla feladása után a rendszer frissíti a projekt tényleges adatait a könyvelési adatokkal a(z) Dataverse felületen. Az alábbi ábra magas szintű fogalmi áttekintést nyújt erről az integrációról.

   ![Projektszámla integrációja.](./media/DW5Invoicing.png)

Miután a Projektmenedzser megerősíti a proforma számlát a Dataverse felületen, a proforma számla fejlécadatai szinkronizálódnak a pénzügyi és műveleti alkalmazásokkal a **Projektszámla-javaslat V2 (számlák)** kettős írású táblaleképezés segítségével. Ez egy egyirányú integráció a Dataverse és a pénzügyi és műveleti alkalmazások között. A Projektszámla-javaslatok létrehozása vagy törlése közvetlenül a pénzügyi és műveleti alkalmazásokban nem támogatott.

A számla visszaigazolása a(z) Dataverse felületen elindítja azt az üzleti logikát is, számlázással kapcsolatos rekordok létrehozásához az **Tényleges adatok** entitásban. A rendszer ezeket a rekordokat a pénzügyi és műveleti alkalmazásokkal a **Project Operations tényleges adatok integrációja (msdyn\_actuals)** kettős írású táblaleképezés segítségével szinkronizálja További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md). 

A projektszámla-javaslatsorokat az **Űrlap importálása** időszakos folyamat hozza létre. Ez a folyamat a **tényleges adatok előkészítési táblájában** szereplő számlázott értékesítési adatokon alapul. További információ: [Projektszámla-javaslatok kezelése](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
