---
title: A Project Operations Dataverse alkalmazás manuális telepítése kettős írási támogatással
description: A témakör ismerteti, hogyan lehet manuálisan telepíteni a Project Operations Dataverse alkalmazást, hogy támogassa a kettős írást.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591223"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>A Project Operations Dataverse alkalmazás manuális telepítése kettős írási támogatással

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A témakör ismerteti, hogyan lehet manuálisan telepíteni a Microsoft Dynamics 365 Project Operations alkalmazást a Microsoft Dataverse rendszerbe, hogy támogassa a kettős írást. A Project Operations észleli a környezet konfigurációját, és további támogatást nyújt a kettős íráshoz, ha teljesülnek az előfeltételek.

Az Microsoft Dynamics Lifecycle Services (LCS) szolgáltatáson keresztüli telepítés esetén, ha követi a témakör útmutatását, kihagyhatja a Microsoft Power Platform integráció (korábban Common Data Service környezet) telepítését.

A Project Operations Dataverse-környezetbe kettős írás támogatással való telepítésének folyamata a következő négy fő lépésből áll:

1. [Hozzon létre egy új környezetet a Dataverse-ben, amely támogatja a kettős írást](#create).
2. [A kettős írás előfeltételeinek megvalósítása a környezetben](#prerequisites).
3. [Adja hozzá a Project Operations Dataverse alkalmazást](#dataverse).
4. [Saját környezetek társítása](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Hozzon létre egy új környezetet a Dataverse-ben, amely támogatja a kettős írást

A művelet befejezéséhez rendszergazdaként kell bejelentkeznie.

1. Nyissa meg [Power Platform felügyeleti központot](https://admin.powerplatform.com), és jelentkezzen be rendszergazdaként.
2. Hozzon léter egy új környezetet, és nevezze el.
3. Válassza ki a környezet típusát. Ha regisztrált a próbaverziós ajánlatra, válassza a **Próbaverzió (előfizetés alapú)** lehetőséget.
4. Erősítse meg a telepítési régiót.
5. Engedélyezze az **Adatbázis létrehozása ehhez a környezethez** beállítást. 
6. Erősítse meg a nyelvet, majd ellenőrizze, hogy a pénznem megegyezik-e a Pénzügy és műveletek alkalmazás pénznemével.
7. Engedélyezze a **Dynamics 365 alkalmazások** beállítást, és győződjön meg arról, hogy az **Automatikusan telepítse ezeket az alkalmazásokat** mező beállítása **Nincs**.
8. Adjon hozzá egy biztonsági csoportot, ha szükséges biztonsági csoport.
9. Válassza ki a **Mentés** gombot a környezet létrehozásához.
10. Várja meg, amíg befejeződik a telepítés, és a környezet eléri a **Kész** állapotot.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>A kettős írás előfeltételeinek megvalósítása a környezetben

A kettős írás támogatása további mezőket tartalmaz, amelyek hozzá vannak adva vannak a kulcsentitásokhoz, például a **Vállalat** entitáshoz. Ha meglévő környezethez kettős írási támogatást ad hozzá, előfordulhat, hogy frissítenie kell az adatokat a támogatás engedélyezéséhez. Az adatokkal inicializálásával információkért lásd: [Cégadatok inicializálása](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). A kettős írású írásról a [Kettős írásúrendszerkövetelményei](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req) oldalon található további tájékoztatás.

Végezze el ezt az eljárást, hogy megteremtse a kettős írás előfeltételeit a környezetében.

1. Nyissa meg az előbb létrehozott környezetet, majd válassza az **Erőforrás** \> **Dynamics 365 alkalmazások** lehetőséget.
2. Válassza az alkalmazáslistában a **Kettős írás alapmegoldás** lehetőséget, és telepítse azt.
3. Várja meg, amíg befejeződik a telepítés. Válassza az alkalmazáslistában a **Kettős írás vezénylési megoldás** lehetőséget, és telepítse azt.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>A Project Operations Dataverse alkalmazás hozzáadása

Ezt az eljárást csak akkor tudja végrehajtani, ha a Project Operations telepítése előtt befejezte az előző eljárásokat. A telepítés során a rendszer elemzi a környezet konfigurációját, és szükség esetén hozzáadja a kettős írást.

1. Nyissa meg az előzőleg létrehozott környezetet, majd válassza az **Erőforrás** \> **Dynamics 365 alkalmazások** lehetőséget.
2. Válassza ki a **Microsoft Dynamics 365 Project Operations** elemet az alkalmazáslistában, és telepítse azt.

## <a name="link-your-environments"></a><a name="link"></a>Saját környezetek társítása

Dataverse A környezet üzembe helyezése után beállíthatja a hivatkozást a Pénzügy és műveletek alkalmazásban. Kövesse a [Kettős írású varázsló használata a környezetek összekapcsoláshoz](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment) rész lépéseit.
