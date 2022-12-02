---
title: Projektalapú proforma számla megerősítése
description: Ez a cikk a proforma projektalapú számlák megerősítéséről nyújt információt.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a4ad243e8959af61993e2ff6ce89209be378f7df
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929447"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Projektalapú proforma számla megerősítése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz. A számla megerősítését követően csak olvasható lesz. A jövőben a számla csak akkor helyesbíthető, ha vannak ügyfél által kezdeményezett helyesbítések vagy jóváírások.

A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel. A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.

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
Foglaló vagy előleg számlázása </p>
            </td>
            <td width="408" valign="top">
                <p>
A <strong>Foglaló</strong> típusú számlázott tényleges értékesítés az előleg vagy a foglaló összegéhez van létrehozva.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Azokat a nem számlázható értékesítési tényadatokat, amelyek negatív összegű foglalóval vagy előleggel rendelkeznek, egyeztetéshez kell használni.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Egy foglaló vagy előleg teljes körű egyeztetése után a számlán.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva. Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy számlázott tényleges értékesítés ezen számla összegéhez.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Egy foglaló vagy előleg részleges egyeztetése után a számlán.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A foglaló vagy előleg nem számlázott értékesítésének sztornírozása, ami egyeztetéshez lett létrehozva. Ez az összeg pozitív, mert a foglaló vagy az előleg számlázásakor létrejött negatív értéket kell kiegyenlítenie.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy számlázott tényleges értékesítés ezen számla összegéhez.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A nem számlázott negatív tényleges értékesítés a fennmaradó foglaló vagy előleg összegéhez, amelyet a rendszer az egyeztetéshez fog használni a későbbi számlákon.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Az időtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Számlázott tényleges értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
A mennyiség csökkentéséhez módosított időtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Egy új, nem számlázott értékesítési tényadat nem számítható fel a hátralévő órákra és összegre, miután levonta a helyesbített összegeket a szerkesztett számlasor részleteiből, az értékesítés tényleges sztornírozásából és az azzal egyenértékű számlázott értékesítésből.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
A mennyiség növeléséhez módosított időtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés összegének sztornírozása az eredeti jóváhagyási időpontra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Az költségtranzakciók számlázása szerkesztés nélkül vázlat állapotú számlára.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
A mennyiség csökkentéséhez módosított költségtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
A mennyiség növeléséhez módosított költségtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés mennyiségének és összegének sztornírozása az eredeti költségjóváhagyásra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Anyagtranzakció számlázása a számlatervezet szerkesztése nélkül.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti anyaghasználati jóváhagyáson.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
A mennyiség és az összeg számlázott értékesítési tényadat az eredeti anyaghasználati jóváhagyáson.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
A mennyiség csökkentése érdekében szerkesztett anyagtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti időjóváhagyáson.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó mennyiséghez a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
A mennyiség növelése érdekében szerkesztett anyagtranzakció számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A mennyiség és az összeg nem számlázott értékesítési sztornírozása az eredeti anyaghasználati jóváhagyáson.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely felszámítható a mennyiséghez és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Díj számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nem számlázott értékesítés díjösszegének sztornírozása az naplósoron.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti díj naplósorán.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Mérföldkő számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Számlázott tényleges értesítés a projektszerződés eredeti mérföldkövén a mérföldkő mennyiségéhez.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
