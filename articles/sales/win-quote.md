---
title: Árajánlat lezárása
description: Ez a cikk a Project Operationsben az idézetek záró idézőjeleiről nyújt tájékoztatást.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45bdfe5fb9eddb8f96ed1bc017596c8fe436245e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931885"
---
# <a name="close-a-quote"></a>Egy ajánlat lezárása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A projektárajánlat megnyertként vagy elvesztettként zárható le. Mivel az Aktiválás és Áttekintés funkciók nem támogatottak az ajánlatok esetében a Microsoft Dynamics 365 Project Operations alkalmazásban, ezért lezárhat egy vázlat ajánlatot.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]