---
title: A Project Operations jogi személyenkénti integrációjának konfigurálása
description: Ez a témakör a jogi személyenkénti integráció beállításáról a Project Operations rendszerben tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122886"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="6d7f7-103">A Project Operations jogi személyenkénti integrációjának konfigurálása</span><span class="sxs-lookup"><span data-stu-id="6d7f7-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="6d7f7-104">_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_</span><span class="sxs-lookup"><span data-stu-id="6d7f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6d7f7-105">Ez a témakör végigvezeti a Dynamics 365 Project Operations jogi személyenként történő konfigurálásához szükséges lépéseken.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="6d7f7-106">Funkciókulcsok engedélyezése a Dynamics 365 Finance szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="6d7f7-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="6d7f7-107">A szükséges funkciók engedélyezéséhez hajtsa végre az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="6d7f7-108">A Dynamics 365 Finance-ben nyissa meg a **Funkciókezelés** munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="6d7f7-109">A **Funkciók listájában** keresse meg és engedélyezze a következő funkciókat:</span><span class="sxs-lookup"><span data-stu-id="6d7f7-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="6d7f7-110">**Több szerződéssor engedélyezése a projekthez**</span><span class="sxs-lookup"><span data-stu-id="6d7f7-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="6d7f7-111">**Project Operations engedélyezése Dynamics 365 Customer Engagement rendszeren**</span><span class="sxs-lookup"><span data-stu-id="6d7f7-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="6d7f7-112">Ha nem látható a listában a **Funkciókulcsok** elem, ellenőrizze, hogy a Finance verziója megfelel-e a minimális verziókövetelménynek (10.0.13-as alkalmazásverzió az összes minőségi frissítéssel, vagy újabb).</span><span class="sxs-lookup"><span data-stu-id="6d7f7-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="6d7f7-113">Válassza a **Frissítések keresése** lehetőséget a funkciólista frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="6d7f7-114">A Project Operations telepítési forgatókönyvének definiálása egy jogi személyhez</span><span class="sxs-lookup"><span data-stu-id="6d7f7-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="6d7f7-115">A Project Operations a Dynamics 365 Customer Engagement rendszeren jogi személy szintjén engedélyezhető.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="6d7f7-116">A Dynamics 365 Customer Engagement rendszerben használt Project Operations segítségével egy jogi személlyel rendelkezhet az erőforrás/nem készletezett alapú forgatókönyvek esetén.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="6d7f7-117">Ugyanabban a környezetben másik jogi személy is használhatja a Project Operationst a készletezett/gyártási rendelés esetekre.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="6d7f7-118">A Dynamics 365 Finance szolgáltatásban lépjen a **Projektmenedzsment és könyvelés** > **Beállítás** > **Globális projektmenedzsment és könyvelési paraméterek** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="6d7f7-119">A rendelkezésre álló jogi személyek listájában válassza ki azokat az entitásokat, ahol a több szerződéssor és a Project Operations a Dynamics 365 Customer Engagement funkciók engedélyezve lesznek.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="6d7f7-120">Hagyja ki azokat a jogi entitásokat, amelyek a Project Operations szolgáltatást készletezett/előállítási rendelési forgatókönyvek esetén használják.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="6d7f7-121">A jogi személyek csak akkor választhatók ki, ha nincs meglévő projektjei.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="6d7f7-122">Projektmenedzsment és könyvelési paraméterek konfigurálása</span><span class="sxs-lookup"><span data-stu-id="6d7f7-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="6d7f7-123">A Project Operationst használó minden jogi személynek a Dynamics 365 Customer Engagement rendszeren egy sor alapértelmezett paramétert kell használnia.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="6d7f7-124">Ezeket a paramétereket a **Project Operations** lapon kell konfigurálni, a **Projektkezelési és könyvelési paraméterek** oldalon.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="6d7f7-125">A paraméterek a következők:</span><span class="sxs-lookup"><span data-stu-id="6d7f7-125">The parameters are:</span></span>

  - <span data-ttu-id="6d7f7-126">**A számlázási típus alapértelmezései**: a Project Operations a számlázási típusú alapértékek rögzített halmazát használja, amelyeket le kell képeznie a Finance sortulajdonságaira.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="6d7f7-127">Hozzon létre egy rekordot minden egyes számlázási típushoz: **nincs megadva**, **számlázható**, **nem számlázható**, **ingyenes**, és **nem érhető el**.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="6d7f7-128">**Projektkategória alapértelmezései**: válassza ki az alapértelmezett projektkategóriákat, amelyeket az egyes tranzakciótípusok esetén használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="6d7f7-129">Ezek az alapértelmezett értékek a **Project Operations integrációs naplóban** és azokban a becslésekben használhatók, ahol a tényleges projekthez nem adtak meg tranzakciós kategóriát.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="6d7f7-130">**Előrejelzések**: válassza ki az idő-és költségbecslésekhez használandó előrejelzési modellt.</span><span class="sxs-lookup"><span data-stu-id="6d7f7-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
