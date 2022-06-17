---
title: Erőforrás-kezelési módok áttekintése
description: Ez a cikk az erőforrás-kezelési funkciókról nyújt tájékoztatást Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928435"
---
# <a name="resource-management-modes-overview"></a>Erőforrás-kezelési módok áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A Dynamics 365 Project Operations két módot támogat a teljes foglalási folyamat végrehajtásához. A kezelési mód projektparaméterként van definiálva, és módosítható az üzleti igények változása esetén.    

## <a name="central-mode"></a>Központi mód
Azoknál a szervezeteknél, akik központosítják az erőforrások elosztását a projektek számára, a központi mód biztosítja, hogy a projektmenedzserek a projekt szintjén meghatározhatják az erőforrás-követelményeket. Az erőforrás-követelmények teljesítését egy erőforrás-kezelőre delegálja a rendszer. A projektmenedzserek elfogadhatják vagy visszautasíthatják azokat az erőforrásokat, amelyeket az erőforrás-kezelő javasolt.

![Központi mód.](./media/resource-management-central.png)

Az erőforrások központi móddal való kezeléséhez lásd:

- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](/dynamics365/project-service/book-named-resource)
- [Erőforrás-kérelem elküldése](/dynamics365/project-service/submit-resource-request)
- [Erőforrás-követelmény teljesítése](/dynamics365/project-service/resource-management-fulfill-requests)
- [Fogadja el vagy utasítsa el a javasolt projekt erőforrást egy erőforrás-kérésből](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibrid mód
Azoknál a szervezeteknél, akik rugalmasságot igényelnek az erőforrások elosztásában, a hibrid mód lehetővé teszi, hogy a projektmenedzserek és az erőforrás-menedzserek is tudják az erőforrásokat foglalni.

![Hibrid mód.](./media/resource-management-hybrid.png)

A támogatott központi módú folyamaton kívül tekintse meg a következő cikkeket az összes többi támogatott foglalási folyamat hibrid módban történő kezeléséhez:

Erőforrás közvetlen foglalása egy projekthez:
- [Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése](/dynamics365/project-service/assign-named-bookable-resource)

Erőforrás foglalása az erőforrás-követelményekből:
- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]