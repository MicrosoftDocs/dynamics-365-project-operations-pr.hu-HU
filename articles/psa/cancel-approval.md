---
title: A korábban jóváhagyott idő- és költségbejegyzések visszavonása
description: Ez a témakör a projekt jóváhagyott idő- és költségtranzakciójának visszavonásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 09b85ea302ac46171afbd531a551aa5fbf5492a3644cba3448be03009840228c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987439"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>A korábban jóváhagyott idő- vagy költségbejegyzések visszavonása

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Dynamics 365 Project Service Automation legújabb verziójában a jóváhagyók visszavonhatják a korábban jóváhagyott idő- és költségbejegyzéseket.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Korábban jóváhagyott idő- vagy költségbejegyzés visszavonása

Az alábbi lépések végrehajtásával vonhatja vissza a korábban jóváhagyott idő- vagy költségbejegyzést.

1. Válassza a **Projektek** \> **Saját munka** \> **Jóváhagyások** lehetőséget.
2. A **Jóváhagyások** listaoldalon módosítsa a nézetet a **Saját korábbi jóváhagyások** értékre. Megjelenik a korábban jóváhagyott idő- és költségbejegyzések listája.
3. Jelöljön ki egy vagy több bejegyzést, majd jelölje be a **Jóváhagyás visszavonása** jelölőnégyzetet. Figyelmeztető üzenet jelenik meg.
4. A jóváhagyás visszavonásához válassza az **OK** gombot.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Az idő- és a költségbejegyzés-jóváhagyás visszavonásának hatásáról

A jóváhagyás visszavonása esetén a működési hatás és a pénzügyi hatás egyaránt fennáll.

### <a name="operational-impact"></a>Működési hatás

A műveletek oldalon a jóváhagyás visszavonásakor a rekord állapota **Tervezet** értékre van állítva, és a jóváhagyás már nem jelenik meg a **Saját korábbi jóváhagyások** nézetben. Ehelyett a visszavont jóváhagyás vagy a **Jóváhagyandó időbejegyzések** nézetben, vagy a **Jóváhagyandó bejegyzések** nézetben jelenik meg attól függően, hogy idő- vagy költségbejegyzés volt-e. Emellett a kapcsolódó idő- vagy költségbejegyzés állapota **Beküldött** lesz, így a kapcsolódó bejegyzés konzisztens lesz a **Tervezet** állapotban lévő jóváhagyásokkal.

Jóváhagyóként a jóváhagyás néhány mezőjét szerkesztheti, amelynek állapota **Tervezet**. Ezekhez a mezőkhöz tartozik a **Számlázás típusa** és az **Időbejegyzések számlázható órái**. A módosítások végrehajtása után ismét jóváhagyhatja a rekordot. Másik lehetőségként elutasíthatja a bejegyzést. Ha elutasítja egy időbejegyzés jóváhagyását, akkor a bejegyzés állapota **Visszaküldött** lesz. Ha elutasítja egy költségbejegyzés jóváhagyását, akkor a bejegyzés állapota **Elutasított** lesz. A visszaküldött és a visszautasított bejegyzések működése megegyezik a **Tervezet** állapotú bejegyzésekkel. A projektcsapat bármelyik tagja elvégezheti a bejegyzéshez szükséges változtatásokat, majd újból beküldheti jóváhagyásra, vagy teljesen törölheti a bejegyzést.

### <a name="financial-impact"></a>Pénzügyi hatás

A projektet a jóváhagyás visszavonása után is éri pénzügyi hatás. Előrször is a következő módon frissíti a rendszer a megfelelő költség- és értékesítési tényadatokat:

- A korrekció állapota **Korrigálva** érték lesz.
- A számlázás állapota **Visszavonva** érték lesz.

A következő lépésként létrejönnek a sztornózott bejegyzések a Tényadatok táblában. Sztornózott bejegyzések létrehozásához a rendszer átmásolja az eredeti tényadatok mezőinek értékeit. Csak a minőségi értékek nem lesznek átmásolva. Ezeket az értékeket sztornózza a rendszer. Mind a **Költség**, mind a **Számlázatlan értékesítés** tényadatai esetén létrejönnek sztornózott tényadatok. A sztornózott tényadat **Korrekció állapota** mezőjének értéke **Nem korrigálható**, a számlázás állapota mező értéke **Visszavonva** lesz.

A módosítások elvégzése után a projektre költött összegként és a projekt bevételi tartalékaként rögzített összeg a továbbiakban nem lesz felszámítva az ezen tényadatok által jelentett összegek esetén.


[!INCLUDE[footer-include](../includes/footer-banner.md)]