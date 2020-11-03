---
title: Értékesítési árlista beállítása
description: Ez a témakör az értékesítési árlisták projektek árképzéséhez történő beállítását ismerteti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078147"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="b1e03-103">Értékesítési árlista beállítása</span><span class="sxs-lookup"><span data-stu-id="b1e03-103">Sales price list setup</span></span>

<span data-ttu-id="b1e03-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="b1e03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b1e03-105">A projektárajánlatok és -szerződések esetében a projekt árlistájának eltérő árfelülbírálási mintázata van, mint egy termék árlistájának.</span><span class="sxs-lookup"><span data-stu-id="b1e03-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="b1e03-106">Egy termékkatalóguson alapuló árajánlati soron felülbírálhatja az árat a szerepkörökre és kategóriákra közvetlenül az árajánlatsorban, mert minden ajánlati sor pontosan egy katalóguselemre mutat.</span><span class="sxs-lookup"><span data-stu-id="b1e03-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="b1e03-107">Projektalapú árajánlati soron azonban nem lehet felülbírálni az árakat szerepkörökre és kategóriákra közvetlenül az árajánlati soron.</span><span class="sxs-lookup"><span data-stu-id="b1e03-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="b1e03-108">A projekt árlistája két külön felülbírálási mintával használható.</span><span class="sxs-lookup"><span data-stu-id="b1e03-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e03-109">Javasoljuk, hogy legyen külön árlista a projekterőforrásokhoz és a katalóguselemekhez, a kettő közötti viselkedési különbségek miatt az árak felülbírálásakor.</span><span class="sxs-lookup"><span data-stu-id="b1e03-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="b1e03-110">A következő entitások mindegyike rendelkezik egy vagy több kapcsolódó értékesítési árlistával a projekt árazásához:</span><span class="sxs-lookup"><span data-stu-id="b1e03-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="b1e03-111">Ügyfél (fiók)</span><span class="sxs-lookup"><span data-stu-id="b1e03-111">Customer (account)</span></span> 
- <span data-ttu-id="b1e03-112">Lehetőség</span><span class="sxs-lookup"><span data-stu-id="b1e03-112">Opportunity</span></span> 
- <span data-ttu-id="b1e03-113">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="b1e03-113">Quote</span></span> 
- <span data-ttu-id="b1e03-114">Projektszerződés</span><span class="sxs-lookup"><span data-stu-id="b1e03-114">Project Contract</span></span>

<span data-ttu-id="b1e03-115">Ezeknek az entitásoknak az árlistához való társulását a projekt árlistái jelzik.</span><span class="sxs-lookup"><span data-stu-id="b1e03-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="b1e03-116">Egy vagy több árlistát társíthat az Ügyfél, a Lehetőség, az Ajánlat és a Projektszerződés értékesítési entitásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b1e03-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="b1e03-117">Az alapértelmezett projektárlistát nem automatikusan írják be az ügyfélrekordba.</span><span class="sxs-lookup"><span data-stu-id="b1e03-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="b1e03-118">A projekt árlistáját azonban manuálisan csatolhatja az ügyfélrekordhoz.</span><span class="sxs-lookup"><span data-stu-id="b1e03-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="b1e03-119">Ennek ellenére csak akkor kell manuálisan csatolnia a projekt árlistáját, ha egyedi árazási megállapodást kötött az ügyféllel.</span><span class="sxs-lookup"><span data-stu-id="b1e03-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="b1e03-120">Ha egy projektárlistát csatolnak egy értékesítési entitáshoz, a rendszer a következő információkat ellenőrzi:</span><span class="sxs-lookup"><span data-stu-id="b1e03-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="b1e03-121">Az árlista rendelkezik **Értékesítés** környezettel.</span><span class="sxs-lookup"><span data-stu-id="b1e03-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="b1e03-122">Az árlista pénzneme megegyezik az ügyfél pénznemével.</span><span class="sxs-lookup"><span data-stu-id="b1e03-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="b1e03-123">A projektszerződéseken a következő prioritási sorrend használatos a kapcsolódó projektárlisták automatikus beállításához:</span><span class="sxs-lookup"><span data-stu-id="b1e03-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="b1e03-124">Ajánlat</span><span class="sxs-lookup"><span data-stu-id="b1e03-124">Quote</span></span>
2. <span data-ttu-id="b1e03-125">Lehetőség</span><span class="sxs-lookup"><span data-stu-id="b1e03-125">Opportunity</span></span>
3. <span data-ttu-id="b1e03-126">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="b1e03-126">Customer</span></span> 
4. <span data-ttu-id="b1e03-127">Globális beállítások</span><span class="sxs-lookup"><span data-stu-id="b1e03-127">Global settings</span></span> 

<span data-ttu-id="b1e03-128">Amikor egy projektárlistát alapértelmezés szerint ad meg, a rendszer ellenőrzi, hogy a pénznem megegyezik-e az ügyfél pénznemével, és hogy a megadott alapértelmezett árlisták az **Értékesítés** kontextusban vannak-e.</span><span class="sxs-lookup"><span data-stu-id="b1e03-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="b1e03-129">Összekapcsolhat több projektárlistát az Ügyfél, a Lehetőség, az Ajánlat és a Projekt szerződéses entitásokkal.</span><span class="sxs-lookup"><span data-stu-id="b1e03-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="b1e03-130">Ez a képesség támogatja a hosszú ideje működő projektszerződés dátum-specifikus alapértelmezett árait, ahol több árlistára lehet szükség az infláció miatt bekövetkező árfrissítések elszámolására.</span><span class="sxs-lookup"><span data-stu-id="b1e03-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="b1e03-131">Azonban ha az Ügyfél, a Lehetőség, az Ajánlat vagy a Projektszerződés entitással társított árlisták hatálya átfedésben van, akkor az alapértelmezett árak helytelenek lehetnek.</span><span class="sxs-lookup"><span data-stu-id="b1e03-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="b1e03-132">Ezért biztosítania kell, hogy az átfedő hatályú projektárak ne legyenek társítva ezekhez az entitásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b1e03-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
