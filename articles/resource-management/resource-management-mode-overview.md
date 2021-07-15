---
title: Erőforrás-kezelési módok áttekintése
description: Ez a témakör a Dynamics 365 Project Operations Erőforráskezelés funkciójáról nyújt információkat.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367894"
---
# <a name="resource-management-modes-overview"></a>Erőforrás-kezelési módok áttekintése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A Dynamics 365 Project Operations két módot támogat a teljes foglalási folyamat végrehajtásához. A kezelési mód projektparaméterként van definiálva, és módosítható az üzleti igények változása esetén.    

## <a name="central-mode"></a>Központi mód
Azoknál a szervezeteknél, akik központosítják az erőforrások elosztását a projektek számára, a központi mód biztosítja, hogy a projektmenedzserek a projekt szintjén meghatározhatják az erőforrás-követelményeket. Az erőforrás-követelmények teljesítését egy erőforrás-kezelőre delegálja a rendszer. A projektmenedzserek elfogadhatják vagy visszautasíthatják azokat az erőforrásokat, amelyeket az erőforrás-kezelő javasolt.

![Központi mód](./media/resource-management-central.png)

Az erőforrások központi móddal való kezeléséhez lásd:

- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](/dynamics365/project-service/book-named-resource)
- [Erőforrás-kérelem elküldése](/dynamics365/project-service/submit-resource-request)
- [Erőforrás-követelmény teljesítése](/dynamics365/project-service/resource-management-fulfill-requests)
- [Fogadja el vagy utasítsa el a javasolt projekt erőforrást egy erőforrás-kérésből](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibrid mód
Azoknál a szervezeteknél, akik rugalmasságot igényelnek az erőforrások elosztásában, a hibrid mód lehetővé teszi, hogy a projektmenedzserek és az erőforrás-menedzserek is tudják az erőforrásokat foglalni.

![Hibrid mód](./media/resource-management-hybrid.png)

A támogatott központi mód folyamata mellett a következő témakörök nyújtanak információkat a hibrid módban használható további támogatott foglalási folyamatokkal kapcsolatban:

Erőforrás közvetlen foglalása egy projekthez:
- [Nevesített foglalható erőforrások foglalása projektcsoporthoz, és feladatok hozzárendelése](/dynamics365/project-service/assign-named-bookable-resource)

Erőforrás foglalása az erőforrás-követelményekből:
- [Általános foglalható erőforrások hozzárendelése egy feladathoz és erőforrás-követelmények generálása](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nevesített erőforrások foglalása erőforrás-követelményekből](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]