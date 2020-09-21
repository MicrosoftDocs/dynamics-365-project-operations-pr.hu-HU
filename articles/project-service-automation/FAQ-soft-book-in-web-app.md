---
title: Hogyan lehet „ideiglenesen lefoglalni” az erőforrásokat az alkalmazás 2.x verziójában?
description: Ez a cikk ismerteti, hogyan lehet „ideiglenesen lefoglalni” projektcsoport-tagokat a Project Service használatával.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752236"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Hogyan lehet „ideiglenesen lefoglalni” az erőforrásokat a webes alkalmazásban (Project Service alkalmazás 2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Feltételesen ütemezhetők vagy „ideiglenesen lefoglalhatók” erőforrások egy projektcsoport számára annak a megjelenítéséhez, hogy erőforrásokat tervez hozzárendelni egy projekthez. Az ideiglenes foglalás nem használja fel az erőforrás rendelkezésre álló kapacitását. Ideiglenesen lefoglalt csoporttagok nem rendelhetők projektfeladatokhoz. A feladatokhoz csak olyan erőforrások rendelhetők, amelyeknek az állapota végleges lefoglalás, a véglegesítési típusa pedig véglegesített (feltéve, hogy rendelkezik elegendő végleges lefoglalási órával a feladat elvégzéséhez).

Ideiglenesen lefoglalt projekt csoporttagok a Csoporttag rácsban az ideiglenesen lefoglalt munkaóráikkal jelennek meg az Ideiglenesen lefoglalt oszlopban. Az ütemezési táblán is megjelennek. Ismét, nem jeleznek kapacitásfelhasználást, mert az ideiglenes lefoglalás nem használja fel az erőforrás kapacitását.

A Project Service 2.x verziójával három módon foglalhatók le ideiglenesen csoporttagok egy projekthez. Ideiglenes lefoglalás történhet az ütemezési tábla használatával, a foglalások karbantartása szolgáltatással, vagy általános erőforrás létrehozásával. A módszerek az alábbiakban találhatók.

## <a name="soft-book-with-the-schedule-board"></a>Ideiglenesen lefoglalás az ütemezési táblával

Ideiglenesen lefoglaláshoz az ütemezési táblával, hajtsa végre ezt: 
1. Ütemezési tábla megnyitása.
2. Az ütemezési tábla alsó, Foglalási követelmények panelén válassza a Projekt lapot.
3. Keresse meg a projektet, amelyhez ideiglenesen le akarja foglalni az erőforrást. Kattintson a Projekt oszlop fejlécére, majd használhatja a szűrőt a projekt megkereséséhez, ha sok projektje van.
4. Kattintson a projektre, majd húzza és ejtse az erőforrás időrácsára.
5. Megjelenik az erőforrás-foglalások létrehozása panel a jobb oldalon. Módosítsa a kezdő és befejező dátumot, válassza ki a Foglalás állapotának az Ideiglenes, és állítása be az órákat. 
6. Kattintson a Lefoglalásra.
7. A projektben ezt követően az erőforrás most már a csoport tagjaként jelenik meg, az ideiglenesen lefoglalt munkaóráikkal jelennek meg az Ideiglenesen lefoglalt oszlopban.

Megjegyzés: nem rendelhet őket feladatokhoz a munkalebontási struktúrában (WBS), mert az erőforrásnak véglegesen lefoglaltnak kell lennie a csapathoz a hozzárendeléshez.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Ideiglenes lefoglalás a foglalások karbantartása szolgáltatással

