---
title: Project Operations telepítése és a konfigurációs adatok integrációja
description: Ez a témakör a Project Operations kettős írású térképeinek beállításával és konfigurálásával kapcsolatban nyújt tájékoztatást.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986539"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations telepítése és a konfigurációs adatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a témakör a Project Operations alkalmazásnak a beállítási és konfigurációs entitások kettős írású integrációjával kapcsolatos információkat nyújt.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektszerződés, szerződéssorok és projektek

A projektszerződéseket, szerződéssorokat és projekteket a(z) Dataverse alkalmazásban hozzák létre, és szinkronizálják a(z) Finance and Operations alkalmazással a további könyvelés érdekében. Az ezekben az entitásokban lévő rekordok csak a(z) Dataverse felületen hozhatók létre és törölhetők. Az Finance and Operations alkalmazásokban azonban számviteli attribútumok, például forgalmi adócsoport-előrejelzések és pénzügyi dimenziók adhatók hozzá ezekhez a rekordokhoz.

  ![Projekt szerződés integrációs koncepciók.](./media/1ProjectContract.jpg)

Az értékesítési tevékenységek leadjei, lehetőségei és árajánlatai nyomon követése a(z) Dataverse felületen történik, és nem szinkronizálódnak a(z) Finance and Operations alkalmazásokkal, mivel ezekhez a tevékenységekhez nem kapcsolódik utólagos könyvelés.

A(z) Dataverse felületen lévő projektszerződés funkció létrehoz egy projektszerződés rekordot a(z) Finance and Operations alkalmazásban a **Projektszerződés fejlécek (értékesítési megrendelések)** táblatérkép segítségével. A projektszerződés Dataverse felületre történő mentése egyben elindítja a projektszerződés ügyfél entitási rekordjának létrehozását is. Ez a rekord a **Projektfinanszírozási forrás (msdyn\_projectcontractssplitbillingrules)** táblatérkép segítségével szinkronizálódik a(z) Finance and Operations alkalmazásokkal. Ez a térkép szinkronizálja a projektszerződések vevőinek kiegészítéseit, frissítéseit és törlését is. A projektszerződéses ügyfelek között osztott számlázási százalékok csak a(z) Dataverse felületen alkalmazhatók, és nem szinkronizálódnak a(z) Finance and Operations alkalmazásokkal.

Miután a(z) Dataverse felületen létrehoztak egy projektszerződést, a projektkönyvelő a(z) Finance and Operations alkalmazásokban a **Projektmenedzsment és könyvelés** > **Projektszerződések** > **Beállítás** > **Egyértelmezett könyvelés megjelenítése** menüpontban frissítheti a projektszerződés számviteli attribútumait. A könyvelő a(z) Finance and Operations alkalmazásban a projektszerződés azonosítójának kiválasztásával áttekintheti a projektszerződés operatív jellemzőit, például a kért teljesítési dátumot és a szerződés összegét, ami megnyitja a kapcsolódó projektszerződés rekordot a(z) Dataverse alkalmazásban.

A projekt entitás szinkronizálva van a(z) Finance and Operations alkalmazásokkal a **Projects V2 (msdyn\_projektek)** táblatérkép használatával. A projekt könyvelője:

  - Áttekintheti a(z) Finance and Operations alkalmazások projektjeit a **Projektmenedzsment és a Könyvelés** > **Minden projekt** lapon. 
  - Frissítheti a projekt számviteli attribútumait a(z) Finance and Operations alkalmazásokban a **Projektmenedzsment és a Könyvelés** > **Minden projekt** > **Beállítás** > **Alapértelmezett könyvelés megjelenítése** pontra lépve.  
  - A(z) Finance and Operations alkalmazásban a projekt azonosítójának kiválasztásával áttekintheti a projekt operatív jellemzőit, például a becsült kezdő- és befejezési dátumokat, ami megnyitja a kapcsolódó projektrekordot a(z) Dataverse alkalmazásban.

A projektek a **Projekt szerződéssor** entitáson keresztül kapcsolódnak egy projektszerződéshez.

