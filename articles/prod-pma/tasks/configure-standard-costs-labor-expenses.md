---
title: A munkaerő és a kiadások elszámolóárainak konfigurálása
description: Ez a témakör azt mutatja be, hogyan állíthatók be a munkaerő és a kiadások elszámolóárai egy projekten belül.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011014"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>A munkaerő és a kiadások elszámolóárainak konfigurálása

[!include [banner](../../includes/banner.md)]

Ez a témakör azt mutatja be, hogyan állíthatók be a munkaerő és a kiadások elszámolóárai egy projekten belül. Ez a feladat a USSI adatkészletet használja.

1. Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Önköltségi ár (óra)** lehetőségre.
2. Válassza az **Új** lehetőséget.
3. Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.
4. Írjon be egy számot az **Önköltségi ár** mezőbe. Itt beállíthat egy elszámolóárat az adott projektkategóriához, illetve beállíthat önköltségi árat a munkavállalók száma, a projektszám, a kategória, a dátum vagy ezek tetszőleges kombinációja alapján. Az alkalmazott önköltségi ár a legrészletesebb szintű önköltségi ár.  
5. Válassza a **Mentés** parancsot.
6. Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Eladási ár (óra)** lehetőségre.
7. Válassza az **Új** lehetőséget.
8. Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.
9. Válasszon az **Érvényes** mezőben lévő lehetőségek közül.
10. Írjon be egy számot az **Árképzés** mezőbe. Itt beállíthat egy szabványos eladási árat az óratranzakciókhoz vagy a projektkategóriákhoz. Emellett az eladási árakat a munkavállalók száma, a projektszám, a kategória, a tranzakció dátuma vagy ezek bármilyen kombinációja szerint is megadhatja. A tényleges eladási ár, amelyet a rendszer akkor alkalmaz, amikor egy munkavállaló tranzakciót ad meg az óranaplóban, a legrészletesebb szintű eladási ár. Ha például egy általános eladási ár és egy munkavállaló-specifikus értékesítési ár is be van állítva, akkor a rendszer a munkavállaló-specifikus értékesítési árat használja.  
11. Válassza a **Mentés** parancsot.
12. Zárja be a lapot.
13. Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Önköltségi ár (kiadás)** lehetőségre.
14. Válassza az **Új** lehetőséget.
15. Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.
16. Írjon be egy számot az **Önköltségi ár** mezőbe. Több mező is kitölthető, de legalább ennyi szükséges a rekord mentéséhez.  
17. Válassza a **Mentés** parancsot.
18. Az ablaktáblán kattintson a **Modulok > Projektvezetés és könyvelés > Beállítás > Árak > Eladási ár (kiadás)** lehetőségre.
19. Válassza az **Új** lehetőséget.
20. Írjon be egy dátumot az **Érvényesség dátuma** mezőbe.
21. Válasszon az **Érvényes** mezőben lévő lehetőségek közül.
22. Írjon be egy számot az **Árképzés** mezőbe. A tényleges eladási ár, amelyet akkor alkalmaz a rendszer, amikor egy munkavállaló tranzakciókat ad meg egy Költségnaplóban, a legrészletesebb szintű eladási ár. Ha például egy általános és egy munkavállaló-specifikus értékesítési ár is be van állítva, akkor a rendszer a munkavállaló-specifikus értékesítési árat használja.  
23. Válassza a **Mentés** parancsot.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]