---
title: Project Operations telepítése és a konfigurációs adatok integrációja
description: Ez a cikk a Project Operations kettős írású leképezéseinek beállításával és konfigurálásával kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914543"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations telepítése és a konfigurációs adatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást a beállítási és konfigurációs entitásokhoz.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektszerződés, szerződéssorok és projektek

A projektszerződések, a szerződéssorok és a Dataverse projektek a Finance and Operations alkalmazásokban jönnek létre és szinkronizálódnak a rendszer a további könyvelés érdekében. Az ezekben az entitásokban lévő rekordok csak a(z) Dataverse felületen hozhatók létre és törölhetők. Ezekhez a rekordokhoz azonban hozzáadhatók olyan könyvelési attribútumok, mint az áfacsoport alapértelmezett értékei és a pénzügyi dimenziók a Finance and Operations alkalmazásokban.

  ![Projekt szerződés integrációs koncepciók.](./media/1ProjectContract.jpg)

Az értékesítési tevékenység érdeklődőinek, lehetőségeinek és árajánlatainak nyomon követése megtörténik Dataverse, és nem szinkronizálódnak a Finance and Operations alkalmazásokkal, mert ehhez a tevékenységhez nincs kapcsolódó alsóbb rétegbeli könyvelés.

A projektszerződés funkciója Dataverse létrehoz egy projektszerződés-rekordot a Finance and Operations alkalmazásokban a **Project-szerződés fejlécei (értékesítési rendelések)** táblatérképének használatával. A projektszerződés Dataverse felületre történő mentése egyben elindítja a projektszerződés ügyfél entitási rekordjának létrehozását is. Ez a rekord a Project finanszírozási forrás (msdyn **projectcontractssplitbillingrules)\_ táblatérkép használatával szinkronizálódik a** Finance and Operations alkalmazásokkal. Ez a térkép szinkronizálja a projektszerződések vevőinek kiegészítéseit, frissítéseit és törlését is. A projektszerződés-ügyfelek közötti felosztott számlázási százalékok csak a Dataverse Finance and Operations alkalmazásokban vannak elsajátítva, és nem szinkronizálódnak velük.

Miután létrehozta Dataverse a projektszerződést, a projektkönyvelő frissítheti a projektszerződés könyvelési attribútumait a Finance and Operations alkalmazásokban a Projektvezetési és könyvelési **projektszerződések** > **beállítása beállítás alapértelmezett könyvelés** > **beállítása** > **menüpontban**. A könyvelő áttekintheti az operatív projektszerződés attribútumait, például a kért szállítási dátumot és a szerződés összegét, ha kiválasztja a projektszerződés azonosítóját a Finance and Operations alkalmazásokban, amely megnyitja a kapcsolódó projektszerződés-rekordot a következőben Dataverse: .

A projektentitás szinkronizálása a Finance and Operations alkalmazásokkal a **Projects V2 (msdyn\_ projects)** táblatérkép használatával történik. A projekt könyvelője:

  - Tekintse át a Projekteket a Finance and Operations alkalmazásokban a **Projektvezetés és könyvelés** > **Minden projekt** oldalon. 
  - Frissítse a projekt könyvelési attribútumait a Finance and Operations alkalmazásokban a **Projektvezetés és könyvelés** > **Minden projekt** > **beállítása Beállítás** > **Alapértelmezett könyvelés** megjelenítése elemre kattintva.  
  - Tekintse át az operatív projektattribútumokat, például a becsült kezdési és befejezési dátumokat úgy, hogy kiválasztja a projektazonosítót a Finance and Operations alkalmazásokban, amely megnyitja a kapcsolódó projektrekordot a következő helyen:Dataverse.

A projektek a **Projekt szerződéssor** entitáson keresztül kapcsolódnak egy projektszerződéshez.

A projektszerződés-sorok létrehoznak Dataverse egy projektszerződés számlázási szabályt a Finance and Operations alkalmazásokban a **Project-szerződéssorok (salesorderdetails)** táblatérkép használatával. A számlázási módszer határozza meg a projektszerződés számlázási szabályának típusát a Finance and Operations alkalmazásokban:

  - Az idő és az anyag számlázási módjával rendelkező projektszerződés-sorok létrehozzák az idő és az anyagtípus számlázási szabályát.
  - A fix áras számlázási mód szerződéses sorok mérföldkő számlázási szabályt hoznak létre.

