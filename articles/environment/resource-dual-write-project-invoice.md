---
title: Projektszámla integrációja
description: Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást az ügyfelek számlázásához.
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

Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást az ügyfelek számlázásához.

A Project Operations felületen a projektmenedzser kezeli a projekt számlázási lemaradást, és proforma számlát hoz létre az ügyfél számára a(z) Microsoft Dataverse felületen. A proforma számla alapján a Kötelezettségek ügyintézője vagy Projektkönyvelő létrehoz egy vevői számlát. A kettős írás integrációja biztosítja, hogy a proforma számla részletei szinkronizálva legyenek a pénzügyi és üzemeltetési alkalmazásokkal. Az ügyféloldali számla feladása után a rendszer frissíti a projekt tényleges adatait a könyvelési adatokkal a(z) Dataverse felületen. Az alábbi ábra magas szintű fogalmi áttekintést nyújt erről az integrációról.

   ![Projektszámla integrációja.](./media/DW5Invoicing.png)

Miután a Projektmenedzser megerősítette a proforma számlát a következőben: Dataverse a proforma számlafejléc adatai szinkronizálódnak a pénzügyi és üzemeltetési alkalmazásokkal a kettős írású táblatérkép, **a V2-es számlajavaslat (számlák) használatával**. Ez egy egyirányú integráció a pénzügyi és üzemeltetési alkalmazásoktól Dataverse kezdve. A Project számlajavaslatok létrehozása vagy törlése közvetlenül a pénzügyi és üzemeltetési alkalmazásokban nem támogatott.

A számla visszaigazolása a(z) Dataverse felületen elindítja azt az üzleti logikát is, számlázással kapcsolatos rekordok létrehozásához az **Tényleges adatok** entitásban. Ezeket a rekordokat a rendszer a kettős írású táblatérkép, **a Project Operations integrációs actuals (msdyn\_ actuals) segítségével szinkronizálja a pénzügyekkel és a műveletekkel.** További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md). 

A projektszámla-javaslatsorokat az **Űrlap importálása** időszakos folyamat hozza létre. Ez a folyamat a **tényleges adatok előkészítési táblájában** szereplő számlázott értékesítési adatokon alapul. További információ: [Projektszámla-javaslatok kezelése](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
