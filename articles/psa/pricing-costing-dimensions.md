---
title: Árképzés és költségdimenziók kezdőlap
description: Ez a témakör áttekintést nyújt az árképzési dimenziókról.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151301"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Árképzés és költségdimenziók kezdőlap

[!include [banner](../includes/psa-now-project-operations.md)]

A projektalapú szervezetekben a munkadíjak és a költségszámítás beállításához használt dimenziókat a következő attribútumok befolyásolják:

- A saját tapasztalataik, szerepkörük vagy földrajzi elhelyezkedésük alapján hasonló munkát végző személyek
- A munka összetettségéhez vagy napszakhoz hasonlóan elvégzendő munka

Tekintettel a munka ezen attribútumainak jellegzetességére és a munka végrehajtásához szükséges személyekre, a Project Service Automation rendszerben kétféle árazási dimenzióérték érhető el: 

- **Értékkészletek**: azon attribútumok, amelyek értékcsoportok rögzített felsorolásai.
- **Entitásalapú értékek**: azon attribútumok, amelyek olyan különböző, de véges értékcsoportokat tartalmazhatnak, amelyek idővel változhatnak.

## <a name="pricing-dimensions"></a>Árazási dimenziók

A PSA alapértelmezett árképzési dimenziókkal rendelkezik. Megnézheti ezeket a **Project Service** > **Paraméterek** részére lépve. A paraméterrekordban az **Összegalapú árképzési dimenziók** fülön ellenőrizze, hogy a **msdyn_resourcecategory** szerepkör és a **msdyn_organizationalunit** erőforrásbiztosító szervezeti egység rendelkezik **Értékesítésre vonatkozó** és **Költségre vonatkozó** mezőkkel, és hogy ezek beállítása **Igen** legyen. Ez lehetővé teszi az egyes szerepkörök és szervezeti egységkombinációk árának és költségének beállítását.

![Képernyőkép a Project Service paramétereiről az „Értékesítésre vonatkozó” mező kiemelésével](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ha a PSA 3. verzióját megelőzően használta a használatra kész szerepköröket és szervezeti egységeket árképzési dimenziókként, akkor nem lesz észlelhető változás. Továbbra is használhatja a Project Service szolgáltatást a megszokott módon. 

Ha további attribútumok használatával szükséges árakat vagy költségeket fizetnie az erőforrásokért, testreszabott mezőket, entitásokat és dimenziókat hozhat létre. További információt a következő témakörökben talál, azonban vegye figyelembe, hogy az eljárásokat az alábbiakban felsorolt sorrendben kell elvégeznie:

- [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md)
- [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz](field-references.md)
- [Egyéni mezők beállítása árazási dimenziókként ](set-up-pricing-dimensions.md)
- [Bővítményattribútumok frissítése új árképzési dimenziók felvételéhez](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Az emberi erőforrás munkaidejének árképzése
Az, hogy a szervezet milyen módon képez árat a humán erőforrás munkaidejére gyakran fontos stratégiai szempont, amely közvetlenül befolyásolja a szervezet jövedelmezőségét. Dolgozzon együtt a pénzügyi csapatokkal és a gyakorlati vezetőkkel, amikor a szervezet készen áll arra, hogy meghatározza, hogyan kívánja beállítani a számla- és költségmértéket az emberi erőforrás munkaidejére vonatkozóan.

Az árképzés egyéb szempontjai között szerepel, hogy újra kell-e használni olyan mezőket vagy entitásokat, amelyek jelenleg nem árképzési dimenziók, ugyanakkor a szervezetben érvényes árképzési dimenzióként alkalmazandók. Az olyan mezők, mint a **Tranzakciós kategória** (**msdyn_transactioncategory**) és a **Lefoglalható erőforrás** (**bookableresource**) példák a jelöltdimenziókra. 

Azt is gondolja át, hogy az árképzési dimenzió tábla vagy értékkészlet legyen-e. Ha egy dimenzió értékének olyan változásait látja előre, amelyek meghaladják a 10-es vagy 12-es értéket, és további attribútumokra van szüksége ezekhez az értékekhez, akkor érdemesebb entitást létrehoznia, nem pedig értékkészletet. Az értékkészlet fenntartásához – például az értékek hozzáadásához vagy eltávolításához – rendszergazda vagy fejlesztő szükséges, míg új sorok hozzáadását a táblához a legtöbb üzleti felhasználó elvégezheti.

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