---
title: Vállalatközi ügyfél- és szállítói számlák létrehozása
description: Ez a témakör a vállalatközi vevői és szállítói létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9448cb29adb4206efaabe3f313a1f619cd32b9be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591499"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Vállalatközi ügyfél- és szállítói számlák létrehozása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A kölcsönadó jogi entitásban a projekt könyvelője létrehoz egy vállalatközi ügyfélszámlát a projektköltségekhez, amelyek át lesznek adva a kölcsönvevő jogi személynek. A vállalatközi vevői számla jóváhagyása és feladása után a kölcsönadó jogi személy elküldi a vállalatközi számlát a kölcsönvevő jogi személynek.

A kölcsönadó jogi személy projektkönyvelője beállíthat egy kötegelt folyamatot, amellyel a vállalatközi számlákat ismétlődő módon lehet létrehozni. A projekt könyvelője határozza meg a feltételeket, például konkrét projekteket, amelyekhez a vállalatközi számlákat kötegelve hozza létre.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Vállalatközi vevői számla manuális létrehozása a projekttranzakciókhoz 

Ezt a folyamatot használhatja vállalatközi vevői számla manuális létrehozására a projekttranzakciókhoz. Órák keresése, amelyeket olyan munkások adtak fel, amelyek a kölcsönvevő jogi személy projektjein dolgoztak, és amelyeket az Ön jogi személye számolt el a kölcsönvevő jogi személy nevében. Kereshet a jogi személy neve, a projekt szerződésszáma, a projektszám, dátumtartomány vagy ezek bármely kombinációja alapján. A keresési eredmények között jelölje ki a vállalatközi számlához adandó tranzakciókat. 

A kölcsönbeadó jogi személyben a következő lépéseket kell végrehajtani. 

1. A Dynamics 365 Finance a Projektmenedzsment és könyvelés **projektszámlák** > **Vállalatközi vevői számlák című témakörben talál** > **helyet**. A **Vállalatközi vevői számlák** listaoldalán, a műveleti ablaktáblán válassza az **Új** lehetőséget.
2. A **Vállalatközi számla létrehozása** oldal **Jogi személy** mezőjében jelöljön ki egy kölcsönvevő jogi személyt.
3. Nem kötelező: Adja meg a specifikus projektszerződést és projektszámot.
4. Szűkítse a keresést egy dátumtartomány kiválasztásával. Adja meg a **Kezdődátum** és a **Záró dátum** mezőben az adott dátumokat. A keresési eredményekben csak azok a vállalatközi tranzakciók jelennek meg, amelyek a dátumtartományban lettek feladva.
5. Állítsa **Projekt összetett naplósor-paranéter** beállítást **Igen** értékre , és válassza a **Keresés** lehetőséget.
6. A keresési eredmények között jelölje ki a vállalatközi számlajavaslat részeként szerepeltetni kívánt tranzakciókat, majd kattintson az **OK** gombra.
7. A **Vállalatközi vevői számla** lapon a keresési eredményekből kiválasztott vállalatközi projekttranzakciók jelennek meg. Ha módosítani szeretné a tranzakciókat, mielőtt elküldi a számlát a kölcsönvevő jogi entitásnak, tegye a következőket:
  
    1. A **Vállalatközi vevői számla** lapon nyissa meg a számla adatait, majd válassza a **Sor hozzáadása** lehetőséget.
    2. Sor eltávolításához jelölje ki, majd válassza az **Eltávolítás** lehetőséget.
    3. Megjegyzések, okok, pénzügyi dimenziók és egyéb információk megtekintése a számlasor adatainak kiválasztott sorával kapcsolatban.
    
8. A vállalatközi vevői számla feladásához, a műveleti ablaktáblán válassza a **Feladás** lehetőséget.

> [!NOTE]
> Ha a szervezet megköveteli, hogy a vállalatközi számlákat a feladás előtt ellenőrizzék, a rendszergazda beállíthat egy munkafolyamatot a vállalatközi számlákhoz. Ha nincs munkafolyamat beállítva a vállalatközi számlákhoz, akkor feladhatja a vállalatközi számlát.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>A vállalatközi számlákhoz tartozó kötegelt feladat létrehozása

Egyszerre több vállalatközi számlát is létrehozhat a kölcsönvevő jogi személyek részére. A keresési funkció segítségével például megkeresheti a kölcsönvett munkavállalók által fealdott és más jogi személyek által kezelt projektekhez kapcsolódó összes tranzakciót. Ezután minden egyes kölcsönvevő jogi személyhez létrehozhat egy vállalatközi számlát a keresési eredményekben megadott tranzakciókhoz.

1. Válassza a **Projektvezetés és könyvelés** > **Időszakos** > **Projektszámlák** > **Vállalatközi vevői számlák létrehozása** lehetőséget.
2. A **Vállalatközi számlék létrehozása** oldal **Vállalat** mezőjében jelöljön ki egy jogi személyt, akinek számláz. Ha nem jelöl ki vállalatot, a keresési feltételeknek megfelelő összes tranzakció megjelenik az összes kölcsönvevő jogi személy esetében.
3. A **Számla létrehozása ez alapján** mezőben válassza ki, hogy a vállalatközi tranzakciók számláját projekt vagy egy kölcsönvevő jogi személy alapján szeretné-e létrehozni.
4. Nem kötelező: Adott projekt-és projekt-szerződés kiválasztásához a vállalatközi számlák létrehozásához kattintson a **Kijelölés** gombra. A **Lekérdezés** lapon a **Feltételek** mezőben jelölje ki a projektszerződést, a projektszámot vagy mindkettőt, majd válassza az **OK** lehetőséget.
5. A **Köteg** lapon állítson be egy kötegelt feldolgozást, amellyel a vállalatközi számlákat ismétlődő módon hozza létre. További tájékoztatás a [Kötegelt feldolgozási munka beküldése egy űrlapról](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form) című témakörben olvasható.
6. A vállalatközi számlák feladásához, a műveleti ablaktáblán válassza a **Feladás** lehetőséget.

> [!NOTE]
> Ha a szervezet megköveteli, hogy a vállalatközi számlákat a feladás előtt ellenőrizzék, a rendszergazda beállíthat egy munkafolyamatot a vállalatközi számlákhoz. Ha nincs munkafolyamat beállítva a vállalatközi számlákhoz, akkor feladhatja a vállalatközi számlákat.

## <a name="post-the-intercompany-vendor-invoice"></a>A vállalatközi szállítói számla feladása

A kölcsönvevő entitásban a projekt könyvelője áttekintheti a vállalatközi függőben lévő számlákat a megfelelő vállalatközi ügyfél-számla feladásakor. A Fininace-ben a kölcsönvevő jogi entitásban nyissa meg a **Kinnlévőségek** > **Számlák** > **Függőben lévő szállítói számla** lehetőséget. A függőben lévő számla száma megegyezik a vállalatközi ügyfél számlaszámával. Ellenőrizze, hogy a számla helyes-e, majd adja fel a számlát. A vállalatközi szállítói számla könyvelésekor létrehoz egy projekt alkönyvet és egy főkönyvi tranzakciót, amely tükrözi a kölcsönvevő jogiszemélynél megjelenő tranzakciós költségeket.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
