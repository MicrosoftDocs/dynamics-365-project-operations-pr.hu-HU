---
title: Projekt-erőforrások beállítása
description: Ez a témakör információkat nyújt a projekterőforrások beállításáról vagy kéréséről.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9af71fe0638a5601ded3f0e80301ae5dfa198c1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682578"
---
# <a name="set-up-project-resources"></a>Projekt-erőforrások beállítása

[!include [banner](../includes/banner.md)]

Be kell állítania egy naptárat, és társítania kell azt egy alkalmazotthoz vagy egy dolgozóhoz. A naptár a projekt és a projekt számára fenntartott erőforrások munkaidejének ütemezésére szolgál. A naptár beállítása során a projektmenedzserek az erőforrás-optimalizálás részeként az erőforrásszintek beállítását is elvégezhetik. A naptár ütemezése alapján a korlátozások alkalmazhatók az erőforrásokon. Beállíthat egy naptárat a **Naptárak** oldalon.

Amikor egy dolgozót projekterőforrásként állít be, kiválaszthatja azokat a dolgozókat, akik annál a vállalatnál dolgoznak, amelyhez az erőforrásokat beállítja. Másik lehetőségként kiválaszthat dolgozókat a szervezete más vállalataitól is. Ezek a dolgozók vállalatközi erőforrásként is ismertek.

A következő eljárások azt ismertetik, hogyan állítható be a dolgozó projekterőforrásként a vállalatánál, és hogyan állítható be egy vállalatközi projekterőforrás.

## <a name="set-up-a-worker-as-a-project-resource"></a>Alkalmazott beállítása projekterőforrásként

1. A **Dolgozók** oldalon található **Dolgozók** listában jelölje ki a projekterőforrásként hozzáadni kívánt munkatársat, és nyissa meg a munkabejegyzést.
2. A Művelet panelen válassza a **Projekt** &gt; **Beállítás** &gt; **Projektbeállítás** lehetőséget.
3. Jelöljön ki egy naptárt, majd zárja be az oldalt.

Az erőforrás alapértelmezett projektjeit az előzetes hozzárendelés típusaként is megadhatja. Az előzetes hozzárendelések akkor is használhatók, ha az erőforrás-menedzser vagy a projektmenedzser előre tudja, hogy mely projekteken fog az erőforrás dolgozni. Az előzetes hozzárendelések a projektszponzor vagy ügyfél kérésén is alapulhatnak. Projekt előzetes hozzárendeléséhez a **Projektek hozzárendelése** oldalon a **Projektek** lap **Hátralévő projektek** listájában válassza ki a megfelelő projektet.

## <a name="set-up-an-intercompany-resource"></a>Vállalatközi erőforrás beállítása

Ha a munkatársat vállalatközi erőforrásként állítja be, akkor a kölcsönadó vállalatnál és a kölcsönvevő vállalatnál is el kell végeznie a beállítást.

### <a name="in-the-lending-company"></a>A kölcsönadó vállalatnál

1. A Pénzügy területen ellenőrizze, hogy a kölcsönző vállalat ki van-e jelölve, majd végezze el az előző, „Alkalmazott beállítása projekterőforrásként” című részben leírt eljárást.
2. A **Vállalatközi könyvelés** oldalon válassza az **Új** lehetőséget.
3. A **Jogi entitás azonosítója** mezőben válassza ki a kölcsönadó vállalatot. Töltse ki megfelelően a hátralévő mezőket, majd válassza a **Mentés** lehetőséget.
4. Az **Transzferár** oldalon válassza az **Új** lehetőséget.
5. A **Kölcsönbe vevő jogi személy** mezőben válassza ki a megfelelő vállalatot.
6. Ha csak az ennek a szakasznak a kezdetén létrehozott erőforrást kívánja kölcsönadni a kölcsönvevő vállalatnak, az **Erőforrás** mezőben jelölje ki a létrehozott erőforrás nevét. Ha a kölcsönadó vállalat összes erőforrását elérhetővé szeretné hozni a kölcsönvevő vállalat számára, akkor hagyja üresen az **Erőforrás** mezőt.
7. A **Projektmenedzsment és könyvelési paraméterek** oldal **Vállalatközi** lapján állítsa a **Vállalatközi erőforrás-ütemezés és az időnyilvántartások engedélyezése** beállítást **Igen** értékre.

### <a name="in-the-borrowing-company"></a>A kölcsönvevő vállalatnál

- Az **Erőforrások listája** oldalon a keresési szűrőben írja be a kölcsönadó vállalathoz létrehozott erőforrás nevét annak ellenőrzéséhez, hogy a név szerepel-e a kölcsönvevő vállalathoz tartozó erőforráslistában.

## <a name="request-project-resources"></a>Projekt erőforrásaira vonatkozó kérelmek
A projektek erőforrás-ütemezésére vonatkozó funkció csak az erőforrás-menedzserek számára teszi lehetővé a munkatársakkal ellátott erőforrások elosztását aktivitásokra vagy projektekre. A szolgáltatás engedélyezéséhez hajtsa végre az alábbi műveleteket, vagy ellenőrizze, hogy befejeződtek-e:

- Számsorozatok beállítása.
- Projektmenedzsment és könyvelés munkafolyamatok beállítása.
- Erőforrás-igénylési munkafolyamatok engedélyezése.

Az előző feladatok befejezését követően az alábbi műveleteket hajthatja végre szükségletei szerint:

- Erőforrás-kérelmek létrehozása egy ideiglenesen lefoglalt, munkatársakkal ellátott erőforrásból.
- Erőforráskérelmek felügyelete.
- Erőforrás-kérelmek teljesítése.
- Munkatársakkal ellátott erőforrás kérelmezése a WBS-ből.
- Erőforrások foglalása egy projekthez egy munkatársakkal ellátott erőforrásra vonatkozó kérelem nélkül.


[!INCLUDE[footer-include](../includes/footer-banner.md)]