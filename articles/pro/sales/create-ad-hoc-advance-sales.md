---
title: Alkalmi előleg létrehozása szerződésen – Lite
description: Ez a témakör a szerződéshez igény szerinti előleg létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181365"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Alkalmi előleg létrehozása szerződésen – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Microsoft Dynamics 365 Project Operations támogatja az előre fizetést és előlegeket tartalmazó számlázási helyzeteket. A **Project Operations** alkalmazásban az **Előlegek** használatának folyamata hasonló a **Foglalóhoz** a szerződéseknél. 

A következő lépések végrehajtásával számlázhat az ügyfélnek előleget.

1. Nyissa meg a **Projektszerződés** lapot, majd jelölje ki az **Előlegek és foglalók** lapot.
2. Az összes előzőleg felvett előleget és előrefizetést felsoroló alrácsban válassza az **+ új projektszerződés-foglaló elemet**. 

    Megnyílik a **Gyorslétrehozás** űrlap az előrefizetés vagy előleg rögzítése céljából.
    
3. Az alábbi táblázat felsorolja az előleg rögzítéséhez szükséges mezőket és azokat a szempontokat, amelyeket az újak létrehozásakor figyelembe kell venni:

    | Mező | Adatfolyam leírása | Alsóbb rétegbeli hatás |
    | --- | --- | --- |
    | **Projektszerződés ügyfele** | Ez a mező jelzi azt az ügyfelet akinek ezt a foglalót vagy előleget kiszámlázzák. | Ha a szerződés több ügyfelet tartalmaz, és ha mindegyiküknek ki szeretné számlázni egy adott foglaló vagy előleg összegét, akkor minden ügyfélhez külön hozzon létre előleget. |
    | **Leírás** | Az előleg céljának vagy időzítésének leírása, amely segítséget nyújt az előleg azonosításában. | Ez a leírás jelenik meg az előleghez számlasorban. |
    | **Összeg** | Az előrefizetés vagy az előleg összege. | Ez az összeg jelenik meg az előleghez számlasorban. |
    | **Számla kelte** | Az előlegnek az ügyfélnek való számlázásának dátuma. | Ez a dátum az automatizált számlalétrehozási folyamathoz tartozik egy számlasor létrehozásához ehhez az előleghez. |
    | **Számla állapota** | Ez egy opcióbeállítás, amely azt jelzi, hogy az előleg hozzáadódik-e az ügyfélre vonatkozó számlavázlathoz. A lehetséges értékek:</br>- **Nem kész a számlázásra**</br>- **Kész a számlázásra** | Ha egy előleget vagy előfizetést **Számlázásra készként** jelölnek meg, akkor a program a számlavázlathoz egy soridőpontként adja hozzá a számlát. A következő számlázási időszakra vonatkozóan csak egy teljesen számlázott előleg használható a projekt költségeivel szembeni egyeztetésére. |

4. Az előleg vagy az előrefizetés rögzítéséhez válassza a **Mentés és bezárás** lehetőséget a gyorslétrehozási párbeszédpanelen.