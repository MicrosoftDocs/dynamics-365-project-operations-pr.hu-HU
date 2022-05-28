---
title: Belső projektek könyvelésének konfigurálása
description: Ez a témakör a Project Operations alkalmazásban a belső projektek könyvelési gyakorlatainak beállításával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597847"
---
# <a name="configure-accounting-for-internal-projects"></a>Belső projektek könyvelésének konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A belső projektek lehetővé teszik a vállalatok számára az olyan tevékenységekkel kapcsolatos költségek nyomon követését, amelyeket nem számláznak az ügyfélnek. A belső projektek példái többek között a következők:

- A termék, például a mobil alkalmazás fejlesztése és a fejlesztéshez kapcsolódó költségek nyomon követése.
- Az értékesítés előtti idő és költség kezelése. Ez az értékesítés előtti belső projekt később átalakítható számlázható projektre, ha az ajánlatot megnyerik.

A rendszer belsőként kezeli a Dynamics 365 Project Operations-szerződéshez nem társított projekteket. A projekt költség- és bevételi profiljai nincsenek használva a projekt könyvelési szabályainak meghatározásához. A belső projektek költségét a rendszer mindig a haszon és a veszteség elvei használatával könyveli. A főkönyvi számlák a feladáshoz a **Főkönyvi feladás beállítása** lapon definiálhatók.

- Az időtranzakciókat a program a **Költség** számla terhelésével és a **Bérlista-hozzárendelés** számla jóváírásával könyveli.
- A Kiadási tranzakciókat a program a **Költség** számla terhelésével és a **Ellenszámla a kiadáshoz** számla jóváírásával könyveli.
- Az elemtranzakciók a **Költség** számla megterhelésével és a **Költség - Elem** számla jóváírásával teszik közzé.

A tranzakciók feladása után a projektbe, ha a projekt egy projektszerződéssel van társítva, a rendszer sztornírozza az összes halmozott tranzakciót, és új számlázható tranzakciókat hoz létre. A számlázható tranzakciók az adott projekt költség és bevételi profiljaiban meghatározott könyvelési szabályokat követik.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
