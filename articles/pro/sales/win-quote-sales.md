---
title: Árajánlat lezárása - Lite
description: Ez a témakör az árajánlatok Project Operationsben való lezárásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175714"
---
# <a name="close-a-quote---lite"></a>Árajánlat lezárása - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektárajánlat megnyertként vagy elvesztettként zárható le. Az Aktiválás és Felülvizsgálat funkciók nem támogatottak a Microsoft Dynamics 365 Project Operations árajánlataiban, ezért a árajánlat-tervezetet lezárhatja.

## <a name="close-a-quote-as-won"></a>Árajánlat lezárása megnyertként

A projektárajánlat megnyertként való lezárása az árajánlat állapotát Lezárt értékkel zárja le, és az állapot oka Megnyert lesz. Az árajánlatok lezárása csak olvashatóvá teszi a projektárajánlatot, és az összes árajánlati információval létrehozza a projektszerződés vázlatát. Mivel a lezárt árajánlat nem nyitható meg újra, egy megerősítő párbeszédpanel jelenik meg, amely a változtatások végrehajtása előtt megerősítést kér, mivel a lezárt árajánlat nem nyitható meg újra, és a változtatások visszafordíthatatlanok.

Ha az árajánlat egy lehetőséghez van csatolva, akkor a lehetőségen szereplő bármely más projektárajánlat automatikusan lezáródik elveszítettként.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Az árajánlat megnyertként történő lezárásának pénzügyi hatása

Ha a projekthez tényleges időadatok lettek rögzítve, miközben még csatolva van a vázlat árajánlathoz, akkor csak az idő vagy a kiadás költsége kerül rögzítésre. Miután egy árajánlatot megnyertként lezárnak, az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újrabontja a költségeket. Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel ezeket a tényleges költségértékeket. Ha a tényleges költségadatok egy idő-és anyagelszámolású szerződéssorra hivatkoznak, a rendszer automatikusan létrehozza a megfelelő, nem számlázott tényleges értékesítési adatokat az ajánlat lezárásakor és a projektszerződés létrehozásakor. Ha a tényleges költségadatok rögzített árú szerződéssorra hivatkoznak, akkor az alkalmazás leállítja a tényleges költségadatok feldolgozását a projektszerződés ügyfeleinek felosztott számlázási szabályai alapján.

## <a name="closing-a-quote-as-lost"></a>Árajánlat lezárása elvesztettként:

A projektárajánlat elvesztettként való lezárása az árajánlat állapotát Lezárt értékre módosítja, és az állapot oka Elvesztett lesz. Az ajánlat lezárása írásvédetté teszi a projektárajánlatot. Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.

Ha az elvesztettként lezárt projektárajánlat valamely sorára egy projekt hivatkozik, akkor az a projekt lezártként van megjelölve, és az adott naptól kezdve az összes erőforrás-foglalás visszavonásra kerül.

> [!NOTE]
> A Project Operationsben az árajánlat megnyertként vagy elvesztettként való lezárása nem befolyásolja a lehetőség állapotát, amely mindaddig nyitva marad, amíg manuálisan le nem zárja.
