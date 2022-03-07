---
title: Költségszabályzatok definiálása
description: Meghatározhatók olyan költségszabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d29b1a9c1a935b933f403f78279b74577d11089007ce1d1090c361075822263a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986359"
---
# <a name="define-expense-policies"></a>Költségszabályzatok definiálása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

Meghatározhatók olyan szabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.         
A költségszabályzatokkal hatékonyan kezelheti a költségeket.         

Beállíthat például egy szabályzatot egy New York Cityben lévő szálloda kiadásaihoz, amely előírja, hogy az éjszakánkénti költség nem haladhatja meg a 250 USD-t.       
Ha egy dolgozó olyan költségjelentést vagy utazási igénylést nyújt be, ahol a szobaár meghaladja ezt az összeget, a rendszer értesíti a         
dolgozót, hogy túllépte a költségre vonatkozó szabályzatban szereplő összeget. A szabályzat meghatározásakor állíthatja be,        
hogy a dolgozó milyen üzenetet kapjon.      
        
Háromféle szabályzat hozható létre:         
        
- **Figyelmeztetés**: A dolgozó beküldheti a költségjelentést vagy az utazási igénylést, de a rendszer minden jóváhagyó számára megjelöli a költséget         
  a későbbi jelentéskészítéshez.        

- **Hiba**: A dolgozónak a költségjelentés vagy az utazási igénylés elküldése előtt úgy kell módosítania a költséget, hogy megfeleljen a szabályzatnak.        
 
 - **Indoklás**: A dolgozónak vagy a vezetőnek a költségjelentés vagy az utazási igénylés elküldése előtt indokolnia kell, hogy miért lépte túl a szabályzatban szereplő összeget.        

## <a name="policy-tips"></a>Szabályzatra vonatkozó tippek
Az alábbiakban néhány olyan javaslatot talál, amely segíthet a költségkezelés új szabályzatainak létrehozásában: 

- A szabályzatok az adott napon lépnek hatályba. Ez azt jelenti, hogy a költség dátuma után létrehozott szabályzat nem érvényes az adott költségek esetén. Olyan szabályzatot léptet például érvénybe, amely 50 USD értékben határozza meg a legmagasabb étkezési költséget. Az előző napon bevitt költségeket a szabályzat nem ellenőrzi.
- Ha tételezhető költségkategóriára vonatkozó szabályzatot hoz létre, érdemes lehet feltételt hozzáadni a költségsor típusához. Bizonyos szabályzatok – például a nyugták köteleővé tétele – nem feltétlenül hasznosak tételezett sorok esetén. Ebben az esetben a szabályzatot csak a fejlécsorra vagy a nem tételezett sorokra alkalmazza a rendszer. 
- A költségkezelési szabályzatokat a rendszer alapértelmezés szerint a forrásentitáshoz képest értékeli ki. Vállalatközi forgatókönyvek esetén beállíthatja, hogy a szabályzatot a célentitáshoz (átvevő entitás) képest értékelje a rendszer. Ha a célentitáshoz szeretne szabályzatokat futtatni, kapcsolja be a **Költségszabályzat értékelése az átvevő jogi személyhez képest** szolgáltatást a **Szolgáltatáskezelés** munkaterületen.

## <a name="when-to-evaluate-policies"></a>Mikor kell értékelni a szabályzatokat?

A költségkezelési paraméterek között kiválaszthatja, hogy a program csak egy sor mentésekor vagy a költségjelentés elküldésekor értékelje ki a költségkezelési szabályzatokat. Ha a sorok mentésekor történő kiértékelést választja, akkor a felhasználók korábban minden olyan részletet láthatnak, amit tenniük kell a költségjelentés végrehajtásához. Ellenkező esetben késleltetheti a szabályzat kiértékelését, és időt takaríthat meg, ha a befejezést követően, a beküldéskor ellenőrzi a munkafolyamatot.


[!INCLUDE[footer-include](../includes/footer-banner.md)]