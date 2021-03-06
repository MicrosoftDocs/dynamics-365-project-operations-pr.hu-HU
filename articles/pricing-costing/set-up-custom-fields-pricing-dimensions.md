---
title: Egyéni mezők beállítása árazási dimenziókként
description: Ez a témakör az egyedi árazási dimenziók egyéni mezőkkel történő beállításáról nyújt információkat.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896599"
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

Az erőforrás munkaidejét (**msdyn_resourceworkhours**) árrésalapú dimenzióként adták hozzá, és a **Feláron alapuló árképzési dimenzió** lapon a rácshoz adták.

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
|             | Contoso USA   |Helyi             |                    |Túlóra                 |20     |


Ha a 100 USD alapdíjat használó Contoso India erőforrása működik a helyszínen, és napi 8 óra normál munkaidőt és 2 óra túlórát jelentenek az időbejegyzéshez, akkor az árképzési motor a 100-as alapdíjat használja a 8 órához, így 800 USD értéket rögzít. A 2 órás túlórára 15%-os felárat kell alkalmazni a 100-as alapárra, hogy 115 USD egységárhoz jussanak, és a teljes költség 230 USD lesz.

### <a name="applicable-to-cost"></a>Költségre alkalmazható 
Ha ezt **Igen**-re állítja , ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörár**és **Szerepkör felár** összeegyeztetéséhez, amikor a költségeket és a felárarányokat lekérdezi.

### <a name="applicable-to-sales"></a>Értékesítésre alkalmazható
Ha ez az **Igen**-re van állítva, akkor ez azt jelzi, hogy a bemeneti kontextusban szereplő dimenzióértéket kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a számla és a felárarány lekérésekor.

### <a name="applicable-to-purchase"></a>Vásárlásra alkalmazható
Ha ezt **Igen**-re állítja, ez azt jelzi, hogy a bemeneti kontextus dimenzióértékét kell használni a **Szerepkörát** és **Szerepkör felár** összeegyeztetéséhez a vételár lekérdezésekor. Az alvállalkozói forgatókönyvek nem támogatottak, így ezt a mezőt nem használja a rendszer. 

### <a name="priority"></a>Prioritás
A dimenzió prioritásának meghatározása abban az esetben is segít az árképzésben, ha nem található pontos egyezés a bemeneti dimenziók értékei és a **Szerepkörár** vagy a **Szerep felár** táblázat értékei között. Ebben a forgatókönyvben a rendszer a súlyok fontossági sorrendben történő megmérésével null értékeket fog használni a nem egyező dimenziók értékeihez.

- **Költségprioritás**: A dimenzió költség prioritásának értéke jelzi annak dimenzióját, amikor összeegyeztetik a költségárakkal. A **Költségprioritás** értékének egyedinek kell lennie, a **Költségre alkalmazható** dimenziókban.
- **Értékesítési prioritás**: A dimenzió eladási prioritása értéke jelzi ennek a dimenziónak a súlyát, amikor egyeztetik az eladási árak vagy a számlázási tarifák beállításával. Az **Értékesítési prioritás** értékének egyedinek kell lennie, az **Értékesítésre alkalmazható** dimenziókban.
