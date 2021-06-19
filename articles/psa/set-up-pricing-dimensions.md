---
title: Egyéni mezők beállítása árazási dimenziókként
description: Ez a témakör az egyedi árazási dimenziók beállításáról nyújt információkat.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cce3a3fe6aef247380f6284f58d49337f969c38c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008314"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Egyéni mezők beállítása árazási dimenziókként 

[!include [banner](../includes/psa-now-project-operations.md)]

Ez a témakör feltételezi, hogy először elvégezte a következő eljárásokat: [Egyéni mezők és entitások létrehozása](create-custom-fields-entities.md) és [Egyéni mezők hozzáadása az ár a telepítést és tranzakciós szervezetek](field-references.md). Ha még nem fejezte be ezeket az eljárásokat, menjen vissza, és fejezze be őket, majd térjen vissza ehhez a témához. 

Ez a témakör az egyedi árazási dimenziók beállításáról nyújt információkat. A Project Service webes felületén, a **Paraméterek** oldalon, az **Összeg alapú árképzési dimenziók** lapon megjelennek az árazási dimenziók entitásaiban szereplő rekordok. Alapértelmezés szerint a Project Service telepítése 2 sort hoz létre a fül rácsában:

- **msdyn_resourcecategory** (Szerepkör)
- **msdyn_OrganizationalUnit** (Szervezeti egység)

> [!IMPORTANT]
> Ne törölje ezeket a sorokat. Azonban, ha nincs rájuk szükség, akkor azokat nem kell alkalmazni egy adott helyzetben a **Költségre alkalmazandó**, **Értékesítésre alkalmazandó** és **Vásárlásra alkalmazandó** paraméterek **Nem** értékre állításával. Ha ezeket az attribútumértékeket **Nem**-re állítja, akkor ugyanaz a hatása, ha nem rendelkezik mezővel, mint árképzési dimenzióval.

Ahhoz, hogy egy mező árképzési dimenzióvá váljon, a következőknek kell lennie:

- Mezőként lett létrehozva a **Szerepkörát** és **Szerepkör felár** entitásokban. További információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és a tranzakciós entitásokhoz](field-references.md).
- Sorként jön létre az **Árazási dimenzió** táblázatban. Például adjon hozzá árképzési dimenziós sorokat a következő ábra szerint. 

![Összeg alapú árképzési dimenziós sorok](media/Amt-based-PD.png)

Vegye figyelembe, hogy az erőforrás-munkaidőt (**msdyn_resourceworkhours**) feláralapú dimenzióként adták hozzá, és a **Feláron alapuló árképzési dimenzió** lapon a rácshoz adták.

![Feláralapú árképzési dimenziós sorok](media/Markup-based-PD.png)

> [!IMPORTANT]
> A táblázat árazási dimenziós adatainak bármilyen megváltozása, létező vagy új, csak a gyorsítótár frissítése után kerül továbbításra a Project Service árazási üzleti logikájába. A gyorsítótár frissítési ideje akár 10 percet is igénybe vehet. Várja meg, amíg az ár alapértelmezett logikájában bekövetkező változások megjelennek, amelyeknek az árképzési dimenzió adatainak megváltozásából kell következniük.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Az Árképzési dimenziók táblázat attribútumai
A következő szakaszok információkat tartalmaznak az **Árazási dimenziók** táblázat különböző attribútumairól.

### <a name="pricing-dimension-name"></a>Árképzési dimenzió neve
Ennek az értéknek pontosan meg kell egyeznie a mezőséma nevével, amelyet a **Szerepkörár** táblázathoz adunk az egyedi árazási dimenziókhoz. A mezőknek a **Szerepkörár** táblájához történő hozzáadásával kapcsolatos további információkért lásd: [Egyéni mezők hozzáadása az árbeállításhoz és tranzakciós entitásokhoz](field-references.md).

