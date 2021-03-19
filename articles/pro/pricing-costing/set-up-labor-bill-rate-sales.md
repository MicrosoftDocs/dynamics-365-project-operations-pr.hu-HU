---
title: A munka számlázási arányának beállítása – Lite
description: Ez a témakör a Project Operationsban a munkaszámlázási díjak beállításával kapcsolatban tartalmaz tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 733b7c83de8137aba6c084d5f03a2a4cf076a16c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274416"
---
# <a name="set-up-labor-bill-rates---lite"></a>A munka számlázási arányának beállítása – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Minden árlistához tartalmaz egy sor szerepkörárakt vagy munkabérdíjat, amelyek hatályosak az árlistafejlécen szereplő környezetnek és esedékességi dátumának megfelelően. A Dynamics 365 Project Operations időre vonatkozó számlázási árfolyamai csak egy pénznemben állíthatók be, ez az Árlista fejlécében található pénznem.

1. Az értékesítési árak listáján szereplő munkabérdíjak beállításához az árlista fejléce alapján hozzon létre egy árlistát. 
2. A **Szerepkörárak** lap részrácsában válassza az **+ Új szerepkörár** lehetőséget. 
3. A **gyors létrehozás** ablaktáblában adja meg azt a szerepkört és szervezeti egységet, amelyhez be kell állítania a számlázási rátát.

  Az alábbi táblázat az **általános** lap és a **gyors létrehozás** ablaktáblájának mezőit tartalmazza, amelyeket érdemes szem előtt tartani, amikor értékesítési árlistát hoz létre a szerepkör-árakon:

  | Mező | Hely | Adatfolyam leírása | Alsóbb rétegbeli hatás |
  | --- | --- | --- | --- |
  | Szerepkör | **Általános** lap és a **Gyorslétrehozás** panel | Válassza ki azt a szerepkört, amelynek számlázási értékét meg szeretné szabni. | A bejövő becslésen vagy a tényleges értéken szereplő szerepkört ezzel a sorral kell összehangolni a szerepkör alapértelmezett számlázási díjának meghatározásához. |
  | Erőforrás-kezelő részleg | **Általános** lap és a **Gyorslétrehozás** panel | Válassza ki azt a szervezeti egységet vagy részleget a vállalattól, ahonnan ez a szerepkör származik. Például a Fabrikam India robotikai divíziójának fejlesztője vagy a Fabrikam USA szoftveres divíziójának fejlesztője. | A bejövő becslésen vagy a tényleges értéken szereplő erőforrás-kezelő egységet ezzel a sorral kell összehangolni a szerepkör alapértelmezett számlázási díjának meghatározásához. |
  | Ár | **Általános** lap és a **Gyorslétrehozás** panel | Állítsa be a szerepkör, az erőforrás-kezelő vállalat és az erőforrás-kezelő egység kombinációjának számlázási díját. Például a Fabrikam India fejlesztője számlázási díja 100 USD, vagy a Fabrikam USA egyik fejlesztője számlázási díja 150 USD. | Ez az ár azt a alapértelmezett számlázási díjat adja meg, amely a bejövő becslés vagy a tényleges sor egységnyi költségére érvényes az Idő tranzakciós osztályban. |
  | Pénznem | **Általános** lap és a **Gyorslétrehozás** panel| A pénznem értéke alapértelmezés szerint az értékesítési árlista fejlécében szereplő pénznemből származik. Az értékesítési árlistán a pénznemet nem lehet felülírni. | Ez a pénznem azt a alapértelmezett pénznemet adja meg, amely a bejövő tényleges értékesítési sor egységnyi árára érvényes az Idő tranzakciós osztályban. |
  | Egységütemezés | **Általános** lap és a **Gyorslétrehozás** panel | Az egység ütemezése alapértelmezés szerint Idő, és nem módosítható a szerepkörár entitáson, mert a rendszer időegységekkel kifejezett árfolyamot alkalmaz. | Ennek a mezőnek nincs későbbi hatása. |
  | Kiszerelés | **Általános** lap és a **Gyorslétrehozás** panel | Az egység értéke szerint az értékesítési árlista fejlécében szereplő **Időegység** értékéből származik. De az érték felülbírálható. Például a Fabrikam India fejlesztőinek számlázási díja 1000 USD **indiai naponként**. A Fabrikam USA fejlesztője 1500 USD számlázási rátával rendelkezik **amerikai naponként**. | A rendszer az egységek rendszerét és a alapegységekre való átváltást használja az egységnyi költség kiszámításához, amely meghatározza az alapértelmezett egységárat a bejövő becslések vagy a tényleges sorok esetében. Például a becslés 10 **indiai nap** mennyiségű munkára vonatkozik egy indiai fejlesztőnél, és az egység, indiai nap meghatározása szerint 10 órát jelent. A becslési sor árazásakor az alkalmazás óránként kiszámítja a becslésben szereplő egységárat 1000 USD/10 óra = 100 USD per óra értékben. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Az transzferárazás vagy a számlázási ráták beállítása más szervezeti egységből vagy divízióból származó erőforrásokhoz 

A projektalapú vállalatoknál a vállalat különböző részlegeinek alkalmazottainak használata projekteken. A projektek végrehajthatók az egyik divízióból, miközben az alkalmazottak vagy a tanácsadók ugyanabból vagy másik vállalati divízióból származnak. A projekt a különböző divízióból származó emberek kombinációjára is kialakítható. A Project Operationsban a projekt teljesítését birtokló vállalat neve a **szerződő egység**. Az erőforrásokat biztosító összes többi divíziót **Erőforrás-kezelő egységnek** nevezzük. A különböző földrajzi és munkaerőpiaci költségekben mutatkozó különbségek miatt a világ minden részén a munka számlázási díja is másképpen a különböző földrajzi helyekre van beállítva.

Például a Fabrikam India egyik fejlesztője, aki egy amerikai projekten dolgozik, kiszámlázhat 100 USD óránkénti árfolyamon. A Fabrikam US egyik fejlesztője, aki egy amerikai projekten dolgozik, kiszámlázhat 150 USD óránkénti árfolyamon.

### <a name="example-set-up-a-bill-rate"></a>Példa: számlázási ráta beállítása

1. Hozzon létre egy értékesítési árlistát a *Fabrikam US számlázási ráták* néven, és állítsa be az érvényességi dátumot.
2. Az értékesítési árlapon adja meg a következő díjadatokat:

    | Szerepkör | Szervezeti egység | Számlázási díj |
    | --- | --- | --- |
    | Fejlesztői | Fabrikam India | 100 dollár |
    | Fejlesztői | Fabrikam-Fülöp-szigetek | $90 |
    | Fejlesztői | Fabrikam US | $150 |

3. Csatolja az értékesítési árlistát, a **Fabrikam US számlázási rátáit** a projektszerződés vagy egy bizonyos Partner projektárlistájához.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]