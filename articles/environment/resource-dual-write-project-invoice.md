---
title: Projektszámla integrációja
description: Ez témakör a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993244"
---
# <a name="project-invoice-integration"></a>Projektszámla integrációja

Ez témakör a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.

A Project Operations felületen a projektmenedzser kezeli a projekt számlázási lemaradást, és proforma számlát hoz létre az ügyfél számára a(z) Microsoft Dataverse felületen. A proforma számla alapján a Kötelezettségek ügyintézője vagy Projektkönyvelő létrehoz egy vevői számlát. A kettős írás integrációja biztosítja, hogy a proforma számla adatai szinkronizálva legyenek a(z) Finance and Operations alkalmazásokkal. Az ügyféloldali számla feladása után a rendszer frissíti a projekt tényleges adatait a könyvelési adatokkal a(z) Dataverse felületen. Az alábbi ábra magas szintű fogalmi áttekintést nyújt erről az integrációról.

   ![Projektszámla integrációja.](./media/DW5Invoicing.png)

Miután a Projektmenedzser megerősíti a proforma számlát a(z) Dataverse felületen, a proforma számla fejlécadatai szinkronizálódnak a(z) Finance and Operations alkalmazásokkal a **Projektszámla-javaslat V2 (számlák)** kettős írású táblatérkép segítségével. Ez egy egyirányú integráció a(z) Dataverse és a(z) Finance and Operations alkalmazások között. A Projektszámla-javaslatok létrehozása vagy törlése közvetlenül a(z) Finance and Operations alkalmazásokban nem támogatott.

A számla visszaigazolása a(z) Dataverse felületen elindítja azt az üzleti logikát is, számlázással kapcsolatos rekordok létrehozásához az **Tényleges adatok** entitásban. A rendszer ezeket a rekordokat a(z) Finance and Operations alkalmazásokkal a **Project Operations tényleges adatok integrációja (msdyn\_actuals)** kettős írású táblatérkép segítségével szinkronizálja. További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md). 

A projektszámla-javaslatsorokat az **Űrlap importálása** időszakos folyamat hozza létre. Ez a folyamat a **tényleges adatok előkészítési táblájában** szereplő számlázott értékesítési adatokon alapul. További információ: [Projektszámla-javaslatok kezelése](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
