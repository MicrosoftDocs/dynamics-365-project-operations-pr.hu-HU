---
title: Proforma számla megerősítése
description: Ez a témakör a proforma számlák jóváhagyását ismerteti.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287871"
---
# <a name="confirm-a-proforma-invoice"></a>Proforma számla megerősítése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz. A számla megerősítését követően csak olvasható lesz. Ezután a számla csak akkor helyesbíthető, ha ügyfél által kezdeményezett helyesbítések vagy jóváírások vannak, vagy ha kifizetettként van megjelölve.

A következő táblázat a rendszer által létrehozott tényleges adatokat sorolja fel. A rendszer ezeket a tényleges adatokat akkor hozza létre, amikor bizonyos műveleteket végrehajtanak a projekt vázlat állapotú számláján a jóváhagyás előtt.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Forgatókönyv</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>A jóváhagyáskor létrehozott tényleges adatok</strong>
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
Az új, nem számlázott tényleges értékesítés, amely felszámítható az órákhoz és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó órákhoz a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a nem számlázott ténylege értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
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