---
title: Költségbejegyzés (Lite)
description: Ez a cikk a költségbejegyzések Lite telepítésben történő használatának módjával kapcsolatos információkat tartalmaz.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917947"
---
# <a name="expense-entry-lite"></a>Költségbejegyzés (Lite)

_**Érvényesség:** Lite telepítés – ajánlattól proforma számlázásig_

Az alapszintű vagy a Lite költségkezelés az egyszerű kiadások rögzítésének képessége. A projektek költségeit rögzítheti egy projekthez, majd a projekt jóváhagyója áttekinti és jóváhagyja azokat.

A Dynamics 365 Project Operations költségképeségeivel kapcsolatos további információk a következő témakörben találhatók: [Költségek áttekintése](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Alapköltség rögzítése

A költségeket rögzítheti, így elküldheti azokat a jóváhagyónak.

1. Lépjen a **Kiadások** pontra, és válassza az **Új** lehetőséget.
2. Az **Új kiadás** lapon adja meg a szükséges költséginformációkat, majd kattintson a **Mentés** gombra.

## <a name="submit-a-basic-expense"></a>Alapköltség elküldése

Miután befejezte az összes kiadás rögzítését, és készen áll a jóváhagyásra, el kell küldenie azokat.

1. Lépjen a **Kiadások** pontra, és válasszon egy kiadást. Másik lehetőségként jelölje ki az összes kiadást a fejlécen lévő jelölőnégyzet használatával.
2. Válassza a **Küldés** lehetőséget. A rendszer feldolgozza a kijelölt bejegyzéseket, majd létrehozza a költségjóváhagyási kérelmeket.

## <a name="add-an-attachment"></a>Melléklet hozzáadása

Előfordulhat, hogy a jóváhagyónak további dokumentációt kell biztosítania az Ön költségére vonatkozóan. A költségbejegyzése idővonalában elismervényt csatolhat. Válassza a **Szerkesztés** lehetőséget, majd az **Idősor** szakaszban jelölje ki a gemkapocs ikont a nyugta csatolásához.

## <a name="recall-a-basic-expense"></a>Alapköltség visszahívása

Amikor tévedésből küld el egy kiadást, visszahívhatja azt. A költségbejegyzés visszahívásához szükséges idő a jóváhagyási fázisától függ.  Ha a jóváhagyó még nem hagyta jóvá a bejegyzést, akkor a visszahívás azonnal megtörténhet. Ha azonban a bejegyzést már jóváhagyták, a jóváhagyónak jóvá kell hagynia a visszahívást, és vissza kell fordítania a tranzakciókat.

1. Nyissa meg a **Kiadások** pontot, majd a kiadások listájában válassza ki a visszahívni kívánt kiadást.
2. Válassza az **Előhívás** lehetőséget. Ha a költségbejegyzést még nem hagyták jóvá, a rendszer azonnal visszahívja. Ha a költségbejegyzést már jóváhagyták, a rendszer egy visszahívási kérést hoz létre, amely értesíti a jóváhagyót, hogy sztornírozza a kiadást. A jóváhagyó ezután megerősíti, hogy a sztornírozás megtehető, és a tétel visszakerül a rendszerbe.

## <a name="delete-a-basic-expense"></a>Alapköltség törlése

A még el nem küldött kiadások törölhetők. Ha már elküldött kiadást szeretne törölni, akkor először vissza kell hívnia.

## <a name="see-also"></a>Kapcsolódó információk

- [Jóváhagyások áttekintése](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]