---
title: Helyesbítő projektalapú számlák
description: Ez a témakör információt nyújt arról, hogyan hozhat létre és erősíthet meg helyesbítő projektalapú számlákat a Project Operations szolgáltatásban.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997159"
---
# <a name="corrective-project-based-invoices"></a>Helyesbítő projektalapú számlák

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A megerősített projekt számlát ki lehet javítani az ügyféllel és a projektmenedzserrel egyeztetett változtatások vagy jóváírások feldolgozásához.

Ha a visszaigazolt számlán szeretne módosításokat készíteni, nyissa meg a visszaigazolt számlát, és válassza a **Számla helyesbítése** lehetőséget. 

> [!NOTE]
> Ez a kiválasztás csak akkor érhető el, ha a projektszámlát megerősítik, vagy ha a projektalapú számlán előlegek vagy foglalók, illetve előlegek vagy foglalók egyeztetése található.

Az új vázlat állapotú számlát a visszaigazolt számla alapján hozza létre a rendszer. A rendszer a korábban visszaigazolt számla minden számlázási adatait átmásolja az új vázlatba. Az alábbiakban néhány olyan alapvető szempontot talál, amelyek fontosak az új helyesbített számla soradataival kapcsolatosan.

- Minden mennyiség nullára van frissítve. A Dynamics 365 Project Operations azt feltételezi, hogy az összes számlázott cikk teljes mértékben jóváírandó. Ha szükséges, manuálisan frissítheti ezeket a mennyiségeket, hogy azok a számlázott mennyiséget tükrözzék, és nem a jóváírt mennyiséget. A megadott mennyiség alapján az alkalmazás kiszámítja a jóváírt mennyiséget. Ez az összeg jelenik meg a helyesbített számla megerősítését követően létrehozott tényadatokban. Ha módosítja az adó összegét, akkor meg kell adnia a helyes adót, és nem a jóváírt adó összegét.
- A mérföldkő-helyesbítéseket a rendszer mindig teljes jóváírásként dolgozza fel.


> [!IMPORTANT]
> Azoknál a számlasor részleteknél, amelyek már más, számlázott költségek helyesbítései, a **Helyesbítés** mező **Igen** értékre van állítva. Azoknál a számláknál, amelyek helyesbített számlasor részletekkel rendelkeznek, a **Helyesbített** mező **Igen** értékre van állítva.

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
Ez a forgatókönyv nem támogatott.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
