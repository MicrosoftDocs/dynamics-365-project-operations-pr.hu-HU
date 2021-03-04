---
title: Időbevitel felhasználói felületének viselkedése
description: Ez a témakör az időbevitel felhasználói felületének viselkedéséről nyújt információkat.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124506"
---
# <a name="time-entry-ui-behavior"></a>Időbevitel felhasználói felületének viselkedése

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


A **Heti időbevitel** rács egy egyéni vezérlőelem, amely két fő részből áll: **Dimenziók** és **Időtartam**.

## <a name="dimensions"></a>Dimenziók
A **Dimenziók** szakasz az összes olyan dimenziót mutatja, amelyre az idő megadható. A következő dimenziók támogatottak gyárilag:

  - Project
  - Projektfeladat
  - Szerepkör
  - Típus szerint
  - Bejegyzés állapota

A **Dimenziók** szakasz nem engedi meg a sorszerkesztést. Ezt a részt egy olyan nézet támogatja, amely lehetővé teszi az egyedi mezők hozzáadását a heti időbeviteli rácshoz.

## <a name="duration"></a>Időtartam
Az Időtartam szakasz a hét napjait mutatja oszlopfejlécként. Ez a szakasz lehetővé teszi a sorszerkesztést. Miután létrehozott egy időbeviteli sort, amely rendelkezik megfelelő dimenziókkal, a felhasználók gyorsan bevihetik az ezen dimenziókra fordított időt.

## <a name="create-a-new-time-entry"></a>Új időbejegyzés létrehozása

1. Az időbeviteli rácsban válassza az **Új** lehetőséget. 
2. Az **Időbevitel gyors létrehozása** párbeszédpanelen válassza ki az időbevitel dátumát.
3. Adja meg a **Projekt**, a **Projektfeladat**, a **Szerepkör** és az **Időtartam** dimenziók adatait. Ezt az információt percben, órában vagy napban kell megadni, a **h**, **m** vagy **d** értéket együtt megadva a számmal. 
4. Adjon meg egy leírást a bevitelhez, és tetszőleges megjegyzéseket, amelyek külsőleg megoszthatók az időbevitelre vonatkozóan. 

Amikor menti a bejegyzést, a beírt értékek megjelennek a **Dimenziók** részben. Az **Időtartam** mezőbe beírt információk abban az időpontban jelennek meg, amelyre az időbejegyzés létrejött.

A keresési mezőket rendszernézetek támogatják. Például, miután egy felhasználó belépett egy projektbe, a **Projektfeladat** mező alapértelmezés szerint **Másolat** nézetre van állítva. Felhasználóhoz nem rendelt feladatokhoz időbejegyzések létrehozásához válassza a **Nézet módosítása** elemet a keresési párbeszédablakban, és válassza ki az **Összes aktív projektfeladat** nézetet.

## <a name="edit-a-time-entry"></a>Időbejegyzés szerkesztése 
Az időbeviteli oldal egyes mezőinek, például a **Leírás** és a **Külső megjegyzések** részletei nem jelennek meg a heti időbeviteli rácsban. Ehelyett egy kis háromszögmutató jelenik meg az **Időtartam** cellákban, amelyek rendelkeznek ezekkel a további részletekkel. 

1. Az időbevitel módosításához jelölje ki a frissíteni kívánt cellát az időbejegyzésben.
2. Válassza a **Részletek szerkesztése** lehetőséget az adatoknak a **Fő időbeviteli űrlap** ablaktáblában történő frissítéséhez. 

## <a name="copy-a-time-entry-row"></a>Időbeviteli sor másolása
A sor létrehozása után a választhatja a **Sor másolása** lehetőséget az egész sort egy új sorra másolásához. Ha egy sort ilyen módon másolnak, akkor a dimenziókat és az időtartamokat is lemásolják. Választhatja a **Sor szerkesztése** elemet is, hogy a dimenzióértékeket és időtartamokat frissítse az **Időtartam** szakaszban.

