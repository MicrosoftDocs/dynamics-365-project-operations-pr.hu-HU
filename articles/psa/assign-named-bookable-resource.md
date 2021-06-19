---
title: Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése
description: Ez a témakör információt nyújt a nevesített erőforrásoknak a projektcsoportokhoz való foglalásáról, és a feladatokhoz való hozzárendeléséről.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009349"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nevesített erőforrást úgy adhat hozzá a projektcsoporthoz, ha közvetlenül a csoporthoz foglalja le azt. Ehhez hajtsa végre az alábbi műveleteket.

1. A Project Service Automation programban lépjen a **Projektek** elemre, majd válassza ki azt a projektet, amelyhez a foglalást végzi.
2. A **Projekt** oldal **Csoport** lapján kattinton az **Új** lehetőségre. 

![Csoporttag hozzáadása a csoport lapról](media/RM-how-to-1.png)

3. Válassza ki a foglalható erőforrást a **Csoporttag gyors létrehozása** párbeszédablabkan. Ha van alapértelmezett szerepkör hozzárendelve az erőforráshoz, az a **Szerepkör** mezőben látható. Szükség esetén a szerepkör módosítható. 
4. Válassza ki, hogy az erőforrásra melyik dátumok között lesz szüksége, majd az erőforrás kapacitásának felosztási módját. 
5. Ha szeretné, hogy egy csoporttag projektjóváhagyó legyen , válassza az **Igen** lehetőséget a **Projektjóváhagyó** mezőben. Ez azt jelenti, hogy a csoporttag jóváhagyhatja a projekt beküldött idő- és költségbejegyzéseit. 
6. Kattintson a **Mentés** gombra.

![Csoporttag hozzáadása a Gyors létrehozás űrlapon](media/RM-how-to-2.png)


Ezután a foglalt erőforrást hozzárendelheti a projekthez kapcsolódó feladatokhoz. Az új erőforráshoz feladatokat rendelhet hozzá, ehhez a **Projekt** lapon kattintson az **Ütemezés fülre**. A feladat rács **Erőforrás** mezőjéből indítható erőforrás-választó a kiválasztható csoporttagokat jeleníti meg.

![Csoporttag hozzárendelése egy feladathoz az Ütemezés lapon](media/RM-how-to-3.png)

Project Service Automation (PSA) 3. verziójában az erőforrás-foglalás és a feladatok hozzárendelése nem párosul szorosan. Ez azt jelenti, hogy ha az erőforrás-választót használja az ütemezésben, akkor a munkacsoport tagjaihoz több óráig is hozzárendelheti a feladatokat, mint a projekten végzett foglalások időfedezete.
A csoporttagok foglalásai és a hozzárendelések közötti különbségeket a **Csoport** vagy az **Erőforrás-egyeztetések** lapon tekintheti meg. A foglalások és az erőforrás-hozzárendelések közötti különbségeket részletesebb szinten is egyeztetheti.

![Erőforrás-egyeztetés lap](media/RM-how-to-4.png)

Az **Ütemezés** lapról elérhető erőforrás-választóval is megkeresheti és kijelölheti azokat a foglalható erőforrásokat, amelyek még nem szerepelnek a projektcsoportban. Ezek az erőforrás-választóban az **Egyéb erőforrások** részen jelennek meg.

![Nem csoporttag erőforrás hozzárendelése egy feladathoz](media/RM-how-to-5.png)

Ennek használatával az erőforrás hozzáadódik a projektcsoporthoz, és hozzárendelésre kerül a feladathoz, de a rendszer nem hoz létre foglalást.

![Csoporttag hozzárendelésekkel, foglalások nélkül](media/RM-how-to-6.png)

Az **Egyeztetés** lapon a Foglalás meghosszabbítása funkció, vagy az **Ütemezési tábla** használatával foglalhatja le az erőforrás kapacitását a projekt számára.

![Csoporttag foglalásainak meghosszabbítása az Erőforrás-egyeztetés lapon](media/RM-how-to-7.png)

Miután egy csoporttag foglalásra került a projekhez, használhatja a Foglalások karbantartása funkciót, vagy az Ütemezési tábla használatával közvetlenül kezelheti annak foglalásait.


[!INCLUDE[footer-include](../includes/footer-banner.md)]