---
title: Projektszintű időnyilvántartás mobilalkalmazás
description: Ez a cikk a Microsoft Dynamics 365 Project Timesheet mobilalkalmazásról nyújt tájékoztatást. A Projektszintű időnyilvántartás mobilalkalmazás lehetővé teszi, hogy a felhasználók elküldjék és jóváhagyják a mobileszközön lévő projektek munkaidő-nyilvántartásait.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110978"
---
# <a name="project-timesheet-mobile-application"></a>Projektszintű időnyilvántartás mobilalkalmazás

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Áttekintés

A Microsoft Dynamics 365 Project Timesheet mobilalkalmazás lehetővé teszi a felhasználók számára, hogy munkaidő-nyilvántartásokat küldjenek el és hagyjanak jóvá a mobileszközükön (iPhone vagy Android). Ez a mobilalkalmazás megjeleníti a munkaidő-nyilvántartási funkciókat, amelyek a Dynamics 365 Finance Projektvezetési és könyvelési területén találhatók. Segít javítani a felhasználók termelékenységét és hatékonyságát, valamint lehetővé teszi a projekt munkaidő-nyilvántartásainak időben történő bevitelét és jóváhagyását.

## <a name="download-and-install-the-mobile-app"></a>Mobilalkalmazás letöltése és telepítése

Töltse le és telepítse a Microsoft Dynamics 365 Project Timesheet Android vagy iPhone rendszerre készült mobilalkalmazást a mobiláruházból az eszközére.

## <a name="enable-the-app"></a>Az alkalmazás engedélyezése 

A Finance rendszerben a Project Timesheet mobilalkalmazást engedélyezni kell. A funkció engedélyezéséhez lépjen a **Projektmenedzsment és könyvelési paraméterek \> Időnyilvántartás** lehetőségre, és válassza az **Microsoft Dynamics 365 Project Timesheet engedélyezése** elemet.

### <a name="resolve-sign-in-issues"></a>Bejelentkezési problémák megoldása

**Probléma:** A Project Timesheet Mobile alkalmazásba való bejelentkezés során a felhasználók hibaüzenetet kapnak, amely szerint "nem férhetnek hozzá az alkalmazáshoz az 2bc50526-cdc3-4e36-a970-c284c34cbd6e adott bérlőben".

**Probléma:** A Project Timesheet Mobile alkalmazásba való bejelentkezés során a felhasználók az alábbi példák egyikéhez hasonló hibaüzenetet kapnak:

- "AADSTS50020: A'[felhasználónév]' felhasználói fiók az identitásszolgáltatótól'https://sts.windows.net/[app id]' nem létezik a'[bérlőazonosító]' bérlőben, és nem fér hozzá a'[app id]' alkalmazáshoz az adott bérlőben."
- "A kiválasztott felhasználói fiók nem létezik a bérlőben a'[bérlő azonosítója]' mezőben, és nem férhet hozzá a'[app id]' alkalmazáshoz az adott bérlőben."

**Magyarázat:** Ezeket a problémákat egy 2022 májusában végrehajtott Azure Active Directory módosítás okozza, Azure AD amely a külső felhasználókkal kapcsolatos.) Mivel ez a módosítás nem az alkalmazások finanszírozására és üzemeltetésére történt, a platform vagy az alkalmazás bármely verziójában lévő ügyfelekre hatással lehet.

