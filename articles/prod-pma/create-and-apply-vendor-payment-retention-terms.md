---
title: Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása és alkalmazása
description: Ez a cikk arról nyújt tájékoztatást, hogyan állíthat be és tarthat fenn visszatartási feltételeket a szállítói kifizetésekhez.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916751"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása és alkalmazása

[!include [banner](../includes/banner.md)] 

A szállítói fizetési visszatartási feltételek beállítása egy projekthez akkor lehet hasznos, ha a szervezet vissza szeretné tartani a szállítónak teljesített fizetések egy részét. Ha például egy szállító esetében vissza szeretne tartani kifizetést, amíg a leszállított termékek meg nem felelnek az elvárásainak. A szállítói kifizetések visszatartási feltételei megadhatók a szállítói szerződés tárgyalása során.

## <a name="create-vendor-payment-retention-terms"></a>Szállítói kifizetéssel kapcsolatos visszatartási feltételek létrehozása

Megadhatja a visszatartandó szállítói kifizetés százalékértékét, és a korábban visszatartott és felszabadítandó összegek százalékos arányát. Az összegek a szállítói számlákhoz automatikusan vissza lesznek tartva mindaddig, amíg a szerződés el nem éri a megadott teljesítési állapotot. Miután beállította a visszatartási feltételeket, az adott szállítóhoz tartozó bármely projektre alkalmazhatja őket.

A következő lépésekkel állíthatja be és tarthatja karban a szállítói kifizetések visszatartási feltételeit. 

1. Nyissa meg a **Projektmenedzsment és könyvelés** > **Visszatartás** > **Szállítói kifizetések visszatartási feltétele** lehetőséget.
2. Új Szállítói visszatartási feltétel hozzáadásához válassza az **Új** lehetőséget. A rendszer automatikusan beviszi az új feltételhez tartozó **Szabályazonosító** értékét. 
3. Írjon be egy rövid leírást a **Leírás** mezőbe, és a **Feltételek** gyorslapon válassza a **Sor hozzáadása** lehetőséget, hogy megadja a feltételek értékeit a következőkhöz:

   - **A leszállított egységek százalékos aránya**: Adja meg a kifejezés teljesítésének százalékos értékét. Az összegek a szállítói számlákhoz automatikusan vissza lesznek tartva mindaddig, amíg a projekt teljesítési állapota el nem éri a megadott teljesítési százalékértéket. Ha például az 50,00 értéket adja meg, akkor a program az összegeket mindaddig visszatartja amíg a projekt 50%-ban be nem fejeződött.
   - **Megtartás százalékos aránya**: Adja meg a visszatartott szállítói számlaösszeg százalékos értékét. Ha például a 10,00 értéket adja meg, akkor a program a szállítói számlán szereplő összeg 10%-át tartja vissza, amíg a projekt e nem éri a **A leszállított egységek százalékos aránya** mezőben meghatározott teljesítési százalékot.
   - **Százalék felszabadításhoz**: Válassza a **Sor hozzáadása** a korábban visszatartott összegek százalékértéknek megadásához a kiválasztott projektteljesítési szinthez.

> [!NOTE]
> Ha a projektek teljesítésének különböző szintjeihez több mérföldkő is tartozik, akkor minden egyes visszatartási szabályhoz adjon meg egy külön szállítói visszatartásifeltétel-sort. Mindegyik sor megadhat egy másik visszatartási százalékértéket és egy másik felszabadítási százalékértéket a projektek teljesítésének egyes meghatározott szintjeire vonatkozóan.

Miután létrehozta a szállítói visszatartási feltételeket egy szállítóhoz, a feltételeket egy projekthez alkalmazhatja.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Szállítói visszatartási feltételek alkalmazása egy projektre

1. Nyissa meg a **Projektmenedzsment és könyvelés** > **Projektek** > **Minden projekt** lehetőséget, és nyissa meg a projektet a projektlista lapról.
2. A **Szállítói megállapodások** gyorslapon jelölje be a **sor hozzáadása** jelölőnégyzetet.
3. Az **Partnerkód mezőben** válasszon a következő lehetőségek közül: 

   - **Táblázat**: A szállítói visszatartási feltételek egyetlen szállítóra vonatkoznak.
   - **Csoport** – a szállítói visszatartási feltételek a szállítói csoport minden szállítója esetében érvényesek.
   - **Összes**: A szállítói visszatartási feltételek az összes szállítóra vonatkoznak.

4. A **Szállító/szállítói csoport mezőben** válassza ki azt a szállítót vagy szállítói csoportot, amelyikre a szállítói visszatartási feltételek vonatkoznak. Ha az előző lépésben az **Összes** lehetőséget választotta, akkor ez a mező nem érhető el.
5. A **Szállítói visszatartási feltételek** mezőben jelölje ki az előző eljárásban létrehozott visszatartási feltételeket.
6. Ha a projekt a szállítóra vonatkozóan fizetéskor fizetett (PWP) feltételek is be vannak állítva, akkor adja meg a projekt küszöbértékét a **PWP-küszöb százalékértéke** mezőben.

A szállítóhoz létrehozott beszerzési megrendeléseken a szállítói visszatartási feltételek is megjelennek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]