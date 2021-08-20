---
title: Projektszintű időnyilvántartás mobilalkalmazás
description: Ez a témakör a Microsoft Dynamics 365 Project Timesheet mobilalkalmazással kapcsolatban tartalmaz információkat. A Projektszintű időnyilvántartás mobilalkalmazás lehetővé teszi, hogy a felhasználók elküldjék és jóváhagyják a mobileszközön lévő projektek munkaidő-nyilvántartásait.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: df6d286b6d5716fb0ea908ed71c2257b4db21ecfd35148fea65dfd96e058ac9a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997204"
---
# <a name="project-timesheet-mobile-application"></a>Projektszintű időnyilvántartás mobilalkalmazás

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Áttekintés

A Microsoft Dynamics 365 Project Timesheet mobilalkalmazás lehetővé teszi, hogy a felhasználók elküldjék és jóváhagyják a mobileszközön (iPhone vagy Android) lévő projektek munkaidő-nyilvántartásait. Ez a mobil alkalmazás megjeleníti a munkaidő-nyilvántartási funkciót, amely a Dynamics 365 Finance Projektmenedzsment és könyvelés területén található, javítja a felhasználók termelékenységét és hatékonyságát, valamint lehetővé teszi a projektek munkaidő-nyilvántartásainak időben történő bevitelét és jóváhagyását.

## <a name="download-and-install-the-mobile-app"></a>Mobilalkalmazás letöltése és telepítése

Töltse le és telepítse a Microsoft Dynamics 365 Project Timesheet Android vagy iPhone rendszerre készült mobilalkalmazást a mobiláruházból az eszközére.

## <a name="enable-the-app"></a>Az alkalmazás engedélyezése 

A Finance rendszerben a Project Timesheet mobilalkalmazást engedélyezni kell. A funkció engedélyezéséhez lépjen a **Projektmenedzsment és könyvelési paraméterek \> Időnyilvántartás** lehetőségre, és válassza az **Microsoft Dynamics 365 Project Timesheet engedélyezése** elemet.

## <a name="sign-in-to-the-app"></a>Bejelentkezés az alkalmazásba

1.  Indítsa el az alkalmazást a mobileszközén.

2.  Adja meg a Finance URL-címét.

3.  Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát. Adja meg a hitelesítő adatait.

4.  Ekkor bejelentkezik az alapértelmezett vállalatba.

## <a name="submit-a-project-timesheet"></a>Projekt munkaidő-nyilvántartásának elküldése

A projekt munkaidő-nyilvántartását az alkalmazásban hozhatja létre és küldheti el. Az előző munkaidő-nyilvántartásokból, a mentett sorokból és a projektek hozzárendeléseiből származó információk alapján új munkaidő-nyilvántartást hozhat létre. Ha meghatalmazottként van kijelölve, akkor más munkavállalók számára is megadhat időnyilvántartásokat. Ha meghatalmazottként szeretne létrehozni egy munkaidő-nyilvántartást, akkor jelölje be a **Menü** gombot, és jelölje ki az erőforrás nevét.

A munkaidő-nyilvántartás oldala az aktuális dátum alapján új időrendet hoz létre a munkaidő-nyilvántartás időszakára vonatkozóan. A munkahét jelenik meg. Ha a munkaidő-nyilvántartási időszak több hetet fed le, a munkahét lapjain másik munkahét is kijelölhető.
Ha az aktuális dátumhoz létezik munkaidő-nyilvántartás, akkor az megjelenik. Ha egy másik munkaidő-nyilvántartási időszakban új munkaidő-nyilvántartást kell létrehoznia, akkor nyomja meg a **Menü** gombot, és válassza az **Új munkaidő-nyilvántartás** lehetőséget.

A projektadatok megadásához kattintson az **Idő hozzáadása** műveletre vagy a **Idő másolása innen:** műveletre. Az **Idő másolása innen:** művelet a projektsor adatait másolja, de az órákat nem. Az **Idő másolása innen:** menü a következő lehetőségeket tartalmazza:

- **Másolás meglévő munkaidő-nyilvántartásból** – A munkaidő-nyilvántartási sorok másolása egy meglévő munkaidő-nyilvántartásból.

