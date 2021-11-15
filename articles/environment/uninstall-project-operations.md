---
title: A(z) Dynamics 365 Project Operations eltávolítása
description: Ez a témakör információkat ad arról, hogyan távolítható el a Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783646"
---
# <a name="uninstall-dynamics-365-project-operations"></a>A(z) Dynamics 365 Project Operations eltávolítása 

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Az Dynamics 365 Project Operations eltávolításhoz rendszergazdai szerepkörrel kell rendelkeznie.

1. Válassza a **Beállítások** > **Megoldások** lehetőséget.

    ![Beállítások oldal.](./media/uninstall-proj-ops-solutions.png)
  
2. A megoldásokat pontosan a felsorolás sorrendjében távolítsa el. 

    | Lépés | Megoldás neve                                    | Feljegyzés                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 0 | msdyn_ProjectServiceUpgrade_managed.cab            | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 2 | ProjectOperations_Anchor                           | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 5 | ProjectService                                     | Nincsenek további megjegyzések.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Nincsenek további megjegyzések.                                                                         |
    | 7 | ProjectServiceCore                                 | Nincsenek további megjegyzések.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 9 | FieldServiceCommon                                 | Szükséges a Dynamics 365 Finance vagy a Dynamics 365 Supply Chain Management kettős írásához.   |
    | 10 | msdyn_AssetCommon                                  | Szükséges a Dynamics 365 Finance vagy a Dynamics 365 Supply Chain Management kettős írásához.   |
    | 11 | msdyn_TESA_Anchor                                  | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 12 | msdyn_TESA_Patch                                   | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 13 | msdyn_TESA                                         | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 14 | ResourceSchedulingControls                         | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | A Dynamics 365 Field Service használatához szükséges.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 19 | Dynamics365Notes                                   | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 21 | DualWriteCore                                      | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 23 | Dynamics365AssetManagement                         | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 26 | HCMCommon                                          | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 28 | Fél                                              | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 29 | Dynamics365Company                                 | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 30 | CurrencyExchangeRates                              | Ha nem található, hagyja ki ezt a megoldást.                                                            |
    | 31 | AssetCommon                                        | Ha nem található, hagyja ki ezt a megoldást.                                                            |
