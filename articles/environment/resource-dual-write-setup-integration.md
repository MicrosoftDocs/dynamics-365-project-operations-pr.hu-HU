---
title: Project Operations telepítése és a konfigurációs adatok integrációja
description: Ez a témakör a Project Operations kettős írású térképeinek beállításával és konfigurálásával kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586899"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations telepítése és a konfigurációs adatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a Project Operations alkalmazásnak a beállítási és konfigurációs entitások kettős írású integrációjával kapcsolatos információkat nyújt.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektszerződés, szerződéssorok és projektek

A projektszerződések, szerződéssorok és projektek további könyvelés céljából a Pénzügy és műveletek alkalmazásban jönnek létre Dataverse és szinkronizálódnak velük. Az ezekben az entitásokban lévő rekordok csak a(z) Dataverse felületen hozhatók létre és törölhetők. A Pénzügyi és műveletek alkalmazásban azonban hozzáadható ezekhez a rekordokhoz olyan könyvelési attribútumok, mint az áfacsoport alapértelmezései és a pénzügyi dimenziók.

  ![Projekt szerződés integrációs koncepciók.](./media/1ProjectContract.jpg)

Az értékesítési tevékenység érdeklődői, a lehetőségek és az ajánlatok nyomon követhetők Dataverse, és nem szinkronizálódnak a Pénzügy és műveletek alkalmazásokkal, mert ehhez a tevékenységhez nincs downstream könyvelés társítva.

A projektszerződések funkciója a Projektszerződések Dataverse **táblaleképezés segítségével projektszerződés-rekordot hoz létre a** Pénzügy és műveletek alkalmazásban. A projektszerződés Dataverse felületre történő mentése egyben elindítja a projektszerződés ügyfél entitási rekordjának létrehozását is. Ez a rekord szinkronizálva van a Pénzügyi és üzemeltetési alkalmazásokkal a **Projektfinanszírozási forrás (msdyn\_ projectcontractssplitbillingrules)** táblatérkép használatával. Ez a térkép szinkronizálja a projektszerződések vevőinek kiegészítéseit, frissítéseit és törlését is. A projektszerződés-ügyfelek közötti megosztott számlázási százalékok csak a Pénzügy és műveleti alkalmazásokban Dataverse vannak elsajátítva, és nem szinkronizálódnak velük.

A projektszerződés létrehozása Dataverse után a projektkönyvelő frissítheti a projektszerződés könyvelési attribútumait a Pénzügy és műveletek alkalmazásban, ha a Projektmenedzsment és könyvelés **projektszerződések** > **beállítása Beállítás** > **Alapértelmezett könyvelés** > **megjelenítése parancsra megy**. A könyvelő áttekintheti a műveleti projektszerződés attribútumait, például a kért szállítási dátumot és a szerződés összegét, ha kiválasztja a projektszerződés azonosítóját a Pénzügy és műveletek alkalmazásban, amely megnyitja a kapcsolódó projektszerződés-rekordot a alkalmazásban Dataverse.

A projekt entitás szinkronizálva van a Finance and Operations alkalmazásokkal a **Projects V2 (msdyn\_ projects)** táblatérkép segítségével. A projekt könyvelője:

  - Tekintse át a projekteket a Pénzügyi és üzemeltetési alkalmazásokban a **Projektmenedzsment és a számvitel** > **minden projekt** megnyitásával. 
  - A projekt számviteli attribútumainak frissítése a Pénzügy és műveletek alkalmazásban a **Projektkezelés és számlázás** > **lapon Minden projekt** > **beállítása** > **Alapértelmezett könyvelés** megjelenítése.  
  - Tekintse át a működési projektattribútumokat, például a becsült kezdési és befejezési dátumokat, ha kiválasztja a projektazonosítót a Pénzügy és műveletek alkalmazásban, amely megnyitja a kapcsolódó projektrekordot a alkalmazásban Dataverse.

A projektek a **Projekt szerződéssor** entitáson keresztül kapcsolódnak egy projektszerződéshez.