- **Másolás a kedvencből** – Új munkaidő-nyilvántartási sorok létrehozása a kedvencekként kiválasztott munkaidő-nyilvántartási beállítások használatával.

- **Másolás hozzárendelésből** – Új munkaidő-nyilvántartási sorok létrehozása a hozzárendelt projektekből.

A megjelenített projektadatok a **Projektmenedzsment és könyvelési paraméterek** oldalon megadott mobil paraméterektől függenek.

A **Jogi entitás** mezőben válassza ki azt a jogi entitást, amelyhez a projektmunkát végezte. A **Jogi entitás** mező csak akkor érhető el, ha a vállalatközi munkaidő-nyilvántartási támogatás engedélyezve van a jogi entitásra vonatkozóan.

Válassza ki azt az ügyfelet, aki hozzá van rendelve a munkaidő-nyilvántartás projektjéhez. Az első Android rendszerű kiadásnál az ügyfél által történő bevitel nem támogatott, mivel előbb ki kell választania a projektet. Ha először kiválasztotta a projektet, akkor az **Ügyfél** mező a rendszer automatikusan kitölti.

A **Projekt** mezőben jelölje ki azt a projektet, amelyhez időt szeretne megadni. Az **Ügyfél** mezőjét a rendszer automatikusan kitölti.

Az ügyfél- és projektkeresések mind az ügyfeleken, mind a projekteken lehetővé teszik a keresést.

Adja meg a kívánt adatokat a **Kategória**, a **Tevékenység**, a **Sortulajdonság**, az **Áfacsoport** és az **Cikk áfacsoportja** mezőkben. Ezeket a mezőket felülírhatja.

A **Sortulajdonság** mező alapértelmezett értékre lesz beállítva a projektmenedzsment és a könyvelési paraméterek alapján. Ha a projekt/kategória és a kategória/erőforrás paraméterek engedélyezve vannak, a **Sortulajdonság** értékét a rendszer az érvényesítéshez megadott alapértelmezett értékre állítja be. Ha a projekt/kategória és a kategória/erőforrás paraméterek nincsenek engedélyezve, a **Sortulajdonság** értéke alapértelmezésre áll be az **Alapértelmezett sortulajdonság engedélyezése** mező alapján a **Projektmenedzsment és könyvelési paraméterek** lapon. A **Sortulajdonság** értéke felülírható.

Válasszon ki egy napot az időpont megadásához. Adja meg, hogy hány órát dolgozott naponta.

Ha megjegyzéseket szeretne fűzni a beírt időpontokhoz, kattintson a **Megjegyzések hozzáadása** lehetőségre, majd adja meg a belső célközönség, az ügyfél célközönség vagy mindkettő számára megjegyzéseit.
A belső megjegyzéseket a projektmenedzserek tekinthetik meg. Az ügyfelek megjegyzései szerepelnek a számlákon.

Ha a sort kedvencként szeretné menteni, jelölje be a jelölőnégyzetet, majd kattintson a **Mentés kedvencként** lehetőségre.

A mobilalkalmazás nem biztosítja a pénzügyi dimenziót és a mellékletek támogatását.

Folytassa a projektek sorainak felvételét a munkaidő-nyilvántartás végrehajtásához szükséges módon.

A **Küldés** gombra kattintva elküldheti a munkaidő-nyilvántartást a jóváhagyási munkafolyamatnak.

## <a name="review-timesheets"></a>Munkaidő-nyilvántartások áttekintése

Az áttekinteni kívánt munkaidő-nyilvántartások listája elérhető a menüben. Ez a beállítás csak akkor érhető el, ha a rendszer a munkafolyamat jóváhagyókjaént jelölte meg. A fejléc és a sor jóváhagyása egyaránt támogatott. A sorszintű jóváhagyás lehetővé teszi egy vagy több sor megjelölését jóváhagyásra. A munkaidő-nyilvántartás adatainak áttekintése után kattintson a **Jóváhagyás**, a **Delegálás** vagy a **Visszatérés** lehetőségre a munkafolyamat folytatásához.


[!INCLUDE[footer-include](../includes/footer-banner.md)]