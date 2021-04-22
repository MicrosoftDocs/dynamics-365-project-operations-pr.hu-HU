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
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857981"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="c8194-103">Belső projektek könyvelésének konfigurálása</span><span class="sxs-lookup"><span data-stu-id="c8194-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="c8194-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="c8194-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c8194-105">A belső projektek lehetővé teszik a vállalatok számára az olyan tevékenységekkel kapcsolatos költségek nyomon követését, amelyeket nem számláznak az ügyfélnek.</span><span class="sxs-lookup"><span data-stu-id="c8194-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="c8194-106">A belső projektek példái többek között a következők:</span><span class="sxs-lookup"><span data-stu-id="c8194-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="c8194-107">A termék, például a mobil alkalmazás fejlesztése és a fejlesztéshez kapcsolódó költségek nyomon követése.</span><span class="sxs-lookup"><span data-stu-id="c8194-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="c8194-108">Az értékesítés előtti idő és költség kezelése.</span><span class="sxs-lookup"><span data-stu-id="c8194-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="c8194-109">Ez az értékesítés előtti belső projekt később átalakítható számlázható projektre, ha az ajánlatot megnyerik.</span><span class="sxs-lookup"><span data-stu-id="c8194-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="c8194-110">A rendszer belsőként kezeli a Dynamics 365 Project Operations-szerződéshez nem társított projekteket.</span><span class="sxs-lookup"><span data-stu-id="c8194-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="c8194-111">A projekt költség- és bevételi profiljai nincsenek használva a projekt könyvelési szabályainak meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="c8194-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="c8194-112">A belső projektek költségét a rendszer mindig a haszon és a veszteség elvei használatával könyveli.</span><span class="sxs-lookup"><span data-stu-id="c8194-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="c8194-113">A főkönyvi számlák a feladáshoz a **Főkönyvi feladás beállítása** lapon definiálhatók.</span><span class="sxs-lookup"><span data-stu-id="c8194-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="c8194-114">Az időtranzakciókat a program a **Költség** számla terhelésével és a **Bérlista-hozzárendelés** számla jóváírásával könyveli.</span><span class="sxs-lookup"><span data-stu-id="c8194-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="c8194-115">A Kiadási tranzakciókat a program a **Költség** számla terhelésével és a **Ellenszámla a kiadáshoz** számla jóváírásával könyveli.</span><span class="sxs-lookup"><span data-stu-id="c8194-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="c8194-116">Az elemtranzakciók a **Költség** számla megterhelésével és a **Költség - Elem** számla jóváírásával teszik közzé.</span><span class="sxs-lookup"><span data-stu-id="c8194-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="c8194-117">A tranzakciók feladása után a projektbe, ha a projekt egy projektszerződéssel van társítva, a rendszer sztornírozza az összes halmozott tranzakciót, és új számlázható tranzakciókat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8194-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="c8194-118">A számlázható tranzakciók az adott projekt költség és bevételi profiljaiban meghatározott könyvelési szabályokat követik.</span><span class="sxs-lookup"><span data-stu-id="c8194-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
