---
title: Egyéni mezők beállítása árazási dimenziókként
description: Ez a témakör az egyedi árazási dimenziók egyéni mezőkkel történő beállításáról nyújt információkat.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d40a80f80bd766bfc19e831ea805a4043baf0030
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004714"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Egyéni mezők beállítása árazási dimenziókként

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Ez a témakör feltételezi, hogy már elvégezte a következő témakörökben ismertetett eljárásokat: [Egyéni mezők és entitások létrehozása](create-custom-fields-entities-pricing-dimensions.md) és [Kötelező egyéni mezők hozzáadása az ár beállításához és a tranzakciós entitások](add-custom-fields-price-setup-transactional-entities.md). Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához. 

Ez a témakör az egyedi árazási dimenziók beállításáról nyújt információkat. A **Paraméterek** oldal **Mennyiségalapú árazási dimenziók** lapján láthatók az árképzési dimenzió entitásaiban lévő rekordok. Alapértelmezés szerint ezen a lapon két sor van a rácsban:

- **msdyn_resourcecategory** (Szerepkör)
- **msdyn_OrganizationalUnit** (Szervezeti egység)

> [!IMPORTANT]
> Ne törölje ezeket a sorokat. Azonban, ha nincs rájuk szükség, akkor azokat nem kell alkalmazni egy adott helyzetben a **Költségre alkalmazandó**, **Értékesítésre alkalmazandó** és **Vásárlásra alkalmazandó** paraméterek **Nem** értékre állításával. Ha ezeket az attribútumértékeket **Nem**-re állítja, akkor ugyanaz a hatása, ha nem rendelkezik mezővel, mint árképzési dimenzióval.

Ahhoz, hogy egy mező árképzési dimenzióvá váljon, a következőknek kell lennie:

- Mezőként lett létrehozva a **Szerepkörát** és **Szerepkör felár** entitásokban. További információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz](add-custom-fields-price-setup-transactional-entities.md).

- Sorként jön létre az **Árazási dimenzió** táblázatban. Például adjon hozzá árképzési dimenziós sorokat a következő ábra szerint. 

![Összeg alapú árképzési dimenziós sorok](media/Amt-based-PD.png)

Az erőforrás munkaidejét (**msdyn_resourceworkhours**) árrésalapú dimenzióként adták hozzá, és a **Feláron alapuló árképzési dimenzió** lapon a rácshoz adták.

![Feláralapú árképzési dimenziós sorok](media/Markup-based-PD.png)


> [!IMPORTANT]
> Ha az árképzési dimenziók táblázatban lévő adatait bárhogy módosítja (legyen szó meglévő vagy új adatokról), a rendszer csak a gyorsítótár frissítése után továbbítja a módosításokat az árképzési üzleti logikába. A gyorsítótár frissítési ideje akár 10 percet is igénybe vehet. Várja meg, amíg az ár alapértelmezett logikájában bekövetkező változások megjelennek, amelyeknek az árképzési dimenzió adatainak megváltozásából kell következniük.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Az Árképzési dimenziók táblázat attribútumai
A következő szakaszok információkat tartalmaznak az **Árazási dimenziók** táblázat különböző attribútumairól.

### <a name="pricing-dimension-name"></a>Árképzési dimenzió neve
Ennek az értéknek pontosan meg kell egyeznie a mezőséma nevével, amelyet a **Szerepkörár** táblázathoz adunk az egyedi árazási dimenziókhoz. A mezőknek a **Szerepkörár** táblájához történő hozzáadásával kapcsolatos további információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és tranzakciós entitásokhoz](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>A dimenzió típusa
Az árképzési dimenzióknak két típusa létezik:
  
  - **Összegalapú dimenziók**: A bemeneti kontextus dimenzióértékei illeszkednek a dimenziós értékekhez a **Szerepkörár** sorban, és az ár/költség alapértelmezés szerint közvetlenül a **Szerepkörár** táblázatból származik.
  - **Árrésen alapuló dimenziók**: Ezek olyan dimenziók, amelyekben a rendszer a következő háromlépcsős eljárást fogja alkalmazni az ár/költség lekérésére:
 
    1. Az alapdíj megállapításához a rendszer egyezteti a bemeneti környezetből származó, nem árrésen alapuló dimenzióértékeket a Szerepkörár sorral.
    2. Az árrés százalékos értékének megállapításához a rendszer egyezteti a bemeneti környezetből származó dimenzióértékeket a **Szerepkörár** sorral.
    3. A végső ár/költség megállapításához a rendszer alkalmazza az árrés második lépésből származó százalékos értékét a **Szerepkörár** táblázatból az első lépésben kinyert alapdíjra.
   
   Az alábbi táblázat szemlélteti az árkülönbözetek kiszámítását.
  
| Szerepkör        | Szerv. egység    |Munka helye      |Normál cím      |Erőforrás-munkaidő      |  Felár|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Telephely            |                    |Túlóra                 |15     |
|             | Contoso India|Helyi             |                    |Túlóra                 |10     |
|             | Contoso US   |Helyi             |                    |Túlóra                 |20     |


Ha a Contoso India erőforrása, amelynek alapára 100 USD, működik a helyszínen, és napi 8 órát szokásos időt és 2 órát túlórát jelent az időbeíráskor, az árazási motor 8 órán keresztül 100-as alapárat fog használni rögzíteni 800 USD. A 2 órás túlórára 15%-os felárat kell alkalmazni a 100-as alapárra, hogy 115 USD egységárhoz jussanak, és a teljes költség 230 USD lesz.

### <a name="applicable-to-cost"></a>Költségre alkalmazható 
Ha ezt **Igen**-re állítja , ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörár** és **Szerepkör felár** összeegyeztetéséhez, amikor a költségeket és a felárarányokat lekérdezi.

### <a name="applicable-to-sales"></a>Értékesítésre alkalmazható
Ha ez az **Igen**-re van állítva, akkor ez azt jelzi, hogy a bemeneti kontextusban szereplő dimenzióértéket kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a számla és a felárarány lekérésekor.

### <a name="applicable-to-purchase"></a>Vásárlásra alkalmazható
Ha ezt **Igen**-re állítja, ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a vételár lekérdezésekor. Az alvállalkozói forgatókönyvek nem támogatottak, így ezt a mezőt nem használja a rendszer. 

### <a name="priority"></a>Prioritás
A dimenzió prioritásának meghatározása abban az esetben is segít az árképzésben, ha nem található pontos egyezés a bemeneti dimenziók értékei és a **Szerepkörár** vagy a **Szerep felár** táblázat értékei között. Ebben a forgatókönyvben a rendszer a súlyok fontossági sorrendben történő megmérésével null értékeket fog használni a nem egyező dimenziók értékeihez.

- **Költségprioritás**: A dimenzió költség prioritásának értéke jelzi annak dimenzióját, amikor összeegyeztetik a költségárakkal. A **Költségprioritás** értékének egyedinek kell lennie, a **Költségre alkalmazható** dimenziókban.
- **Értékesítési prioritás**: A dimenzió eladási prioritása értéke jelzi ennek a dimenziónak a súlyát, amikor egyeztetik az eladási árak vagy a számlázási tarifák beállításával. Az **Értékesítési prioritás** értékének egyedinek kell lennie, az **Értékesítésre alkalmazható** dimenziókban.


[!INCLUDE[footer-include](../includes/footer-banner.md)]