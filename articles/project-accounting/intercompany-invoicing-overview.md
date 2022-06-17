---
title: Vállalatközi számlázás áttekintése
description: Ez a cikk a projekteket érintő vállalatközi számlázással kapcsolatos információkat és példákat tartalmaz.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913577"
---
# <a name="intercompany-invoicing-overview"></a>Vállalatközi számlázás áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Előfordulhat, hogy a szervezethez több olyan részleg, leányvállalat és más jogi személy tartozik, amelyek termékeket és szolgáltatásokat biztosítanak egymásnak a projektjeihez. Az a jogi személy, aki a szolgáltatást vagy terméket nyújtja, az úgynevezett *kölcsönadó jogi személy*. Az a jogi személy, aki a szolgáltatást vagy terméket kapja, az úgynevezett *kölcsönvevő jogi személy*.

A következő ábra egy tipikus forgatókönyvet mutat be, ahol két jogi személy, a Contoso Robotics USA (a kölcsönvevő jogi személy) és a Contoso Robotics UK (a kölcsönvevő jogi személy) erőforrásokat oszt meg az ügyfélnek, a Kalandorboltnak. Ebben az esetben a Contoso Robotics USA szerződést kötött egy munka szállítására az Adventure Works számára.

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