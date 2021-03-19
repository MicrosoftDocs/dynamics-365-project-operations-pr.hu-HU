---
title: A vállalatközi számlázás konfigurálása
description: Ez a témakör információkat és példákat tartalmaz a vállalatközi számlázás konfigurálásához a projektekhez.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2dec6669a41161a23f74ea962df6d8708b905315
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287556"
---
# <a name="configure-intercompany-invoicing"></a>A vállalatközi számlázás konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Hajtsa végre az alábbi lépéseket a vállalatközi számlázás beállításához a Dynamics 365 Project Operations alkalmazásban. A vállalatközi tranzakciók egy projektszerződésből származó idő-és költség-tranzakciók, amelyek egy vállalathoz vagy szervezeti egységhez tartoznak, miközben a projektszerződésben szereplő erőforrások egy másik vállalat vagy szervezeti egység részét képezik.

## <a name="example-configure-intercompany-invoicing"></a>Példa: A vállalatközi számlázás konfigurálása

A következő példában a Contoso Robotics USA (USPM) a kölcsönvevő jogi személy és a Contoso Robotics UK (GBPM) a kölcsönadó jogi személy. 

1. **A vállalatközi könyvelés konfigurálása a jogi személyek között**. A kölcsönadó és kölcsönvevő jogi személyek minden párját tagját be kell állítani a főkönyvi [vállalatközi könyvelés](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup) lapján.
    
    1. A Dynamics 365 Finance alkalmazásban válassza a **Főkönyv** > **Feladás beállításai** > **Vállalatközi könyvelés** lehetőséget. Hozzon létre egy rekordot a következő adatokkal:

        - **Eredeti vállalat** = **GBPM**
        - **Célvállalat** = **USPM**

2. **Adja meg a jogi személyek közötti kereskedési kapcsolatot**. A kölcsönvevő jogi személyt képviselő ügyfélrekordot a kölcsönadó jogi személyében kell létrehozni. A kölcsönadó jogi személyt képviselő szállítói rekordot a kölcsönvevő jogi személyében kell létrehozni.

     1. A Finance-ben válassza ki a jogi személyt: **GBPM**.
     2. Nyissa meg a **Kinnlevőségek** > **Ügyfél** > **Összes ügyfél** menüpontot. Hozzon létre egy új rekordot az **USPM** jogi személyhez.
     3. Bontsa ki a **Név** elemet, szűrje a rekordokat **Típus** szerint, és válassza a **Jogi személyek** lehetőséget. 
     4. Keresse meg és jelölje ki a **Contoso Robotics USA (USPM)** ügyfélrekordot.
     5. Válassza az **Egyezés használata** lehetőséget. 
     6. Jelölje ki az ügyfélcsoportot, majd mentse a rekordot.
     7. Válassza ki a **USPM** jogi személyt.
     8. Nyissa meg a **Kötelezettségek** > **Szállítók** > **Összes szállító** lehetőséget. Hozzon létre egy új rekordot az **GBPM** jogi személyhez.
     9. Bontsa ki a **Név** elemet, szűrje a rekordokat **Típus** szerint, és válassza a **Jogi személyek** lehetőséget. 
     10. Keresse meg és jelölje ki a **Contoso Robotics UK (GBPM)** ügyfélrekordot.
     11. Válassza az **Egyezés használata** lehetőséget , jelölje ki a szállítói csoportot, majd mentse a rekordot.
     12. A szállítói rekordban válassza az **Általános** > **Beállítás** > **Vállalatközi** lehetőséget.
     13. A **Kereskedelmi kapcsolat** lapon állítsa az **Aktív** beállítást **Igen** értékre.
     14. Válassza ki a **GBPM** szállító vállalatot, és a **Saját partnerrekordok** alatt jelölje ki az eljárásban korábban létrehozott ügyfélrekordot.

3. **Konfigurálja a vállalatközi beállításokat a Projektvezetés és könyvelés paraméterekben**. 

    1. Válassza ki a **USPM** jogi személyt, és nyissa meg a **Projektvezetés és könyvelés** > **Beállítások** > **Projektvezetés és könyvelés paraméterei** lehetőséget.
    2. A **Vállalatközi** lapon jelölje ki a beszerzési kategóriát, hogy megfeleltesse az automatikusan generált szállítói számlákat.
    3. Válassza az **Alapértelmezett kategória** alatt a **Vállalatközi erőforrások** lehetőséget.
    4. Válassza ki a **GBPM** jogi személyt, és nyissa meg a **Projektvezetés és könyvelés** > **Beállítások** > **Projektvezetés és könyvelés paraméterei** lehetőséget.
    5. A **Vállalatközi** lapon jelöljön ki egy alapértelmezett projektkategóriát minden tranzakciótípus esetében. A rendszer akkor használja a projektkategóriákat az adó konfigurációjára, ha a vállalatközi tranzakciókban kiszámlázott kategóriák csak a kölcsönbe vevő jogi személy lehetőségben léteznek. Választhatja a bevétel elhatárolását is a vállalatközi tranzakciókra vonatkozóan. Az elhatárolás akkor történik meg, amikor a tranzakciókat feladják a Project Operations integrációs naplójával a kölcsönadó jogi személynél. A rendszer a vállalatközi számla feladásakor sztornózza a naplót.
    6. Az **Erőforrások kölcsönzésekor** csoportban válassza a **...** > **Új** lehetőséget. 
    7. A rácson válassza ki az alábbi információkat.

          - **Kölcsönvevő jogi személy** = **GBPM**
          - **Bevétel elhatárolása** = **Igen**
          - **Alapértelmezett munkaidő-nyilvántartási kategória** = **Alapértelmezett – óra**
          - **Alapértelmezett költségkategória** = **Alapértelmezett – költség**

