---
title: Költségházirendek beállítása
description: Meghatározhatók olyan költségszabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor a Microsoft Dynamics 365 Finance szolgáltatásban.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960700"
---
# <a name="set-up-expense-policies"></a>Költségházirendek beállítása

Meghatározhatók olyan szabályzatok, amelyeket a dolgozóknak be kell tartaniuk a költségjelentések és az utazási igénylések megadásakor és elküldésekor.         
A költségszabályzatokkal hatékonyan kezelheti a költségeket.         

Beállíthat például egy szabályzatot egy New York Cityben lévő szálloda kiadásaihoz, amely előírja, hogy az éjszakánkénti költség nem haladhatja meg a 250 USD-t.       
Ha egy dolgozó olyan költségjelentést vagy utazási igénylést nyújt be, ahol a szobaár meghaladja ezt az összeget, a rendszer értesíti a        
dolgozót, hogy túllépte a költségre vonatkozó szabályzatban szereplő összeget. A szabályzat meghatározásakor állíthatja be,        
hogy a dolgozó milyen üzenetet kapjon.      
        
Háromféle szabályzat hozható létre:         
        
- Figyelmeztetés: A dolgozó beküldheti a költségjelentést vagy az utazási igénylést, de a rendszer minden jóváhagyó számára megjelöli a költséget        
  a későbbi jelentéskészítéshez.        

- Hiba: A dolgozónak a költségjelentés vagy az utazási igénylés elküldése előtt úgy kell módosítania a költséget, hogy megfeleljen a szabályzatnak.       
 
 - Indoklás: A dolgozónak vagy a vezetőnek a költségjelentés vagy az utazási igénylés elküldése előtt indokolnia kell, hogy miért lépte túl a szabályzatban szereplő összeget.        

## <a name="policy-tips"></a>Szabályzatra vonatkozó tippek
Az alábbiakban néhány olyan javaslatot talál, amely segíthet a költségkezelés új szabályzatainak létrehozásában. 
* A szabályzatok az adott napon lépnek hatályba, és a költség dátuma után létrehozott szabályzat nem érvényes az adott költségek esetén. Ha például egy új házirendet hoz létre ma, hogy kikényszerítse a $50 maximális étkezési költséget, akkor a tegnap bevitt összes költséget nem kell ellenőrizni ezzel a házirenddel kapcsolatban.
* Ha tételezhető költségkategóriára vonatkozó szabályzatot hoz létre, érdemes lehet feltételt hozzáadni a költségsor típusához. Előfordulhat, hogy bizonyos szabályzatok, például a kötelező nyugta, nem feltétlenül hasznos a részletezett sorokhoz, és csak a fejlécsorra vagy egy nem részletezett sorra alkalmazhatók. 
* A költségkezelési szabályzatokat a rendszer alapértelmezés szerint a forrásentitáshoz képest értékeli ki. Vállalatközi forgatókönyvek esetén beállíthatja, hogy a szabályzatot a célentitáshoz (átvevő entitás) képest értékelje a rendszer. Ha a célentitáshoz szeretne szabályzatokat futtatni, kapcsolja be a „Költségszabályzat értékelése az átvevő jogi személyhez képest” szolgáltatást a **Funkciókezelés** munkaterületen.

## <a name="when-to-evaluate-policies"></a>Mikor kell értékelni a szabályzatokat?

A költségkezelési paraméterek között kiválaszthatja, hogy a program csak egy sor mentésekor vagy a költségjelentés elküldésekor értékelje ki a költségkezelési szabályzatokat. Ha a sorok mentésekor történő kiértékelést választja, akkor ez biztosítja, hogy a felhasználók korábban minden olyan részletet láthatnak, amit tenniük kell a költségjelentés végrehajtásához. Ellenkező esetben késleltetheti a szabályzat kiértékelését, és időt takaríthat meg, ha a befejezést követően, a beküldéskor kerül sor a munkafolyamat ellenőrzésére.
