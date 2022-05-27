---
title: A pénzügyi dimenzió alapértelmezései
description: Ez a témakör a pénzügyi dimenzió alapértelmezéseinek beállításával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579493"
---
# <a name="financial-dimension-defaults"></a>A pénzügyi dimenzió alapértelmezései

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_



Dynamics 365 Project Operations a [Dynamics 365 Finance Pénzügyi dimenziók](/dynamics365/finance/general-ledger/financial-dimensions) keretrendszerét használja, hogy további betekintést nyújtson a projekt alvállalkozásba és a főkönyvi tranzakciókba.

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
