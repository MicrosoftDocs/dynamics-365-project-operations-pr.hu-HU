---
title: Személyes kiadások egy költségjelentésen
description: Ez a témakör ismerteti, hogyan lehet kezelni a dolgozók személyes kiadásait a Microsoft Dynamics 365 Finance szolgáltatásban.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078241"
---
# <a name="personal-expenses-on-an-expense-report"></a>Személyes kiadások egy költségjelentésen

[!include [banner](../includes/banner.md)]

Az üzleti utazás során a dolgozók néha személyes kiadásokat is terhelhetnek a vállalati hitelkártyákra. Ha nem határoz meg a személyes kiadások kezelésére szolgáló folyamatot, akkor előfordulhat, hogy a költségjelentés jóváhagyási folyamata megszakad, amikor a munkavállalók elküldik a részletezett Költségjelentéseket. 

A dolgozók személyes költségeinek kezeléséhez két módszer áll rendelkezésre:

- **Alkalmazott által fizetendő** - A szervezet nem fizeti ki a személyes költségeket, amelyek megjelennek a vállalati hitelkártya számláján. Ehelyett létrehoz egy jelentést, amely megjeleníti a személyes költségeket a vállalati hitelkártyára terhelt vállalati kiadásokkal együtt.
- **Vállalat által fizetendő** - A szervezet kifizeti a vállalati hitelkártya teljes számláját, majd levonja a dolgozó számlájáról a személyes kiadásokat.

Megadhatja, hogy a szervezet milyen módszert használ a **költségkezelési paraméterek** lapon.
