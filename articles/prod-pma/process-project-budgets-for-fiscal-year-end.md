---
title: A projektek költségvetésének átadása pénzügyi év végén
description: A cikk azt ismerteti, hogy miként lehet áthelyezni a fennmaradó költségvetési összegeket a következő évekre, és létrehozni a költségvetés-nyilvántartási adatokat.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008044"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>A projektek költségvetésének átadása pénzügyi év végén

[!include [banner](../includes/banner.md)]

A többéves projektek használatakor előfordulhat, hogy a pénzügyi év végén megmarad a költségvetés. A fennmaradó költségvetési összegeket átviheti egy jövőbeli évre, és költségvetési tételjegyzéket hozhat létre a kapcsolódó főkönyvi számlákban szereplő összegekre vonatkozóan. Mielőtt átviszi a fennmaradó összegeket, tekintse át és elemezze a többi költségvetési összeget.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Fennmaradó költségvetési összegek áttekintése és elemzése

A következő lépések végrehajtásával tekintheti meg a projektek év végi költségvetési összegeit, de nem viheti át az összegeket.

1. Lépjen a **Projektvezetés és könyvelés** > **Időszakos** > **Költségvetések** > **Költségvetések továbbvitele** elemre. 
2. A **projekt költségvetés átvitelének folyamata** lapon az **év végi beállítások** lapon ellenőrizze, hogy nincs-e engedélyezve az **megmaradt projekt-költségvetési összegek átvitele**.
3. A **paraméterek** lap **projektköltségvetési év** mezőjében válassza ki azt a pénzügyi év, amelynek meg szeretné tekinteni a fennmaradó költségvetési összegét. 
4. A **Nyitó pénzügyi év** mezőben válassza ki azt a pénzügyi év, amelynek meg szeretné tekinteni a fennmaradó költségvetési összegét. 
5. A **Forrás előrejelzési modell** mezőben válassza ki a **fennmaradó költségvetés** elemet. 
6. Ha olyan projekteket szeretne szerepeltetni, amelyek megfelelnek a kiválasztott feltételeknek, és nincs fennmaradó költségvetése, akkor jelölje be a **Nulla fennmaradó érték megjelenítése** elemet.  
7. A **költségvetés kiválasztása** lapon válassza az **összes költségvetés lekérése** lehetőséget a kiválasztott feltételeknek megfelelő összes költségvetés betöltéséhez, majd válassza a **Feldolgozás** lehetőséget. 
8. Ha olyan adatbázis-lekérdezést szeretne tervezni, amely egy adott költségvetés-készletet betölt az ablaktáblába, válassza a **kijelölt költségvetések lekérése** lehetőséget.

Ha további tájékoztatást szeretne az ablaktáblában egy adott sorhoz, jelölje ki a sort, majd válassza a **költségvetés részleteinek megtekintése** vagy a **partnerek megtekintése** lehetőséget.

## <a name="carry-forward-remaining-budget-amounts"></a>A fennmaradó költségvetési összegek átvitele 

