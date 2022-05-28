---
title: Projektszerződés jóváhagyása
description: Ez a témakör a szerződések Project Operations alkalmazásban való megerősítéséről nyújt tájékoztatást.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5dab041bab1268235ed542f06d1b4b4cd240305
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599319"
---
# <a name="confirm-a-project-contract"></a>Projektszerződés jóváhagyása

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

A Dynamics 365 Project Operations projektszerződései aktívak lehet a **Megerősítve** okkal, vagy lezártak az **Elvesztett** okkal. A project-szerződések jóváhagyása esetén az állapot-frissítések **Vázlat** értékről **Aktív** értékre módosul az állapot oka pedig **Megerősítve**. Aktív vagy lezárt szerződés nem módosítható és nem nyitható meg újra. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Egy projektszerződés megerősítésének pénzügyi hatása

A projektszerződés megerősítését követően az alkalmazás a költségeket a régebbi tényleges költségadatok sztornírozásával, illetve az új tényleges költségadatok újralétrehozásával újraszámítja a költségeket. Az alkalmazás a társított projektszerződéssor számlázási módszere alapján dolgozza fel az új aktuális költségeket. Ha a tényleges költségek egy Idő és Anyag szerződéssorra hivatkoznak, akkor az alkalmazás automatikusan újra létrehozza a megfelelő, nem számlázott tényleges értékesítéseket. Ha a tényleges költség egy rögzített árú szerződéssora hivatkozik, akkor az alkalmazás leállítja a tényleges költségek újrafeldolgozását.

A nem meghaladandó korlátok, számlázhatóság beállítása és az árképzés és költségek a tényadatokon értékelve lesznek, majd frissítve a megerősítési folyamat részeként.

## <a name="close-a-project-contract-as-lost"></a>Projektszerződés lezárása befejezettként

Ha elveszettként zár le egy projektszerződést, a szerződés állapota **Lezárva** értékre módosul, és a állapot oka **Elveszett** lesz. A projekt szerződés írásvédett lesz. Egymegerősítő párbeszédpanel jelenik meg a változtatások végrehajtása előtt, mert a lezárt projektek nem nyithatók meg újra.

Ha az elveszettként lezárt projektszerződés a soraiban egy projektre hivatkozik, akkor azt a projektet is lezártként jelöli meg. Az ettől a naptól a függőben lévő összes erőforrás-foglalás visszavonásra kerül. A program sztornírozza a szerződésben szereplő, még nem számlázott tényleges értékesítéseket.

> [!NOTE]
> A Dynamics 365 Project Operations alkalmazásban a projektszerződés elvesztettként való lezárása nem befolyásolja a társított lehetőség állapotát. A lehetőség nyitva marad, és kézzel kell le zárni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]