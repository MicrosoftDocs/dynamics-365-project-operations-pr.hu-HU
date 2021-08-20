---
title: Fejlesztői jegyzetek jóváhagyásokhoz
description: Ez a témakör további fejlesztői információkat nyújt a jóváhagyások használatáról.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991669"
---
# <a name="developer-notes-for-approvals"></a>Fejlesztői jegyzetek jóváhagyásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül. A rekordok helyes átvitele biztosítja a következőket: 

  - Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.
  - A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]