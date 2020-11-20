---
title: Utazási kérelmek
description: Ez a témakör az utazási kérelmekről tartalmaz információkat.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123741"
---
# <a name="travel-requisitions"></a>Utazási kérelmek

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az utazási kérelem felsorolja az utazás céljából felmerülő költségeket. Az utazási kérelmet be kell nyújtani áttekintésre, és felhasználható a kiadások engedélyezésére.

Előfordulhat, hogy utazási kérelmet kell benyújtania, mielőtt felszámíthatna bármilyen kiadást a szervezet felé. Ez a követelmény érvényes, függetlenül attól, hogy a vállalat hitelkártyájára terheli a felmerülő kiadásokat, készpénzelőlegként kapott készpénzt költ, vagy a szervezet által visszatérítendő, saját pénzből fedezett kiadások merültek fel.

Az utazási kérelmek és házirendek használhatók a szervezeti kiadások kezeléséhez. Ha például a szervezet olyan rögzített árú projekten dolgozik, amelyhez utazás szükséges, a projektcsoporttagok utazási költségeinek a projekt költségvetéséhez kell illeszkednie. Ha megköveteli, hogy az utazási költségeket a felszámításuk előtt jóvá kell hagyni, a szervezet segíthet annak biztosításában, hogy a projekt a költségvetésen belül maradjon.

## <a name="configuration"></a>Konfigurálás 

Az utazási kérelmek a „kötelezőként” állíthatók be, ha engedélyezi „Az utazás előzetes engedélyezése kötelező” paramétert a Költségkezelés paraméterei részben. 

## <a name="create-and-submit-a-travel-requisition"></a>Utazási kérelem létrehozása és elküldése

1. Válassza a **Saját kiadások: Utazási kérelem** lehetőséget, és válassza az **Új utazási kérelem** elemet.
2. Adja meg a kérelem célját és úti célját.
3. Az **Utazás leírása** mezőben adja meg a további adatokat. 
4. Az egyes várt kiadások, például a repülés, az étkezés vagy az autókölcsönzés esetén hozzon létre egy költségsortételt. Adja meg a becsült dátumot, a becsült összeget és az egyes kiadások pénznemét. 
5. Amikor befejezte a várható kiadások hozzáadását, válassza a **Mentés** lehetőséget.
6. Amikor készen áll az utazási kérelem elküldésére, válassza a **Munkafolyamat** > **Küldés** lehetőséget.

A jóváhagyott utazási kérelmeket a **Saját kiadások: Utazási kérelem** alatt tekintheti meg. 

## <a name="view-available-travel-requisitions"></a>Rendelkezésre álló utazási kérelmek megtekintése

Az összes jóváhagyott utazási kérelmeket a **Saját kiadások: Utazási kérelmek** alatt tekintheti meg.

## <a name="approve-travel-requisitions"></a>Utazási kérelmek jóváhagyása

Válassza ki a jóváhagyni kívánt utazási kérelmet, majd jelölje ki a **Munkafolyamat** > **Jóváhagyás** lehetőséget.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Költségjelentés elküldése a jóváhagyott utazási kérelem használatával

1. Hozzon létre egy új költségjelentést, és a költségjelentés fejlécében és a jóváhagyott utazási kérelmek listájából válassza a **Leképezés utazási kérelemre** lehetőséget.
2. Az **Utazási kérelem összege** mező automatikusan frissül a költségjelentés fejlécében.
3. Vegyen fel minden utazással kapcsolatban felmerült költséget. Ha az **Előre engedélyezett** mező engedélyezve van, akkor a program frissíti az adott költségkategóriához tartozó egyeztetett összeget és engedélyezett összeget.

> [!NOTE]
> Ha egy költségjelentést jóváhagyott utazási kérelemhez képez hozzá, a tranzakció összege nem lehet nagyobb, mint az engedélyezett összeg. 
