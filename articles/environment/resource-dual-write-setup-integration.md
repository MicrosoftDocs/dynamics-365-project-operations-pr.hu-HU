---
title: Project Operations telepítése és a konfigurációs adatok integrációja
description: Ez a cikk a Project Operations kettős írású leképezéseinek beállításával és konfigurálásával kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029155"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations telepítése és a konfigurációs adatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást a beállítási és konfigurációs entitásokhoz.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektszerződés, szerződéssorok és projektek

A projektszerződések, a szerződéssorok és a projektek a további könyveléshez szükséges Dataverse finanszírozási és üzemeltetési alkalmazásokban jönnek létre, és szinkronizálódnak azokkal. Az ezekben az entitásokban lévő rekordok csak a(z) Dataverse felületen hozhatók létre és törölhetők. Ezekhez a rekordokhoz azonban hozzáadhatók olyan könyvelési attribútumok, mint az áfacsoport alapértelmezett értékei és a pénzügyi dimenziók a finance and operations alkalmazásokban.

  ![Projekt szerződés integrációs koncepciók.](./media/1ProjectContract.jpg)

Az értékesítési tevékenység érdeklődőinek, lehetőségeinek és árajánlatainak nyomon követése megtörténik Dataverse, és nem szinkronizálódik a pénzügyi és üzemeltetési alkalmazásokkal, mert ehhez a tevékenységhez nincs kapcsolódó downstream könyvelés.

A projektszerződés funkciója Dataverse létrehoz egy projektszerződés-rekordot a pénzügyi és műveleti alkalmazásokban a **Projektszerződés fejlécek (értékesítési rendelések)** táblatérkép használatával. A projektszerződés Dataverse felületre történő mentése egyben elindítja a projektszerződés ügyfél entitási rekordjának létrehozását is. Ez a rekord szinkronizálva van a pénzügyi és üzemeltetési alkalmazásokkal a **Project finanszírozási forrás (msdyn\_ projectcontractssplitbillingrules)** táblatérkép használatával. Ez a térkép szinkronizálja a projektszerződések vevőinek kiegészítéseit, frissítéseit és törlését is. A projektszerződés-ügyfelek közötti számlázási százalékok felosztása csak a Dataverse pénzügyi és üzemeltetési alkalmazásokban van elsajátítva, és nem szinkronizálva van azokkal.

Miután létrehozta Dataverse a projektszerződést, a projektkönyvelő frissítheti a projektszerződés könyvelési attribútumait a pénzügyi és üzemeltetési alkalmazásokban a **Projektvezetési és könyvelési** > **projektszerződések** > **beállítása az Alapértelmezett könyvelés** > **megjelenítése** beállítás elemre kattintva. A könyvelő áttekintheti az operatív projektszerződés attribútumait, például a kért teljesítési dátumot és a szerződés összegét, ha kiválasztja a projektszerződés azonosítóját a pénzügyi és üzemeltetési alkalmazásokban, amely megnyitja a kapcsolódó projektszerződés-rekordot a következőben Dataverse: .

A projektentitás szinkronizálása a Finance and Operations alkalmazásokkal a **Projects V2 (msdyn\_ projects)** táblatérkép használatával történik. A projekt könyvelője:

  - Tekintse át a projekteket a pénzügyi és üzemeltetési alkalmazásokban a Projektvezetés és könyvelés **minden projekt** > **oldalon**. 
  - Frissítse a projekt könyvelési attribútumait a pénzügyi és műveleti alkalmazásokban a **Projektvezetés és könyvelés** > **Minden projekt** > **beállítása Beállítás Alapértelmezett** > **könyvelés** megjelenítése elemre kattintva.  
  - Tekintse át az operatív projektattribútumokat, például a becsült kezdési és befejezési dátumokat úgy, hogy kiválasztja a projektazonosítót a pénzügyi és üzemeltetési alkalmazásokban, amely megnyitja a kapcsolódó projektrekordot a következőben Dataverse: .

A projektek a **Projekt szerződéssor** entitáson keresztül kapcsolódnak egy projektszerződéshez.

