---
title: A Project Operations jogi személyenkénti integrációjának konfigurálása
description: Ez a cikk a jogi személyenkénti integráció beállításáról a Project Operations rendszerben tartalmaz tájékoztatást.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914681"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>A Project Operations jogi személyenkénti integrációjának konfigurálása 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk végigvezeti a Dynamics 365 Project Operations jogi személyenkénti konfigurálásához szükséges lépésein.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Kapcsolja be a funkciókulcsokat Dynamics 365 Finance megoldásban

A szükséges funkciók engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. A Dynamics 365 Finance-ben lépjen a **Szolgáltatáskezelés** munkaterületre.
2. A **Funkciók listájában** keresse meg és engedélyezze a következő funkciókat:
  
    - **Több szerződéssor engedélyezése a projekthez**
    - **A Project Operations a Dynamics 365 Customer Engagement alkalmazásban engedélyezése**

> [!NOTE]
> Ha nem látható a listában a **Funkciókulcsok** elem, ellenőrizze, hogy a Finance verziója megfelel-e a minimális verziókövetelménynek (10.0.13-as alkalmazásverzió az összes minőségi frissítéssel, vagy újabb). Válassza a **Frissítések keresése** lehetőséget a funkciólista frissítéséhez.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>A Project Operations telepítési forgatókönyvének definiálása egy jogi személyhez

A Project Operations a Dynamics 365 Customer Engagement alkalmazásban jogi személy szintjén engedélyezhető. A Project Operations a Dynamics 365 Customer Engagement alkalmazásban segítségével egy jogi személlyel rendelkezhet az erőforrás/nem készletezett alapú forgatókönyvek esetén. Ugyanabban a környezetben másik jogi személy is használhatja a Project Operationst a készletezett/gyártási rendelés esetekre.

1. A Dynamics 365 Finance szolgáltatásban lépjen a **Projektmenedzsment és könyvelés** > **Beállítás** > **Globális projektmenedzsment és könyvelési paraméterek** lehetőségre.
2. A rendelkezésre álló jogi személyek listájában válassza ki azokat az entitásokat, ahol a több szerződéssor és a Project Operations a Dynamics 365 Customer Engagement alkalmazásban funkciók engedélyezve lesznek. Hagyja ki azokat a jogi entitásokat, amelyek a Project Operations szolgáltatást készletezett/előállítási rendelési forgatókönyvek esetén használják.

> [!NOTE]
> A jogi személyek csak akkor választhatók ki, ha nincs meglévő projektjei.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektmenedzsment és könyvelési paraméterek konfigurálása

A Project Operations a Dynamics 365 Customer Engagement alkalmazásbant használó minden jogi személynek egy sor alapértelmezett paramétert kell használnia. Ezeket a paramétereket a **Project Operations** lapon kell konfigurálni, a **Projektkezelési és könyvelési paraméterek** oldalon. A paraméterek a következők:

  - **A számlázási típus alapértelmezései**: a Project Operations a számlázási típusú alapértékek rögzített halmazát használja, amelyeket le kell képeznie a Finance sortulajdonságaira. Hozzon létre egy rekordot minden egyes számlázási típushoz: **nincs megadva**, **számlázható**, **nem számlázható**, **ingyenes**, és **nem érhető el**.
  - **Projektkategória alapértelmezései**: válassza ki az alapértelmezett projektkategóriákat, amelyeket az egyes tranzakciótípusok esetén használni szeretne. Ezek az alapértelmezett értékek a **Project Operations integrációs naplóban** és azokban a becslésekben használhatók, ahol a tényleges projekthez nem adtak meg tranzakciós kategóriát.
  - **Előrejelzések**: válassza ki az idő-és költségbecslésekhez használandó előrejelzési modellt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]