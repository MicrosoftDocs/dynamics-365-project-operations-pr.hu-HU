---
title: Rögzített árú bevétel becslési projektjei
description: Ez a témakör információkat nyújt rögzített áru bevételekről a projektekben.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013804"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Rögzített árú bevétel becslési projektjei 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Amikor létrehoz egy projektszerződés-sort a következő attribútumokkal a Dynamics 365 Project Operations alkalmazásban a Microsoft Dataverse alatt, a rendszer automatikusan létrehoz egy rögzített árú bevételbecslési projektet. A projektben szereplő információk a következőkön alapulnak:

  - Rögzített árú számlázási módszer.
  - Egy társított projekt.
  - Legalább egy definiált mérföldkő a **Projekt-szerződéssor** lap **Számla ütemezés** lapján.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Rögzített árú bevétel becslési projektek ellenőrzése
A rögzített árú bevételbecslési projektek áttekintéséhez hajtsa végre a következő lépéseket:

1. A Dynamics 365 Finance környezetben nyissa meg a **Projektvezetés és könyvelés** > **Projektek** > **Rögzített árú bevételbecslési projektek** lehetőséget.
2. Jelölje ki a megtekinteni kívánt projektet, és kattintson duplán a **Projektbecslés azonosítójára** a bejegyzés megnyitásához, és tekintse át a projekt részleteit.
3. Bontsa ki a **Projekt** lapot. A **Kijelölt projektek** rácsán egy projekt jelenik meg. A rendszer ezt használja alapértelmezett projektként, mert a projekt szerződéssorához társított projekt. 
4. A társítás módosításához válasszon ki további projekteket, és vegye fel őket a **Kijelölt projektek** rácsára. Ha ebben a táblázatban több projektet is kijelöl, a projekt százalékos készültségi szintjét és a bevételi becsléseket a program az összes kijelölt projekthez együttesen számítja ki.

  A projekt költségét, a bevételi profilt, a költségsablont és az időszak kódját manuálisan is megadhatja. Ha nem állítanak be manuálisan beállítást, akkor az értékek alapértelmezésre állnak a projekt első becslési számításaiban a projekt költség-és bevételi profiljaihoz beállított szabályok szerint.



[!INCLUDE[footer-include](../includes/footer-banner.md)]