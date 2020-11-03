---
title: Termékalapú szerződéssorok áttekintése
description: Ez a témakör információkat nyújt a termékalapú szerződéssorokról.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078019"
---
# <a name="product-based-contract-lines-overview"></a>Termékalapú szerződéssorok áttekintése

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A Dynamics 365 Project Operations alkalmazásban a termékalapú szerződéssorokat hozhat létre. A termékalapú szerződéssorok lehetnek manuálisan létrehozott sorok vagy a termékkatalógusban szereplő elemek.

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
