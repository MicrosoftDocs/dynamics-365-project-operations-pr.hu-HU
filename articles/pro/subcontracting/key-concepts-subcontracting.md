---
title: Az alvállalkozói szerződéskötés kulcsfogalmai
description: Ez a cikk néhány kulcsfontosságú fogalmat ismertet, amelyek a Microsoft alvállalkozásba adására vonatkoznak Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e75f2cf9c1092604e43e5cb60dda0e2a1b7dcd64
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262172"
---
# <a name="key-concepts-in-subcontracting"></a>Az alvállalkozói szerződéskötés kulcsfogalmai


_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

A cikk néhány kulcsfontosságú fogalmat ismertet, amelyekkel tisztában kell lennie, mielőtt elkezdené használni a Microsoft alvállalkozói funkcióját Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Szerződéskötési egység az alvállalkozói szerződésen

A szerződéskötési egység azt a részleget vagy eljárást jelképezi, amelynek a projekt teljesítése a tulajdonában van. A szerződéskötési egység egyben az a részleg is, amely a szállítóval szerződéses kapcsolatba kerül.

## <a name="purchase-currency"></a>Beszerzési pénznem

A Project Operations alkalmazásban a beszerzési pénznem az a pénznem, amelyben az alvállalkozói szerződés létre van hozva. Ez egyben az a pénznem, amelybe a projekttel alvállalkozói költségeit rögzítik. A beszerzési pénznem eltérhet a projekt pénznemétől, és a projekt pénzneme pedig eltérhet az értékesítési pénznemtől.

## <a name="billing-methods-on-subcontract-lines"></a>Számlázási módszerek alvállalkozói sorokon

A projektek esetében jellemzően rögzített árú és fogyasztásalapú szerződési modellek vannak. A Project Operations az értékesítési és vásárlási környezetben támogatja ezeket a számlázási módszereket. Beszerzés esetén a számlázási módszerek a következők szerint működnek:

- **Idő és anyag** – Ha egy alvállalkozói sor az **Idő és anyag** számlázási módot használja, akkor a projekten az időköltséget alvállalkozói munkaként rögzíti a rendszer az adott projekthez, és rögzíti az időt. Ezt követően az alvállalkozóktól származó költségtranzakciókat a rendszer megfelelteti a szállítói számlákon szereplő sorelemeknek. Ebben a modellben a Project Operations alkalmazást használó projektmenedzserek a szállító számla sorait megegyeztetik és ellenőrizhetik az alvállalkozó által rögzített és jóváhagyott időpontokkal. Az ellenőrzés befejezése után a jóváhagyás után rögzített korábbi költség-tényadatokat a rendszer visszavonja, és a projektben a szállító számláján alapuló új költség-tényadatokat hoz létre a rendszer.
- **Rögzített ár** – Ebben a rögzített árú szerződéskötési modellben a szállítói számlák rögzített mérföldköveken alapulnak. Az alvállalkozói erőforrások azonban időt is jelenthetnek. Ezt követően a projektmenedzser áttekinti és jóváhagyja ezt az időt. Jóváhagyáskor a Project Operations ideiglenes költség-tényadatokat hoz létre a projekten. Miután az szállító számlát küld egy mérföldkövről, a projektvezető a korábban rögzített tényleges költségeket megfeleltetheti a mérföldkőhöz. Az ellenőrzés befejezésekor a rendszer visszavonja a költség tényadatokat, és rögzíti a mérföldkövekalapú költségeket.

## <a name="project-price-lists-on-subcontracts"></a>Projektárlisták alvállalkozói szerződésekhez

A projektárlisták olyan árlisták, amelyek az idő, a költség és a projekthez kapcsolódó egyéb összetevők beszerzési árának beállítására használhatók. Több árlista is lehet, amelyek mindegyikéhez saját hatályossági dátummal rendelkező alvállalkozói szerződése a lehet a Project Operations alkalmazásban. A Project Operations nem támogatja a projektárlisták dátumának átfedő hatályosságát alvállalkozói szerződéshez.

## <a name="transaction-classes-on-subcontracts"></a>Alvállalkozói szerződések tranzakcióosztályai

A Project Operations négyféle típusú tranzakciót támogat:

- Idő
- Költség
- Anyag
- Díj

A beszerzési költségek csak **Idő**, **Költség** és **Anyag** tranzakcióosztályokkal becsülhetők és számíthatók fel. A **Díj** csak bevételi tranzakciós osztály, és nem érhető el a beszerzéssel kapcsolatosan.

## <a name="purchase-pricing-dimensions"></a>Beszerzés árképzési dimenziói

Az árképzési dimenziókkal megszabhatja, hogy milyen attribútumokat használ a rendszer a beszerzési ár beállításához és az időtranzakciók alapértelmezéseinél. A beszerzéssel kapcsolatban a Project Operations csak a rögzített dimenzióhalmazokat támogatja a beszerzési ár beállításához és alapértelmezéseihez. A beszerzési ár beállítása és alapértelmezései esetében az alvállalkozói szerződés soraihoz és időtranzakciókhoz az attribútumok a **Szerepkör** és a **Foglalható erőforrás**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
