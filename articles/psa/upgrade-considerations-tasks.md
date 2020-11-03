---
title: Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat
description: Ez a témakör a munka bontási struktúrájának a Project Service Automation 2.x-ről a 3.x-re történő frissítéséről nyújt információkat.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078174"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat
Ez a témakör a munka bontási struktúrájának a Project Service Automation 2.x-ről a 3.x-re történő frissítéséről nyújt információkat. Ez a témakör a sikeres frissítéshez szükséges Project Service Automation (PSA) projekt egészségi állapotát határozza meg. Információ van a közös blokkolási körülményekről is, amelyek miatt a frissítés meghiúsul. A projektfeladatok és azok funkcióinak a projektütemezésen belüli meghatározásáról lásd: [Projektütemezések](project-creating.md).

## <a name="key-entities"></a>Kulcsfontosságú entitások
A pontos, az erőforrásokkal már megterhelt munka bontási struktúrához a következő entitások szükségesek:

- [Projekt](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektcsoport](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektfeladat](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Erőforrás-hozzárendelések](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projektfeladat függősége](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Lefoglalható erőforrások](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Az erőforrások által betöltött munka bontási struktúrájának meghatározásához a következő lépéseket kell végrehajtania:

1. Hozzon létre egy új projektet. További információ az új projekt létrehozásáról: [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Hozzon létre egy vagy több feladatot. A feladat létrehozásával kapcsolatos további információkért lásd: [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Határozza meg a feladat függőségeit. További információ a [Projektfeladat függősége](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency) című témakörben olvasható.
4. Jelölje ki a projekt csapattagjait. További információ: [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Jelölje ki a projektcsoport tagjait a feladatokhoz. További információ: [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projektcsapat-kapcsolatok

A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:
- A projektcsoport összes tagját hozzárendelni kell foglalható forráshoz.
- A projektcsoport összes tagját azonos projekthez kell társítani. 

## <a name="project-task-relationships"></a>Projekt feladat kapcsolatok
A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:

- Minden kapcsolódó feladatot ugyanahhoz a projekthez kell társítani.
- Minden sorfeladatnak szülői feladattal kell rendelkeznie.
- Minden feladatnak tartalmaznia kell egy szülői projektet.

### <a name="valid-conditions"></a>Érvényes feltételek

- Az összes feladat időtartamának legalább egy óránnak (>=) vagy azzal egyenlőnek kell lennie, és kevesebbnek kell lennie 1 800 000 percnél (1250 nap).*
- Minden feladatnak legkorábban 2000/01/01 kezdő dátummal kell rendelkeznie.*
- Minden feladatnak legkésőbb a mai naptól számított 17 éven belüli kezdő dátummal kell rendelkeznie.*
- Minden feladatnak a kezdési dátummal korábban vagy azzal egyenlőnek kell lennie.
- Az osztályozásban szereplő összes tranzakciótípusnak (költség, anyag, adó és idő) a következőknek kell lennie: **Alapértelmezett egység** és **Egységcsoport**.
- Kerülni kell a betűkkel ellátott dátumformátumot.

### <a name="potential-mitigation-steps"></a>Potenciális kockázatcsökkentési lépések
- Az Irányított keresés segítségével azonosíthatja projektazonosítót nem tartalmazó projekttevékenységeket.
- Az Irányított keresés segítségével azonosíthatók azok a projekttevékenységek, amelyeknél az ütemezett időtartam nagyobb, mint 1 800 000.
- Az adatok módosítása előtt meg kell vizsgálnia az entitáshoz kapcsolódó testreszabásokat, amelyek ahhoz vezethettek, hogy az adatok hibás állapotba kerültek. Ezeket a testreszabásokat kezelni kell az adatokkal kapcsolatos bármilyen frissítések végrehajtása előtt.
- Az azonosított árva feladatok esetében érdemes lehet törölni ezeket a feladatokat, ha nem szükségesek, vagy a megfelelő fölérendelt projekthez kell azokat társítani.
- Minden olyan feladat esetében, ahol az időtartam nagyobb, mint 1250 nap, érdemes több feladatot is felvenni, amelyek kitöltik a teljes időtartamot, ha ez megoldható.

> [!NOTE]
> A csillaggal (\*) megjelölt elemeknek vannak olyan korlátai, amelyek annak a ténynek a következményei, hogy az ügyfélkapcsolat-kezelés (CRM) csak 7320 ismétlődési kiterjesztést támogat. Ezen határ alatt kell maradnia.

## <a name="resource-assignment-relationships"></a>Erőforrás-hozzárendelési kapcsolatok
A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:

- A munkabontási struktúrában szereplő összes erőforrás-hozzárendelésnek ugyanabba a projekthez kell kapcsolódnia.
- A munkabontási struktúrában szereplő összes erőforrás-hozzárendelést társítani kell a projektcsoport tagjaihoz ugyanabban a projektben.

### <a name="potential-mitigation-steps"></a>Potenciális kockázatcsökkentési lépések
- Azonosítsa az összes olyan feladatot, amely kívül esik a fent leírt feltételeken.  
- A már nem érvényes erőforrás-hozzárendeléseket törölni kell.

## <a name="project-task-dependency-relationships"></a>Projektfeladat-függőségi viszonyok
A sikeres frissítés biztosításához a következő kapcsolatokat kell megfelelően fenntartani:

- Az összes projektfeladat-függőségnek ugyanahhoz a projekthez kell kapcsolódnia.
- Egy feladatnak nem lehet ugyanaz a függősége, többször hivatkozva.
