---
title: Ütemezési segéd áttekintése
description: Ez a témakör az erőforrások Ütemezési segéddel végzett foglalásához nyújt tájékoztatást.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014119"
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