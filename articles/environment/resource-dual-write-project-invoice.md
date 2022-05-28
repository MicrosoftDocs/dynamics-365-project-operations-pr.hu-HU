---
title: Projektszámla integrációja
description: Ez témakör a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581241"
---
# <a name="project-invoice-integration"></a>Projektszámla integrációja

Ez témakör a Project Operations felületen a vevők felé történő számlázás kettős írással történő integrációjáról nyújt tájékoztatást.

A Project Operations felületen a projektmenedzser kezeli a projekt számlázási lemaradást, és proforma számlát hoz létre az ügyfél számára a(z) Microsoft Dataverse felületen. A proforma számla alapján a Kötelezettségek ügyintézője vagy Projektkönyvelő létrehoz egy vevői számlát. A kettős írású integráció biztosítja, hogy a proforma számla részletei szinkronizálva legyenek a Pénzügy és műveletek alkalmazásokkal. Az ügyféloldali számla feladása után a rendszer frissíti a projekt tényleges adatait a könyvelési adatokkal a(z) Dataverse felületen. Az alábbi ábra magas szintű fogalmi áttekintést nyújt erről az integrációról.

   ![Projektszámla integrációja.](./media/DW5Invoicing.png)

Miután a Projektmenedzser megerősítette a proforma számlát a alkalmazásban Dataverse, a proforma számlafej adatai szinkronizálódnak a Pénzügy és műveletek alkalmazásokkal a kettős írási táblatérkép, **a Project számlajavaslat V2 (számlák) használatával**. Ez egy egyirányú integráció Dataverse a Pénzügy és műveletek alkalmazásokba. A Project számlajavaslatainak létrehozása vagy törlése közvetlenül a Pénzügy és műveletek alkalmazásban nem támogatott.

A számla visszaigazolása a(z) Dataverse felületen elindítja azt az üzleti logikát is, számlázással kapcsolatos rekordok létrehozásához az **Tényleges adatok** entitásban. Ezek a rekordok szinkronizálódnak a Pénzügy és műveletek programmal a kettős írású táblaleképezés, **a Projektműveletek integrációs tényleges adatai (msdyn\_ tényleges adatok) használatával.** További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md). 

A projektszámla-javaslatsorokat az **Űrlap importálása** időszakos folyamat hozza létre. Ez a folyamat a **tényleges adatok előkészítési táblájában** szereplő számlázott értékesítési adatokon alapul. További információ: [Projektszámla-javaslatok kezelése](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
