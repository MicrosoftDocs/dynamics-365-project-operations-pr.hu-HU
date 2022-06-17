---
title: Termékalapú árajánlatsorok áttekintése - Lite
description: Ez a cikk a termékalapú árajánlatsorok használatáról nyújt tájékoztatást.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: db0700e789202a8fdd0ef3b49959421ac54fb9ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914313"
---
# <a name="product-based-quote-lines-overview---lite"></a>Termékalapú árajánlatsorok áttekintése - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations szolgáltatásban termékalapú árajánlatsorokat hozhat létre. A termékalapú árajánlatsorok lehetnek manuálisan megadott vagy a termékkatalógusban szereplő elemek.

## <a name="product-catalog"></a>Termékkatalógus

A termékkatalógusban szereplő egyes termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek. Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal. 

Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre. Az összes előfizetési szoftver a következő két attribútummal rendelkezik:

- Felhasználók száma
- Az előfizetés időtartama hónapokban van megadva

Az ilyen típusú katalógus fenntartásához hozzon létre egy **Előfizetési szoftver** nevű termékcsaládot, és adja hozzá a felhasználók számát és az előfizetés időtartamát attribútumként. Következő lépésként egyéni termékeket adhat hozzá az **Előfizetési szoftver** termékcsaládhoz.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Termékkatalógus-elemek hozzáadása a projektárajánlathoz

A **projektárajánlat** és a **projektszerződés** oldalak tartalmaznak szakaszokat a projektalapú sorokhoz és termékalapú sorokhoz. A termékalapú soroknál az árajánlatsorban vagy a projektszerződés-sorban lévő legördülő lista tartalmazza az összes terméket és egységet a termék árlistájában. Olyan termékeket is hozzáadhat, amelyek nem képezik részét a termékárlistának.

Ezen felül kiválaszthat termékeket más árlistákból, vagy közvetlenül a termékkatalógusból. Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához. Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.

Ha az árajánlatsor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül az árajánlatsoron bírálhatja felül. Az árajánlat sora az **Árképzés** mezőben két használható értékkel:

- **Árképzés felülbírálása**
- **Alapértelmezett használata**

Ha az **Árképzés felülbírálása** lehetőséget választja, akkor az alapértelmezett ár nincs beállítva. Ehelyett az árajánlatsorba kell beírnia a termék árát. Ha az **alapértelmezett használata** lehetőséget választja, akkor az alapértelmezett értékesítési árat használja a program, és a mező szerkesztésre zárolva van.

Az alapértelmezett eladási árak az árajánlat termékalapú soraiba kerülnek be. Az **Árképzés** mező ezután **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat az árajánlatsorokon szerkeszthesse. Ez egy olyan Project Operations-specifikus felülbírálás, amely a terméken alapuló sorok viselkedését a Dynamics 365 Salesben felülbírálja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]