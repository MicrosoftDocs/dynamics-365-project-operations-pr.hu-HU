---
title: Fejlesztői jegyzetek jóváhagyásokhoz
description: Ez a témakör további fejlesztői információkat nyújt a jóváhagyások használatáról.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996794"
---
# <a name="developer-notes-for-approvals"></a>Fejlesztői jegyzetek jóváhagyásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül. A rekordok helyes átvitele biztosítja a következőket: 

  - Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.
  - A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]