**Javítás:** Minden külső felhasználót meg kell hívni a bérlőbe a következőn keresztül Azure AD: . További információ: [Felhasználók meghívása B2B-együttműködéssel Azure Active Directory](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Bejelentkezés az alkalmazásba

1.  Indítsa el az alkalmazást a mobileszközén.

2.  Adja meg a Finance URL-címét.

3.  Amikor először jelentkezik be, a rendszer kéri a felhasználónevét és a jelszavát. Adja meg a hitelesítő adatait.

4. Be lesz jelentkezve az alapértelmezett vállalatba.

## <a name="submit-a-project-timesheet"></a>Projekt munkaidő-nyilvántartásának elküldése

A projekt munkaidő-nyilvántartását az alkalmazásban hozhatja létre és küldheti el. Az előző munkaidő-nyilvántartásokból, a mentett sorokból és a projektek hozzárendeléseiből származó információk alapján új munkaidő-nyilvántartást hozhat létre. Ha meghatalmazottként van kijelölve, megadhat egy munkaidő-nyilvántartást egy másik dolgozó számára is. Ha meghatalmazottként szeretne munkaidő-nyilvántartást létrehozni, válassza a **Menü** gombot, majd válasszon ki egy erőforrásnevet.

A munkaidő-nyilvántartás oldala az aktuális dátum alapján új időrendet hoz létre a munkaidő-nyilvántartás időszakára vonatkozóan. A munkahét jelenik meg. Ha a munkaidő-nyilvántartási időszak több hetet fed le, a munkahét lapjain másik munkahét is kijelölhető.
Ha az aktuális dátumhoz létezik munkaidő-nyilvántartás, akkor az megjelenik. Ha egy másik munkaidő-nyilvántartási időszakban új munkaidő-nyilvántartást kell létrehoznia, akkor nyomja meg a **Menü** gombot, és válassza az **Új munkaidő-nyilvántartás** lehetőséget.

A projektadatok megadásához kattintson az **Idő hozzáadása** műveletre vagy a **Idő másolása innen:** műveletre. Az **Idő másolása innen:** művelet a projektsor adatait másolja, de az órákat nem. Az **Idő másolása innen:** menü a következő lehetőségeket tartalmazza:

- **Másolás meglévő munkaidő-nyilvántartásból** – A munkaidő-nyilvántartási sorok másolása egy meglévő munkaidő-nyilvántartásból.

- **Másolás a kedvencből** – Új munkaidő-nyilvántartási sorok létrehozása a kedvencekként kiválasztott munkaidő-nyilvántartási beállítások használatával.

- **Másolás hozzárendelésből** – Új munkaidő-nyilvántartási sorok létrehozása a hozzárendelt projektekből.

A megjelenített projektadatok a **Projektmenedzsment és könyvelési paraméterek** oldalon megadott mobil paraméterektől függenek.

A **Jogi entitás** mezőben válassza ki azt a jogi entitást, amelyhez a projektmunkát végezte. A **Jogi entitás** mező csak akkor érhető el, ha a vállalatközi munkaidő-nyilvántartási támogatás engedélyezve van a jogi entitásra vonatkozóan.

Válassza ki azt az ügyfelet, aki hozzá van rendelve a munkaidő-nyilvántartás projektjéhez. A kezdeti kiadáshoz a Android, az ügyfél szerinti bejegyzés nem támogatott, mivel először ki kell választania a projektet. Ha először kiválasztotta a projektet, akkor az **Ügyfél** mező a rendszer automatikusan kitölti.

**A Projekt** mezőben válassza ki azt a projektet, amelyhez időt ad meg. Az **Ügyfél** mezőjét a rendszer automatikusan kitölti.

Az ügyfél- és projektkeresések mind az ügyfeleken, mind a projekteken lehetővé teszik a keresést.

Adja meg a kívánt adatokat a **Kategória**, a **Tevékenység**, a **Sortulajdonság**, az **Áfacsoport** és az **Cikk áfacsoportja** mezőkben. Ezeket a mezőket felülírhatja.

A **Sortulajdonság** mező alapértelmezett értékre lesz beállítva a projektmenedzsment és a könyvelési paraméterek alapján. Ha a projekt/kategória és a kategória/erőforrás paraméterek engedélyezve vannak, a **Sortulajdonság** értékét a rendszer az érvényesítéshez megadott alapértelmezett értékre állítja be. Ha a projekt/kategória és a kategória/erőforrás paraméterek nincsenek engedélyezve, a **Sor tulajdonság** értéke alapértelmezés szerint lesz alapértelmezett a **Projektvezetési és könyvelési** paraméterek oldal Alapértelmezett sortulajdonság **engedélyezése mezőjének** megfelelően. A **Sortulajdonság** értéke felülírható.

Válasszon ki egy napot az időpont megadásához. Adja meg, hogy hány órát dolgozott naponta.

Ha megjegyzéseket szeretne fűzni a beírt órákhoz, kattintson a Megjegyzések **hozzáadása elemre**, majd írja be a belső célközönség, az ügyfél célközönség vagy mindkettőhöz tartozó megjegyzéseket.
A belső megjegyzéseket a projektmenedzserek tekinthetik meg. Az ügyfelek megjegyzései szerepelnek a számlákon.

Ha a sort kedvencként szeretné menteni, jelölje be a jelölőnégyzetet, majd kattintson a **Mentés kedvencként** lehetőségre.

A pénzügyi dimenzió és a mellékletek támogatása nem érhető el a mobilalkalmazásban.

Folytassa a projektek sorainak felvételét a munkaidő-nyilvántartás végrehajtásához szükséges módon.

A **Küldés** gombra kattintva elküldheti a munkaidő-nyilvántartást a jóváhagyási munkafolyamatnak.

## <a name="review-timesheets"></a>Munkaidő-nyilvántartások áttekintése

A felülvizsgálandó munkaidő-nyilvántartások listája elérhető a menüben. Ez a lehetőség csak akkor érhető el, ha Ön lett kijelölve munkafolyamat-jóváhagyóként. A fejléc és a sor jóváhagyása egyaránt támogatott. A sorszintű jóváhagyás lehetővé teszi egy vagy több sor megjelölését jóváhagyásra. A munkaidő-nyilvántartás adatainak áttekintése után kattintson a **Jóváhagyás**, a **Delegálás** vagy a **Visszatérés** lehetőségre a munkafolyamat folytatásához.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
