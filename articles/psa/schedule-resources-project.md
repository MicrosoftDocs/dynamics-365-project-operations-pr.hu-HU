---
title: Erőforrások ütemezése egy projekthez
description: Erőforrások ütemezése projekthez a Project Service szolgáltatásban
author: JohnPBurrows
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583127"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Erőforrások ütemezése projekthez (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ellenőrizheti az erőforrás-elérhetőséget, hogy átfogó képet kapjon az erőforrások foglaltságáról, vagy szűrheti a megjelenített elemeket képzettségek, csapat, hely és egyéb beállítások szerint.  
  
Az ütemezési táblán az erőforrások és az elérhetőségük látható. Rendelkezésre állás megjelenítése módjának kiválasztása: **óra**, **nap**, **hét**, vagy **hónap**.  
  
Az ütemezés beállítása előtt fontos beállítani. További információ: [Ütemezési tábla konfigurálása (Field Service vagy Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Régebbi verziójú rendszer használata esetén az erőforrások rendelkezésre állásához lásd: [Az erőforrás rendelkezésre állásának megtekintése](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Az ütemezésitábla-foglalás funkcióhoz, a geokódoláshoz és a helyszolgáltatásokhoz be kell kapcsolni a Térképet.  
> 
> 1. Válassza a főmenüben az **Erőforrás-ütemezés** > **Adminisztráció** lehetőséget.  
> 2. Kattintson az **Ütemezési paraméterekre**.  
> 3. Nyissa meg a rekordot, és görgessen le a **Resource Scheduling Optimization** szakaszhoz.  
> 4. A **Csatlakozás a Térképhez** mezőben válassza az **Igen** lehetőséget.  
> 5. Hagyja jóvá a feltételeket és mentse el a rekordot.  
> 6. A főmenüben válassza a **Project Service** > **Ütemezési táblázat** lehetőséget. Innen többféle módon lehetséges egy foglalási követelményt manuálisan ütemezni. Válassza ki az Ön számára megfelelő módot.
  
## <a name="find-available-resources"></a>Elérhető erőforrások keresése

1.  A **Foglalási követelmény**-listán kattintson jobb gombbal egy nem ütemezett foglalásra és válasszon az alábbiak közül:  
  
- Válassza a **Rendelkezésre állás keresése – Aktuális erőforrások** lehetőséget rendelkezésre álló erőforrások kereséséhez a listáról az ütemezési táblán.  
- Válassza a **Rendelkezésre állás keresése – Minden erőforrás** lehetőséget rendelkezésre álló erőforrás kereséséhez a rendszerben  
   > [!NOTE]
   >  Ha ezt elvégzi, akkor a szűrők a kijelölt foglalási szükséglethez tartozó beállításokat fogják megjeleníteni.  
  
2. Amikor egy elérhető sávot lát, kattinson jobb gombbal az idősávra az ütemezési táblán, és válassza a **Foglalás itt** lehetőséget. Vagy húzza és dobja a foglalási követelést az elérhető időszeletbe.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Foglaljon le erőforrást a napi nézet segítségével, és keresse meg a kevésbé lefoglalt felhasználókat
  
1.  Az ütemezési táblán válassza a **Nézet mód** lehetőséget, majd a **Napok** menüpontot.  
  
    Ez annak a rácsnézetét mutatja, hogy hány órát foglalt naponta az erőforrás, és mely napokon szabad.  
  
2.  Kattintson az erőforrás nevére, amelyet le szeretne foglalni, majd válassza a **Lefoglalás** elemet.  
  
3.  Az **Erőforrás-lefoglalás (létrehozás)** párbeszédpanelen válassza ki azt a projektet, amelyhez az erőforrást le akarja foglalni, valamint a foglalás módját, és a kezdő és befejező időpontokat.  
  
4.  Ha kész, válassza a **Foglalás** lehetőséget.  
  
## <a name="view-to-the-schedule-board"></a>Ütemezési tábla megtekintése
  
1.  Válasszon egy nem ütemezett foglalási követelményt a listából alul.  
  
2.  Húzza a foglalási követelést egy rendelkezésre álló erőforrásba/időszeletbe az ütemezési táblázatban.  
  
3.  Ha kész, válassza a **Foglalás** lehetőséget.  
  
### <a name="additional-resources"></a>További információforrások  
 [Erőforráskezelői útmutató](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