4. **A vállalatközi költség-és bevételi számlák beállítása a Főkönyvi feladás beállítása során**. A vállalatközi bevételi számla akkor kerül jóváírásra, amikor a vállalatközi ügyfél számlát feladják a kölcsönadó jogi entitásnak. A vállalatközi költségszámla akkor lesz terhelve, amikor az egyező függőben lévő szállítói számlát feladják a kölcsövevő jogi entitásnak. Ezek a számlák a megfelelő jogi személyekben állíthatók be. 
      
     1. A Finance-ben válassza ki a kölcsönvevő jogi személyt: **USPM**. 
     2. Nyissa meg a **Projektvezetés és könyvelés** > **Beállítások** > **Feladás** > **Főkönyvi feladás- beállítása** lehetőséget. 
     3. A **Költségszámlák** lap **Főkönyvi számla típusa** mezőjében válassza a **Vállalatközi költség** lehetőséget. Hozzon létre egy új rekordot a következő adatokkal:
      
        - **Kölcsönadó jogi személy** = **GBPM**
        - **Főszámla** = Válassza ki a fő számlát a vállalatközi költséghez
        
     4. Válassza ki a **GBPM** kölcsönadó jogi személyt. 
     5. Nyissa meg a **Projektvezetés és könyvelés** > **Beállítások** > **Feladás** > **Főkönyvi feladás- beállítása** lehetőséget. 
     6. A **Bevételi számlák** lap **Főkönyvi számla típusa** mezőjében válassza a **Vállalatközi bevétel** lehetőséget. Hozzon létre egy új rekordot a következő adatokkal:

        - **Kölcsönvevő jogi személy** = **USPM**
        - **Főszámla** = Válassza ki a fő számlát a vállalatközi bevételhez 

5. **A munkaerőhöz tartozó transzferár beállítása**. A vállalatközi transzferár konfigurálása a Project Operations alkalmazásban történik a Dataverse-ben. A [munkadíjak](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) és [munkaerő számlázási árak](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) konfigurálása vállalatközi számlázáshoz. A transzferár nem támogatott a vállalatközi költségtranzakciók esetében. A vállalatközi eladási ár mindig ugyanarra az értékre lesz beállítva, mint a beszerzési egységár.

      A Contoso Robotics UK vállalatnál a fejlesztői erőforrás ára 88 font/óra. A Contoso Robotics UK a Contoso Robotics USA felé120 dollárt számláz minden óráért amit az erőforrás az amerikai projekteken dolgozott. A Contoso Robotics USA az Adventure Works ügyfélnek 200 dollárt számláz a Contoso Robotics UK fejlesztői erőforrása által végzett munkáért.

      1. A Dataverse Project Operations alkalmazásban válassza az **Értékesítés** > **Árlisták** lehetőséget. Hozzon létre egy új önköltségi árlistát a **Contoso Robotics UK önköltségi árak** néven. 
      2. Hozzon létre egy rekordot az önköltségi árlistában, amely a következő információkat tartalmazza:
         - **Szerepkör** = **Fejlesztő**
         - **Költség** = **88 GBP**
      3. Nyissa meg a **Beállítások** > **Szervezeti egységek** elemet, és csatolja ezt az önköltségi árlistát a **Contoso Robotics UK** szervezeti egységhez.
      4. Válassza az **Értékesítés** > **Árlisták** lehetőséget. Hozzon létre egy önköltségi árlistát a **Contoso Robotics USA önköltségi árak** néven. 
      5. Hozzon létre egy rekordot az önköltségi árlistában, amely a következő információkat tartalmazza:
          - **Szerepkör** = **Fejlesztő**
          - **Erőforrás vállalat** = **Contoso Robotics UK**
          - **Költség** = **120 USD**
      6. Nyissa meg a **Beállítások** > **Szervezeti egységek** elemet, és csatolja a **Contoso Robotics USA önköltségi árak** önköltségi árlistát a **Contoso Robotics USA** szervezeti egységhez.
      7. Válassza az **Értékesítés** > **Árlisták** lehetőséget. Hozzon létre egy értékesítési árlistát **Adventure Works számlázási árak** néven. 
      8. Hozzon létre egy rekordot az értékesítési árlistában, amely a következő információkat tartalmazza:
          - **Szerepkör** = **Fejlesztő**
          - **Erőforrás vállalat** = **Contoso Robotics UK**
          - **Számlázási ár** = **200 dollár**
      9. Nyissa meg a **Sales** > **Projektszerződések** lehetőséget és csatolja az **Adventure Works számlázási árak** a projektszerződés Adventure Works projektárlistájához.


[!INCLUDE[footer-include](../includes/footer-banner.md)]