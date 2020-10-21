---
title: Jóváhagyások áttekintése
description: Ez a témakör a jóváhagyások Project Operationsben való használatáról nyújt tájékoztatást.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961169"
---
# <a name="approvals-overview"></a>Jóváhagyások áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az idő- és a kiadásbeküldések egy jóváhagyási munkafolyamaton mennek keresztül. A bejegyzések jóváhagyását követően a rendszer a tényleges adatokban rögzíti a tranzakciókat, és az ütemezésben könyveli az időt.

## <a name="approvals-workflow"></a>Jóváhagyási munkamenet
Amikor idő- vagy költségbejegyzést hoz létre és küld el, egy jóváhagyásibejegyzés jön létre. A projekt jóváhagyója vagy felettese áttekinti és jóváhagyja a bejegyzést. Ha a bejegyzés egy projekthez kapcsolódik, a jóváhagyásakor a rendszer létrehozza a tényleges adatokat. Ez lehetővé teszi a költségek és a számlázás nyomon követését. 

## <a name="approve-an-entry"></a>Bejegyzés jóváhagyása
A **Jóváhagyások** űrlap lehetővé teszi a különböző nézetek közötti váltást, így a különböző típusú jóváhagyások tekinthetők meg.
  
1. Nyissa meg a **Jóváhagyások** űrlapot, és válassza a **Kiadások**, az **Idő** vagy a **Visszahívások** lehetőséget.
2. Tekintse át az egyes jóváhagyásokat, és jelölje ki a jóváhagyni kívántakat.
3. Válassza a **Jóváhagyás** lehetőséget a kijelölt bejegyzések jóváhagyásához.
A rendszer ezeket a bejegyzéseket feldolgozza, és tényleges adatokat vagy foglalást hoz létre.

## <a name="reject-an-entry"></a>Bejegyzés elutasítása
A projekt jóváhagyójaként előfordulhat, hogy a felhasználónak vissza kell küldenie egy bejegyzést a felhasználóhoz helyesbítés céljából.
  
1. Nyissa meg a **Jóváhagyások** űrlapot, és válassza ki az elutasítani kívánt bejegyzést. 
2. Válassza az **Elutasítás** lehetőséget.
3. Nem kötelező – Megjegyzést adhat hozzá az **Elutasítási hozzászólások** párbeszédpanelen, hogy tájékoztassa a felhasználót a bejegyzés visszautasításának okáról.
4. Kattintson az **OK** gombra. A rendszer visszaküldi a bejegyzést a felhasználónak.
  
## <a name="recall-entries"></a>Bejegyzések visszavonása
Előfordulhat, hogy egy elküldött bejegyzést vissza kell hívnia. Ha a bejegyzést még nem hagyták jóvá, akkor a rendszer azonnal visszaküldi. A jóváhagyott bejegyzésnek azonban jelentős hatása lehet. A projekt jóváhagyójának jóvá kell hagynia a visszahívást a tranzakció sztornírozásához a tényleges adatokban.

## <a name="specify-project-approvers"></a>Projekt jóváhagyóinak megadása
Minden projekthez bizonyos számú projektcsapattag tartozik. Megadhatja, hogy mely csoporttagok projektjóváhagyók is egyben.

1. Lépjen a **Projektek** űrlapra, és nyissa meg a projektet a listából.
2. A **Csapat** lapon jelölje ki azt a csapattagot, aki a projekt jóváhagyója lesz, majd válassza a **Szerkesztés** lehetőséget.
3. Állítsa a **Projektjóváhagyó** mezőjét **Igen** értékre.
4. Válassza a **Mentés** parancsot.
5. További projektjóváhagyók hozzáadásához ismételje meg a 2–4. lépést.

## <a name="configure-the-users-manager"></a>A felhasználó felettesének konfigurálása

1. Lépjen a **Beállítások** > **Biztonság** > **Felhasználók** részre.
2. Válassza ki azt a felhasználót, akihez vezetőt rendel, és a **Szervezet adatai** területen jelölje ki a vezetőt a listából. 
3. Válassza a **Mentés** parancsot.


