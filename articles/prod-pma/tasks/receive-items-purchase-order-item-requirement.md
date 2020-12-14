---
title: Cikkek bevételezése a cikkszükségletből származó beszerzési rendelésen
description: Ez a témakör ismerteti, hogyan lehet cikkeket bevételezni egy cikkszükségletből származó beszerzési rendelésen.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078259"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Cikkek bevételezése a cikkszükségletből származó beszerzési rendelésen

[!include [banner](../../includes/banner.md)]

Ez a témakör ismerteti, hogyan lehet cikkeket bevételezni egy cikkszükségletből származó beszerzési rendelésen.

Cikktranzakció helyett egy cikkszükségletet használva megtervezheti a szállítást éppen a cikk tényleges felhasználása előtt, létrehozhat egy beszerzési rendelést, belefoglalhatja a cikket egy megállapodási keretrendszerbe, és belefoglalhatja a cikkszükségletet a gyártási tervezésbe. 

Ez a feladat a USSI adatkészletet használja.

1. Az ablaktáblában kattintson a **Modulok > Projektvezetés és könyvelés > Projektek > Minden projekt** lehetőségre.
2. A listában válassza ki a hivatkozást a kívánt sorban.
3. A Művelet panelen válassza a **Terv** elemet.
4. Válassza a **Cikkszükségletek** lehetőséget.
5. Válassza az **Új** lehetőséget.
6. Az új sorban adjon meg vagy jelöljön ki egy értéket a **Cikkszám** mezőben.
7. Írjon be egy számot a **Mennyiség** mezőbe.
8. Válassza a **Mentés** parancsot.
9. A Művelet panelen válassza a **Kezelés** elemet.
10. Válassza a **Funkciók** lehetőséget.
11. Válassza a **Megrendelés létrehozása** lehetőséget.
12. Kattintson az **Összes belefoglalása** jelölőnégyzetre.
13. Adjon meg vagy jelöljön ki egy értéket a **Partnerfiók** mezőben.
14. Kattintson az **OK** gombra.
15. A Navigáció ablaktáblán nyissa meg a következőt: **Modulok > Kötelezettségek > Megrendelések > Minden megrendelés**.
16. A listában válassza ki a hivatkozást a kívánt sorban.
17. A Művelet panelen válassza a **Beszerzés** elemet.
18. Válassza a **Megerősítés** elemet.
19. A Művelet panelen válassza a **Bevételezés** elemet.
20. Válassza a **Termékbizonylat** elemet.
21. A **Termékbizonylat** mezőbe írjon be egy értéket.
22. Kattintson az **OK** gombra.
