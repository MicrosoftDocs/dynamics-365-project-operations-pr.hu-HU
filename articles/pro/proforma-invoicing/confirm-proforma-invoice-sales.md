---
title: Proforma számla megerősítése – Lite
description: Ez a témakör a proforma számlák a Project Operations alkalmazásban való megerősítéséről nyújt tájékoztatást.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176524"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Proforma számla megerősítése – Lite

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_


A proforma számla megerősítését követően a projektszámla- frissítések állapota **Megerősítve** lesz. A számla megerősítését követően csak olvasható lesz. Ezután a számla csak akkor helyesbíthető, ha ügyfél által kezdeményezett helyesbítések vagy jóváírások vannak, vagy ha a számla kifizetettként van megjelölve.

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
A nem számlázott negatív mennyiségű tényleges értékesítés a foglaló, amelyet a rendszer az egyeztetéshez használni fog.
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
Az új, nem számlázott tényleges értékesítés, amely nem felszámítható a fennmaradó órákhoz a javított értékek levonását követően és összeghez a szerkesztett számlasoradatokhoz, a tényleges értékesítés helyesbítése, és egy ennek megfelelő számlázott tényleges értékesítés.
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
Számlázott tényleges értékesítés mennyiségéhez és összegéhez az eredeti költségjóváhagyásra </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Termékalapú szerződéssor számlázása.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
A terméksorhoz tartozó számlázott értékesítés, a termék alapú szerződéssorból származó mennyiséggel és összeggel.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]