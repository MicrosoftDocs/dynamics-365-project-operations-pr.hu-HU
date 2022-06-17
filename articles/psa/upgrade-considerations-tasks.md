---
title: Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat
description: Ez a cikk a munkalebontási struktúra Project Service Automation 2.x-ről 3.x-re történő frissítéséről nyújt tájékoztatást.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 42bf03b5e3be4b7bdce87148254ce69e381ffdf1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913117"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Frissítse a munka lebontási struktúrájával kapcsolatos szempontokat

[!include [banner](../includes/psa-now-project-operations.md)]

Ez a cikk a munkalebontási struktúra Project Service Automation 2.x-ről 3.x-re történő frissítéséről nyújt tájékoztatást. Ez a cikk a projekt kifogástalan állapotát határozza meg a Project Service Automationben (PSA) a sikeres frissítéshez szükséges. Információ van a közös blokkolási körülményekről is, amelyek miatt a frissítés meghiúsul. A projektfeladatok és azok funkcióinak a projektütemezésen belüli meghatározásáról lásd: [Projektütemezések](project-creating.md).

## <a name="key-entities"></a>Kulcsfontosságú entitások
A pontos, az erőforrásokkal már megterhelt munka bontási struktúrához a következő entitások szükségesek:

- [Projekt](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektcsoport](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektfeladat](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Erőforrás-hozzárendelések](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projektfeladat függősége](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Lefoglalható erőforrások](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Az erőforrások által betöltött munka bontási struktúrájának meghatározásához a következő lépéseket kell végrehajtania:

1. Hozzon létre egy új projektet. További információ az új projekt létrehozásáról: [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Hozzon létre egy vagy több feladatot. A feladat létrehozásával kapcsolatos további információkért lásd: [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Határozza meg a feladat függőségeit. További információ a [Projektfeladat függősége](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency) című témakörben olvasható.
4. Jelölje ki a projekt csapattagjait. További információ: [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Jelölje ki a projektcsoport tagjait a feladatokhoz. További információ: [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