A projektszerződések sorait a Projektkönyvelő a Finance and Operations alkalmazásokban úgy tekintheti meg, hogy megnyitja a **Projektvezetési és könyvelési** > **projektszerződések** > **beállítása Alapértelmezett könyvelés** > **megjelenítése lehetőséget**, és áttekinti a részleteket a **Szerződés sorok** lapon. A könyvelő ezen a lapon alapértelmezett pénzügyi dimenziókat is beállíthat a rögzített árú számlázási módszer szerződéses soraihoz.

## <a name="billing-milestones"></a>Számlázási mérföldkövek

A fix áras számlázási módszert alkalmazó projektszerződések számlázása mérföldköveken keresztül történik. A számlázási mérföldkövek szinkronizálása a Finance and Operations alkalmazások projektszámlás tranzakcióival a **Project Operations integrációs szerződés sorának mérföldkövei (msdyn\_ contractlinescheduleofvalues)** táblatérkép használatával történik.

  ![Számlázási mérföldkövek integrációja.](./media/2Milestones.jpg)

A könyvelő a **Projektmenedzsment és könyvelés** > **Projekt szerződések** > **Karbantartás** > **Számlán belüli tranzakciók** vagy **Projektmenedzsment és számvitel** > **Minden projekt** > **Fenntartás** > **Számlán belüli tranzakciók** pontra lépve tekintheti át a számviteli tranzakciókat és módosíthatja a tranzakciók számviteli attribútumait .

Amikor először hoz létre számlázási mérföldkövet egy adott projektszerződési sorhoz, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet az ehhez a szerződési sorhoz társított projekthez. A fix áras bevételi becslési projektek a **Projektmenedzsment és számvitel** > **Fix áras bevételi becslési projektek** pontban tekinthetők meg.

### <a name="project-tasks"></a>Projektfeladatok

A projekttevékenységek szinkronizálása a Finance and Operations alkalmazásokkal a **Project-tevékenységek (msdyn\_ projecttasks)** táblatérképen keresztül történik, csak referenciaként. A műveletek létrehozása, frissítése és törlése nem támogatott a Finance and Operations alkalmazásokon keresztül.

  ![Projektfeladatok integrálása.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekt-erőforrások

A **Projekterőforrás-szerepkörök** entitás szinkronizálása a Finance and Operations alkalmazásokkal az **összes vállalat (foglalható erőforráskategória)** táblatérkép projekterőforrás-szerepköreinek használatával történik, csak referenciaként. Mivel az Dataverse erőforrás-szerepkörök nem vállalatspecifikusak, a rendszer automatikusan létrehozza a megfelelő vállalatspecifikus erőforrásszerepkörök-rekordokat a Finance and Operations alkalmazásokban automatikusan a kettős írású integrációs hatókörbe tartozó összes jogi személy számára.

![Erőforrás-szerepek konfigurálása.](./media/5Resources.jpg)

A Project Operations projekterőforrásai a Dataverse finance and operations alkalmazásokban vannak karbantartva, és nincsenek szinkronizálva a Finance and Operations alkalmazásokkal.

### <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciós kategóriák karbantartása a Dataverse Finance and Operations alkalmazásokban történik, és szinkronizálódik velük a **Project tranzakciós kategóriák (msdyn\_ transactioncategories)** táblatérkép használatával. A tranzakciókategória-rekord szinkronizálása után a rendszer automatikusan létrehoz négy megosztott kategóriarekordot. Minden rekord egy tranzakciótípusnak felel meg a Finance and Operations alkalmazásokban, és összekapcsolja őket a tranzakciós kategória rekordjával.

![Tranzakciókategóriák integrálása.](./media/4TransactionCategories.jpg)

A becsült és tényleges tranzakciós kategóriák használatához a projekt könyvelőjének vagy rendszergazdájának minden jogi személyben létre kell hoznia a megfelelő projektkategóriákat. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md).
