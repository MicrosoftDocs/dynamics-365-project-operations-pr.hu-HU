---
title: Helyesbítő projektszámlák
description: Ez a cikk arról nyújt tájékoztatást, hogyan hozhat létre és erősíthet meg helyesbítő számlákat a Project Operationsben.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e8e10d69368f4704ec6121106fbfd35394dc441
ms.sourcegitcommit: 95dacb0e74fa8970f56fdb1cbaa915d3fbec6e0f
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023662"
---
# <a name="corrective-project-invoices"></a>Helyesbítő projektszámlák

_**A következőre vonatkozik:** Egyszerű központi telepítés – proforma számlázás, Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.

Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget. 

> [!NOTE]
> Ez a beállítás csak akkor érhető el, ha a projektszámlát megerősítik.

Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer. A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba. Az alábbiakban néhány olyan alapvető szempontot talál, amelyek fontosak az új helyesbített számla soradataival kapcsolatosan.

- Minden mennyiség nullára van frissítve. Az alkalmazás feltételezi, hogy a számlázott elemek teljes mértékben jóváírásra kerülnek. Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget. A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget. Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban. Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.
- A korábban megerősített termékalapú szerződéssorok nem lesznek átmásolva. A terméken alapuló projektszámlán végzett helyesbítések feldolgozása nem támogatott.
- A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.
- A foglaló vagy az előleg összegét korrigálni lehet, ha az ügyfél nem megfelelő összeget számlázott.
- A foglalók és az előlegek egyeztetése korrigálható, ha nem megfelelő összeget használtak a díjak egyeztetésére egy előzőleg visszaigazolt számlán.

> [!IMPORTANT]
> A számlasor részletei esetében, amelyek az egyéb már számlázott díjakra vonatkozóan korrekciók a **Helyesbítés** mező **Igen** értékre van beállítva. A helyesbített számlasor adatait tartalmazó számlákhoz egy **Helyesbítésekkel rendelkezik** mező is tartozik, amelynek értéke szintén **Igen**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Helyesbítő számla visszaigazolásakor létrehozott tényadatok

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
Korábban számlázott anyagtranzakció teljes jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A mennyiség és az összeg számlázott értékesítési sztornírozása az anyag eredeti számlasorának részletein.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az mennyiség és az összeg új számlázatlan értékesítési tényadata az anyag eredeti számlasorának részletein.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Anyagtranzakció részleges jóváírásának számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A számlázott mennyiség és az összeg számlázott értékesítési sztornírozása az anyag eredeti számlasorának részletein.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy új, nem számlázott értékesítési tényadat – amely felszámítható a szerkesztett számlasor részleteiben lévő mennyiségért és összegért – sztornírozása és ezzel egyenértékű számlázott értékesítési tényadata.
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
        <tr>
            <td width="216" valign="top">
                <p>
A korábban számlázott termék alapú szerződéssor jóváírásai és helyesbítései.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem támogatott </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
