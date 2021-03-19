---
title: Bevételelszámolás áttekintése
description: Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278871"
---
# <a name="revenue-recognition-overview"></a>Bevételelszámolás áttekintése

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A Dynamics 365 Project Operations alkalmazásban a bevételelszámolási elvek a projekt vagy a projekt egy részének kiválasztott számlázási módszerén alapulnak. Ez a témakör információkat nyújt a bevételelszámolásról a Project Operations alkalmazásban.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Az idő és anyag számlázási módszerrel könyvelt tranzakciók

- A költség- és bevétel-elszámolás összefügg. A tranzakciós költségeket és a nem számlázott értékesítéseket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program.
- A projekt költség- és bevételi profilja határozza meg, hogy a nem számlázott értékesítési tranzakciók fel lesznek-e adva a főkönyvbe. Ha az **Elhatárolt bevétel** lehetőséget választja, a rendszer a **Folyamatban lévő munka értékesítési értéke** és az **Elhatárolt bevétel eladási érték** számlákat használja a könyvelés során. Alább egy példát lát erre a módszerre.  

  | Tranzakció típusa | Terhelés/Jóváírás | Mennyiség |
  | --- | --- | --- |
  | Folyamatban lévő termelés – értékesítési érték | Terhelés | 100 |
  | Elhatárolt bevétel értékesítési értéke | Jóváírás | 100 |

- Bevétel a számlázásnál lesz elismerve. A rendszer a feladás során a **Számlázott bevétel** számlát használja. Alább egy példát lát erre a módszerre.  

  | Tranzakció típusa | Terhelés/Jóváírás | Mennyiség |
  | --- | --- | --- |
  | Vevő egyenlege | Terhelés | 120 |
  | Fizetendő forgalmi adó | Jóváírás | 20 |
  | Számlázott bevétel | Jóváírás | 100 |

- Ha a bevétel elhatárolt volt a nem számlázott értékesítések feladásakor, a rendszer sztornírozza az elhatárolt bevételt a számlázáskor.

  | Tranzakció típusa | Terhelés/Jóváírás | Mennyiség |
  | --- | --- | --- |
  | Folyamatban lévő termelés – értékesítési érték | Jóváírás | 100 |
  | Elhatárolt bevétel értékesítési értéke | Terhelés | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>A fixáras számlázási módszerrel könyvelt tranzakciók

- A költség- és bevétel-elszámolás különállók. A tranzakciós költségeket a [Project Operations integrációs naplójában](../project-accounting/project-operations-integration-journal.md) könyveli a program. A nem számlázott értékesítési tranzakciók nem jönnek létre.
- A bevétel akkor imemrtethető el a számlázás során, ha a projekt költség- és bevételi profiljánál a **Projektkészenlét számításához használt elv** **Nem folyamatban lévő munka**. Ezt a módszert csak rövid távú, egyszerű projektekhez használja.
- A bevétel fix árbevétel-becslésekkel ismertethető fel a **Befejezett szerződés** vagy a **Készültségi százalék bevétel-felismerés** módszerrel.

## <a name="additional-resources"></a>További információforrások
[Számlázható projektek könyvelésének konfigurálása cikk](../project-accounting/configure-accounting-billable-projects.md)

[Rögzített árú bevétel becslési projektjei](rev-rec-percentage-completion-method.md)

[Bevételi becslések kezelése](rev-rec-completed-contract-method.md)

[Teljesítési költség módszerei](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]