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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="c8366-103">Fejlesztői jegyzetek jóváhagyásokhoz</span><span class="sxs-lookup"><span data-stu-id="c8366-103">Developer notes for Approvals</span></span>

<span data-ttu-id="c8366-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c8366-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c8366-105">A Dynamics 365 Project Operations olyan érvényesítési logikát tartalmaz, amely biztosítja a pontos rekordátvitelt a jóváhagyási fázisokon keresztül.</span><span class="sxs-lookup"><span data-stu-id="c8366-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="c8366-106">A rekordok helyes átvitele biztosítja a következőket:</span><span class="sxs-lookup"><span data-stu-id="c8366-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="c8366-107">Az összes támogató sor a kapcsolódó táblákban jön létre, például a naplók és a tényadatok.</span><span class="sxs-lookup"><span data-stu-id="c8366-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="c8366-108">A jóváhagyó a továbblépés előtt a **Projekt jóváhagyójának** van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="c8366-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]