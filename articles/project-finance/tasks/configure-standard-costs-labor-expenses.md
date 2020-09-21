---
title: A munkaerő és a kiadások elszámolóárainak konfigurálása
description: Ez a témakör azt mutatja be, hogyan állíthatók be a munkaerő és a kiadások elszámolóárai egy projekten belül.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752317"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>A munkaerő és a kiadások elszámolóárainak konfigurálása

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