A projektszerződéssorok Dataverse létrehozása projektszerződés számlázási szabályt hoz létre a Pénzügy és műveletek alkalmazásban a **Projektszerződéssorok (salesorderdetails)** táblatérkép használatával. A számlázási módszer határozza meg a projektszerződés számlázási szabálytípusát a Pénzügy és műveletek alkalmazásban:

  - Az idő és az anyag számlázási módjával rendelkező projektszerződés-sorok létrehozzák az idő és az anyagtípus számlázási szabályát.
  - A fix áras számlázási mód szerződéses sorok mérföldkő számlázási szabályt hoznak létre.

A projektszerződéssorokat a Projektkönyvelő a Pénzügy és műveletek alkalmazásban **a Projektmenedzsment és könyvelés** > **projektszerződések** > **beállítása Alapértelmezett** > **könyvelés** megjelenítése menüpontban, valamint a **Szerződéssorok** lapon található részletek áttekintésével tekintheti felül a projektkönyvelő. A könyvelő ezen a lapon is beállíthatja a rögzített árú számlázási mód szerződéssorainak alapértelmezett pénzügyi dimenzióit.

## <a name="billing-milestones"></a>Számlázási mérföldkövek

A fix áras számlázási módszert alkalmazó projektszerződések számlázása mérföldköveken keresztül történik. A számlázási mérföldkövek szinkronizálása a Projektműveletek integrációs szerződéssor mérföldkövei (msdyn **contractlineschedule ofvalues)\_ táblatérkép segítségével szinkronizálódik a** projekt részszámlázási tranzakcióival.

  ![Számlázási mérföldkövek integrációja.](./media/2Milestones.jpg)

A könyvelő a **Projektmenedzsment és könyvelés** > **Projekt szerződések** > **Karbantartás** > **Számlán belüli tranzakciók** vagy **Projektmenedzsment és számvitel** > **Minden projekt** > **Fenntartás** > **Számlán belüli tranzakciók** pontra lépve tekintheti át a számviteli tranzakciókat és módosíthatja a tranzakciók számviteli attribútumait .

Amikor először hoz létre számlázási mérföldkövet egy adott projektszerződési sorhoz, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet az ehhez a szerződési sorhoz társított projekthez. A fix áras bevételi becslési projektek a **Projektmenedzsment és számvitel** > **Fix áras bevételi becslési projektek** pontban tekinthetők meg.

### <a name="project-tasks"></a>Projektfeladatok

A projekttevékenységek szinkronizálása a Pénzügy és műveletek alkalmazásokkal a **Project tevékenységek (msdyn\_ projecttasks)** táblatérképen keresztül történik, csak referenciacélokra. A létrehozási, frissítési és törlési műveleteket a Pénzügy és műveletek alkalmazások nem támogatják.

  ![Projektfeladatok integrálása.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekt-erőforrások

A **Project erőforrás-szerepkörök** entitása szinkronizálva van a Pénzügy és műveletek alkalmazásokkal, amelyek a **Project erőforrás-szerepköreit használják az összes vállalat (könyvelhető forráskategória)** táblatérképén, csak referencia célokra. Mivel a programban szereplő Dataverse erőforrás-szerepkörök nem vállalatspecifikusak, a rendszer automatikusan létrehozza a megfelelő vállalatspecifikus erőforrás-szerepkörrekordokat a Pénzügy és műveletek alkalmazásokban a kettős írási integrációs hatókörbe tartozó összes jogi személy számára.

![Erőforrás-szerepek konfigurálása.](./media/5Resources.jpg)

A Project Operations projekterőforrásai a rendszerben Dataverse vannak, és nincsenek szinkronizálva a Pénzügy és műveletek alkalmazásokkal.

### <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciókategóriákat a Project tranzakciókategóriák (msdyn Dataverse tranzakciókategóriák) **táblatérképén a Rendszer a \_ Pénzügy és műveletek alkalmazásokkal** tartja karban, és szinkronizálja velük. A tranzakciókategória-rekord szinkronizálása után a rendszer automatikusan létrehoz négy megosztott kategóriarekordot. Minden rekord megfelel egy tranzakciótípusnak a Pénzügy és műveletek alkalmazásban, és összekapcsolja őket a tranzakciókategória-bejegyzéssel.

![Tranzakciókategóriák integrálása.](./media/4TransactionCategories.jpg)

A becsült és tényleges tranzakciós kategóriák használatához a projekt könyvelőjének vagy rendszergazdájának minden jogi személyben létre kell hoznia a megfelelő projektkategóriákat. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md).