Ideiglenes lefoglaláshoz a foglalások karbantartása szolgáltatással, hajtsa végre ezt:
1. A csoporttag rácson kattintson az Új elemre.
2. Jelölje ki a foglalható erőforrást, szerepkört, kezdő és befejező dátumokat.
3. Adja meg a foglalási módszert, ami nem lehet Nincs:
- Teljes kapacitás
- Kapacitás százalékos értéke
- Óránként felosztás egyenlően
- Órák lefoglalása minél hamarabb
4. Kattintson a Mentés gombra. Az erőforrás megjelenik a csapatrácsban, az órái pedig Véglegesek.
5. Az erőforrás lefoglalásainak karbantartásához kattintson Lefoglalások karbantartására.
6. Az ütemezés tábla megnyílásakor bontsa ki az erőforrást a foglalások megjelenítéséhez. A lefoglalás Végleges állapotúként jelenik meg.
7. Kattintson a jobb gombbal a Lefoglalásra, az állapot módosítása alatt válassza az Ideiglenes lefoglalás, majd az Ideiglenes lehetőséget. A foglalási állapot most már Ideiglenes.
8. Az ütemezési tábla bezárása után láthatja, az erőforrás munkaórái Véglegesről Ideiglenesre változtak csoport tagja rácson.
Megjegyzés: ha véglegesen foglal le egy erőforrást egy csoporthoz, és feladatokat rendel hozzá az WBS-ben, amikor a lefoglalások karbantartását használja az állapot átállítására Véglegesről Ideiglenesre, eltávolítja a hozzárendeléseket a feladatokról az erőforrásnál, mert csak a véglegesen lefoglalt erőforrások rendelhetők hozzá feladatokhoz.

## <a name="soft-book-by-creating-a-generic-resource"></a>Ideiglenes lefoglalás általános erőforrás létrehozásával

Létrehozhat egy ideiglenes foglalást egy általános erőforrás-csoport tag létrehozásával, ütemezési tábla vagy erőforrás-kérés teljesítéssel, és a foglalás során a típus megváltoztatásával.
Ehhez kövesse az alábbi eljárást:

1. A projekt WBS-ben szerepkörök hozzárendelése a feladatokhoz, amelyekhez általános csoporttagokat szeretne generálni.
2. Kattintson a Projektcsoport létrehozása elemre.
3. A projektcsoporttag rácson jelölje ki az általános erőforrást, majd kattintson a Lefoglalásra.
4. Az ütemezési táblán válassza ki a lefoglalni kívánt erőforrást.
5. Az ütemezési tábla erőforrás-foglalások létrehozása paneljén állítsa a foglalás állapotát Ideiglenesre.
6. Kattintson a Lefoglalás vagy Lefoglalás és kilépés elemre.

Miután bezárja az Ütemezés táblát, látni fogja, hogy a kiválasztott erőforrás hozzá lett adva a csoporthoz Ideiglenesen elfoglalt órákka, valamint a hozzárendelt órákkal. Azt is látni fogja, hogy az általános erőforrás továbbra is a csapat tagja, azt jelezve, hogy a feladatok egy ideiglenesen lefoglalt csoporttaghoz vannak rendelve.

Amikor készen áll módosítani az ideiglenesen lefoglalt csoporttag erőforrást végleges csoporttaggá, hogy feladatokat lehessen hozzárendelni, tegye a következőket:

1. Válassza ki az erőforrást, majd kattintson a foglalások karbantartása elemre.
2. Az ütemezés tábla megnyílásakor bontsa ki az erőforrást a foglalások megjelenítéséhez. A lefoglalás Ideiglenes állapotúként jelenik meg.
3. Kattintson a jobb gombbal a Lefoglalásra, az állapot módosítása alatt válassza a Végleges lefoglalás, majd a Végleges lehetőséget. A foglalási állapot most már Végleges.
4. Az ütemezési tábla bezárása után láthatja, az erőforrás munkaórái Ideiglenesről Véglegesre változtak csoport tagja rácson. Most már hozzárendelheti az erőforrást feladatokhoz (feltéve, hogy a végleges órák és hozzárendelésre váró feladat munkaórái között igazítás van). Vegye figyelembe, hogy ha a fenti 3. lehetőség általános erőforrás teljesítése lépéseit követte, amikor módosítja az ideiglenesen foglalható erőforrás állapotát véglegesre, az általános csoporttag törlődik a csoportból.
