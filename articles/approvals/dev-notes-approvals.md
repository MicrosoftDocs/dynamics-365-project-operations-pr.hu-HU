---
title: Fejlesztői jegyzetek jóváhagyásokhoz
description: Ez a témakör további fejlesztői információkat nyújt a jóváhagyások használatáról.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483951"
---
# <a name="developer-notes-for-approvals"></a>Fejlesztői jegyzetek jóváhagyásokhoz

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül. A rekordok helyes átvitele biztosítja a következőket: 

  - Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.
  - A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.