A fennmaradó költségvetési összegek feldolgozása során a főkönyvben hozhat létre tranzakciókat az összegekhez, amelyeket átvisz. A főkönyvi tranzakciók létrehozásához hajtsa végre a [Költségvetési összegek továbbvitele és főkönyvi tranzakciók létrehozása](#carry-forward) szakasz lépéseit. 

> [!NOTE]
> Az átvitt költségvetési összegek átkerülnek az előrejelzési modellbe, amelyek az **Előrejelzési modellek** lapon kiválasztott a továbbítási előrejelzési modellként.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Költségvetési összegek továbbvitele és főkönyvi tranzakciók létrehozása

1.  Válassza a **Projektvezetés és könyvelés** > **Időszakos** > **Költségvetések** > **Költségvetések továbbvitele** elemet. 
2. A **projektköltségvetés átviteli folyamata** lapon jelölje ki az **év végi** beállítást, majd engedélyezze a **Fennmaradó projektköltségvetési összegek átvitele** valamint a **Költségvetés tételjegyzék-tételek létrehozását a főkönyvi könyvelésben** lehetőséget. 
3. A **Paraméterek** lapon, a **Projektparaméterek** mezőcsoportban válassza a következőt:

   - A **Projektköltségvetési év**: válassza ki azt a pénzügyi év kezdetét, amelynek meg szeretné tekinteni a fennmaradó költségvetési összegeit. 
   - **Nyereség és veszteség**: Eredménytranzakciók létrehozása a főkönyvi könyvelésben. 
   -  **Befejezetlen termelés**: Befejezetlen termelési (WIP) tranzakciók létrehozása a főkönyvi könyvelésben.
   -  **Bérelszámolása**: Bérelszámolás-felosztási tranzakciók létrehozása a főkönyvi naplóban. 

5. Az **Főkönyv** mezőcsoportban adja meg a következő adatokat: 

   - A **Nyitó pénzügyi év** mezőben válassza ki azt a pénzügyi év, amelynek át szeretné vinni a projektekhez fennmaradó költségvetési összegét. Az alapértelmezett érték egy évvel a **projekt költségvetési év** mezőjében szereplő érték után történik.
   -  A **továbbítási időszak** mezőben jelölje ki azt az időszakot, ameddig a főkönyvi könyvelésben a költségvetés tételjegyzék adatait létre szeretné hozni. Ez általában a nyitó pénzügyi év első időszaka.

6. Az **Másolás innen/ide** mezőcsoportban adja meg a következő adatokat:

   - Az **Forrás előrejelzési modell** mezőjében válassza ki a projektekhez átvinni kívánt fennmaradó költségvetési összeghez kapcsolódó projekt-előrejelzési modellt. 
   - Az **Cél előrejelzési modell** mezőjében válassza ki a főkönyvbe átvinni kívánt költségvetési összeghez kapcsolódó főkönyvi költségvetési modellt. 
   -  Válassza az **Értékesítési pénznem átvitele** lehetőséget, ha a projekt értékesítési pénznemét szeretné használni a projektek költségvetési összegének átadásakor létrehozott főkönyvi tranzakciókhoz. Ha a lehetőség nincs bejelölve, akkor a tranzakciók a számlázási pénznemet használják. 
   -  Jelölje be a **Nulla fennmaradó érték megjelenítése** jelölőnégyzetet, ha meg szeretné jeleníteni a fennmaradó költségvetési összegeket nem tartalmazó projekteket, amelyek teljesítik az alsó ablaktáblában megjelenő projektekben kiválasztott egyéb feltételeket.

7. A **költségvetés kiválasztása** lapon válassza az **összes költségvetés lekérése** lehetőséget a kiválasztott feltételeknek megfelelő összes költségvetés betöltéséhez. Ha olyan adatbázis-lekérdezést szeretne tervezni, amely egy adott projektköltségvetés-készletet betölt az ablaktáblába, válassza a **kijelölt költségvetések lekérése** lehetőséget.
8. A feldolgozni kívánt projektek mindegyikéhez jelölje ki a beállítást a projekt első sorában.

    > [!TIP]
    > Az összes vagy a legtöbb projekt kijelöléséhez jelölje be a bal felső sarokban lévő jelölőnégyzetet. Bizonyos projektek feldolgozásának kizárásához törölje a jelet a projekt bejelöléséről.

9. Ha a kijelölt projektek fennmaradó költségvetési összegeit át szeretné helyezni a kijelölt pénzügyi évre, és a főkönyvbe költségvetési tételjegyzéket szeretne létrehozni, akkor jelölje be a **folyamat** elemet.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Költségvetési összegek továbbvitele főkönyvi tranzakciók létrehozása nélkül

1. Lépjen a **Projektvezetés és könyvelés** > **Időszakos** > **Költségvetések** > **Költségvetések továbbvitele** elemre.
2. A **projekt költségvetés átvitelének folyamata** lapon az **év végi beállítások** mezőben válassza a **fennmaradó projekt-költségvetési összegek átvitele** elemet.
3. A **paraméterek** csoportban, a **projektköltségvetési év** mezőjében válassza ki azt a pénzügyi év, amelynek meg szeretné tekinteni a fennmaradó költségvetési összegét.
4. Az **Másolás innen/ide** csoportban adja meg a következő adatokat:

   - Az **Forrás előrejelzési modell** mezőjében válassza ki a projektekhez átvinni kívánt fennmaradó költségvetési összeghez kapcsolódó projekt-előrejelzési modellt. 
   - Jelölje be a **Nulla fennmaradó érték megjelenítése** elemet, ha olyan projekteket szeretne szerepeltetni, amelyek megfelelnek a kiválasztott feltételeknek, és nincs fennmaradó költségvetése.
   - A **költségvetés kiválasztása** csoportban válassza az **összes költségvetés lekérése** lehetőséget a kiválasztott feltételeknek megfelelő összes költségvetés betöltéséhez. Ha olyan adatbázis-lekérdezést szeretne tervezni, amely egy adott projektköltségvetés-készletet betölt az ablaktáblába, válassza a **kijelölt költségvetések lekérése** lehetőséget.

5. A feldolgozni kívánt projektek mindegyikéhez jelölje ki a beállítást a projekt első sorában. 
6. Válassza a **folyamat** lehetőséget a fennmaradó költségvetési összegek átadásához a kijelölt projekteknél a kijelölt pénzügyi évre.



[!INCLUDE[footer-include](../includes/footer-banner.md)]