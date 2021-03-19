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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290272"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="1b506-103">Fejlesztői jegyzetek jóváhagyásokhoz</span><span class="sxs-lookup"><span data-stu-id="1b506-103">Developer notes for Approvals</span></span>

<span data-ttu-id="1b506-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="1b506-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1b506-105">A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül.</span><span class="sxs-lookup"><span data-stu-id="1b506-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="1b506-106">A rekordok helyes átvitele biztosítja a következőket:</span><span class="sxs-lookup"><span data-stu-id="1b506-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="1b506-107">Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.</span><span class="sxs-lookup"><span data-stu-id="1b506-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="1b506-108">A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="1b506-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]