---
title: Erőforrás-kezelési módok áttekintése
description: Ez a témakör a Dynamics 365 Project Operations Erőforráskezelés funkciójáról nyújt információkat.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279456"
---
# <a name="resource-management-modes-overview"></a>Erőforrás-kezelési módok áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A Dynamics 365 Project Operations két módot támogat a teljes foglalási folyamat végrehajtásához. A kezelési mód projektparaméterként van definiálva, és módosítható az üzleti igények változása esetén.    

## <a name="central-mode"></a>Központi mód
Azoknál a szervezeteknél, akik központosítják az erőforrások elosztását a projektek számára, a központi mód biztosítja, hogy a projektmenedzserek a projekt szintjén meghatározhatják az erőforrás-követelményeket. Az erőforrás-követelmények teljesítését egy erőforrás-kezelőre delegálja a rendszer. A projektmenedzserek elfogadhatják vagy visszautasíthatják azokat az erőforrásokat, amelyeket az erőforrás-kezelő javasolt.

![Központi mód](./media/resource-management-central.png)

Az erőforrások központi móddal való kezeléséhez lásd:

- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Erőforrás-kérelem elküldése](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Erőforrás-követelmény teljesítése](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Fogadja el vagy utasítsa el a javasolt projekt erőforrást egy erőforrás-kérésből](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibrid mód
Azoknál a szervezeteknél, akik rugalmasságot igényelnek az erőforrások elosztásában, a hibrid mód lehetővé teszi, hogy a projektmenedzserek és az erőforrás-menedzserek is tudják az erőforrásokat foglalni.

![Hibrid mód](./media/resource-management-hybrid.png)

A támogatott központi mód folyamata mellett a következő témakörök nyújtanak információkat a hibrid módban használható további támogatott foglalási folyamatokkal kapcsolatban:

Erőforrás közvetlen foglalása egy projekthez:
- [Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Erőforrás foglalása az erőforrás-követelményekből:
- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]