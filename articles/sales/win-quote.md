---
title: Egy ajánlat lezárása
description: Ez a témakör az árajánlatok Project Operationsben való lezárásáról nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898894"
---
# <a name="close-a-quote"></a>Egy ajánlat lezárása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektárajánlat megnyertként vagy elvesztettként zárható le. Mivel az Aktiválás és Felülvizsgálat funkciók nem támogatottak a Microsoft Dynamics 365 Project Operations árajánlataiban, lezárhatja az árajánlat-tervezetet.

## <a name="close-a-quote-as-won"></a>Árajánlat lezárása megnyertként

A projektárajánlat megnyertként való lezárása az árajánlat állapotát **Lezárt** értékre módosítja, és az állapot oka **Megnyert** lesz. Az árajánlatok lezárása csak olvashatóvá teszi őket, és az összes árajánlati információval létrehozza a projektszerződés vázlatát. Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.

A projektárajánlatból létrehozott projektszerződés a Project Operations Projektmenedzsment és könyvelés moduljában is elérhetővé válik. Ha egy projektszerződés nincs leképezve egy projektre annak bármelyik sorában, akkor ez a projektszerződés inaktív projektszerződésként elérhetővé válik, és akkor aktiválódik, amikor egy projekt le van képezve a szerződéssorai legalább egyikére.

Ha az árajánlat egy lehetőséghez van csatolva, akkor a lehetőségen szereplő bármely más projektárajánlat automatikusan lezáródik elveszítettként.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Az árajánlat megnyertként történő lezárásának pénzügyi hatása

Ha a projekthez tényleges időadatok lettek rögzítve, miközben még csatolva van a vázlat árajánlathoz, akkor csak az idő vagy a kiadás költsége kerül rögzítésre. Miután egy árajánlatot megnyertként lezárnak, az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újrabontja a költségeket. Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel ezeket a tényleges költségértékeket. Ha a tényleges költségadatok egy idő-és anyagelszámolású szerződéssorra hivatkoznak, a rendszer automatikusan létrehozza a megfelelő, nem számlázott tényleges értékesítési adatokat az ajánlat lezárásakor és a projektszerződés létrehozásakor. Ha a tényleges költségadatok rögzített árú szerződéssorra hivatkoznak, akkor az alkalmazás leállítja a tényleges költségadatok feldolgozását a projektszerződés ügyfeleinek felosztott számlázási szabályai alapján.

Az összes újrafeldolgozott tényleges adat elérhető a projekt könyvelőjének Projektmenedzsment és könyvelés moduljában, hogy áttekintse, frissítse és könyvelje a tételeket a főkönyvbe. 

## <a name="close-a-quote-as-lost"></a>Árajánlat lezárása elvesztettként

A projektárajánlat elvesztettként való lezárása az árajánlat állapotát **Lezárt** értékre módosítja, és az állapot oka **Elvesztett** lesz. Az árajánlat a lezárás hatására írásvédett lesz. Mivel egy lezárt árajánlatot nem lehet újra megnyitni, mielőtt lezárja az árajánlatot, egy megerősítő párbeszédpanel jelenik meg a módosítások megerősítéséhez.

Ha az elvesztettként lezárt projektárajánlat valamely sorára egy projekt hivatkozik, akkor az a projekt lezártként van megjelölve, és az adott naptól kezdve az összes erőforrás-foglalás visszavonásra kerül.

> [!NOTE]
> A Project Operationsben az árajánlat megnyertként vagy elvesztettként való lezárása nem befolyásolja a lehetőség állapotát, amely mindaddig nyitva marad, amíg manuálisan le nem zárja.
