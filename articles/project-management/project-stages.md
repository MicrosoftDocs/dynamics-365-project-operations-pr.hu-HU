---
title: Projektfázisok
description: Ez a témakör a Microsoft Dynamics Project Operations projektszakaszairól nyújt információt.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a25f32badd8776c89ad6eb56ad77ff61ad0cccae
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586209"
---
# <a name="project-stages"></a>Projektfázisok

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az Projekt szakaszainak célja, hogy tükrözzék a projekt előrehaladásának állapotát. A testreszabások segítségével automatikusan frissítheti a fázisokat az üzleti folyamatok, a Power Automate, illetve a beépülőmodul-bővítmények használatával.

Az alapértelmezett üzleti folyamat a következő szakaszokat tartalmazza:

- Új
- Ajánlat
- Csomag
- Kiszállítás
- Befejeződött
- Bezárás 

## <a name="new"></a>Új

Amikor létrehoz egy projektet, a projekt állapotát **Új**-ra állítja. Ha a projektet sablonból hozták létre, akkor lehet, hogy van ütemezése, becslése és a csapat adatai. Egyébként ez a projekt vázlata, és a fennmaradó komponenseket be kell adni.

## <a name="quote"></a>Ajánlat

Ha egy projektet árajánlattal társít, vagy amikor projektet árajánlatból készít, akkor a projekt állapotát **Árajánlat**-ra állítja , és a becsült kezdési és befejezési dátumot frissítik. Amíg a projekt **Ajánlat** szakaszban van, az **Értékesítés** lap a **Projektentitás** oldalon az árajánlat részleteit mutatja.

## <a name="plan"></a>Terv

Ha nyer egy projekthez társított ajánlatot, és a projektet a **Szerződés** szakaszba váltják, a projekt szakasza **Terv**-re frissül. Amíg a projekt a **Terv** szakaszban van, a **Projektentitás** oldal a szerződés részleteit mutatja.

## <a name="deliver"></a>Kiszállítás

Amikor a projektterv elkészült, és készen áll a projekt elindítására, a projektmenedzsernek frissítenie kell a projekt szakaszát a **Teljesítés** elemre, hogy megmutatja, hogy a projekt elindult.

## <a name="complete"></a>Teljes 

Amikor a projekt munkája befejeződött, a projektmenedzser frissítheti a szakaszt a **Kész** értékre. A projekt szakaszának a **Teljes** értékre történő frissítésével a projektmenedzser kijelenti , hogy a munka 100%-ban befejeződött, de a projektet nyitva tartják, hogy minden függőben lévő idő- vagy költségbejegyzés rögzíthető legyen.

## <a name="close"></a>Bezárás

Amikor az összes tranzakciót rögzítik a projektnél, a projektmenedzser frissítheti a szakaszt a **Bezárás** értékre. Ezen a ponton nem lehet tranzakciókat rögzíteni, és a projektet csak olvashatóvá állítják be.



[!INCLUDE[footer-include](../includes/footer-banner.md)]