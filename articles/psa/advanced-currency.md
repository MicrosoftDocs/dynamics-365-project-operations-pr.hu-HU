---
title: Több pénznemű forgatókönyvek (3.x verzió)
description: Ez a témakör több pénznemű forgatókönyvekről tartalmaz információt.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7be029eeca3129d30f4bec1bf9b180a0a5122a86
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078202"
---
# <a name="multiple-currency-scenarios"></a>Több pénznemű forgatókönyvek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A Microsoft Dynamics 365 szolgáltatásban két pénznem van:

- **Tranzakció pénzneme** – az a pénznem, amelyen a tranzakció végbe megy. 
- **Alappénznem** – a Dynamics 365 példányának pénzneme. Ez a pénznem akkor lesz beállítva, amikor kiépítenek egy Dynamics 365-példányt. Nem módosítható.

Például a Contoso US eladott 100 pólót egy vásárlónak az Egyesült Királyságban 15 font sterling (GBP) darabáron. Az alábbi táblázat azt mutatja be, hogyan történik a tranzakció rögzítése a megrendelés termékentitásában.

| Termék | Mennyiség | Kiszerelésenkénti ár | Pénznem | Összeg | Árfolyam | Egységár (alappénznem)| Összeg (alappénznem)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Póló | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1725 USD       |

A **Pénznem** oszlop a tranzakció pénznemét jeleníti meg, amely az értékesítés pénzneme. Az **Átváltási árfolyam** oszlop a tranzakció pénzneme és az alappénznem közötti átváltási árfolyam. Az alappénznem az amerikai dollár (USD). Az alappénznemet akkor álították be, amikor kiépítettek egy Dynamics 365-példányt.
A táblázat mutatja, hogy minden tranzakciót a tranzakció pénznemében és az alappénznemben kell rögzíteni. A Dynamics 365 a pénznem átváltási árfolyamán számítja ki az alappénznem összegeit.

## <a name="project-service-automation-extensions"></a>Project Service Automation-bővítmények

A Dynamics 365 Project Service Automation befolyásolja a tranzakció pénznemét, mivel az üzleti tranzakcióknak általában két szempontjuk van: költség és értékesítés.

A következő entitások üzleti tranzakcióknak számítanak:

- Árajánlatsor részletei
- Projektszerződés sorának részletei
- Becsléssor
- Naplósor
- Számlasor részletei
- Tény

A fenti entitások mindegyikében van egy rekord, amely a költség összegét vagy az értékesítés összegét jelzi. Ami az **Összeg** mezőt tartalmazó Dynamics 365-entitásokat illeti, mindegyik rekord tartalmazza a tranzakció pénznemében és az alappénznemben megadott összegeket is. 

A PSA a következőképpen bővíti ki a tranzakció pénznemének fogalmát a költség és az értékesítés szempontjából:

- Az időtranzakciók költségtranzakciós pénzneme mindig a projektet birtokló vagy kezelő szervezeti egység pénzneme. Ez a szervezeti egység, mint a szerződő részleg ismeretes.
- Az idő- és költségtranzakciók értékesítési tranzakciós pénzneme mindig a projektszerződés pénzneméből származik.
- A költségekhez használt költségtranzakció pénzneme a költségbejegyzés létrehozási pénzneméből származik.

## <a name="multiple-currency-scenario"></a>Több pénznemű forgatókönyv

Ez a rész egy olyan projekt példáját írja le, amelyet a Contoso UK a japán Fabrikam nevű ügyfél számára hajt végre. Íme a forgatókönyv létrehozása:

1. Az angol font (GBP) és a japán jen (JPY) beállítása a **Beállítások** \> **Vállalatkezelés** \> **Pénznemek** pontban. 
2. A **Fabrikam – Japan** nevű ügyfélfiók beállítása, majd a fiók pénznemeként a JPY kiválasztása.
3. A **Contoso UK** nevű szervezeti egység beállítása, majd a GBP kiválasztása pénznemként.
4. Létrejön egy projektszerződés, amelyben a **Contoso UK** szerepel szerződő részlegként, a **Fabrikam – Japan** pedig ügyfélként van megadva.
5. A projekt szerződéssorai a projekt különféle tranzakcióosztályainak számlázási megállapodásai alapján jönnek létre, például számlázás idő alapján vagy számlázás költségek alapján.
6. Projekt létrehozása, amelyben a **Contoso UK** szerepel szerződő részlegként. A projekt a projekt szerződéssoraihoz jön létre és azokhoz van leképezve.


Az árajánlatsor részleteit, a projekt szerződéssorának részleteit vagy az ütemezés becsléssorát használó becslés során a rendszer minden esetben két rekordot hoz létre az entitásban. Az egyik rekord a költségre, míg a másik az értékesítésre szolgál.

- Alapértelmezés szerint a költségrekord tranzakciós pénzneme a projekt szerződő részlegének pénznemére van beállítva. Ebben a példában a GBP a pénznem.
- Alapértelmezés szerint az értékesítési rekord tranzakciós pénzneme a projektszerződés pénznemére van beállítva. Ebben a példában a JPY a pénznem.

Amikor az időbejegyzés vagy a naplósor időpontra vonatkozó tényadatokat hoz létre, a következő viselkedés fordul elő:

- Alapértelmezés szerint a költségrekord tranzakciós pénzneme a projekt szerződő részlegének pénznemére van beállítva.
- Alapértelmezés szerint az értékesítési rekord tranzakciós pénzneme a projektszerződés pénznemére van beállítva.

Amikor a költségbejegyzés vagy a naplósor költségekre vonatkozó tényadatokat hoz létre, a következő viselkedés fordul elő:

- A költség összegét bármilyen pénznemben rögzítheti. Válassza ki a pénznemet a **Költségbejegyzés** lapon vagy a **Naplósor** lapon a pénznemválasztó segítségével. Alapértelmezés szerint az költségrekord tranzakciós pénzneme a költségbejegyzés pénznemére van beállítva. 
- Alapértelmezés szerint az értékesítési rekord tranzakciós pénzneme a projektszerződés pénzneme. A pénznem beállításához a rendszer először a felhasználó által az alappénznemhez megadott pénznemben váltja át a tranzakció összegét. Ezt követően az összeget a projektszerződés pénznemére váltja át. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Számítási összesítések a projekttényadatok több tranzakciós pénznemben történő rögzítésekor

A Dynamics 365 automatikusan kezeli a különböző pénznemekben lévő összegek összesítéseit. Íme egy példa.

| Tranzakcióosztály | Tranzakció típusa| Date   | Erőforrás | Tranzakció kategóriája | Mennyiség | Egységár | Összeg      | Árfolyam | Összeg az alappénznemben |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Számlázatlan értékesítés   | Jún. 14. | Ferenc  |                      | 8 óra    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Time              | Számlázatlan értékesítés   | Jún. 15. | Ferenc  |                      | 8 óra    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Költség           | Számlázatlan értékesítés   | Jún. 16. | Ferenc  | Szálloda                | Darabonként 1     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Költség           | Számlázatlan értékesítés   | Jún. 17. | Ferenc  | Autókölcsönzés           | Darabonként 1     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

A projekt teljes számlázatlan értékesítési értékének kiszámításához az összes kapcsolódó, számlázatlan értékesítésre vonatkozóan létrehozhat egy összesítési **Összeg** mezőt. Az összesítés mező a Dynamics 365 olyan konstrukciója, amely lehetővé teszi gyors képletek alkalmazását a kapcsolódó rekordokra.
