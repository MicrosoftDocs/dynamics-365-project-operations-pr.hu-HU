---
title: Számlafeldolgozás áttekintése
description: A témakör a számlák Project Operations szolgáltatással való feldolgozásának áttekintését részletezi az erőforrás/nem készletezett anyagokon alapuló forgatókönyvekhez.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582713"
---
# <a name="invoicing-process-overview"></a>Számlafeldolgozás áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Project Operations erőforrás-/nem készleten alapuló forgatókönyvek átfogó lehetőségeket nyújtanak, amelyek mind a Projektmenedzser, mind a követelésügyintéző/projektkönyvelő igényeinek megfelelően testre vannak szabva. A számlázási folyamat során a Projektmenedzser kezeli a projekt számlázási elmaradását, és a követelésügyintéző/projektkönyvelő egy megfelelő és pontos számladokumentumot hoz létre az ügyfél számára.

![Számlázási folyamat ábrája.](./media/invoicing-flow.png)

A projektszerződéssor meghatározza a társított projekttranzakciók számlázási módját. Amikor a Projektmenedzser jóváhagyja az idő- és költségtranzakciókat, a rendszer rögzíti a tranzakciókat a **Projekt actuals** entitásban, és elküldi az információkat a **projektmenedzsment és a könyvelés modulnak** Dynamics 365 Finance. A Projektkönyvelő ezután a [Project Operations integrációs](../project-accounting/project-operations-integration-journal.md) napló segítségével áttekinti és közzéteszi a rekordokat. Ez a folyamat fontos könyvelési részleteket tartalmaz a projekt tényadataihoz, mint például a számlázás, az áfacsoport, a számlázási cikkek értékesítési áfacsoportja és a pénzügyi dimenziók.

A Projektmenedzser áttekintheti a számlázatlan értékesítési tranzakciókat az idő és anyag számlázási módszerrel, az [Idő és anyag számlázási elmaradás](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) lehetőségben, és a rögzített árú számlázásban a [Rögzített árú mérföldkövek](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones) lehetőségben. Ezek a nézetek lehetővé teszik a következő számlázási ciklusba bevehető tranzakciók szűrését és kiválasztását, majd **Számlázásra kész** megjelölését.

[Manuálisan is létrehozhat proforma számlát](../proforma-invoicing/create-manual-proforma-invoice.md) vagy használhatja a [periodikus folyamat](../proforma-invoicing/configure-automated-invoice-creation.md) lehetőséget is. A Projektmenedzser szükség szerint [módosíthatja a tervezet proforma számlát](../proforma-invoicing/manage-proforma-invoice.md), majd megerősítheti.

A megerősített proforma számlát elküldik a Pénzügyek **Projektmenedzsment és könyvelés** modulnak. A Projektkönyvelő formázza és frissíti a projekt számlajavaslatát, majd közzéteszi és kinyomtatja a dokumentumot. A közzétett projektszámlákat a rendszer a Főkönyvben, valamint az Ügyfél és a Projekt részfőkönyvekben rögzíti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]