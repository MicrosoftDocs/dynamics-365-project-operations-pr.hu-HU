---
title: Költségkezelés integrációja
description: Ez témakör a Project Operations felületen a költségjelentések kettős írással történő integrációjáról nyújt tájékoztatást.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585795"
---
# <a name="expense-management-integration"></a>Költségkezelés integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez témakör a Project Operations felületen a költségjelentések kettős írással történő [teljes költségkihelyezéséről](../expense/expense-overview.md) nyújt tájékoztatást.

## <a name="expense-categories"></a>Költségkategóriák

A teljes költség-üzembe helyezés során költségkategóriákat hoz létre és tart fenn a Pénzügy és műveletek alkalmazásban. Új költségkategória létrehozásához hajtsa végre a következő lépéseket:

1. A(z) Microsoft Dataverse-ben hozzon létre egy **Tranzakció** kategóriát. A kettős írású integráció szinkronizálja ezt a tranzakciókategóriát a Pénzügy és műveletek alkalmazásokkal. További információ: [Projektkategóriák konfigurálása](/dynamics365/project-operations/project-accounting/configure-project-categories) és [Project Operations beállítása és konfigurációs adatintegráció](resource-dual-write-setup-integration.md). Ennek az integrációnak az eredményeként a rendszer négy megosztott kategóriarekordot hoz létre a Finance and Operations alkalmazásokban.
2. A Pénzügyekben lépjen a **Költségkezelés** > **Beállítás** > **Megosztott kategóriák**, és válasszon egy megosztott kategóriát a **Költség** tranzakciós osztállyal. Állítsa a **Költségben használható** paramétert **Igaz** értékre, és határozza meg a használni kívánt költségtípust.
3. Ezzel a megosztott kategóriarekord használatával hozzon létre egy új költségkategóriát a **Költségkezelés** > **Beállítás** > **Költségkategóriák** pontra lépéssel, és az **Új** lehetőség kiválasztásával. A rekord mentésekor a kettős írás a **Project Operations integrációs projekt költségkategóriáinak exportáló entitása (msdyn \_expensecategories)** táblaleképezést használja a rekord Dataverse elemmel való szinkronizálásához: .

  ![Költségkategóriák integrációja.](./media/DW6ExpenseCategories.png)

A Pénzügy és műveletek alkalmazások költségkategóriái vállalat- vagy jogi személyspecifikusak. Külön, megfelelő jogiszemély-specifikus nyilvántartások vannak a(z) Dataverse felületen. Amikor egy projektmenedzser megbecsüli a költségeket, nem választhatja ki azokat a költségkategóriákat, amelyeket egy másik vállalat tulajdonában lévő projekthez hoztak létre, mint az a vállalat, amely az éppen kidolgozás alatt lévő projekt tulajdonosa. 

## <a name="expense-reports"></a>Költségjelentések

A költségjelentések a Pénzügy és műveletek alkalmazásban jönnek létre és kerülnek jóváhagyásra. További információt a [Költségjelentések létrehozása és feldolgozása a(z) Dynamics 365 Project Operations felületen](/learn/modules/create-process-expense-reports/) című lapban talál. Miután a projektmenedzser jóváhagyta a költségjelentést, az felkerült a főkönyvbe. A Project Operations felületen a projekttel kapcsolatos költségjelentési sorok feladása speciális könyvelési szabályok alkalmazásával történik:

  - A projekttel kapcsolatos költségek (beleértve a vissza nem térítendő adót is) nem kerülnek azonnal projektköltség-számlára a főkönyvben, hanem a költségintegrációs számlára kerülnek. Ez a fiók a **Projektkezelés és könyvelés** > **Beállítás** > **Projektkezelés és könyvelés paraméterei**, **Project Operations a Dynamics 365 Customer engagement felületen** lapon van beállítva.
  - A kettős írás szinkronizálása a(z) Dataverse elemmel a **Project Operations integrációs projektköltségeket exportáló entitás (msdyn \_expenses)** táblaleképezés használatával.
  - Az adózói alkönyv, a szállítói alkönyv és egyéb pénzügyi könyvelések a költségelszámolás könyvelésekor kerülnek rögzítésre.

  ![Költségjelentések integrálása.](./media/DW6ExpenseReports.png)

Ha egy rekordot írnak a **Költség** entitásba a(z) Dataverse felületen, a rendszer elindítja a rekord automatikus jóváhagyási folyamatát. Szükség esetén az automatizált jóváhagyási folyamat állapota a(z) Dataverse felületen a **Kifejlett beállítások** > **Rendszer** > **Rendszeres munkák** pontban ellenőrizhető. A jóváhagyás befejezése után a költségtranzakció osztályrekordjai létrejönnek a **Tényleges adatok** entitásban.

A költséggel kapcsolatos tényleges adatok feldolgozása ezt követően a **Project Operations integrációja tényleges adataival (msdyn\_actuals)** kettős írású táblaleképezés segítségével történik. További tudnivalókért lásd: [Projektbecslések és Tényleges adatok](resource-dual-write-estimates-actuals.md).

Az **Importálás az előkészítésből** időszakos folyamat költségjelentéssel kapcsolatos naplósorokat hoz létre a Project Operations integrációs naplójában. Az ellentételezési számla nem teljesít a költségintegrációs számlán. A Könyvelés integrációs napló törli a költségtranzakció számlaegyenlegét, és a költségösszeget a projekt költségszámlájára helyezi át. A rendszer projekt alprogram-tranzakciókat is létrehoz a későbbi számlázási és bevétel-felismerési célokra.
