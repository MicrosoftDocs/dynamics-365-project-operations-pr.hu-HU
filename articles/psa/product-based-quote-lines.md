---
title: Termékalapú árajánlatsorok
description: Ez a témakör információkat nyújt a termékalapú árajánlatsorokról.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 3cc2e8788ea699b57ef75903ec3771f2e66fe867a9b8b6328a55b484eb13ede4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008589"
---
# <a name="product-based-quote-lines"></a>Termékalapú árajánlatsorok

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


A Dynamics 365 Project Service Automation szolgáltatásban termékalapú árajánlatsorokat hozhat létre. A termékalapú árajánlatsorok lehetnek „beírási” sorok vagy a termékkatalógusban szereplő elemek.

## <a name="product-catalog"></a>Termékkatalógus

A Dynamics 365 termékkatalógusban szereplő termékek alapértelmezett egységgel és egységcsoporttal rendelkeznek. Ha több termék ugyanazon attribútumkészlettel rendelkezik, akkor létrehozhat egy termékcsaládot, amely szintén rendelkezik ezekkel az attribútumokkal. Egy termékcsalád összes terméke ugyanazt az attribútumkészletet örökli.

Például egy vállalat előfizetési licenceket értékesít különféle szoftverekre. Az összes előfizetési szoftver a következő két attribútummal rendelkezik:

- Felhasználók száma 
- Előfizetés időtartama (hónapokban)

Az ilyen típusú katalógus fenntartásának megfelelő módja egy termékcsalád létrehozása, amelynek neve **Előfizetési szoftver**, és amely rendelkezik **Felhasználók száma** és **Előfizetés időtartama** attribútumokkal. Ezután különálló termékeket, például a **Dynamics 365 Sales** szolgáltatást vagy a **Dynamics 365 Field Service** szolgáltatást hozzáadhatja az **Előfizetési szoftver** termékcsaládhoz.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Termékkatalógus-elemek hozzáadása a projektárajánlathoz

A projektárajánlat és a projektszerződés oldalak kétféle sort tartalmaznak: projektalapú sorok és termékalapú sorok. Termékalapú sorok esetén a Dynamics 365 használatával elemeket adhat hozzá termékkatalógusból egy árajánlathoz. Az árajánlatsorban vagy a projektszerződés-sorban lévő legördülő lista tartalmazza az összes terméket és egységet a termék árlistájában, amelyet csatolt az árajánlathoz vagy a projektszerződéshez. Olyan termékeket is hozzáadhat, amelyek nem képezik részét az árajánlat termékárlistájának.

Ezen felül kiválaszthat termékeket más árlistákból, vagy közvetlenül a termékkatalógusból is kiválaszthatja a termékeket. Ha közvetlenül termékkatalógusból választja ki a termékeket, akkor az adott termék alapértelmezett árlistáját kell használnia a termék értékesítési árának meghatározásához. Ha nincs megadva alapértelmezett árlista, akkor az ár 0 (nulla) értékre lesz állítva.

Ha az árajánlatsor egy termékkatalóguson alapul, akkor az értékesítési árat közvetlenül az árajánlatsoron bírálhatja felül. Vegye figyelembe, hogy a Dynamics 365 árajánlatsora rendelkezik **Árképzés** mezővel. Két érték áll rendelkezésre:

- Árképzés felülbírálása  
- Alapértelmezett használata

Ha ezt a mezőt **Árképzés felülbírálása** értékre állítja, a Dynamics 365 nem állít be alapértelmezett árat. Az árajánlatsorba kell beírnia a termék árát. Ha ezt a mezőt **Alapértelmezett használata** értékre állítja, akkor a Dynamics 365 az alapértelmezett értékesítési árat használja, és bezárja a mezőt a szerkesztés megakadályozása érdekében.

A PSA telepítése után az alapértelmezett eladási árak az árajánlat termékalapú soraiba kerülnek be. Az **Árképzés** mező ezután **Árképzés felülbírálása** értékre lesz állítva, hogy az alapértelmezett árat az árajánlatsorokon szerkeszthesse.

> ![Árképzés felülbírálásának beállítása.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>A termékek mennyiségi tényezői

A PSA mennyiségi tényezőket alkalmaz az előfizetésen alapuló termékek értékesítésének támogatására. Az előfizetésen alapuló termékek esetében az árajánlat vagy a projektszerződés sorában szereplő mennyiséget a felhasználói/hónap számában fejezik ki.

Az előfizetési szoftver ára általában a katalógusban kerül tárolásra havi felhasználónkénti árként. Ehelyett más időleírásokat is használhat. Az értékesítési folyamat során az árajánlatsorban a felhasználónkénti havi ár általában az IT-értékesítési ügynökkel való egyeztetés után és az általa megadott árengedménnyel születik meg. Minden egyes ügyletnek eltérő felhasználói száma és előfizetési hónapjai vannak. Az árajánlatsor összegének kiszámításához használt mennyiség a felhasználók számának és az előfizetési hónapoknak a szorzata.

Az ilyen típusú értékesítés támogatása érdekében a PSA bevezette a mennyiségi tényezők fogalmát. A mennyiségi tényezők a Dynamics 365 termékattribútumaira támaszkodnak. Amikor egy adott termék tulajdonságait konfigurálja, a PSA lehetővé teszi, hogy mennyiségi tényezőként jelölje meg ezen tulajdonságok egy részhalmazát vagy az összes tulajdonságot.

A PSA ügyel rá, hogy csak a numerikus vagy a numerikus adattípusú termékjellemzők kerülhessenek megjelölésre mennyiségi tényezőként. Ha egy termék, amelynek mennyiségi tényezőit konfigurálják, hozzáadásra kerül egy árajánlatsorhoz, az árajánlatsor **Mennyiség** mezője „csak olvasható” mező lesz. Miután megadta a terméktulajdonságok értékeit, amelyek mennyiségi tényezők, a PSA kiszámítja az árajánlatsor mennyiségét.

Például a Dynamics 365 a következő tulajdonságokkal rendelkezik: 

- **Felhasználók száma** – a felhasználók száma 
- **Hónapok száma** – az előfizetési hónapok száma
- **Termék cikkszáma** 

A **Felhasználók száma** és a **Hónapok száma** tulajdonságok megjelölhetők mennyiségi tényezőként a terméksor tulajdonságainak szerkesztésével. 

> ![A felhasználók számának és a hónapok számának megjelölése minőségi tényezőként.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]