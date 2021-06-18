---
title: Termékalapú szerződéssorok áttekintése - Lite
description: Ez a témakör információkat nyújt a termékalapú szerződéssorokról.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994544"
---
# <a name="product-based-contract-lines-overview---lite"></a>Termékalapú szerződéssorok áttekintése - Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations szolgáltatásban termékalapú szerződéssorokat hozhat létre. A termékalapú szerződéssorok lehetnek manuálisan létrehozott sorok vagy a termékkatalógusban szereplő elemek.

## <a name="product-catalog"></a>Termékkatalógus

A termékkatalógusban szereplő termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek. Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal. Egy termékcsalád összes terméke ugyanazt az attribútumkészletet örökli.

Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre. Az összes előfizetési szoftver a következő két attribútummal rendelkezik:

- Felhasználók száma
- Előfizetés időtartama (hónapokban)

Az ilyen típusú katalógus karbantartásához hozzon létre egy **előfizetési szoftver** nevű termékcsaládot. Adja hozzá az attribútumokat, a **felhasználók számát** és az **előfizetési időtartamot** a termékcsalád számára. Ezután vegye fel az egyes termékeket az **előfizetői szoftver** termékcsaládba.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Termékkatalógus-elemek hozzáadása a projektszerződéshez

A projektszerződések kétféle sort tartalmaznak: projektalapú sorok és termékalapú sorok. A terméken alapuló sorok tartalmazzák az összes terméket és egységet a szerződéshez tartozó termékárlistán. Olyan termékeket is hozzáadhat, amelyek nem képezik részét a szerződés termékárlistájának.

A termékeket más árlistákből, vagy közvetlenül a termékkatalógusból is kijelölheti. Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához. Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.

Ha a szerződéssor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül a soron bírálhatja felül. A szerződéssoron szerepel az **Árképzés** mező két értékkel:

- **Árképzés felülbírálása**
- **Alapértelmezett használata**

Ha az **Árképzés** mezőt az **Árképzés felülbírálása** értékre állítja, nem állít be alapértelmezett árat. Adja meg a szerződéssor termékének árát. Ha a mezőt **Alapértelmezett érték használata** értékre állítja, akkor a rendszer az alapértelmezett értékesítési árat használja, és a mező nem szerkeszthető.

A Project Operations telepítése után az alapértelmezett eladási árak a szerződés termékalapú soraiba kerülnek be. Az **Árképzés** mező **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat a szerződéssorokon szerkeszthesse. Ez a Project Operations-specifikus felülbírálás a termék alapú sorok működésénál a Dynamics 365 Sales alkalmazásban.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]