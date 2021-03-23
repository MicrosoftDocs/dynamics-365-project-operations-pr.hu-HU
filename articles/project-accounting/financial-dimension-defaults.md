---
title: A pénzügyi dimenzió alapértelmezései
description: Ez a témakör a pénzügyi dimenzió alapértelmezéseinek beállításával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287376"
---
# <a name="financial-dimension-defaults"></a>A pénzügyi dimenzió alapértelmezései

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

A Dynamics 365 Project Operations a [Pénzügyi dimenziók](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) keretrendszert használja a Dynamics 365 Finance alkalmazásban, hogy betekintést nyújtson a projektek alkönyvei és a főkönyvek tranzakcióiba.

Az alapértelmezett pénzügyi dimenziókat az ügyfél, a projekt finanszírozása, a mérföldkő, a projekt szerződéssor vagy a projekt szintjén lehet beállítani.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Az ügyfél alapértelmezett pénzügyi dimenzióinak definiálása

Az ügyfelek dimenzióinak alapértékei a Finance-ben vannak meghatározva. A dimenziók alapértelmezéseinek beállításához hajtsa végre az alábbi műveleteket.

1. Nyissa meg a **Kinnlevőségek** > **Ügyfelek** > **Összes ügyfél** menüpontot.
2. Az **Ügyfelek** lap **Pénzügyi dimenziók** fülén állítsa be adott ügyfél pénzügyidimenzió-értékeit.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Az projektszerződések alapértelmezett pénzügyi dimenzióinak definiálása

A projektszerződések a Common Data Service (CDS) szolgáltatásban hozhatók létre és tarthatók karban. A projektszerződések számlázási attribútumait a **Projektmenedzsment és könyvelés** modulban lehet beállítani a Finance-ben.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Pénzügyi dimenziók beállítása a projektek finanszírozási forrásaihoz

1. Lépjen a **Projektvezetés és könyvelés** > **Projektek** > **Projektszerződések** elemre.
2. Jelölje ki a frissíteni kívánt rekordot, majd a **Projektszerződés** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.
3. Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Finanszírozási források** lapot.
4. Állítsa be a pénzügyi dimenzió alapértelmezéseit. Figyelje meg, hogy a pénzügyi dimenziók alapértelmezései az ügyfélfiókból származnak.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Pénzügyi dimenziók beállítása a projektszerződés-sorhoz

1. Lépjen a **Projektvezetés és könyvelés** > **Projektek** > **Projektszerződések** elemre.
2. Jelölje ki a frissíteni kívánt rekordot, majd a **Projektszerződés** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.
3. Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Szerződéssorok** lapot.
4. Állítsa be a pénzügyi dimenzió alapértelmezéseit. A pénzügyi dimenzió alapértelmezései érvényesek, és csak rögzített áras (mérföldkő) szerződéssorokhoz használhatók.

Ezek az alapértelmezések a kapcsolódó projekt számlatranzakciói és számlasorai esetén használhatók.

## <a name="define-default-financial-dimensions-for-projects"></a>Az projektek alapértelmezett pénzügyi dimenzióinak definiálása

A projektek CDS szolgáltatásban hozhatók létre és tarthatók karban. A projektek számlázási attribútumait a **Projektmenedzsment és könyvelés** modulban lehet beállítani a Finance-ben.

1. Lépjen a **Projektmenedzsment és könyvelés** > **Projektek** > **Minden projekt** elemre.
2. Jelölje ki a frissíteni kívánt rekordot, majd a **Projekt** lapon válassza az **Alapértelmezett könyvelés megjelenítése** jelölőnégyzetet.
3. Bontsa ki a **Kapcsolódó információk** elemet, és válassza ki a **Beállítások** lapot.
4. Állítsa be a pénzügyi dimenzió alapértelmezéseit. Figyelje meg, hogy a pénzügyi dimenziók alapértelmezései az ügyfélfiókból származnak. Ha a projekt olyan szerződéssorhoz van társítva, amely több szerződésese ügyfelet tartalmaz, akkor az elsődleges ügyfél lesz használva a pénzügyi dimenzió alapértelmezéseiben.

A projekt alapértelmezett pénzügyi dimenziói az idő-, költség-és díj tranzakciók naplósorai alapértelmezéseinek beállítására szolgálnak a **Project Operations integrációs naplóban** és a kapcsolódó projektszámla-sorokban.


[!INCLUDE[footer-include](../includes/footer-banner.md)]