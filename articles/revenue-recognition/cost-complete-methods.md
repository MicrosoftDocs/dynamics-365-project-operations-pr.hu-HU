---
title: Teljesítési költség módszerei
description: Ez a cikk a projektek teljesítési költségének kiszámításához használt módszerekre vonatkozó információkat tartalmaz.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920293"
---
# <a name="cost-to-complete-methods"></a>Teljesítési költség módszerei

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a projektek teljesítési költségének kiszámításához használt módszerekre vonatkozó információkat tartalmaz. Többféle módszerrel is kiszámíthatja a projektek teljesítéséhez szükséges költséget. 

Ha egy projekthez becslést hoz létre, a **Becslés létrehozása** lapon a **Teljesítési költség módszerhez** mezőben, kiválaszthatja a következő teljesítési költség módszerek egyikét.

| Teljesítési költség módszer    | Adatfolyam leírása                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Teljes költség - tényleges            | Adja meg manuálisan a becslési költségeket a **Teljes költség** vagy a **Teljes mennyiség** mezőben a **Költségbecslés** gombbal a **Becslés oldalon**. A rendszer kivonja a tényleges költségeket a megadott végösszegből. A végösszeg a projekt teljesítésének költsége. Ez a módszer nem használja a Microsoft Dataverse-re épített Project Operations alkalmazásban megadott költség becsléseket és erőforrás-hozzárendeléseket. A teljes költség vagy teljes mennyiség bármikor frissíthető, ha szükséges.  |
| Előrejelzés összesen – tényleges        | Az erőforrás-hozzárendelések és a költségek becslése a projekt teljes előrejelzési összegének meghatározására szolgál. A program a tényleges költségeket hasonlítja össze ezzel az előrejelzéssel, hogy kiszámítsa a teljesítés költségét.                                                                                                                                                                                                                                                                          |
| Korábbi becslésként         | Az előző időszakban használt becslési módszerek lettek használva itt is. Ha az előző időszakban előrejelzési modellre volt szükség, akkor ehhez a módszerhez is előrejelzési modell szükséges.                                                                                                                                                                                                                                                                                                                           |
| Teljesítési költség nullára állítása | A becsült projekt eltávolítása előtt használatos általában, ez a módszer egyeztet a könyvelt tényleges tranzakciókkal, és a költséget kiüríti a **Teljesítési költség** oszlopot. Amikor a elkészült, az eredmény mindig 100 százalék. Minden létrehozott költségsor esetén az **Előrejelzés** jelölőnégyzet nincs bejelölve, és a teljes becslést a program a korábbi költségbecslésből másolja. A projekt teljesítéséhez a rendszer levonja a becslési időszak tényleges fogyasztását a költségekből.              |
| Költségsablonból           | A kiválasztott becsült projekthez társított költség sablonban beállított teljesítési költség módszer.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]