A(z) Dataverse felületen lévő projektszerződéssorok létrehoznak egy projektszerződés rekordot a(z) Finance and Operations alkalmazásban a **Projektszerződéssorok (salesorderdetails)** táblatérkép segítségével. A számlázási módszer a(z) Finance and Operations alkalmazásokban a projektszerződés számlázási szabályának típusát határozza meg:

  - Az idő és az anyag számlázási módjával rendelkező projektszerződés-sorok létrehozzák az idő és az anyagtípus számlázási szabályát.
  - A fix áras számlázási mód szerződéses sorok mérföldkő számlázási szabályt hoznak létre.

A projekt szerződéses sorait a projekt könyvelője a(z) Finance and Operations alkalmazásokban a **Projektmenedzsment és könyvelés** > **Projektszerződések** > **Beállítás** > **Előreállított könyvelés megjelenítése** menüpontban tekintheti meg, és a **Szerződéses sorok** lapon megtekintheti a részleteket. A könyvelő ezen a lapon állíthatja be a fix áras számlázási módszerrel kötött szerződéssorok alapértelmezett pénzügyi dimenzióit is.

## <a name="billing-milestones"></a>Számlázási mérföldkövek

A fix áras számlázási módszert alkalmazó projektszerződések számlázása mérföldköveken keresztül történik. A számlázási mérföldkövek szinkronizálása a(z) Finance and Operations alkalmazásokban a **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** táblatérkép használatával történik.

  ![Számlázási mérföldkövek integrációja.](./media/2Milestones.jpg)

A könyvelő a **Projektmenedzsment és könyvelés** > **Projekt szerződések** > **Karbantartás** > **Számlán belüli tranzakciók** vagy **Projektmenedzsment és számvitel** > **Minden projekt** > **Fenntartás** > **Számlán belüli tranzakciók** pontra lépve tekintheti át a számviteli tranzakciókat és módosíthatja a tranzakciók számviteli attribútumait .

Amikor először hoz létre számlázási mérföldkövet egy adott projektszerződési sorhoz, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet az ehhez a szerződési sorhoz társított projekthez. A fix áras bevételi becslési projektek a **Projektmenedzsment és számvitel** > **Fix áras bevételi becslési projektek** pontban tekinthetők meg.

### <a name="project-tasks"></a>Projektfeladatok

A projektfeladatok szinkronizálása a(z) Finance and Operations alkalmazásokkal a **Projektfeladatok (msdyn\_projecttasks)** táblatérképen keresztül történik – mindössze referenciaként. A létrehozási, frissítési és törlési műveletek nem támogatottak a(z) Finance and Operations alkalmazásokban.

  ![Projektfeladatok integrálása.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekt-erőforrások

A **Projekt erőforrás-szerepek** entitást a **Projekterőforrás-szerepek minden vállalat számára (bookableresourcecategories)** táblatérkép segítségével szinkronizáljuk a(z) Finance and Operations alkalmazással, csak referenciaként. Mivel a(z) Dataverse felületen lévő erőforrás-szerepek nem cégspecifikusak, a rendszer automatikusan létrehozza a megfelelő cégspecifikus erőforrás-szerepek rekordjait a(z) Finance and Operations alkalmazásokban a kettős írású integrációs hatókörbe bevont összes jogalany számára.

![Erőforrás-szerepek konfigurálása.](./media/5Resources.jpg)

A Project Operations projekt-erőforrásainak karbantartása a(z) Dataverse felületen történik, és nem szinkronizálódnak a(z) Finance and Operations alkalmazásokkal.

### <a name="transaction-categories"></a>Tranzakciókategóriák

A tranzakciók kategóriáit a(z) Dataverse alkalmazásban tartják fenn, és a(z) Finance and Operations alkalmazással szinkronizálják a **Projekt tranzakciók kategóriái (msdyn\_transactioncategories)** táblatérkép segítségével. A tranzakciókategória-rekord szinkronizálása után a rendszer automatikusan létrehoz négy megosztott kategóriarekordot. Minden rekord megfelel a(z) Finance and Operations alkalmazások tranzakciótípusának, és összekapcsolja azokat a tranzakciós kategória rekordja.

![Tranzakciókategóriák integrálása.](./media/4TransactionCategories.jpg)

A becsült és tényleges tranzakciós kategóriák használatához a projekt könyvelőjének vagy rendszergazdájának minden jogi személyben létre kell hoznia a megfelelő projektkategóriákat. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md).
