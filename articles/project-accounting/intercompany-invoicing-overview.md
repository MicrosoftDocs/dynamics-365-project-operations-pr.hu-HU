---
title: Vállalatközi számlázás áttekintése
description: Ez a témakör információkat és példákat tartalmaz a vállalatközi számlázásról a projektekhez.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c343c5bf525574e496036793cd4e131394e8b1b471153147a66cfebe1acf3fce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005394"
---
# <a name="intercompany-invoicing-overview"></a>Vállalatközi számlázás áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Előfordulhat, hogy a szervezethez több olyan részleg, leányvállalat és más jogi személy tartozik, amelyek termékeket és szolgáltatásokat biztosítanak egymásnak a projektjeihez. Az a jogi személy, aki a szolgáltatást vagy terméket nyújtja, az úgynevezett *kölcsönadó jogi személy*. Az a jogi személy, aki a szolgáltatást vagy terméket kapja, az úgynevezett *kölcsönvevő jogi személy*.

Az alábbi ábra egy tipikus forgatókönyvet mutat be, amelyben két jogi személy, a Contoso Robotics USA (a kölcsönvevő entitás) és a Contoso Robotics UK (a kölcsönadó entitás) megosztja az erőforrásokat a projekt elkészítéséhez az Adventure works számára. Ebben az esetben a Contoso Robotics USA van megbízva a szállítással az Adventure Works számára.

![Vállalatközi számlázás.](./media/IntercompanyScenario.png) 

A Dynamics 365 Project Operations a következő folyamatot használja a vállalatközi tranzakciók feldolgozásához:

1. A kölcsönadó jogi személy vállalatközi idő- és költségtranzakciói felhasználása költségtranzakciókként úgy, hogy időt és költséget könyvelnek a kölcsönvevő jogi személy projektjeivel szemben.
2. Az idő-és költség árát a kölcsönadó vállalatnál vannak rögzítve a kölcsönvevő vállalat önköltségi árlistájával.
3. A vállalatközi számlázatlan értékesítési tranzakciók a kölcsönadó vállalatnál vannak rögzítve a kölcsönvevő vállalat önköltségi árlistájával.
4. A nem számlázott bevételeket a kölcsönvevő vállalatnál lehet nyilvántartani a projekt szerződés értékesítési árlistája segítségével. Az ügyfél részére akkor lehet számlázni, ha nem számlázott bevételt rögzítenek. Az ügyfélnek nem kell megvárnia, amíg a vállalatközi számla feldolgozása befejeződött.
5. A vállalatközi ügyfélszámlák rendszeresen létrejönnek a kölcsönadó vállalatnál. A számlák létrehozása manuálisan vagy periodikus automatizált folyamat segítségével történik. Létrehozható egyetlen számla minden egyes kölcsönvevő jogi személyhez, illetve külön számlák is létrehozhatók projekt szerint.
6. Amikor a vállalatközi ügyfélszámlát feladják a kölcsönadó jogi személyben, ez ennek megfelelő szállítói számla létrejön a kölcsönvevő jogi személynél. A függőben lévő szállítói számla költségeit a rendszer a számla könyvelésekor rögzíti a projekt alkönyvébe.

A következő ábra a vállalatközi számlázást mutatja be, ahogy az kapcsolódik könyvelési eseményekhez és a várt feladásokhoz a főkönyvbe.

![Vállalatközi folyamat.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>További információforrások

- [A vállalatközi számlázás konfigurálása](configure-intercompany-invoicing.md)
- [Vállalatközi tranzakciók rögzítése](create-intercompany-transactions.md)
- [Vállalatközi ügyfél- és szállítói számlák létrehozása](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]