---
title: Frissítéssel kapcsolatos szempontok – frissítés a Microsoft Dynamics 365 Project Service Automation 2.x vagy 1.x verzióról a 3. verzióra
description: Ez a témakör információkat nyújt azokról a szempontokról, amelyeket mérlegelnie kell, amikor a Project Service Automation 2.x vagy 1.x verziójáról a 3-as verzióra frissít.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b29ef5d6d2c1c97658d79bbbe82e5893adeafe4d20354e90058dde79b67cb716
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000084"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Frissítési szempontok - A PSA 2.x vagy 1.x verziója a 3. verzióra

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation és Field Service
A Dynamics 365 Project Service Automation és a Dynamics 365 Field Service is a Universal Resourcing Scheduling (URS) megoldást használja az erőforrás-ütemezéshez. Ha Project Service Automation és a Field Service megoldások vannak a példányában, akkor mindkét megoldást frissítenie kell a legújabb verzióra. A 3.x verziójú Project Service Automation-höz. A Field Service esetében ez a 8.x verzió. A Project Service Automation vagy a Field Service frissítése telepíteni fogja az URS legújabb verzióját. Ha a Project Service Automation és a Field Service megoldások ugyanabban a példányban nem frissülnek a legújabb verzióra, annak valamilyen inkonzisztens viselkedés lehet az oka.

## <a name="resource-assignments"></a>Erőforrás-hozzárendelések
A Project Service Automation 2. és 1. verziójában a feladat-hozzárendeléseket gyermekfeladatokként (más néven sori feladatokként ) tárolták a **Feladatentitásban**, és közvetetten kapcsolódtak az **Erőforrás-hozzárendelés** entitáshoz. A sori feladat látható volt a munkalebontási struktúra (WBS) hozzárendelés előugró ablakában.

![Sorfeladatok a WBS-ben a Project Service Automation 2. és 1. verziójában.](media/upgrade-line-task-01.png)

A Project Service Automation 3. verziójában megváltozott a foglalható erőforrások feladatokhoz rendelésének alapjául szolgáló séma. A sori feladat már elavult, és van egy közvetlen 1:1 kapcsolat a feladatot a **Feladatentitás** és a csapat tagja az **Erőforrás-hozzárendelés** entitás között. A projektcsoport tagjaihoz rendelt feladatokat most közvetlenül az erőforrás-hozzárendelés entitás tárolja.  

Ezek a változások befolyásolják minden meglévő projekt frissítését, amelyhez a projektcsoportban megnevezett foglalható erőforrásokhoz és általános erőforrásokhoz vannak hozzárendelve erőforrás-hozzárendelések. Ez a témakör azokat a szempontokat tartalmazza, amelyeket figyelembe kell vennie a projekteknél, amikor a 3. verzióra frissít. 

### <a name="tasks-assigned-to-named-resources"></a>A megnevezett erőforrásokhoz rendelt feladatok
Az alapul szolgáló feladat entitás felhasználásával a 2. és az 1. verzió feladatai lehetővé tették a csapat tagjai számára, hogy az alapértelmezésben meghatározott szerepüktől eltérő szerepet is ábrázoljanak. Például Gracie George-ot, aki alapértelmezés szerint a programmenedzser szerepét kapta, hozzá lehet rendelni egy Fejlesztői szereppel bíró feladathoz. A 3. verzióban a megnevezett csapattagok szerepe mindig az alapértelmezés, tehát minden olyan feladat, amelyre Gracie George hozzá van rendelve, Garcie a programkezelő alapértelmezett szerepét használja.

