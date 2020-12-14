---
title: Belső projektek könyvelésének konfigurálása
description: Ez a témakör a Project Operations alkalmazásban a belső projektek könyvelési gyakorlatainak beállításával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132381"
---
# <a name="configure-accounting-for-internal-projects"></a>Belső projektek könyvelésének konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A belső projektek lehetővé teszik a vállalatok számára az olyan tevékenységekkel kapcsolatos költségek nyomon követését, amelyeket nem számláznak az ügyfélnek. A belső projektek példái többek között a következők:

- A termék, például a mobil alkalmazás fejlesztése és a fejlesztéshez kapcsolódó költségek nyomon követése.
- Az értékesítés előtti idő és költség kezelése. Ez az értékesítés előtti belső projekt később átalakítható számlázható projektre, ha az ajánlatot megnyerik.

A Dynamics 365 Project Operations alkalmazásban szerződéshez nem társított összes projekt belsőként kezelendő. A projekt költség- és bevételi profiljai nincsenek használva a projekt könyvelési szabályainak meghatározásához. A belső projektek költségét a rendszer mindig a haszon és a veszteség elvei használatával könyveli. A főkönyvi számlák a feladáshoz a **Főkönyvi feladás beállítása** lapon definiálhatók.

- Az időtranzakciókat a program a **Költség** számla terhelésével és a **Bérlista-hozzárendelés** számla jóváírásával könyveli.
- A Kiadási tranzakciókat a program a **Költség** számla terhelésével és a **Ellenszámla a kiadáshoz** számla jóváírásával könyveli.

A tranzakciók feladása után a projektbe, ha a projekt egy projektszerződéssel van társítva, a rendszer sztornírozza az összes halmozott tranzakciót, és új számlázható tranzakciókat hoz létre. A számlázható tranzakciók az adott projekt költség és bevételi profiljaiban meghatározott könyvelési szabályokat követik.

