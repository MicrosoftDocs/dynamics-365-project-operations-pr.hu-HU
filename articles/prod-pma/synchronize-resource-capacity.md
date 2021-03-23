---
title: Erőforrás-kapacitás szinkronizálása
description: Ez a témakör információkat tartalmaz arról, hogyan szinkronizálható az erőforrások kapacitása a naptárak és a projektek között.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288563"
---
# <a name="synchronize-resource-capacity"></a>Erőforrás-kapacitás szinkronizálása

[!include [banner](../includes/banner.md)]

Az erőforrás-szinkronizálási folyamatok segítségével biztosítható, hogy a naptár és az alapnaptár adatai eljutnak a projekterőforrás-ütemezésébe. A naptár módosítása esetén a folyamat végrehajtja a projektek erőforrásainak ütemezéséhez szükséges frissítéseket. A folyamatok a teljesítmény javítását is segítik, mivel a naptár erőforrás-információit előre szinkronizálja a rendszer. Ezért gyorsabban történnek az erőforrás-ütemezési adatok frissítései. Javasoljuk, hogy a folyamatokat ne egyenként, hanem kötegelve ütemezze. Ellenkező esetben fennáll annak a veszélye, hogy valaki elfelejti a bezárólagos dátumokat, amikor az adatok legutóbbi szinkronizálása megtörtént. Ha nem bezárólagos dátumokat használ, akkor a szinkronizálás során hézagok keletkezhetnek.

![Naptár szinkronizálása](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Erőforráskapacitás-összesítések szinkronizálása

A szinkronizálási folyamat az összes erőforrásnaptár-információ szinkronizálására szolgál. Ezek az információk a projekt erőforrásnaptár-kapacitásainak táblázatában bekövetkezett változásokkal kapcsolatos alapvető naptár-információkat tartalmazza. Ha új erőforrásokat vesz fel a projektbe, a szinkronizálás segít biztosítani, hogy a frissített naptárinformációk elérhetők legyenek. A szinkronizálás bármikor végrehajtható.

Javasoljuk, hogy használja használjon köteget. A beállítások a kapacitásfoglalások szinkronizálása során érhetők el.

1. Válassza a **Projektmenedzsment és könyvelés** &gt; **Időszakos** &gt; **Kapacitás szinkronizálása** &gt; **Erőforráskapacitás-összesítések szinkronizálása** lehetőséget.
2. Adja meg a beállításokat a következő táblázatban.

    | Beállítás      | Ismertetés |
    |-------------|-------------|
    | Időszak kódja | Opcionálisan kiválaszthatja a főkönyvi dátum intervallumkódját az erőforráskapacitás-összesítések szinkronizálási folyamatához tartozó kezdő és záró dátumok beállításához. |
    | Kezdő dátum  | Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának kezdő dátumát. |
    | Befejező dátum    | Adja meg az erőforráskapacitás-összesítések szinkronizálási folyamatának záró dátumát. |

[![Szinkronizálási folyamat](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]