---
title: 2022. novemberi újdonságok – A Project Operations Lite telepítés
description: Ez a cikk a Microsoft Dynamics 365 Project Operations lite központi telepítésének 2022. novemberi kiadásában elérhető minőségi frissítésekről nyújt tájékoztatást.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831145"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>2022. novemberi újdonságok – A Project Operations Lite telepítés

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Ez a cikk a következő Microsoft Dynamics 365 Project Operations összetevőkre és verziókra vonatkozik:

- Project Operations 4.58.0.119 verziójú Dataverse-környezetben


## <a name="quality-updates"></a>Minőségi frissítések

| Funkcióterület | Hivatkozási szám | Minőségi frissítés |
| --- | --- | --- |
| Számlázás és árképzés | 2781818. | A kulcs nem található hiba az anyaghasználati napló alapértelmezett árának megadásakor. |
| Számlázás és árképzés | 2922373. | Nem lehet az idézőjeles sort olyan projekthez kapcsolni, amely elveszett árajánlatként zárult le. |
| Számlázás és árképzés | 2943206. | **A Projektentitás Szerződéssor** mezőjének nem kötelezőnek kell lennie. |
| Számlázás és árképzés | 2953182. | A helyesbítő számlák hibaüzenetének javítása.|
| Számlázás és árképzés | 2959500. | Nem lehet árajánlatsort csatolni olyan projekttevékenységhez, amely már társítva van egy elveszett árajánlathoz.|
| Számlázás és árképzés | 2959560. | "Ez az ügyfél már szerepel a projektszerződésben" üzenet érkezett, miközben bizonyos helyszíneken megnyertként zárta az árajánlatot. |
| Számlázás és árképzés | 3031727. | Az erőforrás-hozzárendelések sikertelenek, és a kötelező "msdyn_Company" mező hiányzik a hibából. |
| Számlázás és árképzés | 3036905. | A tulajdonos vállalat soha nem inicializálódik a ProjectTeamMember-en. |
| Lehetőségkezelés | 2763519. | Null értékű hivatkozási hiba az EnsureProjectContractAllowsUpdates fájlban. |
| Lehetőségkezelés | 2783798. | Ha projektbecsléseket importál az árajánlati sorba, a költség- és anyagbecslésekhez hiányoznak a tevékenységleírások.|
| Lehetőségkezelés | 2988635. | Javítsa a hiba msg leírását az Ügyfél árajánlatból törlésekor. |
| Lehetőségkezelés | 3001191. | Nem lehet árajánlatot létrehozni a Lehetőségből, ha a számlázási módszer null értékként van megadva. |
| Magasabb szintre váltás | 3012324. | A projekt átalakítása sikertelen volt egy olyan projektnél, amelynek nevében olyan vezérlőkarakterek szerepeltek, mint a Tab. || Projekttervezés és nyomon követés | 2790384. | A Függőben lévő műveletkészlet időtúllépése túl rövid. |
| Projekttervezés és nyomon követés | 3044275. | Hiányzó honosítás: missingProjectSchedulerErrorMessage. |
| Projekttervezés és nyomon követés | 3044277. | A Project Recon rácsa nem töltődik be, ha az ütemező nincs beállítva.|
| Erőforráskezelés | 2943153. | Frissítse a Követés lapot, hogy két tizedesjegyet jelenítsen meg az Időtartamhoz.|
| Alvállalkozásba adás | 2932774. | A szállítói számlasor csak olvasási hibája helytelenül jelenik meg. |
| Alvállalkozásba adás | 2939556. | A szállítói számla fejlécének állapotát nem szabad Piszkozat online törlésre állítani, ha nem aktív. |
| Idő és költség | 2939998. | Vegye fel az új TESA verziót a ProjOps-ban. |
