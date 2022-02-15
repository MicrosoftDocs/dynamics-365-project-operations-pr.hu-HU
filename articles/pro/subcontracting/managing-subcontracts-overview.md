---
title: Alvállalkozói szerződések kezelése Project Operations-ben
description: Ez a téma áttekintést nyújt a projektalapú szervezeteknél jellemzően végponttól végpontig tartó alvállalkozói szerződéskezelési folyamatról.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323599"
---
# <a name="subcontract-management-in-project-operations"></a>Alvállalkozói szerződések kezelése Project Operations-ben

[!include [banner](../../includes/dataverse-preview.md)]

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a téma áttekintést nyújt a projektalapú szervezetek alvállalkozói szerződések teljes körű menedzsment folyamatáról. A szolgáltatások alvállalkozásba adása jellemzően az alábbi ábrán látható üzleti folyamatok folyamatát követi.

![Alvállalkozói folyamat](../media/SubcontractingProcessFlow.png)

Az alábbi lista lépésről lépésre ismerteti az alvállalkozói szerződéskötési folyamatot.

1. A projektvezető alvállalkozói szerződést hoz létre egy alvállalkozóval. Alapértelmezés szerint a szállítói rekordhoz csatolt árlistákat használja a rendszer az alvállalkozóhoz. A szállítói fióknak egy **Szállító** vagy **Beszállító** kapcsolattípusa van.
2. A projektmenedzser az alvállalkozónál minden vásárlást sorelemként felszámíthat. Az alvállalkozósorok időre, kiadásokra vagy termékekre vonatkoznak. Az alvállalkozói szerződéssor tranzakciós osztálya határozza meg, hogy mire szolgál a sor.
3. A szállítói account manager és a projektmenedzser meg tud iterálni az alvállalkozói szerződésen. Az árképzés korrigálható a beszerzési árlistákon, amelyek csatolva vannak az alvállalkozói szerződéshez.
4. Ezen a ponton vagy a folyamat későbbi szakaszában, ha az alvállalkozói szerződéssor időre szól, a szállítói számlavezető minden egyes alvállalkozói szerződéssorhoz hozzárendeli a szállítói kapcsolatokat. Ez a társítás az alvállalkozóval dolgozó projektmenedzser számára nyújt tájékoztatást. Amikor egy alvállalkozói szerződéssorhoz egy szállítói kapcsolat kapcsolódik, a rendszer automatikusan létrehoz egy foglalható erőforrást a kapcsolatból, ha még nem létezik foglalható erőforrás.
5. Az egyes alvállalkozói sorok számlázási módja lehet **Rögzített árú vagy** **Idő és anyag**. A fix áras alvállalkozói szerződéses sorok esetében mérföldkő-alapú számlázási ütemterv kerül felállításra.
6.  Miután az alvállalkozói szerződés létrejön és a tárgyalások lezárultak, azt megerősítik. A megerősített alvállalkozói szerződéseket nem lehet szerkeszteni, de ha változások történnek, az alvállalkozói szerződés „újranyitható szerkesztésre”, ami a státuszt a **Megerősítettről** visszaállítja a **Tervezetre**, és a tárgyalást újra meg lehet nyitni. 
7.  Amikor egy projektben általános csoporttagot hoz létre, a csoporttagot egy alvállalkozói szerződéssorhoz is hozzárendelheti. Ez azt jelzi, hogy az általános csoporttagot alvállalkozói kapacitással kell ellátni.
8.  Nevezett csapattagokat közvetlenül egy projektben hozhat létre, vagy az erőforrás-ütemezéssel kapcsolatos tapasztalatok segítségével történő foglalással hozhatja létre őket. Ha egy megnevezett projektcsapat tagja szerződéses munkavállaló, akkor ezt egy alvállalkozói sorhoz lehet társítani. Ez csökkenti a rendelkezésre álló kapacitást egy alvállalkozói vonalon.
9.  Az alvállalkozói erőforrások naplózhatják a projektek és projektfeladatok idejét, költségeit és anyagfelhasználását, majd jóváhagyásra benyújthatják. Ez a munkavállalók esetében is hasonló. Az idő nyilvántartásakor a szerződéses munkavállaló kiválaszthat egy adott alvállalkozót és alvállalkozói sort.
10. A jóváhagyást követően az alvállalkozói szerződések által jóváhagyott idő a projekt tényleges költségeit a szerződéses munkavállaló beszerzési ára vagy a projektben betöltött szerepe alapján rögzíti.
11. A szállítói számlák és szállítói számlatételek rögzíthetők a rendszerben a szállítói erőforrások által elvégzett munkáról vagy a szállító által szállított termékekről. A szállítói számlasoroknak egy adott projektre kell vonatkozniuk, és az idő, költség, termék/anyag, mérföldkő vagy díj tranzakciós osztályra kell vonatkozniuk. Opcionálisan a szállítói számlasorok hivatkozhatnak alvállalkozói szerződéssorra.
12. A rendszer automatikusan hozzárendeli a szállítói számlához az összes olyan tényleges költséget, amely megfelel az alvállalkozói szerződés sorának és a projektnek. Ez megkönnyíti a 3-irányú egyeztetési és ellenőrzési folyamatot.
13. A projektmenedzser ezután felülvizsgálhatja az automatikusan illesztett tényleges projektköltségeket, eltávolíthat vagy hozzáadhat más tényleges projektköltségeket, és befejezheti az ellenőrzési folyamatot.
14. Ha az ellenőrzési folyamat minden soron befejeződik, a szállítói számla **kifizetésre késznek** minősül. Ebben a szakaszban a szállítói számla és a sorok átvihetők a könyvelési vagy fizetési rendszerbe, hogy feldolgozzák a szállítónak történő kifizetést. A korábban rögzített projektköltségeket vissza kell vonni, és a szállítói számla soron szereplő tényleges költségeket kell rögzíteni a projektben.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Mennyiségalapú alvállalkozói szerződéssorok és munkaalapú alvállalkozói szerződéssorok

Az alvállalkozói szerződéssor lehet mennyiségi vagy munkaalapú. 

Ha egy alvállalkozói szerződéssor **mennyiségi alapú**, az alvállalkozói szerződéssoron időre, költségre vagy anyagra vásárolt mennyiség bármely projektben felhasználható.

Ha egy alvállalkozói szerződés sora **munkaalapú**, az alvállalkozói szerződés sora a projekttervben egy csomópont által képviselt munkarészhez tartozik. Az alvállalkozói szerződéssor értéke az adott munkarész teljesítéséhez szükséges összes komponens összege. Ezeket alvállalkozói szerződéssor részleteiként modellezik, és lehetnek idő-, költség- vagy anyaggyűjtemények. Munkán alapuló alvállalkozói szerződéssor esetében az alvállalkozói szerződéssor szintén egyetlen projekthez van rendelve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
