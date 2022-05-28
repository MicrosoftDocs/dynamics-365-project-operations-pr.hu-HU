---
title: Projektsablon létrehozása
description: Projektsablon létrehozása a Project Service szolgáltatásban
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 127b6e43a15f19a42791e78b55865ab11ca50c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598997"
---
# <a name="create-a-project-template-project-service"></a>Projektsablon létrehozása (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

A projektsablonokkal időt takaríthat meg, ha a vállalat rendszeresen tesz ajánlatot hasonló típusú projektekre. Egy bizonyos típusú projekthez standard szerepeket és becsült órákat nyújt. A fiókmenedzserek és a projektmenedzsereket létrehozhatnak projekteken alapuló sablonokat, vagy másolhatnak egy sablont, és létrehozhatják a sajátjukat.  
  
## <a name="components-of-project-template"></a>Projektsablon összetevői
 A projektsablon három összetevőből áll:  
  
- **Munkalebontási szerkezet**: A munkalebontási szerkezet egy projektsablonban ugyanazokat az elemeket tartalmazza, mint a projekt. Létrehozhat feladathierarchiát, kioszthat szerepeket feladatokhoz, meghatározhat ütemezési attribútumokat, beállíthat függőségeket és megtekinthet minden adatot a Gantt-diagramon. A projektsablonok munkalebontási szerkezete támogatja az egyes feladatok feladatmódját. Nincs különbség a projektsablon és a projekt között, amikor ütemtervet hoz létre.  
  
- **Projektbecslés**: A projektbecslések a sablonokban ugyanúgy működnek, ahogy a projektekben, kivéve, hogy a költségeket és eladási árakat meghatározó árlisták mind a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] paraméterek között megtalálható alapértelmezett költség- és eladásiár-listák. A többi funkció ugyanaz, mint egy projektben.  
  
- **Projektcsoport létrehozása**: Amikor projektcsoportot hoz létre projektsablonból, nem foglalhat le névvel rendelkező erőforrást a sablonban. A munkalebontási struktúrában használhatja a **Projektcsoport létrehozása** lehetőséget az általános erőforrások generálásához. Megadhatja a szükséges készségeket és a szakmai tapasztalatokat az általános erőforrásokhoz. Nem helyettesíthet általános erőforrást foglalható erőforrással a projektsablonokban.  
  
## <a name="create-a-project-from-a-template"></a>Projekt létrehozása sablonból  
 A következő módokon hozhat létre projektet sablonból:  
  
-   Amikor árajánlatból hoz létre projektet, kiválaszthat projektsablont a projekt gyorslétrehozási űrlapján.  
  
-   Amikor projektet hoz létre az **Új projekt** lehetőségre kattintva, megjelenik a projektűrlap a rekord mentése előtt. Innen kattintson a **Sablon kiválasztása** mezőre, hogy válasszon a vállalkozásában előre meghatározott projektsablonok közül.  
  
-   Kattintson a **Projekt létrehozása sablonból** lehetőségre a **Projektsablon** lapon, ha sablonból szeretne projektet létrehozni.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Összetevők másolása sablonból projektbe  
 Amikor összetevőt másol sablonból projektbe, van néhány dolog, amiről tudnia kell.  
  
 **Munkalebontási struktúra másolása**: Amikor munkalebontási struktúrát másol projektsablonba, ha a projektnek más a projektnaptára, mint a sablonnak, akkor a projektnaptár munkaórái a feladatok ütemezéséhez kerülnek. Ez az ütemezést a projektnaptárhoz igazítja. Ehhez hasonlóan a munkalebontási struktúrában az első feladat a projekt kezdési dátumának megadása, így a feladathierarchia ütemezésének fennmaradó része a sablon munkalebontási struktúrájában meghatározott időtartam és függőségek alapján frissül.  
  
 **Projektbecslések másolása**: Ha projektbecslési sorokat másol, az árlisták a projekt tulajdonosegységének önköltségi listája alapján frissülnek, és az ügyfél az értékesítési árlista alapján. Az egységköltség és az eladási árak az árlista alapján kerülnek meghatározásra azoknál a projekteknél, amelyek értékesítési entitással vannak összekapcsolva.  
  
 **Projektcsapat másolása**: Amikor a projektcsapatot sablonból projektbe másolja, akkor az általános erőforrásokat is másolja a rendszer a sablonban meghatározott képességekkel és szakmai tapasztalatokkal együtt. Az általános erőforrás-hozzárendelések is megmaradnak a projektsablon szerint.  
  
### <a name="see-also"></a>Kapcsolódó információk  
 [Projektmenedzseri útmutató](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
