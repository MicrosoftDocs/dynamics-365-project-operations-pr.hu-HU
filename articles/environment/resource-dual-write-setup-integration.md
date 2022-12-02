---
title: Project Operations telepítése és a konfigurációs adatok integrációja
description: Ez a cikk a Project Operations kettős írású térképeinek beállításával és konfigurálásával kapcsolatban nyújt tájékoztatást.
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

Ez a cikk a Project Operations alkalmazásnak a beállítási és konfigurációs entitások kettős írású integrációjával kapcsolatos információkat nyújt.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektszerződés, szerződéssorok és projektek

A projektszerződéseket, szerződéssorokat és projekteket a(z) Dataverse alkalmazásban hozzák létre, és szinkronizálják a pénzügyi és műveleti alkalmazásokkal a további könyvelés érdekében. Az ezekben az entitásokban lévő rekordok csak a(z) Dataverse felületen hozhatók létre és törölhetők. Az pénzügyi és műveleti alkalmazásokban azonban számviteli attribútumok, például forgalmi adócsoport-előrejelzések és pénzügyi dimenziók adhatók hozzá ezekhez a rekordokhoz.

  ![Projekt szerződés integrációs koncepciók.](./media/1ProjectContract.jpg)

Az értékesítési tevékenységek leadjei, lehetőségei és árajánlatai nyomon követése a Dataverse felületen történik, és nem szinkronizálódnak a pénzügyi és műveleti alkalmazásokkal, mivel ezekhez a tevékenységekhez nem kapcsolódik utólagos könyvelés.

A Dataverse felületen lévő projektszerződés funkció létrehoz egy projektszerződés rekordot a pénzügyi és műveleti alkalmazásokban a **Projektszerződés fejlécek (értékesítési megrendelések)** táblaleképezés segítségével. A projektszerződés Dataverse felületre történő mentése egyben elindítja a projektszerződés ügyfél entitási rekordjának létrehozását is. Ez a rekord a **Projektfinanszírozási forrás (msdyn\_projectcontractssplitbillingrules) táblatérkép** segítségével szinkronizálódik pénzügyi és műveleti alkalmazásokkal. Ez a térkép szinkronizálja a projektszerződések vevőinek kiegészítéseit, frissítéseit és törlését is. A projektszerződéses ügyfelek között osztott számlázási százalékok csak a Dataverse felületen alkalmazhatók, és nem szinkronizálódnak pénzügyi és műveleti alkalmazásokkal.

Miután a Dataverse-felületen létrehoztak egy projektszerződést, a projektszerződéssel a pénzügyi és műveleti alkalmazásokban ehhez a projektszerződéshez a **Projektmenedzsment és könyvelés** > **Projektszerződések** > **Beállítások** > **Alapértelmezett könyvelés megjelenítése**. A könyvelő pénzügyi és műveleti alkalmazásokban a projektszerződés azonosítójának kiválasztásával áttekintheti a projektszerződés operatív jellemzőit, például a kért teljesítési dátumot és a szerződés összegét, ami megnyitja a kapcsolódó projektszerződés rekordot a Dataverse alkalmazásban.

A projekt entitás szinkronizálva van a pénzügyi és műveleti alkalmazásokkal a **Projects V2 (msdyn\_projektek)** táblaleképezés használatával. A projekt könyvelője:

  - Áttekintheti a pénzügyi és műveleti alkalmazások projektjeit a **Projektmenedzsment és a Könyvelés** > **Minden projekt** lapon. 
  - Frissítheti a projekt számviteli attribútumait a pénzügyi és műveleti alkalmazások alkalmazásokban a **Projektmenedzsment és a Könyvelés** > **Minden projekt** > **Beállítások** > **Alapértelmezett könyvelés megjelenítése** pontra lépve.  
  - A pénzügyi és műveleti alkalmazások alkalmazásban a projekt azonosítójának kiválasztásával áttekintheti a projekt operatív jellemzőit, például a becsült kezdő- és befejezési dátumokat, ami megnyitja a kapcsolódó projektrekordot a Dataverse-ben.

A projektek a **Projekt szerződéssor** entitáson keresztül kapcsolódnak egy projektszerződéshez.