A projektszerződés-sorok létrehoznak Dataverse egy projektszerződés számlázási szabályt a pénzügyi és üzemeltetési alkalmazásokban a **Project-szerződéssorok (salesorderdetails)** táblatérkép használatával. A számlázási módszer határozza meg a projektszerződés számlázási szabályának típusát a pénzügyi és üzemeltetési alkalmazásokban:

  - Az idő és az anyag számlázási módjával rendelkező projektszerződés-sorok létrehozzák az idő és az anyagtípus számlázási szabályát.
  - A fix áras számlázási mód szerződéses sorok mérföldkő számlázási szabályt hoznak létre.

A projektszerződések sorait a projektkönyvelő áttekintheti a pénzügyi és műveleti alkalmazásokban, ha a **Projektvezetési és könyvelési** > **projektszerződések** > **beállítása Az alapértelmezett könyvelés** > **megjelenítése beállításra** talál, és áttekinti a részleteket a **Szerződéssorok** lapon. A könyvelő ezen a lapon alapértelmezett pénzügyi dimenziókat is beállíthat a rögzített árú számlázási módszer szerződéses soraihoz.

## <a name="billing-milestones"></a>Számlázási mérföldkövek

A fix áras számlázási módszert alkalmazó projektszerződések számlázása mérföldköveken keresztül történik. A számlázási mérföldkövek szinkronizálása a pénzügyi és üzemeltetési alkalmazások fiókon belüli tranzakcióival a **Project Operations integrációs szerződés sorának mérföldkövei (msdyn\_ contractscheduleofvalues)** táblatérkép használatával történik.

  ![Számlázási mérföldkövek integrációja.](./media/2Milestones.jpg)

A könyvelő a **Projektmenedzsment és könyvelés** > **Projekt szerződések** > **Karbantartás** > **Számlán belüli tranzakciók** vagy **Projektmenedzsment és számvitel** > **Minden projekt** > **Fenntartás** > **Számlán belüli tranzakciók** pontra lépve tekintheti át a számviteli tranzakciókat és módosíthatja a tranzakciók számviteli attribútumait .

Amikor először hoz létre számlázási mérföldkövet egy adott projektszerződési sorhoz, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet az ehhez a szerződési sorhoz társított projekthez. A fix áras bevételi becslési projektek a **Projektmenedzsment és számvitel** > **Fix áras bevételi becslési projektek** pontban tekinthetők meg.

### <a name="project-tasks"></a>Projektfeladatok

A projekttevékenységek szinkronizálása a Pénzügyi és műveleti alkalmazásokkal a **Projekttevékenységek (msdyn\_ projekttevékenységek)** táblatérképen keresztül történik, csak referenciaként. A műveletek létrehozása, frissítése és törlése nem támogatott a pénzügyi és üzemeltetési alkalmazásokon keresztül.

  ![Projektfeladatok integrálása.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekt-erőforrások

A **Projekterőforrás-szerepkörök** entitás szinkronizálása a pénzügyi és műveleti alkalmazásokkal az **összes vállalat projekterőforrás-szerepkörei (foglalható erőforráskategóriák)** táblatérképének használatával történik, csak referenciaként. Mivel az Dataverse erőforrásszerepkörök nem vállalatspecifikusak, a rendszer automatikusan létrehozza a megfelelő vállalatspecifikus erőforrás-szerepkörök rekordjait a pénzügyi és üzemeltetési alkalmazásokban automatikusan a kettős írású integrációs hatókörbe tartozó összes jogi személy számára.

![Erőforrás-szerepek konfigurálása.](./media/5Resources.jpg)

A Project Operations projekterőforrásai a Dataverse rendszer a pénzügyi és üzemeltetési alkalmazásokban van karbantartva, és nincsenek szinkronizálva a pénzügyi és üzemeltetési alkalmazásokkal.

### <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciós kategóriák karbantartása és Dataverse szinkronizálása a Pénzügyi és műveleti alkalmazásokban történik a **Project tranzakciós kategóriák (msdyn\_ transactioncategories)** táblatérkép használatával. A tranzakciókategória-rekord szinkronizálása után a rendszer automatikusan létrehoz négy megosztott kategóriarekordot. Minden rekord egy tranzakciótípusnak felel meg a pénzügyi és műveleti alkalmazásokban, és összekapcsolja őket a tranzakciós kategória rekordjával.

![Tranzakciókategóriák integrálása.](./media/4TransactionCategories.jpg)

A becsült és tényleges tranzakciós kategóriák használatához a projekt könyvelőjének vagy rendszergazdájának minden jogi személyben létre kell hoznia a megfelelő projektkategóriákat. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md).
