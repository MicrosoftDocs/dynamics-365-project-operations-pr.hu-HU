---
title: Árazási dimenziók áttekintése
description: Ez a témakör a Dynamics 365 Project Operations árazási dimenzióiról nyújt információkat.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650197"
---
# <a name="pricing-dimensions-overview"></a>Árképzési dimenziók áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Az árképzéshez és a költségek meghatározásához az emberi erőforrásokban felhasznált dimenziók két kategóriába sorolhatók:

- Személyek
- Tervezett munka

Emiatt kétféle árképzési dimenzió érhető el:

- **Értékkészletek**: Azon dimenziók, amelyek értékcsoportok rögzített enumerálásai.
- **Entitásalapú értékek**: Azon dimenziók, amelyek különböző értékcsoportok lehetnek.

## <a name="pricing-dimensions"></a>Árképzési dimenziók

A Dynamics 365 Project Operations alapértelmezett árképzési dimenziókkal rendelkezik. Ezek az árképzési dimenziók a **Project Operations** > **Paraméterek** részén tekinthetők meg. A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen. Ha engedélyezi ezeket a mezőket, beállíthatja az egyes szerepkörök és szervezeti egységek kombinációjához tartozó árakat és költségeket.

![Képernyőkép a Project Service paramétereiről az „Értékesítésre vonatkozó” mező kiemelésével](media/PS-OOB-parameters.png)

Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre. További tájékoztatás a következő témakörökben. 
  
  > [!NOTE]
  > Az eljárásokat a felsorolás sorrendjében kell elvégezni.

1. [Megoldás létrehozása egyéni árképzési dimenziókhoz](../sales/create-solution-custompd.md)
2. [Egyéni mezők és entitások létrehozása](create-custom-fields-entities-pricing-dimensions.md)
3. [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz ](add-custom-fields-price-setup-transactional-entities.md)
4. [Egyéni mezők beállítása árazási dimenziókként ](set-up-custom-fields-pricing-dimensions.md)
5. [Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez](update-plugin-attributes-pd.md)


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]