A pénzügyi és műveleti alkalmazások felületen lévő Dataverse-projektszerződéssorok létrehoznak egy projektszerződés rekordot a pénzügyi és műveleti alkalmazásokban a **Projektszerződéssorok (salesorderdetails)** táblaleképezés segítségével. A számlázási mód meghatározza a projektszerződés számlázási szabálytípusát a pénzügyi és műveleti alkalmazásokban:

  - Az idő és az anyag számlázási módjával rendelkező projektszerződés-sorok létrehozzák az idő és az anyagtípus számlázási szabályát.
  - A fix áras számlázási mód szerződéses sorok mérföldkő számlázási szabályt hoznak létre.

A projekt szerződéses sorait a projekt könyvelője a pénzügyi és műveleti alkalmazásokban a **Projektmenedzsment és könyvelés** > **Projektszerződések** > **Beállítások** > **Alapértelmezett könyvelés** megjelenítése menüpontban tekintheti meg, és a **Szerződéses sorok** lapon megtekintheti a részleteket. A könyvelő ezen a lapon állíthatja be a fix áras számlázási módszerrel kötött szerződéssorok alapértelmezett pénzügyi dimenzióit is.

## <a name="billing-milestones"></a>Számlázási mérföldkövek

A fix áras számlázási módszert alkalmazó projektszerződések számlázása mérföldköveken keresztül történik. A számlázási mérföldkövek szinkronizálása a pénzügyi és műveleti alkalmazásokban a **Project Operations integráció szerződéssor-mérföldkövek (msdyn\_contractlinescheduleofvalues)** táblaleképezés használatával történik.

  ![Számlázási mérföldkövek integrációja.](./media/2Milestones.jpg)

A könyvelő a **Projektmenedzsment és könyvelés** > **Projekt szerződések** > **Karbantartás** > **Számlán belüli tranzakciók** vagy **Projektmenedzsment és számvitel** > **Minden projekt** > **Fenntartás** > **Számlán belüli tranzakciók** pontra lépve tekintheti át a számviteli tranzakciókat és módosíthatja a tranzakciók számviteli attribútumait .

Amikor először hoz létre számlázási mérföldkövet egy adott projektszerződési sorhoz, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet az ehhez a szerződési sorhoz társított projekthez. A fix áras bevételi becslési projektek a **Projektmenedzsment és számvitel** > **Fix áras bevételi becslési projektek** pontban tekinthetők meg.

### <a name="project-tasks"></a>Projektfeladatok

A projektfeladatok szinkronizálása a pénzügyi és műveleti alkalmazásokkal a **Projektfeladatok (msdyn\_projecttasks)** táblaleképezésen keresztül történik – mindössze referenciaként. A létrehozási, frissítési és törlési műveletek nem támogatottak a pénzügyi és műveleti alkalmazásokban.

  ![Projektfeladatok integrálása.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekt-erőforrások

A **Projekt erőforrás-szerepek** entitást a **Projekterőforrás-szerepek minden vállalat számára (bookableresourcecategories)** táblaleképezés segítségével szinkronizáljuk a pénzügyi és műveleti alkalmazásokkal, csak referenciaként. Mivel a Dataverse-felületen lévő erőforrás-szerepek nem cégspecifikusak, a rendszer automatikusan létrehozza a megfelelő cégspecifikus erőforrás-szerepek rekordjait a pénzügyi és műveleti alkalmazásokban a kettős írású integrációs hatókörbe bevont összes jogalany számára.

![Erőforrás-szerepek konfigurálása.](./media/5Resources.jpg)

A Project Operations projekt-erőforrásainak karbantartása a Dataverse-ben történik, és nem szinkronizálódnak a pénzügyi és műveleti alkalmazásokkal.

### <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciók kategóriáit a Dataverse-alkalmazásban tartják fenn, és a pénzügyi és műveleti alkalmazásokkal szinkronizálják a **Projekt tranzakciók kategóriái (msdyn\_transactioncategories)** táblaleképezés segítségével. A tranzakciókategória-rekord szinkronizálása után a rendszer automatikusan létrehoz négy megosztott kategóriarekordot. Minden rekord megfelel a pénzügyi és műveleti alkalmazások tranzakciótípusának, és összekapcsolja azokat a tranzakciós kategória rekordja.

![Tranzakciókategóriák integrálása.](./media/4TransactionCategories.jpg)

A becsült és tényleges tranzakciós kategóriák használatához a projekt könyvelőjének vagy rendszergazdájának minden jogi személyben létre kell hoznia a megfelelő projektkategóriákat. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md).
