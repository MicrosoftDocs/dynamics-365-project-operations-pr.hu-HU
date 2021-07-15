---
title: Ütemezési segéd áttekintése
description: Ez a témakör az erőforrások Ütemezési segéddel végzett foglalásához nyújt tájékoztatást.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368119"
---
# <a name="schedule-assistant-overview"></a>Ütemezési segéd áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az Ütemezési segéd erőforrások foglalására szolgál a projektmenedzser által meghatározott követelmények alapján. Az ütemezési segéd az erőforrás-követelményben megadott paraméterekre támaszkodik az erőforrás megkereséséhez. Az Ütemezési segéd olyan erőforrásokat javasol, amelyek megfelelnek a vonatkozó követelményeknek, például az időablakoknak vagy a szükséges szakértelmeknek.

A megfelelő erőforrások azonosítását követően az erőforráskezelő vagy a projektmenedzser lefoglalhatja az erőforrást a munkához.

## <a name="prerequisites"></a>Előfeltételek

Az Ütemezési segéd a Universal Resource Scheduling megoldás része. Ez a megoldás megtalálható és telepítve van a Dynamics 365 Project Operations, a Dynamics 365 Field Service és a Dynamics 365 Customer Service rendszerekbe.

## <a name="matching-requirements-and-resources"></a>Erőforrások és követelmények párosítása

A létrehozott erőforrás-követelmény olyan részleteken alapul, mint például:

-   Jellemzők
-   Szerepkörök
-   Részlegek
-   Erőforrás-preferenciák
-   Munkaigénykontúrok
-   Időzóna

Az Ütemezési segéd ezeket az adatokat használja az erőforrások szűréséhez.

## <a name="launch-the-schedule-assistant"></a>Az Ütemezési segéd indítása

Az ütemezési segéd kétféleképpen indítható el. Ha hibrid módot használ, a csapattagrácsában bármelyik csapattagot kijelölheti, akinek nem teljesült erőforrás-követelménye van, majd kiválaszthatja a **Foglalás** lehetőséget. Ha a központi módot használja, az erőforrás-kezelő megkeresi és kiválasztja az erőforrást.

## <a name="schedule-assistant-filters"></a>Ütemezési segéd szűrői

Az Ütemezési segéd futását követően az erőforrás-követelmény részletei szűrt értékként jelennek meg a bal oldali ablaktáblában. Az erőforrás-kezelő vagy a projektmenedzser az ütemezési igényeknek megfelelően, a szűrők módosításával finomíthatja az eredményeket.

A szűrőablakon a munkával kapcsolatos beállítások láthatók, például:

-   Munka kezdete és befejezése
-   Jellemzők
-   Szerepkörök
-   Szervezeti egységek
-   Erőforrás-kezelő vállalat
-   Erőforrástípusok
-   Előnyben részesített erőforrások


[!INCLUDE[footer-include](../includes/footer-banner.md)]