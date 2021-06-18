---
title: Jóváhagyások áttekintése
description: Ez a témakör a jóváhagyások Project Operationsben való használatáról nyújt tájékoztatást.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996704"
---
# <a name="approvals-overview"></a>Jóváhagyások áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az idő-, költség- és anyaghasználati beküldések egy jóváhagyási munkafolyamaton haladnak át. A bejegyzések jóváhagyását követően a rendszer a tényleges adatokban rögzíti a tranzakciókat, és az ütemezésben könyveli az időt.

## <a name="approvals-workflow"></a>Jóváhagyási munkamenet
Idő-, költség- vagy anyagfelhasználási tétel létrehozásakor és elküldésekor jóváhagyási rekord jön létre. A projekt jóváhagyója vagy vezetője áttekinti és jóváhagyja a bejegyzést. Ha a bejegyzés egy projekthez kapcsolódik, a tényadatok a jóváhagyáskor jönnek létre. Ez lehetővé teszi a költségek és a számlázás nyomon követését.

## <a name="approve-an-entry"></a>Bejegyzés jóváhagyása
A **Jóváhagyások** lapon válthat a különböző nézetek között, így megtekintheti a különböző típusú jóváhagyásokat.
  
1. Menjen a **Jóváhagyások** lapra, és válassza a **Költségek**, **Idő**, **Anyaghasználat** vagy a **Visszahívások** lehetőséget.
2. Tekintse át az egyes jóváhagyásokat, és jelölje ki a jóváhagyni kívántakat.
3. Válassza a **Jóváhagyás** lehetőséget a kijelölt bejegyzések jóváhagyásához.
A rendszer feldolgozza ezeket a bejegyzéseket, és tényadatokat hoz létre.

## <a name="reject-an-entry"></a>Bejegyzés elutasítása
A projekt jóváhagyójaként előfordulhat, hogy a felhasználónak vissza kell küldenie egy bejegyzést a felhasználóhoz helyesbítés céljából.
  
1. Menjen a **Jóváhagyások** lapra, és jelölje ki az elutasítani kívánt bejegyzést. 
2. Válassza az **Elutasítás** lehetőséget.
3. Nem kötelező, de hozzáadhat megjegyzést az **Elutasítási megjegyzések** párbeszédpanelen, hogy tájékoztassa a felhasználót a bejegyzés elutasításának okairól.
4. Kattintson az **OK** gombra. A rendszer visszaküldi a bejegyzést a felhasználónak.
  
## <a name="cancel-approval"></a>Jóváhagyás visszavonása
Bizonyos esetekben előfordulhat, hogy törölnie kell egy korábban jóváhagyott bejegyzést. Egy korábban jóváhagyott bejegyzés visszavonása pénzügyi hatással jár. 

## <a name="approving-recall-requests"></a>Visszahívási kérelmek jóváhagyása
Bizonyos esetekben előfordulhat, hogy egy tanácsadónak vissza kell hívnia egy korábban jóváhagyott bejegyzést. Egy korábban jóváhagyott bejegyzés visszavonása pénzügyi hatással jár. A projekt jóváhagyójának jóvá kell hagynia a visszahívást a Tényadatokban sztornírozhassák a tranzakciót.

## <a name="specify-project-approvers"></a>Projekt jóváhagyóinak megadása
Minden projekthez bizonyos számú projektcsapattag tartozik. Megadhatja, hogy mely csoporttagok projektjóváhagyók is egyben.

1. Menjen a **Projektek** lapra, és nyissa meg a projektet a listából.
2. A **Csapat** lapon jelölje ki azt a csapattagot, aki a projekt jóváhagyója lesz, majd válassza a **Szerkesztés** lehetőséget.
3. Állítsa a **Projektjóváhagyó** mezőjét **Igen** értékre.
4. Válassza a **Mentés** parancsot.
5. További projektjóváhagyók hozzáadásához ismételje meg a 2–4. lépést.

## <a name="configure-the-users-manager"></a>A felhasználó felettesének konfigurálása

1. Lépjen a **Beállítások** > **Biztonság** > **Felhasználók** részre.
2. Válassza ki azt a felhasználót, akihez vezetőt rendel, és a **Szervezet adatai** területen jelölje ki a vezetőt a listából. 
3. Válassza a **Mentés** parancsot.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
