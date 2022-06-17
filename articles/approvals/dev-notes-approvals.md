---
title: Fejlesztői jegyzetek jóváhagyásokhoz
description: Ez a cikk további fejlesztői információkat tartalmaz a jóváhagyásokkal kapcsolatos munkáról.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924755"
---
# <a name="developer-notes-for-approvals"></a>Fejlesztői jegyzetek jóváhagyásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül. A rekordok helyes átvitele biztosítja a következőket: 

  - Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.
  - A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.


[!INCLUDE[footer-include](../includes/footer-banner.md)]