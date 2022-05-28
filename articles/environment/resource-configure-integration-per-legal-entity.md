---
title: A Project Operations jogi személyenkénti integrációjának konfigurálása
description: Ez a témakör a jogi személyenkénti integráció beállításáról a Project Operations rendszerben tartalmaz tájékoztatást.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585841"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>A Project Operations jogi személyenkénti integrációjának konfigurálása 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A témakör végigvezeti a Dynamics 365 Project Operations jogi személyenkénti konfigurálásához szükséges lépésein.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Szolgáltatáskulcsok engedélyezése Dynamics 365 Finance

A szükséges funkciók engedélyezéséhez hajtsa végre az alábbi lépéseket.

1. A Dynamics 365 Finance nyissa meg a **Szolgáltatáskezelés** munkaterületet.
2. A **Funkciók listájában** keresse meg és engedélyezze a következő funkciókat:
  
    - **Több szerződéssor engedélyezése a projekthez**
    - **Projektműveletek engedélyezése Dynamics 365 Customer Engagement**

> [!NOTE]
> Ha nem látható a listában a **Funkciókulcsok** elem, ellenőrizze, hogy a Finance verziója megfelel-e a minimális verziókövetelménynek (10.0.13-as alkalmazásverzió az összes minőségi frissítéssel, vagy újabb). Válassza a **Frissítések keresése** lehetőséget a funkciólista frissítéséhez.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>A Project Operations telepítési forgatókönyvének definiálása egy jogi személyhez

A Projektműveletek jogi személy szintjén engedélyezheti a Dynamics 365 Customer Engagement. Egy jogi személy is használhatja a Project Operations on Dynamics 365 Customer Engagement-t erőforrás-/nem raktározott forgatókönyvekhez. Ugyanabban a környezetben másik jogi személy is használhatja a Project Operationst a készletezett/gyártási rendelés esetekre.

1. A Dynamics 365 Finance a **Projektmenedzsment és könyvelés** > **beállítása Globális** > **projektmenedzsment és könyvelési paraméterek című témakörben olvashat**.
2. Az elérhető jogi személyek listájában válassza ki azokat a szervezeteket, amelyekben több szerződéssor és projektművelet engedélyezve lesz Dynamics 365 Customer Engagement funkciókon. Hagyja ki azokat a jogi entitásokat, amelyek a Project Operations szolgáltatást készletezett/előállítási rendelési forgatókönyvek esetén használják.

> [!NOTE]
> A jogi személyek csak akkor választhatók ki, ha nincs meglévő projektjei.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektmenedzsment és könyvelési paraméterek konfigurálása

Minden olyan jogi személynek, aki a Project Operations on Dynamics 365 Customer Engagement használja, szüksége van egy sor alapértelmezett paraméterre. Ezeket a paramétereket a **Project Operations** lapon kell konfigurálni, a **Projektkezelési és könyvelési paraméterek** oldalon. A paraméterek a következők:

  - **A számlázási típus alapértelmezései**: a Project Operations a számlázási típusú alapértékek rögzített halmazát használja, amelyeket le kell képeznie a Finance sortulajdonságaira. Hozzon létre egy rekordot minden egyes számlázási típushoz: **nincs megadva**, **számlázható**, **nem számlázható**, **ingyenes**, és **nem érhető el**.
  - **Projektkategória alapértelmezései**: válassza ki az alapértelmezett projektkategóriákat, amelyeket az egyes tranzakciótípusok esetén használni szeretne. Ezek az alapértelmezett értékek a **Project Operations integrációs naplóban** és azokban a becslésekben használhatók, ahol a tényleges projekthez nem adtak meg tranzakciós kategóriát.
  - **Előrejelzések**: válassza ki az idő-és költségbecslésekhez használandó előrejelzési modellt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]