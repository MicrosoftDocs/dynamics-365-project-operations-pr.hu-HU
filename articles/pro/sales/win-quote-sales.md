---
title: Projektárajánlatok bezárása
description: Ez a cikk az árajánlatok Project Operationsben való lezárásáról nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826178"
---
# <a name="close-project-quotes"></a>Projektárajánlatok bezárása

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A projektárajánlat megnyertként vagy elvesztettként zárható le. A tervezet ajánlatok azért zárhatóak le, mert a Microsoft Dynamics 365 Project Operations nem támogatja az ajánlatok aktiválása és átdolgozása műveleteket.

## <a name="close-a-quote-as-won"></a>Árajánlat lezárása megnyertként

Ha Megnyertként zár le egy projektajánlatot, akkor az állapota Lezárva, és az állapot oka Megnyert lesz. Az árajánlatok lezárása csak olvashatóvá teszi a projektárajánlatot, és az összes árajánlati információval létrehozza a projektszerződés vázlatát. Mivel a lezárt ajánlat nem nyitható meg újra, a megerősítő párbeszédpanel fogja megerősíteni a változtatásokat.

Ha az árajánlat egy lehetőséghez van csatolva, akkor a lehetőségen szereplő bármely más projektárajánlat automatikusan lezáródik elveszítettként.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Az árajánlat megnyertként történő lezárásának pénzügyi hatása

Ha egy projektre vonatkozó tényadatokat a tervezet ajánlatához csatolja, csak az idő- vagy pénzköltséget rögzíti a rendszer. Miután egy árajánlatot megnyertként lezárnak, az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újrabontja a költségeket. Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel ezeket a tényleges költségértékeket. Ha a költség tényadatai idő- és anyagszerződéssorra hivatkoznak, a rendszer a megfelelő számlázatlan értékesítési tényadatokat hozza létre az ajánlat lezáráskor és a projektszerződés létrehozásakor. Ha a költség tényadatai egy rögzített árú szerződéssorra hivatkoznak, az alkalmazás leállítja a projektszerződés ügyfeleire vonatkozó számlázási szabályokon alapuló költségtényadatok újbóli feldolgozását.

## <a name="closing-a-quote-as-lost"></a>Idézet lezárása elveszettként

Ha Elvesztettként zár le egy projektajánlatot, akkor az állapota Lezárva, és az állapot oka Elvesztett lesz. Az ajánlat lezárása írásvédetté teszi a projektárajánlatot. Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.

Ha az Elvesztettként lezárt projektajánlat hivatkozik valamelyik sorában lévő projektre, akkor az adott projekt Lezártként is meg lesz jelölve. Az ettől a naptól a függőben lévő összes erőforrás-foglalás visszavonásra kerül.

> [!NOTE]
> A Project Operationsben az árajánlat megnyertként vagy elvesztettként való lezárása nem befolyásolja a lehetőség állapotát, amely mindaddig nyitva marad, amíg manuálisan le nem zárja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
