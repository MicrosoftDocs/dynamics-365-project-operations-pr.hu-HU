---
title: Költségrészletezés
description: Ez a cikk azt mutatja be, hogyan lehet a kiadásokat tételezni használni az újragondolt Költség munkaterület használatával.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920937"
---
# <a name="expense-itemization"></a>Költségrészletezés

[!include [banner](../includes/banner.md)]

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A szervezetek gyakran megkövetelik, hogy az alkalmazottak részletesen tételezzék az utazás során felmerülő költségeket. Egy hotel nyugtája több tételsornyi elemet is tartalmazhat a szobaárra, az adóra, a parkolásra, valamint az egyéb a tartózkodás napjain felmerülő költségekre. Az is előfordulhat, hogy egy étkezéssel kapcsolatos kiadásbál részletesebb tételezést kell benyújtani a reggelihez, ebédhez vagy vacsorához. Az egyes költségkategóriák a szervezet igényeitől függetlenül beállíthatók úgy, hogy tükrözzék az alkategóriákat vagy a kiadást kitevő tételsorokat. Ugyan a **Költségkezelésben** mindig is támogatott volt a tételezés az **Újragondolt költségek** munkaterület hatékonyabb tételezési lehetőséget biztosít, ha engedélyezve a **Képesség az ismétlődő költségek gyors tételezésére** funkció.  

## <a name="enable-quick-itemization"></a>A gyors tételezé engedélyezése 

A **Képesség az ismétlődő költségek gyors tételezésére** funkció használatával gyorsan tételezheti az ismétlődő kiadásokat, úgy hogy nem kell minden alkalommal a napi kiadásokat beírni a tartózkodás időtartamára. A gyors tételezés engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. Látogasson el a **Funkciókezelés** munkaterületre, és a funkciók listájában keresse meg és válassza ki az **Újragondolt költségjelentések** lehetőséget. 
2. Válassza ki az **Engedélyezés most** lehetőséget. 
3. Keresse meg és jelölje ki a szolgáltatáslistában a **Képesség az ismétlődő költségek gyors tételezésére** lehetőséget .
4. Válassza ki az **Engedélyezés most** lehetőséget. 

## <a name="itemization-grid"></a>Tételezési rács 

Ha egy költségkategóriához alkategóriák vagy különböző összetevők tartoznak, amelyekből az adott költség összeáll, akkor ezeket tételezni lehet. Egy költség tételezéséhez jelölje ki a költségsort a költségjelentésben, és a **Költség részletei** ablaktáblában válassza a **Műveletek** > **Tételezés** elemet. A **Tételezés** csúszka egy mezőket tartalmazó rácsot fed fel. Az alábbi táblázatban egy-egy példa látható a rács egyes mezőire, illetve arra, hogy ez a mező hogyan van a költségjelentésben megjelenítve. 

|     Mező          |     Description                                                                                  |     Példa              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alkategória    |     A **Hotel** típsuú költségkategóriák alatt konfigurált alkategóriák listája.             |     Napi szobaár      |
|     Kezdési dátum     |     A költségtétel első felmerülésének dátuma.                                           |     2021/09/13           |
|     Napi díj     |     A költségelemhez kapcsolódó összeg.                                                    |     200                  |
|     Mennyiség       |     Hány alkalommal ismétlődik a díj egy folyamatos időszakban.                       |     3                    |

![Költség tételezése.](media/Itemization%20screen%201.png)

Amikor elmenti a tételezést, egy különálló tételezett sor jelenik meg a Tételezési rácsban megadott mennyiséghez. Minden egyes sor a rácsban megadott dátumon kezdődik.

![Tételezett jelentés.](media/Itemization%20screen%202.png)

