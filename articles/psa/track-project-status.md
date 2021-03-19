---
title: Projektállapot nyomon követése
description: Projekt állapotának nyomkövetése a Project Service szolgáltatásban
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281931"
---
# <a name="track-a-projects-status-project-service"></a>Projekt állapotának nyomkövetése (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

A [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] használatával nyomon követhető egy ügyfél projektjének fejlődése.  

Az ügylet előrehaladásával a projekt fázisai frissülnek, hogy tükrözzék az ügylet fázisát:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Új**    | A projekt létrehozásakor a fázis értéke az **Új**. Ha a projektet egy sablonból hozta létre, akkor a projekt ebben a fázisban rendelkezhet ütemezéssel, becslésekkel és a csoportadatokkal. Ellenkező esetben a projekt vázlata lesz, és manuálisan kell megadni a többi projekt-összetevőt. |
|  **Ajánlat**   |      Amikor egy árajánlathoz társít egy projektet, vagy egy árajánlatból hozza azt létre, a projekt fázisa **Árajánlat** lesz, és frissülnek a becsült kezdési és befejezési dátumok is. Amikor a projekt az árajánlati fázisban tart, az árajánlat részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.      |
|   **Terv**   |                                     Amikor nyer egy projekthez társított árajánlattal, és az ügylet eléri a szerződés fázist, a projekt fázis a **Terv** fázisra frissül. A szerződés részletei a **Sales** lapon jelennek meg, a **Projekt** oldalon.                                      |
| **Teljes** |                    Amikor a projekten végzett munka véget ért, módosíthatja a fázist **Befejezettre**. Ha a projektfázis értéke befejezett, az azt jelenti, hogy a munka 100%-át sikerült elvégezni, de a projekt még nyitott, hogy meg lehessen adni az esetlegesen még függő idő- és kiadásbejegyzéseket.                     |
|  **Bezárás**   |           Amikor a projekthez tartozó minden tranzakció rögzítésre került, és nem várja továbbiak naplózását, akkor manuálisan beállíthatja a fázist **Lezártra**. Ha a projekt fázisa **Lezárt**, nem rögzíthet további tranzakciókat a projekthez, és a projekt csak olvasható lesz.           |

## <a name="to-track-a-projects-status"></a>Projektállapot követése  

1.  Lépjen a **Project Service > Projektek** pontba.  

2.  Kattintson arra a projektre, amellyel dolgozni szeretne.  

3.  A képernyő felső részén található sávon válassza ki a projekt neve melletti lefelé mutató nyilat, majd kattintson a **Projektkövetés** lehetőségre.  

4.  Válassza a **Ráfordításkövetés** vagy a **Költségkövetés** lehetőséget a legördülő listában a feladatlista felett.  

5.  Kattintson duplán a szerkeszteni kívánt feladatra. Áthelyezheti vagy átméretezheti az Gantt-diagram oszlopait, ha módosítani akarja egy feladat idejét és előrehaladását.  

### <a name="see-also"></a>Kapcsolódó információk  
 [Projektmenedzseri útmutató](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]