## <a name="open-a-time-entry-behavior"></a>Időbeviteli viselkedés megnyitása
Az optimális és gyors bevitel támogatására a legszembetűnőbb mezőkben a heti időbeviteli rács a kiválasztott dimenziók és időtartamok egy részhalmazát mutatja. Az egy bejegyzés összes részletének megtekintéséhez a **Bejegyzés szerkesztése** válassza a **Megnyitás** lehetőséget.

## <a name="submit-a-time-entry"></a>Időbejegyzés beküldése
Egyetlen időbejegyzést vagy időbejegyzéscsoportot nyújthat be, kiválasztva a cellák egy tömbjét vagy egy teljes időbeviteli sort, majd a **Küldés** menüpontot használva. A benyújtott időbejegyzések olyan bejegyzésekként jelennek meg, amelyek jóváhagyásra várnak a jóváhagyók **Jóváhagyás** oldalán. Az időbejegyzések sikeres benyújtás után nem szerkeszthetők.

## <a name="recall-a-time-entry"></a>Időpont előhívása
Előhívhatja a benyújtott időbejegyzéseket. Előhívhat egyetlen időbejegyzést, időbejegyzés-blokkot vagy az időbejegyzések egész sorát. A visszahívott időbevitelek szerkeszthetők.

## <a name="time-entry-status"></a>Időbejegyzés állapota

- **Vázlat**: Az új időbevitelek automatikusan **Vázlat** státuszt kapnak. Csak a **Vázlat** állapotú időbejegyzéseket lehet törölni.
- **Beküldve**: Időbevitel benyújtásakor az állapot frissül **Beküldve** értékre. 
- **Jóváhagyott**: Amikor a benyújtott időbejegyzés jóváhagyásra kerül, az állapot frissül **Jóváhagyott** értékre. 
- **Visszaadott**: Ha egy időbejegyzés elutasításra kerül, az állapot frissül **Visszaadott** értékre, és a bejegyzés javításra és újbóli elküldésre rendelkezésre áll. 

## <a name="view-rejection-comments"></a>Az elutasító megjegyzések megtekintése
Ha egy jóváhagyó elutasítja az időbejegyzést, a jóváhagyó megjegyzéseket fűzhet hozzá, hogy segítse az erőforrást az elutasítás okának megértésében. Az időbejegyzés elutasító megjegyzéseinek megtekintéséhez válassza a **Bejegyzés megnyitása** lehetőséget. Az elutasító megjegyzések megjelennek az idővonalban. A felhasználó a bejegyzés újbóli elküldése előtt válaszolhat az elutasítási megjegyzésekre.

## <a name="copy-week"></a>Hét másolása
Néhány bejegyzés létrehozása után a felhasználók egyszerre több időbejegyzést is létrehozhatnak.

1. Az **Időbejegyzések** űrlapon válassza a **Hét másolása** elemet a további időbejegyzések tömeges létrehozásához. 
2. Az **Időszak kezdete** rész **Másolás** párbeszédpanelén használja a **Kezdő dátum** és **Záró dátum** mezőket a dátumtartomány meghatározására, ahonnan másolni szeretné az időbejegyzéseket. 
3. Az **Időszak vége** szakaszban, a **Kezdő dátum** mezőben adja meg a dátumot, ahova időbejegyzéseket szeretne létrehozni. 
4. Válassza a **Másolás** lehetőséget. A **Záró időszak** részben megadott dátumra elkészül a **Kezdő időszak** részben a hét megfelelő napjára vonatkozó időbejegyzések másolata. Például a múlt hét hétfői időbejegyzését annak a hétnek a hétfőjére másolják, amelyet **Záró időszak** elemként adtak meg.

## <a name="import"></a>Importálás
Ugyanazt az alapvető eljárást használják a foglalásokból, megbízásokból és cserékből történő importáláshoz. Meghatározhatja az dátumtartományt, amelyből a foglalások importálásra kerülnek, majd kifejezetten kiválaszthatja azokat a foglalásokat, amelyeket vázlat időbejegyzésekbe kell másolni. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]