---
title: Árazási dimenziók áttekintése
description: Ez a témakör a Dynamics 365 Project Operations árképzési dimenzióiról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898219"
---
# <a name="pricing-dimensions-overview"></a>Árazási dimenziók áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az árképzéshez és a költségek meghatározásához az emberi erőforrásokban felhasznált dimenziók két kategóriába sorolhatók:

- Személyek
- Tervezett munka

Emiatt kétféle árképzési dimenzió érhető el:

- **Értékkészletek**: Azon dimenziók, amelyek értékcsoportok rögzített enumerálásai.
- **Entitásalapú értékek**: Azon dimenziók, amelyek különböző értékcsoportok lehetnek.

## <a name="pricing-dimensions"></a>Árazási dimenziók

A Dynamics 365 Project Operations szolgáltatás részét képezi az árképzési dimenziók alapértelmezett csoportja. Ezek az árképzési dimenziók a **Project Operations** > **Paraméterek** részén tekinthetők meg. A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen. Ha engedélyezi ezeket a mezőket, beállíthatja az egyes szerepkörök és szervezeti egységek kombinációjához tartozó árakat és költségeket.

Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre.

## <a name="pricing-human-resource-time"></a>Az emberi erőforrás munkaidejének árképzése
Az, hogy a szervezet milyen módon képez árat a humán erőforrás munkaidejére gyakran fontos stratégiai szempont, amely közvetlenül befolyásolja a szervezet jövedelmezőségét. Dolgozzon együtt a pénzügyi csapatokkal és a gyakorlati vezetőkkel, amikor a szervezet készen áll arra, hogy meghatározza, hogyan kívánja beállítani a számla- és költségmértéket az emberi erőforrás munkaidejére vonatkozóan.

Az árképzés egyéb szempontjai között szerepel, hogy újra kell-e használni olyan mezőket vagy entitásokat, amelyek jelenleg nem árképzési dimenziók, ugyanakkor a szervezetben érvényes árképzési dimenzióként alkalmazandók. Az olyan mezők, mint a **Tranzakciós kategória** (**msdyn_transactioncategory**) és a **Lefoglalható erőforrás** (**bookableresource**) példák a jelöltdimenziókra. 

Azt is gondolja át, hogy az árképzési dimenzió tábla vagy értékkészlet legyen-e. Ha egy dimenzió értékének olyan változásait látja előre, amelyek meghaladják a 10-et vagy 12-őt, és további attribútumokra van szüksége ezekhez az értékekhez, akkor érdemesebb entitást létrehoznia, mint értékkészletet. Az értékkészlet fenntartásához, például az értékek hozzáadásához vagy eltávolításához, rendszergazda vagy fejlesztő szükséges, míg új sorok hozzáadását a táblához a legtöbb felhasználó megteheti.

A következő példa azt a számlamértéket mutatja, amelyet azon szerepkör és erőforrásbiztosító szervezeti egység alapján állítanak fel, amelyhez az erőforrás tartozik. A költség mértéke általában a munkavállaló fizetési sávjától és attól a szervezeti egységtől függ, amelyhez tartozik. Ebben a példában a számlázási és költségtáblázatok a következőképpen alakulnak.

**Számlaminta**

| Szerepkör        | Szerv. egység    |Egység      |Ár      |Pénznem  |
| ------------|-------------|----------|----------:|----------|
| Fejlesztő   | Contoso USA  |Hour | 200|USD     |
| Fejlesztő   | Contoso India |Hour|   112|USD     |


**Költségminta**

| Fizetési sáv     | Szerv. egység    |Egység      |Ár      |Pénznem  |
| ----------------|-------------|----------|----------:|----------|
| Cégem_Sáv1 | Contoso USA  |Hour | 145|USD     |
| Cégem_Sáv2 | Contoso India |Hour|   67|USD     |
