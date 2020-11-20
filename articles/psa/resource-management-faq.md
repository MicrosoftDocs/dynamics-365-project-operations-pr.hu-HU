---
title: Erőforrás-kezelési GYIK
description: Ez a témakör válaszokat ad az erőforrás-kezeléssel kapcsolatos gyakran feltett kérdésekre.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120141"
---
# <a name="resource-management-faq"></a>Erőforrás-kezelési GYIK

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Mi a különbség a csapat tagja és az erőforrás igény között?

A projektcsoport tagjai hozzárendelhetők a feladatokhoz, lefoglalhatók vagy túlfoglalva, és jóváhagyóként állíthatók be. Erőforrásigény létezhet egy projektcsoport tagja nélkül, a keresletjegyzet tervezeteként. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Mi a különbség a javasolt és a puha foglalású órák között?

A javasolt órák és a puha foglalású órák eltérnek a láthatóságtól. A javasolt órák csak azoknak az erőforrás-kezelőknek és a projektmenedzsernek láthatók, akik erőforrás-igénylés alapján kezdeményezték a keresletet. A nem lefoglalt órák mindenki számára láthatóak, akik hozzáférhetnek az Ütemezési táblához.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Hogyan láthatom a csoport erőforrásainak puhán lekötött óráit?

A puha foglalást akkor lehet elvégezni, amikor egy erőforrás-igényt foglal le. Azok a források, amelyeket egy projektcsapatnál lefoglalnak, olyan csapattagként jelennek meg, akiknek kevés a lefoglalása. Megjelennek az Ütemezési táblán.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Hogyan változtathatom meg a lefoglalt erőforrás (általános vagy megnevezett) szükséges óráit, valamint a kezdési és befejezési dátumát?

Az erőforrások lefoglalása után válassza ki a **Foglalások karbantartása** elemet a szükséges módosítások elvégzéséhez.

## <a name="what-resources-types-does-project-service-automation-support"></a>Milyen erőforrás-típusokat támogat a Project Service Automation?

**Felhasználó** és **Kapcsolat** az egyetlen erőforrás típusok támogatottak a Dynamics 365 Project Service Automation rendszerben. Bár lehet létrehozni más típusú erőforrások (például **Berendezések** és **Csoport**), nincs end-to-end használat támogatva.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Mi a különbség a megbízás és a foglalás között?

A hozzárendelések az erőforrások hozzárendelése a projekt feladataihoz a projekt ütemtervében. Az erőforrások lehetnek valós vagy általános erőforrások. A foglalások a források nehéz vagy puha elosztása egy projekthez. A kemény foglalások felhasználják az erőforrás kapacitását. Ideális esetben a valós források esetében a foglalásoknak és a feladatoknak egyezniük kell, mert nem különböznek egymástól. A PSA azonban nem hajtja végre ezt a megállapodást. Az egyeztetés nézet egy projektmenedzser helyét mutatja, ahol az erőforrás foglalása és feladatai nem egyeznek meg.
