---
title: Fejlesztői jegyzetek jóváhagyásokhoz
description: Ez a témakör további fejlesztői információkat nyújt a jóváhagyások használatáról.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579723"
---
# <a name="developer-notes-for-approvals"></a>Fejlesztői jegyzetek jóváhagyásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül. A rekordok helyes átvitele biztosítja a következőket: 

  - Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.
  - A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]