Ha a 2. és az 1. verzióban az erőforrást az alapértelmezett szerepükön kívüli feladatokhoz rendelt, akkor a megnevezett erőforrás az összes feladat-hozzárendeléshez alapértelmezett szerepet kap, függetlenül a 2. verzióbeli szerepkör-hozzárendeléstől. Ez a hozzárendelés eltéréseket fog eredményezni a kiszámított becslésekben a 2. vagy 1. verzióról a 3. verzióra, mivel a becsléseket az erőforrás szerepe alapján számítják ki, nem pedig a sor feladat hozzárendelése alapján. Például a 2. verzióban két feladatot rendeltek Ashley Chinn-hez. Az 1. feladat online feladatában a Fejlesztő és a 2. feladatban a Programkezelő szerepe van. Ashley Chinn alapértelmezett szerepe a Programmenedzser.

![Több erőforrás hozzárendelve egy erőforráshoz.](media/upgrade-multiple-roles-02.png)

Mivel a fejlesztő és a programmenedzser szerepei különböznek, a költség- és eladási becslések a következők:

![Az erőforrás-szerepek költségbecslései.](media/upggrade-cost-estimates-03.png)

![Értékesítési becslések az erőforrás-szerepekhez.](media/upgrade-sales-estimates-04.png)

A 3. verzióra való frissítéskor a sorfeladatok helyébe erőforrás-hozzárendelések kerülnek, amelyeket a foglalható erőforrás-csoport tagja végez. A hozzárendelés a foglalható erőforrás alapértelmezett szerepét fogja használni. A következő ábrán Ashley Chinn van, aki Programmenedzser szerepet tölt be.

![Erőforrás-hozzárendelések.](media/resource-assignment-v2-05.png)

Mivel a becslések az erőforrás alapértelmezett szerepén alapulnak, az értékesítési és költségbecslések változhatnak. A következő ábrán már nem látja a **Fejlesztő** szerepet, mivel a szerep most a foglalható erőforrás alapértelmezett szerepéből származik.

![Alapértelmezett szerepek költségbecslése](media/resource-assignment-cost-estimate-06.png)
![Alapértelmezett szerepek eladási becslése.](media/resource-assignment-sales-estimate-07.png)

A frissítés befejezése után szerkesztheti a csapattagok szerepét úgy, hogy az eltérjen a hozzárendelt alapértelmezettől. Ha azonban megváltoztatja a csapattagok szerepét, akkor az megváltozik minden hozzárendelt feladatban, mivel a 3. verzióban a csapattagoknak nem osztható ki több szerepkör.

![Erőforrás szerep frissítése.](media/resource-role-assignment-08.png)

Ugyanez vonatkozik a megnevezett erőforrásokhoz rendelt vonali feladatokra is, amikor az erőforrás szervezeti egységét alapértelmezettről egy másik szervezeti egységre változtatja. Miután a 3. verzió frissítése befejeződött, a hozzárendelés az erőforrás alapértelmezett szervezeti egységét fogja használni a vonali feladatban beállított egység helyett.

### <a name="tasks-assigned-to-generic-resources"></a>Általános erőforrásokhoz rendelt feladatok
A 2. és az 1. verzióban beállíthatja a feladat szerepét és az szervezeti egységet, majd a **Csapat létrehozása** funkció segítségével generálhat általános erőforrásokat a feladaton beállított attribútumok alapján. A 3. verzióban létrehozza az általános csapattagokat szerep- és szervezeti egységgel, majd a csoporttagokat feladatokhoz rendeli.

A 2. és az 1. verzióban az általános erőforrásokkal rendelkező projektek két állapotban lehetnek, vagy a feladat szintjén mindkettő keveréke lehet. Például a következő forgatókönyvek lehetnek:

- Feladatok, ahol szerepek és szervezeti egységek vannak beállítva, de nem jött létre kapcsolt erőforrás-hozzárendelés.
- Feladatok általános csapattag-erőforrás-hozzárendelésekkel, amelyeket általános erőforrás létrehozásával rendeltek hozzá a **Csapat generálása** szolgáltatás segítségével.

A frissítés megkezdése előtt azt javasoljuk, hogy hozza létre a csoportot minden olyan projekthez, amelynek általános erőforrásokhoz rendelt feladatai vannak, vagy még nem kell futtatniuk a generáló csoport folyamatát.