### <a name="type-of-dimension"></a>A dimenzió típusa
Az árképzési dimenzióknak két típusa létezik:
  
  - **Összegalapú dimenziók**: A bemeneti kontextus dimenzióértékei illeszkednek a dimenziós értékekhez a **Szerepkörár** sorban, és az ár/költség alapértelmezés szerint közvetlenül a **Szerepkörár** táblázatból származik.
  - **Feláron alapuló dimenziók** : Ezek olyan dimenziók, amelyekben a Project Service a következő háromlépcsős eljárást fogja alkalmazni az ár/költség megszerzésére
 
    1. A Project Service összeegyezteti a nem jelölésen alapuló dimenziós értékeket a bemeneti környezetből a Szerepkörár sorba az alapkamat megszerzéséhez.
    2. A Project Service az összes dimenziós értéket egyezteti a bemeneti környezetből a **Szerepkörár** sorig, hogy megkapja a felárszázalékot.
    3. A Project Service a második lépéstől a jelölési százalékot az alapvető kamatlábakhoz használja, amelyeket az első lépésben a **Szerepkörár** táblázatból nyert, hogy elérje a végső árat/költségeket.
   
   Az alábbi táblázat szemlélteti az árkülönbözetek kiszámítását.
  
| Szerepkör        | Szerv. egység    |Munka helye      |Normál cím      |Erőforrás-munkaidő      |  Felár|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Telephely            |                    |Túlóra                 |15     |
|             | Contoso India|Helyi             |                    |Túlóra                 |10     |
|             | Contoso US   |Helyi             |                    |Túlóra                 |20     |


Ha a Contoso India erőforrása, amelynek alapára 100 USD, működik a helyszínen, és napi 8 órát szokásos időt és 2 órát túlórát jelent az időbeíráskor, a Project Service árazási motor 8 órán keresztül 100-as alapárat fog használni rögzíteni 800 USD. A 2 órás túlórára 15%-os felárat kell alkalmazni a 100-as alapárra, hogy 115 USD egységárhoz jussanak, és a teljes költség 230 USD lesz.

### <a name="applicable-to-cost"></a>Költségre alkalmazható 
Ha ezt **Igen**-re állítja , ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörár** és **Szerepkör felár** összeegyeztetéséhez, amikor a költségeket és a felárarányokat lekérdezi.

### <a name="applicable-to-sales"></a>Értékesítésre alkalmazható
Ha ez az **Igen**-re van állítva, akkor ez azt jelzi, hogy a bemeneti kontextusban szereplő dimenzióértéket kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a számla és a felárarány lekérésekor.

### <a name="applicable-to-purchase"></a>Vásárlásra alkalmazható
Ha ezt **Igen**-re állítja, ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a vételár lekérdezésekor. A Project Service jelenleg nem támogatja az alvállalkozási forgatókönyveket, ezért ezt a mezőt nem használja. 

### <a name="priority"></a>Prioritás
A dimenzió prioritásának meghatározása segít a Project Service árazásában abban az esetben is, ha nem talál pontos egyezést a bemeneti dimenziók értékei és a **Szerepkörát** vagy a **Szerep felár** táblázatok értékei között. Ebben a forgatókönyvben a Project Service null értékeket fog használni a páratlan dimenziós értékekhez, a súlyok fontossági sorrendben történő megmérésével.

- **Költségprioritás**: A dimenzió költség prioritásának értéke jelzi annak dimenzióját, amikor összeegyeztetik a költségárakkal. A **Költségprioritás** értékének egyedinek kell lennie, a **Költségre alkalmazható** dimenziókban.
- **Értékesítési prioritás**: A dimenzió eladási prioritása értéke jelzi ennek a dimenziónak a súlyát, amikor egyeztetik az eladási árak vagy a számlázási tarifák beállításával. Az **Értékesítési prioritás** értékének egyedinek kell lennie, az **Értékesítésre alkalmazható** dimenziókban.


[!INCLUDE[footer-include](../includes/footer-banner.md)]