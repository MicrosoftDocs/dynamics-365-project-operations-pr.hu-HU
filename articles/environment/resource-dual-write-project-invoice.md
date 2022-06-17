---
title: Projektszámla integrációja
description: Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást az ügyfelek számlázásához.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912105"
---
# <a name="project-invoice-integration"></a>Projektszámla integrációja

Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást az ügyfelek számlázásához.

A Project Operations felületen a projektmenedzser kezeli a projekt számlázási lemaradást, és proforma számlát hoz létre az ügyfél számára a(z) Microsoft Dataverse felületen. A proforma számla alapján a Kötelezettségek ügyintézője vagy Projektkönyvelő létrehoz egy vevői számlát. A kettős írás integrációja biztosítja, hogy a proforma számla részletei szinkronizálva legyenek a Finance and Operations alkalmazásokkal. Az ügyféloldali számla feladása után a rendszer frissíti a projekt tényleges adatait a könyvelési adatokkal a(z) Dataverse felületen. Az alábbi ábra magas szintű fogalmi áttekintést nyújt erről az integrációról.

   ![Projektszámla integrációja.](./media/DW5Invoicing.png)

Miután a Projektmenedzser megerősítette a proforma számlát Dataverse, a proforma számlafejléc adatai szinkronizálódnak a Finance and Operations alkalmazásokkal a kettős írású táblatérkép, **a V2-es számlajavaslat (számlák) használatával**. Ez egy egyirányú integráció a Finance and Operations alkalmazásoktól Dataverse. A Project számlajavaslatok létrehozása vagy törlése közvetlenül a Finance and Operations alkalmazásokban nem támogatott.

A számla visszaigazolása a(z) Dataverse felületen elindítja azt az üzleti logikát is, számlázással kapcsolatos rekordok létrehozásához az **Tényleges adatok** entitásban. Ezek a rekordok a Finance and Operations rendszerrel szinkronizálódnak a kettős írású táblatérkép, **a Project Operations integrációs actuals (msdyn\_ actuals) használatával.** További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md). 

A projektszámla-javaslatsorokat az **Űrlap importálása** időszakos folyamat hozza létre. Ez a folyamat a **tényleges adatok előkészítési táblájában** szereplő számlázott értékesítési adatokon alapul. További információ: [Projektszámla-javaslatok kezelése](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