Az általános csoporttagokhoz rendelt olyan feladatok esetében, amelyeket a **Csapat generálása** segítségével hoztak létre, a frissítés az általános erőforrást hagyja a csapaton, és a hozzárendelést az adott csoporttagnak hagyja. Javasoljuk, hogy a frissítés után, de mielőtt lefoglalja vagy benyújt egy erőforrás-kérelmet, generáljon erőforrás-igényt az általános csapattag számára. Ez megőrzi az általános csoporttagoknak a projekt szerződéses szervezeti egységétől eltérő szervezeti egységekhez rendelt feladatait.

Például a Project Z projektben a szerződéses szervezeti egység a Contoso US. A projekttervben a végrehajtási szakaszon belüli tesztelési feladatokra technikai tanácsadó szerepet kaptak, és a kijelölt szervezeti egység a Contoso India.

![Végrehajtási szakasz szervezeti hozzárendelés.](media/org-unit-assignment-09.png)

A megvalósítási szakasz után az integrációs teszt feladatot a Műszaki tanácsadó szerephez rendelik, de az org értéke Contoso US.  

![Integrációs teszt feladat org hozzárendelés.](media/org-unit-generate-team-10.png)

Amikor létrehoz egy csapatot a projekthez, akkor két általános csoporttagot hoznak létre a feladatok különböző szervezeti egységei miatt. Az 1. műszaki tanácsadó a Contoso India feladatait, a 2. műszaki tanácsadó pedig a Contoso USA feladatait kapja.  

![Generált generikus csapattagok.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> A Project Service Automation 2. és 1. verziójában a csapat tagja nem tartja a szervezeti egységet, amelyet a vonali feladatban tartanak fenn.

![2. verziós és 1. verziós sorfeladatok a Project Service Automation megoldásban.](media/line-tasks-12.png)

A becslések nézetben láthatja a szervezeti egységet. 

![Org egység becslések.](media/org-unit-estimates-view-13.png)
 
A frissítés befejezése után az általános csapattagnak megfelelő vonali feladatban lévő szervezeti egységet hozzáadják az általános csapattaghoz, és a vonali feladatot eltávolítják. Emiatt azt javasoljuk, hogy a frissítés előtt hozzon létre vagy generálja újra a csoportot minden olyan projekthez, amely általános erőforrásokat tartalmaz.

Az olyan feladatok esetén, amelyeket egy olyan szerv-egységgel rendelnek hozzá, amely eltér a szerződéses projekt szervezeti egységétől, és nem alakult ki egy csapat, az frissítés általános csoporttagot hoz létre a szerephez, de a projekt a csapattag szervezeti egységéhez. Visszatérve a Z Projekt példájára, ez azt jelenti, hogy a Contoso US szerződéses szervezeti egységet és a megvalósítási szakaszban lévő projektterv-tesztelési feladatokat a Contoso Indiához rendelt szervezeti egységgel műszaki tanácsadóként látják el. Az integrációs teszt feladat, amely a végrehajtási szakasz után fejeződik be, a Műszaki tanácsadó szerepkörbe kerül. Az org egység Contoso USA, és nem hoztak létre csapatot. A Frissítés létrehoz egy általános csoporttagot, egy műszaki tanácsadót, akinek mindhárom feladat kijelölt órája van, és a Contoso USA szervezeti egységét, a projekt szerződéses szervezeti egységét.   
 
A különféle erőforrás-ellátó szervezeti egységek alapértelmezett értékének megváltoztatása a nem létrehozott csoporttagoknál az az oka, hogy a frissítés előtt generáljunk vagy generáljunk újból minden olyan projektet, amely általános erőforrásokat tartalmaz, hogy az org egység-hozzárendelések ne vesszenek el.



[!INCLUDE[footer-include](../includes/footer-banner.md)]