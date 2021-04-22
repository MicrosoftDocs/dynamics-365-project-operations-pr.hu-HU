---
title: Projektalapú helyesbítő számlák létrehozása
description: Ez témakör a Project Operations szolgáltatásban lévő helyesbítő számlákról nyújt információt.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788864"
---
# <a name="create-corrective-project-based-invoices"></a>Projektalapú helyesbítő számlák létrehozása 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.

Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget. 

> [!NOTE]
> Ez a beállítás csak akkor érhető el, ha a projektszámlát megerősítik.

Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer. A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba. Az alábbiakban néhány fontos szempontot talál, amelyek segítenek jobban megérteni az új helyesbített számla sorrészleteit:

- Minden mennyiség nullára van frissítve. Ez azt feltételezi, hogy az összes számlázott cikk teljes mértékben jóváírandó. Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget. A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget. Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban. Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.
- A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.
- A foglaló vagy az előleg összegét korrigálni lehet, ha az ügyfél nem megfelelő összeget számlázott.
- A foglalók és az előlegek egyeztetése korrigálható, ha nem megfelelő összeget használtak a díjak egyeztetésére egy előzőleg visszaigazolt számlán.

> [!IMPORTANT]
> Azon számlasor részleteknél, amelyek más, számlázott költségek helyesbítései, a **Helyesbítés** mező **Igen** értékre van állítva. A helyesbített számlasor adatait tartalmazó számlákhoz egy **Helyesbítésekkel rendelkezik** mező is tartozik, amelynek értéke szintén **Igen**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>A helyesbítő számla megerősítésével létrehozott tényadatok

Az alábbi tábla azokat a tényadatokat sorolja fel, amelyek a helyesbítő számla visszaigazolásakor jönnek létre.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Forgatókönyv</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
A számlázott előleg vagy a foglaló korrekciójának megerősítése.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva. Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell visszavonni.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A kiszámlázott értékesítési sztornírozás tényleges adata jön létre a foglaló vagy előleg összegéhez az eredeti számlázott értékesítés sztornírozásához.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A rendszer egy új számlázott értékesítési tényadatot hoz létre a foglaló vagy előleg helyesbített összegéhez a javított számlasoron.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A nem számlázott negatív mennyiségű tényleges értékesítés a foglalón vagy előlegen alapuló helyesbített számlasor, amelyet a rendszer az egyeztetéshez használni fog.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
A korábban egyeztetett foglaló vagy előleg helyesbítésének megerősítése.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva. Ez az összeg pozitív, és a foglaló vagy az előleg egyeztetésekor létrejött negatív értéket kell visszavonni.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A számlázott értékesítés tényleges sztornírozása az előző számla összegéhez.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A rendszer egy új számlázott tényleges értékesítést létre a foglaló helyesbített összegéhez, ami alkalmazva van a javított számlán.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló vagy előleg javított maradékából, amelyet a rendszer az egyeztetéshez használni fog.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Egy korábban számlázott időtranzakció teljes jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegére vonatkozó új nem számlázott tényleges értékesítés az idő esetében.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Egy részleges jóváírás számlázása egy időtranzakcióban.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása az idő esetében.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy új, nem számlázott tényleges értékesítés, amely a hátralévő órákra és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Egy korábban számlázott költségtranzakció teljes jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a kiadáshoz.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének új nem számlázott tényleges értékesítése.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Egy korábban számlázott költségtranzakció részleges jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása egy kiadáshoz.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a helyesbített számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy új, nem számlázott tényleges értékesítés, amely a hátralévő mennyiségre és az összegre felszámolható, a helyesbített értékek levonása után a számlasor részleteiben.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Egy korábban számlázott díjtranzakció teljes jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása a díjhoz.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének díjának új nem számlázott tényleges értékesítése.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Egy korábban számlázott díjtranzakció részleges jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés mennyiségének összegének sztornírozása díjhoz.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a javított, helyesbítő számlasoradatokhoz, ennek helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Egy korábban számlázott mérföldkő teljes jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Az eredeti számlasor részleteire vonatkozó számlázott értékesítés összegének sztornírozása a mérföldkőhöz.
                </p>
                <p>
A mérföldkő számlaállapota a <b>Közzétett ügyfélszámla</b> értékről <b>Számlázásra kész</b> állapotra frissül.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Egy korábban számlázott mérföldkő részleges jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem támogatott </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
